# Grade-Evaluator
```

import java.util.Scanner;
public class Main {
	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		int Again = 0;
		do {
		System.out.println("=== Grade Evaluator ===");
		System.out.print("How many students? ");
		int students = input.nextInt();
		
		for (int ctr=0;ctr<students;ctr++) {
			System.out.println("\n--- Student " + (ctr + 1) + " ---");
			int sum = 0;
			for (int ctr2=0;ctr2<5;ctr2++) {
				System.out.print("Enter grade " + (ctr2+1) + ": ");
				int grade = input.nextInt();
				sum += grade;
				
			}
			
			double average = sum/5;
			System.out.println("Average: " + average);
			if (sum >= 75) {
				System.out.println("Status: Passed");
			} else {
				System.out.println("Status: Failed");
			}
			
		}
		
		while (true) {
		System.out.print("\nDo you want to enter another set of students? (Y/N): ");
		char YN = input.next().charAt(0);
		if (YN == 'Y') {
			Again = 1;
			break;
		} else if (YN == 'N') {
			Again = 0;
			System.out.println("\n- Ending Program..");
			break;
		} else {
			System.out.println("\n- Invalid option. Try Again!");
			continue;
		}
		}
		System.out.println();
	}while (Again == 1);
		input.close();
	}
}

```
