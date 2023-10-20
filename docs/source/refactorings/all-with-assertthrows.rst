.. _All with assertthrows:
 Replace the try/catch block and the @Test expected and @Rule annotations with the assertThrows method
===========================================

**Definition:**

Developers should use the language constructs to handle exceptions.
In practice, we identified developers using the *assertThrows* method for refactoring the *try/catch* block, the *@Test expected* and *@Rule* annotations.

**Example from practice #1:**

The following code snippet shows the replacement of *try/catch* block within the `testBadConfiguration <https://github.com/apache/camel/commit/c30deabcaed4726bce4371d76257db63f2eba87c>`_
test method of the `Camel <https://github.com/apache/camel>`_ project with the *assertThrows* method. More specifically, the refactoring consists of the:

#. removal of the *try/catch* block (lines 109 - 114, highlighted in red),
#. addition of the parameters  in the *assertThrows* method (lines 113 - 114, highlighted in green):

    #. the *ResolveEndpointFailedException* exception class found in the *catch* statement,
    #. the call for the *sendBody* production method raising the exception, and
    #. the optional message which explains the assertion.


.. image:: /pdfs/Listing6.png
   :alt: Replacing the *try/catch* block with the *assertThrows* method
   :align: center


**Example from practice #2:**

The following code snippet shows the replacement of *@Rule* annotation in the
`UnsynchronizedBufferTest <https://github.com/apache/accumulo/commit/d4fd27f32dc2611a23f67b1d3e8dafd8ee05a1cb>`_ test class of
the `Accumulo <https://github.com/apache/accumulo>`_ project with the *assertThrows* method. The test class contains the *ExpectedException* rule, which is used by the *testByteBufferConstructor*
through the *@Rule* annotation to check whether the exception behaves as expected. The refactoring consists of the:

#. removal of the *@Rule* annotation (lines 35 and 36, highlighted in red) in the class;
#. removal of the expected exception from the method (lines 57 - 59, highlighted in red);
#. addition of the *assertThrows* method in the test method with the parameters:

    #. optional message that explains the assertion;
    #. the ArrayIndexOutOfBoundsException exception class found in the thrown.expect method;
    #. the call for the readBytes production method raising the exception (lines 54 - 58, highlighted in green).


.. image:: /pdfs/Listing7.png
   :alt: Replacing the *@Rule* annotation with the *assertThrows* method
   :align: center


**Example from practice #3:**

The following code snippet shows the replacement of *@Test expected* annotation of the
`testNonDefaultConfig <https://github.com/apache/camel/commit/626196af0baf18a859c55bdf91526b447b367faf>`_
of the `Camel <https://github.com/apache/camel>`_ project with the *assertThrows* method. The test method uses the
*@Test expected* annotation to handle the exception (line 41, highlighted in red). The refactoring consists of the:

#. Removal the *@Test expected* annotation;
#. Addition of the *assertThrows* method with the parameters:

 #. the *IllegalArgumentException* exception class found in the *@Test expected* annotation (line 46, highlighted in green),
 #. the statements raising or not the exception (44 - 51, highlighted in green).

.. image:: /pdfs/Listing8.png
   :alt: Replacing the *@Test* expected annotation with the *assertThrows* method
   :align: center