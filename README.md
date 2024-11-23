# libgmath
Library for vector and matrix operations

## Install
To install library run
```
cc -o gnub gnub.c
sudo ./gnub
```
in your terminal.

## Quick example
```c
#include <gmath.h>
#include <gtransform.h>

int main(int argc, char* argv)
{
    mat4x4 perspective_matrix = transform__projection_inline(90, 0.1, 100); // create perspective matrix
    vec4 point                = { 0, 1, 2, 1 };                             // create point

    math_mat4x4__apply_to_vec4(&perspective_matrix, &point); // apply perspective matrix to point
}
```
and compile this with `cc -o example example.c -lgmath`.
