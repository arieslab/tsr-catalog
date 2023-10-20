Empty Test
=====================

**Definition:**

It occurs when a test method has no executable statements.

**Consequences:**

As the test method does not assert any condition, JUnit always indicates that the test passes.

**Detection:**

#. *Identifying methods with no executable body.* The detection consists of identifying test
methods containing an empty or commented body, i.e., with no executable statements.

**Refactorings:**

* Code addition
* Code removal