# Estruturas de Repetição em Python

Este repositório reúne exemplos de código em Python que foram desenvolvidos como parte das atividades da disciplina de Fundamentos de Algoritmo do curso de Análise e Desenvolvimento de Sistemas (ADS) pela Universidade Federal do Cariri (UFCA). Através da resolução destas atividades, o objetivo principal foi fornecer uma prática sólida e consolidar os conceitos fundamentais relacionados às estruturas de repetição em Python, aprofundando a compreensão e o aprimoramento das habilidades de programação nessa linguagem.

## Estrutura do Repositório

O repositório foi organizado para facilitar a navegação e a revisão dos códigos. Cada bloco de atividade é representado por um tópico, contendo os códigos referentes à atividade específica.

## Atividades

1. **Escreva um programa para imprimir na tela três números, começando de 1 até o 3.**<br>

    ```python
    # Impressão em sequência de 1 a 3
    
    for numero in range(1, 4):
        print(numero)
    ```
<hr>

2. **Modifique o programa da 1ª. para exibir os números de 1 a 100.**

    ```python
    # Impressão em sequência de 1 a 100
    
    for numero in range(1, 101):
      print(numero)
    ```
<hr> 

3. **Modifique o programa da 2ª questão para exibir os números de 50 a 100.**

    ```python
    # Impressão em sequência de 50 a 100
    
    for numero in range(50, 101):
      print(numero)
    ```
<hr>
 
4. **Faça um programa para escrever a contagem regressiva do lançamento de um foguete. O programa deve imprimir 10, 9, 8 ..., 1, 0 e Fogo!!! Na tela.**

    ```python
    # Contagem regressiva
    
    for contagem in range(10, -1, -1):
        print(f'Contagem regressiva em {contagem}', end=' ')
    
        if contagem == 0:
            print('e ... Fogo!!!')
        else:
            print('...')
    ```
<hr>

5. **Faça um programa para imprimir os números inteiros entre 1 e um valor digitado pelo usuário.**

    ```python
    # Imprime inteiros entre 1 e um valor qualquer
    
    valor = int(input('Digite um valor: '))
    
    for numero in range(1, valor + 1):
      print(numero)
    ```
<hr>

6. **Modifique o programa anterior para imprimir os números inteiros entre 1 e um valor digitado pelo usuário, mas, dessa vez, apenas os ímpares.**<br>

    ```python
    # Imprime inteiros ímpares entre 1 e um valor qualquer
    
    valor = int(input('Digite um valor: '))
    
    for numero in range(1, valor + 1, 2):
      print(numero)
    ```
<hr>

7. **Escreva um programa que exiba uma lista de opções (menu): Adição, subtração, divisão e multiplicação e sair. Imprima o resultado da operação escolhida entre dois números informados pelo usuário. Repita até que a opção sair seja escolhida.**

    ```python
    # Calculadora Interativa
    
    while True:
    
      print('Menu:')
      print('1. Adição')
      print('2. Subtração')
      print('3. Multiplicação')
      print('4. Divisão')
      print('5. Sair')
    
      escolha = input('Escolha uma opção (1-5): ')
    
      # Encerrando
      if escolha == '5':
        print('Programa encerrado')
        break
    
      # Entrada dos dados
      elif escolha in ('1', '2', '3', '4'):
        num1 = float(input('Digite o primeiro número: '))
        num2 = float(input('Digite o segundo número: '))
    
        # Adição
        if escolha == '1':
          resultado = num1 + num2
          print(f'Resultado da adição: {resultado}')
        # Subtração
        elif escolha == '2':
          resultado = num1 - num2
          print(f'Resultado da subtração: {resultado}')
        # Multiplicação
        elif escolha == '3':
          resultado = num1 * num2
          print(f'Resultado da multiplicação: {resultado}')
        # Divisão
        elif escolha == '4':
          # Evitando a divisão por zero
          if num2 != 0:
            resultado = num1 / num2
            print(f'Resultado da divisão: {resultado}')
          else:
            print('Erro: Divisão por zero.')
      else:
          print('Opção inválida. Por favor, escolha uma opção válida.')
    ```
<hr>

8. **Elabore um programa que calcule ∑ (𝑗), onde N é informado pelo usuário. Caso o usuário forneça um valor negativo, o programa deve apresentar a mensagem: “Digite apenas valores maiores ou iguais a zero.”**    

    ```python
    # Calculadora de Somatória
    
    N = int(input('Digite um valor para N: '))
    
    if N < 0:
      print('Digite apenas valores maiores ou iguais a zero.')
    else:
      soma = sum(range(1, N + 1))
      print(f'A soma dos números de 1 até {N} é: {soma}')
    ```
<hr>

9. **Elabore um programa que deve calcular uma integral, na qual a função deve ser implementada no código fonte. O usuário deve fornecer os limites de integração da função considerada. Divida o intervalo em 10000 partições, e faça um somatório, avaliando a função e somando todos os resultados.   Exemplo: calcule a integral da função f(x) = 2x no intervalo de 0 a 1. Para calcular esta integral, deve ser implementada no código fonte e os intervalos devem ser fornecidos pelo usuário. O programa deve dividir o intervalo em 10000 partes, e atribuir a x o valor do limite inferior, ou seja 0.  A função deve ser avaliada para x = 0 e depois disso, para cada uma das 10000 partições feitas. Todas as vezes que x for avaliado, o resultado deve ser armazenado em um somatório. Este somatório é o resultado da integral.**

    ```python
    # Calculadora de Integral
    
    def funcao(x):
        return 2 * x  # f(x) = 2x
    
    # Solicita ao usuário os limites de integração
    limite_inferior = float(input("Digite o limite inferior de integração: "))
    limite_superior = float(input("Digite o limite superior de integração: "))
    
    num_particoes = 10000
    
    tamanho_particao = (limite_superior - limite_inferior) / num_particoes
    
    # Somatório
    soma_resultados = 0
    
    # Avaliando a função nas partições e somando os resultados
    for i in range(num_particoes + 1):
        # Calculando o valor de x para a partição atual
        x = limite_inferior + i * tamanho_particao
    
        # Avaliando a função no ponto x e adicionando ao somatório
        resultado_parcial = funcao(x)
        soma_resultados += resultado_parcial
    
    # Multiplicando a soma pelo tamanho de cada partição para obter o resultado da integral
    resultado_integral = soma_resultados * tamanho_particao
    
    # Resultado
    print(f"O resultado da integral é: {round(resultado_integral, 2)}")
    ```
<hr>

## Navegação
* **Atividade 1: Pseudocódigo**
   - [Repositório da Lista de Atividades I](https://github.com/devitruvius/FA-pseudocodigos-atividades)

* **Atividade 2: Aplicando Conceitos das Estruturas de Condição em Python**
   - [Repositório da Lista de Atividades II](https://github.com/devitruvius/FA-python-conditional-statement)

* **Atividade 3: Aplicando Conceitos das Estruturas de Repetição em Python**
   - ***Repositório da Lista de Atividades III***

* **Atividade 4: Aplicando Conceitos das Estruturas de Listas em Python**
   - [Repositório da Lista de Atividades IV](https://github.com/devitruvius/ADS-python-lists)

* **Atividade 5: Aplicando Conceitos das Estruturas de Funções em Python**
   - [Repositório da Lista de Atividades V](https://github.com/devitruvius/ADS-python-functions)

* **Repositório Pai: Fundamentos de Algoritmos**
   - [Fundamentos de Algoritmos](https://github.com/devitruvius/ADS-fundamentos-de-algoritmos)
 
## Licença

Este repositório está licenciado sob a licença [MIT](https://choosealicense.com/licenses/mit/).
