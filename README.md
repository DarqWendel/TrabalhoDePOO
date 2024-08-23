# TrabalhoDePOO

**01) Faça um programa que recebe um número do teclado e calcula o dobro utilizando um método**
```
package trabalhoPOO;
import java.util.Scanner;
public class questãoUm {

	public static void main(String[] args) {
	Scanner entrada = new Scanner(System.in);

	int numero;
	
	System.out.println("Digite um número: ");
	numero = entrada.nextInt();
	calcularDobro(numero);
	}
	
	
	public static void calcularDobro(int numero){
		System.out.println("O Dobro de " + numero + " é: " + numero *2);
	}
}
```
**02)	Faça um programa que recebe o comprimento, largura e profundidade de uma piscina. Deve-se calcular o perímetro, área e volume, de acordo com o menu abaixo:
MENU
1-	Digite 1 para calcular o PERÍMETRO
2-	Digite 2 para calcular a ÁREA
3-	Digite 3 para calcular o VOLUME
OBS: Você deve criar procedimentos para cada cálculo acima.**
```
package trabalhoPOO;
import java.util.Scanner;
public class questãoDOIS {

	public static void main(String[] args) {
		Scanner entrada = new Scanner(System.in);
		int comprimento, largura, profundidade;
		int menu;
		System.out.println("Digite o comprimento da piscina: ");
		comprimento = entrada.nextInt();
		System.out.println("Digite a largura da piscina: ");
		largura = entrada.nextInt();
		System.out.println("Digite a profundidade da piscina: ");
		profundidade = entrada.nextInt();
		
		System.out.println("Menu: \nDigite 1 para calcular o PERÍMETRO\r\n"
				+ "Digite 2 para calcular a ÁREA\r\n"
				+ "Digite 3 para calcular o VOLUME");
		menu = entrada.nextInt();
		
		calculos(menu, comprimento, largura, profundidade);
	}

	public static void calculos(int menu, int comprimento, int largura, int profundidade){
	switch (menu) {
	case 1: System.out.println(2*comprimento+largura); break;
	case 2: System.out.println(comprimento*largura);   break;
	case 3: System.out.println(comprimento*largura*profundidade); break;
	}
	} }
```
**03) Faça um programa que recebe a idade de um atleta na MAIN. Crie um método do tipo
boolean que verifica se ele é “ de MAIOR idade” ou “ de MENOR idade”.
OBS: A impressão é na MAIN**
```
package trabalhoPOO;
import java.util.Scanner;
public class questãoTrês {

	public static void main(String[] args) {
		Scanner entrada = new Scanner(System.in);
		int idade;
		
		
		System.out.println("Digite uma idade: ");
		idade = entrada.nextInt();
		
		boolean resultado = verificarIdade(idade);
		if(resultado == true){
			System.out.println("Você é maior de idade");
		}else {
			System.out.println("Você é menor de idade");
		}
	}
	
	public static boolean verificarIdade(int idade) {
		if(idade >= 18) {
			return true;
		} else {
			return false;
		}
	}
	
}
```
**PARTE TEÓRICA - INFORMAÇÕES ESSENCIAIS PARA APRENDER POO**

Responda o que se pede abaixo:

Exercício:

**Construtores:**
   
.1	O que é um construtor em Java?
```
Em Java, um construtor é um método especial usado para inicializar objetos quando eles são criados. Ele tem o mesmo nome da classe e não retorna nenhum valor (nem mesmo void). O construtor é chamado automaticamente quando um novo objeto da classe é instanciado.

Aqui estão alguns pontos importantes sobre construtores:
01 - Nome: O construtor deve ter o mesmo nome que a classe.
02 - Sem valor de retorno: Um construtor não pode ter um tipo de retorno, nem mesmo void.
03 - Sobrecarregamento: Uma classe pode ter múltiplos construtores com diferentes parâmetros. Isso é chamado de sobrecarga de construtores.
04 - Construtor padrão: Se você não definir nenhum construtor em sua classe, o Java fornecerá um construtor padrão sem parâmetros automaticamente. No entanto, se você definir algum construtor (com ou sem parâmetros), o construtor padrão não será mais fornecido automaticamente.
```


●	Qual é o objetivo de um construtor?
```
O objetivo dos construtores é inicializar um objeto quando ele é criado, configurando seus valores iniciais e preparando-o para uso.
```


**Métodos Get e Set:**

●	O que são métodos Get e Set em Java?
```
Get: Método que retorna o valor de um atributo.
Set: Método que define o valor de um atributo.
```

●	Qual é o propósito de um método Get?
```
O propósito de um método Get é retornar o valor de um atributo de um objeto.
```

●	Qual é o propósito de um método Set?
```
O propósito de um método Set é atribuir um valor a um atributo privado de uma classe.
```

**Modificadores de Acesso:**
●	Liste e explique brevemente os modificadores de acesso em Java.
```
Aqui estão os modificadores de acesso em Java:

.public: O membro é acessível de qualquer lugar no código.
.protected: O membro é acessível dentro da mesma classe, subclasses e pacotes.
.default (nenhum modificador): O membro é acessível apenas dentro do mesmo pacote.
.private: O membro é acessível somente dentro da própria classe.
```
●	Qual é a diferença entre public, private e protected?  	Impressão do Objeto:
```
Aqui está a diferença entre public, private e protected:

.public: Acesso irrestrito. Qualquer classe pode acessar o membro.
.private: Acesso restrito. Somente a própria classe pode acessar o membro.
.protected: Acesso limitado. O membro pode ser acessado pela própria classe, subclasses e classes no mesmo pacote.
```
●	Por que é importante ter um método toString() em uma classe?
```
É importante ter um método `toString()` em uma classe porque ele fornece uma representação legível e informativa do objeto quando convertido para uma string, facilitando a visualização e depuração do objeto.
```
●	Como você pode imprimir as informações de um objeto em Java?
```
Você pode imprimir as informações de um objeto em Java chamando o método `toString()` do objeto, geralmente usando `System.out.println(objeto);`. Se você definir o método `toString()` na sua classe, ele será chamado automaticamente para obter a representação em string do objeto.
```

