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
