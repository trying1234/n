# Book Recommendation System
### Check Out Our Blog On Book Recommendation System Here:
<a href=https://ashima96.medium.com/building-a-book-recommendation-system-a98c58a4f1bb>Book Recommendation System</a>
## Description:
<p>A Book Recommendation System which recommends the users a selection of books based on their interests.</p>
<p>Data used for this project was taken from <a href=http://www2.informatik.uni-freiburg.de/~cziegler/BX/>here</a></p>

### 1. Data Cleaning and Pre-Processing
The dataset consists of three tables; Books, Users, and Ratings. Data from all three tables are cleaned and preprocessed separately as defined below briefly:<br><br>
For Books Table:
* Drop all three Image URL features.
* Check for the number of null values in each column. There comes only 3 null values in the table. Replace these three empty cells with ‘Other’.
* Check for the unique years of publications. Two values in the year column are publishers. Also, three tuples have the name of the author of the book got merged with the title of the book. Manually set the values for these three above obtained tuples for each of their features using the ISBN of the book.
* Convert the type of the years of publications feature to the integer.
* By keeping the range of valid years as less than 2022 and not 0, replace all invalid years with the mode of the publications that is 2002.
* Upper-casing all the alphabets present in the ISBN column and removal of duplicate rows from the table.

For Users Table:
* Check for null values in the table. The Age column has more than 1 lakh null values.
* Check for unique values present in the Age column. There are many invalid ages present like 0 or 244.
* By keeping the valid age range of readers as 10 to 80 replace null values and invalid ages in the Age column with the mean of valid ages.
* The location column has 3 values city, state, and country. These are split into 3 different columns named; City, State, and Country respectively. In the case of null value, ‘other’ has been assigned as the entity value.
* Removal of duplicate entries from the table.

For Ratings Table:
* Check for null values in the table.
* Check for Rating column and User-ID column to be an integer.
* Removal of punctuation from ISBN column values and if that resulting ISBN is available in the book dataset only then considering else drop that entity.
* Upper-casing all the alphabets present in the ISBN column.
* Removal of duplicate entries from the table.

### 2. Algorithms Implemented:
#### 2.1 Popularity Based Recommendation :

* ##### Popular in the Whole Collection <br>
We have sorted the dataset according to the total ratings each of the books have received in non-increasing order and then recommended top n books.

* ##### Popular at a Given Place <br>
The dataset was filtered according to a given place (city, state, or country) and then sorted it according to total ratings they have received by the users in decreasing order of that place and recommended top n books.

* ##### Books By the Same Author, Publisher of Given Book Name <br>
For this model we have sorted the books by rating for the same author and same publisher of given book and recommended top n books.

* ##### Popular Books Yearly <br>
This is the most basic model in which we have grouped all the books published in the same year and recommended the top-rated book yearly.

#### 2.2 Recommendation using Average Weighted Rating
We have calculated the weighted score using the below formula, of all the books and recommended the books with the highest score. <br>
score= t/(t+m)∗a + m/(m+t)∗c <br>
where, <br>
t represents the total number of ratings received by the book <br>
m represents the minimum number of total ratings considered to be included <br>
a represents the average rating of the book and, <br>
c represents the mean rating of all the books. 
 	
#### 2.3 User-Item Collaborative Filtering Recommendation

#### 2.4 Correlation Based Recommendation

#### 2.5 Nearest Neighbour Based Recommendation

#### 2.6 Content Based Recommendation
#### 2.7 Hybrid Approach (Collaborative+Content) Recommendation

### 3. Libraries Used:

* ipython-notebook - Python Text Editor
* sklearn - Machine learning library
* seaborn, matplotlib - Visualization libraries
* numpy, scipy- number python library
* pandas - data handling library

### 4. Acknowledgements:

Machine Learning Monsoon 2020 (CSE543) @IIIT Delhi
