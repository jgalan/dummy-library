# The REST Dummy Library

This README.md is a template to be used as an example to write the library README. 

This file should include basic information to understand the main use trend of the library. It should include a brief description, what is intended for, features, functionalities, connection to other REST libraries, etc. And a description of the main use of this library.
    
NOTE: The use of this library should be documented through examples and doxygen class description.

This particular library contains basic examples of a metadata class implementation, `TRestDummyMetadata`, a dummy event data example, `TRestDummyEvent`, a dummy internal process, `TRestDummyNameProcess`, and a process connecting to another existing REST library, `TRestDummyToDetectorHitsProcess`.

You may copy directly this directory, rename the classes and define the library name inside the CMakeLists.txt file. By convention, the name of all classes/objects defined in a given library with name `XXX` will start by `TRestXXX`. This will be useful to determine a particular object belongs to a particular library.

This example is provided to help you create your own event, metadata and processes integrated in REST. Please, carefully replace the existing examples, documentation, etc, by the specific documentation of your class.

*IMPORTANT:* For creating new REST-for-Physics processes it is highly recommended to use the macro producing REST processes template files: `REST_MakeProcess.C`.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine.

TODO: Add a description and explain that the recommended way is to install it as a git submodule in RestFramework project.

Additionaly you may download a copy of this library cloning it using the corresponding git command.

```
git clone git@lfna.unizar.es:rest-development/RestDummyLib.git
```

### Prerequisites

The only mandatory prerequisite is that REST and ROOT6 are installed in your system. Details on the installation of ROOT will be found at the [ROOT's official site](root.cern.ch). 
To avoid problems during the installation it is recommended that REST libraries will be compiled using the same version of g++ compiler used to compile ROOT and REST.


### Installing

Just place your library directory at the `source/libraries/` from the main REST source repositories, and enable the compilation of the library at the main REST compilation system:

```
cd rest-framework/build
cmake -DRESTLIB_DUMMY=ON ..
```

The REST compilation system will identify the option `-DRESTLIB_DUMMY` with a directory named `source/libraries/dummy`, just replace `DUMMY` by the name of your library directory name.


### Basic tests of this library

You can test now that REST libraries are loaded without errors inside the ROOT environment using the `restRoot` command. After launching `restRoot` you should see a message on screen similar to the following one, where the recently compiled library will be found in the list of loaded libraries.

```
   ------------------------------------------------------------
  | Welcome to ROOT 6.14/06                http://root.cern.ch |
  |                               (c) 1995-2018, The ROOT Team |
  | Built for macosx64                                         |
  | From tags/v6-14-06@v6-14-06, Dec 11 2018, 12:58:00         |
  | Try '.help', '.demo', '.license', '.credits', '.quit'/'.q' |
   ------------------------------------------------------------

Loading library : libRestDummy.dylib
Loading library : libRestFramework.dylib
Loading library : libRestDetector.dylib
```

### A brief description of the examples provided

## License

This project is licensed under the GNU License - see the [LICENSE](https://github.com/rest-for-physics/framework/blob/master/LICENCE) file for details.

## Acknowledgments

`TOBE written`

* Hat tip to anyone whose code was used
* Inspiration
* etc
