# Dicionário de Python

## 1. Entrada e saída de dados

### `print()`

**Finalidade:** Exibe informações na tela.

```python
nome = "André"
print("Olá,", nome)
```

**Saída:**
```text
Olá, André
```

### `input()`

**Finalidade:** Lê informações digitadas pelo usuário. O valor retornado é uma string.

```python
nome = input("Digite seu nome: ")
print(nome)
```

### `input().split()`

**Finalidade:** Lê uma linha e separa os valores utilizando espaços em branco como separadores, retornando uma lista de strings.

```python
valores = input().split()
print(valores)
```

**Entrada:**
```text
10 20 30
```

**Saída:**
```text
['10', '20', '30']
```

### `map()`

**Finalidade:** Aplica uma função a cada elemento de um iterável, permitindo converter vários valores de uma vez.

```python
numeros = map(int, input().split())
print(list(numeros))
```

**Entrada:**
```text
10 20 30
```

**Saída:**
```text
[10, 20, 30]
```

### Leitura de dois números na mesma linha

**Finalidade:** Lê dois números inteiros, separando-os por espaços e armazenando cada valor em uma variável.

```python
x, y = map(int, input().split())

print(x)
print(y)
```

**Entrada:**
```text
5 10
```

**Saída:**
```text
5
10
```

### Leitura de um vetor em uma única linha

**Finalidade:** Lê vários números inteiros e armazena todos em uma lista, que também pode ser chamada de vetor.

```python
vetor = list(map(int, input().split()))

print(vetor)
```

**Entrada:**
```text
1 2 3 4 5
```

**Saída:**
```text
[1, 2, 3, 4, 5]
```

**Explicação dos comandos:**

- `input()` lê a linha digitada.
- `.split()` separa os valores.
- `map(int, ...)` converte cada valor para inteiro.
- `list(...)` armazena os valores em uma lista.

### Leitura de uma quantidade definida de números

**Finalidade:** Lê uma quantidade de números informada pelo usuário e armazena os valores em uma lista.

```python
n = int(input())
vetor = list(map(int, input().split()))

print(n)
print(vetor)
```

**Entrada:**
```text
4
10 20 30 40
```

**Saída:**
```text
4
[10, 20, 30, 40]
```

---

## 2. Variáveis e tipos de dados

### Variáveis

**Finalidade:** Armazenam valores que podem ser utilizados e modificados durante a execução do programa.

```python
nome = "André"
idade = 17
altura = 1.75

print(nome, idade, altura)
```

### Tipos de dados

**Finalidade:** Definem a natureza dos valores armazenados nas variáveis.

| Tipo | Descrição | Exemplo |
|---|---|---|
| `int` | Números inteiros | `idade = 17` |
| `float` | Números decimais | `altura = 1.75` |
| `str` | Textos | `nome = "Ana"` |
| `bool` | Valores lógicos | `aprovado = True` |
| `list` | Lista de elementos | `numeros = [1, 2, 3]` |

### `type()`

**Finalidade:** Identifica o tipo de dado de uma variável.

```python
numero = 10
print(type(numero))
```

**Saída:**
```text
<class 'int'>
```

### `int()`

**Finalidade:** Converte um valor compatível para inteiro.

```python
numero = int("25")
print(numero + 5)
```

**Saída:** `30`

### `float()`

**Finalidade:** Converte um valor compatível para número decimal.

```python
numero = float("2.5")
print(numero * 2)
```

**Saída:** `5.0`

### `str()`

**Finalidade:** Converte um valor para texto.

```python
idade = 17
texto = str(idade)

print("Idade: " + texto)
```

### `bool()`

**Finalidade:** Converte um valor para verdadeiro ou falso.

```python
print(bool(1))
print(bool(0))
```

**Saída:**
```text
True
False
```

### Atribuição de variáveis

**Finalidade:** O operador `=` atribui um valor a uma variável.

```python
numero = 10
numero = numero + 5

print(numero)
```

**Saída:** `15`

---

## 3. Operadores

### Operadores aritméticos

**Finalidade:** Realizam operações matemáticas.

| Operador | Operação | Exemplo | Resultado |
|---|---|---|---|
| `+` | Adição | `5 + 3` | `8` |
| `-` | Subtração | `5 - 3` | `2` |
| `*` | Multiplicação | `5 * 3` | `15` |
| `/` | Divisão | `5 / 2` | `2.5` |
| `//` | Divisão inteira | `5 // 2` | `2` |
| `%` | Resto da divisão | `5 % 2` | `1` |
| `**` | Potenciação | `2 ** 3` | `8` |

```python
a = 10
b = 3

print(a + b)
print(a - b)
print(a * b)
print(a / b)
print(a // b)
print(a % b)
print(a ** b)
```

### Operadores relacionais

**Finalidade:** Comparam valores e retornam `True` ou `False`.

| Operador | Finalidade |
|---|---|
| `==` | Igual a |
| `!=` | Diferente de |
| `>` | Maior que |
| `<` | Menor que |
| `>=` | Maior ou igual a |
| `<=` | Menor ou igual a |

```python
a = 10
b = 5

print(a > b)
print(a == b)
print(a != b)
```

**Saída:**
```text
True
False
True
```

### Operadores lógicos

**Finalidade:** Combinam condições ou invertem seus resultados.

- `and`: verdadeiro quando ambas as condições são verdadeiras.
- `or`: verdadeiro quando pelo menos uma condição é verdadeira.
- `not`: inverte o resultado lógico.

```python
idade = 20

print(idade >= 18 and idade < 60)
print(idade < 18 or idade >= 60)
print(not idade < 18)
```

### Operadores de atribuição

**Finalidade:** Atribuem ou atualizam valores de variáveis.

| Operador | Exemplo | Equivalência |
|---|---|---|
| `=` | `x = 10` | Atribui 10 |
| `+=` | `x += 2` | `x = x + 2` |
| `-=` | `x -= 2` | `x = x - 2` |
| `*=` | `x *= 2` | `x = x * 2` |
| `/=` | `x /= 2` | `x = x / 2` |
| `//=` | `x //= 2` | `x = x // 2` |
| `%=` | `x %= 2` | `x = x % 2` |
| `**=` | `x **= 2` | `x = x ** 2` |

```python
x = 10
x += 5

print(x)
```

**Saída:** `15`

### Operadores de pertencimento

**Finalidade:** Verificam se um elemento está presente em uma sequência ou coleção.

- `in`: verifica se o elemento está presente.
- `not in`: verifica se o elemento não está presente.

```python
numeros = [1, 2, 3, 4, 5]

print(3 in numeros)
print(8 not in numeros)
```

**Saída:**
```text
True
True
```

---

## 4. Estruturas condicionais

### `if`

**Finalidade:** Executa um bloco de código quando uma condição é verdadeira.

```python
idade = 18

if idade >= 18:
    print("Maior de idade")
```

### `elif`

**Finalidade:** Verifica outra condição quando as condições anteriores são falsas.

```python
nota = 7

if nota >= 9:
    print("Excelente")
elif nota >= 7:
    print("Aprovado")
```

### `else`

**Finalidade:** Executa um bloco quando as condições anteriores não são satisfeitas.

```python
nota = 5

if nota >= 7:
    print("Aprovado")
else:
    print("Reprovado")
```

### Condicionais combinadas

**Finalidade:** Utilizam operadores lógicos para verificar várias condições.

```python
idade = 20
tem_documento = True

if idade >= 18 and tem_documento:
    print("Entrada permitida")
else:
    print("Entrada negada")
```

---

## 5. Estruturas de repetição

### `for`

**Finalidade:** Percorre os elementos de uma sequência ou executa um bloco para cada elemento.

```python
for numero in [1, 2, 3, 4, 5]:
    print(numero)
```

### `while`

**Finalidade:** Repete um bloco de código enquanto uma condição for verdadeira.

```python
contador = 1

while contador <= 5:
    print(contador)
    contador += 1
```

### `range()`

**Finalidade:** Gera uma sequência de números, sendo utilizada principalmente com `for`.

```python
for numero in range(1, 6):
    print(numero)
```

**Saída:** Números de `1` até `5`.

### `break`

**Finalidade:** Interrompe imediatamente o laço de repetição.

```python
for numero in range(1, 10):
    if numero == 5:
        break
    print(numero)
```

**Saída:** `1`, `2`, `3` e `4`.

### `continue`

**Finalidade:** Pula a iteração atual e continua com a próxima.

```python
for numero in range(1, 6):
    if numero == 3:
        continue
    print(numero)
```

**Saída:** `1`, `2`, `4` e `5`.

### Percorrendo um vetor com `for`

**Finalidade:** Acessa cada elemento de uma lista sem precisar utilizar seu índice.

```python
vetor = [10, 20, 30, 40]

for numero in vetor:
    print(numero)
```

### Percorrendo um vetor por índices

**Finalidade:** Utiliza os índices para acessar os elementos de uma lista.

```python
vetor = [10, 20, 30, 40]

for i in range(len(vetor)):
    print(vetor[i])
```

### Soma dos elementos de um vetor

**Finalidade:** Percorre uma lista e acumula a soma de seus elementos.

```python
vetor = [10, 20, 30]
soma = 0

for numero in vetor:
    soma += numero

print(soma)
```

**Saída:** `60`

---

## 6. Funções para números

### `abs()`

**Finalidade:** Retorna o valor absoluto de um número.

```python
print(abs(-10))
```

**Saída:** `10`

### `round()`

**Finalidade:** Arredonda um número para a quantidade de casas decimais indicada.

```python
print(round(3.14159, 2))
```

**Saída:** `3.14`

### `pow()`

**Finalidade:** Calcula a potência de um número.

```python
print(pow(2, 3))
```

**Saída:** `8`

### `min()`

**Finalidade:** Retorna o menor valor de uma coleção ou entre vários argumentos.

```python
numeros = [10, 5, 20, 3]

print(min(numeros))
```

**Saída:** `3`

### `max()`

**Finalidade:** Retorna o maior valor de uma coleção ou entre vários argumentos.

```python
numeros = [10, 5, 20, 3]

print(max(numeros))
```

**Saída:** `20`

### `sum()`

**Finalidade:** Soma os elementos de uma coleção numérica.

```python
numeros = [1, 2, 3, 4]

print(sum(numeros))
```

**Saída:** `10`

### `divmod()`

**Finalidade:** Retorna o quociente inteiro e o resto de uma divisão.

```python
print(divmod(17, 5))
```

**Saída:** `(3, 2)`

### `int()` e `float()` em cálculos

**Finalidade:** Convertem valores para permitir operações matemáticas.

```python
a = int("10")
b = float("2.5")

print(a + b)
```

**Saída:** `12.5`

---

## 7. Funções para strings

### `upper()`

**Finalidade:** Converte todos os caracteres alfabéticos para maiúsculas.

```python
texto = "python"
print(texto.upper())
```

**Saída:** `PYTHON`

### `lower()`

**Finalidade:** Converte todos os caracteres alfabéticos para minúsculas.

```python
texto = "PYTHON"
print(texto.lower())
```

**Saída:** `python`

### `strip()`

**Finalidade:** Remove espaços em branco do início e do final de uma string.

```python
texto = "   Python   "
print(texto.strip())
```

**Saída:** `Python`

### `replace()`

**Finalidade:** Substitui um trecho de texto por outro.

```python
texto = "Eu gosto de Java"
print(texto.replace("Java", "Python"))
```

**Saída:** `Eu gosto de Python`

### `split()`

**Finalidade:** Divide uma string em uma lista de partes, utilizando espaços em branco como separadores por padrão.

```python
texto = "10 20 30"
print(texto.split())
```

**Saída:** `['10', '20', '30']`

**Aplicação com números:**

```python
numeros = list(map(int, input().split()))
print(numeros)
```

**Entrada:**
```text
10 20 30
```

**Saída:**
```text
[10, 20, 30]
```

### `find()`

**Finalidade:** Retorna o índice da primeira ocorrência de um trecho. Se não encontrar, retorna `-1`.

```python
texto = "Python é legal"
print(texto.find("legal"))
```

**Saída:** `10`

### `len()`

**Finalidade:** Retorna a quantidade de caracteres de uma string.

```python
texto = "Python"
print(len(texto))
```

**Saída:** `6`

### `startswith()`

**Finalidade:** Verifica se uma string começa com determinado trecho.

```python
texto = "Python"
print(texto.startswith("Py"))
```

**Saída:** `True`

### `endswith()`

**Finalidade:** Verifica se uma string termina com determinado trecho.

```python
arquivo = "dados.txt"
print(arquivo.endswith(".txt"))
```

**Saída:** `True`

### `isdigit()`

**Finalidade:** Verifica se todos os caracteres da string são dígitos.

```python
print("12345".isdigit())
print("12a45".isdigit())
```

**Saída:**
```text
True
False
```

### F-strings

**Finalidade:** Permitem inserir variáveis diretamente em textos.

```python
nome = "André"
idade = 17

print(f"Meu nome é {nome} e tenho {idade} anos.")
```

---

## 8. Funções para listas (vetores)

### Criação de uma lista

**Finalidade:** Armazena vários elementos em uma única variável.

```python
vetor = [10, 20, 30, 40]

print(vetor)
```

### `list()`

**Finalidade:** Cria uma lista a partir de um iterável.

```python
texto = "Python"
letras = list(texto)

print(letras)
```

**Saída:** `['P', 'y', 't', 'h', 'o', 'n']`

### `len()`

**Finalidade:** Retorna a quantidade de elementos de uma lista.

```python
vetor = [10, 20, 30, 40]

print(len(vetor))
```

**Saída:** `4`

### `append()`

**Finalidade:** Adiciona um elemento ao final da lista.

```python
vetor = [10, 20, 30]
vetor.append(40)

print(vetor)
```

**Saída:** `[10, 20, 30, 40]`

### `insert()`

**Finalidade:** Insere um elemento em uma posição específica.

```python
vetor = [10, 30, 40]
vetor.insert(1, 20)

print(vetor)
```

**Saída:** `[10, 20, 30, 40]`

### `remove()`

**Finalidade:** Remove a primeira ocorrência de um valor.

```python
vetor = [10, 20, 30]
vetor.remove(20)

print(vetor)
```

**Saída:** `[10, 30]`

### `pop()`

**Finalidade:** Remove e retorna um elemento da lista. Sem argumento, remove o último elemento.

```python
vetor = [10, 20, 30]
valor = vetor.pop()

print(valor)
print(vetor)
```

**Saída:**
```text
30
[10, 20]
```

### `sort()`

**Finalidade:** Ordena os elementos da lista em ordem crescente por padrão.

```python
vetor = [5, 2, 8, 1]
vetor.sort()

print(vetor)
```

**Saída:** `[1, 2, 5, 8]`

Para ordenar em ordem decrescente:

```python
vetor = [5, 2, 8, 1]
vetor.sort(reverse=True)

print(vetor)
```

**Saída:** `[8, 5, 2, 1]`

### `reverse()`

**Finalidade:** Inverte a ordem atual dos elementos da lista.

```python
vetor = [10, 20, 30]
vetor.reverse()

print(vetor)
```

**Saída:** `[30, 20, 10]`

### `index()`

**Finalidade:** Retorna o índice da primeira ocorrência de um valor.

```python
vetor = [10, 20, 30]

print(vetor.index(20))
```

**Saída:** `1`

### `count()`

**Finalidade:** Conta quantas vezes um valor aparece na lista.

```python
vetor = [1, 2, 2, 3, 2]

print(vetor.count(2))
```

**Saída:** `3`

### `sum()`

**Finalidade:** Soma os elementos numéricos da lista.

```python
vetor = [10, 20, 30]

print(sum(vetor))
```

**Saída:** `60`

### `max()` e `min()`

**Finalidade:** Retornam o maior e o menor elemento da lista.

```python
vetor = [10, 5, 30, 15]

print(max(vetor))
print(min(vetor))
```

**Saída:**
```text
30
5
```

### Acesso por índice

**Finalidade:** Permite acessar um elemento específico pelo seu índice. A contagem começa em zero.

```python
vetor = [10, 20, 30]

print(vetor[0])
print(vetor[2])
```

**Saída:**
```text
10
30
```

### Leitura de um vetor em uma linha

**Finalidade:** Lê vários números inteiros separados por espaços e os armazena em uma lista.

```python
vetor = list(map(int, input().split()))

print(vetor)
```

**Entrada:**
```text
4 8 12 16
```

**Saída:**
```text
[4, 8, 12, 16]
```

### Leitura de dois valores em uma linha

**Finalidade:** Armazena dois números inteiros em variáveis distintas.

```python
x, y = map(int, input().split())

print(x + y)
```

**Entrada:**
```text
5 7
```

**Saída:** `12`

### Soma dos elementos de um vetor

**Finalidade:** Calcula a soma de todos os valores armazenados na lista.

```python
vetor = [1, 2, 3, 4, 5]

soma = sum(vetor)

print(soma)
```

**Saída:** `15`

---

## 9. Manipulação de arquivos

### `open()`

**Finalidade:** Abre um arquivo para leitura ou escrita.

Principais modos:

| Modo | Finalidade |
|---|---|
| `"r"` | Abre para leitura |
| `"w"` | Abre para escrita, substituindo o conteúdo |
| `"a"` | Adiciona conteúdo ao final |
| `"x"` | Cria um arquivo novo, gerando erro se ele já existir |

```python
arquivo = open("dados.txt", "w", encoding="utf-8")
arquivo.write("Olá, Python!")
arquivo.close()
```

### `write()`

**Finalidade:** Escreve texto em um arquivo.

```python
arquivo = open("dados.txt", "w", encoding="utf-8")
arquivo.write("Primeira linha\n")
arquivo.write("Segunda linha")
arquivo.close()
```

### `read()`

**Finalidade:** Lê todo o conteúdo de um arquivo.

```python
arquivo = open("dados.txt", "r", encoding="utf-8")
conteudo = arquivo.read()
print(conteudo)
arquivo.close()
```

### `readline()`

**Finalidade:** Lê uma linha do arquivo por vez.

```python
arquivo = open("dados.txt", "r", encoding="utf-8")
linha = arquivo.readline()
print(linha)
arquivo.close()
```

### `readlines()`

**Finalidade:** Lê todas as linhas e as retorna em uma lista.

```python
arquivo = open("dados.txt", "r", encoding="utf-8")
linhas = arquivo.readlines()
print(linhas)
arquivo.close()
```

### `close()`

**Finalidade:** Fecha um arquivo aberto, liberando os recursos utilizados.

```python
arquivo = open("dados.txt", "w", encoding="utf-8")
arquivo.write("Teste")
arquivo.close()
```

### `with`

**Finalidade:** Abre um arquivo e fecha-o automaticamente ao final do bloco, mesmo que ocorra um erro.

```python
with open("dados.txt", "w", encoding="utf-8") as arquivo:
    arquivo.write("Arquivo salvo com sucesso.")
```

### Adicionando conteúdo a um arquivo

**Finalidade:** Utiliza o modo `"a"` para acrescentar informações sem apagar o conteúdo existente.

```python
with open("dados.txt", "a", encoding="utf-8") as arquivo:
    arquivo.write("\nNova informação")
```

### Lendo um arquivo linha por linha

**Finalidade:** Percorre o arquivo sem precisar carregar todas as linhas em uma lista.

```python
with open("dados.txt", "r", encoding="utf-8") as arquivo:
    for linha in arquivo:
        print(linha.strip())
```

**Observação:** os exemplos de leitura pressupõem que o arquivo `dados.txt` já tenha sido criado. Os exemplos de escrita criam o arquivo caso ele não exista.

---

**Documentação oficial:** [Python — Documentação em português](https://docs.python.org/pt-br/3/)
