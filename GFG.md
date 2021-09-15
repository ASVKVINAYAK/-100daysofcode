
## #100Days of Geekforgeeks

#  Day1

Date: 15/09/21

1 [Solved sort 0 1 and 2 ](https://practice.geeksforgeeks.org/problems/sort-an-array-of-0s-1s-and-2s4231/1)
*** Solved it by Dutch national Problem method***
```bash 
  class Solution
{
    public static void sort012(int arr[], int n)
    {
        // code here 
        int low,high,current,temp;
   low = current = 0;
  high = n-1;
  while(current<=high){
 switch (arr[current]) 
 { 
 case 0:{
 temp = arr[low];
 arr[low] = arr[current];
 arr[current] = temp;
 low++;
 current++;
 break;
 }
 case 1:{
 current++;
 break;
 }
 case 2:{
     temp = arr[high];
 arr[high] = arr[current];
 arr[current] = temp;
 high--;
 break;
 }
 }
  }
}
}
```
