# Lista de Exercícios 2

> **Recomendação:**  
É recomendado que cada aluno salve as soluções dos exercícios em seus perfis pessoais do GitHub.  
Isso contribui para a construção de um portfólio profissional e facilita consultas futuras
durante a aprendizagem e desenvolvimento de projetos.

### Questão 1 
Uma empresa de engenharia utiliza cabos para sustentar cargas em um projeto.  
Crie um programa que leia o **peso da carga (em kg)** e verifique se ela está:
- **Abaixo de 500 kg:** exibir `"Carga dentro do limite seguro"`.
- **Entre 500 kg e 1000 kg:** exibir `"Carga próxima ao limite máximo"`.
- **Acima de 1000 kg:** exibir `"Carga acima do limite permitido!"`.

<details>
<summary><strong>Solução</strong></summary>

```python
# Entrada de dados
peso = float(input("Digite o peso da carga (kg): "))

# Verificação das condições
if peso < 500:
    print("Carga dentro do limite seguro.")
elif peso <= 1000:
    print("Carga próxima ao limite máximo.")
else:
    print("Carga acima do limite permitido!")
```
</details> 

<hr>

### Questão 2
Elabore um programa que leia o **rendimento (%) de um motor** e classifique-o conforme a tabela:
- Rendimento < 40% → `"Baixa eficiência"`
- Rendimento entre 40% e 70% → `"Eficiência média"`
- Rendimento ≥ 70% → `"Alta eficiência"`

<details>
<summary><Strong>Solução</Strong></summary>

```python
    # Entrada de dados
    rendimento = float(input("Digite o rendimento do motor (%): "))

    # Estrutura condicional para classificação
    if rendimento < 40:
        print("Baixa eficiência.")
    elif rendimento < 70:
        print("Eficiência média.")
    else:
        print("Alta eficiência.") 
```
</details>

<hr>

### Questão 3 
Uma linha de produção testa a resistência de peças. Desenvolva um programa que:
1. Leia a resistência (em N) de 5 peças
2. Conte quantas têm resistência ≥ 100 N (`aprovadas`)
3. Conte quantas têm resistência < 100 N (`reprovadas`)
4. Exiba os totais ao final

<details>
<summary><Strong>Solução</Strong></summary>

```python
    # Inicialização dos contadores
    aprovadas = 0
    reprovadas = 0

    # Loop para ler a resistência de 5 peças
    for i in range(1, 6):
        resistencia = float(input(f"Digite a resistência da peça {i} (N): "))
    
        # Verificação de qualidade
        if resistencia >= 100:
            aprovadas += 1  # soma mais uma peça aprovada
        else:
            reprovadas += 1  # soma mais uma peça reprovada

    # Exibição do resultado
    print(f"Peças aprovadas: {aprovadas}")
    print(f"Peças reprovadas: {reprovadas}")
```
</details>

<hr>

### Questão 4 
Desenvolva um sistema para:
1. Perguntar quantas leituras de temperatura serão realizadas
2. Ler cada temperatura (em °C) usando `while`
3. Calcular e exibir a média das temperaturas

<details>
<summary><Strong>Solução</Strong></summary>

```python
    # Entrada de dados
    qtd_leituras = int(input("Quantas leituras de temperatura serão realizadas? "))

    # Inicialização de variáveis
    soma_temperaturas = 0
    contador = 0

    # Loop while para ler as temperaturas
    while contador < qtd_leituras:
        temp = float(input(f"Digite a temperatura {contador + 1} (°C): "))
        soma_temperaturas += temp # acumula as temperaturas
        contador += 1 # incrementa o contador

    # Cálculo da média
    media = soma_temperaturas / qtd_leituras

    # Exibição do resultado
    print(f"A média das temperaturas é: {media:.2f} °C")
```
</details>

<hr>

### Questão 5
Crie um programa que simule o carregamento de uma máquina:
1. Inicie com carga = 0 kg
2. Solicite valores de carga adicionados iterativamente
3. Some os valores até atingir/exceder 1000 kg
4. Exiba: `"Carga máxima atingida com X kg"`

<details>
<summary><Strong>Solução</Strong></summary>

```python
    # Inicializa a variável da carga total
    carga_total = 0

    # Loop até que a carga total atinja ou ultrapasse 1000 kg
    while carga_total < 1000:
        carga = float(input("Digite a carga adicionada (kg): "))
        carga_total += carga  # soma a carga ao total

    # Exibe a carga final
    print(f"Carga máxima atingida com {carga_total} kg.")
```
</details>  
