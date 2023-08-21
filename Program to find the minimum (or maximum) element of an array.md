
[https://www.geeksforgeeks.org/program-find-minimum-maximum-element-array/]

Given an array, write functions to find the minimum and maximum elements in it. The most simplest way to find min and max value of an element is to use inbuilt function sort()
Time complexity : O(n log(n))
Auxiliary Space : O(n)

if we use recursion Time Complexity: O(n)
Auxiliary Space: O(n), as implicit stack is used due to recursion


#include <bits/stdc++.h>
using namespace std;

int getMin(int arr[], int n)
{
	return *min_element(arr, arr + n);
}

int getMax(int arr[], int n)
{
	return *max_element(arr, arr + n);
}

int main()
{
	int arr[] = { 12, 1234, 45, 67, 1 };
	int n = sizeof(arr) / sizeof(arr[0]);
	cout << "Minimum element of array: " << getMin(arr, n) << "\n";
	cout << "Maximum element of array: " << getMax(arr, n);
	return 0;
}



Time Complexity: O(n)
Auxiliary Space: O(1), as no extra space is used
