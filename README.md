package com.company;

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);
        float change;
        do {
            System.out.print("Change owed: ");
            change = input.nextFloat();
        } while (change <= 0f);

        int cents = Math.round(change * 100);
        int coins = 0;

        int denomination[] = {25,10,5,1};

        for (int i=0; i < 4; i++) {

            coins += cents/denomination[i];
            cents = cents % denomination[i];
        }
        System.out.println(coins);
    }

}
