/*Reverse Array

Reverse an array in-place without using another array.
Example: [1, 2, 3, 4, 5] → [5, 4, 3, 2, 1]*/
//1
#include<iostream>
using namespace std;
int main(){
    int arr[]={1, 2, 3, 4, 5};
    int n=sizeof(arr)/sizeof(arr[0]);
    int start=0;
    int end=n-1;
    while(start<end){
        swap(arr[start],arr[end]);
        start++;
        end--;
    }
    for(int i=0;i<n;i++)
    cout<<arr[i]<<' ';
}
//2
#include<iostream>
using namespace std;
int main(){
    int arr[]={1, 2, 3, 4, 5};
    int n=sizeof(arr)/sizeof(arr[0]);
    for(int i=0;i<n/2;i++){
        swap(arr[i],arr[n-1-i]);
    }
    for(int i=0;i<n;i++){
        cout<<arr[i];
    }
}
//3 --> with creating an array
#include<iostream>
using namespace std;
int main(){
    int arr[]={1, 2, 3, 4, 5};
    int n=sizeof(arr)/sizeof(arr[0]);
    int temp[n];
    int i=n-1;
    int j=0;
    while(i>=0){
        temp[j]=arr[i];
        j++,i--;
    }
    for(int i=0;i<n;i++){
        cout<<temp[i];
    }
}
