# Repo-1
Maximum Sum of Sub-array using Kadane's Algorithm

import java.util.*;

public class MaxSumOfArray
{
  public static void main(String[] args)
  {
    int[] a = {-2,1,-3,4,-1,2,1,-5,4};
    int max_so_far = Integer.MIN.VALUE;
    int max_ending_here = 0;
    int start = 0, end = 0, s = 0;
    for(int i = 0; i < 5; i++)
    {
      max_ending_here = max_ending_here + a[i];

     if(max_so_far < max_ending_here)
     {
       max_so_far = max_ending_here;
       start = s;
       end = i;
     }
     if(max_ending_here < 0)
     {
       max_ending_here = 0;
       s = i+1;
     }
  }
   System.out.println("The Starting Element is: "+start);
   System.out.println("The Ending Element is: "+end);
  System.out.println("Maximum sum of subarray is: "+max_so_far);
}
}

    
