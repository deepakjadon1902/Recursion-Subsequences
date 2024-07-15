
import java.util.Scanner;

public class Main {
    static int count = 0;

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String str = scanner.next();
        printSubsequences(str, "");
        System.out.println();
        System.out.println((int)Math.pow(2, str.length()));
    }

    public static void printSubsequences(String str, String curr) {
        if (str.isEmpty()) {
            System.out.print(curr + " ");
            count++;
            return;
        }
        printSubsequences(str.substring(1), curr);
        printSubsequences(str.substring(1), curr + str.charAt(0));
    }
}
