

# Bank Account Product Line Experiments and Results
The Bank Account Product Line has forty two(42) product configurations and ninty seven(97) one-increment i.e., one feature addition, testing scenarios in total. In our study, we select 30 of the testing scenarios randomly. In the selection process of the one increment scenarios, the following two rules are applied:
1. The same scenario has not been selected more than once.
2. The same PUC has not been selected more than twice.

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

## Data on PUCs
The numbers of k-sequences where k=1,2,3,4 are given to give a notion of the sizes of the selected PUCs in the testing scenarios.

| Product Under Consideration ID | k = 1 |  k = 2 | k = 3 | k = 4 |
| ------------------------------ | ----- | ------ | ----- | ----- |
| 6                              | 8     | 9      | 11    | 14    |
| 24                             | 10    | 10     | 10    | 12    |
| 2                              | 12    | 12     | 12    | 13    |
| 4                              | 11    | 11     | 11    | 14    |
| 14                             | 14    | 14     | 14    | 17    |
| 7                              | 11    | 11     | 11    | 14    |
| 9                              | 10    | 13     | 17    | 23    |
| 8                              | 13    | 13     | 13    | 15    |
| 15                             | 11    | 14     | 18    | 25    |
| 19                             | 15    | 18     | 20    | 27    |
| 20                             | 17    | 20     | 22    | 28    |
| 13                             | 12    | 12     | 12    | 16    |
| 36                             | 12    | 12     | 12    | 16    |
| 16                             | 14    | 16     | 18    | 25    |
| 21                             | 13    | 17     | 21    | 29    |
| 17                             | 16    | 18     | 20    | 26    |
| 40                             | 17    | 18     | 18    | 25    |
| 23                             | 18    | 21     | 23    | 30    |
| 22                             | 16    | 19     | 21    | 29    |
| 25                             | 13    | 12     | 10    | 12    |
| 30                             | 11    | 11     | 11    | 14    |
| 26                             | 15    | 14     | 12    | 13    |
| 28                             | 14    | 13     | 11    | 14    |
| 32                             | 16    | 15     | 13    | 15    |
| 38                             | 17    | 16     | 14    | 17    |
| 33                             | 13    | 15     | 17    | 23    |
| 35                             | 18    | 19     | 19    | 24    |
| 34                             | 16    | 17     | 17    | 23    |
| 39                             | 14    | 16     | 18    | 25    |
| 41                             | 19    | 20     | 20    | 26    |

[Click for the PDF version of the table](https://github.com/esg4aspl/SPL-FESG-Examples/blob/master/BankAccount/Data%20on%20PUCs.pdf)

## Data on Number of Faults
The table below contains the total number of possible faults and the number of faults seeded for various m values for each PUC. The entire number of possible faults for each PUC for a given value of m is directly proportional to the number of m-sequences in the PUC's ESG, and the total number of seeded faults is 20% of the summation of number of possible faults for m=2,3,4,5.

| Scenario ID | PUC ID | m=2 | m=3 | m=4 | m=5 | Total Number of Possible Faults | Number of Seeded Faults |
| ----------- | ------ | --- | --- | --- | --- | ------------------------------- | ----------------------- |
| 2           | 6      | 17  | 20  | 25  | 30  | 92                              | 18                      |
| 3           | 24     | 20  | 20  | 22  | 26  | 88                              | 18                      |
| 4           | 2      | 24  | 24  | 25  | 27  | 100                             | 20                      |
| 5           | 4      | 22  | 22  | 25  | 30  | 99                              | 20                      |
| 17          | 14     | 28  | 28  | 31  | 35  | 122                             | 24                      |
| 19          | 7      | 22  | 22  | 25  | 30  | 99                              | 20                      |
| 20          | 9      | 23  | 30  | 40  | 53  | 146                             | 29                      |
| 23          | 8      | 26  | 26  | 28  | 31  | 111                             | 22                      |
| 31          | 15     | 25  | 32  | 43  | 57  | 157                             | 31                      |
| 36          | 19     | 33  | 38  | 47  | 62  | 180                             | 36                      |
| 39          | 20     | 37  | 42  | 50  | 63  | 192                             | 38                      |
| 41          | 13     | 24  | 24  | 28  | 34  | 110                             | 22                      |
| 43          | 36     | 24  | 24  | 28  | 34  | 110                             | 22                      |
| 49          | 16     | 30  | 34  | 43  | 57  | 164                             | 33                      |
| 50          | 21     | 30  | 38  | 50  | 66  | 184                             | 37                      |
| 52          | 17     | 34  | 38  | 46  | 58  | 176                             | 35                      |
| 54          | 40     | 35  | 36  | 43  | 57  | 171                             | 34                      |
| 55          | 23     | 39  | 44  | 53  | 67  | 203                             | 41                      |
| 62          | 22     | 35  | 40  | 50  | 66  | 191                             | 38                      |
| 64          | 25     | 25  | 22  | 22  | 26  | 95                              | 19                      |
| 66          | 30     | 22  | 22  | 25  | 30  | 99                              | 20                      |
| 67          | 26     | 29  | 26  | 25  | 27  | 107                             | 21                      |
| 68          | 28     | 27  | 24  | 25  | 30  | 106                             | 21                      |
| 71          | 32     | 31  | 28  | 28  | 31  | 118                             | 24                      |
| 76          | 38     | 33  | 30  | 31  | 35  | 129                             | 26                      |
| 78          | 33     | 28  | 32  | 40  | 53  | 153                             | 31                      |
| 83          | 35     | 37  | 38  | 43  | 54  | 172                             | 34                      |
| 85          | 34     | 33  | 34  | 40  | 53  | 160                             | 32                      |
| 86          | 39     | 30  | 34  | 43  | 57  | 164                             | 33                      |
| 89          | 41     | 39  | 40  | 46  | 58  | 183                             | 37                      |

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

## Reuse Rates
The table below shows reuse rates of test sequences and events in the testing scenarios.

| Scenario ID | Existing Product ID | PUC ID | Test Set | Test Sequences Reused in Test Set/PUC Number of Sequences | Test Sequences Reused in Test Set/Existing Product Number of Sequences | Events Reused in Test Sequences/PUC Number of Events | Events Reused in Test Sequences/Existing Product Number of Events |
| ----------- | ------------------- | ------ | -------- | --------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------- | ----------------------------------------------------------------- |
| 2           | 0                   | 6      | inc(2)   | 75                                                        | 100                                                                    | 88.23529412                                          | 100                                                               |
| 2           | 0                   | 6      | inc(3)   | 71.42857143                                               | 100                                                                    | 71.11111111                                          | 100                                                               |
| 2           | 0                   | 6      | inc(4)   | 75                                                        | 100                                                                    | 70.90909091                                          | 100                                                               |
| 3           | 0                   | 24     | inc(2)   | 60                                                        | 100                                                                    | 78.94736842                                          | 100                                                               |
| 3           | 0                   | 24     | inc(3)   | 62.5                                                      | 100                                                                    | 74.41860465                                          | 100                                                               |
| 3           | 0                   | 24     | inc(4)   | 75                                                        | 100                                                                    | 90.69767442                                          | 100                                                               |
| 4           | 1                   | 2      | inc(2)   | 83.33333333                                               | 100                                                                    | 82.60869565                                          | 100                                                               |
| 4           | 1                   | 2      | inc(3)   | 88.88888889                                               | 100                                                                    | 90.69767442                                          | 100                                                               |
| 4           | 1                   | 2      | inc(4)   | 88.88888889                                               | 100                                                                    | 90.69767442                                          | 100                                                               |
| 5           | 1                   | 4      | inc(2)   | 83.33333333                                               | 100                                                                    | 90.47619048                                          | 100                                                               |
| 5           | 1                   | 4      | inc(3)   | 72.72727273                                               | 100                                                                    | 72.22222222                                          | 100                                                               |
| 5           | 1                   | 4      | inc(4)   | 66.66666667                                               | 100                                                                    | 60.9375                                              | 100                                                               |
| 17          | 5                   | 14     | inc(2)   | 85.71428571                                               | 100                                                                    | 92                                                   | 100                                                               |
| 17          | 5                   | 14     | inc(3)   | 83.33333333                                               | 100                                                                    | 79.03225806                                          | 100                                                               |
| 17          | 5                   | 14     | inc(4)   | 85.71428571                                               | 100                                                                    | 79.48717949                                          | 100                                                               |
| 19          | 6                   | 7      | inc(2)   | 66.66666667                                               | 100                                                                    | 80.95238095                                          | 100                                                               |
| 19          | 6                   | 7      | inc(3)   | 72.72727273                                               | 100                                                                    | 79.62962963                                          | 100                                                               |
| 19          | 6                   | 7      | inc(4)   | 83.33333333                                               | 100                                                                    | 93.33333333                                          | 100                                                               |
| 20          | 6                   | 9      | inc(2)   | 57.14285714                                               | 100                                                                    | 60.71428571                                          | 100                                                               |
| 20          | 6                   | 9      | inc(3)   | 57.14285714                                               | 100                                                                    | 53.08641975                                          | 100                                                               |
| 20          | 6                   | 9      | inc(4)   | 50                                                        | 100                                                                    | 44.44444444                                          | 100                                                               |
| 23          | 7                   | 8      | inc(2)   | 85.71428571                                               | 100                                                                    | 84                                                   | 100                                                               |
| 23          | 7                   | 8      | inc(3)   | 90.90909091                                               | 90.90909091                                                            | 105.8823529                                          | 100                                                               |
| 23          | 7                   | 8      | inc(4)   | 91.66666667                                               | 100                                                                    | 92.98245614                                          | 100                                                               |
| 31          | 9                   | 15     | inc(2)   | 87.5                                                      | 100                                                                    | 93.33333333                                          | 100                                                               |
| 31          | 9                   | 15     | inc(3)   | 81.25                                                     | 100                                                                    | 80.51948052                                          | 100                                                               |
| 31          | 9                   | 15     | inc(4)   | 85.71428571                                               | 100                                                                    | 83.48623853                                          | 100                                                               |
| 36          | 10                  | 19     | inc(2)   | 75                                                        | 100                                                                    | 74.41860465                                          | 100                                                               |
| 36          | 10                  | 19     | inc(3)   | 75                                                        | 100                                                                    | 73.33333333                                          | 100                                                               |
| 36          | 10                  | 19     | inc(4)   | 66.66666667                                               | 90                                                                     | 71.65354331                                          | 95.78947368                                                       |
| 39          | 11                  | 20     | inc(2)   | 75                                                        | 100                                                                    | 75.55555556                                          | 100                                                               |
| 39          | 11                  | 20     | inc(3)   | 80                                                        | 100                                                                    | 81.52173913                                          | 100                                                               |
| 39          | 11                  | 20     | inc(4)   | 67.85714286                                               | 90.47619048                                                            | 75.18796992                                          | 96.15384615                                                       |
| 41          | 12                  | 13     | inc(2)   | 71.42857143                                               | 100                                                                    | 82.60869565                                          | 100                                                               |
| 41          | 12                  | 13     | inc(3)   | 76.92307692                                               | 100                                                                    | 82.25806452                                          | 100                                                               |
| 41          | 12                  | 13     | inc(4)   | 86.66666667                                               | 100                                                                    | 94.59459459                                          | 100                                                               |
| 43          | 12                  | 36     | inc(2)   | 71.42857143                                               | 100                                                                    | 82.60869565                                          | 100                                                               |
| 43          | 12                  | 36     | inc(3)   | 76.92307692                                               | 100                                                                    | 82.25806452                                          | 100                                                               |
| 43          | 12                  | 36     | inc(4)   | 86.66666667                                               | 100                                                                    | 94.59459459                                          | 100                                                               |
| 49          | 15                  | 16     | inc(2)   | 80                                                        | 100                                                                    | 88.23529412                                          | 100                                                               |
| 49          | 15                  | 16     | inc(3)   | 88.88888889                                               | 100                                                                    | 95.0617284                                           | 100                                                               |
| 49          | 15                  | 16     | inc(4)   | 91.66666667                                               | 100                                                                    | 96.55172414                                          | 100                                                               |
| 50          | 15                  | 21     | inc(2)   | 72.72727273                                               | 100                                                                    | 73.17073171                                          | 100                                                               |
| 50          | 15                  | 21     | inc(3)   | 80                                                        | 100                                                                    | 81.91489362                                          | 100                                                               |
| 50          | 15                  | 21     | inc(4)   | 66.66666667                                               | 90.90909091                                                            | 68.75                                                | 98.21428571                                                       |
| 52          | 16                  | 17     | inc(2)   | 90.90909091                                               | 100                                                                    | 89.47368421                                          | 100                                                               |
| 52          | 16                  | 17     | inc(3)   | 89.47368421                                               | 100                                                                    | 87.05882353                                          | 100                                                               |
| 52          | 16                  | 17     | inc(4)   | 95.83333333                                               | 100                                                                    | 96.46017699                                          | 100                                                               |
| 54          | 16                  | 40     | inc(2)   | 83.33333333                                               | 100                                                                    | 89.47368421                                          | 100                                                               |
| 54          | 16                  | 40     | inc(3)   | 90                                                        | 100                                                                    | 95.29411765                                          | 100                                                               |
| 54          | 16                  | 40     | inc(4)   | 84.61538462                                               | 95.65217391                                                            | 89.16666667                                          | 96.3963964                                                        |
| 55          | 17                  | 23     | inc(2)   | 76.92307692                                               | 100                                                                    | 76.59574468                                          | 100                                                               |
| 55          | 17                  | 23     | inc(3)   | 81.81818182                                               | 100                                                                    | 83                                                   | 100                                                               |
| 55          | 17                  | 23     | inc(4)   | 70.96774194                                               | 95.65217391                                                            | 74.14965986                                          | 96.46017699                                                       |
| 62          | 21                  | 22     | inc(2)   | 83.33333333                                               | 100                                                                    | 90.47619048                                          | 100                                                               |
| 62          | 21                  | 22     | inc(3)   | 85.71428571                                               | 100                                                                    | 87.77777778                                          | 100                                                               |
| 62          | 21                  | 22     | inc(4)   | 88.88888889                                               | 92.30769231                                                            | 100                                                  | 99.21259843                                                       |
| 64          | 24                  | 25     | inc(2)   | 71.42857143                                               | 100                                                                    | 82.60869565                                          | 100                                                               |
| 64          | 24                  | 25     | inc(3)   | 81.81818182                                               | 100                                                                    | 92                                                   | 100                                                               |
| 64          | 24                  | 25     | inc(4)   | 81.81818182                                               | 100                                                                    | 92                                                   | 100                                                               |
| 66          | 24                  | 30     | inc(2)   | 83.33333333                                               | 100                                                                    | 90.47619048                                          | 100                                                               |
| 66          | 24                  | 30     | inc(3)   | 80                                                        | 100                                                                    | 75                                                   | 100                                                               |
| 66          | 24                  | 30     | inc(4)   | 81.81818182                                               | 100                                                                    | 74.19354839                                          | 100                                                               |
| 67          | 25                  | 26     | inc(2)   | 87.5                                                      | 100                                                                    | 85.18518519                                          | 100                                                               |
| 67          | 25                  | 26     | inc(3)   | 90.90909091                                               | 100                                                                    | 91.4893617                                           | 100                                                               |
| 67          | 25                  | 26     | inc(4)   | 90.90909091                                               | 100                                                                    | 91.4893617                                           | 100                                                               |
| 68          | 25                  | 28     | inc(2)   | 87.5                                                      | 100                                                                    | 92                                                   | 100                                                               |
| 68          | 25                  | 28     | inc(3)   | 76.92307692                                               | 100                                                                    | 74.13793103                                          | 100                                                               |
| 68          | 25                  | 28     | inc(4)   | 78.57142857                                               | 100                                                                    | 73.52941176                                          | 100                                                               |
| 71          | 26                  | 32     | inc(2)   | 87.5                                                      | 100                                                                    | 92.59259259                                          | 100                                                               |
| 71          | 26                  | 32     | inc(3)   | 91.66666667                                               | 100                                                                    | 89.65517241                                          | 100                                                               |
| 71          | 26                  | 32     | inc(4)   | 84.61538462                                               | 100                                                                    | 76.47058824                                          | 100                                                               |
| 76          | 29                  | 38     | inc(2)   | 88.88888889                                               | 100                                                                    | 93.10344828                                          | 100                                                               |
| 76          | 29                  | 38     | inc(3)   | 92.85714286                                               | 100                                                                    | 90.90909091                                          | 100                                                               |
| 76          | 29                  | 38     | inc(4)   | 81.25                                                     | 100                                                                    | 71.95121951                                          | 100                                                               |
| 78          | 30                  | 33     | inc(2)   | 66.66666667                                               | 100                                                                    | 65.625                                               | 100                                                               |
| 78          | 30                  | 33     | inc(3)   | 62.5                                                      | 100                                                                    | 55.29411765                                          | 100                                                               |
| 78          | 30                  | 33     | inc(4)   | 57.14285714                                               | 100                                                                    | 49.58677686                                          | 100                                                               |
| 83          | 32                  | 35     | inc(2)   | 72.72727273                                               | 100                                                                    | 71.05263158                                          | 100                                                               |
| 83          | 32                  | 35     | inc(3)   | 72.22222222                                               | 100                                                                    | 65.93406593                                          | 100                                                               |
| 83          | 32                  | 35     | inc(4)   | 56                                                        | 100                                                                    | 47.82608696                                          | 100                                                               |
| 85          | 33                  | 34     | inc(2)   | 81.81818182                                               | 100                                                                    | 88.88888889                                          | 100                                                               |
| 85          | 33                  | 34     | inc(3)   | 88.88888889                                               | 100                                                                    | 94.80519481                                          | 100                                                               |
| 85          | 33                  | 34     | inc(4)   | 82.60869565                                               | 90.47619048                                                            | 94.33962264                                          | 98.03921569                                                       |
| 86          | 33                  | 39     | inc(2)   | 90                                                        | 100                                                                    | 94.11764706                                          | 100                                                               |
| 86          | 33                  | 39     | inc(3)   | 83.33333333                                               | 100                                                                    | 81.48148148                                          | 100                                                               |
| 86          | 33                  | 39     | inc(4)   | 78.26086957                                               | 90                                                                     | 80.53097345                                          | 95.78947368                                                       |
| 89          | 35                  | 41     | inc(2)   | 91.66666667                                               | 100                                                                    | 95                                                   | 100                                                               |
| 89          | 35                  | 41     | inc(3)   | 89.47368421                                               | 100                                                                    | 90                                                   | 100                                                               |
| 89          | 35                  | 41     | inc(4)   | 73.07692308                                               | 86.36363636                                                            | 77.77777778                                          | 97.02970297                                                       |

[Click for the PDF version of the table](https://github.com/esg4aspl/SPL-FESG-Examples/blob/master/BankAccount/ReuseRates.pdf)
