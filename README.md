# SIMD_Vectorization_MultiCore

This software package illustrates the power of SIMD (Single Instruciton Multiple Data) through vectorization techniques as well as multi-core processing with the latest Microsoft .NET System.Numerics library. The codebase examples illustrate the marked speedup of processing using in the context of computer graphics, a very common application for the use of vectors and matricies. The solution contains two projects: Mandelbrot and RayTracer. The code is an update of a post by Immo Landwerth which had last been updated on 4/4/2014. https://code.msdn.microsoft.com/windowsdesktop/SIMD-Sample-f2c8c35a

The modified codebase I have posted has the following changes:
The projects were upgraded to the latest version of the System.Numerics.Vectors (4.3.0) which can be obtained via NuGet here: https://www.nuget.org/packages/System.Numerics.Vectors.

Upgrading from the previous Microsoft.Bcl.Simd.1.0.1-beta library, necessitated a number of changes.
Most of the helper functions in Util.c were deprecated and were replaced with the new native functions available in the newer library.
Some minor bug fixes were made.

// MandelBrot file upagres 
App.xaml.cs
FlyThru.cs
Mandelbrot.csproj
packages.config (removed)
VectorDouble.cs
VectorDoubleStruct.cs
VectorFloat.cs
VectorFloatStruct.cs
VectorHelpers.cs

//RayTrace file upgrade
App.xaml.cs
Camera.cs
Color.cs
Intersection.cs
Light.cs
Packages.config (removed)
Ray.cs
RayTracer.csproj
Scene.cs
SceneObjectBase.cs
Utils.cs

The following scripts are no longer needed
enable-jit.cmd 
disable-jit.cmd

How to run this code:
You must have Visual Studio 2015 Community, Professional, Enterprise (.NET 4.5 or higher) running on a multi-core computer.

This code requires version 4.3.0 of the System.Numerics.Vectors library or later. To get this:
Go to https://www.nuget.org/packages/System.Numerics.Vectors
(you must have NuGet installed on your system)
To install System.Numerics.Vectors, run the following command in the Nuget Package Manager Console
Install-Package System.Numerics.Vectors

To learn more about the SIMD goto https://code.msdn.microsoft.com/windowsdesktop/SIMD-Sample-f2c8c35a but note, a number of items are now obsolete, especially in the Prerequisites section.
