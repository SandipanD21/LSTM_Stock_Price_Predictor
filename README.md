# LSTM Time Series Predictor

## Overview

This project implements a Long Short-Term Memory (LSTM) neural network for time series prediction. It's designed to be flexible and scalable, suitable for various time series forecasting tasks such as stock price prediction, weather forecasting, energy consumption prediction, or sales forecasting.

## Features

- Flexible LSTM model architecture configurable via JSON
- Data preprocessing and windowing for sequence prediction
- Multiple training options: in-memory and generator-based for large datasets
- Various prediction methods: point-by-point, multiple sequences, and full sequence
- Result visualization using matplotlib
- Modular design for easy maintenance and extension

## Project Structure

- `run.py`: Main script to run the entire process
- `core/data_processor.py`: Handles data loading and preprocessing
- `core/model.py`: Defines the LSTM model architecture and training/prediction methods
- `core/utils.py`: Utility functions (currently includes a Timer class)
- `config.json`: Configuration file for model architecture and training parameters

## Requirements

- Python 3.x
- TensorFlow 2.x
- Keras
- Pandas
- NumPy
- Matplotlib

Install the required packages using:

pip install tensorflow pandas numpy matplotlib

## Usage

1. Prepare your time series data in CSV format.
2. Modify the `config.json` file to set your desired model architecture and training parameters.
3. Run the main script:

python run.py

## Configuration

The `config.json` file allows you to configure various aspects of the model and training process:

- Data parameters (filename, train/test split, columns to use)
- Model architecture (number and type of layers, neurons, activation functions)
- Training parameters (batch size, epochs)
- Sequence length for prediction

## Customization

- To use your own dataset, update the `filename` in `config.json` and ensure your CSV has the correct format.
- Modify the model architecture in `config.json` to experiment with different LSTM configurations.
- Adjust training parameters in `config.json` to optimize for your specific use case.

## Results

The script will output training progress and final results. Predictions will be plotted against the true data for visual comparison.

