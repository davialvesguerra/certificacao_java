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

