# News-Category-Prediction-

## Problem Statement 
  Build a ML model in python that can Identify the category of news based on headlines and short descriptions.

## Data 
  This dataset contains around 125k news headlines from the year 2013 to 2018 obtained from HuffPost.

<p>Sample data</p>


<p>{<p/>
   <p> "short_description": "She left her husband. He killed their children. Just another day in America.",</p>
    <p>"headline" : "There Were 2 Mass Shootings In Texas Last Week, But Only 1 On TV",</p>
    <p>"date" : "2018-05-26",</p>
    <p>"link": "https://www.huffingtonpost.com/entry/texas-amanda-painter-mass-shooting_us_5b081ab4e4b0802d69caad89"</p>
    <p>"authors": "Melissa Jeltsen",</p>
    <p>"category" : "CRIME"<p/></P>
<p>}</p>

## Content
<p>Each news headline has a corresponding category.</p>

<p>Categories and corresponding article counts are as follows:</p>

   <p>POLITICS: 32739</p>
   <p>ENTERTAINMENT: 14257</p>
   <p>HEALTHY LIVING: 6694</p>
   <p>QUEER VOICES: 4995</p>
   <p>BUSINESS: 4254</p>
   <p>SPORTS: 4167</p>
   <p>COMEDY: 3971</p>
   <p>PARENTS: 3955</p>
   <p>BLACK VOICES: 3858</p>
   <p>THE WORLDPOST: 3664</p>
   <p>WOMEN: 3490</p>
   <p>CRIME: 2893</p>
   <p>MEDIA: 2815</p>
   <p>WEIRD NEWS: 2670</p>
   <p>GREEN: 2622</p>
   <p>IMPACT: 2602</p>
   <p>WORLDPOST: 2579</p>
   <p>RELIGION: 2556</p>
   <p>STYLE: 2254</p>
   <p>WORLD NEWS: 2177</p>
   <p>TRAVEL: 2145</p>
   <p>TASTE: 2096</p>
   <p>ARTS: 1509</p>
   <p>FIFTY: 1401</p>
   <p>GOOD NEWS: 1398</p>
   <p>SCIENCE: 1381</p>
   <p>ARTS & CULTURE: 1339</p>
   <p>TECH: 1231</p>
   <p>COLLEGE: 1144</p>
   <p>LATINO VOICES: 1129</p>
   <p>EDUCATION: 1004</p>

## Data Cleaning
<p> 1. The date variable consists of timestamp which may lead to a problem while classifying a text so its better to drop date variable.</P>
<p> 2. The row 13312 authors variable has '\n' and it will classify authors data into two strings, only if we use \n as a separator. The best way to over come this problem is to impute the authors data by removing \n.</p>

## 

## Text Classification

###### Feature Extraction Techniques:
The collection of text documents is converted to a matrix of token counts using count vectorize that produces a sparse representation of the counts.

TFIDF,term frequency–inverse document frequency, is the statistic that is intended to reflect how important a word is to a document in our corpus. This is used to extract the most meaningful words in the Corpus. 

###### Description
<p> After the cleaning process the next step is to clasification of given text to the form which is familier for all the ML algorithems. The input file is json which can be red easily by pandas library. when we read json file using pandas the file data will be stored in pandas core dataframe. I have converted each observation into separate text file groupped by their respective category folders and the whole data is stored in local file data2. Using glob library each file directory is found, the variables headline, descriptions are joined with space separator and the result it fed to training data dictionary key data. The respective category index is stored in the flag key of training data. Now the training dictionary is converted to dataframea and the collection of text documents is converted to a matrix of token counts using count vectorize that produces a sparse representation of the counts.r. Later this vector data is converted to TF IDF form which can be understood by ML models.
  
   

