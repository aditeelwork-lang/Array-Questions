/* Fibonacci — nth Position

Find the nth Fibonacci number using an iterative approach.
Example: n = 6 → 8
Assume: F(0)=0, F(1)=1 */
#include<iostream>
using namespace std;
int main(){
    int arr[50];
    arr[0]=0;
    arr[1]=1;
    int n;
    cout<<"enter n";
    cin>>n;
    for(int i=2;i<=n;i++){
    arr[i]=arr[i-1]+arr[i-2];
    
}
 cout<<arr[n];
}
