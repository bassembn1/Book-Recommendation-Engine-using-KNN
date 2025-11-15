# Book-Recommendation-Engine-using-KNN
This project builds a simple book recommendation system using the K-Nearest Neighbors (KNN) algorithm. The goal is to recommend books that are similar to a selected book based on user ratings. irst, the project loads three datasets: books, users, and ratings. Then, it cleans the data by keeping only users and books with enough ratings to ensure better recommendations. After that, it creates a pivot table where each row represents a book and each column represents a user, with the ratings as values.

Using this matrix, the KNN model finds books that are most similar to the chosen book by measuring the cosine distance between rating vectors. Finally, the system returns a list of recommended books along with their similarity scores.

This project demonstrates basic concepts in machine learning, data preprocessing, and building a recommendation engine using Python and scikit-learn.

After going to that link, create a copy of the notebook either in your own account or locally. Once you complete the project and it passes the test (included at that link), submit your project link below. If you are submitting a Google Colaboratory link, make sure to turn on link sharing for "anyone with the link."

We are still developing the interactive instructional content for the machine learning curriculum. For now, you can go through the video challenges in this certification. You may also have to seek out additional learning resources, similar to what you would do when working on a real-world project.

In this challenge, you will create a book recommendation algorithm using K-Nearest Neighbors.

In this project, you will use the Book-Crossings dataset, which contains 1.1 million ratings (scale of 1-10) of 270,000 books by 90,000 users. The dataset is already imported in the notebook, so no additional download is required.

Use NearestNeighbors from sklearn.neighbors to develop a model that shows books that are similar to a given book. The Nearest Neighbors algorithm measures the distance to determine the “closeness” of instances.

Create a function named get_recommends that takes a book title (from the dataset) as an argument and returns a list of 5 similar books with their distances from the book argument.

This code:

get_recommends("The Queen of the Damned (Vampire Chronicles (Paperback))")

should return:

[
  'The Queen of the Damned (Vampire Chronicles (Paperback))',
  [
    ['Catch 22', 0.793983519077301], 
    ['The Witching Hour (Lives of the Mayfair Witches)', 0.7448656558990479], 
    ['Interview with the Vampire', 0.7345068454742432],
    ['The Tale of the Body Thief (Vampire Chronicles (Paperback))', 0.5376338362693787],
    ['The Vampire Lestat (Vampire Chronicles, Book II)', 0.5178412199020386]
  ]
]

Notice that the data returned from get_recommends() is a list. The first element in the list is the book title passed into the function. The second element in the list is a list of five more lists. Each of the five lists contains a recommended book and the distance from the recommended book to the book passed into the function.

If you graph the dataset (optional), you will notice that most books are not rated frequently. To ensure statistical significance, remove from the dataset users with less than 200 ratings and books with less than 100 ratings.
