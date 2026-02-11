# NumberGame.java
import java.util.Scanner;
import java.util.Random;

public class Main {
    public static void main(String[] args) {

       Scanner sc = new Scanner(System.in);
      //main a=new main
        Random rand = new Random();

        int number = rand.nextInt(100) + 1;  // 1 to 100
        int guess = 0;

        System.out.println("Guess a number between 1 and 100:");

        while (guess != number) {

            System.out.print("Enter your guess: ");
            guess = sc.nextInt();

            if (guess > number) {
                System.out.println("Too High!");
            } 
            else if (guess < number) {
                System.out.println("Too Low!");
            } 
            else {
                System.out.println("Correct! You guessed it 🎉");
            }
        }

        sc.close();
    }
}