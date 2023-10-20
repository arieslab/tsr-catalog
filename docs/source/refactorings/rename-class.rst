.. _Rename class:
Rename class
===========================================

**Definition:**

The refactoring consists of pre-pending or appending the *Test* word in the test class name.

**Example from practice:**

The following code snippet shows the rename of the test class.
The `ProducerUploadFile <https://github.com/apache/camel/commit/9dc4dc6cd2c6cee75892e9a57105d79bfdcc8f5c>`_ test class of the `Camel <https://github.com/apache/camel>`_ project.
The class does not follow the naming convention of JUnit (line 35, highlighted in red). Its
refactoring consists of renaming the class to *ProducerUploadFileTest* by appending the *Test* word in it
(line 35, highlighted in green).

.. image:: /pdfs/Listing14.png
   :alt: Renaming the test class
   :align: center