### 1. Introduction
#### Algorithm Library Framework
![image](https://github.com/peoffice/docs/blob/master/pngs/alg_framework.png)
Algorithm are developped by C&C++ language for crossing platform(Linux,Windows). Algorithm Wrapper are developped by C# or Java language for C# or Java calling.
#### Develop IDE and Running System
##### Develop IDE
- Algorithm: Visual Studio 2013
- Algorithm Wrapper for .NET: Visual Studio 2013
- Algorithm Wrapper for Java: Eclipse
##### Running System
- Windows 32&64 System
- Linux 64
### 2. Overall Priciple of Algorithm Library Development
- Provide algorithm design documents and unit test cases based on standard templates
- Develop algorithm under the algorithm design documents strictly
- Coding based on standard C&C++ to cross platform 
- Third party libraries must accord with corssing platform and suitable license
- Just funtions are acceptable as export objects for library
- Algorithm classification is managed by namespace way
- Accurate and stander code annotation and can be created help doc by doxygen tool
- Code enters algorithm library after code reviewing
- Calling wrappers for C# and Java are provided as well as algorithms
### 2. Code Standards
#### introduction of code solution
##### Algorithm code solution
![image](https://github.com/peoffice/docs/blob/master/pngs/alg_code_sln.png)
##### Algorithm wrapper code solution
![image](https://github.com/peoffice/docs/blob/master/pngs/alg_wrapper_sln.png)
#### Code specifications
##### Bsic specifications
- Just functions are exported from the algorithm library module, but you can design your program with OOP
- for input parameters type of exporting function, basic types are recommended, but if you think struct type is more fittable, you can use it after review this problem. But bool type is not permitted to use.
- Return type of exporting function must be int, and the meaning of values is descripted in code annotation.
- Message,warning,erroring information are recorded by log tools in algorithm library.
- Use standard library, common function library and third party library for crossing flatform requirements
- When you need to use big object with much memory, think of creating it in heap memory.
- Annotation is keeping with code modification
- Annotation of header files and functions is essential
- Be cautious to use global variable
##### Code annotation
###### Header file annotation
![image](https://github.com/peoffice/docs/blob/master/pngs/code_annotation_header.png)
###### Function annotation
![image](https://github.com/peoffice/docs/blob/master/pngs/code_annotation_function.png)
###### Class, Structure and Enumtype annotation
![image](https://github.com/peoffice/docs/blob/master/pngs/code_annotation_class.png)
###### Programming annotation
- `/*annotation*/`
- `//annotation`
### 3. Algorithm Library Wrapper
- Java wrapper is developped based on JNA(Java Native  Access) Open Source Library, it's license is LGPL
- C# wrapper is developped based on P/Invoke framework of Microsoft
### 3. Third party Libraries Installation
###### 1. Boost
- Version 1.65.1
- License [Boost license](http://www.boost.org/users/license.html "Boost license")
- WebSite [http://www.boost.org/](http://www.boost.org/ "Boost")
- Installation
  - Windows
    1. Not be used 
  - Linux
    1. Go to the directory tools/build/
    2. Run bootstrap.sh
    3. Run b2 install --prefix=PREFIX where PREFIX is the directory where you want Boost Build to be installed
    4. Add PREFIX/bin to your PATH environment variable
###### 2. Log4Cpp
- Version 1.1.3
- License LGPL v2
- WebSite [https://sourceforge.net/projects/log4cpp/](https://sourceforge.net/projects/log4cpp/ "Log4Cpp")
- Installation
  - Windows
    1. Open the project file with vs2013 and build
  - Linux
    1. ./Configure
    2. make
    3. make check
    4. make install
###### 3. GoogleTest
- Version 1.7.0
- License BSD 3-clause
- WebSite [https://github.com/google/googletest](https://github.com/google/googletest "GoogleTest")
- Installation
  - Windows
    1. Open the project file with vs2013 and build
  - Linux
    1. Suppose you put Google Test in directory ${GTEST_DIR)
    2. g++ -isystem ${GTEST_DIR}/include -I${GTEST_DIR} -pthread -c ${GTEST_DIR}/src/gtest-all.cc
    3. ar -rv libgtest.a gtest-all.o
###### 4. Tinyxml
- Version 1.0.1
- License zlib/libpng license
- WebSite [https://sourceforge.net/projects/tinyxml/](https://sourceforge.net/projects/tinyxml/ "Tinyxml")
- Installation
  - Windows
    1. Open the project file with vs2013 and build
  - Linux
    1. make
### 2. Algorithm Library Building
#### Windows
1. Enter solutions folder
2. Open alg_core.sln file with vs2013 and set MathUTRunner project to active project
3. Build whole solution for win32 and x86 version
4. Run or debug
#### Linux
1. Enter Linux folder
2. sudo ./alg_build_deploy.sh
3. ./alg_run.sh for running test 
