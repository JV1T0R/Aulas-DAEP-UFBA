# Lista de Exercícios 4

> **Recomendação:**  
É recomendado que cada aluno salve as soluções dos exercícios em seus perfis pessoais do GitHub.  
Isso contribui para a construção de um portfólio profissional e facilita consultas futuras
durante a aprendizagem e desenvolvimento de projetos.

### Questão 1
Crie uma **função** que receba como parâmetros a **potência útil (W)** e a **potência total (W)** de uma máquina e retorne a **eficiência (%)**.  
Em seguida, solicite os valores ao usuário, chame a função e exiba o resultado formatado.

<details>
<summary><strong>Solução</strong></summary>

```python
# Definição da função para calcular a eficiência
def calcular_eficiencia(potencia_util, potencia_total):
    eficiencia = (potencia_util / potencia_total) * 100
    return eficiencia

# Programa principal
potencia_util = float(input("Digite a potência útil da máquina (W): "))
potencia_total = float(input("Digite a potência total da máquina (W): "))

resultado = calcular_eficiencia(potencia_util, potencia_total)

# Exibição do resultado formatado com 2 casas decimais
print(f"A eficiência da máquina é de {resultado:.2f}%")
```
</details> 

<hr>

### Questão 2 
Implemente duas funções:
1. Uma função `converter_celsius_fahrenheit(c)` que converta graus Celsius para Fahrenheit.  
2. Uma função `converter_fahrenheit_celsius(f)` que faça a conversão inversa.  

Permita que o usuário escolha qual conversão deseja realizar, reutilizando as funções criadas.

<details>
<summary><strong>Solução</strong></summary>

```python
# Função para converter Celsius para Fahrenheit
def converter_celsius_fahrenheit(celsius):
    return (celsius * 9/5) + 32

# Função para converter Fahrenheit para Celsius
def converter_fahrenheit_celsius(fahrenheit):
    return (fahrenheit - 32) * 5/9

# Programa principal
temperatura = float(input("Digite a temperatura: "))
escala = input("Informe a escala da temperatura digitada (C para Celsius / F para Fahrenheit): ").strip().upper()

# Condicional para realizar a conversão correta
if escala == "C":
    resultado = converter_celsius_fahrenheit(temperatura)
    print(f"{temperatura:.2f}°C equivalem a {resultado:.2f}°F")
elif escala == "F":
    resultado = converter_fahrenheit_celsius(temperatura)
    print(f"{temperatura:.2f}°F equivalem a {resultado:.2f}°C")
else:
    print("Escala inválida! Por favor, utilize 'C' para Celsius ou 'F' para Fahrenheit.")
```
</details>

<br>  

<hr>

### Questão 3 
Utilizando o arquivo `manufacturing_dataset.csv`, crie um programa em Python que:
1. Leia os dados utilizando a biblioteca **pandas**.  
2. Exiba a quantidade **total de peças produzidas** (`Units_Produced`) no dataset.  
3. Mostre também a **média de produção por registro**.

<details>
<summary><strong>Solução</strong></summary>

```python
import pandas as pd

# Leitura do arquivo CSV
df = pd.read_csv("manufacturing_dataset.csv")

# Soma total de peças produzidas
total_produzidas = df["Units Produced"].sum()

# Média de produção por registro
media_producao = df["Units Produced"].mean()

# Exibição dos resultados
print(f"Total de peças produzidas: {total_produzidas}")
print(f"Média de produção por registro: {media_producao:.2f}")
```
</details>

<br>  

<hr>

### Questão 4 
Com base nos dados do arquivo `manufacturing_dataset.csv`, desenvolva um programa que:
1. Filtre e exiba apenas as linhas onde o número de **Defects seja maior que 0**.  
2. Mostre quantos registros atendem a esse critério.  
3. Calcule a **porcentagem de produtos com defeito** em relação ao total produzido.

<details>
<summary><strong>Solução</strong></summary>

```python
import pandas as pd

# Leitura do arquivo CSV
df = pd.read_csv("manufacturing_dataset.csv")

# Filtrar linhas com defeitos
produtos_com_defeito = df.query('Defects > 0')

# Contagem de registros com defeitos
qtd_com_defeito = len(produtos_com_defeito)

# Cálculo da porcentagem de produtos defeituosos
total_produzidas = df["Units Produced"].sum()
total_defeituosas = produtos_com_defeito["Defects"].sum()
porcentagem_defeitos = (total_defeituosas / total_produzidas) * 100

# Exibição dos resultados
print("Registros com defeitos encontrados:")
display(produtos_com_defeito)

print(f"\nQuantidade de registros com defeitos: {qtd_com_defeito}")
print(f"Porcentagem de produtos com defeito: {porcentagem_defeitos:.2f}%")
```
</details>

<br>  

<hr>

### Questão 5
A partir dos dados do arquivo `manufacturing_dataset.csv`, crie um programa que:
1. Agrupe as informações por **Product_Type**.  
2. Calcule a **soma total de unidades produzidas** para cada tipo de produto.  
3. Exiba os resultados em ordem decrescente de produção. 

<details>
<summary><strong>Solução</strong></summary>

```python
import pandas as pd

# Leitura do arquivo CSV
df = pd.read_csv("manufacturing_dataset.csv")

# Agrupar por tipo de produto e somar unidades
producao_por_tipo = df.groupby("Product Type")["Units Produced"].sum()

# Ordenar resultados em ordem decrescente
producao_ordenada = producao_por_tipo.sort_values(ascending=False)

# Exibir resultados
print("Produção total por tipo de produto:")
print(producao_ordenada)
```
</details>