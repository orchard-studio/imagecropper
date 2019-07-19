# Image Cropper

Image Cropper is a field extension for the Symphony CMS. It adds image cropping functionality to upload fields.

## Installation

1. Upload the 'imagecropper' folder in this archive to your Symphony 'extensions' folder.

2. Enable it by selecting the "Field: Image Cropper", choose Enable from the with-selected menu, then click Apply.

3. You can now add the "Image Cropper" field to your sections with already existing upload fields. The section has to be saved with an upload field before you can add an imagecropper field.

4. Make sure you have [Modified JIT Image Manipulation extension](http://github.com/klaftertief/jit_image_manipulation/tree/jCrop) installed and activated.

## Documentation

### Frontend

The XML output is something like

	<thumbnail cropped="yes" x1="123" x2="723" y1="123" y2="523" width="600" height="400" ratio="1.5" />

The jCrop mode of JIT expects a url like `/image/5/crop_width/crop_height/crop_x/crop_y/resize_width/resize_height/path/to/image.jpg`. `resize_width` and `resize_height` should either equal `crop_width` and `crop_height` (no resizing) or one should be 0 and the other smaller than the crop value (proportional resize).

### Backend

There needs to be an upload field in the section before you can add an imagecropper field. The section has to be saved with an upload field before you can add an imagecropper field.

You can add a filter to your datasource. The syntax is like `width: >200`, `height: <=300`, `cropped: yes` and `ratio: >1`.
There is an optional thumbnail preview in entry overview tables.

## Credits

* Thanks to all extension developers for inspirations.
* Image cropper uses [Jcrop » the jQuery Image Cropping Plugin](http://deepliquid.com/content/Jcrop.html)
