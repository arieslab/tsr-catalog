.. _Add Message:
Add an explanation message to the assertion
===========================================

**Definition.** `Deursen et al. (2001) <https://dl.acm.org/doi/10.5555/869201>`_. suggested using the optional first parameter of the assert methods of JUnit4 to give an explanatory message to the user when the assertion fails. In the case of JUnit5, the explanatory message goes in the third parameter.

**Example from practice.** The following code presents the refactoring for a group of undocumented assertions (lines 170, 173, and 176 highlighted in red) in the  `testMirrorSourceConnectorTaskConfig <https://github.com/apache/kafka/blob/db288e4a64cf41501c445b13e778e4d225a48a14/connect/mirror/src/test/java/org/apache/kafka/connect/mirror/MirrorSourceConnectorTest.java>`_. test method of the Kafka project. Given that the test code is written in JUnit5, the refactoring consists of adding a third optional parameter with the explanation messages (lines 170, 173, and 176 highlighted in green).


.. image:: /pdfs/Listing10.png
   :alt: Assertion Roulette
   :align: center
