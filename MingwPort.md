# MinGW port of picotls

## Status

Experimental.

At least compiles OK and `test-minicrypto.t.exe` unit test passes finely.

* [x] minicrypto build
* [ ] OpenSSL build

## Supported compilers

* [x] ming-w64 cross compiler
  * 7.3-win32. Ubuntu 18.04 apt installed mingw-w64 package.
* [x] llvm-mingw
  * clang 10. 20200325 https://github.com/mstorsjo/llvm-mingw

## CMake cross compilation procedure

### MinGW gcc

Edit path to mingw gcc in `scripts/bootstrap-cmake-mingw-gcc-cross.sh`, then

```
$ ./scripts/bootstrap-cmake-mingw-gcc-cross.sh
$ cd build-mingw/
$ make
```

### llvm-mingw

Assume ninja(ninja-build) is installed on your system.

Edit path to llvm-mingw clang in `scripts/bootstrap-cmake-llvm-mingw-cross.sh`, then

```
$ ./scripts/bootstrap-cmake-mingw-gcc-cross.sh
$ cd build-llvm-mingw/
$ ninja
```


## TODO

* [ ] Support OpenSSL backend
* [ ] Support MinGW native build(e.g. MSYS)
* [ ] 32bit build
* [ ] Run fuzzer

