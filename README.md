# Multivariate Data Analysis

This project demonstrates various techniques for analyzing and visualizing multivariate data using Python. The steps include computing mean vectors, covariance matrices, correlation, and visualizing attributes in the dataset. The project also identifies attributes with the largest/smallest variance and covariance.

## Features

- **Multivariate Mean Vector:** Compute the mean of all attributes.
- **Covariance Matrices:**
  - Computed using both inner and outer products.
- **Correlation Analysis:** Measure the correlation (cosine similarity) between two attributes.
- **Attribute Distributions:**
  - Visualize the probability density function (PDF) of an attribute assuming normal distribution.
- **Scatter Plots:** Analyze relationships between attribute pairs.
- **Variance and Covariance:**
  - Identify attributes with the largest and smallest variances.
  - Find attribute pairs with the largest and smallest covariances.

## Dataset

- The project uses a CSV file named `telescope_data.csv`.
- Ensure the dataset is structured with numerical attributes and no missing values.
- Remove the last column in the dataset if it is non-numerical before analysis.

## Setup and Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/multivariate-data-analysis.git
   ```
2. Install the required Python libraries:
   ```bash
   pip install numpy pandas matplotlib seaborn scipy
   ```
3. Place your dataset (`telescope_data.csv`) in the project directory.
4. Run the script:
   ```bash
   python analysis_script.py
   ```

## Code Highlights

### 1. Compute Mean and Covariance
```python
mean_vector = data.mean()
cov_matrix_inner = np.dot(centered_data.T, centered_data) / (len(data) - 1)
```

### 2. Correlation Between Attributes
```python
cosine_similarity = np.dot(attribute_1, attribute_2) / (np.linalg.norm(attribute_1) * np.linalg.norm(attribute_2))
```

### 3. Variance and Covariance Analysis
```python
largest_attribute = variances.idxmax()
largest_cov = cov_matrix.values[np.triu_indices_from(cov_matrix, 1)].max()
```

### 4. Visualization
- **Scatter Plots:** To analyze relationships.
- **Pairplot:** Overview of attribute relationships.
- **Probability Density Function:** For normal distribution fitting.

## Visualizations

1. **Scatter Plot:** Attribute 1 vs Attribute 2  

2. **PDF of Attribute 1:**  

3. **Attribute Pairplot:**  

## Results

- **Largest Variance:** Attribute X  
- **Smallest Variance:** Attribute Y  
- **Largest Covariance:** Attribute A and B  
- **Smallest Covariance:** Attribute C and D  


## License

This project is licensed under the Apache 2.0 license.

---
