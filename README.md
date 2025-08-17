
# Introdução ao Python: Do Básico ao Especialista em Manipulação de Dados

## Sumário
- [Sobre o Python](#sobre-o-python)
- [Instalação e Configuração](#instalacao-e-configuracao)
- [Primeiros Passos](#primeiros-passos)
- [Estruturas de Dados Básicas](#estruturas-de-dados-basicas)
- [Controle de Fluxo](#controle-de-fluxo)
- [Funções e Módulos](#funcoes-e-modulos)
- [Trabalhando com Arquivos](#trabalhando-com-arquivos)
- [Manipulação de Dados com Bibliotecas](#manipulacao-de-dados-com-bibliotecas)
- [Visualização de Dados](#visualizacao-de-dados)
- [Projetos e Práticas Avançadas](#projetos-e-praticas-avancadas)
- [Referências e Materiais Complementares](#referencias-e-materiais-complementares)

---

## Sobre o Python
Python é uma linguagem de programação de alto nível, interpretada, de fácil leitura e escrita. É amplamente utilizada em ciência de dados, inteligência artificial, automação, desenvolvimento web, entre outras áreas.

**Principais características:**
- Sintaxe simples e clara
- Grande comunidade e vasta documentação
- Multiplataforma
- Rico ecossistema de bibliotecas

---

## Instalação e Configuração
1. **Download:** [python.org/downloads](https://www.python.org/downloads/)
2. **Verificação:**
	 ```bash
	 python --version
	 ```
3. **Ambientes Virtuais:**
	 ```bash
	 python -m venv venv
	 source venv/bin/activate  # Linux/Mac
	 venv\Scripts\activate    # Windows
	 ```

---

## Primeiros Passos
- **Hello World:**
	```python
	print("Hello, World!")
	```
- **Tipos de Dados:** int, float, str, bool
- **Operadores:** aritméticos, lógicos, relacionais

---

## Estruturas de Dados Básicas
- **Listas:**
	```python
	lista = [1, 2, 3]
	lista.append(4)
	```
- **Tuplas:**
	```python
	tupla = (1, 2, 3)
	```
- **Dicionários:**
	```python
	dicionario = {"chave": "valor"}
	```
- **Conjuntos:**
	```python
	conjunto = {1, 2, 3}
	```

---

## Controle de Fluxo
- **Condicionais:**
	```python
	if x > 0:
			print("Positivo")
	elif x < 0:
			print("Negativo")
	else:
			print("Zero")
	```
- **Laços:**
	```python
	for i in range(5):
			print(i)

	while x < 10:
			x += 1
	```

---

## Funções e Módulos
- **Definindo funções:**
	```python
	def soma(a, b):
			return a + b
	```
- **Importando módulos:**
	```python
	import math
	print(math.sqrt(16))
	```

---

## Trabalhando com Arquivos
- **Leitura e escrita:**
	```python
	with open('arquivo.txt', 'r') as f:
			conteudo = f.read()

	with open('saida.txt', 'w') as f:
			f.write('Olá, mundo!')
	```

---

## Manipulação de Dados com Bibliotecas
### 1. **NumPy**
- Arrays e operações matemáticas eficientes.
	```python
	import numpy as np
	arr = np.array([1, 2, 3])
	print(arr.mean())
	```

### 2. **Pandas**
- Estruturas DataFrame e Series para análise de dados.
	```python
	import pandas as pd
	df = pd.read_csv('dados.csv')
	print(df.head())
	```
- Limpeza, filtragem, agrupamento e manipulação de dados.

### 3. **Openpyxl / xlrd**
- Manipulação de arquivos Excel.

### 4. **Requests**
- Consumo de APIs e dados web.
	```python
	import requests
	r = requests.get('https://api.github.com')
	print(r.json())
	```

---

## Visualização de Dados
### 1. **Matplotlib**
- Gráficos básicos e avançados.
	```python
	import matplotlib.pyplot as plt
	plt.plot([1, 2, 3], [4, 5, 6])
	plt.show()
	```

### 2. **Seaborn**
- Visualizações estatísticas aprimoradas.
	```python
	import seaborn as sns
	sns.histplot(df['coluna'])
	plt.show()
	```

---

## Projetos e Práticas Avançadas
- **ETL (Extract, Transform, Load)**
- **Automação de tarefas**
- **Dashboards interativos (Dash, Streamlit)**
- **Machine Learning (scikit-learn, TensorFlow, PyTorch)**
- **Boas práticas: testes, documentação, versionamento**

---

## Referências e Materiais Complementares
- [Documentação Oficial Python](https://docs.python.org/pt-br/3/)
- [Curso Python - Curso em Vídeo](https://www.cursoemvideo.com/course/curso-python-3/)
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [NumPy Documentation](https://numpy.org/doc/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
- [Seaborn Documentation](https://seaborn.pydata.org/)
- [Real Python](https://realpython.com/)
