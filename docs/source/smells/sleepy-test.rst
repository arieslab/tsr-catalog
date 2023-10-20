Sleepy Test
=====================

**Definition:**

It occurs when a test method needs to pause its execution for a certain duration and then
continue its execution.

**Consequences:**

It can lead to unexpected results depending on the testing environments.

**Detection:**

#. *Identifying Thread.sleep method.* The detection consists of identifying test methods
that call the *Thread.sleep* to force the test code to wait for some result and then
proceed with its execution.

**Refactorings:**

* Code addition