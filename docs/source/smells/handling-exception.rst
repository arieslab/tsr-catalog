
Handling Exception
=====================

**Definition:**

It occurs when developers do not use language constructs to handle exceptions, which may vary from JUnit versions.
For example, JUnit4 provides the *@Rule* and *@Test expected* annotations, while JUnit5 provides the *assertThrows* method
to verify the exception raised by a method.

**Consequences:**

This can lead to inconsistent test results and obscure the actual behavior of the code under test,
making it difficult to identify and resolve potential issues.

**Detection:**

#. *Identify try/catch blocks.* `Peruma et al. (2019) <https://dl.acm.org/doi/10.5555/3370272.3370293>`_ state that
the *Exception Handling* test smell occurs when a test method contains either a throw statement or catch statement.
#. *Identify @Rule annotation.* The *@Rule* annotation checks whether a test method throws an exception through the
*ExpectedException* rule. That annotation does not require the developer to customize the exception handling or throw an
exception to pass or fail the test.


**Refactorings:**

* :ref:`Try with test annotation`
* :ref:`Replace the try/catch, @Test expected and @Rule annotations with the assertThrows method`
