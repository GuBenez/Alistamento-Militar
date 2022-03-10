#Faça um programa que leia o ano de nascimento de um jovem e informe, de acordo com a sua idade, 
se ele ainda vai se alistar ao serviço militar, se é a hora exata de se alistar ou se já passou do 
tempo do alistamento. Seu programa também deverá mostrar o tempo que falta ou que passou do prazo.

from datetime import date
hoje = date.today().year
idade = int(input("Insira o seu ano de nascimento: "))
sexo = str(input("Digite 'M' para Masculino ou 'F' para Feminino:"))
alistamento = hoje - idade

if alistamento == 18 and sexo == "M":
    print("Você deve realizar seu alistamento IMEDIATAMENTE!")
elif alistamento > 18 and sexo == "M":
    print("Você já deveria ter se alistado há {} anos".format(alistamento - 18))
elif alistamento < 18 and sexo == "M":
    print("O seu alistamentro militar será em {} anos".format(18 - alistamento))
else:
    print("Você não precisará se alistar")