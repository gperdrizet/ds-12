## 1. Bag-of-words

To use any type of model on text we first need to represent that text as numbers. We have seen methods to do this previously, such as factorization or one-hot-encoding, but these won't work here. We may have long stings of text and texts of different lengths.

One of the simplest ways to 'vectorize' or turn text into numbers is to use word frequencies:

|text                  |
|----------------------|
|The food was good     |
|The food was awesome  |
|The food was terrible |

In this collection of documents, we have the following word counts:

```text
the: 3
food: 3
was: 3
good: 1
awesome: 1
terrible: 1
```

And those words can be used as features:

|text                  | the | food | was | good | awesome | terrible |
|----------------------|-----|------|-----|------|---------|----------|
|The food was good     | 1   | 1    | 1   | 1    | 0       | 0        |
|The food was awesome  | 1   | 1    | 1   | 0    | 1       | 0        |
|The food was terrible | 1   | 1    | 1   | 0    | 0       | 1        |

This type of analysis is known as bag-of-words because it throws all of the words together, jumbles them up and only looks at their frequencies. Think about drawing color marbles from a bag as a probability demonstration in a statistics class.

## 2. Naive bayes

The naive bayes model learns the probability of the label based on it's co-occurrence with the features in the training set. Let's add a label to our toy data:

|text                  | the | food | was | good | awesome | terrible | review sentiment |
|----------------------|-----|------|-----|------|---------|----------|------------------|
|The food was good     | 1   | 1    | 1   | 1    | 0       | 0        | positive         |
|The food was awesome  | 1   | 1    | 1   | 0    | 1       | 0        | positive         |
|The food was terrible | 1   | 1    | 1   | 0    | 0       | 1        | negative         |


The probability that a review is negative in the test set is 33% (1/3). While the probability that a review is negative given that it contains the word bad is 100% (1/1)! Obviously real data is not this simple, but this is simple explanation of how the naive bayes model can learn from data.
