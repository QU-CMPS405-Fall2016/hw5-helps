This is a BIG HINT for the Simple testcases.
Here is the input and expected output for each algorithm.

### Input
```
10
100
10
10
555
```

### fifo.trace
```
Time	Event		Task
6	Arrival		Task 0 (at:6,bt:10,pr:2)
6	Serving		Task 0 (at:6,bt:10,pr:2)
11	Arrival		Task 1 (at:11,bt:5,pr:0)
14	Arrival		Task 2 (at:14,bt:81,pr:0)
15	Arrival		Task 3 (at:15,bt:14,pr:0)
16	Departure	Task 0 (at:6,bt:10,pr:2)
16	Serving		Task 1 (at:11,bt:5,pr:0)
21	Departure	Task 1 (at:11,bt:5,pr:0)
21	Serving		Task 2 (at:14,bt:81,pr:0)
21	Arrival		Task 4 (at:21,bt:40,pr:1)
30	Arrival		Task 5 (at:30,bt:89,pr:1)
39	Arrival		Task 6 (at:39,bt:84,pr:0)
45	Arrival		Task 7 (at:45,bt:64,pr:2)
50	Arrival		Task 8 (at:50,bt:73,pr:0)
51	Arrival		Task 9 (at:51,bt:21,pr:1)
102	Departure	Task 2 (at:14,bt:81,pr:0)
102	Serving		Task 3 (at:15,bt:14,pr:0)
116	Departure	Task 3 (at:15,bt:14,pr:0)
116	Serving		Task 4 (at:21,bt:40,pr:1)
156	Departure	Task 4 (at:21,bt:40,pr:1)
156	Serving		Task 5 (at:30,bt:89,pr:1)
245	Departure	Task 5 (at:30,bt:89,pr:1)
245	Serving		Task 6 (at:39,bt:84,pr:0)
329	Departure	Task 6 (at:39,bt:84,pr:0)
329	Serving		Task 7 (at:45,bt:64,pr:2)
393	Departure	Task 7 (at:45,bt:64,pr:2)
393	Serving		Task 8 (at:50,bt:73,pr:0)
466	Departure	Task 8 (at:50,bt:73,pr:0)
466	Serving		Task 9 (at:51,bt:21,pr:1)
487	Departure	Task 9 (at:51,bt:21,pr:1)

Performance Measures:
	Average waiting time: 156.80
	Average response time: 156.80
	Average turnaround time: 204.90
	CPU Utilization: 100.00%
```

### sjf.trace
```
Time    Event           Task
6       Arrival         Task 0 (at:6,bt:10,pr:2)
6       Serving         Task 0 (at:6,bt:10,pr:2)
11      Arrival         Task 1 (at:11,bt:5,pr:0)
14      Arrival         Task 2 (at:14,bt:81,pr:0)
15      Arrival         Task 3 (at:15,bt:14,pr:0)
16      Departure       Task 0 (at:6,bt:10,pr:2)
16      Serving         Task 1 (at:11,bt:5,pr:0)
21      Departure       Task 1 (at:11,bt:5,pr:0)
21      Serving         Task 3 (at:15,bt:14,pr:0)
21      Arrival         Task 4 (at:21,bt:40,pr:1)
30      Arrival         Task 5 (at:30,bt:89,pr:1)
35      Departure       Task 3 (at:15,bt:14,pr:0)
35      Serving         Task 4 (at:21,bt:40,pr:1)
39      Arrival         Task 6 (at:39,bt:84,pr:0)
45      Arrival         Task 7 (at:45,bt:64,pr:2)
50      Arrival         Task 8 (at:50,bt:73,pr:0)
51      Arrival         Task 9 (at:51,bt:21,pr:1)
75      Departure       Task 4 (at:21,bt:40,pr:1)
75      Serving         Task 9 (at:51,bt:21,pr:1)
96      Departure       Task 9 (at:51,bt:21,pr:1)
96      Serving         Task 7 (at:45,bt:64,pr:2)
160     Departure       Task 7 (at:45,bt:64,pr:2)
160     Serving         Task 8 (at:50,bt:73,pr:0)
233     Departure       Task 8 (at:50,bt:73,pr:0)
233     Serving         Task 2 (at:14,bt:81,pr:0)
314     Departure       Task 2 (at:14,bt:81,pr:0)
314     Serving         Task 6 (at:39,bt:84,pr:0)
398     Departure       Task 6 (at:39,bt:84,pr:0)
398     Serving         Task 5 (at:30,bt:89,pr:1)
487     Departure       Task 5 (at:30,bt:89,pr:1)

Performance Measures:
        Average waiting time: 107.20
        Average response time: 107.20
        Average turnaround time: 155.30
        CPU Utilization: 100.00%
```

### rr.trace
```
Time	Event		Task
6	Arrival		Task 0 (at:6,bt:10,pr:2)
6	Serving		Task 0 (at:6,bt:10,pr:2)
11	Arrival		Task 1 (at:11,bt:5,pr:0)
14	Arrival		Task 2 (at:14,bt:81,pr:0)
15	Arrival		Task 3 (at:15,bt:14,pr:0)
16	Departure	Task 0 (at:6,bt:10,pr:2)
16	Serving		Task 1 (at:11,bt:5,pr:0)
21	Departure	Task 1 (at:11,bt:5,pr:0)
21	Serving		Task 2 (at:14,bt:81,pr:0)
21	Arrival		Task 4 (at:21,bt:40,pr:1)
30	Arrival		Task 5 (at:30,bt:89,pr:1)
31	Preempt		Task 2 (at:14,bt:81,pr:0)
31	Serving		Task 3 (at:15,bt:14,pr:0)
39	Arrival		Task 6 (at:39,bt:84,pr:0)
41	Preempt		Task 3 (at:15,bt:14,pr:0)
41	Serving		Task 4 (at:21,bt:40,pr:1)
45	Arrival		Task 7 (at:45,bt:64,pr:2)
50	Arrival		Task 8 (at:50,bt:73,pr:0)
51	Preempt		Task 4 (at:21,bt:40,pr:1)
51	Serving		Task 5 (at:30,bt:89,pr:1)
51	Arrival		Task 9 (at:51,bt:21,pr:1)
61	Preempt		Task 5 (at:30,bt:89,pr:1)
61	Serving		Task 2 (at:14,bt:71,pr:0)
71	Preempt		Task 2 (at:14,bt:71,pr:0)
71	Serving		Task 6 (at:39,bt:84,pr:0)
81	Preempt		Task 6 (at:39,bt:84,pr:0)
81	Serving		Task 3 (at:15,bt:4,pr:0)
85	Departure	Task 3 (at:15,bt:4,pr:0)
85	Serving		Task 7 (at:45,bt:64,pr:2)
95	Preempt		Task 7 (at:45,bt:64,pr:2)
95	Serving		Task 8 (at:50,bt:73,pr:0)
105	Preempt		Task 8 (at:50,bt:73,pr:0)
105	Serving		Task 4 (at:21,bt:30,pr:1)
115	Preempt		Task 4 (at:21,bt:30,pr:1)
115	Serving		Task 9 (at:51,bt:21,pr:1)
125	Preempt		Task 9 (at:51,bt:21,pr:1)
125	Serving		Task 5 (at:30,bt:79,pr:1)
135	Preempt		Task 5 (at:30,bt:79,pr:1)
135	Serving		Task 2 (at:14,bt:61,pr:0)
145	Preempt		Task 2 (at:14,bt:61,pr:0)
145	Serving		Task 6 (at:39,bt:74,pr:0)
155	Preempt		Task 6 (at:39,bt:74,pr:0)
155	Serving		Task 7 (at:45,bt:54,pr:2)
165	Preempt		Task 7 (at:45,bt:54,pr:2)
165	Serving		Task 8 (at:50,bt:63,pr:0)
175	Preempt		Task 8 (at:50,bt:63,pr:0)
175	Serving		Task 4 (at:21,bt:20,pr:1)
185	Preempt		Task 4 (at:21,bt:20,pr:1)
185	Serving		Task 9 (at:51,bt:11,pr:1)
195	Preempt		Task 9 (at:51,bt:11,pr:1)
195	Serving		Task 5 (at:30,bt:69,pr:1)
205	Preempt		Task 5 (at:30,bt:69,pr:1)
205	Serving		Task 2 (at:14,bt:51,pr:0)
215	Preempt		Task 2 (at:14,bt:51,pr:0)
215	Serving		Task 6 (at:39,bt:64,pr:0)
225	Preempt		Task 6 (at:39,bt:64,pr:0)
225	Serving		Task 7 (at:45,bt:44,pr:2)
235	Preempt		Task 7 (at:45,bt:44,pr:2)
235	Serving		Task 8 (at:50,bt:53,pr:0)
245	Preempt		Task 8 (at:50,bt:53,pr:0)
245	Serving		Task 4 (at:21,bt:10,pr:1)
255	Departure	Task 4 (at:21,bt:10,pr:1)
255	Serving		Task 9 (at:51,bt:1,pr:1)
256	Departure	Task 9 (at:51,bt:1,pr:1)
256	Serving		Task 5 (at:30,bt:59,pr:1)
266	Preempt		Task 5 (at:30,bt:59,pr:1)
266	Serving		Task 2 (at:14,bt:41,pr:0)
276	Preempt		Task 2 (at:14,bt:41,pr:0)
276	Serving		Task 6 (at:39,bt:54,pr:0)
286	Preempt		Task 6 (at:39,bt:54,pr:0)
286	Serving		Task 7 (at:45,bt:34,pr:2)
296	Preempt		Task 7 (at:45,bt:34,pr:2)
296	Serving		Task 8 (at:50,bt:43,pr:0)
306	Preempt		Task 8 (at:50,bt:43,pr:0)
306	Serving		Task 5 (at:30,bt:49,pr:1)
316	Preempt		Task 5 (at:30,bt:49,pr:1)
316	Serving		Task 2 (at:14,bt:31,pr:0)
326	Preempt		Task 2 (at:14,bt:31,pr:0)
326	Serving		Task 6 (at:39,bt:44,pr:0)
336	Preempt		Task 6 (at:39,bt:44,pr:0)
336	Serving		Task 7 (at:45,bt:24,pr:2)
346	Preempt		Task 7 (at:45,bt:24,pr:2)
346	Serving		Task 8 (at:50,bt:33,pr:0)
356	Preempt		Task 8 (at:50,bt:33,pr:0)
356	Serving		Task 5 (at:30,bt:39,pr:1)
366	Preempt		Task 5 (at:30,bt:39,pr:1)
366	Serving		Task 2 (at:14,bt:21,pr:0)
376	Preempt		Task 2 (at:14,bt:21,pr:0)
376	Serving		Task 6 (at:39,bt:34,pr:0)
386	Preempt		Task 6 (at:39,bt:34,pr:0)
386	Serving		Task 7 (at:45,bt:14,pr:2)
396	Preempt		Task 7 (at:45,bt:14,pr:2)
396	Serving		Task 8 (at:50,bt:23,pr:0)
406	Preempt		Task 8 (at:50,bt:23,pr:0)
406	Serving		Task 5 (at:30,bt:29,pr:1)
416	Preempt		Task 5 (at:30,bt:29,pr:1)
416	Serving		Task 2 (at:14,bt:11,pr:0)
426	Preempt		Task 2 (at:14,bt:11,pr:0)
426	Serving		Task 6 (at:39,bt:24,pr:0)
436	Preempt		Task 6 (at:39,bt:24,pr:0)
436	Serving		Task 7 (at:45,bt:4,pr:2)
440	Departure	Task 7 (at:45,bt:4,pr:2)
440	Serving		Task 8 (at:50,bt:13,pr:0)
450	Preempt		Task 8 (at:50,bt:13,pr:0)
450	Serving		Task 5 (at:30,bt:19,pr:1)
460	Preempt		Task 5 (at:30,bt:19,pr:1)
460	Serving		Task 2 (at:14,bt:1,pr:0)
461	Departure	Task 2 (at:14,bt:1,pr:0)
461	Serving		Task 6 (at:39,bt:14,pr:0)
471	Preempt		Task 6 (at:39,bt:14,pr:0)
471	Serving		Task 8 (at:50,bt:3,pr:0)
474	Departure	Task 8 (at:50,bt:3,pr:0)
474	Serving		Task 5 (at:30,bt:9,pr:1)
483	Departure	Task 5 (at:30,bt:9,pr:1)
483	Serving		Task 6 (at:39,bt:4,pr:0)
487	Departure	Task 6 (at:39,bt:4,pr:0)

Performance Measures:
	Average waiting time: 1150.60
	Average response time: 25.00
	Average turnaround time: 269.60
	CPU Utilization: 100.00%
```

### multilevel.trace
```
Time	Event		Task
6	Arrival		Task 0 (at:6,bt:10,pr:2)
6	Serving		Task 0 (at:6,bt:10,pr:2)
11	Arrival		Task 1 (at:11,bt:5,pr:0)
14	Arrival		Task 2 (at:14,bt:81,pr:0)
15	Arrival		Task 3 (at:15,bt:14,pr:0)
16	Departure	Task 0 (at:6,bt:10,pr:2)
16	Serving		Task 1 (at:11,bt:5,pr:0)
21	Departure	Task 1 (at:11,bt:5,pr:0)
21	Serving		Task 2 (at:14,bt:81,pr:0)
21	Arrival		Task 4 (at:21,bt:40,pr:1)
30	Arrival		Task 5 (at:30,bt:89,pr:1)
39	Arrival		Task 6 (at:39,bt:84,pr:0)
45	Arrival		Task 7 (at:45,bt:64,pr:2)
50	Arrival		Task 8 (at:50,bt:73,pr:0)
51	Arrival		Task 9 (at:51,bt:21,pr:1)
102	Departure	Task 2 (at:14,bt:81,pr:0)
102	Serving		Task 3 (at:15,bt:14,pr:0)
116	Departure	Task 3 (at:15,bt:14,pr:0)
116	Serving		Task 6 (at:39,bt:84,pr:0)
200	Departure	Task 6 (at:39,bt:84,pr:0)
200	Serving		Task 8 (at:50,bt:73,pr:0)
273	Departure	Task 8 (at:50,bt:73,pr:0)
273	Serving		Task 9 (at:51,bt:21,pr:1)
294	Departure	Task 9 (at:51,bt:21,pr:1)
294	Serving		Task 4 (at:21,bt:40,pr:1)
334	Departure	Task 4 (at:21,bt:40,pr:1)
334	Serving		Task 5 (at:30,bt:89,pr:1)
423	Departure	Task 5 (at:30,bt:89,pr:1)
423	Serving		Task 7 (at:45,bt:64,pr:2)
433	Preempt		Task 7 (at:45,bt:64,pr:2)
433	Serving		Task 7 (at:45,bt:54,pr:2)
443	Preempt		Task 7 (at:45,bt:54,pr:2)
443	Serving		Task 7 (at:45,bt:44,pr:2)
453	Preempt		Task 7 (at:45,bt:44,pr:2)
453	Serving		Task 7 (at:45,bt:34,pr:2)
463	Preempt		Task 7 (at:45,bt:34,pr:2)
463	Serving		Task 7 (at:45,bt:24,pr:2)
473	Preempt		Task 7 (at:45,bt:24,pr:2)
473	Serving		Task 7 (at:45,bt:14,pr:2)
483	Preempt		Task 7 (at:45,bt:14,pr:2)
483	Serving		Task 7 (at:45,bt:4,pr:2)
487	Departure	Task 7 (at:45,bt:4,pr:2)

Performance Measures:
	Average waiting time: 398.10
	Average response time: 150.30
	Average turnaround time: 198.40
	CPU Utilization: 100.00%
```
