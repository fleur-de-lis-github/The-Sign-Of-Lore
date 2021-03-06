# The Sign Of Lore

## Problem Scenario

`American Sign Language (ASL)` substantially facilitates communication in the deaf community. However, there are only ~250,000-500,000 speakers which significantly limits the number of people that they can easily communicate with. The alternative of written communication is cumbersome, impersonal and even impractical when an emergency occurs.

## Our Approach 

The project derives its name from the etymology of `lore`- *a body of traditions and knowledge on a subject or held by a particular group, typically passed from person to person by word of mouth.*

 In order to
diminish this obstacle and to enable dynamic communication, we present an ASL recognition system that uses Convolutional Neural Networks (CNN) in real time to translate data of a user’s ASL signs into text. Our problem consists of three tasks to be done :

```diff
- Obtaining data of the user signing (input)
+ Classifying each frame in the data to a letter
! Reconstructing and displaying the most likely word from classification scores (output)
# text in gray

```
## Potential Client
Being an inclusive business and addressing the needs of hard of hearing and Deaf customers can offer significant benefits to your business. Making an effort to be inclusive can open up many new opportunities for your business that would otherwise be missed. 

Talented people with hearing impairments will feel more comfortable working for the company if a program like this is in place when they arrive.

The value that these accommodations can provide for customers and clients should not be overlooked either. It is simply good customer service. Most people who are hearing impaired or deaf will be pleasantly surprised to have someone available that they can communicate with easily, and they will remember this positive experience.

![image](https://user-images.githubusercontent.com/73738414/142749963-9372be2a-c937-4bc7-8864-171898fc03ac.png)




## Project Workflow

:pushpin: Import Libraries and Load the ASL Dataset <br />
:pushpin: Exploratory Data Analysis(EDA) <br />
      - Data Preprocessing
      - Normlization
      - Reshaping the Data <br />
:pushpin: Data Augmentation  <br />
:pushpin: Convolution Neural Networks <br />
      - Model Optimization <br />
:pushpin: Data Analysis and Evaluation <br />
:pushpin: Visualize the Predictions <br />
:pushpin: Conclusion and Future Work <br />



## Data Description

![#f03c15](https://via.placeholder.com/15/f03c15/000000?text=+) The dataset format is patterned to match closely with the classic MNIST. 

>Each training and test case represents a label (0-25) as a one-to-one map for each alphabetic letter A-Z (and no cases for 9=J or 25=Z because of gesture motions). 
>The training data (27,455 cases) and test data (7172 cases) are approximately half the size of the standard MNIST but otherwise similar with a header row of label, >pixel1,pixel2….pixel784 which represent a single 28x28 pixel image with grayscale values between 0-255. 

![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+)The original hand gesture image data represented multiple users repeating the gesture against different backgrounds.

>The Sign Language MNIST data came from greatly extending the small number (1704) of the color images included as not cropped around the hand region of interest. To create new >data, an image pipeline was used based on ImageMagick and included cropping to hands-only, gray-scaling, resizing, and then creating at least 50+ variations to enlarge the >quantity. 

![#1589F0](https://via.placeholder.com/15/1589F0/000000?text=+)The modification and expansion strategy was filters ('Mitchell', 'Robidoux', 'Catrom', 'Spline', 'Hermite'), along with 5% random pixelation, +/- 15% brightness/contrast, and finally 3 degrees rotation. Because of the tiny size of the images, these modifications effectively alter the resolution and class separation in interesting, controllable ways.

The dataset API `kaggle datasets download -d datamunge/sign-language-mnist`

## Citation
- https://link.springer.com/chapter/10.1007/978-981-13-9939-8_3
- https://www.researchgate.net/publication/345359906_CNN_Model_for_American_Sign_Language_Recognition
- https://www.ijert.org/sign-language-recognition-system-using-convolutional-neural-network-and-computer-vision
