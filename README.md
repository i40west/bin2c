# bin2c
Convert a binary file into a C source vector.

This is adapted from a bin2c by Sandro Sigala I found somewhere on the net,
years ago.

It takes a file and converts it to an unsigned char in C code, so it can
be embedded in source code.

## Usage

    bin2c [-c] [-s] [-z] <input_file> <output_file>

        -c    add "const" to the definition
        -s    add "static" to the definition
        -z    terminate the array with a zero (useful for embedded C strings)

## Examples

    bin2c -c myimage.png myimage_png.c
    bin2c -z sometext.txt sometext_txt.c
