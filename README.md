# 📘 Dicionário de Python

**Estudante:** André Ricardo Schultz  
**Disciplina:** Lógica de Programação
**Linguagem:** Python

## Sumário

1. [Entrada e saída de dados](#1-entrada-e-saída-de-dados)
2. [Variáveis e tipos de dados](#2-variáveis-e-tipos-de-dados)
3. [Operadores](#3-operadores)
4. [Estruturas condicionais](#4-estruturas-condicionais)
5. [Estruturas de repetição](#5-estruturas-de-repetição)
6. [Manipulação de números](#6-manipulação-de-números)
7. [Manipulação de strings](#7-manipulação-de-strings)
8. [Manipulação de listas](#8-manipulação-de-listas)
9. [Tuplas, conjuntos e dicionários](#9-tuplas-conjuntos-e-dicionários)
10. [Funções](#10-funções)
11. [Manipulação de arquivos](#11-manipulação-de-arquivos)
12. [Tratamento de exceções](#12-tratamento-de-exceções)
13. [Bibliotecas úteis](#13-bibliotecas-úteis)

---

## 1. Entrada e saída de dados

### `print()`

Exibe informações na tela.

```python
nome = "André"
print("Olá,", nome)
```

**Saída:** `Olá, André`

### `input()`

Permite receber informações digitadas pelo usuário. O valor retornado é uma string.

```python
nome = input("Digite seu nome: ")
print(f"Bem-vindo, {nome}!")
```

### `int()`

Converte um valor compatível para um número inteiro.

```python
idade = int(input("Digite sua idade: "))
print(idade + 1)
```

### `float()`

Converte um valor compatível para um número decimal.

```python
preco = float(input("Digite o preço: "))
print(preco)
```

### `sep` e `end`

O parâmetro `sep` define o separador entre valores, enquanto `end` define o que será colocado ao final da impressão.

```python
print("2026", "10", "16", sep="-")
print("Olá", end=" ")
print("mundo!")
```

**Saída:**
```text
2026-10-16
Olá mundo!
```

## 2. Variáveis e tipos de dados

### Variáveis

Armazenam valores que podem ser utilizados e modificados durante a execução do programa.

```python
nome = "André"
idade = 17
altura = 1.75

print(nome)
print(idade)
print(altura)
```

### Armazenamento em linha

Suportam mais de um valor em uma única linha de entrada, sendo a quantidade conhecida ou não.

```python
a, b = map(int, input().split()) #quantidade conhecida. Ex: 2 (a e b)

vetor = list(map(int, input().split())) #quantidade desconhecida. Ex: N valores
```

### Tipos de dados

| Tipo | Descrição | Exemplo |
|---|---|---|
| `int` | Números inteiros | `idade = 17` |
| `float` | Números decimais | `altura = 1.75` |
| `str` | Textos | `nome = "André"` |
| `bool` | Valores lógicos | `aprovado = True` |
| `list` | Lista de elementos | `notas = [8, 9, 10]` |
| `tuple` | Coleção imutável | `coordenadas = (10, 20)` |
| `dict` | Pares de chave e valor | `aluno = {"nome": "Ana"}` |
| `set` | Elementos únicos | `numeros = {1, 2, 3}` |
| `NoneType` | Ausência de valor | `resultado = None` |

### `type()`

Retorna o tipo de uma variável ou valor.

```python
idade = 17
print(type(idade))
```

**Saída:** `<class 'int'>`

### Conversão de tipos

As funções `int()`, `float()`, `str()` e `bool()` convertem valores entre tipos compatíveis.

```python
numero = 10

print(str(numero))
print(float(numero))
```

### Operador de atribuição `=`

Atribui um valor a uma variável.

```python
saldo = 100
saldo = saldo + 50

print(saldo)
```

**Saída:** `150`

## 3. Operadores

### Operadores aritméticos

Realizam operações matemáticas.

| Operador | Finalidade | Exemplo | Resultado |
|---|---|---|---|
| `+` | Adição | `5 + 3` | `8` |
| `-` | Subtração | `5 - 3` | `2` |
| `*` | Multiplicação | `5 * 3` | `15` |
| `/` | Divisão | `5 / 2` | `2.5` |
| `//` | Divisão inteira | `5 // 2` | `2` |
| `%` | Resto da divisão | `5 % 2` | `1` |
| `**` | Potenciação | `2 ** 3` | `8` |

```python
numero = 10

print(numero + 5)
print(numero * 2)
print(numero % 3)
print(numero ** 2)
```

### Operadores de comparação

Comparam valores e retornam `True` ou `False`.

| Operador | Finalidade |
|---|---|
| `==` | Igual a |
| `!=` | Diferente de |
| `>` | Maior que |
| `<` | Menor que |
| `>=` | Maior ou igual a |
| `<=` | Menor ou igual a |

```python
idade = 18

print(idade >= 18)
print(idade == 18)
print(idade < 18)
```

### Operadores lógicos

Combinam ou invertem condições.

- `and`: ambas as condições precisam ser verdadeiras.
- `or`: pelo menos uma condição precisa ser verdadeira.
- `not`: inverte o valor lógico.

```python
idade = 20
possui_documento = True

print(idade >= 18 and possui_documento)
print(idade < 18 or possui_documento)
print(not possui_documento)
```

### Operadores de atribuição composta

Permitem atualizar o valor de uma variável.

| Operador | Exemplo |
|---|---|
| `+=` | `x += 5` |
| `-=` | `x -= 5` |
| `*=` | `x *= 2` |
| `/=` | `x /= 2` |
| `//=` | `x //= 2` |
| `%=` | `x %= 3` |
| `**=` | `x **= 2` |

```python
saldo = 100
saldo += 50
saldo -= 20

print(saldo)
```

**Saída:** `130`

### Operadores de identidade e pertencimento

- `is` e `is not`: verificam se duas referências apontam para o mesmo objeto.
- `in` e `not in`: verificam se um elemento pertence a uma coleção ou sequência.

```python
frutas = ["maçã", "banana", "uva"]

print("banana" in frutas)
print("laranja" not in frutas)

valor = None
print(valor is None)
```

## 4. Estruturas condicionais

### `if`

Executa um bloco quando uma condição é verdadeira.

```python
idade = 18

if idade >= 18:
    print("Maior de idade")
```

### `else`

Executa um bloco alternativo quando a condição do `if` é falsa.

```python
idade = 16

if idade >= 18:
    print("Maior de idade")
else:
    print("Menor de idade")
```

### `elif`

Verifica condições adicionais quando as anteriores são falsas.

```python
nota = 7

if nota >= 9:
    print("Excelente")
elif nota >= 7:
    print("Aprovado")
else:
    print("Recuperação")
```

### Condicionais aninhadas

São estruturas condicionais colocadas dentro de outras estruturas condicionais.

```python
idade = 20
possui_ingresso = True

if idade >= 18:
    if possui_ingresso:
        print("Entrada permitida")
    else:
        print("Ingresso necessário")
else:
    print("Entrada não permitida")
```

### Operador condicional em uma linha

Permite escolher um valor de acordo com uma condição.

```python
idade = 20
situacao = "Maior de idade" if idade >= 18 else "Menor de idade"

print(situacao)
```

## 5. Estruturas de repetição

### `for`

Percorre os elementos de uma sequência ou coleção.

```python
frutas = ["maçã", "banana", "uva"]

for fruta in frutas:
    print(fruta)
```

### `range()`

Gera uma sequência de números, normalmente utilizada com `for`.

```python
for numero in range(1, 6):
    print(numero)
```

**Saída:** números de `1` até `5`.

### `while`

Repete um bloco enquanto uma condição for verdadeira.

```python
contador = 1

while contador <= 5:
    print(contador)
    contador += 1
```

### `break`

Interrompe o laço de repetição.

```python
for numero in range(1, 10):
    if numero == 5:
        break
    print(numero)
```

### `continue`

Pula a iteração atual e passa para a próxima.

```python
for numero in range(1, 6):
    if numero == 3:
        continue
    print(numero)
```

### `pass`

Não executa nenhuma ação e pode ser utilizado como marcador para código que será implementado posteriormente.

```python
def futura_funcao():
    pass

print("Programa executado")
```

### `enumerate()`

Permite percorrer uma sequência obtendo o índice e o valor de cada elemento.

```python
nomes = ["Ana", "Pedro", "Lucas"]

for indice, nome in enumerate(nomes):
    print(indice, nome)
```

### `zip()`

Combina elementos de duas ou mais sequências.

```python
nomes = ["Ana", "Pedro"]
notas = [9, 8]

for nome, nota in zip(nomes, notas):
    print(f"{nome}: {nota}")
```

## 6. Manipulação de números

### `abs()`

Retorna o valor absoluto de um número.

```python
print(abs(-15))
```

**Resultado:** `15`

### `round()`

Arredonda um número para a quantidade de casas decimais indicada.

```python
print(round(3.14159, 2))
```

**Resultado:** `3.14`

### `min()` e `max()`

Retornam o menor e o maior valor, respectivamente.

```python
numeros = [10, 5, 20, 8]

print(min(numeros))
print(max(numeros))
```

### `sum()`

Soma os elementos de uma coleção numérica.

```python
notas = [7, 8, 9]
print(sum(notas))
```

**Resultado:** `24`

### `divmod()`

Retorna uma tupla com o quociente inteiro e o resto da divisão.

```python
print(divmod(17, 5))
```

**Resultado:** `(3, 2)`

### `math.sqrt()`

Calcula a raiz quadrada de um número.

```python
import math

print(math.sqrt(81))
```

**Resultado:** `9.0`

### `math.ceil()` e `math.floor()`

Arredondam um número para cima ou para baixo, respectivamente.

```python
import math

print(math.ceil(4.2))
print(math.floor(4.8))
```

**Resultados:** `5` e `4`.

### `random.randint()`

Gera um número inteiro aleatório entre os limites informados, incluindo ambos.

```python
import random

numero = random.randint(1, 10)
print(numero)
```

## 7. Manipulação de strings

Strings são sequências de caracteres utilizadas para representar textos.

### `len()`

Retorna a quantidade de caracteres.

```python
texto = "Python"
print(len(texto))
```

**Resultado:** `6`

### `upper()` e `lower()`

Convertem as letras para maiúsculas ou minúsculas.

```python
texto = "Python"

print(texto.upper())
print(texto.lower())
```

### `capitalize()` e `title()`

`capitalize()` coloca o primeiro caractere em maiúscula. `title()` coloca a primeira letra de cada palavra em maiúscula.

```python
print("olá mundo".capitalize())
print("olá mundo".title())
```

### `strip()`

Remove espaços em branco do início e do final da string.

```python
nome = "   André   "
print(nome.strip())
```

### `replace()`

Substitui um trecho de texto por outro.

```python
texto = "Eu gosto de Java"
print(texto.replace("Java", "Python"))
```

### `split()`

Divide uma string em uma lista de partes.

```python
frase = "Python é uma linguagem"
palavras = frase.split()

print(palavras)
```

### `join()`

Une elementos de uma sequência de strings utilizando um separador.

```python
palavras = ["Python", "é", "legal"]
frase = " ".join(palavras)

print(frase)
```

### `find()`

Retorna o índice da primeira ocorrência de um trecho. Se não encontrar, retorna `-1`.

```python
texto = "Programação Python"
print(texto.find("Python"))
```

**Resultado:** `12`

### `startswith()` e `endswith()`

Verificam se uma string começa ou termina com determinado trecho.

```python
arquivo = "dados.csv"

print(arquivo.startswith("dados"))
print(arquivo.endswith(".csv"))
```

### `count()`

Conta quantas vezes um trecho aparece.

```python
texto = "banana"
print(texto.count("a"))
```

**Resultado:** `3`

### F-strings

Permitem inserir variáveis e expressões diretamente em textos.

```python
nome = "André"
idade = 17

print(f"Meu nome é {nome} e tenho {idade} anos.")
```

### Indexação e fatiamento

Permitem acessar caracteres ou partes de uma string.

```python
texto = "Python"

print(texto[0])
print(texto[-1])
print(texto[0:3])
```

**Resultados:** `P`, `n` e `Pyt`.

## 8. Manipulação de listas

Listas armazenam coleções ordenadas e mutáveis de elementos.

### Criação e acesso

```python
frutas = ["maçã", "banana", "uva"]

print(frutas[0])
print(frutas[-1])
```

### `append()`

Adiciona um elemento ao final da lista.

```python
frutas = ["maçã", "banana"]
frutas.append("uva")

print(frutas)
```

### `insert()`

Insere um elemento em uma posição específica.

```python
numeros = [10, 30]
numeros.insert(1, 20)

print(numeros)
```

### `extend()`

Adiciona os elementos de outra sequência à lista.

```python
numeros = [1, 2]
numeros.extend([3, 4])

print(numeros)
```

### `remove()`

Remove a primeira ocorrência de um valor.

```python
frutas = ["maçã", "banana", "uva"]
frutas.remove("banana")

print(frutas)
```

### `pop()`

Remove e retorna um elemento da lista. Sem argumento, remove o último.

```python
numeros = [10, 20, 30]
removido = numeros.pop()

print(removido)
print(numeros)
```

### `sort()`

Ordena os elementos da lista.

```python
numeros = [5, 2, 8, 1]
numeros.sort()

print(numeros)
```

Para ordenar em ordem decrescente:

```python
numeros.sort(reverse=True)
print(numeros)
```

### `reverse()`

Inverte a ordem dos elementos.

```python
numeros = [1, 2, 3]
numeros.reverse()

print(numeros)
```

### `index()` e `count()`

`index()` retorna a posição da primeira ocorrência. `count()` conta quantas vezes um valor aparece.

```python
numeros = [10, 20, 10, 30]

print(numeros.index(20))
print(numeros.count(10))
```

### `copy()` e `clear()`

`copy()` cria uma cópia superficial da lista. `clear()` remove todos os elementos.

```python
original = [1, 2, 3]
copia = original.copy()

copia.append(4)
print(original)
print(copia)

copia.clear()
print(copia)
```

### Fatiamento de listas

Permite obter partes de uma lista.

```python
numeros = [10, 20, 30, 40, 50]

print(numeros[1:4])
print(numeros[:3])
print(numeros[::2])
```

### List comprehension

Permite criar listas de forma compacta.

```python
quadrados = [numero ** 2 for numero in range(1, 6)]

print(quadrados)
```

**Resultado:** `[1, 4, 9, 16, 25]`

## 9. Tuplas, conjuntos e dicionários

### Tuplas (`tuple`)

São coleções ordenadas e imutáveis.

```python
coordenadas = (10, 20)

print(coordenadas[0])
print(coordenadas[1])
print(len(coordenadas))
```

### Conjuntos (`set`)

Armazenam elementos únicos, sem garantir uma ordem específica.

```python
numeros = {1, 2, 2, 3}
print(numeros)
```

### `add()`

Adiciona um elemento ao conjunto.

```python
numeros = {1, 2}
numeros.add(3)

print(numeros)
```

### `discard()`

Remove um elemento, caso exista, sem gerar erro se estiver ausente.

```python
numeros = {1, 2, 3}
numeros.discard(2)

print(numeros)
```

### `union()` e `intersection()`

`union()` retorna a união dos conjuntos. `intersection()` retorna os elementos presentes em ambos.

```python
a = {1, 2, 3}
b = {3, 4, 5}

print(a.union(b))
print(a.intersection(b))
```

### Dicionários (`dict`)

Armazenam informações em pares de chave e valor.

```python
aluno = {
    "nome": "André",
    "idade": 17,
    "nota": 9.0
}

print(aluno["nome"])
print(aluno["nota"])
```

### `get()`

Obtém o valor de uma chave, permitindo definir um valor padrão caso ela não exista.

```python
aluno = {"nome": "André"}

print(aluno.get("nome"))
print(aluno.get("turma", "Não informada"))
```

### `keys()`, `values()` e `items()`

Permitem acessar as chaves, os valores e os pares de um dicionário.

```python
aluno = {"nome": "Ana", "idade": 16}

print(aluno.keys())
print(aluno.values())
print(aluno.items())
```

### `update()`

Adiciona ou atualiza pares de chave e valor.

```python
aluno = {"nome": "Ana", "idade": 16}
aluno.update({"idade": 17, "nota": 9})

print(aluno)
```

### `pop()`

Remove uma chave e retorna seu valor.

```python
aluno = {"nome": "Ana", "idade": 17}
idade = aluno.pop("idade")

print(idade)
print(aluno)
```

### Percorrendo um dicionário

```python
produto = {
    "nome": "Teclado",
    "preco": 150
}

for chave, valor in produto.items():
    print(f"{chave}: {valor}")
```

## 10. Funções

Funções são blocos de código reutilizáveis que executam tarefas específicas.

### `def`

Define uma função.

```python
def saudacao():
    print("Olá, mundo!")

saudacao()
```

### Parâmetros e argumentos

Permitem fornecer informações para uma função.

```python
def saudacao(nome):
    print(f"Olá, {nome}!")

saudacao("André")
```

### `return`

Retorna um resultado para o local onde a função foi chamada.

```python
def somar(a, b):
    return a + b

resultado = somar(5, 3)
print(resultado)
```

### Parâmetros com valores padrão

Definem valores utilizados quando um argumento não é informado.

```python
def calcular_preco(preco, desconto=0):
    return preco - (preco * desconto / 100)

print(calcular_preco(100))
print(calcular_preco(100, 10))
```

### Argumentos nomeados

Permitem informar valores pelo nome dos parâmetros.

```python
def apresentar(nome, idade):
    print(f"{nome} tem {idade} anos.")

apresentar(idade=17, nome="André")
```

### `lambda`

Cria uma função anônima simples.

```python
dobro = lambda numero: numero * 2

print(dobro(5))
```

### `map()`

Aplica uma função a cada elemento de uma sequência.

```python
numeros = [1, 2, 3]
dobros = list(map(lambda n: n * 2, numeros))

print(dobros)
```

### `filter()`

Seleciona os elementos que atendem a uma condição.

```python
numeros = [1, 2, 3, 4, 5, 6]
pares = list(filter(lambda n: n % 2 == 0, numeros))

print(pares)
```

## 11. Manipulação de arquivos

Python permite criar, ler e modificar arquivos.

### `open()`

Abre um arquivo para leitura ou escrita.

| Modo | Finalidade |
|---|---|
| `"r"` | Leitura |
| `"w"` | Escrita, substituindo o conteúdo |
| `"a"` | Adição ao final do arquivo |
| `"x"` | Criação exclusiva de um arquivo novo |
| `"b"` | Modo binário |
| `"+"` | Leitura e escrita combinadas com outro modo |

### `with open()`

Abre um arquivo e garante seu fechamento automático ao sair do bloco.

### `write()`

Escreve texto em um arquivo.

```python
with open("dados.txt", "w", encoding="utf-8") as arquivo:
    arquivo.write("Olá, Python!\n")
    arquivo.write("Arquivo criado com sucesso.")
```

### `read()`

Lê todo o conteúdo de um arquivo.

```python
with open("dados.txt", "r", encoding="utf-8") as arquivo:
    conteudo = arquivo.read()

print(conteudo)
```

### `readline()`

Lê uma linha do arquivo.

```python
with open("dados.txt", "r", encoding="utf-8") as arquivo:
    primeira_linha = arquivo.readline()

print(primeira_linha)
```

### `readlines()`

Retorna uma lista contendo as linhas do arquivo.

```python
with open("dados.txt", "r", encoding="utf-8") as arquivo:
    linhas = arquivo.readlines()

print(linhas)
```

### Modo `"a"`

Adiciona texto ao final do arquivo sem substituir o conteúdo anterior.

```python
with open("dados.txt", "a", encoding="utf-8") as arquivo:
    arquivo.write("\nNova informação adicionada.")
```

### `seek()`

Altera a posição de leitura ou escrita dentro do arquivo.

```python
with open("dados.txt", "r", encoding="utf-8") as arquivo:
    arquivo.seek(0)
    print(arquivo.read())
```

### `tell()`

Retorna a posição atual do cursor no arquivo.

```python
with open("dados.txt", "r", encoding="utf-8") as arquivo:
    print(arquivo.tell())
    arquivo.read(5)
    print(arquivo.tell())
```

**Observação:** os exemplos de leitura pressupõem que o arquivo `dados.txt` já tenha sido criado.

## 12. Tratamento de exceções

Permite tratar erros durante a execução do programa.

### `try` e `except`

O `try` contém o código que pode gerar um erro, enquanto o `except` define como tratá-lo.

```python
try:
    numero = int(input("Digite um número inteiro: "))
    print(numero * 2)
except ValueError:
    print("Digite um número inteiro válido.")
```

### `else`

É executado quando nenhuma exceção ocorre no bloco `try`.

```python
try:
    numero = int("10")
except ValueError:
    print("Valor inválido")
else:
    print(f"Número convertido: {numero}")
```

### `finally`

É executado ao final do tratamento, independentemente de ter ocorrido uma exceção.

```python
try:
    print("Executando operação")
except Exception:
    print("Ocorreu um erro")
finally:
    print("Operação finalizada")
```

### `raise`

Permite gerar uma exceção manualmente.

```python
def verificar_idade(idade):
    if idade < 0:
        raise ValueError("A idade não pode ser negativa.")
    return idade

print(verificar_idade(18))
```

### Tratamento de erros de arquivos

```python
try:
    with open("inexistente.txt", "r", encoding="utf-8") as arquivo:
        print(arquivo.read())
except FileNotFoundError:
    print("O arquivo não foi encontrado.")
```

## 13. Bibliotecas úteis

### `math`

Oferece funções e constantes matemáticas.

```python
import math

print(math.pi)
print(math.sqrt(25))
print(math.factorial(5))
```

### `random`

Gera valores aleatórios e seleciona elementos de sequências.

```python
import random

print(random.randint(1, 100))
print(random.choice(["Python", "Java", "JavaScript"]))
```

### `datetime`

Permite trabalhar com datas e horários.

```python
from datetime import date, datetime

hoje = date.today()
agora = datetime.now()

print(hoje)
print(agora)
```

### `statistics`

Oferece funções para cálculos estatísticos básicos.

```python
import statistics

notas = [7, 8, 9, 10]

print(statistics.mean(notas))
print(statistics.median(notas))
```

### `json`

Permite converter dados entre estruturas Python e o formato JSON.

```python
import json

aluno = {"nome": "André", "idade": 17}

texto_json = json.dumps(aluno, ensure_ascii=False)
print(texto_json)

aluno_convertido = json.loads(texto_json)
print(aluno_convertido["nome"])
```

**Referência:** [Documentação oficial do Python em português](https://docs.python.org/pt-br/3/)
