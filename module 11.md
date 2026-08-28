

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
```
#include <stdio.h>

int max_of_four(int n1, int n2, int n3, int n4)
{
    int greater;

    if (n1 >= n2 && n1 >= n3 && n1 >= n4)
    {
        greater = n1;
    }
    else if (n2 >= n1 && n2 >= n3 && n2 >= n4)
    {
        greater = n2;
    }
    else if (n3 >= n1 && n3 >= n2 && n3 >= n4)
    {
        greater = n3;
    }
    else
    {
        greater = n4;
    }

    return greater;
}

int main()
{
    int n1, n2, n3, n4, greater;

    printf("Enter four numbers:\n");
    scanf("%d %d %d %d", &n1, &n2, &n3, &n4);

    greater = max_of_four(n1, n2, n3, n4);

    printf("Greatest number is %d", greater);

    return 0;
}
```

Output:
<img width="737" height="281" alt="image" src="https://github.com/user-attachments/assets/b81174ae-8d59-45fe-b416-6939d731601b" />


Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
```
#include <stdio.h>

void calculate_the_max(int n, int k)
{
    int a = 0, o = 0, x = 0;
    int i, j;
    int and_value, or_value, xor_value;

    for (i = 1; i <= n; i++)
    {
        for (j = i + 1; j <= n; j++)
        {
            and_value = i & j;
            or_value = i | j;
            xor_value = i ^ j;

            if (and_value < k && and_value > a)
            {
                a = and_value;
            }

            if (or_value < k && or_value > o)
            {
                o = or_value;
            }

            if (xor_value < k && xor_value > x)
            {
                x = xor_value;
            }
        }
    }

    printf("%d\n", a);
    printf("%d\n", o);
    printf("%d\n", x);
}

int main()
{
    int n, k;

    scanf("%d %d", &n, &k);

    calculate_the_max(n, k);

    return 0;
}
```

Output:
<img width="740" height="272" alt="image" src="https://github.com/user-attachments/assets/1fd3d211-8922-4358-afd5-85cb61ec30af" />


Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int noshel, noque;
    int i, type, x, y;
    int nobookarr[100];
    int shelarr[100][100];

    scanf("%d %d", &noshel, &noque);

    for (i = 0; i < noshel; i++)
    {
        nobookarr[i] = 0;
    }

    for (i = 0; i < noque; i++)
    {
        scanf("%d %d %d", &type, &x, &y);

        if (type == 1)
        {
            shelarr[x][nobookarr[x]] = y;
            nobookarr[x]++;
        }
        else if (type == 2)
        {
            printf("%d\n", shelarr[x][y]);
        }
    }

    return 0;
}
```

Output:
<img width="742" height="430" alt="image" src="https://github.com/user-attachments/assets/d0ede135-dc25-4ff8-838e-d983f2f27169" />



Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
```
#include <stdio.h>

int main()
{
    int n, i;
    int a[100];
    int sum = 0;

    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        scanf("%d", &a[i]);
        sum = sum + a[i];
    }

    printf("Sum of integers = %d", sum);

    return 0;
}
```

Output:
<img width="737" height="252" alt="image" src="https://github.com/user-attachments/assets/f54f0eb3-e274-4446-82c4-884506bf3b26" />

 


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
```
#include <stdio.h>
#include <string.h>

int main()
{
    char sentence[200];
    int i, count = 0;
    int inword = 0;

    printf("Enter a sentence: ");
    fgets(sentence, sizeof(sentence), stdin);

    for (i = 0; sentence[i] != '\0'; i++)
    {
        if (sentence[i] != ' ' && sentence[i] != '\n' && sentence[i] != '\t')
        {
            if (inword == 0)
            {
                count++;
                inword = 1;
            }
        }
        else
        {
            inword = 0;
        }
    }

    printf("Number of words = %d", count);

    return 0;
}
```

Output:
<img width="738" height="171" alt="image" src="https://github.com/user-attachments/assets/b4a88a98-5897-4a10-ba3d-8f8fdaa07478" />



Result:
Thus the code for the give program has been executed successfully.
Thus, the program that counts the number of words in a given sentence is verified 
successfully.
