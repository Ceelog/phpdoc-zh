Cairo is a native PHP extension to create and modify graphics using the
Cairo Graphics Library.

The Cairo Graphics Library is a 2D library written in C with support for
multiple output devices. Currently supported output targets include the
X Window System, Quartz, Win32, image buffers, PostScript, PDF, and SVG
file output. Experimental backends include OpenGL (through glitz), XCB,
BeOS, OS/2, and DirectFB. The library also has support for two types of
text manipulation and layout. The "toy" API provides demo quality
support, and the glyphs API, although full-featured, works best with a
helper library such as pango. Font backend support includes FreeType,
Quartz, Win32, and User fonts.

There are two types of computer graphics, vector and raster. Raster
graphics are the representation of images as an array of pixels. Vector
graphics use geometrical primitives such as points, lines, curves or
polygons to represent images. The primitives are created using
mathematical equations. The Cairo Graphics Library takes a vector
approach to graphics, allowing smaller size, infinite zooming, and
moving, scaling and rotating without degrading image quality.

Operations in the cairo graphics library including stroking and filling
cubic Bézier splines, transforming and compositing translucent images,
and antialiased text rendering. All drawing operations can be
transformed by any affine transformation (scale, rotation, shear, and
others) This is very similar to drawing operations for PostScript and
PDF drawing.

The Cairo PHP Extension aims to provide support for all officially
supported font backends and surface backends, as well as expose all
available functionality in cairo to PHP users.
