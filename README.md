# ImageEditor

Image Editor written in Java to demonstrate MVC design paradigm. Work done as part of CS5010 coursework.

Modes of operation:
1. GUI - Interactive editor featuring operations for loading and saving an image, with menu for performing the image editing. Menu supports both keyboard shortcuts and point-and-click style of use.
2. CLI - Script based usage for bulk operations on images.

Supported image manipulations:
1. Filtering - Blur/sharpen an image using either the built-in or custom filters.
2. Color transformations: Built-in transformations (Sepia and Greyscale) as well as support for user-defined kernels.
3. Image mosaicing.
4. Dithering an image.
5. Modular logic for building checkerboard and rainbow patterns with user-specified parameters.
6. Modular logic for constructing flags of nations according to their standard specification. Currently supported flags: Switzerland, Greece and France.

The project follows the Model-View-Controller (MVC) design paradigm. As such, the source code is structured into three main directories:
1. /src/model - contains the model interfaces and implementation. Model objects serve as containers for data as it flows through the application.
2. /src/view - handles data ingress/egress while interacting with the user. Both CLI and GUI modes of operation are supported, with modular interfaces to facilitate extensibility.
3. /src/controller - handles the application logic, which in this case is the implementation of various image edit operations. The controller exposes interfaces that the view works with, and hides the implemementation details for abstraction purposes. Also, the controller interface is modular and supports multiple modes of use, such as GUI or CLI modes without any code changes.

There are additional directories that contain things like object factories for the Factory design pattern, utility functions and I/O functions.
