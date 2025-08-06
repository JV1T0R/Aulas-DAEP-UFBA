# Lista de Execícios 1

>**Recomendação:**  
É recomendado que cada aluno salve as soluções dos exercícios em seus perfis pessoais do GitHub.  
Isso contribui para a construção de um portfólio profissional e facilita consultas futuras
durante a aprendizagem e desenvolvimento de projetos.

### Questão 1
Desenvolva um programa que:
1. Solicite dois números ao usuário
2. Calcule a soma dos valores
3. Exiba o resultado formatado

<details>
<summary><Strong>Solução</Strong></summary>

```python
    # Solicita os números ao usuário (input retorna strings, convertemos para float)
    num1 = float(input("Digite o primeiro número: "))
    num2 = float(input("Digite o segundo número: "))

    # Cálculo da soma
    soma = num1 + num2

    # Saída formatada
    print(f"A soma é: {soma}")   
```
</details>

<br>  

<hr>

### Questão 2
Elabore um programa que:
1. Leia a base e altura de um retângulo
2. Calcule a área (base × altura)
3. Exiba o resultado com unidades (m²)

<details>
<summary><Strong>Solução</Strong></summary>

```python
    # Entrada de dados
    base = float(input("Digite a base do retângulo: "))
    altura = float(input("Digite a altura do retângulo: "))

    # Cálculo da área 
    area = base * altura

    # Saída formatada
    print(f"A área do retângulo é: {area}")
```
</details>

<br>

<hr>

### Questão 3
Crie um programa que:
1. Leia três notas e seus respectivos pesos
2. Calcule a média ponderada usando a fórmula:  
   `(nota1 × peso1 + nota2 × peso2 + nota3 × peso3) ÷ (peso1 + peso2 + peso3)`
3. Exiba o resultado com 2 casas decimais.

<details>
<summary><Strong>Solução</Strong></summary>

```python
    # Entrada de dados
    nota1 = float(input("Digite a primeira nota: "))
    peso1 = float(input("Digite o peso da primeira nota: "))

    nota2 = float(input("Digite a segunda nota: "))
    peso2 = float(input("Digite o peso da segunda nota: "))

    nota3 = float(input("Digite a terceira nota: "))
    peso3 = float(input("Digite o peso da terceira nota: "))

    # Cálculo da média ponderada
    media_ponderada = (nota1 * peso1 + nota2 * peso2 + nota3 * peso3) / (peso1 + peso2 + peso3)

    # Saída formatada
    print(f"A média ponderada do aluno é: {media_ponderada}")
```
</details>

<br>

<hr>

### Questão 4
Desenvolva um conversor que:
1. Leia uma temperatura em Celsius (°C)
2. Converta para Fahrenheit usando:  
   `F = C × 9/5 + 32`
3. Exiba o resultado com 2 casas decimais e unidade (°F)

<details>
<summary><Strong>Solução</Strong></summary>

```python
    # Entrada de dados
    celsius = float(input("Digite a temperatura em graus Celsius (°C): "))

    # Conversão para Fahrenheit
    fahrenheit = celsius * 9/5 + 32

    # Saída formatada
    print(f"A temperatura em Fahrenheit é: {fahrenheit:.2f} °F") # :.2f limita a 2 casas decimais
```
</details>

<br> 

<hr>

### Questão 5
Elabore um programa que:
1. Leia a força aplicada (em N) e a área da seção transversal (em m²)
2. Calcule a tensão usando:  
   `σ = F ÷ A`
3. Exiba o resultado em Pascal (Pa) com 2 casas decimais

<details>
<summary><Strong>Solução</Strong></summary>

```python
    # Entrada de dados
    forca = float(input("Digite a força aplicada (N): "))
    area = float(input("Digite a área da seção transversal (m²): "))

    # Cálculo da tensão
    tensao = forca / area

    # Saída formatada
    print(f"A tensão no cabo é: {tensao:.2f} Pa") # :.2f limita a 2 casas decimais
```
</details>