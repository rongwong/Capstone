# Emotion Detection on CNN


![Emotion_to_ratings](https://github.com/rongwong/capstone_cnn_emotion_to_ratings/blob/master/images/emotion_to_ratings.png?raw=true)



## Executive Summary

According to Statista, Singapore has over 4.65M smartphone users (i.e over 90% of its population) with Apple's share of mobile devices to be at 33.6% of the marketshare. This plays to the tune of .. 1.6M Apple smartphone users in Singapore alone and large market for profit for Apple's App Store.

To improve the quality and quantiy of reviews in the App Store, I prospose the ideal of having the consumer take a real time picture and have a Multi-class Classifier detect emotions and translate it to a quantitative review rating. 

For this task, I have gathered four datasets:

CK+: The Extended Cohn-Kanade (CK+) database, 593 sequences across 123 subjects, labelled 8 emotions.
FER-2013: The Facial Expression Recognition 2013 (FER-2013) Dataset, 32,298 images, labelled 7 emotions.
KDEF: The Karolinska Directed Emotional Faces (KDEF), 4900 images across 70 subjects, labelled 7 emotions.
GENKI-4K: The MPLab GENKI Database , 4000 images, labelled 2 emotions.

I have choosen to work with Deep Learning, using a Convolutional neural network (ConvNets or CNNs) for this image recognition task and have built a network from scratch.

During Image processing, the datasets were merged and effects were added on:

1. Original
2. Adaptive Exposure (0.3)
3. Adaptive Exposure then Equalized
4. Equalized
5. Equalized then Adaptive Exposure


In seperate notebooks, the 5 datasets were trained and validated, as well as a sixth baseline model trained on the original dataset. The AE Dataset and AEE Datatset both produced the same weighted-F1 score, with further analysis on the Confusion Matrix, Recall and Precision scores, I decided to use the AEE Dataset for the final run.

The Dataset of AEE was used on my final CNN multi-class Classifer with a final score was a weighted-F1 of 0.78, beating out our baseline by 0.31


---- 

## Contents:

- 1.0 Import and Sort Images
- 2.0 EDA
- 3.0 Image Processing
- 4.0 Model and Dataset Selection


----

## Conclusion and Recommendations

While all data points to heavy usage of Apps in the App Store, when browsing through the store, we see only a fraction of user reviews coupled with very skewed ratings. This shows users not leaving their reviews and misrepresentation of ratings due to many reasons.

To improve the quality and quantiy of reviews in the App Store, I prospose the ideal of having the consumer take a real time picture and have a Multi-class Classifier detect emotions and translate it to a quantitative review rating. This also has the future option to add on recommender system to recommend popular words to add to the review. If sucessful, the tool will accurately predict emotions of faces.

Using a combined Dataset preprcoessed with Adaptive Exposure and Equalization, the CNN Model was able to achieve a weighted-F1 score of 0.79, beating the baseline score by 0.31.

The Application of the CNN model would include a real time prediction of emotions by the user, this then will translate to ratings populated by the model tied to each emotional response. This new form of reviewing may encourage more users to rate the products in the App Store.

Improvement of the Model requires higher quality and quantity of data being fed into the model for further training and generalisation.


## Datasets:

Due to size, my dataset is found here:
refer to Google Drive: https://drive.google.com/file/d/16sCyrxE5CGXtM0Qmvhhg3xhic-s6-haR/view?usp=sharing

Please find Image Datasets here:

- CK+ : http://www.jeffcohn.net/resources/
- KDEF: https://www.kdef.se/
- FER-2013: https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge/data
- GENKI-4K: https://inc.ucsd.edu/mplab/wordpress/index.html%3Fp=398.html


### Datasets References and Acknowledgements:

For CK+:
P. Lucey, J.F. Cohn, T. Kanade, J. Saragih, Z. Ambadar and I. Matthews, "The Extended Cohn-Kanade Dataset (CK+): A complete dataset for action unit and emotion-specified expression", in the Proceedings of IEEE workshop on CVPR for Human Communicative Behavior Analysis, San Francisco, USA, 2010.

For fer2013:
"Challenges in Representation Learning: A report on three machine learning contests." I Goodfellow, D Erhan, PL Carrier, A Courville, M Mirza, B Hamner, W Cukierski, Y Tang, DH Lee, Y Zhou, C Ramaiah, F Feng, R Li, X Wang, D Athanasakis, J Shawe-Taylor, M Milakov, J Park, R Ionescu, M Popescu, C Grozea, J Bergstra, J Xie, L Romaszko, B Xu, Z Chuang, and Y. Bengio. arXiv 2013.

For KDEF:
Lundqvist, D., Flykt, A., & ÷hman, A. (1998). "The Karolinska Directed Emotional Faces - KDEF", CD ROM from Department of Clinical Neuroscience, Psychology section, Karolinska Institutet, ISBN 91-630-7164-9.

For GENKI-4K:
http://mplab.ucsd.edu, The MPLab GENKI-4K Dataset.

#### Other References:

Apple's App Store ecosystem facilitated over half a trillion dollars in commerce in 2019. (2020, July 15). Retrieved August 06, 2020, from https://www.apple.com/newsroom/2020/06/apples-app-store-ecosystem-facilitated-over-half-a-trillion-dollars-in-commerce-in-2019/

E-Conomy SEA 2018: Southeast Asia's internet economy hits an inflection point. (n.d.). Retrieved August 06, 2020, from https://www.thinkwithgoogle.com/intl/en-apac/tools-resources/research-studies/e-conomy-sea-2018-southeast-asias-internet-economy-hits-inflection-point/

Grab Celebrates Fifth Anniversary and Significant User Milestones. (2017, September 07). Retrieved August 06, 2020, from https://www.grab.com/sg/press/business/grab-celebrates-fifth-anniversary-significant-user-milestones/ 

Lazada and Shopee, top e-commerce mobile shopping apps in Southeast Asia, according to market survey by iPrice Group and App Annie. (2019, May 15). Retrieved August 06, 2020, from https://www.onlinecitizenasia.com/2019/05/15/lazada-and-shopee-top-e-commerce-mobile-shopping-apps-in-southeast-asia-according-to-market-survey-by-iprice-group-and-app-annie/

Müller, J. (n.d.). Topic: Smartphones in Singapore. Retrieved August 06, 2020, from https://www.statista.com/topics/5842/smartphones-in-singapore/

Ping, C. (2019, August 27). Shopee extends lead over Lazada to be region's top online shopping platform: IPrice. Retrieved August 06, 2020, from https://www.straitstimes.com/business/shopee-extends-lead-over-lazada-to-be-regions-top-online-shopping-platform-iprice

Singapore users complain the most but that's a 'good thing', says Gojek co-CEO. (n.d.). Retrieved August 06, 2020, from https://www.todayonline.com/singapore/singapore-users-complain-most-thats-good-thing-says-gojek