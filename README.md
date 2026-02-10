<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>House Price Prediction Project - README</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            line-height: 1.6;
            color: #24292e;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            border-radius: 12px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 60px 40px;
            text-align: center;
        }

        .header h1 {
            font-size: 3em;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        .header .subtitle {
            font-size: 1.3em;
            opacity: 0.95;
            margin-top: 15px;
        }

        .badges {
            margin-top: 25px;
            display: flex;
            gap: 10px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .badge {
            display: inline-block;
            padding: 6px 12px;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 20px;
            font-size: 0.9em;
            font-weight: 600;
            backdrop-filter: blur(10px);
        }

        .content {
            padding: 40px;
        }

        .nav {
            background: #f6f8fa;
            padding: 30px;
            border-radius: 8px;
            margin-bottom: 40px;
        }

        .nav h2 {
            color: #0366d6;
            margin-bottom: 20px;
            font-size: 1.8em;
        }

        .nav ul {
            list-style: none;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 12px;
        }

        .nav li a {
            color: #0366d6;
            text-decoration: none;
            padding: 10px 15px;
            display: block;
            background: white;
            border-radius: 6px;
            transition: all 0.3s ease;
            border-left: 4px solid #0366d6;
        }

        .nav li a:hover {
            background: #0366d6;
            color: white;
            transform: translateX(5px);
        }

        section {
            margin-bottom: 50px;
        }

        h2 {
            color: #0366d6;
            font-size: 2.2em;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 3px solid #0366d6;
        }

        h3 {
            color: #6f42c1;
            font-size: 1.6em;
            margin-top: 30px;
            margin-bottom: 15px;
        }

        h4 {
            color: #d73a49;
            font-size: 1.3em;
            margin-top: 20px;
            margin-bottom: 10px;
        }

        p {
            margin-bottom: 15px;
            color: #586069;
            font-size: 1.05em;
        }

        ul, ol {
            margin-left: 30px;
            margin-bottom: 20px;
        }

        li {
            margin-bottom: 8px;
            color: #586069;
        }

        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }

        .feature-card {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-5px);
        }

        .feature-card h3 {
            color: white;
            margin-top: 0;
            font-size: 1.4em;
        }

        .feature-card p {
            color: rgba(255, 255, 255, 0.9);
        }

        .code-block {
            background: #f6f8fa;
            border: 1px solid #d1d5da;
            border-radius: 6px;
            padding: 16px;
            margin: 20px 0;
            overflow-x: auto;
            font-family: 'Courier New', monospace;
            font-size: 0.95em;
        }

        .code-block pre {
            margin: 0;
            color: #24292e;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin: 25px 0;
            background: white;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
            overflow: hidden;
        }

        thead {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
        }

        th, td {
            padding: 15px;
            text-align: left;
            border-bottom: 1px solid #e1e4e8;
        }

        th {
            font-weight: 600;
            font-size: 1.05em;
        }

        tbody tr:hover {
            background: #f6f8fa;
        }

        .tech-stack {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin: 25px 0;
        }

        .tech-item {
            background: #f6f8fa;
            padding: 15px;
            border-radius: 8px;
            border-left: 4px solid #0366d6;
        }

        .tech-item strong {
            color: #0366d6;
            display: block;
            margin-bottom: 5px;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }

        .stat-card {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            color: white;
            padding: 25px;
            border-radius: 10px;
            text-align: center;
        }

        .stat-card h3 {
            color: white;
            font-size: 2.5em;
            margin: 10px 0;
        }

        .stat-card p {
            color: rgba(255, 255, 255, 0.9);
            font-size: 1.1em;
        }

        .alert {
            background: #fff3cd;
            border-left: 4px solid #ffc107;
            padding: 15px 20px;
            margin: 20px 0;
            border-radius: 6px;
        }

        .alert.success {
            background: #d4edda;
            border-left-color: #28a745;
        }

        .alert.info {
            background: #d1ecf1;
            border-left-color: #17a2b8;
        }

        .alert.danger {
            background: #f8d7da;
            border-left-color: #dc3545;
        }

        .project-structure {
            background: #24292e;
            color: #f6f8fa;
            padding: 20px;
            border-radius: 8px;
            font-family: 'Courier New', monospace;
            margin: 25px 0;
            overflow-x: auto;
        }

        .project-structure pre {
            margin: 0;
            line-height: 1.8;
        }

        .btn {
            display: inline-block;
            padding: 12px 24px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-decoration: none;
            border-radius: 6px;
            font-weight: 600;
            transition: all 0.3s ease;
            margin: 10px 5px;
        }

        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 15px rgba(102, 126, 234, 0.4);
        }

        .footer {
            background: #24292e;
            color: white;
            padding: 40px;
            text-align: center;
        }

        .footer p {
            color: rgba(255, 255, 255, 0.8);
            margin: 10px 0;
        }

        .emoji {
            font-size: 1.3em;
            margin-right: 8px;
        }

        .challenge-solution {
            background: #f6f8fa;
            padding: 20px;
            border-radius: 8px;
            margin: 20px 0;
            border-left: 4px solid #6f42c1;
        }

        .challenge-solution h4 {
            color: #d73a49;
        }

        .step-list {
            counter-reset: step-counter;
            list-style: none;
            margin-left: 0;
        }

        .step-list li {
            counter-increment: step-counter;
            margin-bottom: 25px;
            padding-left: 50px;
            position: relative;
        }

        .step-list li::before {
            content: counter(step-counter);
            position: absolute;
            left: 0;
            top: 0;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            width: 35px;
            height: 35px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <div class="header">
            <h1>🏠 House Price Prediction Project</h1>
            <p class="subtitle">A machine learning web application that predicts house prices based on various features</p>
            <div class="badges">
                <span class="badge">🐍 Python 3.8+</span>
                <span class="badge">⚡ Flask 2.0+</span>
                <span class="badge">🤖 Scikit-learn 1.0+</span>
                <span class="badge">📊 Machine Learning</span>
                <span class="badge">🌐 Live Deployment</span>
            </div>
        </div>

        <!-- Main Content -->
        <div class="content">
            <!-- Table of Contents -->
            <nav class="nav">
                <h2>📋 Table of Contents</h2>
                <ul>
                    <li><a href="#overview">Overview</a></li>
                    <li><a href="#features">Features</a></li>
                    <li><a href="#dataset">Dataset</a></li>
                    <li><a href="#tech-stack">Technology Stack</a></li>
                    <li><a href="#project-structure">Project Structure</a></li>
                    <li><a href="#installation">Installation</a></li>
                    <li><a href="#usage">Usage</a></li>
                    <li><a href="#model">Model Development</a></li>
                    <li><a href="#deployment">Deployment</a></li>
                    <li><a href="#results">Results</a></li>
                    <li><a href="#challenges">Challenges & Solutions</a></li>
                    <li><a href="#future">Future Enhancements</a></li>
                    <li><a href="#acknowledgements">Acknowledgements</a></li>
                </ul>
            </nav>

            <!-- Overview Section -->
            <section id="overview">
                <h2><span class="emoji">🎯</span>Overview</h2>
                
                <h3>Objective</h3>
                <p>Develop a machine learning web application that predicts house prices based on various features such as location, size, condition, and temporal factors.</p>

                <h3>Problem Statement</h3>
                <p>Real estate prices are influenced by multiple factors that are often complex to analyze manually. This project aims to:</p>
                <ul>
                    <li>Create a predictive model using historical housing data</li>
                    <li>Build an intuitive web interface for users</li>
                    <li>Deploy the application for public access</li>
                    <li>Provide accurate price estimations based on input parameters</li>
                </ul>
            </section>

            <!-- Features Section -->
            <section id="features">
                <h2><span class="emoji">✨</span>Key Features</h2>
                <div class="feature-grid">
                    <div class="feature-card">
                        <h3>👥 User-Friendly Interface</h3>
                        <p>Clean, responsive web design with intuitive form inputs and modern styling</p>
                    </div>
                    <div class="feature-card">
                        <h3>⚡ Real-time Predictions</h3>
                        <p>Instant price estimation with response time under 2 seconds</p>
                    </div>
                    <div class="feature-card">
                        <h3>📊 Multiple Parameters</h3>
                        <p>17 different features affecting house prices for accurate predictions</p>
                    </div>
                    <div class="feature-card">
                        <h3>🌐 Live Deployment</h3>
                        <p>Accessible online 24/7 via web browser on Render platform</p>
                    </div>
                </div>
            </section>

            <!-- Dataset Section -->
            <section id="dataset">
                <h2><span class="emoji">📊</span>Dataset</h2>
                
                <h3>Dataset Specifications</h3>
                <div class="stats-grid">
                    <div class="stat-card">
                        <p>Total Records</p>
                        <h3>21,613</h3>
                        <p>Houses</p>
                    </div>
                    <div class="stat-card">
                        <p>Features</p>
                        <h3>18</h3>
                        <p>Columns</p>
                    </div>
                    <div class="stat-card">
                        <p>Time Period</p>
                        <h3>1 Year</h3>
                        <p>May 2014 - May 2015</p>
                    </div>
                    <div class="stat-card">
                        <p>Location</p>
                        <h3>King County</h3>
                        <p>Washington, USA</p>
                    </div>
                </div>

                <div class="alert info">
                    <strong>📌 Dataset Source:</strong> Kaggle - House Sales in King County, USA<br>
                    <strong>Contributor:</strong> Shreya Chaudhary
                </div>

                <h3>Data Preprocessing Steps</h3>
                <ol class="step-list">
                    <li><strong>Handling Missing Values:</strong> Checked for null values and handled appropriately</li>
                    <li><strong>Feature Engineering:</strong> Extracted year, month, day from date column</li>
                    <li><strong>Categorical Encoding:</strong> Encoded city and country variables using label encoding</li>
                    <li><strong>Feature Selection:</strong> Selected 17 most relevant features for model training</li>
                    <li><strong>Normalization:</strong> Applied normalization where necessary for optimal model performance</li>
                </ol>
            </section>

            <!-- Technology Stack Section -->
            <section id="tech-stack">
                <h2><span class="emoji">🛠</span>Technology Stack</h2>
                
                <h3>Backend Technologies</h3>
                <div class="tech-stack">
                    <div class="tech-item">
                        <strong>Python</strong>
                        <p>Primary programming language</p>
                    </div>
                    <div class="tech-item">
                        <strong>Flask</strong>
                        <p>Lightweight web framework</p>
                    </div>
                    <div class="tech-item">
                        <strong>Scikit-learn</strong>
                        <p>Machine learning algorithms</p>
                    </div>
                    <div class="tech-item">
                        <strong>Pandas</strong>
                        <p>Data manipulation and analysis</p>
                    </div>
                    <div class="tech-item">
                        <strong>NumPy</strong>
                        <p>Numerical operations</p>
                    </div>
                    <div class="tech-item">
                        <strong>Pickle</strong>
                        <p>Model serialization</p>
                    </div>
                </div>

                <h3>Frontend Technologies</h3>
                <div class="tech-stack">
                    <div class="tech-item">
                        <strong>HTML5</strong>
                        <p>Markup language</p>
                    </div>
                    <div class="tech-item">
                        <strong>CSS3</strong>
                        <p>Styling with animations</p>
                    </div>
                </div>

                <h3>Development Tools</h3>
                <div class="tech-stack">
                    <div class="tech-item">
                        <strong>PyCharm</strong>
                        <p>IDE for Python development</p>
                    </div>
                    <div class="tech-item">
                        <strong>Git</strong>
                        <p>Version control system</p>
                    </div>
                    <div class="tech-item">
                        <strong>GitHub</strong>
                        <p>Code repository hosting</p>
                    </div>
                    <div class="tech-item">
                        <strong>Jupyter Notebook</strong>
                        <p>Interactive development</p>
                    </div>
                </div>

                <h3>Deployment</h3>
                <div class="tech-stack">
                    <div class="tech-item">
                        <strong>Render</strong>
                        <p>Cloud deployment platform</p>
                    </div>
                    <div class="tech-item">
                        <strong>Gunicorn</strong>
                        <p>WSGI HTTP Server</p>
                    </div>
                </div>
            </section>

            <!-- Project Structure Section -->
            <section id="project-structure">
                <h2><span class="emoji">📁</span>Project Structure</h2>
                <div class="project-structure">
                    <pre>
House-Price-Prediction/
│
├── app.py                      # Flask application
├── MINI_PROJECT.pkl           # Trained model file
├── requirements.txt           # Python dependencies
├── Procfile                   # Render deployment config
│
├── templates/
│   └── index.html            # Main HTML template
│
├── static/
│   ├── css/
│   │   └── style.css         # Custom styles
│   └── js/
│       └── script.js         # JavaScript (if any)
│
├── notebooks/
│   └── model_training.ipynb  # Jupyter notebook
│
├── data/
│   └── data.csv              # Dataset
│
└── README.md                 # Documentation
                    </pre>
                </div>
            </section>

            <!-- Installation Section -->
            <section id="installation">
                <h2><span class="emoji">🚀</span>Installation</h2>
                
                <div class="alert">
                    <strong>⚠️ Prerequisites:</strong> Python 3.8 or higher, pip package manager
                </div>

                <h3>Step 1: Clone the Repository</h3>
                <div class="code-block">
                    <pre>git clone https://github.com/yourusername/house-price-prediction.git
cd house-price-prediction</pre>
                </div>

                <h3>Step 2: Create Virtual Environment</h3>
                <div class="code-block">
                    <pre>python -m venv venv</pre>
                </div>

                <h3>Step 3: Activate Virtual Environment</h3>
                <div class="code-block">
                    <pre># Windows
venv\Scripts\activate

# macOS/Linux
source venv/bin/activate</pre>
                </div>

                <h3>Step 4: Install Dependencies</h3>
                <div class="code-block">
                    <pre>pip install -r requirements.txt</pre>
                </div>
            </section>

            <!-- Usage Section -->
            <section id="usage">
                <h2><span class="emoji">💻</span>Usage</h2>
                
                <h3>Running Locally</h3>
                <ol class="step-list">
                    <li>
                        <strong>Start the Flask application:</strong>
                        <div class="code-block">
                            <pre>python app.py</pre>
                        </div>
                    </li>
                    <li>
                        <strong>Access the application:</strong>
                        <p>Open your browser and navigate to: <code>http://localhost:5000</code></p>
                    </li>
                    <li>
                        <strong>Make a prediction:</strong>
                        <ul>
                            <li>Fill in the form with house details (17 features)</li>
                            <li>Click the "Predict Price" button</li>
                            <li>View the estimated house price</li>
                        </ul>
                    </li>
                </ol>

                <h3>Input Features</h3>
                <table>
                    <thead>
                        <tr>
                            <th>Feature</th>
                            <th>Description</th>
                            <th>Type</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>Bedrooms</td>
                            <td>Number of bedrooms</td>
                            <td>Integer</td>
                        </tr>
                        <tr>
                            <td>Bathrooms</td>
                            <td>Number of bathrooms</td>
                            <td>Float</td>
                        </tr>
                        <tr>
                            <td>Sqft Living</td>
                            <td>Living area square footage</td>
                            <td>Float</td>
                        </tr>
                        <tr>
                            <td>Sqft Lot</td>
                            <td>Lot size square footage</td>
                            <td>Float</td>
                        </tr>
                        <tr>
                            <td>Floors</td>
                            <td>Number of floors</td>
                            <td>Float</td>
                        </tr>
                        <tr>
                            <td>Waterfront</td>
                            <td>Waterfront property (0 or 1)</td>
                            <td>Binary</td>
                        </tr>
                        <tr>
                            <td>View</td>
                            <td>View quality rating (0-4)</td>
                            <td>Integer</td>
                        </tr>
                        <tr>
                            <td>Condition</td>
                            <td>Overall condition (1-5)</td>
                            <td>Integer</td>
                        </tr>
                        <tr>
                            <td>Sqft Above</td>
                            <td>Square footage above ground</td>
                            <td>Float</td>
                        </tr>
                        <tr>
                            <td>Sqft Basement</td>
                            <td>Basement square footage</td>
                            <td>Float</td>
                        </tr>
                        <tr>
                            <td>Yr Built</td>
                            <td>Year the house was built</td>
                            <td>Integer</td>
                        </tr>
                        <tr>
                            <td>Yr Renovated</td>
                            <td>Year renovated (0 if never)</td>
                            <td>Integer</td>
                        </tr>
                        <tr>
                            <td>City</td>
                            <td>Encoded city value</td>
                            <td>Integer</td>
                        </tr>
                        <tr>
                            <td>Country</td>
                            <td>Encoded country value</td>
                            <td>Integer</td>
                        </tr>
                        <tr>
                            <td>Year</td>
                            <td>Sale year</td>
                            <td>Integer</td>
                        </tr>
                        <tr>
                            <td>Month</td>
                            <td>Sale month</td>
                            <td>Integer</td>
                        </tr>
                        <tr>
                            <td>Day</td>
                            <td>Sale day</td>
                            <td>Integer</td>
                        </tr>
                    </tbody>
                </table>
            </section>

            <!-- Model Development Section -->
            <section id="model">
                <h2><span class="emoji">🧠</span>Model Development</h2>
                
                <h3>Algorithm: Custom Linear Regression</h3>
                <p>The model implements Linear Regression from scratch using <strong>Singular Value Decomposition (SVD)</strong> for numerical stability.</p>

                <h3>Why Linear Regression?</h3>
                <ul>
                    <li>Simple and interpretable</li>
                    <li>Works well with continuous target variables</li>
                    <li>Low computational cost</li>
                    <li>Good baseline model for regression tasks</li>
                </ul>

                <h3>Implementation Overview</h3>
                
                <h4>1. Data Loading & Preprocessing</h4>
                <div class="code-block">
                    <pre>class MINIPROJECT:
    def __init__(self, data):
        # Load dataset
        self.df = pd.read_csv(data)
        
        # Date feature engineering
        self.df['date'] = pd.to_datetime(self.df['date'])
        self.df['year'] = self.df['date'].dt.year
        self.df['month'] = self.df['date'].dt.month
        self.df['day'] = self.df['date'].dt.day</pre>
                </div>

                <h4>2. Feature Engineering</h4>
                <ul>
                    <li><strong>Temporal Features:</strong> Extracted year, month, day from date</li>
                    <li><strong>Categorical Encoding:</strong> Manual label encoding for city and country</li>
                    <li><strong>Feature Selection:</strong> Dropped irrelevant columns (date, statezip, street)</li>
                </ul>

                <h4>3. Model Training using SVD</h4>
                <div class="code-block">
                    <pre>def training(self):
    # Mean centering
    X_mean = self.X_train.mean().values
    y_mean = self.y_train.mean()
    X_centered = X_np - X_mean
    y_centered = y_np - y_mean
    
    # SVD decomposition
    U, S, Vt = np.linalg.svd(X_centered, full_matrices=False)
    
    # Compute pseudo-inverse
    X_pinv = Vt.T @ np.diag(S_inv) @ U.T
    
    # Calculate coefficients and intercept
    self.m = X_pinv @ y_centered
    self.c = y_mean - np.dot(X_mean, self.m)</pre>
                </div>

                <h4>4. Model Evaluation Metrics</h4>
                <ul>
                    <li><strong>RMSE (Root Mean Squared Error):</strong> Measures average prediction error</li>
                    <li><strong>R² Score:</strong> Measures how well the model explains variance in prices</li>
                </ul>
            </section>

            <!-- Deployment Section -->
            <section id="deployment">
                <h2><span class="emoji">🌐</span>Deployment</h2>
                
                <h3>Deployment on Render</h3>
                
                <ol class="step-list">
                    <li>
                        <strong>Prepare Files</strong>
                        <p>Ensure you have these files in your repository:</p>
                        <ul>
                            <li><code>requirements.txt</code> - All Python dependencies</li>
                            <li><code>Procfile</code> - Deployment configuration</li>
                            <li><code>app.py</code> - Flask application</li>
                            <li><code>MINI_PROJECT.pkl</code> - Trained model</li>
                        </ul>
                    </li>
                    <li>
                        <strong>Create Render Account</strong>
                        <p>Sign up at <a href="https://render.com" target="_blank">render.com</a> and connect your GitHub account</p>
                    </li>
                    <li>
                        <strong>Deploy Web Service</strong>
                        <ul>
                            <li>Click "New +" → "Web Service"</li>
                            <li>Connect your GitHub repository</li>
                            <li>Configure settings:
                                <ul>
                                    <li>Name: house-price-predictor</li>
                                    <li>Environment: Python</li>
                                    <li>Build Command: <code>pip install -r requirements.txt</code></li>
                                    <li>Start Command: <code>gunicorn app:app</code></li>
                                </ul>
                            </li>
                            <li>Click "Create Web Service"</li>
                        </ul>
                    </li>
                    <li>
                        <strong>Access Live Application</strong>
                        <p>Render provides a live URL that's accessible 24/7</p>
                    </li>
                </ol>

                <h3>Required Files</h3>
                
                <h4>requirements.txt</h4>
                <div class="code-block">
                    <pre>flask
numpy
pandas
scikit-learn
gunicorn</pre>
                </div>

                <h4>Procfile</h4>
                <div class="code-block">
                    <pre>web: gunicorn app:app</pre>
                </div>
            </section>

            <!-- Results Section -->
            <section id="results">
                <h2><span class="emoji">📈</span>Results</h2>
                
                <h3>Sample Prediction</h3>
                
                <div class="alert success">
                    <h4>Input Values:</h4>
                    <ul>
                        <li>Bedrooms: 4</li>
                        <li>Bathrooms: 4</li>
                        <li>Sqft Living: 1340</li>
                        <li>Sqft Lot: 9050</li>
                        <li>Floors: 2</li>
                        <li>Waterfront: 1930</li>
                        <li>View: 1</li>
                        <li>Condition: 1</li>
                        <li>Sqft Above: 1900</li>
                        <li>Sqft Basement: 2000</li>
                        <li>Yr Built: 1200</li>
                        <li>Yr Renovated: 1350</li>
                        <li>City: 1</li>
                        <li>Country: 1</li>
                        <li>Year: 2001</li>
                        <li>Month: 12</li>
                        <li>Day: 1</li>
                    </ul>
                    
                    <h4 style="color: #28a745; font-size: 1.5em; margin-top: 20px;">Output:</h4>
                    <p style="font-size: 1.8em; font-weight: bold; color: #28a745;">Estimated House Price: $267,143.32</p>
                </div>

                <h3>Performance Metrics</h3>
                <div class="stats-grid">
                    <div class="stat-card">
                        <p>Response Time</p>
                        <h3>&lt; 2s</h3>
                        <p>For Prediction</p>
                    </div>
                    <div class="stat-card">
                        <p>Availability</p>
                        <h3>24/7</h3>
                        <p>Via Render URL</p>
                    </div>
                    <div class="stat-card">
                        <p>Model Type</p>
                        <h3>Linear</h3>
                        <p>Regression (SVD)</p>
                    </div>
                </div>
            </section>

            <!-- Challenges Section -->
            <section id="challenges">
                <h2><span class="emoji">🛡</span>Challenges & Solutions</h2>
                
                <div class="challenge-solution">
                    <h4>Challenge 1: Feature Engineering</h4>
                    <p><strong>Problem:</strong> Original dataset had categorical variables (city, country) that needed encoding for the model.</p>
                    <p><strong>Solution:</strong></p>
                    <ul>
                        <li>Used label encoding for categorical variables</li>
                        <li>Extracted temporal features (year, month, day) from date</li>
                        <li>Created new encoded features for model input</li>
                    </ul>
                </div>

                <div class="challenge-solution">
                    <h4>Challenge 2: Model Persistence</h4>
                    <p><strong>Problem:</strong> Trained model needed to be saved and loaded for web deployment.</p>
                    <p><strong>Solution:</strong></p>
                    <ul>
                        <li>Used Python's <code>pickle</code> module for model serialization</li>
                        <li>Saved model as <code>.pkl</code> file</li>
                        <li>Loaded model in Flask application</li>
                    </ul>
                </div>

                <div class="challenge-solution">
                    <h4>Challenge 3: Form Input Handling</h4>
                    <p><strong>Problem:</strong> HTML form returns string values, but model expects numerical values.</p>
                    <p><strong>Solution:</strong></p>
                    <div class="code-block">
                        <pre>a = [float(i) for i in request.form.values()]</pre>
                    </div>
                </div>

                <div class="challenge-solution">
                    <h4>Challenge 4: Deployment Issues</h4>
                    <p><strong>Problem:</strong> Render deployment failed due to missing dependencies.</p>
                    <p><strong>Solution:</strong></p>
                    <ul>
                        <li>Created complete <code>requirements.txt</code> with exact versions</li>
                        <li>Used <code>gunicorn</code> as production server</li>
                        <li>Added <code>Procfile</code> for Render configuration</li>
                    </ul>
                </div>
            </section>

            <!-- Future Enhancements Section -->
            <section id="future">
                <h2><span class="emoji">🚀</span>Future Enhancements</h2>
                
                <h3>Model Improvements</h3>
                <ul>
                    <li>Try different algorithms (Random Forest, Gradient Boosting, Neural Networks)</li>
                    <li>Add polynomial features and interaction terms</li>
                    <li>Implement hyperparameter tuning (Grid Search, Random Search)</li>
                    <li>Cross-validation for robust evaluation</li>
                </ul>

                <h3>Application Features</h3>
                <ul>
                    <li>Add data visualization charts</li>
                    <li>Include historical price trends</li>
                    <li>Save prediction history</li>
                    <li>Compare multiple predictions</li>
                    <li>Export results to PDF/Excel</li>
                    <li>Mobile app version</li>
                </ul>

                <h3>Performance & Scalability</h3>
                <ul>
                    <li>Docker containerization</li>
                    <li>Implement caching for faster predictions</li>
                    <li>Add API rate limiting</li>
                    <li>Database integration for storing predictions</li>
                    <li>Load balancing for multiple instances</li>
                </ul>

                <h3>Monitoring & Analytics</h3>
                <ul>
                    <li>Add logging and error tracking</li>
                    <li>Performance monitoring dashboard</li>
                    <li>Usage analytics</li>
                    <li>User management system</li>
                </ul>
            </section>

            <!-- Acknowledgements Section -->
            <section id="acknowledgements">
                <h2><span class="emoji">🙏</span>Acknowledgements</h2>
                
                <h3>Dataset Source</h3>
                <ul>
                    <li><strong>Dataset Name:</strong> House Sales in King County, USA</li>
                    <li><strong>Source:</strong> Kaggle</li>
                    <li><strong>Contributor:</strong> Shreya Chaudhary</li>
                    <li><strong>Context:</strong> This dataset contains house sale prices for King County, which includes Seattle</li>
                </ul>

                <h3>Tools and Libraries</h3>
                <div class="tech-stack">
                    <div class="tech-item">Flask - Web framework for Python</div>
                    <div class="tech-item">Scikit-learn - Machine learning library</div>
                    <div class="tech-item">NumPy - Numerical computing</div>
                    <div class="tech-item">Pandas - Data manipulation</div>
                    <div class="tech-item">Pickle - Model serialization</div>
                    <div class="tech-item">HTML/CSS - Frontend development</div>
                    <div class="tech-item">Render - Cloud deployment platform</div>
                    <div class="tech-item">Git/GitHub - Version control</div>
                </div>

                <h3>Special Thanks</h3>
                <ul>
                    <li>Kaggle community for providing the dataset</li>
                    <li>Open-source contributors of all libraries used</li>
                    <li>Render platform for free deployment hosting</li>
                </ul>
            </section>

            <!-- Call to Action -->
            <div style="text-align: center; margin: 50px 0;">
                <a href="#" class="btn">🔗 View Live Demo</a>
                <a href="#" class="btn">📂 GitHub Repository</a>
                <a href="#" class="btn">📥 Download Project</a>
            </div>
        </div>

        <!-- Footer -->
        <div class="footer">
            <h3>📜 License</h3>
            <p>This project is licensed under the MIT License</p>
            
            <h3 style="margin-top: 30px;">📞 Contact</h3>
            <p><strong>Project By:</strong> M. Sachin</p>
            <p><strong>Last Updated:</strong> 10-2-2026</p>
            
            <p style="margin-top: 30px; font-size: 1.2em;">⭐ If you found this project helpful, please consider giving it a star!</p>
            <p style="margin-top: 20px; font-size: 1.1em;">Made with ❤️ and Python</p>
        </div>
    </div>
</body>
</html>
