Redundant Print
=====================

**Definition:**

It occurs when test methods use print statements. The
unit tests are executed as part of an automated script, making the print
statements redundant.

**Detection:**

#. *Identifying calls for the System.out.print method.* The detection
consists of identifying lines where developers call the *System.out.print*
of Java to print the test methods output instead of using assertions.

**Refactorings:**

* Code removal