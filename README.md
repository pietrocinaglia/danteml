# DANTEml - DANTE for (m)ulti(l)ayer network alignment
DANTEml is a software tool for the pairwise global alignment of multilayer networks (MLNs), based on an our existing method optimized for dynamic networks (i.e., DANTE, https://github.com/pietrocinaglia/dante).

We C-compiled it (via Nuitka, https://nuitka.net) for macOS, Linux, and Windows.


## Installation

DANTEml needs Python3 >= 3.9, and the dependencies listed in 'requirements.txt'.

It has been tested on the following O.S.:
- macOS (Ventura 13.5, Apple M1), Python v3.11.
- Linux (Ubuntu, AMD64), Python v3.10.
- Windows 11 (AMD64), Python v3.11.

The packages listed into 'requirements.txt' can be installed via [Python Package Installer (pip)](https://pip.pypa.io/en/stable/):

```
pip install -r requirements.txt
```

(or its alias 'pip3', if any).


## Help

./DANTEml [-h] -s SOURCE -t TARGET [-sm SIMILARITY_MATRIX] -o OUTPUT

Options:

  -h, --help : Show this help message and exit

  -s SOURCE, --source SOURCE : Path of Multilayer Network 1 (G, source).

  -t TARGET, --target TARGET : Path of Multilayer Network 1 (G, source).

  -sm SIMILARITY_MATRIX, --similarity_matrix SIMILARITY_MATRIX : Path of the existing Node Similarities as 'Similarity Matrix (.sm)' file format; compression: gzip.

  -o OUTPUT, --output OUTPUT : Output filename (Default: 'output.txt').


## Run the toy example
You may use the dataset included into this repository ('toy_example'), for demonstration purposes only, as follows:

```
./DANTEml toy_example/smallMLN.txt toy_example/largeMLN.txt my_alignment.txt
```

<br />

You may see the Help by executing:

```
./DANTEml --help
```

<br />

## MIT License

Copyright (c) 2022

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.