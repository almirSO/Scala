# Scala
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

def pascal(col: Int, lin: Int): Int = {
  if(col == 0 || col == lin){
    return 1;
  }else if(col > lin){
    return 0;
  }else{
    return pascal(col, lin-1) + pascal (col-1, lin-1);
  }
}

println( pascal (0,0) + " teste 1");
println( pascal (0,1) + " teste 2"); 
println( pascal (1,1) + " teste 3");
println( pascal (9,0) + " teste 4");
println( pascal (5,7) + " teste 5");
println( pascal (1,2) + " teste 6");
println( pascal (2,2) + " teste 7");

//teste
println( pascal (0,0));
print( pascal (0,1)); println( pascal (1,1));
println( pascal (9,0));
println( pascal (5,7));


// 
def fat(n: Int): Int = n match {
    case 0 => 1
    case _ => n * fat(n-1)
}



def fib(num: Int): Int = num match{
  case 0 => 0
  case 1 => 1
  case _ => fib(num-1) + fib(num-2)
}

//teste
println( fib(0));
println( fib (1)); 
println( fib (2));
println( fib (7));
