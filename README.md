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
