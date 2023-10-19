Welcome to Factor-T Catalog: The Open Catalog of Test Refactorings 
===================================

The catalog outlines the reengineering process for conducting test-specific refactorings to remove test smells. Initially, the catalog unifies information on test smells and test refactorings manually classified from 375 test files from Apache Foundation. 

This manual is licensed under the `Creative Commons Attribution-NonCommercial-ShareAlike License <https://creativecommons.org/licenses/by-nc-sa/1.0/>`_.


Catalog of Test Refactoring
------------------------------

Test smell X description
Link to ref1 Link to ref2

   
Test Smells 
------------------------------

Learn about test smells.

* :doc:`Assertion Roulette </smells/assertion-roulette>`
* :doc:`Bad Naming </smells/bad-naming>`
* :doc:`Inappropriate Assertion </smells/inappropriate-assertion>`
* :doc:`Handling Exception </smells/handling-exception>`
* :doc:`Ignored Test </smells/ignored-test>`
* :doc:`Redundant Print </smells/redundant-print>`
* :doc:`Empty Test </smells/empty-test>`
* :doc:`Unknown Test </smells/unknown-test>`
* :doc:`Sleep Test </smells/sleep-test>`


.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: Test Smells
   
   /smells/assertion-roulette
   /smells/bad-naming
   /smells/inappropriate-assertion
   /smells/handling-exception
   /smells/ignored-test
   /smells/redundant-print
   /smells/empty-test
   /smells/unknown-test
   /smells/sleep-test


Test Refactorings
------------------------------

Learn about test refactorings.

* :doc:`Renaming the test class </refactorings/rename-class>`
* :doc:`Replace try/catch block with @Test expected annotation </refactorings/try-with-test-annotation>`
* :doc:`Replace try/catch block, @Test expected or @Rule annotations with the assertThrows </refactorings/all-with-assertthrows>`
* :doc:`Replace the not operator within the assertions </refactorings/replace-not-operator>`
* :doc:`Split conditional expressions into two different parameters </refactorings/split-conditional>`
* :doc:`Replace reserved words with an appropriate assertion </refactorings/replace-reserved-words>`
* :doc:`Add an explanation message to the assertion </refactorings/add-message>`
* :doc:`Split assertions into single test methods </refactorings/split-assertions>`
* :doc:`Surround assertions with assertAll </refactorings/surround-assertall>`

.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: Test Refactorings

   /refactorings/rename-class
   /refactorings/try-with-test-annotation
   /refactorings/all-with-assertthrows
   /refactorings/replace-not-operator
   /refactorings/split-conditional
   /refactorings/replace-reserved-words
   /refactorings/add-message
   /refactorings/split-assertions
   /refactorings/surround-assertall


About us
------------------------------

Learn about the ARIES Lab organization to find out how you can get involved and contribute to the development and success of FactorT and many others!

* :doc:`Contributing </contribute>`
* :doc:`Our Team </team>`


.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: About us

   /contribute
   /team
