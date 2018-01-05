### 1. Introduction
### 2. Algorithm Library Building
### 3. Third party Libraries Installation
##### Linux System
###### 1. Boost
- Version 1.65.1
- License [Boost license](http://www.boost.org/users/license.html "Boost license")
- WebSite [http://www.boost.org/](http://www.boost.org/ "Boost")
- Installation
  1. Go to the directory tools/build/
  2. Run bootstrap.sh
  3. Run b2 install --prefix=PREFIX where PREFIX is the directory where you want Boost Build to be installed
  4. Add PREFIX/bin to your PATH environment variable
###### 2. Log4Cpp
- Version 1.1.3
- License LGPL v2
- WebSite [https://sourceforge.net/projects/log4cpp/](https://sourceforge.net/projects/log4cpp/ "Log4Cpp")
- Installation
  1. ./Configure
  2. make
  3. make check
  4. make install
###### 3. GoogleTest
- Version 1.7.0
- License BSD 3-clause
- WebSite [https://github.com/google/googletest](https://github.com/google/googletest "GoogleTest")
- Installation
  1. Suppose you put Google Test in directory ${GTEST_DIR)
  2. g++ -isystem ${GTEST_DIR}/include -I${GTEST_DIR} \
    -pthread -c ${GTEST_DIR}/src/gtest-all.cc
  3. ar -rv libgtest.a gtest-all.o
###### 4. Tinyxml
- Version 1.0.1
- License zlib/libpng license
- WebSite [https://sourceforge.net/projects/tinyxml/](https://sourceforge.net/projects/tinyxml/ "Tinyxml")
- Installation
  1. make
