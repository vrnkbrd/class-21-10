# class-21-10
### Task 7kyu
Create function fib that returns n'th element of Fibonacci sequence (classic programming task).
#### My solution: 
`Java 
public class Fibonacci {
	public static long fib (int n){
   if (n <= 1)
            return n;
        return fib(n - 1) + fib(n - 2);
		
	}
}
`
#### Fav solution: 
`Java 
public class Fibonacci {
  
  public static long fib (int n) {
    if (n < 3) return 1;
    
    long first = 1;
    long second = 1;
    for (int i = 3; i <= n; i++) {
      second += first;
      first = second - first;
    }
    return second;
  }
}
`
It is the classic one. Had the same vision but got how to made it with recurtion

### Task 2 7kyu
Count the number of divisors of a positive integer n.
#### My solution
`Java 
public class FindDivisor {

  public long numberOfDivisors(int n) {
     long counter =0;
      for(int i=1; i<=n; i++){
          if(n % i == 0){
          counter++;
          }
      }
      return counter;
  }
}

`

#### Fav solution:

`Java 
import java.util.*;

public class FindDivisor {
  public long numberOfDivisors(int n) {
  ArrayList<Integer> list = new ArrayList<Integer>();
  for (int i = 1; i <= n; i++) { if (n % i == 0) list.add(i); }
  return list.size();
  }
}
`
List structure was used
