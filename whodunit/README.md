# Questions

## What's `stdint.h`?

stdint.h is a header file that establishes aliases for different implementations of integers by typedefining the different types. The implementation of different integer types (signed vs unsigned for example) differs by system.  stdint.h therebye helps make programs portable across systems by establishing conventions for the object representation of integers. The object representation of an integer consists of 0 or more padding bits, 1 or more value bits, and either 0 or 1 sign bits depending on the signedness of the integer type. The value representation represents the number itself.

## What's the point of using `uint8_t`, `uint32_t`, `int32_t`, and `uint16_t` in a program?

If each integer inhabits only the number of bits required of it - memory use and storage is maximised. The alternative, of an integer inhabiting more bits than it requires, would be wasteful. An integer would require more bits to represent higher numbers or to represent both the negative and positive numbers (signed). Also, certain systems or domains expect specific integer bit widths for specific behaviours or purposes.

## How many bytes is a `BYTE`, a `DWORD`, a `LONG`, and a `WORD`, respectively?
BYTE - 1 byte
DWORD - 4 bytes
LONG - 4 bytes
WORD -2 bytes

## What (in ASCII, decimal, or hexadecimal) must the first two bytes of any BMP file be? Leading bytes used to identify file formats (with high probability) are generally called "magic numbers."

hexadecimal - 42 4D
ascii - BM
decimal -16973

## What's the difference between `bfSize` and `biSize`?

bfSize - the size of the BMP file itself including the header files
biSize - the size of the BITMAPINFOHEADER file. This is constant at 40 bytes.

## What does it mean if `biHeight` is negative?

If biHeight is positive, the bitmap is a bottom-up DIB and its origin is the lower-left corner. If biHeight is negative, the bitmap is a top-down DIB and its origin is the upper-left corner.

## What field in `BITMAPINFOHEADER` specifies the BMP's color depth (i.e., bits per pixel)?

biBitCount

## Why might `fopen` return `NULL` in lines 24 and 32 of `copy.c`?

If the file doesnt exist or if the file doesnt have the requisite permissions.

## Why is the third argument to `fread` always `1` in our code?

Because we are only looking for one of the respective structures of the size described.

## What value does line 63 of `copy.c` assign to `padding` if `bi.biWidth` is `3`?

3

## What does `fseek` do?

fseek moves the file position to a desired location within the file .

## What is `SEEK_CUR`?

SEEK_CUR is a macro that sets the position from which to move - to be the current file position.
