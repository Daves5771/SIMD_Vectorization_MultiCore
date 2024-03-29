# SIMD vectorization, and parallel algorithms in the context of computer graphics.

This software package illustrates the power of SIMD (Single Instruction Multiple Data) through vectorization techniques as well as parallel processing with the latest Microsoft .NET System—Numerics library. The codebase examples illustrate the marked speedup of processing in the context of computer graphics, a very common application for the use of vectors and matrices. The solution contains two projects: Mandelbrot and RayTracer. The code I created which is available here is derived from an old library that was missing several features.

The modified codebase I have posted has numerous changes from the original as the library and JIT had undergone significant changes:
The projects were upgraded to the latest version of the System.Numerics.Vectors (4.3.0) which can be obtained via NuGet here: https://www.nuget.org/packages/System.Numerics.Vectors.

Upgrading from the previous Microsoft.Bcl.Simd.1.0.1-beta library necessitated a number of changes.
Most of the helper functions in Util.c I deprecated and  replaced with the native functions available in the newer library.
A number of bug fixes were also made.

The following scripts are no longer needed:
enable-jit.cmd 
disable-jit.cmd

#How to run this code:
Visual Studio 2015 (or newer) Community, Professional, Enterprise (.NET 4.5 or higher) must be running on a multi-core computer.

This code requires version 4.3.0 of the System.Numerics.Vectors library or later. To get this:
Go to https://www.nuget.org/packages/System.Numerics.Vectors
(you must have NuGet installed on your system)
To install System.Numerics.Vectors, run the following command in the Nuget Package Manager Console
Install-Package System.Numerics.Vectors

To learn more about the SIMD goto https://code.msdn.microsoft.com/windowsdesktop/SIMD-Sample-f2c8c35a but note, a number of items are now obsolete, especially in the Prerequisites section.


![Alt text](ScreenShots/Mandelbrot_Single.png  "Figure 1 - Single Threaded Mandelbrot Flythru")
![Alt text](ScreenShots/Mandelbrot_Multi.png  "Figure 2 - Multi Threaded Mandelbrot Flythru")
![Alt text](ScreenShots/Mandelbrot_Multi_SIMD.png  "Figure 3 - Multi Threaded-SIMD Mandelbrot Flythru")
![Alt text](ScreenShots/RayTracerDoublePlaneSingle.png  "Figure 4a -Ray Tracer Double Plane Single Threaded")
![Alt text](ScreenShots/RayTracer Double Plan.png  "Figure 4b -Ray Tracer Double Plane Multi Threaded")
![Alt text](ScreenShots/RayTracerSinglePlaneSingle.png  "Figure 5a -Ray Tracer Single Plane Single Threaded")
![Alt text](ScreenShots/RayTracer Single Plane.png  "Figure 5b -Ray Tracer Single Plane Multi Threaded")
![Alt text](ScreenShots/Mandelbrot_Stat_Single.png  "Figure 1 - Single Threaded Mandelbrot")
![Alt text](ScreenShots/Mandelbrot_Stat_Multi.png  "Figure 2 - Multi Threaded Mandelbrot")
![Alt text](ScreenShots/Mandelbrot_Stationary_SIMD.png  "Figure 3 - Multi Threaded-SIMD Mandelbrot")
