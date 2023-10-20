Ignored Test
=====================

**Definition:**

It occurs when test methods are suppressed from running.

**Consequences:**

The ignored test methods result in overhead with respect to compilation time.

**Detection:**

#. *Identifying ignored methods.* The detection consists of identifying classes or methods
with the *@Disabled* annotation in JUnit5 or *@Ignored* annotation in previous versions of JUnit testing framework.

**Refactorings:**

* Code removal