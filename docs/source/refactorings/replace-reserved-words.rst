.. _Reserved words:
Replace the reserved words with an appropriate assertion
===========================================

**Definition:**

JUnit supports specific assert methods to the reserved words. If one of the parameters in the assert method is:

* *true*, then developers should replace the assert method with *assertTrue*,
* *false*, then developers should replace the assert method with *assertFalse*,
* *null*, then developers should replace the assert method with *assertNull*.

**Example from practice:**

The following code snippet present the refactoring for the `testSoapHeader
< https://github.com/apache/cxf/commit/4955ca652f16e781524612383af27c650e10cbdc>`_ test method
of the `Cxf <https://github.com/apache/cxf/>`_ project. It uses an *assertEquals* method
with a *true* value as a parameter (line 879, highlighted in red). The refactoring consists of:

#. removal of the *.equals* method within the assertTrue,
#. replace the *assertEquals* method with the *assertTrue* method,
#. removal of the unnecessary parameter (line 879, highlighted in green).

.. image:: /pdfs/Listing11.png
   :alt: Replacing the assertEquals method with the assertTrue
   :align: center



