# COVID-19-Fake-News-Detection

![image](https://drive.google.com/file/d/1buHRQIFzZPqL01wHfefDcxP-VegloYdR)


# Abstract:
Since 2019, the COVID-19 pandemic has impacted the entire world and affected the lives of billions of people. This pandemic has led to unprecedented consequences on the public health, economy, and all other sectors as well. Therefore, at the beginning of the semester, I decided to build an AI solution that will allow us to learn the pandemic’s behavior within this uncertainty and know when and under what conditions countries will expect increases, peaks, and reductions in the number of new cases based on cases history and governments polices. However, after doing extensive research and learning from what others have done so far, I came to a conclusion that this problem relies on unpredicted human behaviors and there are plenty of factors other than government policies can affect the number of cases which will as a result affect our model accuracy. On the other hand, all datasets that I found were very broad and not enough to build an accurate model. The best dataset I have got was about COVID-19 cases in Russia and training the model only on COVID-19 cases in Russia will not be enough to generalize it on other countries so it will not be an efficient solution. On the other hand, the topic is still understudying and data about government policies isn’t fully prepared. In short, I found it risky for us as beginners to continue with the idea and I decided to shift the idea a little bit and decided to tackle another problem related to this topic. It is the spread of COVID-19 FAKE NEWS!!!

# Introduction: 
Nowadays, everyone has access to posting anything on social media and these posts are being accessible by everyone. Wrong information is being circulated among different channels. Thus, searching for reliable resources is becoming extremely hard especially with news related to COVID-19 pandemic. People are sharing misleading information about precaution measures, how the virus is spreading, and most importantly, the vaccine. This is a global issue because people started to believe these rumors and decided not to take the vaccine. Such misinformation has caused confusion, disruption, and even deadly consequences in some cases.
I decided to build an AI solution that will allow us to detect whether the given news is true or false. The different social media channels can make use of our solution to make their platforms credible and trusted by giving a warning sign next to the suspicious news so that people don’t take it for granted. 
Related Work:
I did extensive research looking for good datasets and finally I found a big one (more than 40,000) with general news labeled as fake or true which I can use to build the model and make sure it is working well with high accuracy on the general news. I also found a COVID-19 fake news dataset that contains many files with real and fake tweets which I can clean and combine to make a big and well-organized dataset that can serve our purpose.
Dataset:
 Both datasets are from Kaggle website and can be accessed through the following links:
•	General news dataset 
•	COVID-19 news dataset 

# Datasets:
General news dataset:  

![image](https://drive.google.com/uc?export=view&id=1loZErA_zaYRQsIRa6Gy08luOwDKv2zvC)

Covid-19 true news dataset:  

![image](https://drive.google.com/uc?export=view&id=1_2p60q5VHxN2X_AMruLbCcK4Po3Jn-KA)

Covid-19 fake news dataset:  

![image](https://drive.google.com/uc?export=view&id=1TsmZ6a26QEoF_78ze9jgfppgGIMo91x_)   
# Model and Methodology:
-	Importing libraries: such as numpy, pandas, nltk, and re. 
-	Reading data: I started building the model by first reading the data and then labelling true news as 0 and fake news as 1. 
-	Data Processing and cleaning: Because I am dealing with messy texts that contain stopwords, blank lines and unnecessary punctuations, I had to remove them for our model to perform better. I used ntlk.stem package to clear the data and perform stemming to reduce inflection in words and get their root form. 
-	Tokenization: To break up our text into pieces such as words.
-	Data Splitting: After I cleaned the data, I splitted it into parts to train, validate, and test.
-	Model Building: The typical deep learning models such as Convolutional Neural Networks (CNN) and Recurrent Neural Networks (RNN) can be usually used to detect complex patterns in textual data. I built the model using Long Short-term Memory (LSTM) from recurrent neural network (RNN) which is a tree-structured recurrent neural network used for classification to classify if the news is fake or true and it can also process an entire sequence of data so it will perform better than RNN on such long sequential data. LSTM allows looking at particular sequence both from front-to-back as well as from back-to-front.  I started by creating a sequential model and add layers to it. Then I trained the model and evaluate its accuracy. 

I used 70% of the data for training and 30% for testing because LSTM models (neural networks) internally splits the training into validation. Thus, in model.fit(), I assigned the testing data as validation data to assess the result and avoid overfitting.


# Results:
I ended up with a 97.99% accuracy.

