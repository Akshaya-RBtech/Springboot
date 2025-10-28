public class SpringBoot {
    private static final String STUDENT_NAME = "sam";
    private static final String STUDENT_ID = "12345";
    private static final int[] MARKS = {85, 92, 78}; 
    private static final String[] SUBJECTS = {"Math", "Science", "English"};
    public static int calculateTotal(int[] marks) {
        int total = 0;
        for (int mark : marks) {
            total += mark;
        }
        return total;
    }
    public static double calculateAverage(int[] marks) {
        return (double) calculateTotal(marks) / marks.length;
    }
    public static String determineGrade(double average) {
        if (average >= 90) {
            return "A";
        } else if (average >= 80) {
            return "B";
        } else if (average >= 70) {
            return "C";
        } else if (average >= 60) {
            return "D";
        } else {
            return "F";
        }
    }
    public static void main(String[] args) {
        System.out.println("Student Details:");
        System.out.println("Name: " + STUDENT_NAME);
        System.out.println("ID: " + STUDENT_ID);
        System.out.println("\nMarks:");
        for (int i = 0; i < SUBJECTS.length; i++) {
            System.out.println(SUBJECTS[i] + ": " + MARKS[i]);
        }
        int total = calculateTotal(MARKS);
        double average = calculateAverage(MARKS);
        String grade = determineGrade(average);
        System.out.println("\nResults:");
        System.out.println("Total Marks: " + total);
        System.out.println("Average Marks: " + String.format("%.2f", average));
        System.out.println("Grade: " + grade);
    }
}
