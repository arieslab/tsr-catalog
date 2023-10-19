Assertion Roulette
=====================

*Definition:* Occurs when a test method has multiple non-documented assertions. 

*Consequences:* Multiple assertion statements in a test method without a descriptive message impacts readability/understandability/maintainability 
as it’s not possible to understand the reason for the failure of the test.

*Detection:* A test method contains more than one assertion statement without without an explanation/message (parameter in the assertion method).
  
*Example:*
