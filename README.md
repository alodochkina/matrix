# matrix_library

Library for processing numerical matrices in C. Provides basic matrix creation, arithmetic, linear-algebra helpers (determinant, complements, inverse) and unit tests.

## Build & test

- Build and run the unit tests:
  ```sh
  make test
  ```
- Generate coverage report:
  ```sh
  make gcov_report
  ```

See the build rules in the [Makefile](Makefile).

## Usage

Include the public header in your code:
- [`s21_matrix.h`](s21_matrix.h)

Create and manipulate matrices with the provided API (implementations are linked):

- Creation / destruction
  - [`s21_create_matrix`](s21_create_matrix.c)
  - [`s21_remove_matrix`](s21_remove_matrix.c)

- Comparison / basic ops
  - [`s21_eq_matrix`](s21_eq_matrix.c)
  - [`s21_sum_matrix`](s21_sum_matrix.c)
  - [`s21_sub_matrix`](s21_sub_matrix.c)
  - [`s21_mult_number`](s21_mult_number.c)
  - [`s21_mult_matrix`](s21_mult_matrix.c)
  - [`s21_transpose`](s21_transpose.c)

- Linear algebra
  - [`s21_calc_complements`](s21_calc_complements.c)
  - [`s21_determinant`](s21_determinant.c)
  - [`s21_inverse_matrix`](s21_inverse_matrix.c)

Example (pseudo):
```c
#include "s21_matrix.h"

matrix_t A, B, R;
s21_create_matrix(2, 2, &A);
s21_create_matrix(2, 2, &B);
/* fill A, B */
s21_sum_matrix(&A, &B, &R);
```

## Tests

Unit tests are in [s21_test.c](s21_test.c) and use the Check framework. The Makefile links against Check when running `make test`.

## License

This project is licensed under the terms in [LICENSE](LICENSE).

## Files in this repository

- [s21_calc_complements.c](s21_calc_complements.c)
- [s21_create_matrix.c](s21_create_matrix.c)
- [s21_determinant.c](s21_determinant.c)
- [s21_eq_matrix.c](s21_eq_matrix.c)
- [s21_inverse_matrix.c](s21_inverse_matrix.c)
- [s21_matrix.h](s21_matrix.h)
- [s21_mult_matrix.c](s21_mult_matrix.c)
- [s21_mult_number.c](s21_mult_number.c)
- [s21_remove_matrix.c](s21_remove_matrix.c)
- [s21_sub_matrix.c](s21_sub_matrix.c)
- [s21_sum_matrix.c](s21_sum_matrix.c)
- [s21_transpose.c](s21_transpose.c)
- [s21_test.c](s21_test.c)
- [Makefile](Makefile)
- [LICENSE](LICENSE)
- [README.md](README.md)
