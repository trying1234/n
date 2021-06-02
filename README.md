# Book Recommendation System
### Check Out Our Blog On Book Recommendation Systems Here:
<a href=''>Book Recommendation System</a>
## Description:
<p>A book recommendation system which recommends books based on previous users preferences. </p>
<p>Data used for this project was taken from <a href=''>here</a></p>

### 1. Data Cleaning and Pre-Processing
The data consist of three tables books, users and ratings. Data from all three tables is cleaned and preprocessed separately as:<br><br>
For Books Table:
* Drop all three Image URL features.
* Check for the number of null values in each column. There comes only 3 null values in the table. Replace these three empty cells with ‘Other’.
* Check for the unique years of publications. Two values in year column are publishers. Also, three tuples have the name of the author of the book got merged with the title of the book.Manually set the values for these three above obtained tuples for each of their features using the ISBN number of the book.
* Convert the type of the years of publications feature to the integer.
* By keeping the range of valid years as less than 2022 and obviously not 0, replace all invalid years with the mode of the publications that is 2002.
* Upper-casing all the alphabets present in ISBN column and removal of duplicate rows from the table.

For Users Table:
* Check for null values in the table. The Age column has more than 1 lakh null values.
* Check for unique values present in Age column. There are many invalid ages present like 0 or 244.
* By keeping the valid age range of readers as 10 to 80 replace null values and invalid ages in Age column with the mean of valid ages.
* The location column has 3 values city, state, and country. These are split into 3 different columns named as City, State, and Country respectively. In the case of null value, ‘other’ has been assigned as the entity value.
* Removal of duplicate entries from the table.

For Ratings Table:
* Check for null values in the table.
* Check for Rating column and User-ID column to be integer.
* Removal of punctuation from ISBN column values and if that resulting ISBN is available in the book dataset only then considering else drop that entity.
* Upper-casing all the alphabets present in ISBN column.
* Removal of duplicate entries from the table.
### 2. Algorithms Implemented:
#### 2.1 Popularity Based Recommendation :


* Popular in Whole Collection
* Popular in Given Place
* Books By Same Author, Publisher of Given Book Name
* Popular Books Yearly


#### 2.2 Recommendation using Average Weighted Rating
 	
#### 2.3 User-Item Collaborative Filtering Recommendation
#### 2.4 Correlation Based Recommendation
#### 2.5 Nearest Neighbour Based Recommendation

#### 2.6 Content Based Recommendation
#### 2.7 Hybrid Approach (Collaborative+Content) Recommendation

### 3. Libraries Used:

* ipython-notebook - Python Text Editor
* sklearn - Machine learning library
* seaborn, matplotlib.pyplot, - Visualization libraries
* numpy, scipy- number python library
* pandas - data handling library
