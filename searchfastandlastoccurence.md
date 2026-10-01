/*Given a sorted array:

arr = {1, 2, 2, 2, 3, 4, 5, 5, 6}

Write a C++ program using Binary Search to find the first and last occurrence of:

target = 2
Expected Output
First occurrence = 1
Last occurrence = 3*/
#include<iostream>
using namespace std;
int main(){
    int arr[]={1, 2, 2, 2, 3, 4, 5, 5, 6};
    int n=sizeof(arr)/sizeof(arr[0]);
    int mid,start=0, end=n-1,first=-1,last=-1,target=2;
    while(start<=end){
        mid=start+(end-start/2);
        if(arr[mid]==target){
            first=mid;
            end=mid-1;
        }
        else if(arr[mid]>target){
            end=mid-1;
        }
        else
        start=mid+1;
    }
    start=0;end=n-1;
    while(start<=end){
        mid=start+(end-start/2);
        if(arr[mid]==target){
            last=mid;
            start=mid+1;
        }
        else if(arr[mid]>target){
            end=mid-1;
        }
        else
        start=mid+1;

}
cout<<first<<last;

}
