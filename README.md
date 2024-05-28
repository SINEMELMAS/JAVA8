# JAVA8
package lab2;
import java.util.Scanner;
class FactorialCalculations {
    static long calculateFactorial(int i) {
        if (i == 0 || i == 1) {
            return 1;
        } else {
            return i * calculateFactorial(i - 1);
        }
    }
}
public class Q1 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Please enter a number: ");
        int num = scanner.nextInt();

        scanner.close();

        if (num < 0) {
            System.out.println("Error! Value can not be a negative number.");
        } else {
        	FactorialCalculations factorialCalculations = new FactorialCalculations();
            long result = factorialCalculations.calculateFactorial(num);
            System.out.println("Factorial of " + num + " is: " + result);
        }
    }
}
