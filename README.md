import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int caseNum = scan.nextInt();
        for (int i=0; i<caseNum; i++) {
            int n = scan.nextInt();
            int a[] = new int[n];
            for (int j=0; j<n; j++) {
                a[j] = scan.nextInt();
            }
            System.out.println(calArr(a));
        }
    }
    
    private static double getAverage(int[] arr) {
        double avg = 0.0;
        return avg;
    }
    
    private static int calArr(int[] arr) {
        int sum = 1;
        for (int i=1; i<arr.length; i++) {
            sum++;
            int num = 1;
            while (num <= i && arr[i] > arr[i-num]) {
                sum++;
                num++;
            }
        }
        return sum;
    }
}
