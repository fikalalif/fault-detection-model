# GeoValid - Fault & Breccia Detection Model

**GeoValid Detection Model** is the core computer vision component of the GeoValid project. It utilizes deep learning, specifically a DeepLabV3+ architecture, to perform semantic segmentation on geological images, accurately detecting faults and breccia. 

## 🚀 Features

* **Semantic Segmentation:** Generates precise `mask.png` and `overlay.png` outputs to visualize geological faults.
* **Model Inference:** Standalone inference script (`infer.py`) for processing images through the trained model.
* **API Integration:** Built-in application backend (`app.py`) powered by FastAPI for seamless communication with frontend and database services.
* **Custom Dataset Handling:** Dedicated utilities (`dataset_class.py`, `check_dataset.py`) for robust data loading and validation.

## 🛠️ Tech Stack

* **Language:** Python
* **Machine Learning:** PyTorch (DeepLabV3+)
* **API Framework:** FastAPI
* **Computer Vision:** OpenCV / PIL (for mask and overlay generation)

## 📂 Project Structure

* `app.py`: Main API application entry point.
* `model.py`: Defines the neural network architecture.
* `infer.py`: Handles model inference and saves segmentation outputs.
* `dataset_class.py`: Custom dataset class for managing the geological imagery.
* `check_dataset.py`: Utility script to validate and verify dataset integrity.
* `output/`: Directory containing generated inference results, structured by unique IDs.

## ⚙️ Getting Started

### Prerequisites
* Python 3.8+
* A CUDA-compatible GPU (recommended for training and fast inference)

### Installation

1.  Clone this repository.
2.  Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3.  Run the API server:
    ```bash
    uvicorn app:app --host 0.0.0.0 --port 8000
    ```
4.  To run standalone inference:
    ```bash
    python infer.py
    ```

## 🧑‍💻 Developer

**Fikal Alif Al Amin**

## 📄 License

See the `LICENSE` file for more details.
