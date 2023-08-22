(https://www.geeksforgeeks.org/find-a-peak-in-a-given-array/)



Given an array arr[] of integers. Find a peak element i.e. an element that is not smaller than its neighbors. 

Note: For corner elements, we need to consider only one neighbor. 




Input: array[]= {5, 10, 20, 15}
Output: 20
Explanation: The element 20 has neighbors 10 and 15, both of them are less than 20.

Input: array[] = {10, 20, 15, 2, 23, 90, 67}
Output: 20 or 90
Explanation: The element 20 has neighbors 10 and 15, both of them are less than 20, similarly 90 has neighbors 23 and 67.







// A C++ program to find a peak element
#include <bits/stdc++.h>
using namespace std;

// Find the peak element in the array
int findPeak(int arr[], int n)
{
	// first or last element is peak element
	if (n == 1)
		return 0;
	if (arr[0] >= arr[1])
		return 0;
	if (arr[n - 1] >= arr[n - 2])
		return n - 1;

	// check for every other element
	for (int i = 1; i < n - 1; i++) {

		// check if the neighbors are smaller
		if (arr[i] >= arr[i - 1] && arr[i] >= arr[i + 1])
			return i;
	}
}

// Driver Code
int main()
{
	int arr[] = { 1, 3, 20, 4, 1, 0 };
	int n = sizeof(arr) / sizeof(arr[0]);
	cout << "Index of a peak point is " << findPeak(arr, n);
	return 0;
}

********************************************************************************************************************************************************************************************

[https://leetcode.com/problems/find-peak-element/description/]
**********************************************************************************************************
class Solution {
public:
    int findPeakElement(vector<int>& nums) {
        int n=nums.size();
        int start=0;
        int end=n-1;
        while(start<end)
        {
            int mid=start+(end-start)/2;
            if(nums[mid]>nums[mid+1]){end=mid;}
            else {start=mid+1;}
        }
        return start;
    }
};
************************************************************************************************************
