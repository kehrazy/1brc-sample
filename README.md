# 1brc-sample

This is a program for generating sample data for the [1 Billion Row Challenge](https://1brc.dev) challenge.

It utilizes the [OpenMP](https://www.openmp.org/) library to parallelize the generation of the data,
as well as good strategies for good IO performance to minimize the time it takes to generate the data.

# Usage

```sh
$ ./create-sample <number-of-rows>
```

Where `<number-of-rows>` is the number of rows to generate.

# Build

```sh
$ clang -Ofast -march=native -fopenmp=libomp -lm -std=c11 -flto -Wall -Wextra -Wpedantic -Werror create-sample.c -o create-sample
```

# Benchmarks

Per 100,000 measurements, this tool takes about 80ms to run on my machine.
```
Benchmark 1: ./create-sample 100000
  Time (mean ± σ):      78.4 ms ±   5.6 ms    [User: 421.3 ms, System: 38.7 ms]
  Range (min … max):    75.3 ms … 109.1 ms    40 runs
```
# License

This program is licensed under the MIT license. See the [LICENSE](LICENSE) file for details.
