# ⚙️ Funções, Lambdas & Closures em Python ✨

---

## 🔴 FUNÇÕES BÁSICAS
🔧 CARACTERÍSTICAS
│
├── Reutilizáveis ✅
├── Parâmetros flexíveis ✅
└── Escopo local (variáveis só existem dentro)

📝 SINTAXE
┌─────────────────────────────────────┐
│ def nome(parametros): │
│ # código │
│ return valor │
└─────────────────────────────────────┘

💡 PARÂMETROS PADRÃO
┌─────────────────────────────────────┐
│ def cumprimentar(nome="Visitante"):│
└─────────────────────────────────────┘

text

**Exemplo:**
```python
def ola_mundo(nome):
    return f"Olá, {nome}!"

def somar(a, b):
    return a + b
```

---

## 🟢 FUNÇÕES BUILT-IN
🏗️ PRONTAS NO PYTHON (sem import)

┌────────────────────┬─────────────────────────────────────┐
│ CATEGORIA │ EXEMPLOS │
├────────────────────┼─────────────────────────────────────┤
│ Interação │ print(), input() │
│ Inspeção │ type(), len(), isinstance() │
│ Conversão │ str(), int(), float(), list() │
│ Matemática │ abs(), round(), max(), sum() │
│ Iteráveis │ map(), filter(), zip(), sorted() │
└────────────────────┴─────────────────────────────────────┘

text

**Exemplos:**
```python
len("Python")                    # 6
max(3, 5, 1)                     # 5
list(map(lambda x: x*2, )) #[1][2][3][4][5]
```

---

## 🔵 FUNÇÕES RECURSIVAS
🔄 CHAMA A SI MESMA + CONDIÇÃO DE PARADA

📝 PADRÃO
┌─────────────────────────────────────┐
│ def fatorial(n): │
│ if n == 0: │
│ return 1 │
│ return n * fatorial(n-1) │
└─────────────────────────────────────┘

text

**Exemplo:**
```python
def fatorial(n):
    if n == 0:
        return 1
    return n * fatorial(n - 1)

fatorial(5)  # 120
```

---

## 🟡 LAMBDAS (Anônimas)
λ FUNÇÃO DE 1 LINHA SEM NOME

📝 SINTAXE
┌─────────────────────────────────────┐
│ lambda args: expressao │
└─────────────────────────────────────┘

🎯 USO COM MAP/FILTER/SORTED
┌─────────────────────────────────────┐
│ map(lambda x: x*2, ) │

│ filter(lambda x: x>2, ) │

└─────────────────────────────────────┘

text

**Exemplos:**
```python
soma = lambda a, b: a + b
list(filter(lambda x: x > 2, ))  #[4][1][2][3]
```

---

## 🟣 CLOSURES (Função Interna)
📦 FUNÇÃO QUE "LEMBRA" VARIÁVEIS EXTERNAS

📝 PADRÃO
┌─────────────────────────────────────┐
│ def externa(n): │
│ def interna(x): │
│ return x * n │
│ return interna │
└─────────────────────────────────────┘

text

**Exemplo:**
```python
def multiplicador(n):
    def multiplica(x):
        return x * n
    return multiplica

triplo = multiplicador(3)
triplo(5)  # 15
```

---

## 📊 RESUMO VISUAL RÁPIDO

| TIPO              | SINTAXE              | QUANDO USAR                  |
|-------------------|----------------------|------------------------------|
| **🔴 Básicas**    | `def func():`       | Lógica reutilizável          |
| **🟢 Built-in**   | `len()`, `map()`    | Funções prontas do Python    |
| **🔵 Recursivas** | `func(n-1)`         | Problemas que se repetem     |
| **🟡 Lambda**     | `lambda x: x*2`     | Operações simples inline     |
| **🟣 Closure**    | Função dentro função| Encapsular lógica/estado     |

---
