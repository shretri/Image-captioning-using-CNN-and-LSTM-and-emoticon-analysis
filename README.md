# Image-captioning-using-CNN-and-LSTM-and-emoticon-analysis

Image captioning is used to generate automatic captions describing an image. 
Thus here we present an implementation of image captioning based on neural network (i.e. CNN + LSTM).The model first extracts the image feature by CNN and then generates captions by RNN (LSTM). CNN is VGG16 and RNN is a standard LSTM. Normal Sampling and Beam Search were used to predict the caption of images.
After getting the text, we applied sentimental analysis to our text which results in output as a sentiment. These sentiments are then mapped with emojis to get the caption with emoji. The dataset we used here is Flickr 8k. 

Steps

1)	Import the dataset Flickr 8K and store it in the file from where you can save it in pandas data frame.
2)	Cleansing of the caption is to be done i.e. removing punctuation and higher frequency words (doesn’t contain important information).
3)	Add two tokens named start and end in the captions.
4)	Create features for the images by applying the pre-trained model VGC16 and Inception V3.
5)	Mapped image with the respective text. Then change the character into integers for entering it into the model as the model accepts only integers.
6)	Split training and testing data. Trained the model using training data.
7)	Test the model and evaluate performance.
8)	The generated text then passed for sentimental analysis which generates sentiments for a particular text.
9)	The output sentiments are mapped with emojis. Then merge the emoticons with text for generating a better caption.
