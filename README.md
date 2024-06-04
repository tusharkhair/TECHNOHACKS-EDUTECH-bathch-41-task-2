import java.util.Random;
import java.util.Scanner;

public class NumberGuessingGame {
  public static void main(String[] args) {
    // Generate a random number between 1 and 100
    Random rand = new Random();
    int secretNumber = rand.nextInt(100) + 1;

    // Create a scanner to read user input
    Scanner scanner = new Scanner(System.in);

    int guess;
    do {
      // Ask the user to guess a number
      System.out.print("Guess a number between 1 and 100: ");
      guess = scanner.nextInt();

      // Give hints to the user
      if (guess < secretNumber) {
        System.out.println("Too low! Try again.");
      } else if (guess > secretNumber) {
        System.out.println("Too high! Try again.");
      }
    } while (guess!= secretNumber);

    // Congratulations! The user guessed the correct number
    System.out.println(" Congratulations! You guessed the correct number: " + secretNumber);
  }
}
