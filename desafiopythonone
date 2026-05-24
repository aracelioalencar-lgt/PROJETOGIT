saldo =0
deposito =0
extrato = ""
quant_saques=0
LIMITE_SAQUE=3

barra = "Menu"
barra_extrato ="Extrato"

registro_saques=[]
registro_deposito=[]


menu = '''
            Depositar[d]
            Sacar    [s]
            Extrato  [e]
            Sair     [q]
       '''
while True:

	print(barra.center(30,"-"))
	print(menu)
	print(barra.center(30,"-"))

	opcao = input("Entre com a opção: ")

    #DEPOSITO
	if opcao =='d':	

		valor = int(input("Insira o valor do deposito: "))

		if valor >0:
			saldo += valor
			registro_deposito.append(valor)
			print(f"Depósito de R${valor:.2f} realizado!")
		else:
			print("Valores negativos não permitos")

	#SAQUE
	elif opcao == 's':
		valor = int(input("Insira o valor do saque: "))
		if valor > 500:
			print("O valor excede o limete de R$500!")
			
		elif quant_saques >=LIMITE_SAQUE:
			print("Limite de saques diarios excedido!")
			
		elif valor > saldo:
			print("Saldo insuficiente!")
		
		elif valor <= 0:
				print("Valor invalido!")
				
		else:
			saldo -= valor
			registro_saques.append(valor)
			quant_saques +=1

			print(f"Saque de R${valor:.2f} realizado!")
	
	#EXTRATO
	elif opcao == 'e':
		print(barra_extrato.center(30, "-"))
		
		print("\nDepósitos:")
		for i, valor in enumerate(registro_deposito, start=1):
			print(f"{i}. R${valor:.2f}")
		
		print("\nSaques:")
        
		for i, valor in enumerate(registro_saques, start=1):
			print(f"{i}. R${valor:.2f}")
		
		print(f"\nSaldo atual: R${saldo:.2f}")
		
		print(barra_extrato.center(30, "-"))


	#SAIR
	elif opcao == 'q':
		print("Sistema encerrado.")
		break
		
	else:
		print("Opção invalida, por favor selecione novamente a operaçaõ desejada. ")
