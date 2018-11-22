# News Category Prediction

## Problem Statement 
  Build a ML model in python that can Identify the category of news based on headlines and short descriptions.


## Data 
  This dataset contains around 125k news headlines from the year 2013 to 2018 obtained from HuffPost.
  [Click here for Data File](https://drive.google.com/open?id=1_g0qNjlqMGTKw5ipcJ_L5-FybsAgRNZS)
  
  
  ###### Models implemented:

 * Multinomial Naive Bayes 
 * Support Vector Machines 
 * Neural Network with Softmax Layer


###### Sample data

    {
    "short_description": "She left her husband. He killed their children. Just another day in America.",
    "headline" : "There Were 2 Mass Shootings In Texas Last Week, But Only 1 On TV",
    "date" : "2018-05-26",
    "link": "https://www.huffingtonpost.com/entry/texas-amanda-painter-mass-shooting_us_5b081ab4e4b0802d69caad89"
    "authors": "Melissa Jeltsen",
    "category" : "CRIME"
    }


## Content
 Each news headline has a corresponding category.

Categories and corresponding article counts are as follows:

    POLITICS: 32739
    ENTERTAINMENT: 14257
    HEALTHY LIVING: 6694
    QUEER VOICES: 4995
    BUSINESS: 4254
    SPORTS: 4167
    COMEDY: 3971
    PARENTS: 3955
    BLACK VOICES: 3858
    THE WORLDPOST: 3664
    WOMEN: 3490
    CRIME: 2893
    MEDIA: 2815
    WEIRD NEWS: 2670
    GREEN: 2622
    IMPACT: 2602
    WORLDPOST: 2579
    RELIGION: 2556
    STYLE: 2254
    WORLD NEWS: 2177
    TRAVEL: 2145
    TASTE: 2096
    ARTS: 1509
    FIFTY: 1401
    GOOD NEWS: 1398
    SCIENCE: 1381
    ARTS & CULTURE: 1339
    TECH: 1231
    COLLEGE: 1144
    LATINO VOICES: 1129
    EDUCATION: 1004


## Data Cleaning
* The date variable consists of timestamp which may lead to a problem while classifying a text so its better to drop date variable.</P>
* The row 13312 authors variable has '\n' and it will classify authors data into two strings, only if we use \n as a separator. The best way to over come this problem is to impute the authors data without \n.</p>


## Text Classification

###### Feature Extraction Techniques:

* The collection of text documents is converted to a matrix of token counts using count vectorize that produces a sparse representation of the counts.

* TFIDF,term frequency–inverse document frequency, is the statistic that is intended to reflect how important a word is to a document in our corpus. This is used to extract the most meaningful words in the Corpus. 

* Create file data2 which contain all category folders in home direcory to write each text file according to respective category.

###### Description
<p> After the cleaning process the next step is clasification of given text to the form which is familier to all the ML algorithems. The input file is json which can be red easily by pandas package. when we read json file using pandas the file data will be stored in pandas core dataframe. I have converted each observation into separate text file groupped by their respective category folders and the whole data is stored in local file data2. Using glob package each file directory is found, the variables headline, descriptions are joined with space separator and the result is fed to training data dictionary key data. The respective category index is stored in the flag key of training data. Now the training dictionary is converted to dataframea and the collection of text documents is converted to a matrix of token counts using count vectorize that produces a sparse representation of the counts.r. Later this vector data is converted to TF IDF form which can be understood by ML models.</p>
 
###### Packages Required

   * Sklearn
   * Pandas
   * Numpy


## Results

   * Support Vector Machines - 91.8%
   * Neural Network with Softmax Layer - 53%
   * Multinomial Naive Bayes - 35%


   

