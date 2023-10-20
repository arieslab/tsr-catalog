Bad naming
=====================

**Definition:**

It occurs when test suites written with JUnit framework does not follow the naming
conventions as pre-pending or appending the word *Test* to the name of the production class
under test in the same package hierarchy.


**Consequences:**

The absence of consistent naming conventions makes it challenging for developers
to identify the test cases of a production class, leading to a difficulty in understanding the purpose
and scope of different test suites.

**Detection:**

#. Identify test classes’ names without the word *Test* in it.

**Refactorings:**

* :ref:`Rename class:`
