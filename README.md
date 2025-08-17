
# Introdução ao Python: Do Básico ao Especialista em Manipulação de Dados

## Sumário das Aulas
1. Introdução ao Python e Instalação
2. Tipos de Dados e Operadores
3. Estruturas de Controle (if, for, while)
4. Funções e Módulos
5. Estruturas de Dados (Listas, Tuplas, Dicionários, Conjuntos)
6. Manipulação de Arquivos
7. Bibliotecas para Manipulação de Dados (NumPy, Pandas)
8. Visualização de Dados (Matplotlib, Seaborn)
9. Projetos Práticos e Desafios
10. Boas Práticas e Próximos Passos

---

## Aula 1: Introdução ao Python e Instalação (Duração: 3h)

### 1.1. O que é Python?
Python é uma linguagem de programação de alto nível, interpretada, de fácil leitura e escrita. É utilizada em diversas áreas como ciência de dados, automação, web, inteligência artificial, entre outras.

**Vantagens:**
- Sintaxe simples e intuitiva
- Grande comunidade
- Multiplataforma
- Amplo suporte de bibliotecas

### 1.2. Instalação do Python
1. Acesse: https://www.python.org/downloads/
2. Baixe e instale a versão recomendada para seu sistema operacional.
3. Verifique a instalação no terminal:
	```bash
	python --version
	# ou
	python3 --version
	```

#### Ambientes Virtuais
Ambientes virtuais permitem isolar dependências de projetos.
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate    # Windows
```

### 1.3. Primeiros Passos no Python
#### Seu primeiro programa
```python
print("Olá, mundo!")
```

#### Usando o interpretador interativo
Basta digitar `python` ou `python3` no terminal para acessar o modo interativo.

### 1.4. Tipos de Dados Básicos
- **int**: números inteiros
- **float**: números decimais
- **str**: textos (strings)
- **bool**: valores lógicos (True/False)

#### Exemplos:
```python
idade = 25           # int
altura = 1.75        # float
nome = "Maria"       # str
estudante = True     # bool
```

### 1.5. Operadores
- **Aritméticos:** +, -, *, /, //, %, **
- **Relacionais:** >, <, >=, <=, ==, !=
- **Lógicos:** and, or, not

#### Exemplos:
```python
print(2 + 3)      # 5
print(10 / 3)     # 3.333...
print(10 // 3)    # 3
print(2 ** 3)     # 8
print(5 > 2)      # True
print(True and False)  # False
```

### 1.6. Entrada e Saída de Dados
```python
nome = input("Qual seu nome? ")
print("Bem-vindo,", nome)
```

### 1.7. Comentários
```python
# Isso é um comentário de linha única
"""
Isso é um comentário
de múltiplas linhas
"""
```

---

## Exercícios Aula 1

1. Escreva um programa que peça o nome e a idade do usuário e exiba uma mensagem personalizada.
2. Calcule a soma, subtração, multiplicação e divisão de dois números informados pelo usuário.
3. Peça ao usuário um número e mostre se ele é par ou ímpar.
4. Crie um programa que converta graus Celsius para Fahrenheit.
5. Faça um programa que pergunte quanto dinheiro você tem na carteira e mostre quantos dólares pode comprar (considere US$1 = R$5,00).

**Desafio:**
Crie um programa que leia o nome, idade e altura de uma pessoa e exiba tudo formatado em uma frase.

---


## Aula 2: Resolução dos Exercícios e Tipos de Dados/Operadores (Duração: 3h)

### 2.1. Resolução dos Exercícios da Aula 1

**Exercício 1:**
> Escreva um programa que peça o nome e a idade do usuário e exiba uma mensagem personalizada.
```python
nome = input("Qual seu nome? ")
idade = input("Qual sua idade? ")
print(f"Olá, {nome}! Você tem {idade} anos.")
```
**Explicação:**
Utilizamos a função `input()` para capturar dados do usuário e o f-string para formatar a mensagem.

**Exercício 2:**
> Calcule a soma, subtração, multiplicação e divisão de dois números informados pelo usuário.
```python
num1 = float(input("Digite o primeiro número: "))
num2 = float(input("Digite o segundo número: "))
print("Soma:", num1 + num2)
print("Subtração:", num1 - num2)
print("Multiplicação:", num1 * num2)
print("Divisão:", num1 / num2)
```
**Explicação:**
Convertendo as entradas para `float` para permitir números decimais. Operações básicas são realizadas e exibidas.

**Exercício 3:**
> Peça ao usuário um número e mostre se ele é par ou ímpar.
```python
numero = int(input("Digite um número: "))
if numero % 2 == 0:
	print("Par")
else:
	print("Ímpar")
```
**Explicação:**
O operador `%` retorna o resto da divisão. Se for zero, o número é par.

**Exercício 4:**
> Crie um programa que converta graus Celsius para Fahrenheit.
```python
celsius = float(input("Informe a temperatura em Celsius: "))
fahrenheit = (celsius * 9/5) + 32
print(f"{celsius}°C equivalem a {fahrenheit}°F")
```
**Explicação:**
Aplicação direta da fórmula de conversão.

**Exercício 5:**
> Pergunte quanto dinheiro você tem na carteira e mostre quantos dólares pode comprar (US$1 = R$5,00).
```python
reais = float(input("Quanto dinheiro você tem na carteira? R$ "))
dolares = reais / 5
print(f"Você pode comprar US${dolares:.2f}")
```
**Explicação:**
Dividimos o valor em reais pela cotação do dólar e formatamos para duas casas decimais.

**Desafio:**
> Leia o nome, idade e altura de uma pessoa e exiba tudo formatado em uma frase.
```python
nome = input("Nome: ")
idade = int(input("Idade: "))
altura = float(input("Altura (em metros): "))
print(f"{nome} tem {idade} anos e {altura:.2f}m de altura.")
```

---

### 2.2. Tipos de Dados e Operadores (Aprofundamento)

#### Tipos Numéricos
- **int:** números inteiros (ex: 10, -5, 0)
- **float:** números decimais (ex: 3.14, -0.1)

#### Strings
- Definição: sequência de caracteres entre aspas simples ou duplas.
```python
mensagem = "Olá, Python!"
print(mensagem.upper())  # Maiúsculas
print(mensagem.lower())  # Minúsculas
print(mensagem[0:3])    # Fatiamento
```

#### Booleanos
- **True** e **False**
```python
ativo = True
print(type(ativo))
```

#### Conversão de Tipos
```python
idade = "30"
idade = int(idade)
print(idade + 5)
```

#### Operadores Aritméticos
- Soma (+), Subtração (-), Multiplicação (*), Divisão (/), Divisão inteira (//), Módulo (%), Potência (**)

#### Operadores Relacionais
- >, <, >=, <=, ==, !=
```python
print(5 > 2)   # True
print(3 == 4)  # False
```

#### Operadores Lógicos
- and, or, not
```python
print(True and False)  # False
print(True or False)   # True
print(not True)        # False
```

---

### 2.3. Exercícios Propostos
1. Peça dois números ao usuário e mostre qual é o maior.
2. Solicite um texto e mostre quantos caracteres ele possui.
3. Peça um número e mostre o dobro, triplo e raiz quadrada.
4. Solicite o nome completo do usuário e mostre em maiúsculas, minúsculas e quantas letras tem (sem espaços).
5. Crie um programa que leia um número real e mostre apenas a parte inteira.

---


## Aula 3: Estruturas de Controle (if, for, while) (Duração: 3h)

### 3.1. Correção dos Exercícios da Aula 2

**Exercício 1:**
> Peça dois números ao usuário e mostre qual é o maior.
```python
a = float(input("Digite o primeiro número: "))
b = float(input("Digite o segundo número: "))
if a > b:
	print(f"O maior número é {a}")
elif b > a:
	print(f"O maior número é {b}")
else:
	print("Os números são iguais.")
```

**Exercício 2:**
> Solicite um texto e mostre quantos caracteres ele possui.
```python
texto = input("Digite um texto: ")
print(f"O texto possui {len(texto)} caracteres.")
```

**Exercício 3:**
> Peça um número e mostre o dobro, triplo e raiz quadrada.
```python
import math
num = float(input("Digite um número: "))
print(f"Dobro: {num*2}")
print(f"Triplo: {num*3}")
print(f"Raiz quadrada: {math.sqrt(num):.2f}")
```

**Exercício 4:**
> Solicite o nome completo do usuário e mostre em maiúsculas, minúsculas e quantas letras tem (sem espaços).
```python
nome = input("Digite seu nome completo: ")
print(nome.upper())
print(nome.lower())
print(f"Total de letras (sem espaços): {len(nome.replace(' ', ''))}")
```

**Exercício 5:**
> Crie um programa que leia um número real e mostre apenas a parte inteira.
```python
num = float(input("Digite um número real: "))
print(f"Parte inteira: {int(num)}")
```

---

### 3.2. Estruturas de Controle

#### 3.2.1. Estruturas Condicionais (if, elif, else)
Permitem executar blocos de código de acordo com condições.
```python
idade = int(input("Qual sua idade? "))
if idade < 18:
	print("Menor de idade")
elif idade < 60:
	print("Adulto")
else:
	print("Idoso")
```

#### 3.2.2. Estruturas de Repetição: for
Usado para percorrer sequências (listas, strings, ranges).
```python
for i in range(1, 6):
	print(f"Contando: {i}")

frutas = ["maçã", "banana", "uva"]
for fruta in frutas:
	print(fruta)
```

#### 3.2.3. Estruturas de Repetição: while
Executa enquanto a condição for verdadeira.
```python
contador = 0
while contador < 5:
	print(f"Valor: {contador}")
	contador += 1
```

#### 3.2.4. Controle de Fluxo com break e continue
```python
for i in range(10):
	if i == 5:
		break  # Interrompe o laço
	if i % 2 == 0:
		continue  # Pula para o próximo
	print(i)
```

---

### 3.3. Exercícios Práticos
1. Peça ao usuário um número e mostre a tabuada desse número de 1 a 10 usando for.
2. Solicite números ao usuário até que ele digite 0. Ao final, mostre a soma de todos os números digitados.
3. Peça um texto e conte quantas vogais ele possui.
4. Crie um programa que leia 5 nomes e armazene em uma lista, depois exiba todos com for.
5. Faça um programa que leia números até o usuário digitar um negativo. Mostre quantos números foram digitados.

---


## Aula 4: Funções, Parâmetros, Retorno e Modularização (Duração: 3h)

### 4.1. Correção dos Exercícios da Aula 3

**Exercício 1:**
> Peça ao usuário um número e mostre a tabuada desse número de 1 a 10 usando for.
```python
num = int(input("Digite um número: "))
for i in range(1, 11):
	print(f"{num} x {i} = {num * i}")
```

**Exercício 2:**
> Solicite números ao usuário até que ele digite 0. Ao final, mostre a soma de todos os números digitados.
```python
soma = 0
while True:
	n = int(input("Digite um número (0 para sair): "))
	if n == 0:
		break
	soma += n
print(f"Soma total: {soma}")
```

**Exercício 3:**
> Peça um texto e conte quantas vogais ele possui.
```python
texto = input("Digite um texto: ").lower()
vogais = 'aeiou'
cont = 0
for letra in texto:
	if letra in vogais:
		cont += 1
print(f"Quantidade de vogais: {cont}")
```

**Exercício 4:**
> Crie um programa que leia 5 nomes e armazene em uma lista, depois exiba todos com for.
```python
nomes = []
for i in range(5):
	nomes.append(input(f"Digite o {i+1}º nome: "))
for nome in nomes:
	print(nome)
```

**Exercício 5:**
> Faça um programa que leia números até o usuário digitar um negativo. Mostre quantos números foram digitados.
```python
contador = 0
while True:
	n = int(input("Digite um número (negativo para sair): "))
	if n < 0:
		break
	contador += 1
print(f"Foram digitados {contador} números.")
```

---

### 4.2. Funções em Python

Funções são blocos de código reutilizáveis que executam uma tarefa específica.

#### Definindo Funções
```python
def saudacao():
	print("Olá, seja bem-vindo!")

saudacao()
```

#### Parâmetros e Argumentos
```python
def soma(a, b):
	return a + b

resultado = soma(3, 5)
print(resultado)
```

#### Retorno de Valores
Funções podem retornar valores usando a palavra-chave `return`.

#### Escopo de Variáveis
Variáveis definidas dentro da função só existem ali (escopo local).
```python
def exemplo():
	x = 10
	print(x)

exemplo()
# print(x)  # Isso gera erro, pois x não existe fora da função
```

#### Funções com Parâmetros Opcionais
```python
def saudacao(nome="visitante"):
	print(f"Olá, {nome}!")

saudacao()
saudacao("Maria")
```

#### Documentação de Funções (docstring)
```python
def quadrado(n):
	"""Retorna o quadrado de n."""
	return n ** 2
```

#### Boas Práticas de Modularização
- Crie funções para tarefas repetitivas
- Use nomes descritivos
- Documente suas funções
- Separe funções em arquivos (módulos) quando o projeto crescer

---

### 4.3. Exercícios Práticos
1. Crie uma função que receba um nome e imprima uma saudação personalizada.
2. Escreva uma função que receba dois números e retorne o maior.
3. Faça uma função que receba um número e retorne True se for par, False se for ímpar.
4. Implemente uma função que receba uma lista de números e retorne a soma de todos.
5. Crie um módulo chamado `utilidades.py` com pelo menos duas funções úteis e mostre como importá-lo em outro arquivo.

---


## Aula 5: Módulos e Estruturas de Dados (Duração: 3h)

### 5.1. Correção dos Exercícios da Aula 4

**Exercício 1:**
```python
def saudacao(nome):
	print(f"Olá, {nome}!")
saudacao("Ana")
```

**Exercício 2:**
```python
def maior(a, b):
	return a if a > b else b
print(maior(10, 7))
```

**Exercício 3:**
```python
def eh_par(n):
	return n % 2 == 0
print(eh_par(4))  # True
print(eh_par(7))  # False
```

**Exercício 4:**
```python
def soma_lista(lista):
	return sum(lista)
print(soma_lista([1, 2, 3, 4]))
```

**Exercício 5:**
Arquivo: utilidades.py
```python
def dobro(n):
	return n * 2

def quadrado(n):
	return n ** 2
```
Como importar:
```python
import utilidades
print(utilidades.dobro(5))
print(utilidades.quadrado(3))
```

---

### 5.2. Importação de Módulos

Módulos são arquivos Python com funções, classes ou variáveis reutilizáveis.
- Para importar um módulo próprio: `import utilidades`
- Para importar apenas uma função: `from utilidades import dobro`
- Para importar módulos da biblioteca padrão: `import math`

---

### 5.3. Estruturas de Dados em Python

#### Listas
Coleção ordenada e mutável de elementos.
```python
frutas = ["maçã", "banana", "uva"]
frutas.append("laranja")
print(frutas[0])  # maçã
print(frutas[-1]) # laranja
for fruta in frutas:
	print(fruta)
```

#### Tuplas
Coleção ordenada e imutável.
```python
cores = ("vermelho", "verde", "azul")
print(cores[1])
```

#### Dicionários
Coleção de pares chave-valor.
```python
pessoa = {"nome": "João", "idade": 30}
print(pessoa["nome"])
for chave, valor in pessoa.items():
	print(chave, valor)
```

#### Conjuntos
Coleção não ordenada de elementos únicos.
```python
numeros = {1, 2, 3, 2}
print(numeros)  # {1, 2, 3}
numeros.add(4)
```

---


### 5.4. Exercícios Práticos
1. Crie uma lista com 5 números e mostre o maior e o menor valor.
2. Peça ao usuário nomes e armazene em uma tupla. Depois, mostre todos os nomes.
3. Crie um dicionário para armazenar nome e nota de 3 alunos e mostre a média das notas.
4. Peça ao usuário para digitar números até digitar 0. Armazene em um conjunto e mostre os valores únicos digitados.
5. Importe o módulo `math` e use a função `sqrt` para calcular a raiz quadrada de um número informado pelo usuário.

---

## Aula 6: Manipulação de Arquivos Texto e CSV (Duração: 3h)

### 6.1. Correção dos Exercícios da Aula 5

**Exercício 1:**
```python
numeros = [5, 2, 9, 1, 7]
print(f"Maior: {max(numeros)} | Menor: {min(numeros)}")
```

**Exercício 2:**
```python
nomes = tuple(input("Digite um nome: ") for _ in range(3))
print(nomes)
```

**Exercício 3:**
```python
alunos = {}
for _ in range(3):
	nome = input("Nome do aluno: ")
	nota = float(input("Nota: "))
	alunos[nome] = nota
media = sum(alunos.values()) / len(alunos)
print(f"Média das notas: {media:.2f}")
```

**Exercício 4:**
```python
conjunto = set()
while True:
	n = int(input("Digite um número (0 para sair): "))
	if n == 0:
		break
	conjunto.add(n)
print(f"Valores únicos: {conjunto}")
```

**Exercício 5:**
```python
import math
num = float(input("Digite um número: "))
print(f"Raiz quadrada: {math.sqrt(num):.2f}")
```

---

### 6.2. Manipulação de Arquivos Texto

#### Escrevendo em um arquivo
```python
with open('exemplo.txt', 'w') as f:
	f.write('Olá, mundo!\n')
	f.write('Segunda linha.')
```

#### Lendo um arquivo
```python
with open('exemplo.txt', 'r') as f:
	conteudo = f.read()
	print(conteudo)
```

#### Lendo linha a linha
```python
with open('exemplo.txt', 'r') as f:
	for linha in f:
		print(linha.strip())
```

---

### 6.3. Manipulação de Arquivos CSV

#### Escrevendo em CSV
```python
import csv
with open('dados.csv', 'w', newline='') as f:
	escritor = csv.writer(f)
	escritor.writerow(['nome', 'idade'])
	escritor.writerow(['Ana', 22])
	escritor.writerow(['João', 30])
```

#### Lendo CSV
```python
import csv
with open('dados.csv', 'r') as f:
	leitor = csv.reader(f)
	for linha in leitor:
		print(linha)
```

---

### 6.4. Exercícios Práticos
1. Escreva um programa que grave 5 nomes em um arquivo texto, um em cada linha.
2. Leia e exiba o conteúdo do arquivo criado acima.
3. Crie um arquivo CSV com nome e nota de 3 alunos.
4. Leia o arquivo CSV e mostre a média das notas.
5. Faça um programa que leia um arquivo texto e conte quantas linhas ele possui.

---


## Aula 7: Manipulação de Dados com NumPy e Pandas (Duração: 3h)

### 7.1. Correção dos Exercícios da Aula 6

**Exercício 1:**
```python
with open('nomes.txt', 'w') as f:
	for _ in range(5):
		nome = input('Digite um nome: ')
		f.write(nome + '\n')
```

**Exercício 2:**
```python
with open('nomes.txt', 'r') as f:
	print(f.read())
```

**Exercício 3:**
```python
import csv
with open('alunos.csv', 'w', newline='') as f:
	escritor = csv.writer(f)
	for _ in range(3):
		nome = input('Nome: ')
		nota = input('Nota: ')
		escritor.writerow([nome, nota])
```

**Exercício 4:**
```python
import csv
with open('alunos.csv', 'r') as f:
	leitor = csv.reader(f)
	notas = []
	for linha in leitor:
		notas.append(float(linha[1]))
	print(f"Média das notas: {sum(notas)/len(notas):.2f}")
```

**Exercício 5:**
```python
with open('exemplo.txt', 'r') as f:
	linhas = f.readlines()
	print(f"Total de linhas: {len(linhas)}")
```

---

### 7.2. Introdução ao NumPy

NumPy é uma biblioteca para computação numérica eficiente com arrays multidimensionais.

#### Instalação
```bash
pip install numpy
```

#### Principais operações
```python
import numpy as np
arr = np.array([1, 2, 3, 4])
print(arr.mean())
print(arr.shape)
print(arr * 2)
matriz = np.array([[1, 2], [3, 4]])
print(matriz)
```

---

### 7.3. Introdução ao Pandas

Pandas é uma biblioteca para análise e manipulação de dados tabulares (DataFrames).

#### Instalação
```bash
pip install pandas
```

#### Principais operações
```python
import pandas as pd
df = pd.DataFrame({
	'nome': ['Ana', 'João', 'Maria'],
	'idade': [22, 30, 25]
})
print(df)
print(df['idade'].mean())
df.to_csv('saida.csv', index=False)
df2 = pd.read_csv('saida.csv')
print(df2)
```

#### Leitura de arquivos CSV
```python
import pandas as pd
df = pd.read_csv('alunos.csv', names=['nome', 'nota'])
print(df)
print(df['nota'].astype(float).mean())
```

#### Limpeza de dados
```python
df = pd.DataFrame({'A': [1, 2, None], 'B': [4, None, 6]})
print(df.isnull())
print(df.fillna(0))
print(df.dropna())
```

---

### 7.4. Exercícios Práticos
1. Crie um array NumPy com 10 números e mostre a soma e média.
2. Leia um arquivo CSV com Pandas e mostre as 5 primeiras linhas.
3. Calcule a média da coluna 'nota' de um DataFrame lido de um CSV.
4. Remova valores nulos de um DataFrame e mostre o resultado.
5. Exporte um DataFrame para um novo arquivo CSV.

---


## Aula 8: Visualização de Dados com Matplotlib e Seaborn (Duração: 3h)

### 8.1. Correção dos Exercícios da Aula 7

**Exercício 1:**
```python
import numpy as np
arr = np.arange(1, 11)
print(f"Soma: {arr.sum()} | Média: {arr.mean()}")
```

**Exercício 2:**
```python
import pandas as pd
df = pd.read_csv('alunos.csv', names=['nome', 'nota'])
print(df.head())
```

**Exercício 3:**
```python
print(df['nota'].astype(float).mean())
```

**Exercício 4:**
```python
df = df.dropna()
print(df)
```

**Exercício 5:**
```python
df.to_csv('alunos_limpo.csv', index=False)
```

---

### 8.2. Introdução ao Matplotlib

Matplotlib é uma biblioteca para criação de gráficos em Python.

#### Instalação
```bash
pip install matplotlib
```

#### Exemplos básicos
```python
import matplotlib.pyplot as plt
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]
plt.plot(x, y)
plt.title('Gráfico de Linha')
plt.xlabel('Eixo X')
plt.ylabel('Eixo Y')
plt.show()
```

#### Gráfico de barras
```python
categorias = ['A', 'B', 'C']
valores = [10, 7, 5]
plt.bar(categorias, valores)
plt.title('Gráfico de Barras')
plt.show()
```

#### Histograma
```python
import numpy as np
dados = np.random.randn(100)
plt.hist(dados, bins=10)
plt.title('Histograma')
plt.show()
```

---

### 8.3. Introdução ao Seaborn

Seaborn é uma biblioteca baseada no Matplotlib para visualizações estatísticas mais sofisticadas.

#### Instalação
```bash
pip install seaborn
```

#### Exemplos básicos
```python
import seaborn as sns
import pandas as pd
df = pd.DataFrame({'categoria': ['A', 'B', 'A', 'C'], 'valor': [10, 20, 15, 5]})
sns.barplot(x='categoria', y='valor', data=df)
plt.title('Barplot com Seaborn')
plt.show()
```

#### Gráfico de dispersão
```python
import seaborn as sns
import matplotlib.pyplot as plt
import numpy as np
df = pd.DataFrame({'x': np.random.rand(50), 'y': np.random.rand(50)})
sns.scatterplot(x='x', y='y', data=df)
plt.title('Scatterplot com Seaborn')
plt.show()
```

#### Histograma com Seaborn
```python
import seaborn as sns
import matplotlib.pyplot as plt
import numpy as np
dados = np.random.randn(100)
sns.histplot(dados, bins=10)
plt.title('Histograma com Seaborn')
plt.show()
```

---

### 8.4. Exercícios Práticos
1. Crie um gráfico de linha com Matplotlib mostrando a evolução de uma variável fictícia.
2. Gere um histograma com 100 valores aleatórios usando Seaborn.
3. Faça um gráfico de barras com os nomes e notas de alunos lidos de um CSV.
4. Crie um scatterplot (dispersão) com duas colunas numéricas de um DataFrame.
5. Personalize um gráfico com título, rótulos e cores.

---


## Aula 9: Projetos Práticos e Desafios Finais (Duração: 3h)

### 9.1. Correção dos Exercícios da Aula 8

**Exercício 1:**
```python
import matplotlib.pyplot as plt
x = list(range(1, 11))
y = [v**2 for v in x]
plt.plot(x, y)
plt.title('Evolução Quadrática')
plt.xlabel('X')
plt.ylabel('Y')
plt.show()
```

**Exercício 2:**
```python
import seaborn as sns
import numpy as np
import matplotlib.pyplot as plt
dados = np.random.randn(100)
sns.histplot(dados, bins=10)
plt.title('Histograma Aleatório')
plt.show()
```

**Exercício 3:**
```python
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv('alunos.csv', names=['nome', 'nota'])
plt.bar(df['nome'], df['nota'].astype(float))
plt.title('Notas dos Alunos')
plt.xlabel('Nome')
plt.ylabel('Nota')
plt.show()
```

**Exercício 4:**
```python
import seaborn as sns
import pandas as pd
import numpy as np
df = pd.DataFrame({'x': np.random.rand(50), 'y': np.random.rand(50)})
sns.scatterplot(x='x', y='y', data=df)
plt.title('Dispersão')
plt.show()
```

**Exercício 5:**
```python
plt.plot(x, y, color='red', marker='o')
plt.title('Gráfico Personalizado')
plt.xlabel('Eixo X')
plt.ylabel('Eixo Y')
plt.grid(True)
plt.show()
```

---

### 9.2. Projetos Práticos de Análise de Dados

#### Projeto 1: Análise de Vendas
- Leia um arquivo CSV com dados de vendas (produto, quantidade, valor).
- Calcule o total vendido por produto.
- Gere um gráfico de barras com os resultados.

#### Projeto 2: Análise de Notas de Alunos
- Leia um CSV com nomes e notas.
- Calcule média, maior e menor nota.
- Gere um gráfico de barras e um histograma das notas.

#### Projeto 3: Análise de Dados Meteorológicos
- Baixe um dataset público (ex: temperaturas diárias).
- Limpe dados nulos, calcule médias mensais e gere gráficos de linha.

---

### 9.3. Desafios Finais
1. Crie um DataFrame com dados fictícios de funcionários (nome, idade, salário) e faça análises estatísticas.
2. Importe um dataset real do Kaggle ou IBGE, faça limpeza e análise exploratória.
3. Gere pelo menos 3 tipos de gráficos diferentes com seus dados.
4. Documente seu projeto em um arquivo README próprio, explicando cada etapa.

6. Faça um relatório de insights dos dados analisados.
7. Crie um dashboard simples com Streamlit ou Dash.
8. Implemente testes automatizados para funções do seu projeto.
9. Faça análise de correlação entre variáveis numéricas.
10. Faça análise de valores ausentes e trate-os.
11. Faça análise de outliers e trate-os.
12. Faça análise de distribuição de uma variável numérica.
13. Faça análise de agrupamento (clustering) simples.
14. Faça análise de regressão linear simples.
15. Faça análise de classificação simples.
16. Faça análise de séries temporais simples.
17. Faça análise de dados geográficos simples.
18. Escreva um artigo explicando seu projeto e resultados.

---

## Listas de Exercícios por Aula

### Aula 1: Introdução ao Python e Instalação
1. O que é Python? Explique com suas palavras.
2. Cite 3 vantagens do Python.
3. Instale o Python em seu computador e mostre o comando para verificar a versão.
4. Crie um ambiente virtual e ative-o.
5. Escreva um programa que exiba "Bem-vindo ao Python!".
6. Mostre como usar o interpretador interativo.
7. Declare variáveis dos tipos int, float, str e bool.
8. Faça um programa que peça o nome do usuário e o cumprimente.
9. Mostre exemplos de operadores aritméticos.
10. Mostre exemplos de operadores relacionais.
11. Mostre exemplos de operadores lógicos.
12. Faça um programa que leia dois números e exiba a soma.
13. Faça um programa que leia um número e exiba o dobro.
14. Escreva um comentário de linha única e um de múltiplas linhas.
15. Faça um programa que leia a idade do usuário e exiba se é maior de idade.
16. Faça um programa que leia um número e diga se é positivo ou negativo.
17. Mostre como converter string para inteiro.
18. Mostre como converter float para string.
19. Faça um programa que leia dois números e exiba o maior.
20. Explique a diferença entre input() e print().

### Aula 2: Tipos de Dados e Operadores
1. Crie variáveis de todos os tipos básicos do Python.
2. Faça operações com int e float.
3. Mostre como concatenar strings.
4. Faça um programa que leia um texto e exiba em maiúsculas.
5. Faça um programa que leia um texto e exiba em minúsculas.
6. Faça um programa que leia um número e exiba o quadrado.
7. Faça um programa que leia dois números e exiba a média.
8. Faça um programa que leia um número e exiba se é par ou ímpar.
9. Faça um programa que leia um número e exiba se é múltiplo de 3.
10. Faça um programa que leia um número e exiba se é divisível por 5.
11. Faça um programa que leia um texto e exiba o número de caracteres.
12. Faça um programa que leia um texto e exiba o primeiro caractere.
13. Faça um programa que leia um texto e exiba o último caractere.
14. Faça um programa que leia um número e exiba o resto da divisão por 2.
15. Faça um programa que leia dois números e exiba se são iguais.
16. Faça um programa que leia dois números e exiba se o primeiro é maior.
17. Faça um programa que leia um número e exiba se está entre 10 e 20.
18. Faça um programa que leia um número e exiba se é diferente de 0.
19. Faça um programa que leia um texto e exiba se contém a letra "a".
20. Faça um programa que leia um texto e exiba quantas vezes aparece a letra "e".

### Aula 3: Estruturas de Controle
1. Faça um programa que leia um número e diga se é positivo, negativo ou zero.
2. Faça um programa que leia dois números e exiba o maior.
3. Faça um programa que leia três números e exiba o maior.
4. Faça um programa que leia um número e exiba se é par ou ímpar.
5. Faça um programa que leia um número e exiba a tabuada de 1 a 10.
6. Faça um programa que leia 5 números e exiba a soma.
7. Faça um programa que leia números até digitar 0 e exiba a soma.
8. Faça um programa que leia números até digitar negativo e exiba a quantidade.
9. Faça um programa que leia um texto e conte as vogais.
10. Faça um programa que leia 5 nomes e exiba todos.
11. Faça um programa que leia 10 números e exiba o maior.
12. Faça um programa que leia 10 números e exiba o menor.
13. Faça um programa que leia 10 números e exiba a média.
14. Faça um programa que leia um número e exiba se é primo.
15. Faça um programa que leia um número e exiba todos os divisores.
16. Faça um programa que leia um número e exiba a soma dos dígitos.
17. Faça um programa que leia um texto e exiba se é palíndromo.
18. Faça um programa que leia um texto e exiba o inverso.
19. Faça um programa que leia um número e exiba a sequência de Fibonacci até ele.
20. Faça um programa que leia um número e exiba o fatorial.

### Aula 4: Funções e Modularização
1. Crie uma função que exiba uma mensagem de boas-vindas.
2. Crie uma função que receba dois números e retorne a soma.
3. Crie uma função que receba um número e retorne se é par.
4. Crie uma função que receba um texto e retorne em maiúsculas.
5. Crie uma função que receba uma lista e retorne a soma dos elementos.
6. Crie uma função que receba uma lista e retorne o maior elemento.
7. Crie uma função que receba uma lista e retorne o menor elemento.
8. Crie uma função que receba um número e retorne o fatorial.
9. Crie uma função que receba um texto e retorne o número de vogais.
10. Crie uma função que receba um texto e retorne se é palíndromo.
11. Crie uma função que receba uma lista e retorne a média.
12. Crie uma função que receba dois números e retorne o maior.
13. Crie uma função que receba um número e retorne a sequência de Fibonacci até ele.
14. Crie uma função que receba um número e retorne a soma dos dígitos.
15. Crie uma função que receba uma lista e retorne apenas os pares.
16. Crie uma função que receba uma lista e retorne apenas os ímpares.
17. Crie uma função que receba um texto e retorne o inverso.
18. Crie uma função que receba uma lista e retorne sem duplicatas.
19. Crie um módulo com duas funções e importe em outro arquivo.
20. Crie uma função que receba um nome e idade e retorne uma saudação personalizada.

### Aula 5: Estruturas de Dados
1. Crie uma lista com 10 números e exiba todos.
2. Crie uma tupla com 5 nomes e exiba todos.
3. Crie um dicionário com nome e idade de 3 pessoas.
4. Crie um conjunto com 5 números e exiba todos.
5. Adicione um elemento a uma lista.
6. Remova um elemento de uma lista.
7. Adicione um elemento a um conjunto.
8. Remova um elemento de um conjunto.
9. Adicione um par chave-valor a um dicionário.
10. Remova um par chave-valor de um dicionário.
11. Acesse o terceiro elemento de uma lista.
12. Acesse o último elemento de uma tupla.
13. Verifique se um valor está em uma lista.
14. Verifique se uma chave está em um dicionário.
15. Faça a união de dois conjuntos.
16. Faça a interseção de dois conjuntos.
17. Ordene uma lista de números.
18. Inverta uma lista.
19. Conte quantos elementos tem uma lista.
20. Faça um programa que percorra um dicionário e exiba as chaves e valores.

### Aula 6: Manipulação de Arquivos
1. Crie um arquivo texto e escreva 5 linhas.
2. Leia e exiba o conteúdo de um arquivo texto.
3. Conte quantas linhas tem um arquivo texto.
4. Conte quantas palavras tem um arquivo texto.
5. Escreva uma lista de nomes em um arquivo texto.
6. Leia nomes de um arquivo texto e exiba um por linha.
7. Crie um arquivo CSV com nome e idade de 3 pessoas.
8. Leia um arquivo CSV e exiba os dados.
9. Adicione uma nova linha a um arquivo texto.
10. Apague o conteúdo de um arquivo texto.
11. Faça um programa que copie o conteúdo de um arquivo para outro.
12. Faça um programa que leia um arquivo e exiba apenas as linhas pares.
13. Faça um programa que leia um arquivo e exiba apenas as linhas ímpares.
14. Faça um programa que leia um arquivo e exiba as linhas invertidas.
15. Faça um programa que leia um arquivo e exiba as linhas em ordem alfabética.
16. Faça um programa que leia um arquivo e exiba as linhas sem duplicatas.
17. Faça um programa que leia um arquivo e exiba as linhas que contêm a letra "a".
18. Faça um programa que leia um arquivo e exiba as linhas que começam com "A".
19. Faça um programa que leia um arquivo e exiba as linhas que terminam com ".".
20. Faça um programa que leia um arquivo CSV e exiba a média de uma coluna numérica.

### Aula 7: NumPy e Pandas
1. Crie um array NumPy com 10 números inteiros.
2. Calcule a soma dos elementos de um array NumPy.
3. Calcule a média dos elementos de um array NumPy.
4. Crie uma matriz 3x3 com NumPy.
5. Some duas matrizes NumPy.
6. Multiplique dois arrays NumPy.
7. Crie um DataFrame Pandas com 3 colunas e 5 linhas.
8. Leia um arquivo CSV com Pandas.
9. Exiba as 3 primeiras linhas de um DataFrame.
10. Exiba as 3 últimas linhas de um DataFrame.
11. Calcule a média de uma coluna numérica de um DataFrame.
12. Remova linhas com valores nulos de um DataFrame.
13. Preencha valores nulos de um DataFrame com zero.
14. Exporte um DataFrame para CSV.
15. Filtre linhas de um DataFrame por valor de uma coluna.
16. Agrupe um DataFrame por uma coluna e calcule a média.
17. Crie um DataFrame a partir de um dicionário.
18. Adicione uma nova coluna a um DataFrame.
19. Remova uma coluna de um DataFrame.
20. Faça um gráfico de barras com dados de um DataFrame.

### Aula 8: Visualização de Dados
1. Crie um gráfico de linha com Matplotlib.
2. Crie um gráfico de barras com Matplotlib.
3. Crie um histograma com Matplotlib.
4. Crie um scatterplot com Matplotlib.
5. Personalize um gráfico com título e rótulos.
6. Crie um gráfico de barras com Seaborn.
7. Crie um histograma com Seaborn.
8. Crie um scatterplot com Seaborn.
9. Altere as cores de um gráfico com Seaborn.
10. Adicione uma legenda a um gráfico.
11. Salve um gráfico como imagem.
12. Plote múltiplos gráficos em uma mesma figura.
13. Plote um gráfico de pizza com Matplotlib.
14. Plote um gráfico de caixa (boxplot) com Seaborn.
15. Plote um gráfico de violino com Seaborn.
16. Plote um gráfico de barras empilhadas com Matplotlib.
17. Plote um gráfico de área com Matplotlib.
18. Plote um gráfico de dispersão com diferentes tamanhos de pontos.
19. Plote um gráfico de dispersão com diferentes cores por categoria.
20. Plote um gráfico de linha com múltiplas séries.

### Aula 9: Projetos e Desafios Finais
1. Crie um projeto de análise de vendas com gráficos.
2. Crie um projeto de análise de notas de alunos com gráficos.
3. Crie um projeto de análise de dados meteorológicos.
4. Importe um dataset real do Kaggle e faça análise exploratória.
5. Gere pelo menos 3 tipos de gráficos diferentes com seus dados.
6. Documente seu projeto em um README próprio.
7. Compartilhe seu projeto no GitHub.
8. Faça um relatório de insights dos dados analisados.
9. Crie um dashboard simples com Streamlit ou Dash.
10. Implemente testes automatizados para funções do seu projeto.
11. Faça análise de correlação entre variáveis numéricas.
12. Faça análise de valores ausentes e trate-os.
13. Faça análise de outliers e trate-os.
14. Faça análise de distribuição de uma variável numérica.
15. Faça análise de agrupamento (clustering) simples.
16. Faça análise de regressão linear simples.
17. Faça análise de classificação simples.
18. Faça análise de séries temporais simples.
19. Faça análise de dados geográficos simples.
20. Escreva um artigo explicando seu projeto e resultados.

---

