# IIT-Madras-ML-Crack-Detection

Team Members - Ayush Agarwal , Utkarsh Sahu , Yashwardhan Sable 

This repositor is an entry for "PS-1 , Concrete Crack detection"  L&T EduTech Hackathon held under Shaastra , the tech fest of IIT Madras .

## Our results 

Our model has achieved a perfect F1 score of 1 . To know more read along 

## Our methodology - 

* __Bilateral Filtering__ : After manual data exploration and analysis of the images , it was found that the images were contaminated with salt and pepper like noise . I wanted to amplify the differene between the positive and the negative image class , so image processing was a vital step of our solution approach . Initially we experimented with __Median Filtering__ , since it is known fact in Image Processing and computer vision that salt and pepper noise is best removed my median filter . 

However the results were not that satisfactory . This was because median filtering does not preserve edges , and the crucial differenciating factor in our dataset are the crack edges . After studying a bit , we observed that __Bilateral Filtering__ preserves the edges as well as gets rid of salt and pepper like noises with some tradeoff as compared to the median filter , hence this was selected . It gave satisfactory results on our dataset . 

* __


