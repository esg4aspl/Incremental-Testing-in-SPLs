

# Bank Account Product Line Experiments and Results
The Bank Account Product Line has forty two(42) product configurations and ninty seven(97) one-increment i.e., one feature addition, testing scenarios in total. In this study, we select 30 of the testing scenarios out of 97 scenarios randomly. In the selection process of the one increment scenarios, the following two rules are applied:
1. The same scenario has not been selected more than once.
2. The same PUC has not been selected more than twice.

The product information can be found [on](https://github.com/esg4aspl/SPL-FESG-Examples/blob/master/BankAccount/Products.pdf).

## Testing Scenarios
In this table, the selected testing scenarios are given with their Scenario IDs, Product Under Consideration(PUC) IDs, Existing Product IDs and Features and Increment. Existing Product refers to the product that we already have the model and the test sequences. In incremental test generation approach, the existing product's test sequences and increment's test sequences are composed so that the test sequences of the PUC is obtained without generating and composing all of its features from scratch.

| Scenario ID | Product Under Consideration ID | Existing Product ID | Existing Product Features                                                                  | New Feature        |
| ----------- | ------------------------------ | ------------------- | ------------------------------------------------------------------------------------------ | ------------------ |
| 4           | 2                              | 1                   | deposit, withdraw, interest                                                                | interestEstimation |
| 5           | 4                              | 1                   | deposit, withdraw, interest                                                                | cancelDeposit      |
| 2           | 6                              | 0                   | deposit, withdraw                                                                          | cancelWithdraw     |
| 19          | 7                              | 6                   | deposit, withdraw, cancelWithdraw                                                          | interest           |
| 23          | 8                              | 7                   | deposit, withdraw, interest, cancelWithdraw                                                | interestEstimation |
| 20          | 9                              | 6                   | deposit, withdraw, cancelWithdraw                                                          | dailyLimit         |
| 41          | 13                             | 12                  | deposit, withdraw, cancelDeposit, cancelWithdraw                                           | interest           |
| 17          | 14                             | 5                   | deposit, withdraw, cancelDeposit, interest, interestEstimation                             | cancelWithdraw     |
| 31          | 15                             | 9                   | deposit, withdraw, cancelWithdraw, dailyLimit                                              | cancelDeposit      |
| 49          | 16                             | 15                  | deposit, withdraw, cancelDeposit, cancelWithdraw, dailyLimit                               | interest           |
| 52          | 17                             | 16                  | deposit, withdraw, cancelDeposit, interest, cancelWithdraw, dailyLimit                     | interestEstimation |
| 36          | 19                             | 10                  | deposit, withdraw, interest, cancelWithdraw, dailyLimit                                    | overdraft          |
| 39          | 20                             | 11                  | deposit, withdraw, interest, cancelWithdraw, dailyLimit, interestEstimation                | overdraft          |
| 50          | 21                             | 15                  | deposit, withdraw, cancelDeposit, cancelWithdraw, dailyLimit                               | overdraft          |
| 62          | 22                             | 21                  | deposit, withdraw, cancelDeposit, cancelWithdraw, dailyLimit, overdraft                    | interest           |
| 55          | 23                             | 17                  | deposit, withdraw, cancelDeposit, interest, cancelWithdraw, dailyLimit, interestEstimation | overdraft          |
| 3           | 24                             | 0                   | deposit, withdraw                                                                          | credit             |
| 64          | 25                             | 24                  | deposit, withdraw, credit                                                                  | interest           |
| 67          | 26                             | 25                  | deposit, withdraw, credit, interest                                                        | interestEstimation |
| 68          | 28                             | 25                  | deposit, withdraw, credit, interest                                                        | cancelDeposit      |
| 66          | 30                             | 24                  | deposit, withdraw, credit                                                                  | cancelWithdraw     |
| 71          | 32                             | 26                  | deposit, withdraw, credit, interest, interestEstimation                                    | cancelWithdraw     |
| 78          | 33                             | 30                  | deposit, withdraw, credit, cancelWithdraw                                                  | dailyLimit         |
| 85          | 34                             | 33                  | deposit, withdraw, credit, cancelWithdraw, dailyLimit                                      | interest           |
| 83          | 35                             | 32                  | deposit, withdraw, credit, interest, cancelWithdraw, interestEstimation                    | dailyLimit         |
| 43          | 36                             | 12                  | deposit, withdraw, cancelDeposit, cancelWithdraw                                           | credit             |
| 76          | 38                             | 29                  | deposit, withdraw, cancelDeposit, credit, interest, interestEstimation                     | cancelWithdraw     |
| 86          | 39                             | 33                  | deposit, withdraw, credit, cancelWithdraw, dailyLimit                                      | cancelDeposit      |
| 54          | 40                             | 16                  | deposit, withdraw, cancelDeposit, interest, cancelWithdraw, dailyLimit                     | credit             |
| 89          | 41                             | 35                  | deposit, withdraw, credit, interest, cancelWithdraw, dailyLimit, interestEstimation        | cancelDeposit      |

[Click for the PDF version of the table](https://github.com/esg4aspl/SPL-FESG-Examples/blob/master/BankAccount/Testing%20Scenarios.pdf)



## Data on Number of Faults
The table below contains the total number of possible faults and the number of faults seeded for various m values for each PUC. The entire number of possible faults for each PUC for a given value of m is directly proportional to the number of m-sequences in the PUC's ESG, and the total number of seeded faults is 20% of the summation of number of possible faults for m=2,3.

| Scenario ID | PUC ID | m=2 | m=3 | Total Number of Possible Faults | Number of Seeded Faults |
| ----------- | ------ | --- | --- | ------------------------------- | ----------------------- |
| 2           | 6      | 17  | 20  | 37                              | 18                      |
| 3           | 24     | 20  | 20  | 40                              | 18                      |
| 4           | 2      | 24  | 24  | 48                              | 20                      |
| 5           | 4      | 22  | 22  | 44                              | 20                      |
| 17          | 14     | 28  | 28  | 56                              | 24                      |
| 19          | 7      | 22  | 22  | 44                              | 20                      |
| 20          | 9      | 23  | 30  | 53                              | 29                      |
| 23          | 8      | 26  | 26  | 52                              | 22                      |
| 31          | 15     | 25  | 32  | 57                              | 31                      |
| 36          | 19     | 33  | 38  | 71                              | 36                      |
| 39          | 20     | 37  | 42  | 79                              | 38                      |
| 41          | 13     | 24  | 24  | 48                              | 22                      |
| 43          | 36     | 24  | 24  | 48                              | 22                      |
| 49          | 16     | 30  | 34  | 64                              | 33                      |
| 50          | 21     | 30  | 38  | 68                              | 37                      |
| 52          | 17     | 34  | 38  | 72                              | 35                      |
| 54          | 40     | 35  | 36  | 71                              | 34                      |
| 55          | 23     | 39  | 44  | 83                              | 41                      |
| 62          | 22     | 35  | 40  | 75                              | 38                      |
| 64          | 25     | 25  | 22  | 47                              | 19                      |
| 66          | 30     | 22  | 22  | 44                              | 20                      |
| 67          | 26     | 29  | 26  | 55                              | 21                      |
| 68          | 28     | 27  | 24  | 51                              | 21                      |
| 71          | 32     | 31  | 28  | 59                              | 24                      |
| 76          | 38     | 33  | 30  | 63                              | 26                      |
| 78          | 33     | 28  | 32  | 60                              | 31                      |
| 83          | 35     | 37  | 38  | 75                              | 34                      |
| 85          | 34     | 33  | 34  | 67                              | 32                      |
| 86          | 39     | 30  | 34  | 64                              | 33                      |
| 89          | 41     | 39  | 40  | 79                              | 37                      |

[Click for the PDF version of the table](https://github.com/esg4aspl/SPL-FESG-Examples/blob/master/BankAccount/Data%20on%20Number%20of%20Faults.pdf)

## Data on Test Generation and Execution
Table below presents data on fault coverage and performance statistics on test set generation and test execution processes.

| Scenario ID | PUC ID | Approach | Length of EP Test Set | Length of PUC Test Set | Events Reused | Generation Time (ms) | Faults Seeded | Events Executed | Faults Revealed |
| ----------- | ------ | -------- | --------------------- | ---------------------- | ------------- | -------------------- | ------------- | --------------- | --------------- |
| 2           | 6      | inc      | 15                    | 17                     | 15            | 0.8                  | 18            | 67              | 13              |
| 2           | 6      | sm       | \-                    | 17                     | \-            | 64.11                | 18            | 67              | 13              |
| 3           | 24     | inc      | 15                    | 19                     | 15            | 1.45                 | 18            | 56              | 13              |
| 3           | 24     | sm       | \-                    | 19                     | \-            | 63.01                | 18            | 56              | 13              |
| 4           | 2      | inc      | 19                    | 23                     | 19            | 0.83                 | 20            | 78              | 16              |
| 4           | 2      | sm       | \-                    | 23                     | \-            | 75.56                | 20            | 78              | 16              |
| 5           | 4      | inc      | 19                    | 21                     | 19            | 0.99                 | 20            | 68              | 13              |
| 5           | 4      | sm       | \-                    | 21                     | \-            | 52.38                | 20            | 84              | 13              |
| 17          | 14     | inc      | 23                    | 25                     | 23            | 0.82                 | 24            | 68              | 16              |
| 17          | 14     | sm       | \-                    | 27                     | \-            | 55.26                | 24            | 128             | 20              |
| 19          | 7      | inc      | 17                    | 21                     | 17            | 1.2                  | 20            | 75              | 14              |
| 19          | 7      | sm       | \-                    | 21                     | \-            | 56.06                | 20            | 75              | 14              |
| 20          | 9      | inc      | 17                    | 28                     | 17            | 2.43                 | 29            | 110             | 24              |
| 20          | 9      | sm       | \-                    | 28                     | \-            | 51.31                | 29            | 118             | 24              |
| 23          | 8      | inc      | 21                    | 25                     | 21            | 0.94                 | 22            | 77              | 16              |
| 23          | 8      | sm       | \-                    | 25                     | \-            | 71.48                | 22            | 83              | 17              |
| 31          | 15     | inc      | 28                    | 30                     | 28            | 0.82                 | 31            | 128             | 23              |
| 31          | 15     | sm       | \-                    | 30                     | \-            | 52.44                | 31            | 147             | 21              |
| 36          | 19     | inc      | 32                    | 43                     | 32            | 1.7                  | 36            | 115             | 23              |
| 36          | 19     | sm       | \-                    | 43                     | \-            | 58.12                | 36            | 131             | 23              |
| 39          | 20     | inc      | 34                    | 45                     | 34            | 1.44                 | 38            | 155             | 30              |
| 39          | 20     | sm       | \-                    | 47                     | \-            | 63.00                | 38            | 157             | 30              |
| 41          | 13     | inc      | 19                    | 23                     | 19            | 1.32                 | 22            | 71              | 14              |
| 41          | 13     | sm       | \-                    | 23                     | \-            | 55.55                | 22            | 81              | 15              |
| 43          | 36     | inc      | 19                    | 23                     | 19            | 1.21                 | 22            | 71              | 14              |
| 43          | 36     | sm       | \-                    | 23                     | \-            | 55.55                | 22            | 81              | 15              |
| 49          | 16     | inc      | 30                    | 34                     | 30            | 1.14                 | 33            | 124             | 23              |
| 49          | 16     | sm       | \-                    | 34                     | \-            | 55.94                | 33            | 128             | 22              |
| 50          | 21     | inc      | 30                    | 41                     | 30            | 1.28                 | 37            | 129             | 25              |
| 50          | 21     | sm       | \-                    | 41                     | \-            | 58.36                | 37            | 159             | 24              |
| 52          | 17     | inc      | 34                    | 38                     | 34            | 0.90                 | 35            | 107             | 21              |
| 52          | 17     | sm       | \-                    | 38                     | \-            | 60.69                | 35            | 147             | 24              |
| 54          | 40     | inc      | 34                    | 38                     | 34            | 1.16                 | 34            | 121             | 23              |
| 54          | 40     | sm       | \-                    | 38                     | \-            | 56.74                | 34            | 115             | 21              |
| 55          | 23     | inc      | 36                    | 47                     | 36            | 1.69                 | 41            | 159             | 31              |
| 55          | 23     | sm       | \-                    | 49                     | \-            | 56.49                | 41            | 157             | 26              |
| 62          | 22     | inc      | 38                    | 42                     | 38            | 1.43                 | 38            | 123             | 25              |
| 62          | 22     | sm       | \-                    | 45                     | \-            | 57.95                | 38            | 137             | 24              |
| 64          | 25     | inc      | 19                    | 23                     | 19            | 1.07                 | 19            | 69              | 13              |
| 64          | 25     | sm       | \-                    | 23                     | \-            | 56.71                | 19            | 69              | 13              |
| 66          | 30     | inc      | 19                    | 21                     | 19            | 0.71                 | 20            | 75              | 14              |
| 66          | 30     | sm       | \-                    | 21                     | \-            | 61.37                | 20            | 75              | 14              |
| 67          | 26     | inc      | 23                    | 27                     | 23            | 1.11                 | 21            | 84              | 17              |
| 67          | 26     | sm       | \-                    | 27                     | \-            | 59.68                | 21            | 84              | 17              |
| 68          | 28     | inc      | 23                    | 25                     | 23            | 0.73                 | 21            | 70              | 15              |
| 68          | 28     | sm       | \-                    | 25                     | \-            | 62.82                | 21            | 110             | 16              |
| 71          | 32     | inc      | 25                    | 27                     | 25            | 0.98                 | 24            | 81              | 16              |
| 71          | 32     | sm       | \-                    | 29                     | \-            | 55.46                | 24            | 83              | 16              |
| 76          | 38     | inc      | 27                    | 29                     | 27            | 0.55                 | 26            | 77              | 18              |
| 76          | 38     | sm       | \-                    | 31                     | \-            | 56.57                | 26            | 93              | 19              |
| 78          | 33     | inc      | 21                    | 32                     | 21            | 2..55                | 31            | 112             | 24              |
| 78          | 33     | sm       | \-                    | 32                     | \-            | 57.63                | 31            | 116             | 24              |
| 83          | 35     | inc      | 27                    | 38                     | 27            | 3.01                 | 34            | 127             | 23              |
| 83          | 35     | sm       | \-                    | 40                     | \-            | 63.54                | 34            | 156             | 25              |
| 85          | 34     | inc      | 32                    | 36                     | 32            | 1.03                 | 32            | 117             | 25              |
| 85          | 34     | sm       | \-                    | 36                     | \-            | 58.66                | 32            | 141             | 25              |
| 86          | 39     | inc      | 32                    | 34                     | 32            | 0.86                 | 33            | 124             | 23              |
| 86          | 39     | sm       | \-                    | 34                     | \-            | 57.47                | 33            | 128             | 22              |
| 89          | 41     | inc      | 38                    | 40                     | 38            | 0.66                 | 37            | 110             | 22              |
| 89          | 41     | sm       | \-                    | 42                     | \-            | 61.66                | 37            | 139             | 23              |                            | 66.14           | 37            | 275             | 32              |

[Click for the PDF version of the table](https://github.com/esg4aspl/SPL-FESG-Examples/blob/master/BankAccount/Data%20on%20TestGeneration%26Execution.pdf)
