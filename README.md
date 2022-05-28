# Cinemagus

Cinemagus is a Movie Recommendation Webiste which recommends movies similar to the movie the user searched and analyses the sentiments on the reviews given by the user for that movie.

![Python](https://img.shields.io/badge/Python-3.10-green) 
![Framework](https://img.shields.io/badge/Framework-Flask-red)
![Frontend](https://img.shields.io/badge/Frontend-HTML/CSS/JS-yellow)
![API](https://img.shields.io/badge/API-TMDB-blue)


## Screenshots

![FrontPage](https://github.com/sreoshee-17/cinemagus/blob/main/Movie%20Recommendation%20Project/Screenshot%20(1).png)
![Searching](https://github.com/sreoshee-17/cinemagus/blob/main/Movie%20Recommendation%20Project/Screenshot%20(2).png)
![Searched Result](https://github.com/sreoshee-17/cinemagus/blob/main/Movie%20Recommendation%20Project/Screenshot%20(3).png)
![Top Cast](https://github.com/sreoshee-17/cinemagus/blob/main/Movie%20Recommendation%20Project/Screenshot%20(4).png)
![User Reviews](https://github.com/sreoshee-17/cinemagus/blob/main/Movie%20Recommendation%20Project/Screenshot%20(5).png)
![Recommended Movies For You](https://github.com/sreoshee-17/cinemagus/blob/main/Movie%20Recommendation%20Project/Screenshot%20(6).png)

## API Reference

The details of the movies(title, genre, runtime,rating, poster, etc) are fetched using an API by TMDB, https://www.themoviedb.org/documentation/api
and using the IMDB id of the movie in the API, I performed web scraping to get the reviews given in the IMDB site using `beautifulsoup4` and performed sentiment analysis on those reviews.

## How to get the API Key?

Create an account in https://www.themoviedb.org/, click on the `API` link from the left hand sidebar in your account settings and fill all the details to apply for API key. If you are asked for the website URL, just give "NA" if you don't have one. You will see the API key in your `API` sidebar once your request is approved.
## How to Run this Project?

1. Clone or download this repository to your local machine.
2. Install all the libraries mentioned in the [requirements.txt](https://github.com/sreoshee-17/cinemagus) file with the command `pip install -r requirements.txt`
3. Get your API key from https://www.themoviedb.org/. (Refer the above section on how to get the API key)
3. Replace YOUR_API_KEY in **both** the places (line no. 15 and 29) of `static/recommend.js` file and hit save.
4. Open your terminal/command prompt from your project directory and run the file `main.py` by executing the command `python main.py`.
5. Go to your browser and type `http://127.0.0.1:5000/` in the address bar.
6. Hurray! That's it.
## Architecture

![IMG-20210306-WA0012](https://user-images.githubusercontent.com/36665975/110212434-597bb700-7ec1-11eb-9ffa-7ac319e33123.jpg)
## Similarity Score

How does it decide which item is most similar to the item user likes? Here we use the similarity scores.
   
   It is a numerical value ranges between zero to one which helps to determine how much two items are similar to each other on a scale of zero to one. This similarity score is obtained measuring the similarity between the text details of both of the items. So, similarity score is the measure of similarity between given text details of two items. This can be done by cosine-similarity.
## How does Cosine Similarity work?

Cosine similarity is a metric used to measure how similar the documents are irrespective of their size. Mathematically, it measures the cosine of the angle between two vectors projected in a multi-dimensional space. The cosine similarity is advantageous because even if the two similar documents are far apart by the Euclidean distance (due to the size of the document), chances are they may still be oriented closer together. The smaller the angle, higher the cosine similarity.
  
  ![image](https://user-images.githubusercontent.com/36665975/70401457-a7530680-1a55-11ea-9158-97d4e8515ca4.png)

More about Cosine Similarity : [Understanding the Math behind Cosine Similarity](https://www.machinelearningplus.com/nlp/cosine-similarity/)
## Sources of Datasets

1. [IMDB 5000 Movie Dataset](https://www.kaggle.com/carolzhangdc/imdb-5000-movie-dataset)
2. [The Movies Dataset](https://www.kaggle.com/rounakbanik/the-movies-dataset)
3. [List of movies in 2018](https://en.wikipedia.org/wiki/List_of_American_films_of_2018)
4. [List of movies in 2019](https://en.wikipedia.org/wiki/List_of_American_films_of_2019)
5. [List of movies in 2020](https://en.wikipedia.org/wiki/List_of_American_films_of_2020)

