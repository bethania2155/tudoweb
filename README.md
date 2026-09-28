# tudoweb
simulador de opinião
Python 3.14.7 (tags/v3.14.7:823f032, Aug  5 2026, 10:51:32) [MSC v.1944 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
... total_entrevistados = int(input("Digite a quantidade de entrevistados: "))
...
... # Laço para coletar as respostas de cada cliente
... for i in range(total_entrevistados):
...     print(f"\n--- Entrevistado {i+1} de {total_entrevistados} ---")
...
...     nome = input("Digite o nome: ")
...     idade = int(input("Digite a idade: "))
...
...     # Exibe as opções de opinião
...     print("Qual a sua opinião sobre o atendimento?")
...     print("1 - EXCELENTE")
...     print("2 - BOM")
...     print("3 - RUIM")
...
...     opiniao = int(input("Digite o número correspondente à sua opinião: "))
...
...     # Validação da resposta com estruturas de decisão
...     if opiniao == 1:
...         qtd_excelente += 1
...     elif opiniao == 3:
...         qtd_ruim += 1
...
... # Exibição dos resultados finais
... print("\n" + "="*30)
... print("      RESULTADO DA PESQUISA      ")
... print("="*30)
... print(f"a) Quantidade de respostas 'EXCELENTE': {qtd_excelente}")
... print(f"b) Quantidade de respostas 'RUIM': {qtd_ruim}")
...
Digite a quantidade de entrevistados: 10

--- Entrevistado 1 de 10 ---
Digite o nome: Bellatrix
Digite a idade: 40
Qual a sua opinião sobre o atendimento?
1 - EXCELENTE
2 - BOM
3 - RUIM
Digite o número correspondente à sua opinião: 3

--- Entrevistado 2 de 10 ---
Digite o nome: Corlys
Digite a idade: 50
Qual a sua opinião sobre o atendimento?
1 - EXCELENTE
2 - BOM
3 - RUIM
Digite o número correspondente à sua opinião: 2

--- Entrevistado 3 de 10 ---
Digite o nome: Tyrion
Digite a idade: 24
Qual a sua opinião sobre o atendimento?
1 - EXCELENTE
2 - BOM
3 - RUIM
Digite o número correspondente à sua opinião: 1

--- Entrevistado 4 de 10 ---
Digite o nome: Melisandre
Digite a idade: 55
Qual a sua opinião sobre o atendimento?
1 - EXCELENTE
2 - BOM
3 - RUIM
Digite o número correspondente à sua opinião: 2

--- Entrevistado 5 de 10 ---
Digite o nome: Andromeda
Digite a idade: 36
Qual a sua opinião sobre o atendimento?
1 - EXCELENTE
2 - BOM
3 - RUIM
Digite o número correspondente à sua opinião: 1

--- Entrevistado 6 de 10 ---
Digite o nome: Lucius
Digite a idade: 39
Qual a sua opinião sobre o atendimento?
1 - EXCELENTE
2 - BOM
3 - RUIM
Digite o número correspondente à sua opinião: 3

--- Entrevistado 7 de 10 ---
Digite o nome: Renly
Digite a idade: 27
Qual a sua opinião sobre o atendimento?
1 - EXCELENTE
2 - BOM
3 - RUIM
Digite o número correspondente à sua opinião: 2

--- Entrevistado 8 de 10 ---
Digite o nome: Cersei
Digite a idade: 34
Qual a sua opinião sobre o atendimento?
1 - EXCELENTE
2 - BOM
3 - RUIM
Digite o número correspondente à sua opinião: 3

--- Entrevistado 9 de 10 ---
Digite o nome: Jaime
Digite a idade: 34
Qual a sua opinião sobre o atendimento?
1 - EXCELENTE
2 - BOM
3 - RUIM
Digite o número correspondente à sua opinião: 2

--- Entrevistado 10 de 10 ---
Digite o nome: Druella
Digite a idade: 70
Qual a sua opinião sobre o atendimento?
1 - EXCELENTE
2 - BOM
3 - RUIM
Digite o número correspondente à sua opinião: 1

==============================
      RESULTADO DA PESQUISA
==============================
a) Quantidade de respostas 'EXCELENTE': 3
b) Quantidade de respostas 'RUIM': 3
>>>
>>> # Projeção para 50 entrevistados
... print("\nProjeção para 50 entrevistados:")
... print(f"EXCELENTE: {qtd_excelente * 50 // total_entrevistados}")
... print(f"RUIM: {qtd_ruim * 50 // total_entrevistados}")
... print(f"BOM: {(total_entrevistados - (qtd_excelente + qtd_ruim)) * 50 // total_entrevistados}")
...

Projeção para 50 entrevistados:
EXCELENTE: 15
RUIM: 15
BOM: 20
>>>
... qtd_ruim = 0
...
... total_entrevistados = 50
...
... # Repete os 10 entrevistados até chegar em 50
... for i in range(total_entrevistados):
...     nome = nomes[i % len(nomes)]
...     idade = idades[i % len(idades)]
...     opiniao = opinioes[i % len(opinioes)]
...
...     print(f"\n--- Entrevistado {i+1} de {total_entrevistados} ---")
...     print(f"Nome: {nome}")
...     print(f"Idade: {idade}")
...     print(f"Opinião: {opiniao}")
...
...     if opiniao == 1:
...         qtd_excelente += 1
...     elif opiniao == 2:
...         qtd_bom += 1
...     elif opiniao == 3:
...         qtd_ruim += 1
...
... # Exibição dos resultados finais
... print("\n" + "="*30)
... print("      RESULTADO DA PESQUISA      ")
... print("="*30)
... print(f"a) Quantidade de respostas 'EXCELENTE': {qtd_excelente}")
... print(f"b) Quantidade de respostas 'BOM': {qtd_bom}")
... print(f"c) Quantidade de respostas 'RUIM': {qtd_ruim}")
...

--- Entrevistado 1 de 50 ---
Nome: Bellatrix
Idade: 40
Opinião: 3

--- Entrevistado 2 de 50 ---
Nome: Corlys
Idade: 50
Opinião: 2

--- Entrevistado 3 de 50 ---
Nome: Tyrion
Idade: 24
Opinião: 1

--- Entrevistado 4 de 50 ---
Nome: Melisandre
Idade: 55
Opinião: 2

--- Entrevistado 5 de 50 ---
Nome: Andromeda
Idade: 36
Opinião: 1

--- Entrevistado 6 de 50 ---
Nome: Lucius
Idade: 39
Opinião: 3

--- Entrevistado 7 de 50 ---
Nome: Renly
Idade: 27
Opinião: 2

--- Entrevistado 8 de 50 ---
Nome: Cersei
Idade: 34
Opinião: 3

--- Entrevistado 9 de 50 ---
Nome: Jaime
Idade: 34
Opinião: 2

--- Entrevistado 10 de 50 ---
Nome: Druella
Idade: 70
Opinião: 1

--- Entrevistado 11 de 50 ---
Nome: Bellatrix
Idade: 40
Opinião: 3

--- Entrevistado 12 de 50 ---
Nome: Corlys
Idade: 50
Opinião: 2

--- Entrevistado 13 de 50 ---
Nome: Tyrion
Idade: 24
Opinião: 1

--- Entrevistado 14 de 50 ---
Nome: Melisandre
Idade: 55
Opinião: 2

--- Entrevistado 15 de 50 ---
Nome: Andromeda
Idade: 36
Opinião: 1

--- Entrevistado 16 de 50 ---
Nome: Lucius
Idade: 39
Opinião: 3

--- Entrevistado 17 de 50 ---
Nome: Renly
Idade: 27
Opinião: 2

--- Entrevistado 18 de 50 ---
Nome: Cersei
Idade: 34
Opinião: 3

--- Entrevistado 19 de 50 ---
Nome: Jaime
Idade: 34
Opinião: 2

--- Entrevistado 20 de 50 ---
Nome: Druella
Idade: 70
Opinião: 1

--- Entrevistado 21 de 50 ---
Nome: Bellatrix
Idade: 40
Opinião: 3

--- Entrevistado 22 de 50 ---
Nome: Corlys
Idade: 50
Opinião: 2

--- Entrevistado 23 de 50 ---
Nome: Tyrion
Idade: 24
Opinião: 1

--- Entrevistado 24 de 50 ---
Nome: Melisandre
Idade: 55
Opinião: 2

--- Entrevistado 25 de 50 ---
Nome: Andromeda
Idade: 36
Opinião: 1

--- Entrevistado 26 de 50 ---
Nome: Lucius
Idade: 39
Opinião: 3

--- Entrevistado 27 de 50 ---
Nome: Renly
Idade: 27
Opinião: 2

--- Entrevistado 28 de 50 ---
Nome: Cersei
Idade: 34
Opinião: 3

--- Entrevistado 29 de 50 ---
Nome: Jaime
Idade: 34
Opinião: 2

--- Entrevistado 30 de 50 ---
Nome: Druella
Idade: 70
Opinião: 1

--- Entrevistado 31 de 50 ---
Nome: Bellatrix
Idade: 40
Opinião: 3

--- Entrevistado 32 de 50 ---
Nome: Corlys
Idade: 50
Opinião: 2

--- Entrevistado 33 de 50 ---
Nome: Tyrion
Idade: 24
Opinião: 1

--- Entrevistado 34 de 50 ---
Nome: Melisandre
Idade: 55
Opinião: 2

--- Entrevistado 35 de 50 ---
Nome: Andromeda
Idade: 36
Opinião: 1

--- Entrevistado 36 de 50 ---
Nome: Lucius
Idade: 39
Opinião: 3

--- Entrevistado 37 de 50 ---
Nome: Renly
Idade: 27
Opinião: 2

--- Entrevistado 38 de 50 ---
Nome: Cersei
Idade: 34
Opinião: 3

--- Entrevistado 39 de 50 ---
Nome: Jaime
Idade: 34
Opinião: 2

--- Entrevistado 40 de 50 ---
Nome: Druella
Idade: 70
Opinião: 1

--- Entrevistado 41 de 50 ---
Nome: Bellatrix
Idade: 40
Opinião: 3

--- Entrevistado 42 de 50 ---
Nome: Corlys
Idade: 50
Opinião: 2

--- Entrevistado 43 de 50 ---
Nome: Tyrion
Idade: 24
Opinião: 1

--- Entrevistado 44 de 50 ---
Nome: Melisandre
Idade: 55
Opinião: 2

--- Entrevistado 45 de 50 ---
Nome: Andromeda
Idade: 36
Opinião: 1

--- Entrevistado 46 de 50 ---
Nome: Lucius
Idade: 39
Opinião: 3

--- Entrevistado 47 de 50 ---
Nome: Renly
Idade: 27
Opinião: 2

--- Entrevistado 48 de 50 ---
Nome: Cersei
Idade: 34
Opinião: 3

--- Entrevistado 49 de 50 ---
Nome: Jaime
Idade: 34
Opinião: 2

--- Entrevistado 50 de 50 ---
Nome: Druella
Idade: 70
Opinião: 1

==============================
      RESULTADO DA PESQUISA
==============================
a) Quantidade de respostas 'EXCELENTE': 15[simulador.py](https://github.com/user-attachments/files/32751754/simulador.py)

b) Quantidade de respostas 'BOM': 20
c) Quantidade de respostas 'RUIM': 15
>>>Python 3.14.7 (tags/v3.14.7:823f032, Aug  5 2026, 10:51:32) [MSC v.1944 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
... total_entrevistados = int(input("Digite a quantidade de entrevistados: "))
...
... # Laço para coletar as respostas de cada cliente
... for i in range(total_entrevistados):
...     print(f"\n--- Entrevistado {i+1} de {total_entrevistados} ---")
...
...     nome = input("Digite o nome: ")
...     idade = int(input("Digite a idade: "))
...
...     # Exibe as opções de opinião
...     print("Qual a sua opinião sobre o atendimento?")
...     print("1 - EXCELENTE")
...     print("2 - BOM")
...     print("3 - RUIM")
...
...     opiniao = int(input("Digite o número correspondente à sua opinião: "))
...
...     # Validação da resposta com estruturas de decisão
...     if opiniao == 1:
...         qtd_excelente += 1
...     elif opiniao == 3:
...         qtd_ruim += 1
...
... # Exibição dos resultados finais
... print("\n" + "="*30)
... print("      RESULTADO DA PESQUISA      ")
... print("="*30)
... print(f"a) Quantidade de respostas 'EXCELENTE': {qtd_excelente}")
... print(f"b) Quantidade de respostas 'RUIM': {qtd_ruim}")
...
Digite a quantidade de entrevistados: 10

--- Entrevistado 1 de 10 ---
Digite o nome: Bellatrix
Digite a idade: 40
Qual a sua opinião sobre o atendimento?
1 - EXCELENTE
2 - BOM
3 - RUIM
Digite o número correspondente à sua opinião: 3

--- Entrevistado 2 de 10 ---
Digite o nome: Corlys
Digite a idade: 50
Qual a sua opinião sobre o atendimento?
1 - EXCELENTE
2 - BOM
3 - RUIM
Digite o número correspondente à sua opinião: 2

--- Entrevistado 3 de 10 ---
Digite o nome: Tyrion
Digite a idade: 24
Qual a sua opinião sobre o atendimento?
1 - EXCELENTE
2 - BOM
3 - RUIM
Digite o número correspondente à sua opinião: 1

--- Entrevistado 4 de 10 ---
Digite o nome: Melisandre
Digite a idade: 55
Qual a sua opinião sobre o atendimento?
1 - EXCELENTE
2 - BOM
3 - RUIM
Digite o número correspondente à sua opinião: 2

--- Entrevistado 5 de 10 ---
Digite o nome: Andromeda
Digite a idade: 36
Qual a sua opinião sobre o atendimento?
1 - EXCELENTE
2 - BOM
3 - RUIM
Digite o número correspondente à sua opinião: 1

--- Entrevistado 6 de 10 ---
Digite o nome: Lucius
Digite a idade: 39
Qual a sua opinião sobre o atendimento?
1 - EXCELENTE
2 - BOM
3 - RUIM
Digite o número correspondente à sua opinião: 3

--- Entrevistado 7 de 10 ---
Digite o nome: Renly
Digite a idade: 27
Qual a sua opinião sobre o atendimento?
1 - EXCELENTE
2 - BOM
3 - RUIM
Digite o número correspondente à sua opinião: 2

--- Entrevistado 8 de 10 ---
Digite o nome: Cersei
Digite a idade: 34
Qual a sua opinião sobre o atendimento?
1 - EXCELENTE
2 - BOM
3 - RUIM
Digite o número correspondente à sua opinião: 3

--- Entrevistado 9 de 10 ---
Digite o nome: Jaime
Digite a idade: 34
Qual a sua opinião sobre o atendimento?
1 - EXCELENTE
2 - BOM
3 - RUIM
Digite o número correspondente à sua opinião: 2

--- Entrevistado 10 de 10 ---
Digite o nome: Druella
Digite a idade: 70
Qual a sua opinião sobre o atendimento?
1 - EXCELENTE
2 - BOM
3 - RUIM
Digite o número correspondente à sua opinião: 1

==============================
      RESULTADO DA PESQUISA
==============================
a) Quantidade de respostas 'EXCELENTE': 3
b) Quantidade de respostas 'RUIM': 3
>>>
>>> # Projeção para 50 entrevistados
... print("\nProjeção para 50 entrevistados:")
... print(f"EXCELENTE: {qtd_excelente * 50 // total_entrevistados}")
... print(f"RUIM: {qtd_ruim * 50 // total_entrevistados}")
... print(f"BOM: {(total_entrevistados - (qtd_excelente + qtd_ruim)) * 50 // total_entrevistados}")
...

Projeção para 50 entrevistados:
EXCELENTE: 15
RUIM: 15
BOM: 20
>>>
... qtd_ruim = 0
...
... total_entrevistados = 50
...
... # Repete os 10 entrevistados até chegar em 50
... for i in range(total_entrevistados):
...     nome = nomes[i % len(nomes)]
...     idade = idades[i % len(idades)]
...     opiniao = opinioes[i % len(opinioes)]
...
...     print(f"\n--- Entrevistado {i+1} de {total_entrevistados} ---")
...     print(f"Nome: {nome}")
...     print(f"Idade: {idade}")
...     print(f"Opinião: {opiniao}")
...
...     if opiniao == 1:
...         qtd_excelente += 1
...     elif opiniao == 2:
...         qtd_bom += 1
...     elif opiniao == 3:
...         qtd_ruim += 1
...
... # Exibição dos resultados finais
... print("\n" + "="*30)
... print("      RESULTADO DA PESQUISA      ")
... print("="*30)
... print(f"a) Quantidade de respostas 'EXCELENTE': {qtd_excelente}")
... print(f"b) Quantidade de respostas 'BOM': {qtd_bom}")
... print(f"c) Quantidade de respostas 'RUIM': {qtd_ruim}")
...

--- Entrevistado 1 de 50 ---
Nome: Bellatrix
Idade: 40
Opinião: 3

--- Entrevistado 2 de 50 ---
Nome: Corlys
Idade: 50
Opinião: 2

--- Entrevistado 3 de 50 ---
Nome: Tyrion
Idade: 24
Opinião: 1

--- Entrevistado 4 de 50 ---
Nome: Melisandre
Idade: 55
Opinião: 2

--- Entrevistado 5 de 50 ---
Nome: Andromeda
Idade: 36
Opinião: 1

--- Entrevistado 6 de 50 ---
Nome: Lucius
Idade: 39
Opinião: 3

--- Entrevistado 7 de 50 ---
Nome: Renly
Idade: 27
Opinião: 2

--- Entrevistado 8 de 50 ---
Nome: Cersei
Idade: 34
Opinião: 3

--- Entrevistado 9 de 50 ---
Nome: Jaime
Idade: 34
Opinião: 2

--- Entrevistado 10 de 50 ---
Nome: Druella
Idade: 70
Opinião: 1

--- Entrevistado 11 de 50 ---
Nome: Bellatrix
Idade: 40
Opinião: 3

--- Entrevistado 12 de 50 ---
Nome: Corlys
Idade: 50
Opinião: 2

--- Entrevistado 13 de 50 ---
Nome: Tyrion
Idade: 24
Opinião: 1

--- Entrevistado 14 de 50 ---
Nome: Melisandre
Idade: 55
Opinião: 2

--- Entrevistado 15 de 50 ---
Nome: Andromeda
Idade: 36
Opinião: 1

--- Entrevistado 16 de 50 ---
Nome: Lucius
Idade: 39
Opinião: 3

--- Entrevistado 17 de 50 ---
Nome: Renly
Idade: 27
Opinião: 2

--- Entrevistado 18 de 50 ---
Nome: Cersei
Idade: 34
Opinião: 3

--- Entrevistado 19 de 50 ---
Nome: Jaime
Idade: 34
Opinião: 2

--- Entrevistado 20 de 50 ---
Nome: Druella
Idade: 70
Opinião: 1

--- Entrevistado 21 de 50 ---
Nome: Bellatrix
Idade: 40
Opinião: 3

--- Entrevistado 22 de 50 ---
Nome: Corlys
Idade: 50
Opinião: 2

--- Entrevistado 23 de 50 ---
Nome: Tyrion
Idade: 24
Opinião: 1

--- Entrevistado 24 de 50 ---
Nome: Melisandre
Idade: 55
Opinião: 2

--- Entrevistado 25 de 50 ---
Nome: Andromeda
Idade: 36
Opinião: 1

--- Entrevistado 26 de 50 ---
Nome: Lucius
Idade: 39
Opinião: 3

--- Entrevistado 27 de 50 ---
Nome: Renly
Idade: 27
Opinião: 2

--- Entrevistado 28 de 50 ---
Nome: Cersei
Idade: 34
Opinião: 3

--- Entrevistado 29 de 50 ---
Nome: Jaime
Idade: 34
Opinião: 2

--- Entrevistado 30 de 50 ---
Nome: Druella
Idade: 70
Opinião: 1

--- Entrevistado 31 de 50 ---
Nome: Bellatrix
Idade: 40
Opinião: 3

--- Entrevistado 32 de 50 ---
Nome: Corlys
Idade: 50
Opinião: 2

--- Entrevistado 33 de 50 ---
Nome: Tyrion
Idade: 24
Opinião: 1

--- Entrevistado 34 de 50 ---
Nome: Melisandre
Idade: 55
Opinião: 2

--- Entrevistado 35 de 50 ---
Nome: Andromeda
Idade: 36
Opinião: 1

--- Entrevistado 36 de 50 ---
Nome: Lucius
Idade: 39
Opinião: 3

--- Entrevistado 37 de 50 ---
Nome: Renly
Idade: 27
Opinião: 2

--- Entrevistado 38 de 50 ---
Nome: Cersei
Idade: 34
Opinião: 3

--- Entrevistado 39 de 50 ---
Nome: Jaime
Idade: 34
Opinião: 2

--- Entrevistado 40 de 50 ---
Nome: Druella
Idade: 70
Opinião: 1

--- Entrevistado 41 de 50 ---
Nome: Bellatrix
Idade: 40
Opinião: 3

--- Entrevistado 42 de 50 ---
Nome: Corlys
Idade: 50
Opinião: 2

--- Entrevistado 43 de 50 ---
Nome: Tyrion
Idade: 24
Opinião: 1

--- Entrevistado 44 de 50 ---
Nome: Melisandre
Idade: 55
Opinião: 2

--- Entrevistado 45 de 50 ---
Nome: Andromeda
Idade: 36
Opinião: 1

--- Entrevistado 46 de 50 ---
Nome: Lucius
Idade: 39
Opinião: 3

--- Entrevistado 47 de 50 ---
Nome: Renly
Idade: 27
Opinião: 2

--- Entrevistado 48 de 50 ---
Nome: Cersei
Idade: 34
Opinião: 3

--- Entrevistado 49 de 50 ---
Nome: Jaime
Idade: 34
Opinião: 2

--- Entrevistado 50 de 50 ---
Nome: Druella
Idade: 70
Opinião: 1

==============================
      RESULTADO DA PESQUISA
==============================
a) Quantidade de respostas 'EXCELENTE': 15
b) Quantidade de respostas 'BOM': 20
c) Quantidade de respostas 'RUIM': 15
>>>
>>>[simulador.py](https://github.com/user-attachments/files/32751762/simulador.py)

