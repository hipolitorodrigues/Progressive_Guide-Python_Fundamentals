<div align="center">
   <img height="30" width="40" src="https://github.com/hipolitorodrigues/assets-for-github/blob/985021e61af3982fd9f28be446b106b958f24696/images/01/img-readme-ico.svg">
   <a href="./README.md">
      <img height="30" width="120" src="https://github.com/hipolitorodrigues/assets-for-github/blob/985021e61af3982fd9f28be446b106b958f24696/images/01/img-readme-en.svg">
   </a>
   <a href="./README.pt-BR.md">
      <img height="30" width="60" src="https://github.com/hipolitorodrigues/assets-for-github/blob/985021e61af3982fd9f28be446b106b958f24696/images/01/img-readme-pt-br.svg">
   </a>
</div>

# Guia Progressivo de Fundamentos do Python

Este guia é voltado para programadores que já possuem experiência com outras linguagens, mas são iniciantes em Python. O objetivo é se familiarizar com a sintaxe e os conceitos básicos da linguagem de forma progressiva.

## 1. Conceitos Básicos

### 1.1 Sintaxe e Estrutura Básica
- Indentação obrigatória ao invés de chaves `{}`
- Uso de `:` para definir blocos de código
- Sensível a maiúsculas e minúsculas

```python
if True:
    print("Indentação é obrigatória!")
```

### 1.2 Variáveis e Tipagem Dinâmica
- Python não exige declaração de tipos
- Tipos são inferidos automaticamente

```python
x = 10       # Inteiro
y = 3.14     # Float
nome = "Ana" # String
ativo = True # Booleano
```

### 1.3 Comentários
- Comentário de uma linha: `#`
- Comentário de múltiplas linhas: `""" ... """` ou `''' ... '''`

```python
# Este é um comentário de uma linha
"""
Este é um comentário
de múltiplas linhas
"""
```

## 2. Operadores

### 2.1 Operadores Aritméticos
```python
soma = 10 + 5
subtracao = 10 - 5
multiplicacao = 10 * 5
divisao = 10 / 3       # Retorna float
div_inteira = 10 // 3  # Retorna inteiro
modulo = 10 % 3        # Resto da divisão
potencia = 2 ** 3      # Exponenciação
```

### 2.2 Operadores Lógicos e Comparação
```python
resultado = (10 > 5) and (5 < 8)  # True
resultado = (10 == 5) or (5 != 8) # True
resultado = not (10 > 5)          # False
```

## 3. Estruturas de Controle

### 3.1 Condicionais
```python
x = 10
if x > 5:
    print("Maior que 5")
elif x == 5:
    print("Igual a 5")
else:
    print("Menor que 5")
```

### 3.2 Laços de Repetição
#### 3.2.1 `for`
```python
for i in range(5):
    print(i)  # 0, 1, 2, 3, 4
```

#### 3.2.2 `while`
```python
x = 0
while x < 5:
    print(x)
    x += 1
```

## 4. Estruturas de Dados

### 4.1 Listas
```python
numeros = [1, 2, 3, 4]
numeros.append(5)
numeros.remove(2)
print(numeros)  # [1, 3, 4, 5]
```

#### 4.1.1 Slicing em Listas
```python
lista = [0, 1, 2, 3, 4, 5]
print(lista[1:4])  # [1, 2, 3]
print(lista[:3])   # [0, 1, 2]
print(lista[3:])   # [3, 4, 5]
print(lista[::-1]) # [5, 4, 3, 2, 1, 0]
```

### 4.2 Tuplas
```python
tupla = (1, 2, 3)
print(tupla[0])  # 1
```

### 4.3 Dicionários
```python
dicionario = {"nome": "Ana", "idade": 25}
print(dicionario["nome"])  # Ana
dicionario["idade"] = 26
```

### 4.4 Conjuntos (Sets)
```python
conjunto = {1, 2, 3, 3}
print(conjunto)  # {1, 2, 3} (Sem duplicatas)
```

### 4.5 Manipulação de Strings
```python
texto = "Olá, mundo!"
print(texto.split(","))  # ['Olá', ' mundo!']
print("-".join(["Python", "é", "incrível"]))  # Python-é-incrível
print(texto.replace("mundo", "Python"))  # Olá, Python!
```

## 5. Funções e Programação Funcional

### 5.1 Definição de Funções
```python
def saudacao(nome):
    return f"Olá, {nome}!"
print(saudacao("Ana"))
```

### 5.2 Funções Lambda
```python
quadrado = lambda x: x ** 2
print(quadrado(4))  # 16
```

### 5.3 Map, Filter e Reduce
```python
numeros = [1, 2, 3, 4]
dobro = list(map(lambda x: x * 2, numeros))  # [2, 4, 6, 8]
pares = list(filter(lambda x: x % 2 == 0, numeros))  # [2, 4]
```

## 6. Manipulação de Arquivos
```python
with open("arquivo.txt", "w") as arquivo:
    arquivo.write("Olá, mundo!")
```

## 7. Programação Orientada a Objetos (POO)

### 7.1 Classes e Objetos
```python
class Pessoa:
    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade

    def saudacao(self):
        return f"Olá, meu nome é {self.nome}"

pessoa1 = Pessoa("Ana", 25)
print(pessoa1.saudacao())  # Olá, meu nome é Ana
```

## 8. Tratamento de Exceções
```python
try:
    x = 10 / 0
except ZeroDivisionError:
    print("Erro: divisão por zero")
finally:
    print("Bloco finally sempre é executado")
```

## 9. Módulos e Pacotes

### 9.1 Importação de Módulos
```python
import math
print(math.sqrt(16))  # 4.0
```

### 9.2 Introdução a Pacotes e Bibliotecas
- Utilização de pacotes externos como `numpy`, `pandas`, `requests`.
- Como instalar pacotes com `pip install <pacote>`.

```python
import requests
response = requests.get("https://api.github.com")
print(response.status_code)
```
