
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

#  Day2

Date: 16/09/21

2 [Solved N numbers  ](https://practice.geeksforgeeks.org/problems/n-meetings-in-one-room-1587115620/1#)

*** Solved it in C++***
```bash 
 // { Driver Code Starts
#include <bits/stdc++.h>
using namespace std;

 // } Driver Code Ends
class Solution
{
    public:
    //Function to find the maximum number of meetings that can
    //be performed in a meeting room.
   int maxMeetings(int start[], int end[], int n)
    {
        // Your code here
        vector<pair<int,int>> p;
       for(int i=0;i<n;i++){
           p.push_back({start[i],end[i]});
       }
       sort(p.begin(),p.end());
       int count=0;
       int l=-1;
       
       for(auto i : p){
           if(i.first > l){
               count++;
               l=i.second;
           }
           else if(i.second < l){
               l=i.second;
           }
       }
       return count;
    }
};

// { Driver Code Starts.
int main() {
    int t;
    cin >> t;
    while (t--) {
        int n;
        cin >> n;
        int start[n], end[n];
        for (int i = 0; i < n; i++) cin >> start[i];

        for (int i = 0; i < n; i++) cin >> end[i];

        Solution ob;
        int ans = ob.maxMeetings(start, end, n);
        cout << ans << endl;
    }
    return 0;
}  // } Driver Code Ends
```
