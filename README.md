# Test Workflow
After cloning the repo, update `line 10` of `main.cpp` to reflect the absolute path.

```
git clone 
cd test_fp
mkdir build
cd build
wget https://github.com/sameeul/filepattern/archive/refs/heads/try_cpp_api.zip
unzip try_cpp_api.zip 
mkdir local_install
cd filepattern-try_cpp_api/
mkdir build
cd build
cmake -Dfilepattern_SHARED_LIB=ON -DCMAKE_PREFIX_PATH=../../local_install -DCMAKE_INSTALL_PREFIX=../../local_install ..
make -j4
make install
cd ../../
cmake -DCMAKE_PREFIX_PATH=./local_install -DCMAKE_INSTALL_PREFIX=./local_install ..
make
./test_fp
```