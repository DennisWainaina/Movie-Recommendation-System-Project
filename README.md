## TABLE OF CONTENTS
1. [BUSINESS UNDERSTANDING](#1-business-understanding)
   - 1.1 [INTRODUCTION](#1.1-introduction)
   - 1.2 [OBJECTIVES](#1.2-objectives)
   - 1.3 [PROBLEM STATEMENT](#1.3-problem-statement)
   - 1.4 [MEASURE OF SUCCESS](#1.4-measure-of-success)

<br>

2. [DATA UNDERSTANDING](#2-data-understanding)

   - 2.0 [GENERAL STATEMENT](#2.0-general-statement)
   - 2.1 [RATINGS](#2.1-ratings)
   - 2.2 [MOVIES](#2.2-movies)
   - 2.3 [LINKS](#2.3-links)
   - 2.4 [TAGS](#2.4-tags)

&nbsp;

3. [DATA PREPARATION](#3-data-preparation)

   - 3.1 [COMBINING DATAFRAME USING COMMON KEY](#3.1-combining-dataframe-using-common-key)
   - 3.2 [MISSING VALUES](#3.2-missing-values)
   - 3.3 [CHECKING FOR DUPLICATES](#3.3-checking-for-duplicates)
   - 3.4 [CREATING A NEW YEAR COLUMN FROM THE TITLE COLUMN OF THE DATAFRAME](#3.4-creating-a-new-year-column-from-the-title-column-of-the-dataframe)
   - 3.5 [CHECKING FOR WRONG DATATYPES](#3.5-checking-for-wrong-datatypes)
   - 3.6 [CHECKING FOR OUTLIERS](#3.6-checking-for-outliers)
   - 3.7 [FEATURE ENGINEERING](#3.7-feature-engineering) 

&nbsp;

4. [EXPLORATORY DATA ANALYSIS](#4-exploratory-data-analysis)

   - 4.1 [UNIVARIATE ANALYSIS](#4.1-univariate-analysis)
   
     - 4.1.1 [NUMBER OF MOVIES RELEASED EVERY YEAR](#4.1.1-number-of-movies-released-every-year)
     - 4.1.2 [NUMBER OF MOVIES FOR EACH GENRE RELEASED](#4.1.2-number-of-movies-for-each-genre-released)
     - 4.1.3 [WHAT IS THE DISTRIBUTION OF THE NUMBER OF RATINGS BY USERS](#4.1.3-what-is-the-distribution-of-the-number-of-ratings-by-users)
     - 4.1.4 [IS THERE A RELATION BETWEEN THE AGE OF A MOVIE AND THE CHANCES OF IT BEING RATED](#4.1.4-is-there-a-relation-between-the-age-of-a-movie-and-the-chances-of-it-being-rated)
     - 4.1.5 [WHAT IS THE DISTRIBUTION OF RATINGS IN THIS DATASET](#4.1.5-what-is-the-distribution-of-ratings-in-this-dataset)
   
   &nbsp;
   
   - 4.2 [BIVARIATE ANALYSIS](#4.2-bivariate-analysis)

     - 4.2.1 [IS THERE A CORRELATION BETWEEN THE RELEASE YEAR OF MOVIES AND THEIR AVERAGE RATINGS](#4.2.1-is-there-a-correlation-between-the-release-year-of-movies-and-their-average-ratings)
     - 4.2.2 [HOW DO USER RATINGS DIFFER BETWEEN DIFFERENT MOVIE GENRES](#4.2.2-how-do-user-ratings-differ-between-different-movie-genres)
     - 4.2.3 [HOW HAVE USER RATINGS FOR A PARTICULAR GENRE EVOLVED OVER THE YEARS](#4.2.3-how-have-user-ratings-for-a-particular-genre-evolved-over-the-years)
     
&nbsp;

5. [MODELLING](#5-modelling)

   - 5.1 [BASE MODEL](#5.1-base-model)
   - 5.2 [MODEL 2](#5.2-model-2)
   - 5.3 [MODEL 3](#5.3-model-3)
   - 5.4 [MODEL 4](#5.4-model-4)
   - 5.5 [MODEL 5](#5.5-model-5)

&nbsp;

6. [CONCLUSION](#6-conclusion)

&nbsp;

7. [RECOMMENDATIONS](#7-recommendations)
