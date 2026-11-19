| PC | instruction | R1 | R2 | R3 | mem[20] |
| 1 | LOAD R1, #6 | 6 | ? | ? | ? |
| 2 | LOAD R2, #4 | 6 | 4 | ? | ? |
| 3 | SUB R3, R1, R2 | 6 | 4 | 2 | ? |
| 4 | ADD R3, R3, R3 | 6 | 4 | 4 | ? |
| 5 | STORE [20], R3 | 6 | 4 | 4 | 4 |

This program computes (6 - 4) * 2 and stores the final result (4) in memory address 20