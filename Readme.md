Fuzzing conntrackd and conntrack tools. More infos to come ...

# Instructions

Configure:

```
$ CC=afl-gcc AFL_USE_ASAN=1 CFLAGS=-DFUZZ LDFLAGS=-ldl ./configure
```

Compile: 

```
$ make -j 4
```

Run:

```
$ sudo src/conntrackd -C <config file> -X <fuzz file>
```
