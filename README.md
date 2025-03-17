# Spatial-Aware Hospital Recommendation System

[![Python 3.8+](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-ee4c2c.svg)](https://pytorch.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

A deep learning recommendation system that helps patients find hospitals based on their care priorities and location preferences using HCAHPS survey data.

## 🏥 Overview

This project leverages the Hospital Consumer Assessment of Healthcare Providers and Systems (HCAHPS) dataset to create a sophisticated recommendation engine. By combining collaborative filtering techniques with geospatial awareness, we provide personalized hospital recommendations that balance quality metrics with practical location considerations.
This project implements a collaborative filtering recommendation system utilizing deep learning techniques (PyTorch) to help:
- **Patients** find hospitals that best align with their healthcare quality preferences.
- **Healthcare Administrators** benchmark their facilities and identify areas for improvement.

The system leverages the **Hospital Consumer Assessment of Healthcare Providers and Systems (HCAHPS)** dataset from the Centers for Medicare & Medicaid Services (CMS).

Our model achieves remarkable performance (R² of 0.9995, RMSE of 0.0218) and offers valuable insights for both patients seeking healthcare and administrators looking to improve patient experience.

![Model Architecture](path/to/model_architecture.png)

## Business Objectives

1. **Personalize recommendations** based on patient care quality preferences.
2. **Benchmark hospitals** to identify similar facilities and best practices.
3. **Predict patient satisfaction** effectively.
4. Provide **interactive insights** into hospital performance.
5. Empower **data-driven decision-making** for healthcare stakeholders.
   
## ✨ Features

- **Personalized Recommendations**: Matches hospitals to patient care priorities (nurse communication, doctor communication, cleanliness, etc.)
- **Location-Aware**: Incorporates distance and geographical constraints into recommendations
- **Interactive Visualization**: Explore hospital quality dimensions across geographical regions
- **Deep Learning Powered**: Utilizes neural collaborative filtering with spatial awareness
- **Highly Accurate**: Near-perfect predictive performance on test data

## 📊 Data

- **Dataset:** Hospital Consumer Assessment of Healthcare Providers and Systems (HCAHPS)
- **Provided by:** [The Centers for Medicare & Medicaid Services (CMS)](https://data.cms.gov/provider-data/topics/hospitals/hcahps/)

The system uses the HCAHPS survey dataset from CMS, which includes:
- Patient satisfaction scores across 10 care dimensions
- Data from 4,780 healthcare facilities across the United States
- Enhanced with geospatial features (coordinates, distances, hospital density)


## 🛠️ Technologies

- **Python**: Core programming language
- **PyTorch**: Deep learning framework for model development
- **Pandas/NumPy**: Data manipulation and numerical processing
- **Scikit-learn**: Machine learning utilities and metrics
- **Plotly/Matplotlib**: Data visualization
- **Geopy**: Geographical data processing

## Methodology

1. **Data Preparation**
   - Topic Mapping and NLP categorization.
   - Sentiment analysis using DistilBERT transformer.
   - Generation of sentiment and quantitative scores from qualitative data.

2. **Deep Learning Model**
   - PyTorch-based Neural Collaborative Filtering model.
   - Fine-tuned for improved accuracy and interpretability.

## 🔧 Installation

```bash
# Clone the repository
git clone https://github.com/esengendo/spatial-hospital-recommendation-system.git
cd Spatial-Aware Hospital Recommendation System

# Create and activate virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

## 🚀 Usage

### Basic Usage

```python
from recommend import recommend_hospitals

# Define user preferences (0-1 scale)
user_preferences = {
    'Nurse Communication': 0.9,
    'Cleanliness': 0.8,
    'Doctor Communication': 0.6,
    'Overall Rating': 0.5
}

# User location (latitude, longitude)
user_location = (42.3601, -71.0589)  # Boston

# Get recommendations
recommendations = recommend_hospitals(
    model,
    hospital_df,
    user_preferences,
    user_location=user_location,
    max_distance=50,  # miles
    top_n=5
)

print(recommendations)
```

### Interactive Demo

Launch the interactive demo with:

```bash
python demo.py
```

This opens a browser-based interface where you can:
- Set your care priorities using sliders
- Enter your location
- View recommended hospitals on an interactive map
- Explore detailed information about each recommendation

## 📈 Model Performance Metrics

The model demonstrates exceptional performance across multiple metrics:


| Metric                  | Score  |
|-------------------------|--------|
| Root Mean Square Error (RMSE) | 0.0218 |
| Mean Absolute Error (MAE)     | 0.0168 |
| Mean Sentiment Accuracy       | 92.3% |
| Precision                     | 89.5% |
| Recall                        | 84.7% |
| F1 Score                      | 87.3% |

These metrics confirm the successful achievement of our objectives.

## Project Impact
The developed recommendation system provides:
- Enhanced patient satisfaction through personalized recommendations.
- Strategic insights for hospital benchmarking and quality improvement.
- Improved resource allocation based on actionable insights.

## Next Steps
Future improvements could include:
- Integrating real-time patient feedback.
- Expansion to additional healthcare metrics.
- Interactive web-based platform deployment.
  
## 📖 Documentation

Comprehensive documentation is available in the [docs](./docs) directory:
- [Data Processing](./docs/data_processing.md)
- [Model Architecture](./docs/model_architecture.md)
- [Training Process](./docs/training.md)
- [Evaluation Methodology](./docs/evaluation.md)
- [API Reference](./docs/api.md)

## Repository Structure

- **data/**: HCAHPS dataset and processed files
- **notebooks/**: Exploratory Data Analysis, Model Training & Fine-tuning
- **models/**: Saved PyTorch models
- **reports/**: Project documentation, visualizations

## 📝 Citation

If you use this project in your research or application, please cite:

```
@software{hospital_recommendation_system,
  author = {Emmanuel Sengendo},
  title = {Spatial-Aware Hospital Recommendation System},
  year = {2025},
  url = {https://github.com/esengendo/spatial-hospital-recommendation-system}
}
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📧 Contact

For questions or feedback, please contact:

- **Name:** Emmanuel Sengendo
- **Position:** Data Scientist
- **Contact:** esengendo@gmail.com | LinkedIn: [Emmanuel Sengendo](https://linkedin.com/in/esengendo)
- Email: 







### Visualization of Model Performance

*Include visualizations such as training loss curves, predicted vs. actual rating distributions, and sentiment distributions.*

---


© 2025 [Emmanuel Sengendo]. All rights reserved.


Made with ❤️ for improving healthcare access and quality
