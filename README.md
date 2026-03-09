<<<<<<< HEAD
## Acknowledgements
Rainfall dataset sourced from regional meteorological records.
=======
# RainCast-Multimodal: Dual-Branch Hybrid Neural Network

An advanced deep learning framework that fuses **Computer Vision** and **Time-Series Analysis** to predict urban rainfall. By processing lake surface imagery alongside historical meteorological data, this model achieves high-accuracy forecasting for 24, 48, and 72-hour horizons.

---

## 📌 Project Overview
Traditional forecasting relies heavily on numerical sensors, often missing immediate environmental context. **RainCast-Multimodal** bridges this gap by treating a lake as a natural "sensor." The system analyzes visual disturbances on the lake's surface to determine precipitation states and correlates them with historical duration and intensity data to project future weather patterns.

## 🛠 Tech Stack
* **Deep Learning Frameworks**: Dual implementation in **TensorFlow** and **PyTorch**.
* **Computer Vision**: CNN (Convolutional Neural Networks) for image feature extraction.
* **Sequence Modeling**: RNN (Recurrent Neural Networks) for temporal dependency tracking.
* **Languages & Libraries**: Python, NumPy, Pandas, Scikit-learn, Matplotlib.

---

## 🧠 Model Logic & Architecture
The core of this project is a **Late-Fusion Hybrid Architecture**. Rather than merging raw data at the input layer, the model allows each branch to specialize in its specific data type before combining high-level features for the final prediction.

### 1. The Visual Branch (CNN)
* **Input**: Lake surface images categorized into "Rain" (disturbed surface) and "No-Rain" (calm surface).
* **Logic**: A deep CNN architecture extracts spatial features to identify visual signatures of active precipitation.
* **Outcome**: Provides the "Current State" context to the model.

### 2. The Temporal Branch (RNN)
* **Input**: Time-series CSV data containing historical rainfall duration, intensity, and secondary features.
* **Logic**: Utilizes RNN layers (LSTM/GRU) to model the sequential nature of weather events, identifying how storm intensity builds or dissipates over time.
* **Outcome**: Provides the "Historical Trend" context.



### 3. Multimodal Fusion & Prediction
* **The "Hybrid" Layer**: The feature vectors from both branches are concatenated into a unified dense layer.
* **Forecast Horizons**: The network is trained to output three distinct predictions simultaneously: **24-hour**, **48-hour**, and **72-hour** rainfall forecasts.

---

## 🚀 Key Features
* **Dual-Input Pipeline**: Seamlessly handles both unstructured (images) and structured (CSV) data streams.
* **Comparative Evaluation**: Benchmarked standalone CNN, standalone RNN, and the Hybrid CNN+RNN model to prove that multimodal fusion significantly reduces MSE (Mean Squared Error) for longer 72-hour horizons.
* **Cross-Framework Compatibility**: Full code availability for both TensorFlow and PyTorch environments.
* **Automated Preprocessing**: Custom pipelines for image normalization and sliding-window time-series transformations.

## 📂 Repository Structure
* `preprocessing_modeling/`: Core notebooks for data cleaning, image augmentation, and base model training.
* `day_wise_forecasting/`: Specialized modules for the 24/48/72-hour prediction logic.

---
*Developed by [Chinmay Kulkarni](https://github.com/ckulkarni13)*
>>>>>>> main
