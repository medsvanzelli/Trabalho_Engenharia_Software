# Trabalho_Engenharia_Software

from dataclasses import dataclass


@dataclass
class Funcionario:
    nome: str
    idade: float


def ler_funcionario(numero: int) -> Funcionario:
    print(f'Funcionário de número {numero}')
    nome = input(f'Digite a o nome: ')
    idade = float(input(f'Digite a idade: '))
    return Funcionario(nome, idade)


def mais_velho(a: Funcionario, b: Funcionario) -> Funcionario:
    if a.idade > b.idade:
        return a
    return b


a = ler_funcionario(1)
b = ler_funcionario(2)
c = ler_funcionario(3)

funcionario_mais_velho = mais_velho(mais_velho(a, b), c)
print(f'O mais velho é {funcionario_mais_velho.nome}')