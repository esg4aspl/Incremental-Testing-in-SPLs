# Incremental Testing Data for eMail SPL - Experiments and Results
The Email Product Line has 24 product configurations and 52 one-increment, i.e., one feature addition, testing scenarios in total. In our study, we select 30 of the testing scenarios randomly. In the selection process of the one increment scenarios, the following two rules are applied:
1.	The same scenario has not been selected more than once.	
2.	The same PUC has not been selected more than twice.

The IDs and the features of the products which are used as a PUC or an EP can be found [here](https://github.com/esg4aspl/SPL-FESG-Examples/blob/master/Email/Products.pdf).

## Testing Scenarios
In this table, the selected testing scenarios are given with their Scenario IDs, Product Under Consideration(PUC) IDs, Existing Product IDs and Features and Increment. Existing Product refers to the product that we already have the model and the test sequences. In incremental test generation approach, the existing product's test sequences and increment's test sequences are composed so that the test sequences of the PUC is obtained without generating and composing all of its features from scratch. 

| Scenario ID                   | Product Under Consideration ID | Existing Product ID | Existing Product Features | Increment |
| 1                             | 2 | 0 | \- | autoresponder |
| 2                             | 4 | 0 | \- | forward |
| 3                             | 8 | 0 | \- | encrypt |
| 4                             | 12 | 0 | \- | sign |
| 5                             | 3 | 1 | addressbook | autoresponder |
| 6                             | 5 | 1 | addressbook | forward |
| 7                             | 9 | 1 | addressbook | encrypt |
| 8                             | 13 | 1 | addressbook | sign |
| 9                             | 3 | 2 | autoresponder | addressbook |
| 14                            | 11 | 3 | addressbook, autoresponder | encrypt |
| 18                            | 16 | 4 | forward | sign |
| 19                            | 7 | 5 | addressbook, forward | autoresponder |
| 21                            | 7 | 6 | autoresponder, forward | addressbook |
| 23                            | 19 | 7 | addressbook, autoresponder, forward | sign |
| 26                            | 20 | 8 | encrypt | sign |
| 27                            | 11 | 9 | addressbook, encrypt | autoresponder |
| 28                            | 21 | 9 | addressbook, encrypt | sign |
| 30                            | 22 | 10 | autoresponder, encrypt | sign |
| 31                            | 23 | 11 | addressbook, autoresponder, encrypt | sign |
| 33                            | 14 | 12 | sign | autoresponder |
| 34                            | 16 | 12 | sign | forward |
| 35                            | 20 | 12 | sign | encrypt |
| 36                            | 15 | 13 | addressbook, sign | autoresponder |
| 39                            | 15 | 14 | autoresponder, sign | addressbook |
| 40                            | 18 | 14 | autoresponder, sign | forward |
| 45                            | 18 | 16 | forward, sign | autoresponder |
| 47                            | 19 | 18 | autoresponder, forward, sign | addressbook |
| 48                            | 21 | 20 | encrypt, sign | addressbook |
| 49                            | 22 | 20 | encrypt, sign | autoresponder |
| 51                            | 23 | 22 | autoresponder, encrypt, sign | addressbook |

## Data on Number of Faults
The table below contains the total number of possible faults and the number of faults seeded for various m values for each PUC. The entire number of possible faults for each PUC for a given value of m is directly proportional to the number of m-sequences in the PUC's ESG, and the total number of seeded faults is 20% of the summation of number of possible faults for m=2,3.




# Data on Test Generation and Execution
Table below presents data on fault coverage and performance statistics on test set generation and test execution processes.
