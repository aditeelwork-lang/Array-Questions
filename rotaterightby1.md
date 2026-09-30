/*Rotate Array by 1

Rotate an array one position to the right.
Example: [1, 2, 3, 4, 5] → [5, 1, 2, 3, 4] */
#include<iostream>
using namespace std;
int main(){
  int arr[]={1, 2, 3, 4, 5};
  int n=sizeof(arr)/sizeof(arr[0]);
  int temp=arr[n-1];
  for(int i=n-1;i>0;i--)
  arr[i]=arr[i-1];
  arr[0]=temp;
  for(int i=0;i<n;i++)
  cout<<arr[i];
}
