# DSA-Practice

##Find even digits leetcode

public int findNumbers(int[] nums) {
        int count =0;
        for(int num :nums){
            if(even(num)){
                count++;
            }
        }
        return count;
    }
    
    boolean even(int num){
        int numberofdigits= digits(num);
        return numberofdigits % 2 == 0;
    }
    int digits(int num){
        if(num < 0){
            num = num *-1;
        }
        if(num ==0){
            return 1;
        }
        int count =0;
        while(num>0){
            count++;
            num = num / 10;
        }
        return count;
    }
}
//744 leetcode


 public char nextGreatestLetter(char[] letters, char target) {
        int start = 0;
        int end = letters.length-1;
        
        while(start<=end){
            int mid = start + (end-start)/2;
            if(target < letters[mid]){
                end = mid -1;
            } else{
                start = mid + 1;
            }           
            
        }
        return letters[start % letters.length];
    }
}

//268 leetcode 


public int missingNumber(int[] nums) {
        int i = 0;
        while(i < nums.length){
            int correct = nums[i];
            if(nums[i] < nums.length && nums[i] != nums[correct]){
                swap(nums,i,correct);
            }else{
                i++;
            }
        }
        for(int index = 0; index < nums.length; index++){
            if(nums[index] != index){
                return index;
            }
        }
        return nums.length;
    }
    
     void swap(int[]nums,int first,int second){
        int temp = nums[first];
        nums[first] = nums[second];
        nums[second] = temp;
    }
}

import java.io.*;
import java.util.*;

public class Main {

  public static void permutations(int[] boxes, int ci, int ti){
    // write your code here
    if(ci >ti ){
        for(int i=0; i<boxes.length;i++){
            System.out.print(boxes[i]);
            
        }
        System.out.println();
        return;
    }
    for(int i =0; i<boxes.length;i++){
        if(boxes[i]==0){
            boxes[i] = ci;
            permutations(boxes,ci+1,ti);
            boxes[i] =0;
        }
    }
  }

  public static void main(String[] args) throws Exception {
    BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
    int nboxes = Integer.parseInt(br.readLine());
    int ritems = Integer.parseInt(br.readLine());
    permutations(new int[nboxes], 1, ritems);
  }

}

import java.io.*;
import java.util.*;

public class Main {

  public static void combinations(int cb, int tb, int ssf, int ts, String asf)
  {
    // write your code here
    if(cb>tb){
        if(ssf==ts){
            System.out.println(asf);
            
        }
        return;
        
    }
    
            combinations(cb+1,tb,ssf+1,ts,asf+ "i");
            
            
        
                    combinations(cb+1,tb,ssf,ts,asf + "-");

        

}
  

  public static void main(String[] args) throws Exception {
    BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
    int nboxes = Integer.parseInt(br.readLine());
    int ritems = Integer.parseInt(br.readLine());
    combinations(1, nboxes, 0, ritems, "");
  }

}

package xyz;

public class XYZ {
	static int sum =0;
	static void reverse(int n) {
		if(n==0) {
			return;
		}
		int rem = n % 10;
		sum = sum * 10 + rem;
		reverse(n/10);
		
			
	}

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		reverse(1234);
		System.out.println(sum);

	}

}
package xyz;

public class XYZ {
	static int sum =0;
	static void reverse(int n) {
		if(n==0) {
			return;
		}
		int rem = n % 10;
		sum = sum * 10 + rem;
		reverse(n/10);
		
			
	}

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		reverse(1234);
		System.out.println(sum);

	}

}
package xyz;

public class XYZ {
	static int sum =0;
	static void reverse(int n) {
		if(n==0) {
			return;
		}
		int rem = n % 10;
		sum = sum * 10 + rem;
		reverse(n/10);
		
			
	}

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		reverse(1234);
		System.out.println(sum);

	}

}
package xyz;

public class XYZ {
	static int sum =0;
	static void reverse(int n) {
		if(n==0) {
			return;
		}
		int rem = n % 10;
		sum = sum * 10 + rem;
		reverse(n/10);
		
			
	}

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		reverse(1234);
		System.out.println(sum);

	}

}
package xyz;

public class XYZ {
	static int sum =0;
	static void reverse(int n) {
		if(n==0) {
			return;
		}
		int rem = n % 10;
		sum = sum * 10 + rem;
		reverse(n/10);
		
			
	}

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		reverse(1234);
		System.out.println(sum);

	}

}
package xyz;

public class XYZ {
	static int sum =0;
	static void reverse(int n) {
		if(n==0) {
			return;
		}
		int rem = n % 10;
		sum = sum * 10 + rem;
		reverse(n/10);
		
			
	}

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		reverse(1234);
		System.out.println(sum);

	}

}

import java.io.*;
import java.util.*;

public class Main {

  public static void main(String[] args){
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    int i = scn.nextInt();
    int j = scn.nextInt();
    int k = scn.nextInt();
    int m = scn.nextInt();
    
    //write your code here
    System.out.println(n|(1<<i));
        System.out.println(n & ~(1<<j));
            System.out.println(n^(1<<k));
                System.out.println((n & (1<<m==0)) ? "false":"true");

            
            
    /* public static boolean bd(int m){       
    if(m|1==1){
        System.out.println(true);
    }else{
        System.out.println(false);
    }
}*/


}


    
  }
  import java.io.*;
import java.util.*;

public class Main {

  public static void main(String[] args){
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    int count =0;
    //int mask = (n & (~n + 1));
    while(n!=0){
        //for(int i =0; i< mask;i++){
           // int 
           n ^= (n & (~n)+1);
           count++;
    }
           
        //}
   // }
   System.out.println(count);
    
    //write your code here
  }
}

import java.io.*;
import java.util.*;

public class Main {

  public static void main(String[] args){
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    int[] arr = new int[n];
    for(int i = 0 ; i < n; i++){
      arr[i] = scn.nextInt();
    }
    solution(arr);
  }

  public static void solution(int[] arr){
   //write your code here
   int xor =0;
   for(int i =0; i<arr.length;i++){
       xor^= arr[i];
   } 
   for(int i=1;i<=arr.length;i++){
       xor^= i;
       
   }
  
   int rsb = xor & -xor;
   
   int x =0;
   int y =0;
   
   for(int val : arr){
       if((val & rsb)==0){
           x^= val;
       }else{
           y^= val;
       }
   }
   for(int i=1;i<arr.length;i++){
       if((i & rsb)==0){
           x^=i;
           
       }else{
           y^=i;
           
       }
   }
   for(int val: arr){
       if(val==x){
           System.out.println(y);
                      System.out.println(x);
                      break;

           
       }else if(val ==y){
                      System.out.println(x);
                                 System.out.println(y);
                                 break;


       }
   }
  }

}

public class Main {

  public static void main(String[] args){
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    int[] arr = new int[n];
    for(int i = 0 ; i < n; i++){
      arr[i] = scn.nextInt();
    }
    solution(arr);
  }

  public static void solution(int[] arr){
   //write your code here
   int ans =0;
   for(int i =0; i< 32;i++){
       int count =0;
    for(int j =0; j<arr.length;j++){
        if((arr[j]&(1<<i)) !=0){
            count++;
        }
    }
    if(count%3 !=0){
        ans |= (1<<i);
    }
   }
   
   System.out.println(ans);
  }

}
import java.io.*;
import java.util.*;

public class Main {

	public static void solution(int[] arr){
		//write your code here
		int count =0;
		for(int i=0; i<arr.length;i++){
		    int xor = arr[i];
		for(int k = i+1;k<arr.length;k++){
		    xor^=arr[k];
		    if(xor==0){
		        count += (k-i);
		    }
		}
		}
		System.out.println(count);
		
		
    }
	public static void main(String[] args) {
		Scanner scn = new Scanner(System.in);
		int n = scn.nextInt();
        int[] arr = new int[n];
        for(int i = 0 ; i < arr.length; i++){
            arr[i] = scn.nextInt();
        }
        solution(arr);
    }
    
	
}
import java.io.*;
import java.util.*;

public class Main {

    public static int solution(int n) {
        //write your code here
        int ans =0;
        int count = 0;
        long m = (long)n;
        while(m !=1){
            if(m % 2 ==0){
                m =m/2;
                count++;
            }else{
               // count++;
               if(m==3){
                   count+=2;
                   m=1;
               }else{
                   count++;
                   if(m % 4==0){
                       m-=1;
                   }else{
                       m+=1;
                   }
               }
            }
        }
        return count;
    }
    
	public static void main(String[] args) {
		Scanner scn = new Scanner(System.in);
		int n = scn.nextInt();
        System.out.println(solution(n));
    }
	
	
}
import java.io.*;
import java.util.*;

public class Main {
    public static long ncr(long n, long r){
        if(n < r){
            return 0L;    
        }
        
        long res = 1L;
        
        for(long i = 0L; i < r; i++){
            res = res * (n - i);
            res = res / (i + 1);
        }
        
        return res;
    }
    
    public static long solution(long n, int k, int i) {
      if(i==0){
          return 0;
      }
      long mask= 1L << i;
      long res =0;
      if((n & mask)==0){
          res = solution(n,k,i-1);
          
      }else{
          long res1 = solution(n, k-1,i-1);
          long res0 = ncr(i,k);
          res = res1 + res0;
          
      }
      return res;
    }
    
    public static int csb(long n){
        int res = 0;
        
        while(n > 0){
            long rsb = n & -n;
            n -= rsb;
            res++;
        }
        
        return res;
    }
    
	public static void main(String[] args) {
		Scanner scn = new Scanner(System.in);
        long n = scn.nextLong();
        int k = csb(n);
        System.out.println(solution(n, k, 63));
    }
	
	
}


