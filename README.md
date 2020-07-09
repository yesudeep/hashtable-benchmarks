# Hashtable Benchmarks

Benchmarks for comparing hashtable implementations.

1. Build:

You will need [Bazel](https://bazel.build/) installed to build and run the
benchmarks.  Consider using [Bazelisk](https://github.com/bazelbuild/bazelisk)
to automatically manage Bazel for you and keep it up to date.

```shell
bazel build :hashtable_benchmarks
```

We assume the presence of a C++ 14-compliant compiler.  Also note that `-c opt`
is the default configuration for Bazel.  You can review the
[`.bazelrc`](.bazelrc) configuration file for additional details.

2. Run:

```shell
bazel-bin/hashtable_benchmarks --benchmark_format=json > benchmark-results.json
```

3. Analyze:

You can use [colab.research.google.com](https://colab.research.google.com) along
with [`hashtable_benchmarks.ipynb`](hashtable_benchmarks.ipynb) to parse the
generated `benchmark-results.json`.

4. Contribute:

We would like this to turn into *the* place for comparing hashtables in C++.  We
will accept external dependencies on other hashtable libraries (assuming they
have a compatible licence).  We encourage folks to improve and modify both the
analysis and the benchmarks themselves as we learn things.  Please join the
[discussion](https://groups.google.com/forum/#!forum/hashtable-benchmarks).

# Disclaimer

This is not an officially supported Google product.
