# Cache-Simulator
This program is written in C and it simulates Bélády and Least Recently Used cache replacement methods. It reads in a series of non-zero memory addresses from a .dat file and a command line argument telling it which cache method to use. It also takes command line arguments to determine whether to construct a direct-mapped, 2-way, or 4-way set associative cache. As memory addresses are read in it determines whether there is a hit or miss in the cache construct. It outputs the total amount of hits and misses. Note that the default cache size is 256.

## Command Line Arguments
```./a.out ASSOCIATIVITY CACHE_STYLE INPUT_FILE```

## Argument Meanings
* ```ASSOCIATIVITY```: Enter ```1``` for direct-mapped, enter ```2``` for 2-way, or enter ```4``` for 4-way.  
* ```CACHE_STYLE```: Enter ```LRU``` for Least Recently Used or enter ```B``` for Bélády's.
* ```INPUT_FILE```: Create your own or use a provided ```.dat``` file of integer memory addresses.

## Output
As memory addresses are read in, the program will print them and tell the user whether there was a hit or miss. Once all of the input is read in, it outputs the total amount of hits and misses as well as the cache accesses and the overall hit rate.

## Sample Output
```
bash$ ./a.out 2 LRU ex1.dat
Cache size: 256
Cache associativity: 2
Cache sets: 128
Cache algorithm: LRU
1 (miss)
33 (miss)
2 (miss)
34 (miss)
65 (miss)
1 (hit)
66 (miss)
2 (hit)
97 (miss)
65 (hit)
Cache accesses: 10
Cache hits: 3
Cache misses: 7
Overall hit rate: 0.300000
```
