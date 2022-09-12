# Assignment 1

The assignment has been divided into modules. Each file corresponds to a module, which can be tested separately. Additionally, there is the image enhancement file which contains all enhancements and can be used to apply any combination of them, ie applying skin and shadow saliency enhancement but not sky.

## Notes and Known Issues

The face detection was done with pre-trained models from OpenCV. The models are not perfect and may not detect faces in some images, ie the sample image named 'test.jpg'.
The best results for both skin and shadow saliency enhancement were obtained with the 'side.jpg' image and the 'sky.jpg' image was the best for sky enhancement.

### Skin enhancement
The edge aware constant propagation map was implemented with the pre built function of opencv. This function either rounds up or down a float number to the nearest integer. This way, the resulting image will contain sharp edges and a brighter colour than intended.

### Sky enhancement
The cloud colour correction is not working as intended, as it is applying a blue colour instead of a white one. this way, the ideal blue colour is being applied to the whole sky area instead of just the "clean" sky.

### Shadow enhancement
The wls filter can't be applied to the DARK area of the image, because it throws an error when adding a matrix with its transpose. As such, the resulting image has an halo effect around the shadow area.

## Acknowledgements
The idea of using an rgb skin detection algorithm was given by Arnav Singh.