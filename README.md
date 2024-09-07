# StudentMarksGradeCalculator
i develop this Student marks grade calculator using java programming 
import java.util.Scanner;

public class studentMarksGradeCalculator {
        public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in);

            // Step 1: Take marks obtained in each subject
            System.out.print("Enter the number of subjects: ");
            int numSubjects = scanner.nextInt();
            double[] marks = new double[numSubjects];

            for (int i = 0; i < numSubjects; i++) {
                System.out.print("Enter the marks obtained in subject " + (i + 1) + " (out of 100): ");
                marks[i] = scanner.nextDouble();
            }

            // Step 2: Calculate Total Marks
            double totalMarks = 0;
            for (double mark : marks) {
                totalMarks += mark;
            }

            // Step 3: Calculate Average Percentage
            double averagePercentage = totalMarks / numSubjects;

            // Step 4: Grade Calculation
            char grade;
            if (averagePercentage >= 90) {
                grade = 'A';
            } else if (averagePercentage >= 80) {
                grade = 'B';
            } else if (averagePercentage >= 70) {
                grade = 'C';
            } else if (averagePercentage >= 60) {
                grade = 'D';
            } else {
                grade = 'F';
            }

            // Step 5: Display Results
            System.out.println("\nResults:");
            System.out.println("Total Marks: " + totalMarks);
            System.out.println("Average Percentage: " + averagePercentage + "%");
            System.out.println("Grade: " + grade);

            scanner.close();
        }
    }

