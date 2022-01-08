# Movie_Recommendation

**Project Domain**: Entertainment, Movies.

**Tools used**: Python and Tableau

**Type of Algorithms used**: NearestNeightbors

**Project Summary**: The objective of this project is to create a movie recommendation system.

**Details about the Datasets**:
  - We will use three different Datasets.
  - The first of them ('ratings1m.dat'), consists of 1 million movie reviews. 
  - For each line, 4 different details are provided: 
    - **"User ID"** (every unique ID represents an user),
    - **"Item ID"** (every unique ID represents a movie),
    - **"Rating"** (from 1 to 5).
    - **"Time Stamp"** (will not be used in our analysis).
  - In the beginning of our analysis, we will reduce this Dataset, by only considering the Top 100 movies by count of reviews.
  - This Dataset will be later joined to another Dataset, that contains the name (**Peli_Name**) and Year of Release (**Year**) for every movie.
  - Finally, we will join the refininf Dataset with an Excel file containing the Genres (**Genre_1**, **Genre_2** and **Genre_3**) for each movie.


**Libraries used for Data Preparation**: pandas, numpy, matplotlib.pyplot, and sklearn.model_selection (train_test_split).
  
**Libraries used for Model Creation**: sklearn.neighbors (NearestNeighbors) and sklearn.metrics (mean_squared_error).

**Details about the model**:
  - For the 100 movies contained in our Dataset, we will create a Distance Matrix, using NearestNeighbors.
  - The field **recommended_value** will initially show the cosine distance between different movies. 
  - When we select a movie as our favourite (in **Tableau**, the recommendation system will show watch the movies with the shortest distance).
  - We will also use the Genre related fields to look for coincidences between movies. Every coincidence will also reduce the **recommended_value** between the different pair of movies.
  
**Details about the output**
  - As an output, we have an excel file called 'movies_final_1M_.xlsx'.
  - It contains the following columns:
    - **'Peli Name'** (this is the movie for which we will make a recommendation).
    - **'Year'** (year of the movie for which we will make a recommendation).
    - **'Peli Original'** (Item ID for the movie for which we will make a recommendation)
    - **'recommended_name'** (recommended movie).
    - **'recommended_year'** (year of the recommended movie).
    - **'recommended_movie'** (Item ID for the recommended movie).
    - **'recommended_value'** (calculated distance between both movies. The smaller the distance, the stronger the recommendation).
    - **'Position'** (based on 'recommended_value').

**Tableau**
  - After working our file in Tableau, we can build the following Dashboard.
  - In the example below, we select the movie  Alien (1979), and we get a recommendation to watch Total Recall (1990), Terminator 2: Judgement Day (1991) and Independence Day (1996).

![image](https://user-images.githubusercontent.com/89322259/148655973-b34e3353-3289-4ce5-b660-3e549a2bfd3b.png)

**Link to Dashboard:** https://public.tableau.com/app/profile/agustin.portilla/viz/MoviesRecommendationSystem/Dashboard1

    
      




