# Russian multiplications
A Python exercise: Russian multiplications program

### Credits
The following exercise was originally proposed by Dr. Christie Lee from the Robert Gordon University during the Aberdeen Python User Group MeetUp of February 2020. The Jupyter Notebook contains my solution to the problem.

  ## Russian Multiplication
  
  The problem requires you to implement an unusal multiplication algorithm for positive integers.
  
  Let's mulitply **42 × 1337**. But instead of using normal mulitplication, we will use a method which only uses halving, doubling, and addition!

First, we write the two numbers **a** and **b** in a table (which is which doesn't matter because a×b is the same as b×a, but you'll see it's faster if we put the smaller number on the left).

|  a |     b |
| -: | ----: |
| 42 |  1337 |

Now we complete the first column by halving **a** on each line. 42 halves to give 21. 21 halves to give 10 (don't worry about the fraction part). 10 halves to give 5. 5 halves to give 2 (don't worry about the fraction part). 2 halves to give 1. Now we stop at 1.

|  a |     b |
| -: | ----: |
| 42 |  1337 |
| 21 |       |
| 10 |       |
|  5 |       |
|  2 |       |
|  1 |       |

Since we kept halving **a**, we should double **b** the same number of times. Since we're doubling, no need to worry about any fractions, just double as you normally would.

|  a |     b |
| -: | ----: |
| 42 |  1337 |
| 21 |  2674 |
| 10 |  5348 |
|  5 | 10696 |
|  2 | 21392 |
|  1 | 42784 |

Next, we delete any rows where **a** is even, like the rows where **a** is 42, 10, or 2.

|  a |     b |
| -: | ----: |
| 21 |  2674 |
|  5 | 10696 |
|  1 | 42784 |

And lastly, we add up the **b** column: 2674 + 10696 + 42784 = 56154.

And if you check, magically your origonal two numbers muliutply to give the same number! 42 × 1337 = 56154

Write a Python function to do this proceedure.

Example usage:

    >>> russian_multiplication(42, 1337):
    56154

You may want to try other pairs of positive integers to make sure it works.

