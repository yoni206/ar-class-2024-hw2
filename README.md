# HW 2
The tasks for this HW are found in hw2.pdf.

## Details about Question 1
### How to implement?
The SAT-solvers should be implemented in `sat_solver.py`.
In particular, the naive solver should be implemented in the function
`naive_solve` and the dpll solver should be implemented in the function
`dpll_solve`. 
Currently `sat_solver.py` only contains dummy implementations (e.g., functions that always return True).

### How to run?
This is how your implementation should be called:
```
python3 sat_solver.py <path-to-cnf> <algorithm>
```
where:
- `<path-to-cnf>` is a path to a cnf file
- `<algorithm>` is either "naive" or "dpll"

For example:
```
python3 sat_solver.py benchmarks/example1.cnf naive
python3 sat_solver.py benchmarks/example1.cnf dpll
```
In both cases, the result should be `sat`. 
No other output is allowed, as the implementation will be tested using scripts.

Remarks:

- The directory `benchmarks` includes several cnf files as examples.
- Your implementation will be tested on a super-set of these benchmarks.
- You are free to implement everything within sat_solver.py or use other files and import them. In the latter case, make sure to include them in your submission. The test script will always call `sat_solver.py`.
- It is highly recommended to compare your results to an off-the-shelf SAT solver,
such as `minisat` in order to check that your results are correct.
When testing your implementation, we plan to compare your results to `minisat`'s results.
- `minisat`'s output format is a bit different -- still, your programs must output either `sat` or `unsat` (lower case) -- nothing more, nothing less.
