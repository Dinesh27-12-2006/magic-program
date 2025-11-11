# magic-program
public class magic {
    public static void main(String[] args) {
        int n = 19; // Example number
        int original = n;
        int sum = 0;

        while (n != 0) {
            int digit = n % 10;
            sum += digit; // Add the last digit to sum
            n /= 10; // Remove the last digit
        }

        // Check if the sum is a single-digit number
        while(sum >= 10) {
            int tempSum = 0;
            while (sum != 0) {
                tempSum += sum % 10; // Add the last digit of sum
                sum /= 10; // Remove the last digit
            }
            sum = tempSum; // Update sum with the new sum of digits
        }

        if (sum == 1) {
            System.out.println("Magic Number");
        } else {
            System.out.println("Not a Magic Number");
        }
    }
    
}
