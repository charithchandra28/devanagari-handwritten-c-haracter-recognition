            DEVANAGARI HANDWRITTEN CHARACTER RECOGNITION 
 
1) There are 46 handwritten characters of devanagari.all the images are in black 
background and white foreground(like gray scale images).

2)done exploratory data analysis on train images like
         i)plotting each character
        ii)plotting histogram equalization of images
       iii)finding min-max ranges of rgb image
        iv)finding mean,variance,median of image
         v)finding kurtosis values for an image i.e finding
          how much deeper the image is deviated from gaussian distribution
	   vi)finding skewness of image  i.e finding
	how much deviation from Gaussian distribution(left skewness and right skewness)

3)The metric used is accuracy,dataset is splitted into train,crossvalidation,test.
		
4)then after doing eda i thought of applying ml models.i applied various models like k-nn,logistic regression,naivebayes,linear svm,decision trees,random forest

for each model i have done
        i)finding the right hyperparameter for each model
		ii)plotting training error vs validation error
		iii)finding no of misclassified points
		iV)plotting confusion matrix
		V)plotting precision and recall matrix
			
5)the results are like this
     Alogorithm           Test Accuracy 
i)   K-NN                 91.02 for k=5
ii)  Naive Bayes          58.7 for alpha=1e-05
iii) Logistic Regression  69.0 for c=100
iV)  Linear Svm           65.9 for c=1000
V)   Decision trees       57.2 for d=45 
Vi)  Random Forest        91.4 for d=40 and base learners=100  

6)then i moved to complex approaches i.e convolution neural networks(state of the art for images )

7)Built simple convnet and also built vgg16 transfer learning pretrained(removing top layers and made our own custom layers) on imagenet dataset.

Results look like this
     i)  Simple CONVNET       95.25 for 15 epochs
    ii)  VGG16 PRETRAINED     92.50 for 15 epochs        
	
8)I saved weights of simple convenet as it gives best performance

9)predicted on new images using the above saved model.


10)then lastly i built a web application using django and  hosted  it in heroku app
webapplink: https://charithai.herokuapp.com/ 

11)you can see files at github link:
https://github.com/charithchandra28/devanagari-handwritten-character-recognition

Note:all the notebooks and saved weights which i described above
are there in this zip file 
