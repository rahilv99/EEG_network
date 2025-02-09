# EEG-Based Kinesthenic Imagination Classifier
This project implements an EEGNet model to classify left and right kinesthenic imagination from EEG data.  The model is trained and evaluated using data from the Physionet EEG Motor Movement/Imagery Dataset.

## Features
*   Downloads EEG data from Google Cloud Storage.
*   Preprocesses EEG data including filtering and epoching.
*   Applies Common Spatial Patterns (CSP) for feature extraction.
*   Trains an EEGNet model for classification.
*   Evaluates the model's performance using accuracy.
*   Visualizes CSP patterns and example EEG frequency data.

## Usage
1.  **Authenticate with Google Cloud:**  The notebook requires authentication with your Google Cloud account.  Follow the instructions in the notebook to authenticate.  You'll need a Google Cloud project with appropriate permissions to access the data bucket.
2.  **Install Dependencies:** Install the necessary Python packages using `pip install mne tensorflow`.
3.  **Run the Notebook:** Execute the Jupyter Notebook (`EEG_network.ipynb`).  The notebook will download the data, preprocess it, train the model, and evaluate its performance.
4.  **Unmount Data:** After finishing, unmount the data directory from Google Cloud Storage.

## Installation
1.  **Clone the Repository:** Clone this repository to your local machine using `git clone <repository_url>`.
2.  **Install Dependencies:**  Install the required Python packages listed in the `Dependencies` section.
3.  **Set up Google Cloud:** Ensure you have a Google Cloud project and have configured the necessary authentication credentials.

## Technologies Used
*   **Python:** The primary programming language.
*   **TensorFlow/Keras:** Used for building and training the deep learning model (EEGNet).
*   **MNE-Python:** A powerful Python library for processing EEG data.  Used for data loading, filtering, epoching, and CSP.
*   **Scikit-learn:** Used for data splitting, cross-validation, and Linear Discriminant Analysis (LDA).
*   **NumPy and Pandas:** For numerical computations and data manipulation.
*   **Matplotlib:** For data visualization.
*   **Google Cloud Storage (GCS):** Used for storing and accessing the EEG dataset.
*   **gcsfuse:**  A tool to mount GCS buckets as local file systems.

## Statistical Analysis
The project uses a ShuffleSplit cross-validation strategy to reduce variance in the model's performance evaluation.  Linear Discriminant Analysis (LDA) is used as a classifier in conjunction with Common Spatial Patterns (CSP) for feature extraction.  Model performance is assessed using accuracy.

## Configuration
The model's hyperparameters (e.g., number of epochs, dropout rate, kernel length) can be adjusted within the Jupyter Notebook.

## Dependencies
*   `mne`
*   `tensorflow`
*   `numpy`
*   `pandas`
*   `scikit-learn`
*   `matplotlib`
*   `gcsfuse`

## Contributing
Contributions are welcome! Please open an issue or submit a pull request.

*README.md was made with [Etchr](https://etchr.dev)*