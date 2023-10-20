.. _Replace not operator:
Replace the not (!) operator within the assertions with an appropriate assertion
===========================================

**Definition:**

Instead of creating a conditional logic in the assertions using the *not (!)* operator,
developers should choose the corresponding pair of the specific assert method. In more detail,

* Developers should use *assertFalse* instead of the *not (!)* operator to negate a condition within the *assertTrue*,
* Developers should use *assertNotEquals* instead of the *not (!)* operator to negate a condition within the *assertEquals*,
* Developers should use *assertNotNull* instead of the *not (!)* operator to negate a condition within the *assertNull*.

(and vice-versa).

**Example from practice:**

The following code snippet present the refactoring for the `testGenerateClientId
<https://github.com/apache/kafka/commit/f4c2030b2006fc0c447a10f8b251579424f39f7b>`_ test method
of the `Kafka <https://github.com/apache/kafka/>`_ project. The method uses an *assertTrue* method to check whether the *ids.contains(id)*
condition is false (line 293, highlighted in red). The refactoring of the assertion consists of the:

#. removal of the *not (!)* operator within the conditional expression,
#. replace the *assertTrue* method with the *assertFalse* method (line 293, highlighted in green).
In addition, the developer could also use the *assertThat* method instead of the *.contains* method.

.. image:: /pdfs/Listing9.png
   :alt: Replacing the *assertTrue* method with the *assertFalse* method
   :align: center

