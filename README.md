# IIT-Madras-ML-Crack-Detection

Team Members - Ayush Agarwal , Utkarsh Sahu , Yashwardhan Sable 

This repositor is an entry for "PS-1 , Concrete Crack detection"  L&T EduTech Hackathon held under Shaastra , the tech fest of IIT Madras .

## Our results 

Our model has achieved a perfect F1 score of 1 . To know more read along 

## Our methodology - 

### Bilateral Filtering : 
After manual data exploration and analysis of the images , it was found that the images were contaminated with salt and pepper like noise . I wanted to amplify the differene between the positive and the negative image class , so image processing was a vital step of our solution approach . Initially we experimented with __Median Filtering__ , since it is known fact in Image Processing and computer vision that salt and pepper noise is best removed my median filter . 

However the results were not that satisfactory . This was because median filtering does not preserve edges , and the crucial differenciating factor in our dataset are the crack edges . After studying a bit , we observed that __Bilateral Filtering__ preserves the edges as well as gets rid of salt and pepper like noises with some tradeoff as compared to the median filter , hence this was selected . It gave satisfactory results on our dataset . 

### Opening Operation (Morphological operation) : 

To further remove the concrete like pattern and amplify the difference between the classes , we decided to use the morphological operations . After experimenting with morphological operations opening and closing on the dataset , it was found that single iteration of opening operation with a 3x3 kernel was found to be suitable for our dataset . Opening is a morphological operation in which first erosion and then dilation occus on the image , and is used to remove the small pixels of noise while preserving the foreground bigger subjects . It gave satisfactory results on our dataset .

### Data Augmentation :

Since our dataset is small , and is image based , hence we decided to use data augmentation to increase the size of the dataset . From manual inspection , it was observed that in some of the positive examples , the cracks are at the corners of the image and hence random zooming way throw the cracks out of the pictures , thus creating inconsistencies in the dataset . Hence we decided to only user __perfect 90 and 180 degree rotations , flipping__ etc so as to avoid the risk of creating false positives in our dataset . 

We also decided to __vary the brightness__ by very less amount of around 10% , since the dataset did not have huge difference in contrast and brightness . 

Soon we were able to increase our dataset from 300 examples per class to ???? examples per class . 

### The Machine Learning Modelling part 

Since our dataset consists of images , we were able to choose few ML algorithms as per our requirements . After a bit of analysis of work done in this field from reading research papers , we were able to eliminate down to a few architectures that would be able to perform well on our dataset . Since the problem statement itself said that transfer learning models would be appreciatable , hence we decided to use __Transfer Learning__ instead of training custom architecture models for our dataset . 

We 


