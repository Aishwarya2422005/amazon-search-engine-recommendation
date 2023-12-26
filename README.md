# amazon-search-engine-recommendation
 Let's break down the detailed explanation for the product recommendation in the search engine using the Amazon dataset:

Loading and Preprocessing:

The code begins by loading the Amazon dataset using pandas and removes the 'id' column, which is deemed unnecessary.
Tokenization and Stemming:

The tokenize_and_stem function is defined to tokenize and stem words in the product titles and descriptions using the SnowballStemmer from the NLTK library. This process reduces words to their root form, helping in similarity calculations.
TF-IDF Vectorization:

The TF-IDF (Term Frequency-Inverse Document Frequency) vectorizer (tfidf_vectorizer) is configured with the tokenize_and_stem function. It is used to convert the product titles and descriptions into numerical vectors, representing the importance of each word in the corpus.
Cosine Similarity Calculation:

The cosine_sim function computes the cosine similarity between two sets of tokens. It calculates the similarity between the query and each product in the dataset based on their TF-IDF representations.
Search Function:

The search_products function takes a user query as input, tokenizes and stems it, calculates cosine similarity with each product in the dataset, and sorts the results by similarity. The top 10 products with the highest similarity scores are selected and displayed, including their titles, descriptions, and bullet points.
Streamlit User Interface:

The Streamlit app provides a simple user interface where users can input a product name (query). Upon clicking the 'Search' button, the search_products function is called, and the top 10 most similar products are displayed.
Recommendation Explanation:

The recommendations are based on the cosine similarity between the user's query and the product titles and descriptions in the dataset. Higher similarity scores indicate products that are more closely related to the user's query.
Improvements and Future Work:

To enhance recommendations, future work could involve incorporating more advanced techniques, considering additional product attributes, and obtaining user feedback for iterative improvements.
Overall, the system utilizes natural language processing and vectorization techniques to recommend products that are most relevant to the user's search query, providing a personalized and efficient product search experience on Amazon's dataset.
