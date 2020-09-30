# PizzaPNG by Marat Tanalin

Easy-to-use GDI+ based library that generates clean PNG images free of unneeded meta chunks added by GDI+.

Example — creating a 123×42 green image with 50% opacity:

```
#include "pizza-png/src/Image.h"

uint16_t width = 123, height = 42;
MaratTanalin::PizzaPNG::Image image(width, height);

for (size_t y = 0; y < height; y++) {
	for (size_t x = 0; x < width; x++) {
		image.addPixel(0, 255, 0, 127);
	}
}

std::string pngData = image; // Ready-to-save binary PNG-file data.
```

See the project [webpage](http://tanalin.com/en/projects/pizza-png/) for details.