Unknown Test
=====================

**Definition:**

It occurs when a test method has an executable body but no
assertions.

**Consequences:**

JUnit shows the test method as passing if the statements within
the test method did not result in a thrown exception when executed.

**Detection:**

#. *Identifying methods with executable body but no assertions.* The detection consists of
identifying test methods that do not assert any condition while meeting the criteria:

#. contain an executable body,
#. do not throw an exception,
#. do not contain the tags *@Ignored* or  *@Disabled*,
#. do not call the *System.out.print* method

**Refactorings:**

* Code addition