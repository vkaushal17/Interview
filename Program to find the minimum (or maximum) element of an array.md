
[https://www.geeksforgeeks.org/program-find-minimum-maximum-element-array/]

// CPP program to find minimum (or maximum) element
// in an array.
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