# **Phishing Website Detection Using Machine Learning Techniques**

## **Objective**

Phishing websites are a common social engineering tactic that mimic trustworthy URLs and webpages to deceive users. This project aims to train machine learning models and deep neural networks on a curated dataset to predict phishing websites. Both phishing and legitimate URLs are gathered to create the dataset, from which essential URL and website content-based features are extracted. The performance of various models is measured and compared to determine the most effective approach.

---

## **Data Collection**

### **Phishing URLs**:
- Collected from the open-source service **PhishTank**.
  - PhishTank provides regularly updated phishing URL datasets in multiple formats (CSV, JSON, etc.).
  - Download the data: [PhishTank Developer Info](https://www.phishtank.com/developer_info.php)
  - **Sample Size**: 5,000 random phishing URLs.

### **Legitimate URLs**:
- Sourced from the **University of New Brunswick’s open datasets**.
  - The dataset contains benign, spam, phishing, malware, and defacement URLs.
  - For this project, only **benign URLs** are used.
  - Download the data: [UNB URL Dataset](https://www.unb.ca/cic/datasets/url-2016.html)
  - **Sample Size**: 5,000 random legitimate URLs.

---

## **Feature Extraction**

Seventeen features are extracted from the dataset across three categories:

1. **Address Bar-Based Features**  
   - **9 features** extracted, including checks for URL length, the presence of special characters, and HTTPS usage.

2. **Domain-Based Features**  
   - **4 features** extracted, focusing on domain age, DNS record status, and subdomain counts.

3. **HTML & JavaScript-Based Features**  
   - **4 features** extracted, analyzing scripts, iframe usage, and suspicious tags.

The combined 10,000 URLs and extracted features are stored in the file.

Features were referenced from the [UCI Phishing Websites Dataset](https://archive.ics.uci.edu/ml/datasets/Phishing+Websites).

---

## **Models & Training**

The dataset is split into **80% training data (8,000 samples)** and **20% testing data (2,000 samples)**. This is a **binary classification problem**, where each URL is classified as:
- **Phishing (1)**  
- **Legitimate (0)**  

The following supervised machine learning models were used for training:

- **Decision Tree**
- **Random Forest**
- **Multilayer Perceptrons**
- **XGBoost**
- **Autoencoder Neural Network**
- **Support Vector Machines**

Each model’s performance was evaluated based on accuracy, precision, recall, and F1-score.

---

## **Presentation**

For detailed insights into the methodology and results, view the project presentation:  
[Phishing Website Detection Presentation (PDF)](https://github.com/ssam246/Phishing-Website-Detection/blob/main/Phishing-Website-Detection-by-Machine-Learning-Techniques-master/Phishing%20Website%20Detection/Phishing%20Website%20Detection%20Using%20Machine%20Learning.pdf)

---

## **Next Steps**

### Future Enhancements:
- **Browser Extension**:
  - A browser extension will be developed to predict the nature of URLs (legitimate or phishing) in real-time.
- **Graphical User Interface (GUI)**:
  - A GUI will allow users to input URLs for prediction and visualize results.

*Progress updates on these features will be shared in future project releases.*

---

### **Clone and Run the Project**

To set up and run this project locally:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/ssam246/Phishing-Website-Detection
   cd Phishing-Website-Detection
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Main Program**:
   ```bash
   python main.py
   ```

---

## **Acknowledgments**

This project was inspired and developed using publicly available datasets and frameworks:  
- **PhishTank**: For providing the phishing URLs.  
- **University of New Brunswick (UNB)**: For the legitimate URL dataset.  
- **UCI Machine Learning Repository**: For feature engineering references.

Special thanks to the course instructors and mentors for their guidance in making this project a success.

---

### **Made with 💻 and 🛡️ by Stephen**

