Abaixo vão ter algumas questões que podem cair na prova. Elas foram retiradas
de alguns cursos da alura.

https://unibb.alura.com.br/course/certificacao-java-lambdas-api-de-datas/task/8670


## Trabalhando com a saída do console

O que acontece ao tentar compilar e executar o código a seguir?


### Q1
```java 
class Test{
    public static void main(String[] args){
    System.out.print("a");
    System.out.println('b'); // A
    System.out.print();      // B
    System.out.println("c"); 
    }
}
```

a) Não compila por erro na linha B

b) Compila e imprime

c) Não compila por erro na linha A

Resposta:

O método print não possui versão sem argumentos. A resposta é Não compila por erro na linha B

### Q2
Ao tentar compilar e executar o código a seguir, o que acontece?

```java 
public class Test {
    public static void main(String[] args) {
        System.out.print("a");
        System.out.println("b");
        System.out.printf("c");
        System.out.print("d");
        System.out.println("\n");
        System.out.print("e");
    }
}
```

a) Compila e imprime
```
ab
cd
e
```
b) Não compila
c)Compila e imprime
```
ab
c
d
e
```
d)Compila e imprime
```
ab
cd

e
```

Resposta:

```
ab
cd

e
```

### Q3
```java 

public class Test {
    public static void main(String[] args) {
        System.out.printf("%s",12); //A
        System.out.printf("%d",new Integer(321)); //B
        System.out.printf("%d",(short)(byte)(double) 127); //C
    }
}
```

a)Compila e executa normalmente

b)Erro de compilação na linha B

c)Erro de compilação na linha C

d)Erro de compilação na linha A

e)Erro de compilação nas linhas B e C

### Q4

Ao tentar compilar e executar o seguinte código, o que é impresso?

```java 

public class Testes {
    public static void main(String[] args) {
        System.out.println(new char[]{'a','b','c'}); // A
        System.out.println(new byte[]{'a','b','c'}); // B
        System.out.println("abc"); // C
        System.out.println(new String[]{"abc"}); // D
    }
}
```
a)Todas as linhas imprimem abc

b)Linhas A e C imprimem abc

c)Linhas A, C e D imprimem abc

d)Linha C imprime abc

e)Não compila na linha B

## Desenvolver código que usa classe wrapper

### Q1

```java 
public class Test {
    static long i;

    public static void main(String[] args) {
        i = Integer.valueOf("10",8); // A
        m1(i); // B
    }

    private static void m1(Integer j) { // C
        System.out.println(j);
    }
}
```


a) Erro de compilação na linha B

b) Erro de compilação na linha C

c) Erro de compilação na linhaA

d) Compila mas lança exception

e) Imprime 10

Resposta: 

Erro de compilação na linha B.

### Q2

```java 

public class Test {
    public static void main(String[] args) {
        int a = Short.parseShort("126"); // A
        short s = Integer.parseInt("23").shortValue(); //B
        double h = Double.valueOf("27").floatValue();  //C
        System.out.println(a + s);
    }
}
```
a) Erro de compilação na linha C
b) Imprime 149
c) Erro de compilação na linha A
d) Imprime 176
e) Erro de compilação na linha B


Resposta:

A resposta certa é erro de compilação na linha B pois o método parseInt(..) devolve o tipo primitivo int. Não podemos executar o método shortValue() (ou qualquer outro método) usando um primitivo.


### Q3 

```java 
public class Test {

    public static void main(String[] args) {
        int a = Integer.parseInt("10",2);
        int b = a == 10 ? null : 3;
        System.out.println(a + b);
    }
}
```

a) Imprime 5

b) Ao executar lança NullPointerException

c) Erro de compilação.

d) Imprime 176

e) Erro de compilação na linha B


Resposta: 

A resposta certa é que imprime 5.

## Diferenciar entre variáveis de referência a objetos e tipos primitivos

### Q1 

```java 
class A {
    public static void main(String[] args) {
        int x = 15;
        int y = x;
        y++;
        x++;
        int z = y;
        z--;
        System.out.println(x + y + z);
    }
}
```

a) Imprime 46
b) Imprime 47
c) Imprime 43
d) Imprime 45
e) Imprime 44

*Resposta*

letra b)

### Q2)

```java 

class B {
    int v = 15;
}
class A {
    public static void main(String[] args) {
        B x = new B();
        B y = x;
        y.v++;
        x.v++;
        B z = y;
        z.v--;
        System.out.println(x.v + y.v + z.v);
    }
}
```



a) Imprime 47

b) Imprime 48

c) Imprime 43

d) Imprime 46

e) Imprime 44

*Resposta*

letra b)

## Manipulando Strings

### Q1

```java 

class A{
    public static void main(String [] args){
        String s = "aba";
        for(int i = 0; i < 9; i++) {
            s = s +"aba";
        }
        System.out.println(s.length);
    }
}
```
a) Não compila

b) Compila e imprime 36

c) Compila e imprime 30

d) Compila e imprime 3

e) Compila e imprime 33

*Resposta*

Não compila, pois length() é um método de String, diferente dos arrays em que length é um atributo.

### Q2

```java 
class B {
    String msg;

    void imprime() {
        if (!msg.isEmpty())
            System.out.println(msg);
        else
            System.out.println("vazio");
    }
}
```

a) Compila, mas dá exceção na hora de rodar

b) Compila, roda e não imprime nada

c) Não compila

d) Compila, roda e imprime "vazio"

### Q3

```java 

class B {

    void imprime() {
        String msg;
        if (!msg.isEmpty())
            System.out.println(msg);
        else
            System.out.println("vazio");
    }
}
```

a) Compila, mas dá exceção na hora de rodar

b) Não compila

c) Compila, roda e não imprime nada

d) Compila, roda e imprime "vazio"


*Resposta*

Não compila, pois a variável não foi inicializada

### Q5

```java 
class A {
    String vazio;
    public static void main(String[] args) {
        String full = "Bem-vindo " + vazio;
        System.out.println(full);
    }
}
```

a) Compila e imprime "Bem-vindo ".

b) Compila e imprime outro resultado que não foi mencionado nessas alternativas.

c) Não compila por outro motivo.

d) Compila e imprime "Bem-vindo vazio".

e) Não compila pois vazio é nulo.

*Resposta*

Não compila por outro motivo: a variável `vazio` não é estática.


## Crie métodos com argumentos e valores de retorno

### Q1

```java

class A {
    public static void main(String[] args) {
        x(args.length);
    }
    static int x(int l) {
        for(int i=0;i<100;i++) {
            switch(i) {
                case l:
                    System.out.println(l);
                    if(l==i) return;
                case 0:
                    System.out.println(0);
            }
        }
        System.out.println("Fim");
        return -1;
    }
}
```

a) Não compila

b) Compila e ao rodar com cinco parâmetros, imprime 0, 5, 0, -1 e Fim.

c) Compila e ao rodar com cinco parâmetros, imprime 0, 5, 0 e Fim.

d) Compila e ao rodar com cinco parâmetros, imprime 0, 5 e Fim.

e) Compila e ao rodar com cinco parâmetros, imprime 0 e 5.

*Resposta*

O código não compila pois existe um `return` sem valor e está sendo utilizado um valor não constante no `case` do `switch`.

### Q2 

```java 
class A {
    public static void main(String[] args) {
        System.out.println(a(args.length));
    }
    static int a(int l) {
        if(l<10) return b(l); //A
        else return c(); // B
    }
    static int b(int l) {
        if(l<10) return b(l); // C
        else return c(); // D
    }
    static long c() {
        return 3;
    }
}
```

a) Não compila: erro nas linhas B e D

b) Compila e, ao chamar com 15 argumentos, entra em loop infinito.

c) Não compila: erro nas linha A e C

d) Compila e, ao chamar com 15 argumentos, imprime 3.

e) Não compila por um motivo não listado