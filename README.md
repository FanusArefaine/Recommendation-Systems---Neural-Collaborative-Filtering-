# Recommendation-Systems---Neural-Collaborative-Filtering

# Recommendation-Systems---Neural-Collaborative-Filtering-


    ## 1.0	Model Selection

        In this project, a Deep Learning collaborative filtering based on a Neural Collaborative Filtering paper https://arxiv.org/abs/1708.05031 is used to             build a recommendation system.

    ## 2.0 Model Configuration

        The introduction of Deep Learning model into recommendation system helps to express complex nonlinear relationship among latent features. Based on the           idea to capture linear and nonlinear relationships of latent features, Generalized Matrix Factorization (GCF) and Multi-Layer Perceptron (MLP) are used           to build the recommendation system network.  

        In this project, I am using the following three model configurations:

            1.	Generalized Matrix Factorization (GCF) model only as a recommendation system.

            2.	Multi-Layer Perceptron (MLP) model only as a recommendation system. 

            3.	Combination of both Generalized Matrix Factorization (GCF) and Multi-Layer Perceptron (MLP) as a recommendation system. 

        The implementation of all three systems are based on previous tested models. Loading the dataset followed by building helping functions and all three model configurations are properly illustrated on the implementation.


    3.0 Dataset

	    For this project, I used a Steam Video Game and Bundle Data. The dataset has the following statistics: 

        -	Reviews: 7,793, 069 
        -	Users: 2,567, 538
        -	Items: 15,474
        -	Bundles: 615

        The dataset is divided into different versions and categories. For this project, I worked on Version 1 – User and Item Data found at         [http://deepx.ucsd.edu/public/jmcauley/steam/australian_users_items.json.gz].

        The dataset is a record of 88,310 users watching steam video games of their preferences. There are a total number of steam video games 7851. 



    4.0	Model Evaluation

        I am using top 10 recommendation results as an evaluation metric. To evaluate the model based on top 10 recommendations, I followed the steps below: 

        -	For each user, I picked 100 steam video games not played by the respective user as test negatives.
        -	For each user, I picked 1 steam video game played by the respective user as a holdout. 
        -	For each user, generate top 10 recommendations
        -	For each user, examine if the holdout is included in the top 10 recommendations
        -	Finally, evaluate the model based on how many holdout steam video games are included in top 10 recommendations for all the users. 

        Due to their underlying differences, it is natural for these three model configurations to have different performance. Here is how each model performed: 
