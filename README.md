# QISKit Simulator (https://github.com/QISKit/qiskit-sdk-py/tree/master/src/qiskit-simulator) For Windows
## Building with Microsoft Visual Studio

1. Download and install **Intel® Math Kernel Library (Intel® MKL)** 

   https://software.intel.com/en-us/mkl  

   or 

   http://www.softpedia.com/get/Programming/Components-Libraries/Intel-Math-Kernel-Library.shtml

   **NOTE!** You can maybe use other Windows **LAPACK/BLAS** compatible library, but i am not sure, this project default configured to **Intel® Math Kernel Library (Intel® MKL)**.
  

2. Open project file in Visual Studio. (Visual Studio **>=2012**, recommended **2015**)
3. In Visual Studio go to: **Project/Properties/Configuration Properties/VC++ Directories/Library Directories** and add new string with **YOUR DRIVE LETTER:\YOUR INTEL MATH KERNEL LIBRARY INSTALLATION FOLDER\Intel\Composer XE 2015\mkl\lib\intel64**
4. Build solution for **Release x64** configuration.

    **NOTE!** You can build for other configurations, but this project default configured to **Release x64**.
 
   **NOTE!** If after running application you have error about **missing mkl_rt** library add this file to application root folder. File path: **YOUR DRIVE LETTER:\YOUR INTEL MATH KERNEL LIBRARY INSTALLATION FOLDER\Intel\Composer XE 2015\redist\intel64\mkl\mkl_rt.dll**

5. Happy researching!
***
**NOTE!** Parallelization with OpenMP not yet supported, but i'm working on it)

**NOTE!** Builded and tested in Windows 10 Pro x64.
