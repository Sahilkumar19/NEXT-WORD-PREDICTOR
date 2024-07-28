# Next Word Prediction with LSTM

This project demonstrates how to create a next word prediction model using an LSTM (Long Short-Term Memory) neural network. The model is trained on a given corpus of text data and predicts the next word in a sequence. The project uses TensorFlow and Keras for building the model, and Streamlit for creating a simple web interface to interact with the model.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Model Training](#model-training)
- [Running the App](#running-the-app)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/Sahilkumar19/NEXT-WORD-PREDICTOR.git
    cd NEXT-WORD-PREDICTOR
    ```

2. Create a virtual environment and activate it:

    ```bash
    python -m venv venv
    source venv/bin/activate   # On Windows use `venv\Scripts\activate`
    ```

3. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

## Usage

### Model Training

1. Use hamlet.txt to train the model I have downloaded this from NLTK itself.

2. Run the training script:

    ```bash
    python experiments.py
    ```

    This script will preprocess the data, train the LSTM model, and save the trained model (`next_word_lstm.h5`) and tokenizer (`tokenizer.pickle`) to disk.

### Running the App

1. Ensure the model and tokenizer files (`next_word_lstm.h5` and `tokenizer.pickle`) are in the root directory.

2. Run the Streamlit app:

    ```bash
    streamlit run app.py
    ```

    This will start a web server and open a web interface where you can input a sequence of words and get the predicted next word.


## Model Training

The model training process involves the following steps:

1. **Data Preprocessing:** The text data is tokenized and converted into sequences of word indices. These sequences are then padded to ensure uniform length.

2. **Model Definition:** An LSTM model is defined using Keras, consisting of embedding, LSTM, dropout, and dense layers.

3. **Model Training:** The model is trained on the preprocessed data using categorical cross-entropy loss and the Adam optimizer.

4. **Model Saving:** The trained model and tokenizer are saved to disk for later use in prediction.

## Running the App

The Streamlit app provides a simple web interface for interacting with the trained model. Users can input a sequence of words, and the app will display the predicted next word based on the input.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request to contribute to this project.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.


