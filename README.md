# A2OJ
package test;

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

    	
        Scanner scanner = new Scanner(System.in);
        int T = scanner.nextInt();
        int[][] a = new int[T][];
        int[][] b = new int[T][10];

        for (int t = 0; t < T; t++) {
            int N = scanner.nextInt();
            a[t] = new int[N];

            int n = 0;
            while (n < N)
                a[t][n++] = scanner.nextInt();

            for (int i = 0; i < N; i++)
                b[t][a[t][i]]++;
        }
        scanner.close();

        for (int t = 0; t < T; t++) {
            int squares = 0;
            for (int p = 0; p < 10; p++) {
                squares += (int) (b[t][p] / 4);

            }
            System.out.println(squares);
        }
        scanner.close();

    }

}
