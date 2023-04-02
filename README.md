# java-faktoriyelhesaplama
java-faktoriyelhesaplama

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner klavye = new Scanner(System.in);
        System.out.print("N Değerini Giriniz : ");
        int n = klavye.nextInt();

        System.out.print("R Değerini Giriniz : ");
        int r = klavye.nextInt();

        double f1 = 1;
        for (int i = 2; i <= n; i++) {
            f1 *= i;
        }

        double f2 = 1;
        for (int i = 2; i <= n-r; i++) {
            f2 *= i;
        }

        double f3 = 1;
        for (int i = 2; i <= r; i++) {
            f3 *= i;
        }

        double result = f1 / (f2 * f3);

        System.out.print("C(" + n + "," + r + ") = " + result);
    }
}
