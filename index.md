## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/mrthatdudeman/mrthatdudeman.github.io/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown 

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/mrthatdudeman/mrthatdudeman.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.



# Software Engineering and desgin:

### Fibonacci Sequence Program
```markdown
import java.util.Scanner;
public class JavaExample 
{

    public static void main(String[] args)
    {
        // Declares int numOfTimes (user will determine the number of times the sequence will run)
        int numOfTimes;
        
        // Declares and initializes int variables first and second respectively
        int first = 0;
        int second = 1;
        
        // Asks users for input for number of times the sequence should run and print
        System.out.println("Enter the amount of numbers you would like to see in the Fibonacci sequence:");
        
        // Creates scanner
        Scanner scanner = new Scanner(System.in);
        
        // Initializes next user input as int numOfTimes
        numOfTimes = scanner.nextInt();
       
        // Ends scanner
        scanner.close();
        
        // Prints explanation of what will be displayed to the user
        System.out.print("This is the Fibonacci Sequence for " +numOfTimes+ " numbers: ");

        // Declares and initializes int varable i
        int i = 1;
        
        // While loop that will run as long as int i is less than or equal to the user input (numOfTimes)
        while(i <= numOfTimes)
        {
            // Prints the first number of the sequence and a space
            System.out.print(first + " ");
            
            // Declares and initialize int variable sumOfTwoNums to the sum of the first and second numbers
            int sumOfTwoNums = first + second;
          
            // Stores the value in the second varaible into the first variable
            first = second;
            
            // Stores the value in sumOfTwoNums varable into the second variable
            second = sumOfTwoNums;
            
            // increments i by 1.
            i++;
        }
    }
}
```
### Prime Number Program
```markdown
// Declares and initializes int variable n to equal the last number in the seqeunce
int n = sumOfTwoNums;

// This boolean will check if the int n is prime (true or false)
boolean isPrime(int n) 
{
    // initializes conditions for the for loop
    for(int i = 2; i < n; i++) 
    {
     
     // If-statement will keep checking to see if there is a remander for n that is 0
        if(n % i == 0)
            return false;
    }
    return true;
}
```

# Algorithms and Data Structure:

### Notable Algorithms:
// This is the body of the Fibonacci Sequence, the description is in the comments.

With comments:
```markdown 
  // While loop that will run as long as int i is less than or equal to the user input (numOfTimes)
        while(i <= numOfTimes)
        {
            // Prints the first number of the sequence and a space
            System.out.print(first + " ");
            
            // Declares and initialize int variable sumOfTwoNums to the sum of the first and second numbers
            int sumOfTwoNums = first + second;
          
            // Stores the value in the second varaible into the first variable
            first = second;
            
            // Stores the value in sumOfTwoNums varable into the second variable
            second = sumOfTwoNums;
            
            // increments i by 1.
            i++;
        }
```

Without comments:
```markdown 

        while(i <= numOfTimes)
        {
            System.out.print(first + " ");
            int sumOfTwoNums = first + second;
            first = second;
            second = sumOfTwoNums;
            i++;
        }
```


# Database:
Still in progress..
