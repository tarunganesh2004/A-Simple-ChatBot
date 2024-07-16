# Chatbot with TensorFlow and tflearn

This repository contains a simple chatbot built using TensorFlow and tflearn. The chatbot uses Natural Language Processing (NLP) techniques to understand user queries and respond appropriately.

## Features

- Responds to greetings, thanks, and goodbyes
- Provides information about hours of operation, location, and payment options
- Specializes in daily menu and delivery options

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Intents File](#intents-file)
- [Model Training](#model-training)
- [Running the Chatbot](#running-the-chatbot)
- [License](#license)

## Installation

### Prerequisites

- Python 3.x
- TensorFlow 1.15
- tflearn
- nltk
- numpy
- json

### Installation Steps

1. Clone the repository:

    ```bash
    git clone https://github.com/tarunganesh2004/A-Simple-ChatBot.git
    cd A-Simple-ChatBot
    ```

2. Install the required Python packages:

    ```bash
    pip install tensorflow==1.15.0 tflearn nltk numpy
    ```

3. Download NLTK data:

    ```python
    import nltk
    nltk.download('punkt')
    ```

## Usage

1. Upload the `intents.json` file:

    - This file contains predefined patterns and responses.

2. Run the `Chatbot.ipynb` Jupyter notebook in Google Colab or locally to train the model and interact with the chatbot.

## Intents File

The `intents.json` file defines the different categories of user intents and their associated patterns and responses. Below is an example structure of the `intents.json` file:

```json
{
  "intents": [
    {
      "tag": "greeting",
      "patterns": ["Hi", "How are you", "Is anyone there?", "Hello", "Good day"],
      "responses": ["Hello, thanks for visiting", "Good to see you again", "Hi there, how can I help?"],
      "context_set": ""
    },
    {
      "tag": "goodbye",
      "patterns": ["Bye", "See you later", "Goodbye"],
      "responses": ["See you later, thanks for visiting", "Have a nice day", "Bye! Come back again soon."]
    },
    {
      "tag": "thanks",
      "patterns": ["Thanks", "Thank you", "That's helpful"],
      "responses": ["Happy to help!", "Any time!", "My pleasure"]
    },
    {
      "tag": "hours",
      "patterns": ["What hours are you open?", "What are your hours?", "When are you open?"],
      "responses": ["We're open every day 9am-9pm", "Our hours are 9am-9pm every day"]
    },
    {
      "tag": "location",
      "patterns": ["What is your location?", "Where are you located?", "What is your address?", "Where is your restaurant situated?"],
      "responses": ["We are on the intersection of London Alley and Bridge Avenue.", "We are situated at the intersection of London Alley and Bridge Avenue", "Our Address is: 1000 Bridge Avenue, London EC3N 4AJ, UK"]
    },
    {
      "tag": "payments",
      "patterns": ["Do you take credit cards?", "Do you accept Mastercard?", "Are you cash only?"],
      "responses": ["We accept VISA, Mastercard and AMEX", "We accept most major credit cards"]
    },
    etc
}
```
## Model Training

The `Chatbot.ipynb` notebook contains the complete code for:

- Importing and processing the data
- Building and training the neural network model
- Saving the trained model

## Running the Chatbot

After training the model, you can interact with the chatbot by calling the `response` function with different inputs.

```python
response('Hi')
response('What is the menu for today?')
response('Do you accept credit cards?')
```

## LICENSE

- This project is licensed under the MIT License 
