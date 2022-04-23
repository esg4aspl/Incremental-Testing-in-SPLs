# Incremental Testing Data for Student Attendance System SPL - Experiments and Results

The Student Attendance System product line has 2664 product configurations and 10236 one-increment, i.e., one feature addition, testing scenarios in total. In our study, we select 30 of the testing scenarios randomly. In the selection process of the one increment scenarios, the following two rules are applied:
1.	The same scenario has not been selected more than once.	
2.	The same PUC has not been selected more than twice.

The IDs and the features of the products which are used as a PUC or an EP can be found [here](https://github.com/esg4aspl/SPL-FESG-Examples/blob/master/StudentAttendanceSystem/Products.pdf).

## Testing Scenarios
In this table, the selected testing scenarios are given with their Scenario IDs, Product Under Consideration(PUC) IDs, Existing Product IDs and Features and Increment. Existing Product refers to the product that we already have the model and the test sequences. In incremental test generation approach, the existing product's test sequences and increment's test sequences are composed so that the test sequences of the PUC is obtained without generating and composing all of its features from scratch. 

| Scenario ID | Product Under Consideration ID | Existing Product ID | Existing Product Features                                                                                                                                                                          | Increment               |
| ----------- | ------------------------------ | ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------- |
| 4852        | 1116                           | 1112                | viewClass, viewSchedule, email, studentAccess, teacherAccess, updateRecord, addNewClass, updateClassDetail, addNewSchedule, accessCard                                                             | viewRecord              |
| 962         | 210                            | 206                 | viewSchedule, SMS, studentAccess, teacherAccess, updateRecord, addNewClass, updateClassDetail, traceAttendanceActivity, fingerprint                                                                | viewRecord              |
| 9432        | 2413                           | 2361                | viewClass, SMS, studentAccess, teacherAccess, updateRecord, addNewClass, updateClassDetail, addNewSchedule, editSchedule, assignNewSchedule, barcode                                               | deleteClass             |
| 9436        | 2390                           | 2362                | viewClass, SMS, studentAccess, teacherAccess, updateRecord, addNewClass, updateClassDetail, addNewSchedule, editSchedule, assignNewSchedule, fingerprint                                           | traceAttendanceActivity |
| 2511        | 1493                           | 609                 | viewClass, SMS, studentAccess, teacherAccess, updateRecord, addNewSchedule, monitorAttendanceStatus, barcode                                                                                       | editSchedule            |
| 7500        | 1803                           | 1799                | viewClass, viewSchedule, email, studentAccess, teacherAccess, addNewSchedule, editSchedule, monitorAttendanceStatus, QRCode                                                                        | viewRecord              |
| 3942        | 1231                           | 919                 | viewClass, viewSchedule, email, studentAccess, teacherAccess, addNewSchedule, viewRecord, monitorAttendanceStatus, QRCode                                                                          | deleteClass             |
| 3445        | 816                            | 800                 | viewClass, email, studentAccess, teacherAccess, updateRecord, addNewClass, addNewSchedule, deleteClass, accessCard                                                                                 | monitorAttendanceStatus |
| 9379        | 2655                           | 2343                | viewClass, viewSchedule, email, studentAccess, teacherAccess, updateRecord, addNewClass, updateClassDetail, addNewSchedule, editSchedule, viewRecord, traceAttendanceActivity, deleteClass, QRCode | assignNewSchedule       |
| 4971        | 2027                           | 1143                | viewClass, viewSchedule, email, studentAccess, teacherAccess, updateRecord, addNewClass, updateClassDetail, addNewSchedule, traceAttendanceActivity, QRCode                                        | editSchedule            |
| 7119        | 2211                           | 1691                | viewClass, email, studentAccess, teacherAccess, updateRecord, addNewClass, addNewSchedule, editSchedule, viewRecord, deleteClass, QRCode                                                           | viewSchedule            |
| 6051        | 2307                           | 1423                | viewClass, viewSchedule, email, teacherAccess, updateRecord, addNewClass, updateClassDetail, addNewSchedule, deleteClass, QRCode                                                                   | editSchedule            |
| 8577        | 2079                           | 2127                | viewSchedule, email, teacherAccess, updateRecord, addNewSchedule, editSchedule, traceAttendanceActivity, deleteClass, QRCode                                                                       | studentAccess           |
| 4365        | 1107                           | 1003                | viewClass, viewSchedule, email, studentAccess, teacherAccess, addNewClass, addNewSchedule, viewRecord, QRCode                                                                                      | updateClassDetail       |
| 2217        | 1412                           | 528                 | viewSchedule, email, studentAccess, teacherAccess, updateRecord, addNewClass, updateClassDetail, viewRecord, monitorAttendanceStatus, traceAttendanceActivity, deleteClass, accessCard             | addNewSchedule          |
| 3493        | 813                            | 809                 | viewClass, SMS, studentAccess, teacherAccess, addNewClass, addNewSchedule, monitorAttendanceStatus, deleteClass, barcode                                                                           | viewRecord              |
| 1341        | 352                            | 300                 | viewSchedule, email, studentAccess, teacherAccess, updateRecord, viewRecord, monitorAttendanceStatus, deleteClass, accessCard                                                                      | viewClass               |
| 5914        | 1432                           | 1380                | viewSchedule, email, studentAccess, teacherAccess, addNewClass, updateClassDetail, addNewSchedule, monitorAttendanceStatus, deleteClass, accessCard                                                | viewClass               |
| 6361        | 1562                           | 1510                | viewClass, SMS, studentAccess, teacherAccess, updateRecord, addNewSchedule, editSchedule, viewRecord, traceAttendanceActivity, fingerprint                                                         | addNewClass             |
| 45          | 123                            | 11                  | viewClass, viewSchedule, email, teacherAccess, updateRecord, QRCode                                                                                                                                | addNewClass             |
| 6050        | 1451                           | 1423                | viewClass, viewSchedule, email, teacherAccess, updateRecord, addNewClass, updateClassDetail, addNewSchedule, deleteClass, QRCode                                                                   | traceAttendanceActivity |
| 5283        | 1234                           | 1218                | viewClass, viewSchedule, SMS, studentAccess, teacherAccess, updateRecord, addNewSchedule, deleteClass, fingerprint                                                                                 | monitorAttendanceStatus |
| 7349        | 2328                           | 1756                | viewClass, email, studentAccess, teacherAccess, updateRecord, addNewClass, updateClassDetail, addNewSchedule, editSchedule, viewRecord, monitorAttendanceStatus, deleteClass, accessCard           | viewSchedule            |
| 1706        | 444                            | 392                 | viewSchedule, email, studentAccess, teacherAccess, addNewClass, monitorAttendanceStatus, deleteClass, accessCard                                                                                   | viewClass               |
| 5615        | 2183                           | 1299                | viewSchedule, email, studentAccess, teacherAccess, updateRecord, addNewClass, addNewSchedule, traceAttendanceActivity, deleteClass, QRCode                                                         | editSchedule            |
| 1658        | 487                            | 383                 | viewSchedule, email, teacherAccess, updateRecord, addNewClass, deleteClass, QRCode                                                                                                                 | updateClassDetail       |
| 8178        | 2279                           | 1967                | viewSchedule, email, studentAccess, teacherAccess, updateRecord, addNewClass, updateClassDetail, addNewSchedule, editSchedule, viewRecord, monitorAttendanceStatus, QRCode                         | deleteClass             |
| 3225        | 1634                           | 750                 | viewClass, SMS, studentAccess, teacherAccess, updateRecord, addNewSchedule, deleteClass, fingerprint                                                                                               | editSchedule            |
| 5188        | 1246                           | 1194                | viewSchedule, SMS, studentAccess, teacherAccess, updateRecord, addNewSchedule, traceAttendanceActivity, deleteClass, fingerprint                                                                   | viewClass               |
| 573         | 1005                           | 121                 | viewClass, viewSchedule, SMS, teacherAccess, updateRecord, addNewClass, barcode                                                                                                                    | addNewSchedule          |

[Click for the PDF version of the table - (page 3)](https://github.com/esg4aspl/Incremental-Testing-in-Software-Product-Lines/blob/main/IncrementalTestingData/TestingScenarios.pdf)

## Data on Number of Faults
The table below contains the total number of possible faults and the number of faults seeded for various m values for each PUC. The entire number of possible faults for each PUC for a given value of m is directly proportional to the number of m-sequences in the PUC's ESG, and the total number of seeded faults is 20% of the summation of number of possible faults for m=2,3.

| Scenario ID | PUC ID | m=2 | m=3 | Total Number of Possible Faults | Number of Seeded Faults |
| ----------- | ------ | --- | --- | ------------------------------- | ----------------------- |
| 45          | 123    | 52  | 72  | 124                             | 82                      |
| 573         | 1005   | 69  | 109 | 178                             | 137                     |
| 962         | 210    | 72  | 112 | 184                             | 138                     |
| 1341        | 352    | 58  | 68  | 126                             | 55                      |
| 1658        | 487    | 67  | 106 | 173                             | 134                     |
| 1706        | 444    | 58  | 83  | 141                             | 92                      |
| 2217        | 1412   | 94  | 153 | 247                             | 196                     |
| 2511        | 1493   | 72  | 115 | 187                             | 140                     |
| 3225        | 1634   | 73  | 115 | 188                             | 141                     |
| 3445        | 816    | 76  | 117 | 193                             | 143                     |
| 3493        | 813    | 75  | 117 | 192                             | 142                     |
| 3942        | 1231   | 62  | 87  | 149                             | 95                      |
| 4365        | 1107   | 78  | 136 | 214                             | 184                     |
| 4852        | 1116   | 87  | 147 | 234                             | 193                     |
| 4971        | 2027   | 97  | 175 | 272                             | 241                     |
| 5188        | 1246   | 67  | 94  | 161                             | 101                     |
| 5283        | 1234   | 67  | 94  | 161                             | 101                     |
| 5615        | 2183   | 88  | 147 | 235                             | 192                     |
| 5914        | 1432   | 83  | 143 | 226                             | 191                     |
| 6050        | 1451   | 86  | 143 | 229                             | 190                     |
| 6051        | 2307   | 96  | 171 | 267                             | 237                     |
| 6361        | 1562   | 85  | 142 | 227                             | 187                     |
| 7119        | 2211   | 94  | 156 | 250                             | 201                     |
| 7349        | 2328   | 108 | 188 | 296                             | 251                     |
| 7500        | 1803   | 67  | 108 | 175                             | 137                     |
| 8178        | 2279   | 104 | 181 | 285                             | 244                     |
| 8577        | 2079   | 75  | 117 | 192                             | 143                     |
| 9379        | 2655   | 112 | 198 | 310                             | 272                     |
| 9432        | 2413   | 106 | 192 | 298                             | 265                     |
| 9436        | 2390   | 97  | 178 | 275                             | 253                     |

[Click for the PDF version of the table - (page 3)](https://github.com/esg4aspl/Incremental-Testing-in-Software-Product-Lines/blob/main/IncrementalTestingData/DataOnNumberOfFaults.pdf)

## Data on Test Generation and Execution
Table below presents data on fault coverage and performance statistics on test set generation and test execution processes.

| Scenario ID | PUC ID | Approach | Length of EP Test Set | Length of PUC Test Set | Events Reused | Generation Time (ms) | Faults Seeded | Events Executed | Faults Revealed |
| ----------- | ------ | -------- | --------------------- | ---------------------- | ------------- | -------------------- | ------------- | --------------- | --------------- |
| 45          | 123    | inc      | 35                    | 51                     | 35            | 1.23                 | 82            | 307             | 52              |
| 45          | 123    | sm       | \-                    | 51                     | \-            | 64.35                | 82            | 298             | 51              |
| 573         | 1005   | inc      | 58                    | 74                     | 58            | 1.26                 | 137           | 523             | 87              |
| 573         | 1005   | sm       | \-                    | 74                     | \-            | 62.79                | 137           | 544             | 90              |
| 962         | 210    | inc      | 84                    | 89                     | 84            | 0.90                 | 138           | 489             | 80              |
| 962         | 210    | sm       | \-                    | 89                     | \-            | 69.07                | 138           | 490             | 80              |
| 1341        | 352    | inc      | 64                    | 69                     | 64            | 0.85                 | 55            | 274             | 46              |
| 1341        | 352    | sm       | \-                    | 64                     | \-            | 78.28                | 55            | 263             | 44              |
| 1658        | 487    | inc      | 60                    | 76                     | 60            | 1.60                 | 134           | 518             | 84              |
| 1658        | 487    | sm       | \-                    | 76                     | \-            | 62.37                | 134           | 516             | 84              |
| 1706        | 444    | inc      | 61                    | 66                     | 61            | 0.76                 | 92            | 350             | 61              |
| 1706        | 444    | sm       | \-                    | 61                     | \-            | 64.53                | 92            | 360             | 62              |
| 2217        | 1412   | inc      | 102                   | 118                    | 102           | 1.38                 | 196           | 779             | 124             |
| 2217        | 1412   | sm       | \-                    | 118                    | \-            | 71.05                | 196           | 777             | 124             |
| 2511        | 1493   | inc      | 73                    | 89                     | 73            | 1.51                 | 140           | 515             | 86              |
| 2511        | 1493   | sm       | \-                    | 89                     | \-            | 90.68                | 140           | 513             | 86              |
| 3225        | 1634   | inc      | 71                    | 87                     | 71            | 1.30                 | 141           | 527             | 88              |
| 3225        | 1634   | sm       | \-                    | 87                     | \-            | 99.82                | 141           | 527             | 88              |
| 3445        | 816    | inc      | 87                    | 91                     | 87            | 0.83                 | 143           | 537             | 90              |
| 3445        | 816    | sm       | \-                    | 91                     | \-            | 83.51                | 143           | 541             | 90              |
| 3493        | 813    | inc      | 84                    | 89                     | 84            | 1.05                 | 142           | 509             | 92              |
| 3493        | 813    | sm       | \-                    | 89                     | \-            | 67.18                | 142           | 513             | 92              |
| 3942        | 1231   | inc      | 57                    | 66                     | 57            | 1.30                 | 95            | 363             | 61              |
| 3942        | 1231   | sm       | \-                    | 66                     | \-            | 67.52                | 95            | 389             | 64              |
| 4365        | 1107   | inc      | 69                    | 85                     | 69            | 1.29                 | 184           | 592             | 99              |
| 4365        | 1107   | sm       | \-                    | 85                     | \-            | 64.69                | 184           | 605             | 101             |
| 4852        | 1116   | inc      | 94                    | 99                     | 94            | 0.77                 | 193           | 669             | 112             |
| 4852        | 1116   | sm       | \-                    | 99                     | \-            | 76.57                | 193           | 647             | 108             |
| 4971        | 2027   | inc      | 100                   | 116                    | 100           | 1.59                 | 241           | 878             | 140             |
| 4971        | 2027   | sm       | \-                    | 116                    | \-            | 69.00                | 241           | 867             | 138             |
| 5188        | 1246   | inc      | 77                    | 82                     | 77            | 1.29                 | 101           | 371             | 62              |
| 5188        | 1246   | sm       | \-                    | 77                     | \-            | 65.63                | 101           | 368             | 61              |
| 5283        | 1234   | inc      | 71                    | 75                     | 71            | 0.70                 | 101           | 379             | 63              |
| 5283        | 1234   | sm       | \-                    | 75                     | \-            | 68.41                | 101           | 364             | 60              |
| 5615        | 2183   | inc      | 93                    | 109                    | 93            | 1.27                 | 192           | 701             | 113             |
| 5615        | 2183   | sm       | \-                    | 109                    | \-            | 69.73                | 192           | 699             | 113             |
| 5914        | 1432   | inc      | 93                    | 98                     | 93            | 1.01                 | 191           | 688             | 115             |
| 5914        | 1432   | sm       | \-                    | 93                     | \-            | 79.29                | 191           | 662             | 109             |
| 6050        | 1451   | inc      | 92                    | 98                     | 92            | 0.73                 | 190           | 688             | 106             |
| 6050        | 1451   | sm       | \-                    | 98                     | \-            | 67.68                | 190           | 678             | 105             |
| 6051        | 2307   | inc      | 92                    | 108                    | 92            | 1.01                 | 237           | 827             | 133             |
| 6051        | 2307   | sm       | \-                    | 108                    | \-            | 68.33                | 237           | 838             | 135             |
| 6361        | 1562   | inc      | 89                    | 105                    | 89            | 1.33                 | 187           | 682             | 110             |
| 6361        | 1562   | sm       | \-                    | 105                    | \-            | 77.66                | 187           | 680             | 110             |
| 7119        | 2211   | inc      | 108                   | 113                    | 108           | 0.81                 | 201           | 804             | 124             |
| 7119        | 2211   | sm       | \-                    | 108                    | \-            | 67.50                | 201           | 805             | 124             |
| 7349        | 2328   | inc      | 128                   | 133                    | 128           | 0.88                 | 251           | 943             | 154             |
| 7349        | 2328   | sm       | \-                    | 128                    | \-            | 76.54                | 251           | 920             | 149             |
| 7500        | 1803   | inc      | 68                    | 73                     | 68            | 0.87                 | 137           | 465             | 80              |
| 7500        | 1803   | sm       | \-                    | 73                     | \-            | 62.37                | 137           | 453             | 77              |
| 8178        | 2279   | inc      | 119                   | 128                    | 119           | 1.30                 | 244           | 865             | 142             |
| 8178        | 2279   | sm       | \-                    | 128                    | \-            | 86.92                | 244           | 863             | 142             |
| 8577        | 2079   | inc      | 82                    | 93                     | 82            | 1.28                 | 143           | 516             | 86              |
| 8577        | 2079   | sm       | \-                    | 93                     | \-            | 72.13                | 143           | 512             | 86              |
| 9379        | 2655   | inc      | 130                   | 150                    | 130           | 1.47                 | 272           | 1008            | 159             |
| 9379        | 2655   | sm       | \-                    | 134                    | \-            | 75.58                | 272           | 1025            | 160             |
| 9432        | 2413   | inc      | 137                   | 146                    | 137           | 1.18                 | 265           | 908             | 145             |
| 9432        | 2413   | sm       | \-                    | 130                    | \-            | 79.03                | 265           | 901             | 142             |
| 9436        | 2390   | inc      | 130                   | 136                    | 130           | 0.76                 | 253           | 878             | 135             |
| 9436        | 2390   | sm       | \-                    | 120                    | \-            | 77.79                | 253           | 888             | 135             |

[Click for the PDF version of the table - (page 3)](https://github.com/esg4aspl/Incremental-Testing-in-Software-Product-Lines/blob/main/IncrementalTestingData/DataOnTestGenerationAndExecution.pdf)
