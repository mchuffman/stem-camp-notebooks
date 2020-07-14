# Probability and Statistics, lecture 2
This is for after doing the other prob/stat notebook which covered things like **mean**, **variance**, and **standard deviation**, and **probability** and **independence/correlation/causation**.

## Random Variable
Let's think of rolling dice.  We could say that the **random variable** is the "roll of a dice". The random variable can take on certain **outcomes**, like 1, 2, 3, 4, 5 or 6.  We often use capital letters, like *X*, to represent a random variable, and lower case letters, like *x*, to represent possible outcomes.

When then write statements like *P(X=x)* to denote the probability that the random variable *X* take son value *x*.  Sometimes we just write *P(X)* or *p(x)*.

So if *X* is the roll of a dice, then we can say *P(X=1) = P(X=2) = ... = P(X=6) = 1/6*.

## Expected value
Suppose I offer you $10 if a coin lands on Heads, but you have to pay me $10 if the con lands on Tails. Is this a good bet?  It's a neutral bet: neither good nor bad. We can quantify this by saying the expected outcome is zero.  What we do is look at how much you win or lose in each scenario, weighted by how likely that scenario is.

So now suppose I offer you $60 if you roll a 1 with a dice, but if you roll a 2, 3, 4, 5 or 6, then you have to pay me $10.  Is this a good deal for you?  Let's compute the expected value of your winnings.  You have +60\*1/6 -10\*1/6 - 10\*1/6 - 10\*1/6- 10\*1/6 - 10\*1/6 = 1/6\*( 60 - 5\*10 ) = 10/6. So you expect to make a little under $2 profit. That means if you took this bet millions of times, on average, you'd be profiting $2 per time.  Expected values are very much like averages; in fact, they are averages (or **means**), but we only say **expected value** when we are talking about a random variable, and **not** for a set of outcomes. If you just have a list of data, you do not talk about its expected value, though you can talk about its mean (or sometimes called **sample mean**).

## Joint probability
Now let *X* be the first roll of the dice, and *Y* be the second roll. Because the first roll doesn't affect the second roll (and vice-versa), we say these are **independent** random variables.

Joint probability is *P(X,Y)*, and to be specific, we can ask questions like what is *P(X=2,Y=3)*.  What is *P(X=2,Y=3)*? You might guess 1/36, and that's right. In fact, *P(X=2,Y=3) = P(X=2)P(Y=3)* because they are independent.

We can also ask questions like what is *P(Y=3)*, which means we don't care about *X*. Intuitively, *P(Y=3) = 1/6* (which is correct).  If both *X* and *Y* are random variables, then we say *P(X,Y)* is the **joint** probability distribution, and *P(Y)* is a **marginal** probability distribution.

## Conditional Probability
To make things more clear, let's think of a scenario where the random variables are **dependent**. Let's play the following game: *X* is the roll of the first dice, as before, but now *Y* is either 0, if *X* was a 1, or else the roll of a second die if *X* wasn't a 1.

So, now we can ask a question like *P(Y=3)*.  Is this still 1/6 like it was before?  No. To find out what it is, we need conditional probability.

Since *P(Y=3)* doesn't care about the value of *X*, we can figure out what this is by looking at all possible scenarios. Then, we weigh each scenario by how plausible it is.  Each possible value of *X* is a scenario. We write such a scenario as *P(Y=3 | X=x)* where *x* is the outcome.

So, this means *P(Y=3) = P(Y=3|X=1)P(X=1) + P(Y=3|X=2)P(X=2) + P(Y=3|X=3)P(X=3) + P(Y=3|X=4)P(X=4) + P(Y=3|X=5)P(X=5) + P(Y=3|X=6)P(X=6)*.  Now we can start calculating.  All of the *P(X=x)* terms have the value 1/6. Furthermore, *P(Y=3|X=1) = 0* because of how we defined the rules of the game.

*P(Y=3|X=2)* is 1/6, as is *P(Y=3|X=3)* and the others.  Thus our calculation gives
*P(Y=3) = 1/6( 5/6) = 5/36* which is a bit under *1/6*.

## Conditional probability as a table

|      | Y=1  | Y=2 | Y=3 | Y=4 | Y=5 | Y=6 | |
| --- | --- | --- | --- | --- | --- | --- |--- |
| **X=1**  |
| **X=2**  | P(X=2,Y=1)
| **X=3**  |
| **X=4**  |
| **X=5**  |
| **X=6**  |
|   | P(Y=1)  |

You can fill in entries of the main 6x6 part of the table, and use these to compute marginals and conditional probabilities.

## Bayes rule
This is discussed in the other PDF. After you've seen that, come back here. Recall Bayes' rule is
*P(Y|X) = P(X|Y)P(Y)/P(X)* (of course, it is symmetric with *X* and *Y*, so feel free to swap *X* and *Y* if you want).

Let's revisit the cancer example. The facts we are assuming: among women over age 40, 1% have cancer (note: we are making this number up).  90% of women with cancer will test positive on a screening test. 8% of women without cancer will also test positive ("false positives").  If you are a woman over age 40 and have a positive result from the test, does this mean there is a 90% chance you have cancer?

Let's suppose we have 10,000 women over age 40. We expect about 100 (1%) of them to have cancer. We can use that to fill in the following chart (which will list expected outcomes):

|   | positive result  | negative result   |  (combined) |
| --- | --- | --- | --- |
| **have cancer**  |   |   | 100  |
| **no cancer**  |   |   | 9,900  |
| **(combined)**  |   |   | 10,000  |

Now, fill in the rest of the table. When you're done, check that you get something like this:






|   | positive result  | negative result   |  (combined) |
| --- | --- | --- | --- |
| **have cancer**  | 90  | 10  | 100  |
| **no cancer**  | 792  | 9,108  | 9,900  |
| **(combined)**  | 882  | 9,118  | 10,000  |

So if you have a positive result, you are in the group of 882 people.  In this group, we expect about 90 to have cancer, and 792 not to have cancer. So your odds of having cancer are 90/882 = 10.2%.  So much lower than 90%!
