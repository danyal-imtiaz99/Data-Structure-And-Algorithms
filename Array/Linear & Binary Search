/**
 * Search Algorithms Implementation
 * @author YourName
 */
public class SearchAlgorithms {
    
    // Linear Search - O(n) time, O(1) space
    public static int linearSearch(int[] arr, int target) {
        for (int i = 0; i < arr.length; i++) {
            if (arr[i] == target) return i;
        }
        return -1;
    }
    
    // Binary Search Iterative - O(log n) time, O(1) space
    public static int binarySearch(int[] arr, int target) {
        int left = 0, right = arr.length - 1;
        
        while (left <= right) {
            int mid = left + (right - left) / 2;
            
            if (arr[mid] == target) return mid;
            else if (arr[mid] < target) left = mid + 1;
            else right = mid - 1;
        }
        return -1;
    }
    
    // Binary Search Recursive - O(log n) time, O(log n) space
    public static int binarySearchRecursive(int[] arr, int target) {
        return binarySearchHelper(arr, target, 0, arr.length - 1);
    }
    
    private static int binarySearchHelper(int[] arr, int target, int left, int right) {
        if (left > right) return -1;
        
        int mid = left + (right - left) / 2;
        
        if (arr[mid] == target) return mid;
        else if (arr[mid] < target) return binarySearchHelper(arr, target, mid + 1, right);
        else return binarySearchHelper(arr, target, left, mid - 1);
    }
    
    // Find first occurrence (for duplicates)
    public static int findFirst(int[] arr, int target) {
        int left = 0, right = arr.length - 1, result = -1;
        
        while (left <= right) {
            int mid = left + (right - left) / 2;
            
            if (arr[mid] == target) {
                result = mid;
                right = mid - 1;
            } else if (arr[mid] < target) {
                left = mid + 1;
            } else {
                right = mid - 1;
            }
        }
        return result;
    }
    
    // Find last occurrence (for duplicates)
    public static int findLast(int[] arr, int target) {
        int left = 0, right = arr.length - 1, result = -1;
        
        while (left <= right) {
            int mid = left + (right - left) / 2;
            
            if (arr[mid] == target) {
                result = mid;
                left = mid + 1;
            } else if (arr[mid] < target) {
                left = mid + 1;
            } else {
                right = mid - 1;
            }
        }
        return result;
    }
    
    // Test driver
    public static void main(String[] args) {
        int[] arr = {1, 2, 4, 4, 4, 7, 9};
        
        System.out.println("Linear Search (4): " + linearSearch(arr, 4));
        System.out.println("Binary Search (4): " + binarySearch(arr, 4));
        System.out.println("First occurrence (4): " + findFirst(arr, 4));
        System.out.println("Last occurrence (4): " + findLast(arr, 4));
    }
}
