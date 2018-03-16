This repository contains a [conda][conda] recipe for building [freecontact][fc],
a tool for the prediction of residue-residue contacts from correlated mutations.

## Prerequisites

1. You will need an installation of [conda][miniconda].

2. Your root conda installation must have the `conda-build` installed.

## Building

You should be able to build this package by simply running `conda build .`. A
package will be built for each combination of BLAS library (of `mkl` and
`openblas`) and each supported CPU architecture.

## Patches

This recipe removes some non-standard calls to `tempfile` in the `configure`
script, as well disabling automatic detection of CPU flags. Some patching is
also required to work with `mkl`.

[conda]: https://conda.io
[miniconda]: https://conda.io/miniconda.html
[fc]: https://rostlab.org/owiki/index.php/FreeContact
