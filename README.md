
# 🏡 California Housing Price Prediction

[![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)](https://www.python.org/)
[![Dockerized](https://img.shields.io/badge/Dockerized-Yes-blue?logo=docker)](https://www.docker.com/)
[![CI/CD](https://img.shields.io/badge/CI%2FCD-GitHub%20Actions-blue?logo=github)](https://github.com/shreeyanshm/California-Housing/actions)
[![Deployed](https://img.shields.io/badge/Deployed-Render-green?logo=render)](https://california-housing-73yr.onrender.com/)

> A complete end-to-end ML project to predict California housing prices using linear regression. Built with MLOps practices including Docker, FastAPI, and GitHub Actions for CI/CD.

---

## 🚀 Demo

Try the deployed API (if available):  
**[🔗 Live Endpoint →](https://california-housing-73yr.onrender.com/)**

Example:  
GET /predict?MedInc=8.3&HouseAge=32&AveRooms=6.1&AveBedrms=1.1&Population=1200&AveOccup=2.8&Latitude=36.4&Longitude=-120.3

---

## 📁 Project Structure

```
.
├── app/
│   ├── main.py          # FastAPI app with prediction endpoint
│   ├── model.pkl        # Trained regression model
│   └── utils.py         # Utility functions for prediction
├── Dockerfile           # Containerization setup
├── requirements.txt     # Python dependencies
├── .github/workflows/   # GitHub Actions CI/CD pipeline
└── README.md            # Project documentation
```

---

## 🔧 Tech Stack

- **Language**: Python 3.10  
- **Libraries**: scikit-learn, pandas, FastAPI  
- **MLOps**: Docker, GitHub Actions, Render  
- **Model**: Linear Regression on California Housing dataset

---

## 🧠 Model Details

- Dataset: `sklearn.datasets.fetch_california_housing()`  
- Preprocessing: Normalization of features  
- Target Variable: Median house value (per district)  
- Metric: R² Score ~ 0.85  

---

## 🐳 Dockerized Deployment

To run the project using Docker:

```bash
# Clone the repo
git clone https://github.com/shreeyanshm/California-Housing.git
cd California-Housing

# Build Docker image
docker build -t cali-housing .

# Run container
docker run -d -p 8080:8080 cali-housing
```

---

## 🔄 CI/CD Pipeline

**Trigger**: On push to `main` branch  

**Steps**:

- Lint & test code  
- Build Docker image  
- Deploy to Render (or your cloud platform)  

GitHub Actions handles automatic testing and deployment. [View logs here](https://github.com/shreeyanshm/California-Housing/actions).

---

## 📬 API Usage

**Endpoint**: `GET /predict`  

**Query Parameters (required)**:

| Param      | Type  | Example   |
|------------|--------|-----------|
| MedInc     | float  | 8.3       |
| HouseAge   | float  | 32        |
| AveRooms   | float  | 6.1       |
| AveBedrms  | float  | 1.1       |
| Population | float  | 1200      |
| AveOccup   | float  | 2.8       |
| Latitude   | float  | 36.4      |
| Longitude  | float  | -120.3    |

Example call:

```bash
curl "http://localhost:8080/predict?MedInc=8.3&HouseAge=32&AveRooms=6.1&AveBedrms=1.1&Population=1200&AveOccup=2.8&Latitude=36.4&Longitude=-120.3"
```

---

## 🤝 Contributing

Pull requests are welcome. For major changes, open an issue first to discuss what you'd like to change.




## 🙌 Acknowledgments

- scikit-learn for the dataset  
- FastAPI for the API framework  
- Render for free deployment hosting  
