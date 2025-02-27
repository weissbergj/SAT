I implement a basic, fast, and cdcl solver. These can be run via make check-fast, for example. Compare this to make check-minisat.

The results are the following:

| **Problem**     |           **MiniSat**            |                   **fast**                   |                  **basic**                   |
|-----------------|-----------------------------------|----------------------------------------------|----------------------------------------------|
|                 | Conflicts | Decisions |  Time   | Result | Conflicts  | Decisions |  Time  | Result | Conflicts   |   Decisions   |   Time   | Result |
| **aim-50**      |    0      |    1       | 0.0012 |  SAT   |  11343     |  11352    | 0.006  |  SAT   | 80280297    | 1021582189    | 362.697 |  SAT   |
| **aim-100**     |   10      |   33       | 0.0017 | UNSAT  |    N/A     |    N/A    |  N/A   |  N/A   |    N/A      |     N/A       |   N/A    |  N/A   |
| **big.dimacs**  |  308      |   815      | 0.0071 | UNSAT  |    N/A     |    N/A    |  N/A   |  N/A   |    N/A      |     N/A       |   N/A    |  N/A   |
| **dubois22**    |    0      |    0       | 0.0012 | UNSAT  | 12582912   | 12582911  | 2.555  | UNSAT  | 4194306     | 12582911      | 14.640  | UNSAT  |
| **p10.dimacs**  | 5869722   | 7053110    | 38.5179| UNSAT  | 70872610   | 70872609  | 17.344 | UNSAT  |    N/A      |     N/A       |   N/A    |  N/A   |
| **p2.dimacs**   |    0      |    0       | 0.0009 | UNSAT  |     2      |     1     | 0.003  | UNSAT  |      1      |      1        | 0.004   | UNSAT  |
| **p5.dimacs**   |  204      |   245      | 0.0011 | UNSAT  |   375      |   374     | 0.002  | UNSAT  |     90      |    1240       | 0.002   | UNSAT  |
| **p7.dimacs**   | 12440     |  15320     | 0.0282 | UNSAT  |  32781     |  32780    | 0.008  | UNSAT  | 127340      | 71168128      | 46.436  | UNSAT  |
| **p8.dimacs**   | 75864     |  92767     | 0.2211 | UNSAT  | 378344     | 378343    | 0.082  | UNSAT  |    N/A      |     N/A       |   N/A    |  N/A   |
| **sat.dimacs**  |    0      |    1       | 0.0009 |  SAT   |     0      |     2     | 0.003  |  SAT   |      0      |      2        | 0.004   |  SAT   |
| **test.dimacs** |    0      |    1       | 0.0007 |  SAT   |     0      |     2     | 0.002  |  SAT   |      0      |      2        | 0.002   |  SAT   |
| **uf250-01.cnf**|    0      |    0       | 0.0010 | UNSAT  |    N/A     |    N/A    |  N/A   |  N/A   |    N/A      |     N/A       |   N/A    |  N/A   |
| **uf250-0100.cnf**| 0       |    0       | 0.0010 | UNSAT  |    N/A     |    N/A    |  N/A   |  N/A   |    N/A      |     N/A       |   N/A    |  N/A   |

