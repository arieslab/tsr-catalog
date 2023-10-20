.. _Split conditional:
Split conditional expressions into two different parameters
===========================================

**Definition:**

The refactoring consists of splitting the conditional expression of the *assertTrue* or
*assertFalse* methods into two parameters for an adequate *assert* method. For example:

* Instead of calling the *.equals* within the *assertTrue*, developers should
use the *assertEquals* method,
* Instead of using operators as *==* within the *assertTrue*, developers should
use the *assertEquals* method,
* Instead of using the *.contains* within the *assertTrue*, developers should
use the *assertThat* method.


**Example from practice**

The following code snippet present the refactoring for the `testPhases
< https://github.com/apache/cxf/commit/4955ca652f16e781524612383af27c650e10cbdc>`_ test method
of the `Cxf <https://github.com/apache/cxf/>`_ project. It contains an *assertTrue* method checking whether two objects
(*cxfPhases* and *defaultPhases*) are equal (lines 171 and 175, highlighted in red).
The refactoring consists of:

#. removal of the *.equals* method within the assertTrue,
#. replace the *assertTrue* method with the *assertEquals* method,
#. pass the two objects as parameters in the *assertEquals* (lines 171 and 175, highlighted in green).

.. image:: /pdfs/Listing10.png
   :alt: Replacing the *assertTrue* method with the *assertEquals* method
   :align: center


