
# Software Engineering and design:

### Fibonacci Sequence Program with Prime number tester
This is the entiretly of the Fibonaci Seqeunce Program. The program allows a user to imput a number and the program will output the Fibonacci Sequence. The program will also tell the user wither the inputed number is or is not a Prime Number. There are some checks in the program that only allow for the whole positive number to be used, if it is not used then the user will be asked to try again. 

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
			
// Prime Number Program

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
This is the body of the Fibonacci Sequence, the description is in the comments.
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

In the first image you can see that I created the Database "TwitterData" in a MySQL terminal, I then created a table for the tweets called "Tweets":

<img width="392" alt="Picture1" src="https://user-images.githubusercontent.com/26801971/79695846-1253eb80-8247-11ea-926f-3dff33a47b31.png">

I found some Twitter data online and downloaded the excel file. I notice that the file was extermly bulky so I decided to trim down some of the columns that were not really needed and reduced the count to 1000 entries.

Creating the columns for this database in the terminal proved challenging so I used the MySQL Workbench to create them:

<img width="223" alt="Picture4" src="https://user-images.githubusercontent.com/26801971/79696043-2d732b00-8248-11ea-99c3-5ecba810c8e4.png">

This is a discription of the table's columns: 
airline_sentiment - gives feedback on the airline (neutral, positive, negative)
negativereason - if negatvie airline_sentiment, the reason will be given
airline	- the name of the airline that was flown
name - the name of the user that tweeted
retweet_count - the amount of retweets the tweet received
text - the actual tweet itself, (including mentions @ )
tweet_created - data and time of when the tweet was created
tweet_location - the gernal location the tweet was created and posted
user_timezone - the timezone where ther user is located

Once all of the data was imported successfully, I began testing filtering the database with commands. This one shows all of the cloumn "name": 

<img width="162" alt="Picture2" src="https://user-images.githubusercontent.com/26801971/79695851-197af980-8247-11ea-9672-fb1a613d4b9d.png">

I then wanted to test the database in a little more detail so I searched only "positive" entries in the "airline_sentiment" column. This means only the positive entries will be pulled, but If i only filed by that the word "positive" will be displayed for every positive entry that is in the database. So I used it as a searching term. I displayed all of the "text" (which are the tweets) WHERE the "airline_sentiment" is "positive":

<img width="468" alt="Picture3" src="https://user-images.githubusercontent.com/26801971/79695856-20a20780-8247-11ea-9461-5b3037ce4d81.png">




# Professional Self-Assessment:


I believe some parts of this project I handled well and others I could improve on. I have always been a multitasker so when we had the option to encompass all three categories of the project into a single project I knew that is what I was going to do. I struggled for a day or two trying to think of that project. Finally, I decided it would be best to split it up  into two parts. I combined the Software Engineering and design portion of the project with the Algorithms and Data Structure portion and let the Database portion be its own project. 
I believe my program accurately demonstrates the skills of Software engineering, design, algorithms and data structures. I did this by using different kinds of loops and variable types. The algorithm took the greatest amount of time for me to accomplish. I began by creating the Fibonacci Sequence code, once that was done I was able to put the prime number code in it. I did find myself changing multiple lines out for a more diverse type of code. 
The one part of the  Database portion that was challenging for me was creating the columns for the table in the terminal. I tried multiple times but could not get the command to work. I settled and created the columns in MySQL Workbench. The import of data and testing of the database was done through the terminal. I believe that this project could be improved in the future, The Fibonacci Sequence program could include different types of sequences and number patterns, the Database could potentially have a live stream of tweets so airlines can constantly monitor their customers flight experiences. 

