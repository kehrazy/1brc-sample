# 1brc-sample

This is a program for generating sample data for the [`1 Billion Row Challenge`](https://1brc.dev) challenge.

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

# License

This program is licensed under the MIT license. See the [LICENSE](LICENSE) file for details.
