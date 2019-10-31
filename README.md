This is a random number generator, that shows a list of numbers, and can compare to another number the user specifies.

Additionally, the user can filter all random numbers by odd/even (or disable filtering). So if the user enabled even filtering, only the even random numbers should show!

Tasks:

1. There's a bug when our input field is empty, we should fix this!
    - Open the console to see the error
2. Filtering isn't set up at all!
    - First we should make our 3 buttons in App.vue do something
    - We'll probably need another 'data' to store what filtering is set
    - And we'll need to tell results-list about this new variable
3. Results.vue isn't showing whether a number is greater/less than our 'compare' number
    - We should fix the 'output' computed

Optional:

- Make greater-than Results blue, and less-than Results red.
  - https://vuejs.org/v2/guide/class-and-style.html
