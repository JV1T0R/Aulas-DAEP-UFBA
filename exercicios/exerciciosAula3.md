# Lista de Exercícios 3

> **Recomendação:**  
É recomendado que cada aluno salve as soluções dos exercícios em seus perfis pessoais do GitHub.  
Isso contribui para a construção de um portfólio profissional e facilita consultas futuras
durante a aprendizagem e desenvolvimento de projetos.

### Questão 1
Uma fábrica produz um número variável de peças diariamente.  
Crie um programa que:
1. Leia a **quantidade de peças produzidas** em cada um dos 5 dias da semana e armazene os valores em uma **lista**.  
2. Exiba:
   - O **total produzido na semana**.
   - A **média de produção por dia**. 

<details>
<summary><strong>Solução</strong></summary>

```python
# Lista para armazenar a produção diária
producao = []

# Entrada de dados
for i in range(1, 6):
    quantidade = int(input(f"Digite a quantidade de peças produzidas no dia {i}: "))
    producao.append(quantidade)  # adiciona na lista

# Cálculos
total = sum(producao)
media = total / len(producao)

# Saída de resultados
print(f"Total produzido na semana: {total}")
print(f"Média de produção por dia: {media:.2f}")
```
</details>

<br>  

<hr>

### Questão 2
Uma empresa armazena informações de peças em um **dicionário**, onde a chave é o **nome da peça** e o valor é a **quantidade disponível em estoque**.  
Crie um programa que:
1. Permita cadastrar 3 peças (nome e quantidade).  
2. Solicite ao usuário o **nome de uma peça** e informe a quantidade em estoque.

<details>
<summary><strong>Solução</strong></summary>

```python
# Criação do dicionário
estoque = {}

# Cadastro de 3 peças
for i in range(3):
    nome = input("Digite o nome da peça: ")
    qtd = int(input("Digite a quantidade em estoque: "))
    estoque[nome] = qtd  # adiciona no dicionário

# Consulta
busca = input("Qual peça deseja consultar? ")
if busca in estoque:
    print(f"A quantidade em estoque de {busca} é {estoque[busca]}")
else:
    print("Peça não encontrada no estoque.")
```
</details>

<br>  

<hr>

### Questão 3
Dada a lista de produção diária de uma máquina em peças por turno: `[120, 85, 140, 60, 200, 90]`  
Crie um programa que:
1. Ordene os valores de produção em ordem **crescente e decrescente**.  
2. Mostre a **maior e a menor produção registrada**.

<details>
<summary><strong>Solução</strong></summary>

```python
# Lista inicial
producao = [120, 85, 140, 60, 200, 90]

# Ordenação
ordem_crescente = sorted(producao)
ordem_decrescente = sorted(producao, reverse=True)

# Maior e menor produção
maior = max(producao)
menor = min(producao)

# Saída
print(f"Produção em ordem crescente: {ordem_crescente}")
print(f"Produção em ordem decrescente: {ordem_decrescente}")
print(f"Maior produção: {maior}")
print(f"Menor produção: {menor}")

```
</details>

<br>  

<hr>

### Questão 4
Um sensor registra a **temperatura (°C)** e a **pressão (Pa)** em determinado instante de um processo industrial.  
Crie um programa que:
1. Leia 3 registros contendo temperatura e pressão.  
2. Armazene os registros em **tuplas dentro de uma lista**.  
3. Exiba todos os registros coletados.

<details>
<summary><strong>Solução</strong></summary>

```python
# Lista para armazenar os registros
registros = []

# Leitura dos dados
for i in range(3):
    temp = float(input("Digite a temperatura (°C): "))
    press = float(input("Digite a pressão (Pa): "))
    registros.append((temp, press))  # cria a tupla e adiciona

# Exibição dos registros
print("Registros coletados:")
for idx, (t, p) in enumerate(registros, start=1):
    print(f"{idx} - Temperatura: {t}°C | Pressão: {p} Pa")
```
</details>

<br>  

<hr>

### Questão 5
A produção de peças de uma máquina durante 6 meses foi: `[200, 250, 180, 300, 280, 350]`.  
Crie um programa que utilize a biblioteca **Matplotlib** para:
1. Plotar um gráfico de linha mostrando a produção mensal.  
2. Exibir rótulos para os meses (1 a 6) e a quantidade produzida.

<details>
<summary><strong>Solução</strong></summary>

```python
import matplotlib.pyplot as plt

# Dados
meses = [1, 2, 3, 4, 5, 6]
producao = [200, 250, 180, 300, 280, 350]

# Criação do gráfico
plt.plot(meses, producao, marker='o', linestyle='-', color='b')

# Adicionando títulos e rótulos
plt.title("Produção Mensal de Peças")
plt.xlabel("Meses")
plt.ylabel("Quantidade Produzida")

# Exibição do gráfico
plt.grid(True)
plt.show()
```
</details>