# TASK2
import java.util.Scanner; 
 
public class GradeCalculator { 
    public static void main(String[] args) { 
        Scanner scanner = new Scanner(System.in); 
 
        int numSubjects = 5; 
        int totalMarks = 0; 
        double averagePercentage; 
 
        for (int i = 1; i <= numSubjects; i++) { 
            System.out.print("Enter marks for Subject " + i + " (out of 100): "); 
            int marks = scanner.nextInt(); 
            if (marks < 0 || marks > 100) { 
                System.out.println("Invalid marks! Please enter a value between 0 and 100."); 
                i--; 
            } else { 
                totalMarks += marks; 
            } 
        } 
 
        averagePercentage = (double) totalMarks / numSubjects; 
 
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
 
        System.out.println("\nTotal Marks: " + totalMarks + "/" + (numSubjects * 100)); 
        System.out.println("Average Percentage: " + averagePercentage + "%"); 
        System.out.println("Grade: " + grade); 
    } 
} 
Output 1 
Enter marks for Subject 1 (out of 100): 85 
Enter marks for Subject 2 (out of 100): 92 
Enter marks for Subject 3 (out of 100): 78 
Enter marks for Subject 4 (out of 100): 88 
Enter marks for Subject 5 (out of 100): 91 
 
Total Marks: 434/500 
Average Percentage: 86.8% 
Grade: B 
 
Output 2 
Enter marks for Subject 1 (out of 100): 110 
Invalid marks! Please enter a value between 0 and 100. 
Enter marks for Subject 1 (out of 100): 80 
Enter marks for Subject 2 (out of 100): 70 
Enter marks for Subject 3 (out of 100): 65 
Enter marks for Subject 4 (out of 100): 60 
Enter marks for Subject 5 (out of 100): 85 
Total Marks: 360/500 
Average Percentage: 72.0% 
Grade: C 
