# calculadora de imposto de renda

def calcular_imposto_renda(salario_bruto):
    """
    calcula o imposto de renda devido com base no salário bruto informado.

    parâmetros:
        salario_bruto (float): valor do salário bruto do contribuinte.

    retorno:
        float: valor do imposto de renda devido.
    """
    # verifica a faixa salarial e aplica a alíquota correspondente
    if salario_bruto <= 2112:
        imposto_devido = 0
    elif salario_bruto <= 2826.65:
        imposto_devido = salario_bruto * 0.075 - 158.40
    elif salario_bruto <= 3751.05:
        imposto_devido = salario_bruto * 0.15 - 370.40
    elif salario_bruto <= 4664.68:
        imposto_devido = salario_bruto * 0.225 - 651.73
    else:
        imposto_devido = salario_bruto * 0.275 - 884.96

    # impede que o valor do imposto seja negativo
    if imposto_devido < 0:
        imposto_devido = 0

    return imposto_devido


def calcular_salario_liquido(salario_bruto):
    """
    calcula o salário líquido subtraindo o imposto de renda do salário bruto.

    parâmetros:
        salario_bruto (float): valor do salário bruto do contribuinte.

    retorno:
        float: valor do salário líquido após o desconto do imposto.
    """
    imposto = calcular_imposto_renda(salario_bruto)
    return salario_bruto - imposto


# solicita ao usuário o valor do salário bruto
entrada_salario = float(input("Digite seu salário bruto: R$ "))

# calcula o imposto de renda devido
valor_imposto = calcular_imposto_renda(entrada_salario)

# calcula o salário líquido
salario_liquido = calcular_salario_liquido(entrada_salario)

# exibe os resultados formatados para duas casas decimais
print("\nSalário Bruto: R$ {:.2f}".format(entrada_salario))
print("Imposto de Renda: R$ {:.2f}".format(valor_imposto))
print("Salário Líquido: R$ {:.2f}".format(salario_liquido))
