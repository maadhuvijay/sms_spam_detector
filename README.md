## SMS Spam Detector

This project is to refactor the code from an SMS text classification solution into a function that constructs a linear Support Vector Classification (SVC) model. Once the model is created and trained, a Gradio app is created to host the application, enabling users to test text messages. The application will then provide feedback to users, indicating whether the text is classified as spam or not, based on the model's performance.

### Program modules
1. #### Create the SMS Classification Function
   This function takes a DataFrame with 'text_message' and 'label' columns, splits the data into
    training and testing sets, builds a pipeline with TF-IDF vectorization and Linear Support Vector
    Classification, and fits the model to the training data. 
    The fitted pipeline is returned to make future predictions.

2.  #### Create the SMS Prediction Function
     This function takes a text message and a pre-trained pipeline model, then predicts the
      spam/ham classification of the text. The result is a message stating whether the text is
      classified as spam or not.
   
3.  #### Create the Gradio Interface Application
     This module creates a sms_app that takes a textbox for the inputs and has a textbox for the output.
