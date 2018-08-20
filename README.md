# Scala
/*  0     1
    1     1 1
    2     1 2 1
    3     1 3 3 1
    4     1 4 6 4 1          
          0 1 2 3 4*/



def pascal(col: Int, lin: Int): Int = {
  if(col == 0 || col == lin){
    return 1;
  }else if(col > lin){
    return 0;
  }else{
    return pascal(col-1, lin-1) + pascal (col, lin-1);
  }
}

//teste
println( pascal (0,0));
print( pascal (0,1)); println( pascal (1,1));
println( pascal (9,0));
println( pascal (5,7));
