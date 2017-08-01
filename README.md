# jade-autocompile modified package


Auto compile JADE files on save

[Original atom package site](https://atom.io/packages/jade-autocompile)

## Configuration
The two first comment blocks of file can be used to pass parameters to the compiler.
The first comment block must be a valid JSON.

* If you want to compile the current file you must pass the name of the output file, like this:

  ```jade
  //- {"output":"output.html"}
  ```
  The **output** parameter supports relatives paths and two variables replacement.
  * $1: Name of the original jade file
  * $2: Extension of the original file.

  ​

* If the current file is included as partial or a template you can specify which file to compile using the **main** parameter in the following way:
  ```jade
  //- {"main": "../index.html"}
  ```

  This parameter can be an array of files if necessary:

  ```jade
  //- { "main": ["../index.jade", "../contact.jade"] }
  ```

  Keep in mind that every single file included must have its set of parameters.
  ​

* You can add additional properties to the compiler, like this:

  ```jade
  //- {"output":"output.html", "pretty":false}
  ```

  Note: **pretty** parameter can't be used in the included file as this option is specific for every single file.

  ​
  The second block can have a javascript object to be used as locals for the compiler.

  ```jade
  //{
      name: 'Dan',
      date: new Date,
      myFunc: function(){
        return true;
      }
    }
  ```

## About this Package 
 
This package was forked from jade-autocompile Atom extension by Manuel Rueda: https://github.com/ManRueda/jade-autocompile 


## License

  The MIT License (MIT)

  Copyright (c) 2017

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
