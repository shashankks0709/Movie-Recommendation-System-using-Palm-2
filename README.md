# Movie-Recommendation-System-using-Palm-2
Google Hackathon

**Introduction**

This Movie Recommendation System takes in the name of a movie and recommends similar movies based on the dataset. The recommendation process is powered by the google. generative-ai(presumably a mock-up API for the purpose of this example), which utilises a generative model to provide movie suggestions.

**Requirements**

* Python libraries:
    * os
    * google.generativeai (You need an API key for this)
    * ipywidgets
    * pandas
    * IPython
* Data: A CSV file named IMDBDataset.csv containing a list of movie names.
  
**Setup**

* Set your PALM API key: You can either set it as an environment variable or directly in the code. python Copy code:  PALM_API_KEY = os.getenv("PALM_API_KEY", "YOUR_API_KEY_HERE") 
* Load the movie dataset: The IMDBDataset.csv file is loaded into a pandas dataframe and then converted to a list of movie names.
  
**Usage**

* Create an instance of the Recommend_movies class.
* Use the generate method to get movie recommendations.
* The interface uses IPython widgets for a simple GUI where users can input a movie name and get recommendations.
  
**Workflow**

* The Recommend_movies class configures the generative AI model with the specified parameters.
* Upon providing a movie name and pressing the button, the model takes a sample prompt with movie names and their corresponding recommendations.
* Based on this prompt, the model tries to predict recommendations for the input movie.
* The generated recommendations are then cross-referenced with the dataset to ensure they are valid.
* The results are displayed using IPython.
  
**Note**

* The safety_settings in the Recommend_movies class aims to prevent any inappropriate or harmful content from being generated.
* If the movie name is not found, the system will prompt the user to try a different name.
  
**Improvements**

* A more extensive dataset will provide better recommendations.
* Fine-tuning the model specifically for movie recommendations can yield better results.
* Incorporate user feedback to continually improve the recommendation quality.
  
**Conclusion**

This recommendation system provides a quick and easy way to find similar movies. With the potential to integrate more advanced features and datasets, this system can be further enhanced to suit various user needs.
