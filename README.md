# PuTTY for win32 storing configuration into file
Original patch and documentation can be found at http://jakub.kotrla.net/putty/

## Build with Windows
For building with Windows you need to have following tools installed:
- `Perl`
- `mingw32`
- maybe `msys`

Build
```
perl mkfiles.pl
cd windows
```

mingw32

    mingw32-make XFLAGS=-DCOVERITY -f Makefile.cyg putty.exe

msys

    make XFLAGS=-DCOVERITY -f Makefile.cyg putty.exe

## Build with Linux
For building with Linux you need to have following tools installed:
- `Perl`
- `mingw32`

e.g. for Debian based distributions

    apt-get install perl mingw32

Build

    perl mkfiles.pl
    cd windows
    make TOOLPATH=i586-mingw32msvc- -f Makefile.cyg putty.exe

