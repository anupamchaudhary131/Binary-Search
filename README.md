# Binary-Search
package com.company;
import java.util.*;

class Binary_Search{
    public static int Binary_func(int arr[], int n, int ele)
    {
        int low=0, count=0;
        int high=n-1;
        while(low<high)
        {
            int mid=(low+high)/2;
            if(arr[mid]>ele)
            {
                high=mid-1;
            }
            else if(arr[mid]<ele)
            {
                low=mid+1;
            }
            else
            {
                count++;
            }
        }
        return count;
    }
}

public class DSA_Binary_Search extends Binary_Search{
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int arr[] = {10,20,30,40,50,60,70,80};
        int n = arr.length;
        System.out.println(Arrays.toString(arr));
        System.out.println("Enter the element which you want to search in the array.");
        int ele = sc.nextInt();
        int val = Binary_func(arr,n,ele);
        if(val==0) {
            System.out.println("Element "+ele+ " is not found in the array.");
        }
        else{
            System.out.println("Element "+ele+ " is found in the array.");
        }
    }
}
