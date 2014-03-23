libsixel
========

## What is this?

This package provides encoder/decoder implementation for DEC SIXEL graphics, and
some converter programs.

![img2sixel](http://zuse.jp/misc/libsixel-1.png)

SIXEL is one of image formats for terminal imaging introduced by DEC VT series.
Its data scheme is represented as a terminal-friendly escape sequence.
So if you want to view a SIXEL image file, all you have to do is "cat" it to your terminal.

## Build and install

```
$ ./configure
$ make
# make install
```

To build source package:

```
$ make package
```

## Usage of command line tools

Convert a jpeg image file to a sixel file

```
$ img2sixel -p 16 < image/egret.jpg > egret.sixel
```

Convert a sixel file to a png image file

```
$ sixeltopng < egret.sixel > egret.png
```

## License

The MIT License (MIT)

Copyright (c) 2014 Hayaki Saito

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


tosixel.c and fromsixel.c are derived from "sixel" original version (2014-3-2)
http://nanno.dip.jp/softlib/man/rlogin/sixel.tar.gz

It is written by kmiya@culti.

He distributes it under very permissive license which permits
useing, copying, modification, redistribution, and all other
public activities without any restrictions.

He declares this is compatible with MIT/BSD/GPL.


This software includes stbi-1.33 (stb_image.c),
public domain JPEG/PNG reader.
http://nothings.org/stb_image.c


This software includes stbiw-0.92 (stb_image_write.h),
public domain PNG/BMP/TGA writer.
http://nothings.org/stb/stb_image_write.h

