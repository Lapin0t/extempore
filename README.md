# Extempore

A programming environment for cyberphysical programming.

[![Build status](https://badge.buildkite.com/1c333a08100a9d083983b6c816e6f0163158e0f7f61da8490a.svg)](https://buildkite.com/extemporelang/tests)

## Getting started

To get started, you can either download a binary release or build Extempore from
source yourself.

### The easy way

Download [VSCode](https://code.visualstudio.com/), install the Extempore
extension and then use the _Extempore: Download binary_ command to do the rest.

For more details, head to the [Quickstart
page](https://extemporelang.github.io/docs/overview/quickstart/) in Extempore's
online docs.

### The slightly harder way

Download the latest [binary
release](https://github.com/digego/extempore/releases) for your platform, unzip
it and run `extempore` (`extempore.exe` on Windows) from inside the `extempore`
folder.

Then, [set up your text editor of
choice](https://extemporelang.github.io/docs/guides/editor-support/) and away
you go.

### Build from source

This will download and build all the dependencies you need (including LLVM). So,
if you've got a C++ compiler (for `gcc`, version 4.9 or later is required), git
and CMake, here are some one-liner build commands:

On **Linux/macOS**:

    git clone https://github.com/digego/extempore && mkdir extempore/cmake-build && cd extempore/cmake-build && cmake .. && make && sudo make install
    
On **Linux/macOS with JACK**:

    git clone https://github.com/digego/extempore && mkdir extempore/cmake-build && cd extempore/cmake-build && cmake -DJACK=ON .. && make && sudo make install
    
On **Windows**:

    git clone https://github.com/digego/extempore && mkdir extempore/cmake-build && cd extempore/cmake-build && cmake -G"Visual Studio 14 2015 Win64" .. && cmake --build . --target ALL_BUILD --config Release

#### Other build-from-source notes

- if you want to download the Extempore binary assets as well (required for some
  of the examples, but a ~300MB downloaded) then add the `-DASSETS=ON` CMake
  option to the above build commands

- the `install` target will build both the `extempore` binary executable and
  AOT-compile the standard library (for faster startup)

- on Linux the JACK configuration is not as well tested as the default (ALSA)
  one (patches welcome)

## See Extempore in action

Check out these videos:

- [The Concert Programmer](https://www.youtube.com/watch?v=yY1FSsUV-8c)
- [Interactive, distributed, physics simulation](https://vimeo.com/126577281)
- [Programming in Time](https://www.youtube.com/watch?v=Sg2BjFQnr9s)
- [The Physics Playroom - interactive installation](https://vimeo.com/58239256)
- [An *old* Graphics Demo](https://vimeo.com/37293927)
- [A Programmer's Guide to Western Music](https://www.youtube.com/watch?v=xpSYWd_aIiI)
- [Ben's livecoding gig videos](https://benswift.me/livecoding/)

## Docs & Community

Extempore documentation can be found at https://extemporelang.github.io/docs/

You can also join the Extempore community:

- [Extempore google group](http://groups.google.com/group/extemporelang)
- [Extempore mailing list](mailto:extemporelang@googlegroups.com)
- [#extempore on chat.toplap.org](https://chat.toplap.org/home) (although not as
  well-monitored as the mailing list)

## Cite Extempore

- [Extempore: The design, implementation and application of a cyber-physical programming language](https://openresearch-repository.anu.edu.au/handle/1885/144603)
- [Systems level liveness with extempore](https://dl.acm.org/citation.cfm?id=3133858)

## Licence

Copyright (c) 2011-2018, Andrew Sorensen

All rights reserved.

Redistribution and use in source and binary forms, with or without 
modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, 
   this list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice,
   this list of conditions and the following disclaimer in the documentation 
   and/or other materials provided with the distribution.

Neither the name of the authors nor other contributors may be used to endorse
or promote products derived from this software without specific prior written 
permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" 
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE 
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE 
ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE 
LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR 
CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF 
SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS 
INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN 
CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) 
ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE 
POSSIBILITY OF SUCH DAMAGE.
