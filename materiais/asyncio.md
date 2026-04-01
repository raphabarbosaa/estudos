# Programação assíncrona com `asyncio`

Este projeto apresenta os conceitos básicos de programação assíncrona em Python utilizando a biblioteca padrão `asyncio`. O foco é mostrar como corrotinas, tasks e futures permitem executar várias operações de forma concorrente sem bloquear o programa.

## O que é `asyncio`?

`asyncio` é a biblioteca padrão do Python para escrever código concorrente usando a sintaxe `async`/`await`, muito utilizada para chamadas de API, acesso a arquivos e bancos de dados e criação de servidores e bots que lidam com múltiplas conexões simultâneas.[web:2]

## Awaitables

Awaitables (aguardáveis) são objetos que podem ser “esperados” com `await`. Há três tipos principais:

- Corrotinas (funções declaradas com `async def`, que podem ser pausadas e retomadas).
- Tasks (objetos que executam corrotinas de forma concorrente).
- Futures (valores que ainda serão definidos no futuro, geralmente usados em APIs de baixo nível).

## Corrotinas (`coroutines`)

- Uma corrotina é uma função assíncrona declarada com `async def`.
- Ao usar `await` dentro dela, a execução é pausada para que o event loop possa rodar outras tarefas.
- Para rodar a corrotina principal em um script, utilizamos `asyncio.run(minha_corrotina())`.

Exemplo simples:

```python
import asyncio

async def corrotina():
    print("Início.")
    await asyncio.sleep(2)
    print("Fim.")

asyncio.run(corrotina())
```

## Tasks

- Tasks permitem executar várias corrotinas em concorrência.
- São criadas com `asyncio.create_task(corrotina())` e depois aguardadas com `await`.

```python
import asyncio

async def corrotina(numero):
    print(f"Iniciando tarefa {numero}.")
    await asyncio.sleep(2)
    print(f"Tarefa {numero} concluída!")

async def main():
    tarefa1 = asyncio.create_task(corrotina(1))
    tarefa2 = asyncio.create_task(corrotina(2))
    await tarefa1
    await tarefa2

asyncio.run(main())
```

Nesse caso, as duas tarefas são iniciadas quase ao mesmo tempo e executadas de forma concorrente.

## Futures

- `asyncio.Future` representa um valor que ainda não está disponível.
- Uma corrotina pode receber um `Future`, fazer algum processamento assíncrono e, ao final, definir o resultado com `future.set_result(...)`.
- Outra corrotina pode aguardar esse mesmo `Future` com `await futuro`, desbloqueando apenas quando o resultado estiver pronto.

Isso é útil quando uma tarefa depende explicitamente do resultado de outra.

## Executando múltiplas tasks com `gather`

- `asyncio.gather()` permite aguardar várias corrotinas ao mesmo tempo, retornando quando todas forem concluídas.

```python
import asyncio

async def tarefa(numero):
    print(f"Iniciando tarefa {numero}.")
    await asyncio.sleep(2)
    print(f"Tarefa {numero} concluída!")

async def main():
    await asyncio.gather(
        tarefa(1),
        tarefa(2),
        tarefa(3),
    )

asyncio.run(main())
```

As três tarefas são iniciadas juntas; cada uma termina no seu próprio tempo, sem bloqueio sequencial.

## Comparando com o modelo síncrono

- No modelo síncrono, funções como `time.sleep()` bloqueiam a execução, fazendo as tarefas rodarem estritamente em sequência.
- No modelo assíncrono, `await asyncio.sleep()` apenas cede o controle ao event loop, permitindo que outras tarefas avancem enquanto uma está aguardando E/S ou tempo.

## Referência

Para mais detalhes e APIs avançadas, consulte a documentação oficial do `asyncio` em Python (em português):  
https://docs.python.org/pt-br/3/library/asyncio.html