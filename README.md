**MRI Classification - T1, T2, FLAIR Segregation**
This repository contains code for classifying Magnetic Resonance Imaging (MRI) scans into their respective modalities (T1, T2, FLAIR).

**Features:**
Classifies MRI scans using a Convolutional Neural Network (CNN) built with TensorFlow.
Stores classified scans in a PostgreSQL database (psql).

**Requirements:**
Python 3.x
TensorFlow
psycopg2 (for interacting with PostgreSQL)

**Data:**
Due to data privacy restrictions, the dataset cannot be included in this repository.
The code assumes your dataset is pre-processed and organized appropriately.

## MRI Classification Workflow

This project demonstrates a workflow for classifying MRI images using deep learning and storing results in a PostgreSQL database. The process includes:

### 1. DICOM File Handling
- Read DICOM files from a specified directory structure, organized by MRI sequence type (e.g., T1, T2, FLAIR).
- Count and optionally process specific DICOM files.
- Extract image resolution and display images using matplotlib.

### 2. Data Preprocessing
- Normalize pixel data (min-max scaling).
- Resize images to a fixed size (256x256) using PIL or OpenCV.
- Organize images and labels for each sequence type.

### 3. Model Training
- Split data into training and validation sets.
- Build a Convolutional Neural Network (CNN) using TensorFlow/Keras.
- Train the model to classify MRI sequence types (T1, T2, FLAIR).
- Evaluate model performance (accuracy, loss).

### 4. Database Storage
- Store processed images and labels in PostgreSQL tables (T1, T2, FLAIR).
- Use BYTEA format for image data.
- Provide scripts to check table record counts and retrieve images from the database.

### 5. Image Retrieval
- Fetch and display images from PostgreSQL using PIL.
- Save images to disk if needed.

---

#### Requirements
- Python 3.x
- Libraries: pydicom, numpy, tensorflow, scikit-learn, PIL, psycopg2, matplotlib
- PostgreSQL server

#### Usage
1. Update paths and database credentials in the notebook/code as needed.
2. Run the notebook cells in order to process DICOM files, train the model, and store/retrieve images from the database.
3. Review code comments for customization and troubleshooting.
