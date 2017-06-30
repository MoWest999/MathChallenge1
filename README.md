# MathChallenge1
import java.util.Scanner;

/**
 * Created by Grand Circus Student on 6/30/2017.
 */
public class MathChallenge {
    public static void main(String[] args) {

        int userInput = 0;
        int x = 0;
        int y = 0;
        int z = 0;
        int sumNum = 0;
        int a = 0;
        int b = 0;
        int c = 0;

        System.out.print("Please enter a three digit #,  no smaller than 121: ");

        Scanner scnr = new Scanner(System.in);

        userInput = scnr.nextInt();

        x = userInput % 10; // will give number in the 1s spot
        y = (userInput - x); // will give a number that now is divisible by 10
        z = y / 10; // will end up with a two digit number to start the loop again
        a = z % 10; // isolates number in the tens spot
        b = (z - a);
        c = (b / 10);  // will give number in the hundreds spot
        sumNum = (x * x * x + a * a * a + c * c * c);

        if (sumNum == userInput) {
            System.out.println(userInput +
                    " True.");
        }
        else{
            System.out.println("False");
        }

        // System.out.print("true " + sumNum);

/* I realize this is very primitive - and I didn't use any while or looping... wasn't too confident in those... by the time for the class, tho - I'll be much better!!
*/
    }
}
