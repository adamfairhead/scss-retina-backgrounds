# SCSS Retina Backgrounds

This is a lightweight SCSS mixin to make it quicker and easier to maintain standard and @2x images in your SCSS files.


## Usage

Notice that the file extension is missing in the mixins. The extension lives in the mixin.

To add a jpg standard + @2x combo, use:

	@include background-image-2x-jpg('path/to/file');
	
This will compile as:

	background-image: url('path/to/file.jpg');

	@media only screen and (-webkit-min-device-pixel-ratio: 1.5), 
   	only screen and (-o-min-device-pixel-ratio: 3/2),
    	only screen and (min-device-pixel-ratio: 1.5) {
        	background-image: url('path/to/file@2x.jpg');
    	}

There's a background-image-2x-jpg() mixing for jpgs and background-image-2x-png() for pngs.