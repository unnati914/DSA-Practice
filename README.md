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
class Solution {
    public List<Integer> grayCode(int n) {
 	 List<Integer> ans = new ArrayList<>();
 	 fun(n, ans);
 	 return ans;
     }
     
     public static void fun(int n , List<Integer> ans){
         if(n==0){
             ans.add(0);
             return;
         }
         fun(n-1,ans);
         for(int i = ans.size()-1;i>=0;i--){
             ans.add(ans.get(i) | (1<<(n-1)));
         }
     }

}
	import java.io.*;
import java.util.*;

public class Main {

    public static int solution(int[] arr){
       //write your code here
       int ans =0;
       for(int val : arr){
           ans = ans ^ (2 * val);
           
       }
       
       return ans;
    }
	public static void main(String[] args) {
		Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        int[] arr = new int[n];
        for(int i = 0 ; i < n; i++){
            arr[i] = scn.nextInt();
        }
        System.out.println(solution(arr));
    }
    
   }
			      
			      import java.util.Scanner;
 
class ChkPalindrome
{
   public static void main(String args[])
   {
      String str, rev = "";
      Scanner sc = new Scanner(System.in);
 
      System.out.println("Enter a string:");
      str = sc.nextLine();
 
      int length = str.length();
 
      for ( int i = length - 1; i >= 0; i-- )
         rev = rev + str.charAt(i);
 
      if (str.equals(rev))
         System.out.println(str+" is a palindrome");
      else
         System.out.println(str+" is not a palindrome");
 
   }
}
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        // write your code here
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        
        for(int i =0; i <arr.length;i++){
            arr[i] = scn.nextInt();
        }
        
        int d = scn.nextInt();
       int fi =  firstIndex(arr,0,d);
        System.out.println(fi);
    }

    public static int firstIndex(int[] arr, int idx, int x){
        if(idx == arr.length){
            return -1;
        }
        int fiisa = firstIndex(arr,idx + 1,x);
        if(arr[idx] == x){
            return idx;
        }else{
            return fiisa;
        }
        
    }

}
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        // write your code here
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        int[] arr = new int[n];
        for(int i =0; i <arr.length;i++){
            arr[i] = scn.nextInt();
        }
        
        int d = scn.nextInt();
       int li =  firstIndex(arr,0,d);
        System.out.println(fi);
    }

    public static int lastIndex(int[] arr, int idx, int x){
        if(idx == arr.length){
            return -1;
        }
        int liisa = lastIndex(arr,idx + 1,x);
        if(liisa = -1){
            if(arr[idx] == x)
        
            return idx;
        } else{
            return -1;
        }
    } 
        else{
            return liisa;
        }
        
    }


        

import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        Scanner scn = new Scanner(System.in);
        int n = scn.nextInt();
        ArrayList<String> words = new ArrayList<>();
        System.out.println(words);
        
    }
    static String[] codes = {"abc","def","ghi","jkl","mno","pqrs","tu","vwx","yz"};
    public static ArrayList<String> getKPC(String str) {
        if(str.length() == 0){
            ArrayList<String> bres = new ArrayList<>();
            bres.add("");
            return bres;
        }
        
        char ch = str.charAt(0);//5
        String ros = str.substring(1); //73
        
        ArrayList<String> rres  = getKPS(ros);
        ArrayList<String> mres = new ArrayList<>();
        
        String codeforch = codes[ch];
        for(int i =0; i<codeforch.length();i++){
            char charcode = codeforch.charAt(i);
            
            for(String rstr:rres){
                mres.add(chcode + rstr);
            }
        }
        return mres;
        // null;
    }

}
									import java.io.*;
import java.util.*;

public class Main {

  public static void permutations(int[] boxes, int ci, int ti){
    // write your code here
    if(ci> ti){
        for(int i =0; i<boxes.length;i++){
            System.out.print(boxes[i]);
        }
        System.out.println();
        return;
    }
   // int items-1 = 
   for(int i =0; i<boxes.length;i++){
       if(boxes[i] ==0){
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

  public static void permutations(int cb, int tb, int[] items, int ssf, int ts, String asf){
    if(cb>tb){
        if(ssf == ts){
            System.out.println(asf);
        }
        return;
    }
    
    for(int i =0; i<items.length;i++){
        if(items[i]==0){
            items[i] = cb;
            permutations(cb + 1,tb,items,ssf + 1,ts,asf + (i+1));
            items[i] =0;
        }
    }

        permutations(cb+1,tb,items,ssf,ts,asf + "0");
        
        
    
       // permutations(cb+1,tb,ssf,ts,asf);

  }

  public static void main(String[] args) throws Exception {
    BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
    int nboxes = Integer.parseInt(br.readLine());
    int ritems = Integer.parseInt(br.readLine());
    permutations(1, nboxes, new int[ritems], 0, ritems, "");
  }

}
				       import java.io.*;
import java.util.*;

public class Main {

    public static void queensPermutations(int qpsf, int tq, int[][] chess){
        // write your code here
        if(qpsf == tq){
            for(int i =0; i<chess.length;i++){
                for(int j =0; j<chess[0].length;j++){
                    if(chess[i][j]==0){
                        System.out.print("-\t");
                    }else{
                        System.out.print("q" + chess[i][j] + "\t");
                    }
                }
                System.out.println();
                
            }
            System.out.println();
            return;
        }
        for(int i =0; i< chess.length;i++){
            for(int j =0; j<chess[0].length;j++){
                if(chess[i][j]==0){
                    chess[i][j] = (qpsf+1);
                     queensPermutations(qpsf+1,tq,chess);
                    chess[i][j] = 0;
                }
            }
        }
    }
    public static void main(String[] args) throws Exception {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine());
        int[][] chess = new int[n][n];
        
        queensPermutations(0, n, chess);
    }
}
import java.io.*;
import java.util.*;

public class Main {

    public static void queensPermutations(int qpsf, int tq, int row, int col, String asf, boolean[] queens) {
        if(row == tq){
            if(qpsf == tq){
                System.out.println(asf);
                System.out.println();
                
            }
            return;
            
        }
        int nr = 0;
        int nc =0;
        String sep = "";
        if(col == tq-1){
            nr = row + 1;
            nc =0;
            sep = "\n";
            
        }else{
            nr = row;
            nc = col + 1;
            sep = "\t";
            
        }
        for(int i =0; i< queens.length;i++){
            if(queens[i]==false){
                queens[i] = true;
                queensPermutations(qpsf + 1,tq,nr,nc, asf + "q" +(i+1) + sep, queens);
                queens[i] = false;
            }
       // queensPermutations(qpsf,tq,nr,nc, asf + "-" + sep, queens);

            
        }
                queensPermutations(qpsf,tq,nr,nc, asf + "-" + sep, queens);

    }

    public static void main(String[] args) throws Exception {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine());
        boolean[] queens = new boolean[n];

        queensPermutations(0, n, 0, 0, "", queens);
    }
}
	import java.io.*;
import java.util.*;

public class Main {

    public static void queensCombinations(int qpsf, int tq, boolean[][] chess, int i, int j){
        if(qpsf == tq){
            for(int row =0; row< chess.length;row++){
                for(int col =0; col<chess[0].length;col++){
                    if(chess[row][col]==true){
                        System.out.print("q\t");
                        
                    }else{
                        System.out.print("-\t");
                    }
                    
                }
                System.out.println();
            }
            System.out.println();
            return;
        }
        for(int row = i; row<chess.length;row++){
        for(int col = row == i? j+1 : 0; col<chess[0].length;col++){
            chess[row][col]= true;
            queensCombinations(qpsf + 1, tq,chess,row,col);
            chess[row][col] = false;
        }
        }
    }
    public static void main(String[] args) throws Exception {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine());
        boolean[][] chess = new boolean[n][n];
        
        queensCombinations(0, n, chess, 0, -1);
    }
}
	class Solution {
    public void reverseString(char[] s) {
        int i = 0;
        int j = s.length - 1;
        while(i < j){
            char temp = s[i];
            s[i] = s[j];
            s[j] = temp;
            i++;
            j--;
        }
    }
}
import java.io.*;
import java.util.*;

public class Main {

 

  public static void main(String[] args) throws Exception {
    BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
    String str = br.readLine();
    //int k = Integer.parseInt(br.readLine());
        HashMap<Character,Integer> map = new HashMap<>();
        for(int i =0; i< str.length();i++){
            char ch = str.charAt(i);
            map.put(ch, -1);
            
            
        }
        fun(str, map, 0,new Character[k],0,k);
            int k = Integer.parseInt(br.readLine());


   
  }
  public static void fun(String str, Hashmap<Character, Integer> map, int idx, Character[]spots,int ssf,int ts){
      if(idx == str.length()){
          if(ssf == ts){
              for(int i = 0; i<spots.length;i++){
                  System.out.print(spots[i]);
              }
              System.out.println();
          }
          return;
      }
      char ch = str.charAt(idx);
      int lo = map.get(ch);
      for(int i = lo + 1; i< spots.length;i++){
          if(spots[i]==null){
              spots[i] = ch;
              map.put(ch, i);
              fun(str, map, idx + 1, spots, ssf + 1, ts);
              spots[i] = null;
              map.get(ch, lo);
              
          }
          
      }
      if(lo == -1){
          fun(str, map, idx + 1, spots, ssf, ts);
      }
  }

}
	// { Driver Code Starts
//Initial Template for Java

import java.util.*;

public class GFG
{
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        
        int t = sc.nextInt();
        while (t-- > 0)
        {
            int n = sc.nextInt();
            int A[] = new int[n];
            
            for (int i = 0;i < n;i++)
            {
                A[i] = sc.nextInt();
            }
            int key = sc.nextInt();
            
            System.out.println(new Solution().search(A, 0, n - 1, key));
        }
    }
}// } Driver Code Ends


//User function Template for Java

class Solution
{
    int search(int A[], int key)
    {
        // Complete this function
        int n = A.length;
        int l = 0;
        int h = A.length - 1;
        
        
        while(l <= h){
            int mid = (l + h)/2;
            if(A[mid] == key)
            return mid;
            else if(A[mid] > A[l]){
                if(key <= A[mid] && key >= A[l]){
                    h = mid -1;
                }
                    else{
                        l = mid + 1;
                    }
                    
                    else{
                        if(key <= A[h] && key >= A[mid])
                        l = mid + 1;
                        else{
                            h = mid - 1;
                        }
                        
                    }
                    return -1;
                }
            }
        }
    }
}
	
	/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode() {}
 *     ListNode(int val) { this.val = val; }
 *     ListNode(int val, ListNode next) { this.val = val; this.next = next; }
 * }
 */
class Solution {
    public ListNode deleteDuplicates(ListNode node) {
        if(node == null){
            return node;
        }
        ListNode head = node;
        while(node.next != null){
            if(node.val == node.next.val){
                node.next = node.next.next;
                
            }else{
                node = node.next;
            }
        }
        return head;
        
        
        
    }
}
	/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode() {}
 *     ListNode(int val) { this.val = val; }
 *     ListNode(int val, ListNode next) { this.val = val; this.next = next; }
 * }
 */
class Solution {
    public ListNode mergeTwoLists(ListNode list1, ListNode list2) {
        ListNode dummyHead = new ListNode();
        ListNode tail = dummyHead;
        while(list1 != null && list2 != null){
            if(list1.val < list2.val){
                tail.next = list1;
                list1 = list1.next;
                tail = tail.next;
            }else{
                tail.next = list2;
                list2 = list2.next;
                tail = tail.next;
                
            }
        }
        return dummyHead.next;
    }
}
	/**
 * Definition for singly-linked list.
 * class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) {
 *         val = x;
 *         next = null;
 *     }
 * }
 */
public class Solution {
    public boolean hasCycle(ListNode head) {
      ListNode fast = head;
        ListNode slow = head;
        
        while(fast != null && fast.next != null){
            fast = fast.next.next;
            slow = slow.next;
            
            if(fast == slow){
                return true;
            }
        }
        return false;
    }
}
				      class Solution {
    public int[] intersect(int[] nums1, int[] nums2) {
        int[] freq1 = getfre[nums1];
        int[] freq2 = getfre[nums2];
        
        List<Integer> ans = new ArrayList<>();
        
        for(int i =0; i< freq1.length;i++){
            int count = Math.min(freq1[i], freq2[i]);
            while(count > 0){
                ans.add(i);
            }
        }
        int[] ans = new int[ans.size()];
        for(int i = 0; i< ans.size();i++){
            res[i] = ans.get(i);
            
        }
        return res;
    }
    public int[] getfre(int[] nums){
        int[] nums = new int[1001];
        for(int ele:nums){
            freq[ele]++;
        }
        return freq;
    }
}
	
