
## Install for windows docker

```
docker run -it --rm -v $PWD:/workdir mwaeckerlin/mingw bash

# inside docker
apt install texinfo
git clone https://github.com/y103kim/di-gdb.git
/build.sh --name di-gdb --target=aarch64-linux-gnu
cd /workdir/di-gdb
make -j
cp ./usr/lib/gcc/x86_64-w64-mingw32/9.3-win32/libgcc_s_seh-1.dll workdir/
cp ./usr/lib/gcc/x86_64-w64-mingw32/9.3-win32/libstdc++-6.dll workdir/
```
