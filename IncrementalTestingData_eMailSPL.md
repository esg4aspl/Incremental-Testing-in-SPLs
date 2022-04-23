# Incremental Testing Data for eMail SPL - Experiments and Results
The Email Product Line has 24 product configurations and 52 one-increment, i.e., one feature addition, testing scenarios in total. In our study, we select 30 of the testing scenarios randomly. In the selection process of the one increment scenarios, the following two rules are applied:
1.	The same scenario has not been selected more than once.	
2.	The same PUC has not been selected more than twice.

The IDs and the features of the products which are used as a PUC or an EP can be found [here](https://github.com/esg4aspl/SPL-FESG-Examples/blob/master/Email/Products.pdf).

## Testing Scenarios
In this table, the selected testing scenarios are given with their Scenario IDs, Product Under Consideration(PUC) IDs, Existing Product IDs and Features and Increment. Existing Product refers to the product that we already have the model and the test sequences. In incremental test generation approach, the existing product's test sequences and increment's test sequences are composed so that the test sequences of the PUC is obtained without generating and composing all of its features from scratch. 

| Scenario ID | Product Under Consideration ID | Existing Product ID | Existing Product Features           | Increment     |
| ----------- | ------------------------------ | ------------------- | ----------------------------------- | ------------- |
| 1           | 2                              | 0                   | \-                                  | autoresponder |
| 2           | 4                              | 0                   | \-                                  | forward       |
| 3           | 8                              | 0                   | \-                                  | encrypt       |
| 4           | 12                             | 0                   | \-                                  | sign          |
| 5           | 3                              | 1                   | addressbook                         | autoresponder |
| 6           | 5                              | 1                   | addressbook                         | forward       |
| 7           | 9                              | 1                   | addressbook                         | encrypt       |
| 8           | 13                             | 1                   | addressbook                         | sign          |
| 9           | 3                              | 2                   | autoresponder                       | addressbook   |
| 14          | 11                             | 3                   | addressbook, autoresponder          | encrypt       |
| 18          | 16                             | 4                   | forward                             | sign          |
| 19          | 7                              | 5                   | addressbook, forward                | autoresponder |
| 21          | 7                              | 6                   | autoresponder, forward              | addressbook   |
| 23          | 19                             | 7                   | addressbook, autoresponder, forward | sign          |
| 26          | 20                             | 8                   | encrypt                             | sign          |
| 27          | 11                             | 9                   | addressbook, encrypt                | autoresponder |
| 28          | 21                             | 9                   | addressbook, encrypt                | sign          |
| 30          | 22                             | 10                  | autoresponder, encrypt              | sign          |
| 31          | 23                             | 11                  | addressbook, autoresponder, encrypt | sign          |
| 33          | 14                             | 12                  | sign                                | autoresponder |
| 34          | 16                             | 12                  | sign                                | forward       |
| 35          | 20                             | 12                  | sign                                | encrypt       |
| 36          | 15                             | 13                  | addressbook, sign                   | autoresponder |
| 39          | 15                             | 14                  | autoresponder, sign                 | addressbook   |
| 40          | 18                             | 14                  | autoresponder, sign                 | forward       |
| 45          | 18                             | 16                  | forward, sign                       | autoresponder |
| 47          | 19                             | 18                  | autoresponder, forward, sign        | addressbook   |
| 48          | 21                             | 20                  | encrypt, sign                       | addressbook   |
| 49          | 22                             | 20                  | encrypt, sign                       | autoresponder |
| 51          | 23                             | 22                  | autoresponder, encrypt, sign        | addressbook   |

## Data on Number of Faults
The table below contains the total number of possible faults and the number of faults seeded for various m values for each PUC. The entire number of possible faults for each PUC for a given value of m is directly proportional to the number of m-sequences in the PUC's ESG, and the total number of seeded faults is 20% of the summation of number of possible faults for m=2,3.

| Scenario ID | PUC ID | m=2 | m=3 | Total Number of Seeded Faults | Number of Seeded Faults |
| ----------- | ------ | --- | --- | ----------------------------- | ----------------------- |
| 1           | 2      | 24  | 50  | 74                            | 103                     |
| 2           | 4      | 23  | 50  | 73                            | 102                     |
| 3           | 8      | 25  | 55  | 80                            | 119                     |
| 4           | 12     | 23  | 53  | 76                            | 117                     |
| 5           | 3      | 32  | 60  | 92                            | 122                     |
| 6           | 5      | 31  | 60  | 91                            | 121                     |
| 7           | 9      | 33  | 65  | 98                            | 138                     |
| 8           | 13     | 31  | 63  | 94                            | 136                     |
| 9           | 3      | 32  | 60  | 92                            | 122                     |
| 14          | 11     | 37  | 69  | 106                           | 141                     |
| 18          | 16     | 26  | 57  | 83                            | 119                     |
| 19          | 7      | 35  | 64  | 99                            | 124                     |
| 21          | 7      | 35  | 64  | 99                            | 124                     |
| 23          | 19     | 38  | 71  | 109                           | 141                     |
| 26          | 20     | 28  | 62  | 90                            | 136                     |
| 27          | 11     | 37  | 69  | 106                           | 141                     |
| 28          | 21     | 36  | 72  | 108                           | 155                     |
| 30          | 22     | 32  | 66  | 98                            | 140                     |
| 31          | 23     | 40  | 76  | 116                           | 158                     |
| 33          | 14     | 27  | 57  | 84                            | 120                     |
| 34          | 16     | 26  | 57  | 83                            | 119                     |
| 35          | 20     | 28  | 62  | 90                            | 136                     |
| 36          | 15     | 35  | 67  | 102                           | 139                     |
| 39          | 15     | 35  | 67  | 102                           | 139                     |
| 40          | 18     | 30  | 61  | 91                            | 123                     |
| 45          | 18     | 30  | 61  | 91                            | 123                     |
| 47          | 19     | 38  | 71  | 109                           | 141                     |
| 48          | 21     | 36  | 72  | 108                           | 155                     |
| 49          | 22     | 32  | 66  | 98                            | 140                     |
| 51          | 23     | 40  | 76  | 116                           | 158                     |


# Data on Test Generation and Execution
Table below presents data on fault coverage and performance statistics on test set generation and test execution processes.

| Scenario ID | PUC ID | Approach | Length of EP Test Set | Length of PUC Test Set | Events Reused | Generation Time (ms) | Faults Seeded | Events Executed | Faults Revealed |
| ----------- | ------ | -------- | --------------------- | ---------------------- | ------------- | -------------------- | ------------- | --------------- | --------------- |
| 1           | 2      | inc      | 20                    | 25                     | 20            | 1.50                 | 103           | 192             | 47              |
| 1           | 2      | sm       | \-                    | 25                     | \-            | 52.64                | 103           | 190             | 47              |
| 2           | 4      | inc      | 20                    | 24                     | 29            | 1.58                 | 102           | 182             | 45              |
| 2           | 4      | sm       | \-                    | 24                     | \-            | 54.07                | 102           | 180             | 45              |
| 3           | 8      | inc      | 20                    | 27                     | 25            | 1.95                 | 119           | 215             | 45              |
| 3           | 8      | sm       | \-                    | 22                     | \-            | 53.00                | 119           | 220             | 46              |
| 4           | 12     | inc      | 20                    | 26                     | 20            | 2.20                 | 117           | 220             | 46              |
| 4           | 12     | sm       | \-                    | 21                     | \-            | 52.80                | 117           | 222             | 46              |
| 5           | 3      | inc      | 29                    | 34                     | 29            | 1.23                 | 122           | 216             | 51              |
| 5           | 3      | sm       | \-                    | 29                     | \-            | 52.83                | 122           | 209             | 51              |
| 6           | 5      | inc      | 29                    | 33                     | 31            | 0.76                 | 121           | 244             | 55              |
| 6           | 5      | sm       | \-                    | 28                     | \-            | 56.40                | 121           | 232             | 54              |
| 7           | 9      | inc      | 29                    | 36                     | 27            | 0.83                 | 138           | 313             | 66              |
| 7           | 9      | sm       | \-                    | 26                     | \-            | 51.34                | 138           | 315             | 64              |
| 8           | 13     | inc      | 29                    | 35                     | 20            | 0.76                 | 136           | 286             | 62              |
| 8           | 13     | sm       | \-                    | 25                     | \-            | 51.92                | 136           | 241             | 55              |
| 9           | 3      | inc      | 25                    | 34                     | 29            | 2.71                 | 122           | 216             | 51              |
| 9           | 3      | sm       | \-                    | 29                     | \-            | 52.83                | 122           | 209             | 51              |
| 14          | 11     | inc      | 34                    | 41                     | 34            | 0.88                 | 141           | 296             | 69              |
| 14          | 11     | sm       | \-                    | 31                     | \-            | 52.08                | 141           | 298             | 68              |
| 18          | 16     | inc      | 22                    | 28                     | 36            | 0.92                 | 119           | 205             | 46              |
| 18          | 16     | sm       | \-                    | 25                     | \-            | 57.14                | 119           | 179             | 42              |
| 19          | 7      | inc      | 31                    | 36                     | 20            | 1.20                 | 124           | 213             | 53              |
| 19          | 7      | sm       | \-                    | 33                     | \-            | 55.59                | 124           | 210             | 53              |
| 21          | 7      | inc      | 27                    | 36                     | 29            | 1.07                 | 124           | 213             | 53              |
| 21          | 7      | sm       | \-                    | 33                     | \-            | 55.59                | 124           | 210             | 53              |
| 23          | 19     | inc      | 36                    | 42                     | 26            | 0.81                 | 141           | 304             | 73              |
| 23          | 19     | sm       | \-                    | 34                     | \-            | 54.10                | 141           | 273             | 68              |
| 26          | 20     | inc      | 27                    | 33                     | 35            | 0.84                 | 136           | 304             | 61              |
| 26          | 20     | sm       | \-                    | 23                     | \-            | 54.89                | 136           | 263             | 54              |
| 27          | 11     | inc      | 36                    | 41                     | 31            | 1.19                 | 141           | 296             | 69              |
| 27          | 11     | sm       | \-                    | 31                     | \-            | 52.08                | 141           | 298             | 68              |
| 28          | 21     | inc      | 36                    | 42                     | 22            | 0.75                 | 155           | 336             | 71              |
| 28          | 21     | sm       | \-                    | 30                     | \-            | 55.76                | 155           | 288             | 67              |
| 30          | 22     | inc      | 32                    | 38                     | 26            | 0.89                 | 140           | 262             | 54              |
| 30          | 22     | sm       | \-                    | 28                     | \-            | 55.45                | 140           | 271             | 56              |
| 31          | 23     | inc      | 41                    | 47                     | 31            | 0.77                 | 158           | 317             | 69              |
| 31          | 23     | sm       | \-                    | 35                     | \-            | 58.58                | 158           | 271             | 64              |
| 33          | 14     | inc      | 26                    | 31                     | 28            | 1.27                 | 120           | 203             | 47              |
| 33          | 14     | sm       | \-                    | 26                     | \-            | 63.33                | 120           | 241             | 54              |
| 34          | 16     | inc      | 26                    | 30                     | 36            | 0.82                 | 119           | 207             | 46              |
| 34          | 16     | sm       | \-                    | 25                     | \-            | 57.14                | 119           | 179             | 42              |
| 35          | 20     | inc      | 26                    | 33                     | 33            | 0.96                 | 136           | 304             | 61              |
| 35          | 20     | sm       | \-                    | 23                     | \-            | 54.89                | 136           | 263             | 54              |
| 36          | 15     | inc      | 35                    | 40                     | 27            | 0.98                 | 139           | 275             | 61              |
| 36          | 15     | sm       | \-                    | 30                     | \-            | 54.21                | 139           | 266             | 62              |
| 39          | 15     | inc      | 31                    | 40                     | 26            | 1.20                 | 139           | 275             | 61              |
| 39          | 15     | sm       | \-                    | 30                     | \-            | 54.21                | 139           | 266             | 62              |
| 40          | 18     | inc      | 31                    | 35                     | 36            | 1.00                 | 123           | 227             | 54              |
| 40          | 18     | sm       | \-                    | 30                     | \-            | 55.34                | 123           | 226             | 54              |
| 45          | 18     | inc      | 28                    | 33                     | 33            | 1.23                 | 123           | 225             | 54              |
| 45          | 18     | sm       | \-                    | 30                     | \-            | 55.34                | 123           | 226             | 54              |
| 47          | 19     | inc      | 33                    | 42                     | 32            | 1.13                 | 141           | 304             | 73              |
| 47          | 19     | sm       | \-                    | 34                     | \-            | 54.10                | 141           | 273             | 68              |
| 48          | 21     | inc      | 33                    | 42                     | 33            | 1.49                 | 155           | 336             | 71              |
| 48          | 21     | sm       | \-                    | 30                     | \-            | 55.76                | 155           | 288             | 67              |
| 49          | 22     | inc      | 33                    | 38                     | 41            | 1.45                 | 140           | 262             | 54              |
| 49          | 22     | sm       | \-                    | 28                     | \-            | 55.45                | 140           | 271             | 56              |
| 51          | 23     | inc      | 38                    | 47                     | 38            | 1.36                 | 158           | 317             | 69              |
| 51          | 23     | sm       | \-                    | 35                     | \-            | 58.58                | 158           | 271             | 64              |
