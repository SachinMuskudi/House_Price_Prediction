<h1>🏠 House Price Prediction Project</h1>

<p>
A Machine Learning web application that predicts house prices using historical real-estate data.
The project covers the complete ML lifecycle—from data preprocessing and model training to web deployment.
</p>

<h2>📌 Table of Contents</h2>
<ul>
    <li>Acknowledgements</li>
    <li>Project Overview</li>
    <li>Dataset Description</li>
    <li>Project Structure</li>
    <li>Technology Stack</li>
    <li>Implementation Steps</li>
    <li>Model Development</li>
    <li>Deployment Process</li>
    <li>Results</li>
    <li>Future Enhancements</li>
    <li>Conclusion</li>
</ul>

<h2>🙏 Acknowledgements</h2>
<ul>
    <li><b>Dataset:</b> House Sales in King County, USA (Kaggle)</li>
    <li><b>Contributor:</b> Shreya Chaudhary</li>
    <li>Thanks to the Kaggle community and open-source contributors</li>
    <li>Render platform for free cloud deployment</li>
</ul>

<h2>📊 Project Overview</h2>

<h3>Objective</h3>
<p>
Develop a machine learning web application that predicts house prices based on location,
size, condition, and time-based features.
</p>

<h3>Key Features</h3>
<ul>
    <li>User-friendly web interface</li>
    <li>Real-time house price prediction</li>
    <li>17 input features affecting house prices</li>
    <li>Live deployment using Render</li>
</ul>

<h2>📁 Dataset Description</h2>
<ul>
    <li><b>Total Records:</b> 21,613</li>
    <li><b>Features:</b> 18 columns</li>
    <li><b>Location:</b> King County, Washington, USA</li>
    <li><b>Time Period:</b> May 2014 – May 2015</li>
</ul>

<h3>Preprocessing Steps</h3>
<ul>
    <li>Handled missing values</li>
    <li>Extracted year, month, day from date</li>
    <li>Encoded categorical variables (city, country)</li>
    <li>Selected 17 relevant features</li>
</ul>

<h2>📂 Project Structure</h2>
<pre>
House-Price-Prediction/
│
├── app.py
├── requirements.txt
├── Procfile
├── MINI_PROJECT.pkl
├── templates/
│   └── index.html
└── static/
</pre>

<h2>🛠 Technology Stack</h2>

<h3>Backend</h3>
<ul>
    <li>Python</li>
    <li>Flask</li>
    <li>Scikit-learn</li>
    <li>NumPy, Pandas</li>
    <li>Pickle</li>
</ul>

<h3>Frontend</h3>
<ul>
    <li>HTML5</li>
    <li>CSS3</li>
</ul>

<h3>Deployment</h3>
<ul>
    <li>GitHub</li>
    <li>Render</li>
</ul>

<h2>⚙ Implementation Steps</h2>
<ol>
    <li>Setup virtual environment</li>
    <li>Analyze and preprocess dataset</li>
    <li>Train Linear Regression model</li>
    <li>Save model using pickle</li>
    <li>Develop Flask web application</li>
    <li>Deploy on Render</li>
</ol>

<h2>📐 Model Development</h2>
<p>
<b>Algorithm Used:</b> Linear Regression (Custom implementation using SVD)
</p>

<ul>
    <li>Mean centering for numerical stability</li>
    <li>SVD used to compute pseudo-inverse</li>
    <li>Calculated coefficients (m) and intercept (c)</li>
    <li>Evaluated using RMSE and R² score</li>
</ul>

<h2>🚀 Deployment Process</h2>
<ul>
    <li>Create GitHub repository</li>
    <li>Upload project files</li>
    <li>Connect repository to Render</li>
    <li>Deploy using Gunicorn</li>
</ul>

<h2>📈 Results and Output</h2>
<ul>
    <li>Prediction response time: &lt; 2 seconds</li>
    <li>Accurate predictions based on R² score</li>
    <li>Accessible 24/7 via Render URL</li>
</ul>

<h2>🔮 Future Enhancements</h2>
<ul>
    <li>Advanced models (Random Forest, Gradient Boosting)</li>
    <li>Hyperparameter tuning</li>
    <li>Prediction history and analytics</li>
    <li>Docker-based deployment</li>
</ul>

<h2>✅ Conclusion</h2>
<p>
This project demonstrates a complete end-to-end Machine Learning pipeline with real-world deployment.
It serves as an excellent template for full-stack ML applications.
</p>

<footer>
<p>
<b>Project By:</b> M. Sachin<br>
<b>Last Updated:</b> 10-02-2026<br>
<b>Live App:</b> Project Link<br>
<b>GitHub:</b> Repository Link
</p>
</footer>
