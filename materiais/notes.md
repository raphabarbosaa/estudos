# Estruturas de Dados Python ✨

---

## 🟢 LISTAS

🔧 CARACTERÍSTICAS
│
├── Ordenadas ✅
└── Mutáveis ✅

📝 DECLARAÇÃO
┌─────────────────────────────────────┐
│ lista = [] │ vazia │
│ lista = [1, "Python", 2] │ cheia │
└─────────────────────────────────────┘

🔍 ACESSO (índice começa em 0)
┌──────────────────────────────┐
│ lista → 1 (primeiro) │
│ lista → 2 (terceiro) │
└──────────────────────────────┘

✏️ MODIFICAÇÃO
┌─────────────────────────────────────┐
│ lista = "alterado" │ direto! │
└─────────────────────────────────────┘

⚙️ MÉTODOS PRINCIPAIS
┌─────────────────────────────────────┐
│ append('item') → final │
│ insert(0, 'item') → posição │
└─────────────────────────────────────┘

text

---

## 🔵 TUPLAS

🔧 CARACTERÍSTICAS
│
├── Ordenadas ✅
└── Imutáveis ❌ (fixas!)

📝 DECLARAÇÃO
┌─────────────────────────────────────┐
│ tupla = (1, "Python", 2) │ única! │
└─────────────────────────────────────┘

🔍 ACESSO (índice começa em 0)
┌──────────────────────────────┐
│ tupla → 1 (primeiro) │
│ tupla → 2 (terceiro) │
└──────────────────────────────┘

🚫 NÃO PODE MODIFICAR
┌─────────────────────────────────────┐
│ tupla = "novo" → ERRO! │
└─────────────────────────────────────┘

text

---

## 🟡 DICIONÁRIOS

🔧 CARACTERÍSTICAS
│
├── Ordenados (Python 3.7+) ✅
├── Mutáveis ✅
└── Pares chave:valor 🔑

📝 DECLARAÇÃO
┌─────────────────────────────────────────────┐
│ dict = {} │ vazio │
│ dict = {"nome": "Raphael"} │ cheio │
└─────────────────────────────────────────────┘

🔍 ACESSO (pela CHAVE)
┌─────────────────────────────────────┐
│ dict["nome"] → "Raphael" │
└─────────────────────────────────────┘

✏️ ADICIONAR/MODIFICAR
┌─────────────────────────────────────┐
│ dict["idade"] = 30 │ direto! │
└─────────────────────────────────────┘

🗑️ REMOVER
┌─────────────────────────────────────┐
│ dict.pop("idade") │ remove │
└─────────────────────────────────────┘

⚙️ MÉTODOS PRINCIPAIS
┌─────────────────────────────────────┐
│ keys() → todas chaves │
│ values() → todos valores │
│ items() → pares chave/valor │
└─────────────────────────────────────┘

text

---

## 🟣 SETS

🔧 CARACTERÍSTICAS
│
├── Não ordenados ❌
├── Mutáveis ✅
├── Únicos ✅ (sem duplicatas!)
└── Não indexados ❌

📝 DECLARAÇÃO
┌─────────────────────────────────────┐
│ meu_set = set() │ vazio │
│ meu_set = {1, 2, 3} │ único! │
└─────────────────────────────────────┘

🔍 NÃO TEM ACESSO POR ÍNDICE
┌─────────────────────────────────────┐
│ meu_set → ERRO! │
└─────────────────────────────────────┘

⚙️ OPERAÇÕES MATEMÁTICAS
┌─────────────────────────────────────┐
│ set1 | set2 → união │
│ set1 & set2 → intersecção │
│ set1 - set2 → diferença │
└─────────────────────────────────────┘

💡 EXEMPLO PRÁTICO
┌─────────────────────────────────────┐
│ set1 = {1,2,3}, set2 = {3,4,5} │
│ set1 | set2 → {1,2,3,4,5} │
└─────────────────────────────────────┘

text

---
## 📊 RESUMO VISUAL RÁPIDO

| TIPO          | ORDENADA | MUTÁVEL | ÚNICOS   | ACESSO    | EXEMPLO      |
|---------------|----------|---------|----------|-----------|--------------|
| **🟢 LISTA**  | ✅       | ✅      | ❌       | `[0]`    | `[1,2,3]`   |
| **🔵 TUPLA**  | ✅       | ❌      | ❌       | `[0]`    | `(1,2,3)`   |
| **🟡 DICIONÁRIO** | ✅*  | ✅      | ✅chaves | `["nome"]`| `{"n":"R"}` |
| **🟣 SET**    | ❌       | ✅      | ✅       | nenhum   | `{1,2,3}`   |

_*Python 3.7+_


Nesta aula, aprendemos:

O que é um banco de dados e suas funções principais.
As diferenças entre bancos de dados relacionais (SQL) e não relacionais (NoSQL).
A estrutura de tabelas, chaves primárias e estrangeiras em bancos de dados relacionais.
A flexibilidade estrutural dos bancos de dados não relacionais em formato de chave-valor.
O uso de SQLite em Python para operações básicas com tabelas.
O uso de PyMongo para manipulação de documentos em bancos não relacionais.
Análise comparativa dos contextos de uso das abordagens relacionais e não relacionais.

Nesta aula, aprendemos:

O que é o SQLite e como ele permite manipular bancos de dados relacionais sem servidor.
A usar comandos SQL básicos: CREATE TABLE, INSERT INTO, SELECT, UPDATE, DELETE e JOIN.
A criar e conectar-se a um banco de dados SQLite usando sqlite3.connect.
A definir tabelas com tipos de dados apropriados e utilizar chaves primárias e estrangeiras.
A inserir dados em tabelas protegendo contra injeções de SQL.
A consultar e ler dados de tabelas usando SELECT e cursor.fetchall().
A atualizar dados de forma segura usando UPDATE com condições WHERE.
A confirmar alterações no banco de dados com commit() e utilizar close() para encerrar conexões.

 Uma API REST é uma Application Programming Interface (Interface de Programação de Aplicações), que permite a comunicação entre sistemas. O REST, por sua vez, significa Representational State Transfer (Transferência de Estado Representacional). Trata-se de uma arquitetura, uma padronização de como transferimos dados entre sistemas. A API REST utiliza métodos HTTP.

Já podemos ter ouvido falar dos métodos GET, POST, PUT, DELETE, entre outros, que utilizam endpoints. O que são endpoints? São URLs que esperam ou devolvem algum tipo de informação. No caso das APIs REST, geralmente, elas devolvem arquivos .json, dicionários, entre outros formatos.


# 📝 Strings em Python - Resumo Rápido

---

## 🎯 O que são Strings?
**Sequências de caracteres** para representar texto:
```python
# Aspas simples/duplas
mensagem = 'Olá, mundo!'
mensagem = "Python é incrível!"

# Aspas triplas (multilinha)
texto = """Linha 1
Linha 2
Linha 3"""
🔧 Métodos Essenciais
text
┌─────────────────┬─────────────────────────────────────┐
│   MÉTODO        │              FUNÇÃO                 │
├─────────────────┼─────────────────────────────────────┤
│ strip()         │ Remove espaços início/fim           │
│ lower()         │ Tudo minúsculo                     │
│ upper()         │ Tudo maiúsculo                     │
│ replace()       │ Substitui substring                 │
└─────────────────┴─────────────────────────────────────┘
Exemplos:

python
" exemplo ".strip()     # "exemplo"
"EXEMPLO".lower()       # "exemplo"
"exemplo".upper()       # "EXEMPLO"
"Olá Mundo".replace("Mundo", "Python")  # "Olá Python"
✨ f-Strings (Formatação)
python
nome = "Raphael"
nota = 10
mensagem = f"{nome} tirou nota {nota}!"
# "Raphael tirou nota 10!"
📍 Indexação & Slicing
text
🔍 INDEXAÇÃO (começa em 0)
┌──────────────────────────────┐
│ texto = "Python"             │
│ texto  → "P"  (primeiro)  │
│ texto  → "n"  (último)    │[5]
│ texto[-1] → "n"  (do final)  │
└──────────────────────────────┘

✂️ SLICING [início:fim:passo]
┌──────────────────────────────┐
│ texto[1:4]   → "yth"         │
│ texto[:3]    → "Pyt"         │
│ texto[::2]   → "Pto"         │
└──────────────────────────────┘
✅ Verificações Rápidas
Método	Função	Exemplo
in	Verifica se substring existe	"Py" in texto
startswith()	Começa com...?	texto.startswith("Py")
endswith()	Termina com...?	texto.endswith("on")
Exemplos:

python
texto = "Python"
"Py" in texto              # True
texto.startswith("Py")     # True
texto.endswith("on")       # True
📊 RESUMO VISUAL
text
┌─────────────────────┬─────────────────────────────────────┐
│     CONCEITO        │            EXEMPLO PRÁTICO          │
├─────────────────────┼─────────────────────────────────────┤
│ Declaração          │ 'texto' ou """multilinha"""        │
│ Limpeza             │ .strip() → remove espaços          │
│ Case                │ .lower() / .upper()                │
│ Substituição        │ .replace("antigo", "novo")         │
│ Formatação          │ f"Nome: {nome}, Nota: {nota}"      │
│ Acesso caractere    │ texto ou texto[-1]              │
│ Fatiar string       │ texto[1:4] ou texto[::2]           │
│ Verificar           │ "Py" in texto / startswith()       │
└─────────────────────┴─────────────────────────────────────┘


# 🔍 Regex (Expressões Regulares) em Python - Resumo Rápido

---

## 🎯 O que são Regex?
**Padrões para busca/validação** complexa em strings (e-mails, telefones, etc.)

**Módulo:** `import re`

---

## 🛠️ Elementos Essenciais

### 1. Caracteres Especiais
┌────────────┬─────────────────────────────────────┐
│ SÍMBOLO │ CORRESPONDE │
├────────────┼─────────────────────────────────────┤
│ . │ Qualquer caractere (exceto \n) │
│ \d │ Dígito [0-9] │
│ \D │ Não-dígito │
│ \w │ Alfanumérico + _ │
│ \s │ Espaço em branco │
└────────────┴─────────────────────────────────────┘

text

### 2. Classes de Caracteres `[ ]`
┌────────────┬─────────────────────────────────────┐
│ PADRÃO │ CORRESPONDE │
├────────────┼─────────────────────────────────────┤
│ [abc] │ a OU b OU c │
│ [^abc] │ NÃO a, b ou c │
│ [a-z] │ Letras minúsculas │
│ [0-9] │ Dígitos │
└────────────┴─────────────────────────────────────┘

text

### 3. Quantificadores
┌────────────┬─────────────────────────────────────┐
│ SÍMBOLO │ QUANTIDADE │
├────────────┼─────────────────────────────────────┤
│ * │ 0 ou mais │
│ + │ 1 ou mais │
│ ? │ 0 ou 1 │
│ {n} │ Exatamente n vezes │
│ {n,} │ n ou mais │
│ {n,m} │ Entre n e m vezes │
└────────────┴─────────────────────────────────────┘

text

---

## 📱 Exemplos Práticos

TELEFONE: 
\d
2
\d2 \s \d{4,5} - \d{4}
│ │ │ │ │ │
│ │ │ │ └─ 4 dígitos finais
│ │ │ └─ 4 ou 5 dígitos
│ │ └─ espaço
│ └─ 2 dígitos DDD
└─ parênteses escapados

DATA: \b \d{2} / \d{2} / \d{4} \b
EMAIL: [a-zA-Z0-9._%+-]+ @ [a-zA-Z0-9.-]+ . [a-zA-Z]{2,}

text

---

## ⚙️ Métodos do Módulo `re`

| Método     | Função                              | Exemplo                          |
|------------|-------------------------------------|----------------------------------|
| `search()` | Busca **primeira** ocorrência       | `re.search(r"\d+", texto)`      |
| `match()`  | Verifica **início** da string       | `re.match(r"abc", texto)`       |
| `findall()`| Retorna **todas** em lista         | `re.findall(r"\d+", texto)`     |
| `sub()`    | **Substitui** padrão                | `re.sub(r"\d", "#", texto)`     |
| `group()`  | Extrai o **match** encontrado       | `resultado.group()`             |

---

## 💻 Exemplo Completo (Email)
```python
import re

texto = "Contato: support@example.com"
padrao = r'[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}'

resultado = re.search(padrao, texto)
if resultado:
    print("Email:", resultado.group())  # "support@example.com"
📊 RESUMO VISUAL
text
┌─────────────────────┬─────────────────────────────────────┐
│      REGEX          │            PYTHON                   │
├─────────────────────┼─────────────────────────────────────┤
│ \d{2}              │ Dois dígitos (00-99)               │
│ [a-z]+             │ Uma ou + letras minúsculas         │
│ \w+@\w+\.\w+       │ Email básico                       │
│ \d{4,5}-\d{4}      │ Telefone 4/5 dígitos - 4 dígitos  │
└─────────────────────┴─────────────────────────────────────┘

🔍 TESTE: regex101.com (ferramenta online gratuita!)