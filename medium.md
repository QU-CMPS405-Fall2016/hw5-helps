If you fail the Medium tests but pass the Simple ones, you should double check
to see if you calculate CPU utilization correctly.

Consider the following input:
```
4
100
125
10
555
```

Manually verify that you are calculating CPU utilization correctly.

(Note: This is not the input used for the Medium tests.)

### Bug Note
The solution used by the autograder has a bug related to CPU utilization that
you will need to replicate.  (Fixing the bug would make all the simple cases
much more difficult, which I don't want to do.)

Currently, I calculate CPU utilization according to the following formula:

Utilization = (total_time - idle_time) * 100 / (total_time)

The bug is that when counting the idle_time, I forgot to count the time the
CPU is idle before the arrival of the first process.  You can noticed
this below because all the utilizations are output as 100%, but the trace
shows that the CPU is actually idle for the first 6 ms.
This bug makes the simple
test case much easier (because CPU Utilization is 100%), but is not quite
correct.  Sadly, you need to replicate this bug.

