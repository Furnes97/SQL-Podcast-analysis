# Podcast Reviews Analysis

## Main [Dashboard](https://lookerstudio.google.com/s/hAkxKjOiFgU)

## Second [Dashboard](https://lookerstudio.google.com/s/uVTVEY1VajE) ~~messy dashboard~~

## Obs. Look through the structured_analysis.ipynb for the analysis, checking_db for initial data cleaning and EDA, and analysis.ipynb if you want to see a mess. 

## Real Readme starts here. 


# Aim of the project

This analysis set out to see if there is any relation between podcast category with popularity, mean review rating and what categories are oversaturated and find a potentially untapped market. 
This analysis also set out to see if any words are linked with more negative reviews and others positive.

# Installation
Install all necessary libraries
```
pip install pandas
pip install numpy
pip install matplotlib
pip install seaborn
pip install duckdb
pip install statsmodels
pip install scipy
pip install statistics
```
Or see requirements.txt

# Data Source
The dataset was downloaded from [Kaggle](https://www.kaggle.com/datasets/thoughtvector/podcastreviews/versions/28)

# How to Navigate the Files
__TLDR: Only open__ [structured_analysis.ipynb](https://github.com/TuringCollegeSubmissions/bfurne-DA.2.5/blob/master/structured_analysis.ipynb)


The analysis is mainly found in the __[structured_analysis.ipynb](https://github.com/TuringCollegeSubmissions/bfurne-DA.2.5/blob/master/structured_analysis.ipynb)__, the __[checking_db.ipynb](https://github.com/TuringCollegeSubmissions/bfurne-DA.2.5/blob/master/checking_db.ipynb)__ file is for initial EDA and data cleaning. While the __[analysis.ipynb](https://github.com/TuringCollegeSubmissions/bfurne-DA.2.5/blob/master/analysis.ipynb)__ file is to be avoided at all costs, unless clutter and a dissorganized journey is your cup of tea.

# Findings

* There are a lot of podcast categories and a lot of podcast have many subcategories. 
    * However most podcasts have a few subcategories: Between 1-3 subcategories.
    * The most reviewed podcasts have a few subcategories(based on total reviews)
        * This is not statistically tested, will come back to this in the future
* The most __popular subcategories__ are society, culture, education, business, comedy and spirituality:
    * Society and Culture are the most popular subcategories.
        * Society and Culture are always part of the same category
* Podcasts have become __increasingly more popular__ from 2005 ->  (Based on total reviews, listen time and total plays is not available in this dataset)
    * Podcasts saw a big increase during the __pandemic years__(2019-2021) and a dip in popularity after 2021
        * Podcasts reached peak popularity in 2020
* Podcasts where higher rated between 2012 and 2019 and lower rated between 2006 and 2012 and 2019 and 2023
    * podcast reviews for 2023 are only for the first two months. 
        * Doing a Z-test we found that podcasts where higher rated in 2022 compared to 2021. 
* Podcasts where higher rated on average during spring months (March, April and May) compared to the summer months (June, July and August).
    * A Z-test and confidence interval confirmed this.
        * Why is this ? Winter depression going away? More or fewer new podcasts releasing ? or some other unknown factors?
     
# Future Improvements


* __More__ statistical tests
    * Subcategory 1 vs Subcategory 2
        * Does either subcategory have a greater impact on review score ? 
* Whats the subcategories of the most popular podcasts, when did that podcast gain traction and are there more podcasts in the market after the popular podcast(s) got traction
* The one review per author was a mistake or it should have been handled in another way, hindsight is a menace sometimes, some eager fans have lost many reviews. However it does help that the same author only has one review when using total amount of reviews as a measure of how popular a podcast is. Without it being skewed because of eager fans. 
    * Future analysis, check wether or not removing all but one review per author makes some podcasts climb or fall on the top 10 most popular podcasts.
    * Check how eager fans impact review scores of a few podcasts and if the change (if there is any) has any statistical significance. 


