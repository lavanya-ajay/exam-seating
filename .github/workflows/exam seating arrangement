import java.util.Scanner;

public class ExamSeatingArrangement {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter number of students: ");
        int numStudents = scanner.nextInt();

        System.out.print("Enter number of seats per row: ");
        int seatsPerRow = scanner.nextInt();

        int rows = (int) Math.ceil((double) numStudents / seatsPerRow);

        // Create seating 2D array: rows x seatsPerRow
        int[][] seating = new int[rows][seatsPerRow];

        // Assign student IDs to seats
        int studentId = 1;
        for (int r = 0; r < rows; r++) {
            for (int s = 0; s < seatsPerRow; s++) {
                if (studentId <= numStudents) {
                    seating[r][s] = studentId++;
                } else {
                    seating[r][s] = 0; // 0 means empty seat
                }
            }
        }

        // Display seating arrangement
        System.out.println("\nExam Seating Arrangement:");
        for (int r = 0; r < rows; r++) {
            System.out.print("Row " + (r + 1) + ": ");
            for (int s = 0; s < seatsPerRow; s++) {
                if (seating[r][s] == 0) {
                    System.out.print("[Empty] ");
                } else {
                    System.out.print("[Student " + seating[r][s] + "] ");
                }
            }
            System.out.println();
        }

        scanner.close();
    }
}
