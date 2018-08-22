/*  0     1
    1     1 1
    2     1 2 1
    3     1 3 3 1
    4     1 4 6 4 1          
          0 1 2 3 4
https://pt.slideshare.net/gustavogfs94/introduo-ao-paradigma-funcional-com-scala
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


var lista = 1 :: 2 :: 3 :: 4 :: 5 :: Nil

def somaLista(l: List[Int], soma: Int = 0): Int = l match { 
  case Nil => soma 
  case head::tail => somaLista(tail, head + soma) 
}

println("somatorio da lista: [1,2,3,4,5] = " + somaLista (lista));
