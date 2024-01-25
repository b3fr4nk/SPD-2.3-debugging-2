# Debug Log

**Explain how you used the the techniques covered (Trace Forward, Trace Backward, Divide & Conquer) to uncover the bugs in each exercise. Be specific!**

In your explanations, you may want to answer:

- What is the expected vs. actual output?
- If there is a stack trace, what useful information does it contain?
- Which technique did you use, on which line numbers?
- What assumptions did you have about each line of code, and which ones were proven to be wrong?

_Example: I noticed that the program should show pizza orders once a new order is made, and that it wasn't showing any. So, I used the trace forward technique starting on line 13. I discovered the bug on line 27 was caused by a typo of 'pzza' instead of 'pizza'._

_Then I noticed another bug ..._

## Exercise 1

[[Your answer goes here!]]

## Exercise 2

Expected: display the weather in given location using given units
Actual: Internal server error

I used work backwards from line 53

Assumption: results_json is holding the correct data
Result of experiment: it is not the geolocation is not working

Assumption: the user's city is being received and stored correctly
Result of experiment: None type is received as the user's city

Assumption: the param city_name is correct
Result of experiment: actual city name is stored in 'city' param but still get the nothing to geocode message after the fix

I used work forward from line 42

Assumption: 'place' param in API call is correct
Result of experiment: it is not parameter should be 'q' new internal server error after fix

Assumption: the temperature key is incorrect
Result of the experiment: temperature key is incorrect removing it allows the rest of the page to load

Fix: temperature key in json is 'temp'

NEW BUG: selected unit is not being used

Assumption: 'requested_units' is the correct param name
Result of the experiment: it is actually 'units'

Fix: change 'requested_units' to 'units'

## Exercise 3

[[Your answer goes here!]]
