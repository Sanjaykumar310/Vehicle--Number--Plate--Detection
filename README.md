# 🚘 Automatic License Plate Recognition (ALPR) using Docker

This is a complete **AI-powered Automatic License Plate Recognition (ALPR)** system built with Python and OpenCV, packaged with Docker for easy deployment. It performs real-time or image-based number plate detection and character recognition using deep learning and OCR. Ideal for smart surveillance, parking systems, toll booths, or traffic enforcement systems.

---

## 🔧 Tech Stack

### 📦 **Frameworks & Libraries**

* **OpenCV** – Image processing and contour detection
* **Pytesseract** – Optical Character Recognition (OCR)
* **NumPy** – Numerical operations on arrays
* **Matplotlib** – Visualizing intermediate steps (optional)
* **Flask (optional)** – For building a RESTful API (if using web frontend)

### 🐳 **Tools & Platforms**

* **Docker** – Containerized deployment
* **Tesseract OCR** – External dependency for text recognition
* **Git & GitHub** – Version control and collaboration

### 🖥️ **Frontend** (Optional)

* **HTML/CSS/JavaScript** – Simple UI for uploading images (if web-based)
* **Streamlit** – For building an interactive Python dashboard (optional)

### 🔙 **Backend**

* **Python** – Main programming language for image analysis and OCR
* **Flask** – If building as an API backend
* **Docker** – To isolate and deploy the app easily

---

## 📊 Data Collection Process

### 📸 Input Data

* **Images of vehicles** collected from:

  * Google Images
  * Kaggle datasets
  * Real-time camera footage
  * Custom dataset manually labeled for fine-tuning

### 📂 Preprocessing Steps:

* Convert image to grayscale
* Apply noise reduction
* Use edge detection (Canny)
* Find contours and extract number plate region
* Resize and prepare for OCR

---

## ⚙️ Setup & Usage

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/Automatic-License-Plate-Recognition-Docker.git
cd Automatic-License-Plate-Recognition-Docker
```

### 2️⃣ Build and Run with Docker

```bash
docker build -t alpr-app .
docker run -it --rm -v ${PWD}/input:/app/input alpr-app
```

> Make sure to place your vehicle images inside the `input/` folder before running.

---

## 🧠 How It Works

1. **Image Preprocessing**

   * Convert to grayscale
   * Edge detection using Canny
2. **License Plate Detection**

   * Contour analysis to find plate-like regions
3. **OCR Recognition**

   * Tesseract extracts text from the detected plate area

---

## 📁 Folder Structure

```
Automatic-License-Plate-Recognition-Docker/
├── Dockerfile
├── app.py
├── input/            # Folder to store input images
├── output/           # Detected plates and extracted text
├── requirements.txt
└── README.md
```

---

## 🔧 Requirements (for local run without Docker)

* Python 3.x
* OpenCV
* Pytesseract
* Tesseract OCR (installed on system)

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## 📷 Example

Input Image: `input_car.jpg`

Detected Plate Output: `TN01AB1234`

(Optional: Add image examples in the repo's `examples/` folder.)

---

## 🛡️ Use Cases

* Smart Parking Management Systems
* Toll Booth Automation
* Traffic Rule Enforcement
* Access Control in Secure Zones
* RTO Vehicle Verification


---

## 📝 License

This project is open-source and available under the [MIT License](LICENSE).
