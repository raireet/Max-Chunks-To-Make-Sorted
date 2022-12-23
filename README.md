# Max-Chunks-To-Make-Sorted

Sample Input 0

5

1 0 2 3 4

Sample Output 0

2

Explanation

We can split them into two chunks, such as [1, 0], [2, 3, 4]. However, splitting into [1, 0], [2], [3], [4] is the highest number of chunks possible.


/* package codechef; // don't place package name! */
import java.util.*;
import java.lang.*;
import java.io.*;

/* Name of the class has to be "Main" only if the class is public. */
public class Main
{
    public static void main (String[] args) throws java.lang.Exception
    {
        // your code goes here
		Scanner sc = new Scanner(System.in);
		int n = sc.nextInt();
		int [] arr = new int[n];
		for(int i =0;i<n;i++){
			
			arr[i] = sc.nextInt();

		}
		int cmax = Integer.MIN_VALUE;
		int ans = 0;
		for(int i = 0;i < arr.length;i++){
			cmax = Math.max(cmax , arr[i]);
			if(cmax == i){
				ans++;
			}
		}
		System.out.print(ans);
    }
}
