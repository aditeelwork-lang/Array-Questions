//[10, 20, 30, 40], target 30 → 2
#include<iostream>
using namespace std;
int main(){
    int arr[]={10,20,30,40};
    int n=sizeof(arr)/sizeof(arr[0]);
    int target=30;
    for(int i=0;i<n;i++){
        if(arr[i]==target)
         cout<<i;
    }
}
