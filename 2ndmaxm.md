/*Find the second largest distinct element in an array without sorting.
Example: [10, 5, 20, 8, 20] → 10*/
#include<iostream>
#include<climits>
using namespace std;
int main(){
    int maxm=INT_MIN;
    int arr[]={10,5,20,8,20};
    int n=sizeof(arr)/sizeof(arr[0]);
    for(int i=0;i<n;i++){
    if(arr[i]>maxm){
        maxm=arr[i];
    }
    }
    int second=INT_MIN;
    for(int i=0;i<n;i++){
        if(maxm!=arr[i]){
            second=max(second,arr[i]);
        }
    }
    cout<<maxm;
    cout<<second;
}
