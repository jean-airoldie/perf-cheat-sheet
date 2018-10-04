# perf-cheat-sheet
Various helpfull perf commands.

```bash
# Display coarse-grained stats
perf stat ./benchmark
# Record the program to analyze l8er.
# Might require the binary to be build with the
# frame pointer. e.i -fno-omit-frame-pointer
perf record -g ./benchmark
# Analyzed the recording.
# Reverse the call tree (from caller to callee).
perf repord -g 'graph,0.5,caller'
```
