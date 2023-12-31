README


The Controller package contains all of the interfaces and classes to Control the Image.  
	- interface ImageProcessingController with all the methods needed for running the program, 
		and for saving and loading an image
	- class ActionListenerController that defines all the methods needed for running the program with the GUI


The Model package contains all of the interfaces and classes for the model of the image.  
	
	These interfaces/classes contain methods for loading, altering, and saving an Image
	- interface ImageProcessingModel: contains methods for loading, altering, and saving an image
	- abstract class AbstractImageModel implements ImageProcesssingModel:
		constructs an AbstractImageModel and contains methods for altering an image
	- class PPMImageModel extends AbstractImageModel:
		constructs an PPMImageModel and contains methods for loading and saving an Image
	- class GeneralImageModel extends AbstractImageModel: 
		constructs a GeneralImageModel

	- class ImageUtil: contains methods to use when reading a PPM image

	- image package: all interfaces and classes used to make up an image: 
		- These interfaces/classes create an image with a width, height, maxValue, and an image 
		(which is a list of list of Colors) and has methods to access the fields of the classes
		- interface Image: contains get methods
		- abstract class AbstractImage implements Image: 
		constructs an AbstractImage and defines get methods
		- class PPMImage extends AbstractImage: 
		constructs a PPM image
		- class GeneralImage extendsAbstractImage:
		constructs a general image (an image of any type)

		- class Color: defines a Color as a red, green, and blue value, 
		and contains methods for getting values or altering them as needed

	- imageio package: interface & class to read and write an image
		- interface ImageReadWrite: contains methods for exporting an image or reading the RGB values
		- class GeneralReadWrite extends ImageReadWrite: 
		defines the exportImage method and the readRGB method


The View package contains all of the interfaces and classes required to render the image.
	- interface IView which contains methods for the GUI
	- class JFrameView which defines methods for the GUI
	- interface ImageProcessingView: includes methods to render a message and print all of 		the Colors in an image.
	- class PPMTextViewJava implements ImageProcessingView: 
		constructs a PPMTextView and implements methods to render 
		a message and print each pixel in the image's colors


The program will take in any commands without throwing an error, however they will only run the methods if they are one of the following: "load", "save", "red-component", "green-component", "blue-component", "value-component", "intensity-component", "luma-component", "horizontal-flip", "vertical-flip", "brighten", "darken", "greyscale", "sepia", "blur", or "sharpen".


Changes: 
- made a new controller that implements ActionListener to allow for use of the GUI
- made a new view class and interface that create the functionality for the GUI
- added methods in the Image interface to create a BufferedImage of the Image and a Graphic of the histogram

---Unfortunately, I could not get the images to load for whatever reason, despite working on this for so so long.  Nor the histogram.  I hope that you can look at my code and see what I was trying to do and give me some partial credit.  I'm really sorry.
