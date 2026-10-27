
package com.pakagehospitalmanegment;

import java.util.Scanner;

public class Hospitalmanegment {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        Patient[] p = new Patient[10];
        int count = 0;
        int choice;
 
        do {
            System.out.println("\n1. Add Patient");
            System.out.println("2. Display Patients");
            System.out.println("3. Calculate Bill");
            System.out.println("4. Exit");
            System.out.print("Enter choice: ");
            choice = sc.nextInt();

            switch (choice) {
                case 1:
                    if (count < p.length) {
                        System.out.print("Enter ID: ");
                        int id = sc.nextInt();

                        sc.nextLine();
                        System.out.print("Enter Name: ");
                        String name = sc.nextLine();

                        System.out.print("Enter Age: ");
                        int age = sc.nextInt();

                        System.out.println("1. Normal Patient");
                        System.out.println("2. InPatient");
                        int type = sc.nextInt();

                        if (type == 1) {
                            p[count] = new Patient(id, name, age);
                        } else if (type == 2) {
                            System.out.print("Enter Days: ");
                            int days = sc.nextInt();
                            p[count] = new Inpateint(id, name, age, days);
                        } else {
                            System.out.println("Invalid patient type!");
                            break;
                        }

                        count++;
                        System.out.println("Patient Added!");
                    } else {
                        System.out.println("Patient list is full!");
                    }
                    break;

                case 2:
                    for (int i = 0; i < count; i++) {
                        p[i].display();
                    }
                    break;

                case 3:
                    for (int i = 0; i < count; i++) {
                        p[i].display();
                        System.out.println("Bill: Rs. " + p[i].bill());
                    }
                    break;

                case 4:
                    System.out.println("Thank You!");
                    break;

                default:
                    System.out.println("Invalid Choice!");
            }

        } while (choice != 4);

        sc.close();
    }
}
