# -Most-Imp-Que-HashMap-in-Java-

## Majority Element in Leetcode in Java

import java.util.*;
class Main {
    public static void MajorityEle(int nums[]) {
        HashMap<Integer,Integer> m = new HashMap<>();
        int n= nums.length;
        for(int i=0;i<n;i++){
            
           if(m.containsKey(nums[i])){ // true return function()
           
           
           m.put(nums[i], m.get(nums[i])+1);
           }
           else{
               m.put(nums[i],1);
           }
        }
        for(int i: m.keySet()) {
            if(m.get(i) > n/3){
                System.out.println(i);
            }
        }
    }
    public static void main (String[] args) {
    int  nums[] = {1,3,2,5,1,3,1,5,1};
    MajorityEle(nums);
    }
}
//------------------------------------------------------------------------=========================================================================================
 
 Que2 - Subarray sum qeual to k 
 
 
 import java.util.*;
class Main {
  public static void main (String[] args) {
    int  arr[] = {10,2,-2,-20,10}; //ans = 3
    int k=-10;
    
        HashMap<Integer,Integer> m = new HashMap<>(); //   <key,frequency>
        m.put(0,1);
        int ans=0;
        int sum=0;
        
        for(int i=0;i<arr.length;i++){
            sum+=arr[i];
            if(m.containsKey(sum-k)){
                ans+=m.get(sum-k);
                 
            }
            if(m.containsKey(sum)){
                m.put(sum,m.get(sum)+1);
            }
            else{
                m.put(sum,1);
            }
            
            
        }
        System.out.println("the Ans "+ans);
    }
}
 
 
 
 
 
 
 
 
 
 
 
 


