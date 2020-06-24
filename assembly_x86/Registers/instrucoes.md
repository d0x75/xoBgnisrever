## Instruções Assembly

_Machine instructions generally fall into three categories: data movement, arithmetic/logic, and control-flow. In this section, we will look at important examples of x86 instructions from each category_.

- Uma instrução assemblym completa, terá o Mnemônico da instrução a ser executada, depois o Operador onde ficará o resultado da operação(Operador de destino) e por último podemos ter um Operador origem, que irá fazer parte da operação a ser executada. Exemplo:

		-----------------------------------------
		|Mnemônico | Op.destino |Op. Origem 	|
		|----------------------------------------
		|MOV			ECX,		0x42	    |	 	
		|LEA			EDX,		[EBP-28]    |
		|SUB			ESP,		0x0		    |
		|PUSH			EBP 		            | 
		|XOR			EAX,		EAX         |
		|JMP			0x41414141		        |
		-----------------------------------------



#### Operandos

- Os principais operandos que podemos utilizar são :

		IMEDIATOS : 0x42, 0x00401828, 0x0C
		REGISTRADORES : EAX, ECX, EBP
		ENDEREÇOS DE MEMÓRIA : [0x0012F8D4], [ECX], [EBP + 0x08]

- Quando passamos valores de operandos entre colchetes, como [0xff273] estamos referindo a endereços de memórias.

#### Opcodes 

- Pelo fato do processador só entender os Opcodes ( hexadecimais ), cada instrução em assembly que usamos tem seu respectivo opcode, ou melhor, é o código que o processador sabe que é referente a instrução a ser executada. Exemplo:

		Instrução| MOV EAX, 0x42
		Opcodes | B9 42 00 00 00


- Em suma, Opcodes, são os códigos que o processador consegue ler e entender.
- Mnemônicos, é a tradução legível para humanos dos opcodes que o processador lê.