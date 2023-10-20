Assertion Roulette
=====================

**Definition:**

It occurs when a test method has multiple non-documented assertions.

**Consequences:**

Multiple assertion statements in a test method without a descriptive message impact readability/understandability/maintainability
as it’s not possible to understand the reason for the failure of the test.

**Detection:**

#. *Identify undocumented assertions in a test method.* It consists of identifying test methods with more than one
assertion statement without an explanation/message (parameter in the assertion method).
  
**Example:**

The `testMirrorSourceConnectorTaskConfig <https://github.com/apache/kafka/blob/db288e4a64cf41501c445b13e778e4d225a48a14/connect/mirror/src/test/java/org/apache/kafka/connect/mirror/MirrorSourceConnectorTest.java>`_. test method from Kafka project contains an Assertion Roulette.  

.. code-block:: java
  :linenos:

  @Test
  public void testMirrorSourceConnectorTaskConfig() {

    [...]
  
    Map<String, String> t1 = output.get(0);
    assertEquals("t0-0,t0-3,t0-6,t1-1", t1.get(TASK_TOPIC_PARTITIONS));
  
    Map<String, String> t2 = output.get(1);
    assertEquals("t0-1,t0-4,t0-7,t2-0", t2.get(TASK_TOPIC_PARTITIONS));
  
    Map<String, String> t3 = output.get(2);
    assertEquals("t0-2,t0-5,t1-0,t2-1", t3.get(TASK_TOPIC_PARTITIONS));

    [...]
  
  }


**Refactorings:**

* :ref:`Add Message`
* :ref:`Split assert`
* :ref:`Surround asserttrhows`
