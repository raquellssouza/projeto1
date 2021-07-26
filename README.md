# projeto1def calculate():
    operation = input('''
Por favor, digite a operação matemática que você gostaria de Fazer:
+ Para adição
- Para subtração
* Para multiplicação
/ Para Divisão
''')
import time
t1 = time.time()

# código aqui


def calculate():
    operation = input('''
Por favor, digite a operação matemática que você gostaria de Fazer:
+ Para adição
- Para subtração
* Para multiplicação
/ Para Divisão
''')

    number_1 = int(input('Por favor insira o primeiro número: '))
    number_2 = int(input('Por favor insira o segundo número: '))

    if operation == '+':
        print('{} + {} = '.format(number_1, number_2))
        print(number_1 + number_2)

    elif operation == '-':
        print('{} - {} = '.format(number_1, number_2))
        print(number_1 - number_2)

    elif operation == '*':
        print('{} * {} = '.format(number_1, number_2))
        print(number_1 * number_2)

    elif operation == '/':
        print('{} / {} = '.format(number_1, number_2))
        print(number_1 / number_2)

    else:
        print('Você não digitou um operador válido, execute o programa novamente.')

    # Add again() function to calculate() function
    again()

def again():
    calc_again = input('''
Você quer fazer outro calculo?
precione s para sim e n para não.
''')

    if calc_again.upper() == 's':
        calculate()
    elif calc_again.upper() == 'n':
        print('até logo.')
    else:
        again()

calculate()
tempoExec = time.time() - t1
print("Tempo de execução: {} segundos".format(tempoExec))
