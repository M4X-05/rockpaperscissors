package com.company;

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        //creates a variable computerChoice of type string
        String computerChoice;


        //get user input
        System.out.println("Do you choose 'r' for rock, 'p' for paper, or 's' for scissors?");
        //create a Scanner object
        Scanner user_Choice = new Scanner(System.in);

        //read user input
        String userChoice = user_Choice.nextLine();

        //Check if user input is correct
        if (!userChoice.equals("r") && !userChoice.equals("p") && !userChoice.equals("s")) {
            System.out.println("Your Choice is Invalid, Please pick r, s or p");
        } else {
            //random generator to identify computerChoice
            double rand = Math.random() * 100;

            //Assigning a value of r, p or s for computerChoice depending on the random generator
            if (rand < 34) {
                computerChoice = "r";
            } else if (rand < 67) {
                computerChoice = "p";
            } else computerChoice = "s";


            //If the outcome results in a Draw
            if (computerChoice.equals(userChoice)) {
                System.out.println("Draw! Please play again");
            }
            //if and else statements used to identify the winner and loser when player picks "r"/rock
            if (userChoice.equals("r")) {
                if (computerChoice.equals("s")) {
                    System.out.println("You Win!");
                } else {
                    if (computerChoice.equals("p")) {
                        System.out.println("You Lose");
                    }
                }
            }
            //if and else statements used to identify the winner and loser when player picks "p"/paper
            if (userChoice.equals("p")) {
                if (computerChoice.equals("r")) {
                    System.out.println("You Win!");
                } else {
                    if (computerChoice.equals("s")) {
                        System.out.println("You Lose");
                    }
                }
            }
            //if and else statements used to identify the winner and loser when player picks "s"/scissors
            if (userChoice.equals("s")) {
                if (computerChoice.equals("p")) {
                    System.out.println("You Win!");
                } else {
                    if (computerChoice.equals("r"))
                        System.out.println("You Lose");
                    }
                }
            //If statement used to document the computer and player choices
            if (computerChoice.equals("r")) {
                System.out.print("Computer Choice: rock   ");
            }
            if (computerChoice.equals("p")) {
                System.out.print("Computer Choice: paper   ");
            }
            if (computerChoice.equals("s")) {
                System.out.print("Computer Choice: scissors   ");
            }
            if (userChoice.equals("r")) {
                System.out.println("Player Choice: rock");
            }
            if (userChoice.equals("p")) {
                System.out.println("Player Choice: paper");
            }
            if (userChoice.equals("s")) {
                System.out.println("Player Choice: scissors");
            }
            }
        }
    }
