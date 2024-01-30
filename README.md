# Aplicando Conceitos das Estruturas de Repetição em Python

Este repositório contém exemplos de código em Python que aplicam conceitos das estruturas de repetição. Os códigos foram desenvolvidos como parte das atividades da disciplina de Fundamentos de Algoritmo do curso de Análise e Desenvolvimento de Sistemas (ADS) pela Universidade Federal do Cariri (UFCA). O objetivo principal do cumprimento destas atividades foi fornecer uma prática sólida e consolidar os conceitos fundamentais relacionados aos loop statements em Python, aprofundando a compreensão e o aprimoramento das habilidades de programação nessa linguagem.

## Estrutura do Repositório

A estrutura do repositório foi organizada para proporcionar uma experiência de navegação eficiente e facilitar a revisão dos códigos. Cada atividade está representada por um tópico, dentro do qual você encontrará o repositório dedicado à atividade desenvolvida.

## Atividades

1. **Escreva um programa para imprimir na tela três números, começando de 1 até o 3.**<br>

- ```python
  # 1
  # Impressão em sequência de 1 a 3

  for numero in range(1, 4):
    print(numero)
<br>

2. **Modifique o programa da 1ª. para exibir os números de 1 a 100.**
 
- ```python
  # 2
  # Impressão em sequência de 1 a 100

  for numero in range(1, 101):
    print(numero)
<br> 

3. **Modifique o programa da 2ª questão para exibir os números de 50 a 100.**

- ```python
  # 3
  # Impressão em sequência de 50 a 100

  for numero in range(50, 101):
    print(numero)
<br>
 
4. **Faça um programa para escrever a contagem regressiva do lançamento de um foguete. O programa deve imprimir 10, 9, 8 ..., 1, 0 e Fogo!!! Na tela.**

- ```python
  # 4
  # Contagem regressiva

  for contagem in range(10, -1, -1):
    print(f'Contagem regressiva em {contagem}', end=' ')

    if contagem == 0:
        print('e ... Fogo!!!')
    else:
        print('...')
<br>

5. **Faça um programa para imprimir os números inteiros entre 1 e um valor digitado pelo usuário.**

- ```python
  # 5
  # Imprime inteiros entre 1 e um valor qualquer

  valor = int(input('Digite um valor: '))

  for numero in range(1, valor + 1):
    print(numero)
<br>

6. **Modifique o programa anterior para imprimir os números inteiros entre 1 e um valor digitado pelo usuário, mas, dessa vez, apenas os ímpares.**<br>

- ```python
  # 6
  # Imprime inteiros ímpares entre 1 e um valor qualquer

  valor = int(input('Digite um valor: '))

  for numero in range(1, valor + 1, 2):
    print(numero)
<br>

7. **Escreva um programa que exiba uma lista de opções (menu): Adição, subtração, divisão e multiplicação e sair. Imprima o resultado da operação escolhida entre dois números informados pelo usuário. Repita até que a opção sair seja escolhida.**<br>
   
- [Calculadora Interativa](https://github.com/devitruvius/algoritmo_calculadora_interativa/blob/main/algoritmo_calculadora_interativa.py)
<br>

8. **Elabore um programa que calcule ∑ (𝑗), onde N é informado pelo usuário. Caso o usuário forneça um valor negativo, o programa deve apresentar a mensagem: “Digite apenas valores maiores ou iguais a zero.”**
    
- [Calculadora de Somatória](https://github.com/devitruvius/algoritmo_calculadora_somatoria/blob/main/algoritmo_calculadora_somatoria.py)
<br>

9. **Elabore um programa que deve calcular uma integral, na qual a função deve ser implementada no código fonte. O usuário deve fornecer os limites de integração da função considerada. Divida o intervalo em 10000 partições, e faça um somatório, avaliando a função e somando todos os resultados.   Exemplo: calcule a integral da função f(x) = 2x no intervalo de 0 a 1. Para calcular esta integral, deve ser implementada no código fonte e os intervalos devem ser fornecidos pelo usuário. O programa deve dividir o intervalo em 10000 partes, e atribuir a x o valor do limite inferior, ou seja 0.  A função deve ser avaliada para x = 0 e depois disso, para cada uma das 10000 partições feitas. Todas as vezes que x for avaliado, o resultado deve ser armazenado em um somatório. Este somatório é o resultado da integral.**

- [Calculadora de Funções Integrais](https://github.com/devitruvius/algoritmo_calculadora_integral/blob/main/algoritmo_calculadora_integral.py)
<br>
