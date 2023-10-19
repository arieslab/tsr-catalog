
.. _Try with test annotation:
Replace try/catch block with @Test expected annotation
===========================================

**Definition.** `Meszaros et al. (2001) <http://xunitpatterns.com/>`_ and `Peruma et al. (2019) <https://dl.acm.org/doi/10.5555/3370272.3370293>`_ suggest using JUnit features instead of the try/catch blocks. JUnit4 provides the expected attribute of the @Test expected annotation and the Rule check to handle exceptions. According to `Peruma et al. (2019) <https://dl.acm.org/doi/10.5555/3370272.3370293>`_, developers should split the test method into multiple test methods to verify different error scenarios. Besides, test methods that generate exceptions should contain the @Test expected annotation to fail when the exception occurs.

**Example from practice.** We did not find developers performing this refactoring in practice. Instead, developers also perceive the refactoring suggested by `Peruma et al. (2019) <https://dl.acm.org/doi/10.5555/3370272.3370293>`_ as an improvement.
