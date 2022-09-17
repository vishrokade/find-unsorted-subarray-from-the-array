# find-unsorted-subarray-from-the-array

package vishal;

public class findUnsortedSubarray {
	public static void main(String[] args) {
	int[] nums= {1,1,7,2,2,2};
    int start=-1;
    int end=-1; 
    int ans = 0;
    
    for(int i=0; i<nums.length-1; i++)
    {
        
        if(nums[i]>nums[i+1])
        {
            start = i;
            break;
        }
    }
    
     for(int j=nums.length-1; j>0; j--)
     {
        if(nums[j] < nums[j-1])
        {
            end = j;
            break;
        }
    }
    if(start==end){
       ans = 0;
    }
    else {
  ans= (end-start)+1;
    }
  System.out.println(ans);
};
}
/* int n = nums.length;
        int end = -1, max = nums[0];
        for (int i = 1; i < n; i++){
            if (nums[i] < max)  
                end = i;
            else    
                max = nums[i];
        }
        int start = 0, min = nums[n - 1];
        for (int i = n - 2; i >= 0; i--){
            if (nums[i] > min)  
                start = i;
            else
                min = nums[i];
        }
        return end - start + 1;
        */
