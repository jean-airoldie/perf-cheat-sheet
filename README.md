# perf-cheat-sheet
Various helpfull perf commands.

```bash
# Display coarse-grained stats
perf stat ./benchmark
# Record the program to analyze l8er.
# Might require the binary to be build with the
# frame pointer. e.i -fno-omit-frame-pointer
perf record --call-graph dwarf ./benchmark
# Analyzed the recording.
# Reverse the call tree (from caller to callee).
perf repord --call-graph dwarf 'graph,0.5,caller'
```
https://gist.github.com/KodrAus/97c92c07a90b1fdd6853654357fd557a
https://gist.github.com/dlaehnemann/df31787c41bd50c0fe223df07cf6eb89
