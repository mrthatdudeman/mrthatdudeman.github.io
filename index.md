
# Software Engineering and desgin:

### Fibonacci Sequence Program with Prime number tester
```markdown
import java.util.Scanner;

public class FibonacciNums {

	public static class FiboProj {

		public static void main(String[] args) {

			// Asks users for input for number of times the sequence should run and print
			System.out.println("Enter a positive whole number and your numbers Fibonacci sequence will be shown:");

			// Creates scanner
			Scanner scanner = new Scanner(System.in);

			// Declares int numOfTimes (user will determine the number of times the sequence
			// will run)
			int numOfTimes = 0;

			// Do while loop with nested if else statement will get user input of positive
			// whole number
			do {

				// If the next input into scanner is in fact an int it will be stored into int
				// variable numOfTimes eles user will get a message to try again
				if (scanner.hasNextInt()) {
					numOfTimes = scanner.nextInt();
				} else {
					System.out.println("Positive whole numbers only ... Try again: ");
					scanner.nextLine();
				}
			} while (numOfTimes <= 0);

			// Ends scanner
			scanner.close();

			// Prints explanation of what will be displayed to the user
			System.out.print("This is the Fibonacci Sequence for " + numOfTimes + " numbers: ");

			// Declares and initializes int varable i
			int i = 1;

			// Declares and initializes int variables first, second and sumOfTwoNums
			int first = 0;
			int second = 1;
			int sumOfTwoNums = 0;

			// While loop that will run as long as int i is less than or equal to the user
			// input (numOfTimes)
			while (i <= numOfTimes) {
				// Prints the first number of the sequence and a space
				System.out.print(first + " ");

				// Declares and initialize int variable sumOfTwoNums to the sum of the first and
				// second numbers
				sumOfTwoNums = first + second;

				// Stores the value in the second varaible into the first variable
				first = second;

				// Stores the value in sumOfTwoNums varable into the second variable
				second = sumOfTwoNums;

				// increments i by 1.
				i++;
			}

///	### Prime Number Program

			// Declares and initializes int variable j to equal 2
			int j = 2;

			// creates boolean isPrime to start as true
			boolean isPrime = true;

			// while loop runs as long as int j is less than or equal to the numOfTimes
			// divided by 2
			while (j <= numOfTimes / 2) {
				// if statement checks if the mod of numOfTimes and j is 0
				if (numOfTimes % j == 0) {
					isPrime = false;
					break;
				}
				// increments j after if statement is broke to stop while loop
				j++;
			}

			// If isPrime is true than first message will be displayed telling the user that
			// it
			// was a prime number, If isPrime is false than second message will be displayed
			// telling
			// the user that it was not a prime number.
			if (isPrime)

				System.out.println("\nIt looks like " + numOfTimes + " is a Prime Number");

			else

				System.out.println("\nIt looks like " + numOfTimes + " is NOT a Prime Number");
		}
	}
}

```

# Algorithms and Data Structure:

### Notable Algorithms:
// This is the body of the Fibonacci Sequence, the description is in the comments.
```markdown 
	// While loop that will run as long as int i is less than or equal to the user
	// input (numOfTimes)
	
	while (i <= numOfTimes) {
		// Prints the first number of the sequence and a space
		System.out.print(first + " ");

		// Declares and initialize int variable sumOfTwoNums to the sum of the first and
		// second numbers
		sumOfTwoNums = first + second;

		// Stores the value in the second varaible into the first variable
		first = second;

		// Stores the value in sumOfTwoNums varable into the second variable
		second = sumOfTwoNums;

		// increments i by 1.
		i++;
	}
```

This algorithm only allows for positive whole numbers to be used in the Fibonacci sequence program by using a if-else statement nested in a do while loop.
```markdown

// Do while loop with nested if else statement will get user input of positive
	// whole number
	do {
		// If the next input into scanner is in fact an int it will be stored into int
		// variable numOfTimes eles user will get a message to try again
		if (scanner.hasNextInt()) {
			numOfTimes = scanner.nextInt();
		} else {
			System.out.println("Positive whole numbers only ... Try again: ");
			scanner.nextLine();
		}
	} while (numOfTimes <= 0);

	// Ends scanner
	scanner.close();
```
This algorithm determines if the number is a prime number or note by using a boolean.
```markdown
// Declares and initializes int variable j to equal 2
	int j = 2;

	// creates boolean isPrime to start as true
	boolean isPrime = true;

	// while loop runs as long as int j is less than or equal to the numOfTimes
	// divided by 2
	while (j <= numOfTimes / 2) {
		// if statement checks if the mod of numOfTimes and j is 0
		if (numOfTimes % j == 0) {
			isPrime = false;
			break;
		}
		// increments j after if statement is broke to stop while loop
		j++;
	}

```
# Database:
### Tweets about airline Database

After creating the Database "TwitterData" in a MySQL terminal I created a table for the tweets called "Tweets".

That table includes the following columns:

airline_sentiment - gives feedback on the airline (neutral, positive, negative)
negativereason - if negatvie airline_sentiment, the reason will be given
airline	- the name of the airline that was flown
name - the name of the user that tweeted
retweet_count - the amount of retweets the tweet received
text - the actual tweet itself, (including mentions @ )
tweet_created - data and time of when the tweet was created
tweet_location - the gernal location the tweet was created and posted
user_timezone - the timezone where ther user is located



