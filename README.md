# WinCE Decompressor

[![Python version](https://img.shields.io/badge/python-%3E=_3.7-green.svg)](https://www.python.org/downloads/)
[![GitHub license](https://img.shields.io/github/license/KodaSec/wince-decompr.svg)](https://github.com/KodaSec/wince-decompr/blob/master/LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/KodaSec/wince-decompr?style=social)](https://github.com//KodaSec/wince-decompr/stargazers)

### Description
WinCE firmware images stores compressed Execute-In-Place (XIP) files. WinCE v5+ uses a modified LZX compression algorithm. This script will decompress a WinCE v5+ compressed blob. WinCE Decompressor is cross-compatible with Unix and Windows.

### Installation

WinCE Decompressor only requires Python3.

```
# Install Python3 if it is not installed

# Clone the repo
$ git clone https://github.com/KodaSec/wince-decompr.git

# Change the working directory to wince-decompr
$ cd wince-decompr

# Ready to run script
```

### Usage

```
$ python3 wincedecompr.py -h
usage: wincedecompr.py [-h] [-o uncompressed_dir] [-cs compressed_file_size]
                       [-us uncompressed_file_size]
                       file_name

positional arguments:
  file_name             input file name

optional arguments:
  -h, --help            show this help message and exit
  -d uncompressed_dir   output uncompressed directory
  -cs compressed_file_size
                        compressed file size
  -us uncompressed_file_size
                        uncompressed file size
```

To decompress a WinCE compressed file into a directory:
```
python3 wincedecompr.py -d <output_dir> -cs <compressed_size> -us <uncompressed_size> <input_file>
```

### TODO
* Add LZ77 Support for older versions of WinCE (<5)

### Special Thanks
Collin Moon <<mooncollin@gmail.com>>

Frank Tursi <<frank@kodasec.com>>

Eric Biggers <<ebiggers3@gmail.com>>

Stuart Caie <<kyzer@cabextract.org.uk>>

Ali Scissons <<ali.scissons@gmail.com>>
