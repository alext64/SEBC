My VM have 8 cores and 16GB of ram and my cluster has 3 DataNode, so I have decided to assign 80% of 24 vcores (19!) to the script for testing. 

**Slowest Teragen**

```
Mappers: 1
Reducers: 1
Ram: 512

real    2m43.274s
user    0m14.827s
sys     0m1.766s
```

**Fastest Teragen**

```
Mappers: 19
Reducers: 19
Ram: 512

real    1m8.093s
user    0m14.799s
sys     0m1.984s
```

**Slowest Terasort**

```
Mappers: 1
Reducers: 1
Ram: 512

real    4m39.906s
user    0m17.717s
sys     0m2.442s
```

**Fastest Terasort**

```
Mappers: 1
Reducers: 19
Ram: 512

real    2m46.016s
user    0m17.839s
sys     0m2.172s
```

