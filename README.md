# Cognorise-Infotech-
Number_Guessing_Game
import java.util.Random;
import java.util.Scanner;

	public class NumberGuessingGame {
	    public static void main(String[] args) {
	        Scanner scanner = new Scanner(System.in);
	        Random random = new Random();

	        int randomNumber = random.nextInt(100) + 1; // Generates a random number between 1 and 100
	        int attempts = 0;
	        final int MAX_ATTEMPTS = 5; // Predefined limit for attempts

	        System.out.println("Welcome to the Number Guessing Game!");
	        System.out.println("I have chosen a number between 1 and 100. Can you guess it?");

	        while (attempts < MAX_ATTEMPTS) {
	            System.out.print("Enter your guess: ");
	            int guess = scanner.nextInt();
	            attempts++;

	            if (guess < randomNumber) {
	                System.out.println("Too low! Try again.");
	            } else if (guess > randomNumber) {
	                System.out.println("Too high! Try again.");
	            } else {
	                System.out.println("Congratulations! You guessed the number (" + randomNumber + ") correctly!");
	                System.out.println("It took you " + attempts + " attempts.");
	                return; // End the program
	            }
	        }

	        System.out.println("Sorry, you've run out of attempts!");
	        System.out.println("The correct number was: " + randomNumber);
	    }
	}
	

