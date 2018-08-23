println(" ");
println("---------------------INICIO DA LISTA DE EXERCICIO------------------------");
println(" ");

/*  0     1
    1     1 1
    2     1 2 1
    3     1 3 3 1
    4     1 4 6 4 1          
          0 1 2 3 4
https://pt.slideshare.net/gustavogfs94/introduo-ao-paradigma-funcional-com-scala
http://www.dclick.com.br/2010/12/01/utilizando-listas-em-scala/
https://drive.google.com/drive/folders/0B5wF9O40_yU6MzNpRFBNRGRSSGc
*/

def pascal(col: Int, lin: Int): Int = (col,lin) match{
  case (0,lin) => 1
  case (col,lin) if col==lin => 1
  case (col,lin) if col > lin => 0
  case _ => (pascal(col, lin-1) + pascal (col-1, lin-1))
}

println( pascal (0,0) + " pascal de 0,0");
println( pascal (0,1) + " pascal de 0,1"); 
println( pascal (1,1) + " pascal de 1,1");
println( pascal (9,0) + " pascal de 9,0");
println( pascal (5,7) + " pascal de 5,7");
println( pascal (1,2) + " pascal de 1,2");
println( pascal (2,2) + " pascal de 2,2");

def fat(n: Int): Int = n match {
    case 0 => 1
    case _ => n * fat(n-1)
}

def fib(num: Int): Int = num match{
  case 0 => 1
  case 1 => 1
  case _ => fib(num-1) + fib(num-2)
}

println("fib de 0: " + fib(0) + "| fat de 0: " + fat(0));
println("fib de 1: " + fib(1) + "| fat de 1: " + fat(1)); 
println("fib de 2: " + fib(2) + "| fat de 2: " + fat(2));
println("fib de 3: " + fib(3) + "| fat de 3: " + fat(3));
println("fib de 4: " + fib(4) + "| fat de 4: " + fat(4)); 
println("fib de 5: " + fib(5) + "| fat de 5: " + fat(5));
println("fib de 10: " + fib(10) + "| fat de 10: " + fat(10));

// LISTAS ................................................................................................

println(" ");
println(".....................Usando lista........................");
println(" ");

var lista = 20 :: 1 :: 2 :: 3 :: 4 :: 5 :: Nil

def somaLista(l: List[Int]): Int = l match { 
  case Nil => 0
  case head::tail => head + somaLista(tail) 
}

def subtracaoLista(l: List[Int]): Int = l match { 
  case Nil => 0
  case head::tail => head - somaLista(tail) 
}

def multiplicacaoLista(l: List[Int]): Int = l match { 
  case Nil => 1
  case head::tail => head * somaLista(tail) 
}

println("somatorio da lista: [20,1,2,3,4,5] = " + somaLista (lista));
println("subtração da lista: [20,1,2,3,4,5] = " + subtracaoLista (lista));
println("multiplicação da lista: [20,1,2,3,4,5] = " + multiplicacaoLista (lista));

println(" ");
println("-----------------------FIM DA LISTA DE EXERCICIO----------------------------");
println(" ");

// feito em aula........................................................

println(" ");
println("...................FEIRO EM AULA.......................");
println(" ");

def contaKdeNumero (numero:Int, k:Int):Int = {
  if (numero<10){
    if(numero==k) 1
    else 0
  } 
  else {
    if(numero%10==k) contaKdeNumero(numero/10,k) + 1
    else contaKdeNumero(numero/10,k)
  }
}

println("OCORRENCIAS DE 0 EM 1223339 " + contaKdeNumero(1223339,0))
println("OCORRENCIAS DE 1 EM 1223339 " + contaKdeNumero(1223339,1))
println("OCORRENCIAS DE 2 EM 1223339 " + contaKdeNumero(1223339,2))
println("OCORRENCIAS DE 3 EM 1223339 " + contaKdeNumero(1223339,3))
println("OCORRENCIAS DE 4 EM 1223339 " + contaKdeNumero(1223339,4))
println("OCORRENCIAS DE 5 EM 1223339 " + contaKdeNumero(1223339,5))
println("OCORRENCIAS DE 6 EM 1223339 " + contaKdeNumero(1223339,6))
println("OCORRENCIAS DE 9 EM 1223339 " + contaKdeNumero(1223339,9))



def converteDecBin (numero:Int):String = numero match{
  case (numero) if numero<2 => ""+numero
  case _ => converteDecBin(numero/2) + numero%2
}

println("0 em binario eh: " + converteDecBin(0));
println("1 em binario eh: " + converteDecBin(1));
println("10 em binario eh: " + converteDecBin(10));
println("100 em binario eh: " + converteDecBin(100));
println("2 em binario eh: " + converteDecBin(2));
println("350 em binario eh: " + converteDecBin(350));
println("9 em binario eh: " + converteDecBin(9));
println("12 em binario eh: " + converteDecBin(12));
println("19 em binario eh: " + converteDecBin(19));
println("33 em binario eh: " + converteDecBin(33));
println("99 em binario eh: " + converteDecBin(99));
println("1000 em binario eh: " + converteDecBin(1000));
