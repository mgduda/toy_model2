# MMM Toy Model II

The MMM Toy Model consists of a main program that invokes a physics driver over
a small number of iterations. The physics driver makes calls to various physics
schemes that come from a separate repository.

At build time, an attempt is made to obtain a specified version of phyics
schemes using the ESMCI `manage_externals` tool.  Switching between versions of
physics or between physics repositories is accomplished by modifying the
`Externals.cfg` file in the `config` subdirectory of this repository.

## Building the MMM Toy Model II

Running `make` with either `gnu` or `intel` specified as the target will compile
the toy model with the GNU or Intel compilers, respectively. For example:
```
make gnu
```
The build process will automatically download the physics schemes, or report if
the requested physics schemes cannot be obtained.
