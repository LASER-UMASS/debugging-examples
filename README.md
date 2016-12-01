#Debugging examples
This repository contains three buggy program versions (bug1, bug2, bug3), taken
from the Apache commons-lang project. Each buggy program version contains one
reproducible bug.

Testing
-------
For any buggy program version, run `ant test` in the top-level program directory
(i.e., bug1, bug2, or bug3) to run all test cases and reproduce the bug; run
`ant test.pass` to only run the passing test cases `ant test.fail` to only run
the failing test cases.

Coverage
--------
For any buggy program version, run `ant coverage` in the top-level program
directory (i.e., bug1, bug2, or bug3) to compute the coverage results for the
passing and failing test cases. After completion, you can view the detailed html
coverage reports:
- coverage_results_pass/index.html
- coverage_results_fail/index.html

Fault localization
------------------
The top-level program directory of each buggy program version (i.e., bug1, bug2,
or bug3) provides a suspiciousness ranking (*tarantula.susp*) for each statement
in each bug-related class. A class is related to the bug if it is touched by the
triggering test.
