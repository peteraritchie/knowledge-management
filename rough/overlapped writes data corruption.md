# overlapped writes data corruption
<!-- is this named "singled" or "stripped" -->
```javascript
count += 1
```

Seems pretty innocuous, right? Break that statement down into its component parts, add a bit of hand-waving, and what you end up with is something like this:

1. Load value of variable count into memory.
1. Increment value of count by one in memory.
1. Write newly updated count back to disk.

![](https://assets.alexandria.raywenderlich.com/books/con/images/059bdc302d67cee75048e2d016a228ffc899e0a9b5fb74c698a07d0666506a0e/original.png)
The above graphic shows:

- Thread 1 kicked off a clock cycle before thread 2 and read the value 1 from count.

- On the second clock cycle, thread 1 updates the in-memory value to 2 and thread 2 reads the value 1 from count.

- On the third clock cycle, thread 1 now writes the value 2 back to the count variable. However, thread 2 is just now updating the in-memory value from 1 to 2.

- On the fourth clock cycle, thread 2 now also writes the value 2 to count… except you expected to see the value 3 because two separate threads both updated the value.

This type of race condition leads to incredibly complicated debugging due to the non-deterministic nature of these scenarios.

If thread 1 had started just two clock cycles earlier you’d have the value 3 as expected, but don’t forget how many of these clock cycles happen per second.

You might run the program 20 times and get the correct result, then deploy it and start getting bug reports.