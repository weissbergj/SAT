I implement a basic, fast, and cdcl solver. These can be run via make check-fast, for example. Compare this to make check-minisat.

The results are the following:
<div style="overflow-x: auto;">

| **Problem**       | **Exp.** |            **MiniSat**           |               **fast**               |              **basic**              |                **cdcl**                |
|-------------------|:--------:|----------------------------------|--------------------------------------|--------------------------------------|-----------------------------------------|
|                   |          | Conf.  | Dec.      | Time      | Res.   | Conf.     | Dec.     | Time    | Res.   | Conf.     | Dec.        | Time     | Res.   | Conf. | Dec. | Learn | Time   | Res.   |
| **aim-50**        | SAT      | 0      | 1         | 0.0012    | SAT    | 11343     | 11352    | 0.006   | SAT    | 80280297  | 1021582189  | 362.697 | SAT    | N/A   | N/A | N/A   | N/A   | N/A    |
| **aim-100**       | UNSAT    | 10     | 33        | 0.0017    | UNSAT  | N/A       | N/A      | N/A     | N/A    | N/A       | N/A         | N/A     | N/A    | 1     | 33  | 1     | 0.002 | UNSAT |
| **big.dimacs**    | UNSAT    | 308    | 815       | 0.0071    | UNSAT  | N/A       | N/A      | N/A     | N/A    | N/A       | N/A         | N/A     | N/A    | 1     | 29  | 1     | 0.003 | UNSAT |
| **dubois22**      | UNSAT    | 0      | 0         | 0.0012    | UNSAT  | 12582912  | 12582911 | 2.555   | UNSAT  | 4194306   | 12582911    | 14.640  | UNSAT  | 1     | 24  | 1     | 0.002 | UNSAT |
| **p10.dimacs**    | UNSAT    | 5869722| 7053110   | 38.5179   | UNSAT  | 70872610  | 70872609 | 17.344  | UNSAT  | N/A       | N/A         | N/A     | N/A    | 1     | 20  | 1     | 0.002 | UNSAT |
| **p2.dimacs**     | UNSAT    | 0      | 0         | 0.000942  | UNSAT  | 2         | 1        | 0.003   | UNSAT  | 1         | 1           | 0.004   | UNSAT  | 2     | 1   | 1     | 0.002 | UNSAT |
| **p5.dimacs**     | UNSAT    | 204    | 245       | 0.001135  | UNSAT  | 375       | 374      | 0.002   | UNSAT  | 90        | 1240        | 0.002   | UNSAT  | 1     | 8   | 1     | 0.001 | UNSAT |
| **p7.dimacs**     | UNSAT    | 12440  | 15320     | 0.028152  | UNSAT  | 32781     | 32780    | 0.008   | UNSAT  | 127340    | 71168128    | 46.436  | UNSAT  | 1     | 13  | 1     | 0.002 | UNSAT |
| **p8.dimacs**     | UNSAT    | 75864  | 92767     | 0.221122  | UNSAT  | 378344    | 378343   | 0.082   | UNSAT  | N/A       | N/A         | N/A     | N/A    | 1     | 16  | 1     | 0.001 | UNSAT |
| **sat.dimacs**    | SAT      | 0      | 1         | 0.000922  | SAT    | 0         | 2        | 0.003   | SAT    | 0         | 2           | 0.004   | SAT    | 0     | 2   | 0     | 0.001 | SAT   |
| **test.dimacs**   | SAT      | 0      | 1         | 0.000741  | SAT    | 0         | 2        | 0.002   | SAT    | 0         | 2           | 0.002   | SAT    | 0     | 2   | 0     | 0.001 | SAT   |
| **uf250-01.cnf**  | UNSAT    | 0      | 0         | 0.001003  | UNSAT  | N/A       | N/A      | N/A     | N/A    | N/A       | N/A         | N/A     | N/A    | 1     | 27  | 1     | 0.002 | UNSAT |
| **uf250-0100.cnf**| UNSAT    | 0      | 0         | 0.001006  | UNSAT  | N/A       | N/A      | N/A     | N/A    | N/A       | N/A         | N/A     | N/A    | 1     | 22  | 1     | 0.002 | UNSAT |

</div>
