Inappropriate Assertion
=====================

**Definition:**

The *Assert* class has assert methods that differ in parameters and semantics about what they assert.
For example, the *assertTrue* method receives a mandatory parameter with a condition and asserts whether the
condition is valid. Differently, the *assertEquals* method asserts whether two objects are equal through two
mandatory parameters for the expected and actual values.
However, according to `Schmetzer’s <https://exubero.com/junit/anti-patterns/>`_ online post, many developers use a single assertion
method to develop all the assertions they need, characterizing the *Inappropriate Assertion* test smell.


**Consequences:**

Misusing the Assert class can lead to decreased code readability and comprehensibility.

**Detection:**

#. *Identify the not operator within a parameter.* Identify test methods with a logical expression using the
*not (!)* operator within the assertions.
#. *Identify conditional expressions as a parameter.* Identify test methods with a logical expression using the
*.equals*, *.contains*, and comparisons with operators.
#. *Identify reserved words as parameters.* Identify methods using reserved words (*true*, *false* and *null*)
as an expected value in the assert methods.

*Refactorings:*

* :ref:`Replace not operator`
* :ref:`Split conditional`
* :ref:`Reserved words`
