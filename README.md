import java.util.Scanner;

public class StudentGradeTracker {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the number of students: ");
        int numStudents = scanner.nextInt();
        double[] grades = new double[numStudents];

       
        for (int i = 0; i < numStudents; i++) {
            System.out.print("Enter grade for student " + (i + 1) + ": ");
            grades[i] = scanner.nextDouble();
        }

        double sum = 0;
        double highest = grades[0];
        double lowest = grades[0];

        for (double grade : grades) {
            sum += grade;
            if (grade > highest) {
                highest = grade;
            }
            if (grade < lowest) {
                lowest = grade;
            }
        }

        double average = sum / numStudents;
        System.out.println("\nGrade Report:");
        System.out.println("");
        System.out.printf("Average grade: %.2f\n", average);
        System.out.printf("Highest grade: %.2f\n", highest);
        System.out.printf("Lowest grade: %.2f\n", lowest);

        scanner.close();
    }
}
