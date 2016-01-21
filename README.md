Updated by Ryan O'Connor for both platforms to use full uri and original filename (minus the path) for destination file.

# Image Resizer for Cordova #
By: Protonet GmbH

Authors: Joschka Schulz

## Adding the Plugin ##

Use the Cordova CLI and type in the following command:

`cordova plugin add https://github.com/protonet/cordova-plugin-image-resizer.git`

## Sample Code

At the moment the plugin is only avaible on the android and ios platform.

### resize

    window.ImageResizer.resize(options, success, failed);

### Options
  - **uri**(String): The Uri for the image on the device to get scaled
  - **folderName**(String): The name of the folder the image should be put in
  - **quality**(Number): Quality given as Number for the quality of the new image
  - **width**(Number): The width of the new image,
  - **height**(Number): The height of the new image

### Android Example
    var options = {
          uri: uri,
          folderName: "Protonet Messenger",
          quality: 90,
          width: 1280,
          height: 1280};

    window.ImageResizer.resize(options,
      function(image) {
         // success: image is the new resized image
      }, function() {
        // failed: grumpy cat likes this function
      });
