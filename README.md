### distilbert-offer-recommender
 Leveraging DistilBERT embeddings and cosine similarity, the recommendations are personalized and accurate. It's all packed in a ready-to-use Flask API for seamless integration. Revolutionize your recommendation 
 Welcome to distilbert-offer-recommender, a powerful system that utilizes natural language processing and advanced embeddings to provide personalized product recommendations based on user input.

##Overview
 Distilbert-offer-recommender combines the power of DistilBERT embeddings and cosine similarity to deliver accurate and context-aware product suggestions. Whether you're looking for specific brands, retailers, or product categories, this recommender system has got you covered.

#How it Works
 #Data Processing: The system processes input data from various sources, including offer-retailer relationships, brand-category mappings, and category information.

 #Text Cleaning: Text data, such as product offers, retailers, and brands, undergoes thorough cleaning to ensure accurate and meaningful embeddings.

 #Embeddings Generation: DistilBERT, a state-of-the-art language model, is employed to generate embeddings for key columns like OFFER, RETAILER, BRAND, PRODUCT_CATEGORY, and IS_CHILD_CATEGORY_TO.

 #API Integration: The entire system is encapsulated into a Flask API, making it easy to integrate into your applications.

 #User Input Processing: The API takes user queries, processes them, and calculates cosine similarity scores between the user input and existing product embeddings.

 #Result Presentation: The API returns a list of top product offers based on similarity scores, providing users with highly relevant recommendations.

##Getting Started
 #Installation: Clone this repository and install the required dependencies using pip install -r requirements.txt.

 #Run Data Processing: Execute pre_processing.py to process and clean the data. This step generates the cleaned_data.csv file.

 #Generate Embeddings: Run main.py to generate embeddings for product offers and save the cleaned data.

 #Start the API: Execute main.py to start the Flask API.

 #Make API Requests: Interact with the API by sending POST requests to http://127.0.0.1:5000/get_top_offers with the user input as a parameter.

##API Endpoint
 #Endpoint: /get_top_offers
 #Method: POST
 #Parameter: user_input (string)
 Example API Request (using cURL)
 #bash
 #Copy code: curl --location 'http://127.0.0.1:5000/get_top_offers?user_input=PLANT'
 #Example API Response:- 

json
Copy code
{
  "success": true,
  "result": [
    {"OFFER": "Offer 1", "Similarity Score": 0.92},
    {"OFFER": "Offer 2", "Similarity Score": 0.85},
    ...
  ]
}


##Acknowledgments
DistilBERT model by Hugging Face: https://huggingface.co/distilbert-base-uncased
Enjoy exploring and enhancing your product recommendation experience with distilbert-offer-recommender!
