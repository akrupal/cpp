# cpp
learning c and c++

 g++ cherno/1.cpp
 the above command will generate a.out file which can be run using ./a.out

 if you want to give a specific name use
  g++ cherno/1.cpp -o program
  this will output program which can be run using ./program

  if you have multiple files that need to be compiled just add them before the -o flag and they will be compiled together


  anything starting with a # is a preprocessor statement as it is carried out just before the actual compilation

  cin.get() to wait till the user presses enter

  only cpp files are compiled the header files are just included in the cpp files

  every cpp file will get compiled into an object file(.obj) the linker will then take these obj files and glue them together to make an exe

  if a function is defined in a seperate file a function declaration will fix the compilation error
  if you still have a linker issue it means the linker was not able to wire the function written is another file to this call maybe the function name or some parameter or return value were different

  if I create a function as
  static int Multiply
  that would mean its only accessible to that translation unit

  if you have a function defined in the header file and the header file is included in multiple cpp files you would get an error
  to fix these either make it static so that each translation unit has its own version of that function or
  make it inline function so that every instance of that function call is replaced by the code or
  the best method is to move the defination to any translation unit and add the declaration to the header file so that it will be auto included wherever the header file is included

  int is traditionally 4 bytes
  1byte = 8bits
  4bytes = 32bits

  char a = 'A';
  char a = 65;
  both are same as A has ASCII value 65

  pointers int*
  references int&

  usually we put the function declarations in the header files and the definations in translation units

  #pragma once in header files to make them include only once

  other alternative to pragma once is
  #ifndef _LOG_H
  #define _LOG_H

  #endif

  <> these brackets will search the file in include path folders
  "" these will search relative to file path
  but you can use "" is place of <> to search in include path folders
  for example #include "iostream" will work