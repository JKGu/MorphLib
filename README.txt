MorphLib
==============

This C++ package is a simplified Version (pure c++ Library) for
"Automating Image Morphing using Structural Similarity on a Halfway Domain （Siggraph 2014)"

It has been successfully compiled in the x64 Windows with the compiler Visual Studio 2013. The CPUMorph Library has no other dependency. While the example project which show just how to use the CPUMorph Library requires the OpenCV Library.

Those Simplifications include:
(1)	Remove GPU acceleration
(2)	Remove quadratic path
(3)	Remove Poisson boundary extension
(4)	Use 3x3 ssim neighbors to replace 5x5 neighbors

The full version can be found here:
https://github.com/liaojing/Image-Morphing/

and the executable program is:
https://drive.google.com/folderview?id=0BwMKxLMS8dFBSTBPa2lRUWxGbFk&usp=sharing

Jing Liao

2015/06/01

===============
Package edited

Part of Example/main.cpp has been edited so that it can now morph and produce an "average result" of arbitrary number of images. 

It reads images from UserFiles/InputImages and UserFiles/Masks, and produces an output.png at UserFiles/OutputImages.

Given N images, the time complexity is O(N) and space complexity is O(1). Assuming the alpha is linear, main.cpp will always produce an accurate "average" result.

There is a ready-to-use x64 exectuable release in the release folder.

Limitations: it assumes that all inputs are valid and the working directory is correctly set. It does not do much handling error exceptions.

This modified package is used as part of the project https://github.com/JKGu/xray
Thank the original author for the morphing algorithm.

Junkang Gu
2020/10/24

