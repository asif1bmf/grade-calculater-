import java.util.Scanner;

public class GradeCalculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int totalSubjects = 5;
        int[] marks = new int[totalSubjects];
        int total = 0;

        System.out.println("Enter marks for " + totalSubjects + " subjects (out of 100):");

        for (int i = 0; i < totalSubjects; i++) {
            System.out.print("Subject " + (i + 1) + ": ");
            marks[i] = sc.nextInt();

            if (marks[i] < 0 || marks[i] > 100) {
                System.out.println("Invalid marks! Enter between 0 and 100.");
                i--;
                continue;
            }

            total += marks[i];
        }

        double average = total / (double) totalSubjects;
        String grade;

        if (average >= 90) grade = "A+";
        else if (average >= 80) grade = "A";
        else if (average >= 70) grade = "B";
        else if (average >= 60) grade = "C";
        else if (average >= 50) grade = "D";
        else grade = "F";

        System.out.println("\n--- Result ---");
        System.out.println("Total Marks: " + total + "/500");
        System.out.println("Average: " + average);
        System.out.println("Grade: " + grade);

        boolean pass = true;
        for (int mark : marks) {
            if (mark < 35) {
                pass = false;
                break;
            }
        }

        if (pass && !grade.equals("F")) {
            System.out.println("Status: PASS ✅");
        } else {
            System.out.println("Status: FAIL ❌");
        }

        sc.close();
    }
}
