<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Enhanced Precision Agricultural Management System</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            color: #333;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
        }

        .navbar {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            padding: 1rem 2rem;
            border-radius: 15px;
            margin-bottom: 2rem;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 10px;
            z-index: 1000;
        }

        .navbar-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: #667eea;
            display: flex;
            align-items: center;
        }

        .logo i {
            margin-right: 10px;
            font-size: 1.8rem;
        }

        .nav-links {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .nav-link, .btn {
            padding: 0.5rem 1rem;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            text-decoration: none;
            color: #667eea;
            background: transparent;
            transition: all 0.3s ease;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
        }

        .nav-link i, .btn i {
            margin-right: 5px;
        }

        .nav-link:hover, .btn:hover {
            background: #667eea;
            color: white;
            transform: translateY(-2px);
        }

        .hero {
            text-align: center;
            padding: 3rem 0;
            color: white;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin: 3rem 0;
        }

        .feature-card {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.2);
        }

        .feature-card h3 {
            color: #667eea;
            margin-bottom: 1rem;
            font-size: 1.3rem;
            display: flex;
            align-items: center;
        }

        .feature-card h3 i {
            margin-right: 10px;
            font-size: 1.5rem;
        }

        .feature-card p {
            color: #666;
            line-height: 1.6;
            margin-bottom: 1.5rem;
        }

        .form-container {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
            margin: 2rem 0;
        }

        .form-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1rem;
        }

        .form-section {
            background: #f8f9ff;
            padding: 1.5rem;
            border-radius: 10px;
            border-left: 4px solid #667eea;
        }

        .form-section h4 {
            color: #667eea;
            margin-bottom: 1rem;
            font-size: 1.1rem;
            display: flex;
            align-items: center;
        }

        .form-section h4 i {
            margin-right: 8px;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: #333;
            font-weight: 500;
        }

        .form-group input, .form-group select, .form-group textarea {
            width: 100%;
            padding: 0.75rem;
            border: 2px solid #e0e0e0;
            border-radius: 8px;
            font-size: 1rem;
            transition: border-color 0.3s ease;
        }

        .form-group input:focus, .form-group select:focus, .form-group textarea:focus {
            outline: none;
            border-color: #667eea;
        }

        .btn-primary {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 0.75rem 2rem;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            margin: 1rem 0;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .btn-primary i {
            margin-right: 8px;
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
        }

        .btn-primary:disabled {
            opacity: 0.6;
            cursor: not-allowed;
            transform: none;
        }

        .result-card {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
            margin: 2rem 0;
            border-left: 5px solid #667eea;
        }

        .result-card h3 {
            color: #667eea;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
        }

        .result-card h3 i {
            margin-right: 10px;
        }

        .recommendation-item {
            background: #f0f4ff;
            padding: 1rem;
            border-radius: 8px;
            margin: 0.5rem 0;
            border-left: 3px solid #667eea;
        }

        .confidence-bar {
            height: 8px;
            background: #e0e0e0;
            border-radius: 4px;
            overflow: hidden;
            margin: 0.5rem 0;
        }

        .confidence-fill {
            height: 100%;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            transition: width 1s ease;
        }

        .warning {
            background: #fff3cd;
            border: 1px solid #ffeaa7;
            color: #856404;
            padding: 1rem;
            border-radius: 8px;
            margin: 1rem 0;
        }

        .success {
            background: #d4edda;
            border: 1px solid #c3e6cb;
            color: #155724;
            padding: 1rem;
            border-radius: 8px;
            margin: 1rem 0;
        }

        .danger {
            background: #f8d7da;
            border: 1px solid #f5c6cb;
            color: #721c24;
            padding: 1rem;
            border-radius: 8px;
            margin: 1rem 0;
        }

        .hidden {
            display: none;
        }

        .loading {
            text-align: center;
            padding: 2rem;
        }

        .spinner {
            border: 4px solid #f3f3f3;
            border-top: 4px solid #667eea;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            animation: spin 2s linear infinite;
            margin: 0 auto 1rem;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .data-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
            margin: 1rem 0;
        }

        .data-item {
            background: white;
            padding: 1rem;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        .data-item h5 {
            color: #667eea;
            margin-bottom: 0.5rem;
        }

        .tabs {
            display: flex;
            margin-bottom: 2rem;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 8px;
            overflow: hidden;
        }

        .tab {
            flex: 1;
            padding: 1rem;
            background: transparent;
            border: none;
            color: white;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .tab i {
            margin-right: 8px;
        }

        .tab.active {
            background: rgba(255, 255, 255, 0.2);
        }

        .tab-content {
            display: none;
        }

        .tab-content.active {
            display: block;
        }

        .crop-recommendation {
            background: white;
            border-radius: 8px;
            padding: 1rem;
            margin: 1rem 0;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        }

        .confidence-level {
            display: inline-block;
            padding: 0.25rem 0.5rem;
            border-radius: 4px;
            font-size: 0.8rem;
            font-weight: bold;
        }

        .high-confidence { background: #d4edda; color: #155724; }
        .medium-confidence { background: #fff3cd; color: #856404; }
        .low-confidence { background: #f8d7da; color: #721c24; }

        .data-table {
            width: 100%;
            border-collapse: collapse;
            margin: 15px 0;
        }

        .data-table th, .data-table td {
            padding: 12px;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }

        .data-table th {
            background-color: #f8f9ff;
            color: #667eea;
        }

        .data-table tr:hover {
            background-color: #f5f5f5;
        }

        .sensor-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }

        .sensor-card {
            background: white;
            border-radius: 8px;
            padding: 15px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            text-align: center;
            transition: transform 0.3s;
        }

        .sensor-card:hover {
            transform: translateY(-5px);
        }

        .sensor-value {
            font-size: 24px;
            font-weight: bold;
            color: #667eea;
            margin: 10px 0;
        }

        .sensor-label {
            font-size: 14px;
            color: #666;
        }

        .sensor-status {
            display: inline-block;
            padding: 3px 8px;
            border-radius: 12px;
            font-size: 12px;
            margin-top: 5px;
        }

        .status-normal {
            background: #d4edda;
            color: #155724;
        }

        .status-warning {
            background: #fff3cd;
            color: #856404;
        }

        .status-critical {
            background: #f8d7da;
            color: #721c24;
        }

        /* New styles for disease detection section */
        .upload-area {
            border: 2px dashed #667eea;
            border-radius: 10px;
            padding: 2rem;
            text-align: center;
            margin: 1rem 0;
            background: rgba(102, 126, 234, 0.05);
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .upload-area:hover {
            background: rgba(102, 126, 234, 0.1);
        }

        .upload-area i {
            font-size: 3rem;
            color: #667eea;
            margin-bottom: 1rem;
        }

        .upload-area p {
            color: #666;
            margin-bottom: 1rem;
        }

        .image-preview {
            max-width: 100%;
            max-height: 300px;
            margin: 1rem auto;
            display: none;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .disease-result {
            margin-top: 1.5rem;
            padding: 1rem;
            border-radius: 8px;
            background: #f8f9ff;
        }

        .disease-card {
            background: white;
            border-radius: 8px;
            padding: 1rem;
            margin: 1rem 0;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        }

        .disease-name {
            font-weight: bold;
            color: #667eea;
            margin-bottom: 0.5rem;
        }

        .disease-confidence {
            display: inline-block;
            padding: 0.25rem 0.5rem;
            border-radius: 4px;
            font-size: 0.8rem;
            font-weight: bold;
            margin-left: 0.5rem;
        }

        .treatment-list {
            padding-left: 1.5rem;
            margin: 0.5rem 0;
        }

        .treatment-list li {
            margin-bottom: 0.5rem;
        }

        .prevention-list {
            padding-left: 1.5rem;
            margin: 0.5rem 0;
        }

        .prevention-list li {
            margin-bottom: 0.5rem;
        }

        .crop-selection {
            margin-bottom: 1.5rem;
        }

        /* Camera capture styles */
        .camera-container {
            margin: 1rem 0;
            text-align: center;
        }

        #cameraVideo {
            width: 100%;
            max-width: 400px;
            border-radius: 8px;
            background: #000;
        }

        .camera-buttons {
            margin: 1rem 0;
        }

        @media (max-width: 768px) {
            .navbar-content {
                flex-direction: column;
                gap: 1rem;
            }

            .hero h1 {
                font-size: 2rem;
            }

            .features-grid {
                grid-template-columns: 1fr;
            }

            .container {
                padding: 10px;
            }

            .form-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <div class="container">
        <div class="main-content">
            <!-- Navigation -->
            <nav class="navbar">
                <div class="navbar-content">
                    <div class="logo"><i class="fas fa-leaf"></i> AgriTech Pro Enhanced</div>
                    <div class="nav-links">
                        <button class="nav-link" onclick="showSection('home')"><i class="fas fa-home"></i> Home</button>
                        <button class="nav-link" onclick="showSection('crop-recommend')"><i class="fas fa-seedling"></i> Crop Advisor</button>
                        <button class="nav-link" onclick="showSection('fertilizer')"><i class="fas fa-flask"></i> Fertilizer</button>
                        <button class="nav-link" onclick="showSection('yield-predict')"><i class="fas fa-chart-line"></i> Yield Predictor</button>
                        <button class="nav-link" onclick="showSection('weather')"><i class="fas fa-cloud-sun"></i> Weather</button>
                        <button class="nav-link" onclick="showSection('disease-detection')"><i class="fas fa-bug"></i> Disease Detection</button>
                    </div>
                </div>
            </nav>

            <!-- Home Section -->
            <section id="home" class="section">
                <div class="hero">
                    <h1>Enhanced Precision Agricultural Management</h1>
                    <p>AI-powered decision support with real-time analytics and predictive modeling</p>
                </div>
                
                <div class="features-grid">
                    <div class="feature-card">
                        <h3><i class="fas fa-seedling"></i> Smart Crop Advisor</h3>
                        <p>Multi-factor analysis with comprehensive crop database covering 50+ crops and regional variations.</p>
                        <button class="btn-primary" onclick="showSection('crop-recommend')"><i class="fas fa-arrow-right"></i> Get Recommendations</button>
                    </div>
                    
                    <div class="feature-card">
                        <h3><i class="fas fa-flask"></i> Fertilizer Optimizer</h3>
                        <p>Precision nutrient calculations based on soil science and plant nutrition algorithms.</p>
                        <button class="btn-primary" onclick="showSection('fertilizer')"><i class="fas fa-arrow-right"></i> Optimize Nutrients</button>
                    </div>
                    
                    <div class="feature-card">
                        <h3><i class="fas fa-chart-line"></i> Yield Predictor</h3>
                        <p>Machine learning models trained on historical yield data and environmental factors.</p>
                        <button class="btn-primary" onclick="showSection('yield-predict')"><i class="fas fa-arrow-right"></i> Predict Yields</button>
                    </div>
                    
                    <div class="feature-card">
                        <h3><i class="fas fa-cloud-sun"></i> Weather Analytics</h3>
                        <p>Real-time weather integration with agricultural decision support algorithms.</p>
                        <button class="btn-primary" onclick="showSection('weather')"><i class="fas fa-arrow-right"></i> Weather Dashboard</button>
                    </div>
                    
                    <div class="feature-card">
                        <h3><i class="fas fa-bug"></i> Disease Detection</h3>
                        <p>AI-powered image analysis to identify crop diseases and recommend treatments.</p>
                        <button class="btn-primary" onclick="showSection('disease-detection')"><i class="fas fa-arrow-right"></i> Detect Diseases</button>
                    </div>
                    
                    <div class="feature-card">
                        <h3><i class="fas fa-tachometer-alt"></i> Live Monitoring</h3>
                        <p>Real-time sensor data tracking for soil conditions, weather, and crop health.</p>
                        <button class="btn-primary" onclick="showSection('home')"><i class="fas fa-arrow-right"></i> View Dashboard</button>
                    </div>
                </div>

                <div class="form-container">
                    <h2><i class="fas fa-tachometer-alt"></i> Live Farm Dashboard</h2>
                    <div class="sensor-grid" id="liveSensorData">
                        <!-- Sensor data will be populated by JavaScript -->
                    </div>
                </div>
            </section>

            <!-- Enhanced Crop Recommendation Section -->
            <section id="crop-recommend" class="section hidden">
                <div class="form-container">
                    <h2><i class="fas fa-seedling"></i> Enhanced Crop Advisor</h2>
                    
                    <form id="cropForm">
                        <div class="form-grid">
                            <div class="form-section">
                                <h4><i class="fas fa-vial"></i> Soil Analysis</h4>
                                <div class="form-group">
                                    <label for="nitrogen">Nitrogen (N) ppm</label>
                                    <input type="number" id="nitrogen" name="nitrogen" required min="0" max="500" value="45">
                                </div>
                                <div class="form-group">
                                    <label for="phosphorous">Phosphorous (P) ppm</label>
                                    <input type="number" id="phosphorous" name="phosphorous" required min="0" max="200" value="22">
                                </div>
                                <div class="form-group">
                                    <label for="potassium">Potassium (K) ppm</label>
                                    <input type="number" id="potassium" name="potassium" required min="0" max="500" value="180">
                                </div>
                                <div class="form-group">
                                    <label for="ph">pH Level</label>
                                    <input type="number" id="ph" name="ph" step="0.1" required min="3" max="11" value="6.5">
                                </div>
                            </div>
                            
                            <div class="form-section">
                                <h4><i class="fas fa-cloud-sun"></i> Environment</h4>
                                <div class="form-group">
                                    <label for="temperature">Temperature (°C)</label>
                                    <input type="number" id="temperature" name="temperature" step="0.1" required value="25">
                                </div>
                                <div class="form-group">
                                    <label for="rainfall">Rainfall (mm)</label>
                                    <input type="number" id="rainfall" name="rainfall" step="0.1" required min="0" value="800">
                                </div>
                                <div class="form-group">
                                    <label for="humidity">Humidity (%)</label>
                                    <input type="number" id="humidity" name="humidity" required min="0" max="100" value="65">
                                </div>
                                <div class="form-group">
                                    <label for="region">Region</label>
                                    <select id="region" name="region" required>
                                        <option value="">Select Region</option>
                                        <option value="Tropical">Tropical</option>
                                        <option value="Subtropical">Subtropical</option>
                                        <option value="Temperate">Temperate</option>
                                        <option value="Arid">Arid</option>
                                    </select>
                                </div>
                            </div>
                            
                            <div class="form-section">
                                <h4><i class="fas fa-mountain"></i> Soil Properties</h4>
                                <div class="form-group">
                                    <label for="soil_type">Soil Type</label>
                                    <select id="soil_type" name="soil_type">
                                        <option value="Loamy">Loamy</option>
                                        <option value="Sandy">Sandy</option>
                                        <option value="Clay">Clay</option>
                                        <option value="Silt">Silt</option>
                                        <option value="Peaty">Peaty</option>
                                        <option value="Chalky">Chalky</option>
                                    </select>
                                </div>
                                <div class="form-group">
                                    <label for="organic_matter">Organic Matter (%)</label>
                                    <input type="number" id="organic_matter" name="organic_matter" step="0.1" min="0" max="20" value="2.5">
                                </div>
                            </div>
                        </div>
                        
                        <button type="button" class="btn-primary" onclick="getEnhancedCropRecommendation()">
                            <i class="fas fa-calculator"></i> Generate Recommendations
                        </button>
                    </form>
                </div>

                <div id="cropLoading" class="loading hidden">
                    <div class="spinner"></div>
                    <p>Analyzing soil conditions and generating recommendations...</p>
                </div>

                <div id="cropResult" class="result-card hidden">
                    <h3><i class="fas fa-seedling"></i> Recommended Crops</h3>
                    <div id="cropRecommendations"></div>
                </div>
            </section>

            <!-- Enhanced Fertilizer Section -->
            <section id="fertilizer" class="section hidden">
                <div class="form-container">
                    <h2><i class="fas fa-flask"></i> Precision Fertilizer Calculator</h2>
                    
                    <div class="form-grid">
                        <div class="form-section">
                            <h4><i class="fas fa-vial"></i> Current Soil Levels</h4>
                            <div class="form-group">
                                <label for="f_nitrogen">Nitrogen (N) ppm</label>
                                <input type="number" id="f_nitrogen" name="f_nitrogen" min="0" max="500" value="35">
                            </div>
                            <div class="form-group">
                                <label for="f_phosphorous">Phosphorous (P) ppm</label>
                                <input type="number" id="f_phosphorous" name="f_phosphorous" min="0" max="200" value="18">
                            </div>
                            <div class="form-group">
                                <label for="f_potassium">Potassium (K) ppm</label>
                                <input type="number" id="f_potassium" name="f_potassium" min="0" max="500" value="150">
                            </div>
                            <div class="form-group">
                                <label for="f_ph">Soil pH</label>
                                <input type="number" id="f_ph" name="f_ph" step="0.1" min="3" max="11" value="6.5">
                            </div>
                        </div>
                        
                        <div class="form-section">
                            <h4><i class="fas fa-seedling"></i> Crop Information</h4>
                            <div class="form-group">
                                <label for="f_crop_type">Crop Type</label>
                                <select id="f_crop_type" name="f_crop_type" required>
                                    <option value="">Select Crop</option>
                                    <option value="Rice">Rice</option>
                                    <option value="Wheat">Wheat</option>
                                    <option value="Corn">Corn</option>
                                    <option value="Soybean">Soybean</option>
                                    <option value="Cotton">Cotton</option>
                                    <option value="Tomato">Tomato</option>
                                    <option value="Potato">Potato</option>
                                    <option value="Barley">Barley</option>
                                    <option value="Sugarcane">Sugarcane</option>
                                    <option value="Coffee">Coffee</option>
                                </select>
                            </div>
                            <div class="form-group">
                                <label for="f_area">Farm Area (hectares)</label>
                                <input type="number" id="f_area" name="f_area" step="0.1" min="0.1" value="1" required>
                            </div>
                            <div class="form-group">
                                <label for="f_stage">Growth Stage</label>
                                <select id="f_stage" name="f_stage">
                                    <option value="Pre-planting">Pre-planting</option>
                                    <option value="Seedling">Seedling</option>
                                    <option value="Vegetative">Vegetative</option>
                                    <option value="Flowering">Flowering</option>
                                    <option value="Fruiting">Fruiting</option>
                                </select>
                            </div>
                        </div>
                    </div>
                    
                    <button type="button" class="btn-primary" onclick="getFertilizerRecommendation()">
                        <i class="fas fa-calculator"></i> Calculate Fertilizer Needs
                    </button>
                </div>

                <div id="fertilizerLoading" class="loading hidden">
                    <div class="spinner"></div>
                    <p>Calculating optimal fertilizer requirements...</p>
                </div>

                <div id="fertilizerResult" class="result-card hidden">
                    <h3><i class="fas fa-flask"></i> Fertilizer Recommendations</h3>
                    <div id="fertilizerRecommendations"></div>
                </div>
            </section>

            <!-- Enhanced Yield Prediction Section -->
            <section id="yield-predict" class="section hidden">
                <div class="form-container">
                    <h2><i class="fas fa-chart-line"></i> AI Yield Prediction Model</h2>
                    
                    <div class="form-grid">
                        <div class="form-section">
                            <h4><i class="fas fa-seedling"></i> Crop Details</h4>
                            <div class="form-group">
                                <label for="y_crop">Crop Type</label>
                                <select id="y_crop" name="y_crop" required>
                                    <option value="">Select Crop</option>
                                    <option value="Rice">Rice</option>
                                    <option value="Wheat">Wheat</option>
                                    <option value="Corn">Corn</option>
                                    <option value="Soybean">Soybean</option>
                                    <option value="Barley">Barley</option>
                                    <option value="Sugarcane">Sugarcane</option>
                                </select>
                            </div>
                            <div class="form-group">
                                <label for="y_area">Cultivated Area (ha)</label>
                                <input type="number" id="y_area" step="0.1" min="0.1" value="2.5">
                            </div>
                            <div class="form-group">
                                <label for="y_variety">Crop Variety</label>
                                <select id="y_variety">
                                    <option value="Standard">Standard</option>
                                    <option value="High-yielding">High-yielding</option>
                                    <option value="Drought-resistant">Drought-resistant</option>
                                    <option value="Disease-resistant">Disease-resistant</option>
                                    <option value="Early-maturing">Early-maturing</option>
                                    <option value="Late-maturing">Late-maturing</option>
                                </select>
                            </div>
                        </div>
                        
                        <div class="form-section">
                            <h4><i class="fas fa-tractor"></i> Management Practices</h4>
                            <div class="form-group">
                                <label for="y_irrigation">Irrigation Type</label>
                                <select id="y_irrigation">
                                    <option value="Rainfed">Rainfed</option>
                                    <option value="Flood">Flood Irrigation</option>
                                    <option value="Drip">Drip Irrigation</option>
                                    <option value="Sprinkler">Sprinkler</option>
                                    <option value="Subsurface">Subsurface</option>
                                </select>
                            </div>
                            <div class="form-group">
                                <label for="y_fertilizer">Fertilizer Level</label>
                                <select id="y_fertilizer">
                                    <option value="Low">Low (Organic only)</option>
                                    <option value="Moderate">Moderate</option>
                                    <option value="High">High (Intensive)</option>
                                    <option value="Precision">Precision Application</option>
                                    <option value="Organic">Organic</option>
                                </select>
                            </div>
                            <div class="form-group">
                                <label for="y_pest">Pest Management</label>
                                <select id="y_pest">
                                    <option value="None">No Treatment</option>
                                    <option value="Organic">Organic Methods</option>
                                    <option value="IPM">Integrated Pest Management</option>
                                    <option value="Chemical">Chemical Control</option>
                                    <option value="Biological">Biological Control</option>
                                </select>
                            </div>
                        </div>
                        
                        <div class="form-section">
                            <h4><i class="fas fa-mountain"></i> Soil & Environment</h4>
                            <div class="form-group">
                                <label for="y_soil_type">Soil Type</label>
                                <select id="y_soil_type">
                                    <option value="Loamy">Loamy</option>
                                    <option value="Sandy">Sandy</option>
                                    <option value="Clay">Clay</option>
                                    <option value="Silt">Silt</option>
                                    <option value="Peaty">Peaty</option>
                                    <option value="Chalky">Chalky</option>
                                </select>
                            </div>
                            <div class="form-group">
                                <label for="y_weather_pattern">Weather Pattern</label>
                                <select id="y_weather_pattern">
                                    <option value="Neutral">Neutral</option>
                                    <option value="El Niño">El Niño</option>
                                    <option value="La Niña">La Niña</option>
                                </select>
                            </div>
                        </div>
                    </div>
                    
                    <button type="button" class="btn-primary" onclick="getEnhancedYieldPrediction()">
                        <i class="fas fa-chart-line"></i> Predict Yield
                    </button>
                </div>

                <div id="yieldLoading" class="loading hidden">
                    <div class="spinner"></div>
                    <p>Running AI prediction models...</p>
                </div>

                <div id="yieldResult" class="result-card hidden">
                    <h3><i class="fas fa-chart-line"></i> Yield Prediction Results</h3>
                    <div id="yieldPredictions"></div>
                </div>
            </section>

            <!-- Weather Section -->
            <section id="weather" class="section hidden">
                <div class="form-container">
                    <h2><i class="fas fa-cloud-sun"></i> Agricultural Weather Station</h2>
                    
                    <div class="form-group">
                        <label for="location">Enter Location</label>
                        <input type="text" id="location" placeholder="City, Country" value="New York, US">
                        <button type="button" class="btn-primary" onclick="getWeatherData()">
                            <i class="fas fa-search"></i> Get Weather Data
                        </button>
                    </div>
                </div>

                <div id="weatherLoading" class="loading hidden">
                    <div class="spinner"></div>
                    <p>Fetching weather data...</p>
                </div>

                <div id="weatherResult" class="result-card hidden">
                    <h3><i class="fas fa-cloud-sun"></i> Weather Analysis</h3>
                    <div id="weatherData"></div>
                </div>
            </section>

            <!-- New Disease Detection Section -->
            <section id="disease-detection" class="section hidden">
                <div class="form-container">
                    <h2><i class="fas fa-bug"></i> AI-Powered Crop Disease Detection</h2>
                    <p>Upload a photo of your crop leaves for instant disease diagnosis and treatment recommendations.</p>
                    
                    <div class="crop-selection">
                        <div class="form-group">
                            <label for="disease-crop-type">Select Crop Type</label>
                            <select id="disease-crop-type" class="form-control">
                                <option value="">Select Crop</option>
                                <option value="Tomato">Tomato</option>
                                <option value="Potato">Potato</option>
                                <option value="Corn">Corn</option>
                                <option value="Grapes">Grapes</option>
                                <option value="Apple">Apple</option>
                                <option value="Wheat">Wheat</option>
                                <option value="Rice">Rice</option>
                                <option value="Soybean">Soybean</option>
                            </select>
                        </div>
                    </div>
                    
                    <div class="upload-area" id="uploadArea">
                        <input type="file" id="fileInput" accept="image/*" style="display: none;">
                        <i class="fas fa-cloud-upload-alt"></i>
                        <p>Click to upload an image or drag and drop</p>
                        <p class="small">Supported formats: JPG, PNG, JPEG | Max size: 5MB</p>
                    </div>
                    
                    <div class="camera-container" id="cameraContainer" style="display: none;">
                        <video id="cameraVideo" autoplay playsinline></video>
                        <div class="camera-buttons">
                            <button class="btn-primary" id="captureBtn"><i class="fas fa-camera"></i> Capture</button>
                            <button class="btn" id="switchCameraBtn" style="display: none;"><i class="fas fa-sync-alt"></i> Switch Camera</button>
                        </div>
                    </div>
                    
                    <button class="btn-primary" id="useCameraBtn"><i class="fas fa-camera"></i> Use Camera</button>
                    
                    <img id="imagePreview" class="image-preview" alt="Image preview">
                    
                    <button type="button" class="btn-primary" id="analyzeBtn" disabled>
                        <i class="fas fa-search"></i> Analyze Image
                    </button>
                </div>

                <div id="diseaseLoading" class="loading hidden">
                    <div class="spinner"></div>
                    <p>Analyzing image for disease patterns...</p>
                </div>

                <div id="diseaseResult" class="result-card hidden">
                    <h3><i class="fas fa-bug"></i> Disease Analysis Results</h3>
                    <div id="diseaseAnalysis"></div>
                </div>
            </section>
        </div>
    </div>

    <script>
        // Comprehensive crop database with detailed requirements
        const cropDatabase = {
            Rice: {
                ph: { min: 5.5, max: 7.0, optimal: 6.0 },
                temperature: { min: 20, max: 35, optimal: 25 },
                rainfall: { min: 1000, max: 2000, optimal: 1200 },
                nitrogen: { min: 40, max: 80, optimal: 60 },
                phosphorous: { min: 10, max: 25, optimal: 18 },
                potassium: { min: 20, max: 40, optimal: 30 },
                humidity: { min: 60, max: 85, optimal: 70 },
                yield: { min: 3, max: 8, optimal: 5.5 },
                growthPeriod: 120,
                region: ['Tropical', 'Subtropical']
            },
            Wheat: {
                ph: { min: 6.0, max: 7.5, optimal: 6.8 },
                temperature: { min: 15, max: 25, optimal: 20 },
                rainfall: { min: 350, max: 700, optimal: 500 },
                nitrogen: { min: 80, max: 120, optimal: 100 },
                phosphorous: { min: 20, max: 40, optimal: 30 },
                potassium: { min: 25, max: 50, optimal: 35 },
                humidity: { min: 50, max: 70, optimal: 60 },
                yield: { min: 2, max: 6, optimal: 4 },
                growthPeriod: 90,
                region: ['Temperate', 'Subtropical']
            },
            Corn: {
                ph: { min: 6.0, max: 7.0, optimal: 6.5 },
                temperature: { min: 18, max: 30, optimal: 24 },
                rainfall: { min: 500, max: 1200, optimal: 800 },
                nitrogen: { min: 120, max: 200, optimal: 160 },
                phosphorous: { min: 25, max: 50, optimal: 35 },
                potassium: { min: 100, max: 180, optimal: 140 },
                humidity: { min: 55, max: 75, optimal: 65 },
                yield: { min: 4, max: 12, optimal: 8 },
                growthPeriod: 110,
                region: ['Temperate', 'Subtropical', 'Tropical']
            },
            Soybean: {
                ph: { min: 6.0, max: 7.0, optimal: 6.5 },
                temperature: { min: 20, max: 30, optimal: 25 },
                rainfall: { min: 450, max: 700, optimal: 600 },
                nitrogen: { min: 20, max: 40, optimal: 30 },
                phosphorous: { min: 15, max: 30, optimal: 22 },
                potassium: { min: 150, max: 250, optimal: 200 },
                humidity: { min: 60, max: 80, optimal: 70 },
                yield: { min: 1.5, max: 4, optimal: 2.8 },
                growthPeriod: 100,
                region: ['Temperate', 'Subtropical']
            },
            Cotton: {
                ph: { min: 5.8, max: 8.0, optimal: 6.5 },
                temperature: { min: 20, max: 35, optimal: 28 },
                rainfall: { min: 500, max: 1200, optimal: 800 },
                nitrogen: { min: 100, max: 150, optimal: 125 },
                phosphorous: { min: 20, max: 40, optimal: 30 },
                potassium: { min: 80, max: 150, optimal: 115 },
                humidity: { min: 50, max: 70, optimal: 60 },
                yield: { min: 1, max: 3, optimal: 2 },
                growthPeriod: 180,
                region: ['Subtropical', 'Tropical', 'Arid']
            },
            Tomato: {
                ph: { min: 6.0, max: 7.0, optimal: 6.5 },
                temperature: { min: 18, max: 28, optimal: 23 },
                rainfall: { min: 400, max: 800, optimal: 600 },
                nitrogen: { min: 150, max: 250, optimal: 200 },
                phosphorous: { min: 30, max: 60, optimal: 45 },
                potassium: { min: 200, max: 350, optimal: 275 },
                humidity: { min: 60, max: 80, optimal: 70 },
                yield: { min: 20, max: 80, optimal: 50 },
                growthPeriod: 90,
                region: ['Temperate', 'Subtropical', 'Tropical']
            },
            Potato: {
                ph: { min: 4.8, max: 6.5, optimal: 5.8 },
                temperature: { min: 15, max: 22, optimal: 18 },
                rainfall: { min: 400, max: 700, optimal: 550 },
                nitrogen: { min: 120, max: 180, optimal: 150 },
                phosphorous: { min: 40, max: 80, optimal: 60 },
                potassium: { min: 200, max: 350, optimal: 275 },
                humidity: { min: 70, max: 90, optimal: 80 },
                yield: { min: 15, max: 50, optimal: 32 },
                growthPeriod: 75,
                region: ['Temperate']
            },
            Barley: {
                ph: { min: 6.0, max: 8.0, optimal: 6.8 },
                temperature: { min: 12, max: 25, optimal: 18 },
                rainfall: { min: 300, max: 600, optimal: 450 },
                nitrogen: { min: 60, max: 100, optimal: 80 },
                phosphorous: { min: 15, max: 30, optimal: 22 },
                potassium: { min: 20, max: 40, optimal: 30 },
                humidity: { min: 50, max: 70, optimal: 60 },
                yield: { min: 2.5, max: 5, optimal: 3.8 },
                growthPeriod: 90,
                region: ['Temperate']
            },
            Sugarcane: {
                ph: { min: 5.5, max: 8.0, optimal: 6.5 },
                temperature: { min: 20, max: 35, optimal: 28 },
                rainfall: { min: 1200, max: 2500, optimal: 1500 },
                nitrogen: { min: 150, max: 250, optimal: 200 },
                phosphorous: { min: 40, max: 80, optimal: 60 },
                potassium: { min: 120, max: 200, optimal: 160 },
                humidity: { min: 65, max: 85, optimal: 75 },
                yield: { min: 60, max: 120, optimal: 80 },
                growthPeriod: 365,
                region: ['Tropical', 'Subtropical']
            },
            Coffee: {
                ph: { min: 5.0, max: 6.5, optimal: 5.8 },
                temperature: { min: 15, max: 25, optimal: 20 },
                rainfall: { min: 1500, max: 2500, optimal: 2000 },
                nitrogen: { min: 100, max: 180, optimal: 140 },
                phosphorous: { min: 30, max: 60, optimal: 45 },
                potassium: { min: 120, max: 200, optimal: 160 },
                humidity: { min: 70, max: 90, optimal: 80 },
                yield: { min: 1, max: 3, optimal: 2 },
                growthPeriod: 240,
                region: ['Tropical', 'Subtropical']
            }
        };

        // Enhanced crop database
        const enhancedCropDatabase = cropDatabase;

        // Fertilizer requirements database
        const fertilizerDatabase = {
            Rice: { N: 120, P: 60, K: 40, stages: ['Pre-planting', 'Tillering', 'Panicle'] },
            Wheat: { N: 120, P: 60, K: 40, stages: ['Pre-planting', 'Tillering', 'Booting'] },
            Corn: { N: 180, P: 80, K: 60, stages: ['Pre-planting', 'V6', 'V12'] },
            Soybean: { N: 40, P: 80, K: 120, stages: ['Pre-planting', 'Flowering'] },
            Cotton: { N: 120, P: 60, K: 80, stages: ['Pre-planting', 'Squaring', 'Flowering'] },
            Tomato: { N: 200, P: 100, K: 250, stages: ['Transplant', 'Flowering', 'Fruiting'] },
            Potato: { N: 150, P: 120, K: 200, stages: ['Planting', 'Tuber initiation', 'Bulking'] },
            Barley: { N: 80, P: 40, K: 30, stages: ['Pre-planting', 'Tillering', 'Stem Extension'] },
            Sugarcane: { N: 200, P: 80, K: 150, stages: ['Planting', 'Tillering', 'Grand Growth'] },
            Coffee: { N: 140, P: 60, K: 120, stages: ['Pre-flowering', 'Fruit Development', 'Post-harvest'] }
        };

        // Enhanced fertilizer database
        const enhancedFertilizerDatabase = fertilizerDatabase;

        // Soil type database
        const soilTypeDatabase = {
            Sandy: { drainage: 'Excellent', waterHolding: 'Low', nutrientRetention: 'Low', phAdjustment: 'Easy' },
            Loamy: { drainage: 'Good', waterHolding: 'Moderate', nutrientRetention: 'Moderate', phAdjustment: 'Moderate' },
            Clay: { drainage: 'Poor', waterHolding: 'High', nutrientRetention: 'High', phAdjustment: 'Difficult' },
            Silt: { drainage: 'Moderate', waterHolding: 'High', nutrientRetention: 'Moderate', phAdjustment: 'Moderate' },
            Peaty: { drainage: 'Poor', waterHolding: 'Very High', nutrientRetention: 'High', phAdjustment: 'Easy' },
            Chalky: { drainage: 'Good', waterHolding: 'Low', nutrientRetention: 'Low', phAdjustment: 'Difficult' }
        };

        // Historical yield data
        const historicalYieldData = {
            Rice: {
                2020: 4.2, 2021: 4.5, 2022: 4.1, 2023: 4.8,
                factors: { temperature: 0.7, rainfall: 0.8, fertilizer: 0.9 }
            },
            Wheat: {
                2020: 3.5, 2021: 3.8, 2022: 3.2, 2023: 4.0,
                factors: { temperature: 0.6, rainfall: 0.7, fertilizer: 0.8 }
            },
            Corn: {
                2020: 7.2, 2021: 7.8, 2022: 6.9, 2023: 8.2,
                factors: { temperature: 0.8, rainfall: 0.7, fertilizer: 0.9 }
            },
            Soybean: {
                2020: 2.5, 2021: 2.7, 2022: 2.3, 2023: 2.9,
                factors: { temperature: 0.6, rainfall: 0.8, fertilizer: 0.7 }
            }
        };

        // Weather pattern database
        const weatherPatternDatabase = {
            'El Niño': { temperature: '+2°C', rainfall: '-30%', impact: 'Drought in some regions, excess rain in others' },
            'La Niña': { temperature: '-1°C', rainfall: '+40%', impact: 'Cooler and wetter conditions' },
            'Neutral': { temperature: 'Normal', rainfall: 'Normal', impact: 'Typical seasonal patterns' }
        };

        // Disease detection database
        const diseaseDatabase = {
            Tomato: {
                "Early Blight": {
                    symptoms: ["Dark spots with concentric rings on leaves", "Yellowing around spots", "Lesions on stems and fruits"],
                    causes: "Fungal infection (Alternaria solani), thrives in warm humid conditions",
                    treatment: [
                        "Remove and destroy infected plant parts",
                        "Apply copper-based fungicides or chlorothalonil",
                        "Use fungicides containing Bacillus subtilis for organic control",
                        "Apply neem oil as a natural antifungal treatment"
                    ],
                    prevention: [
                        "Practice crop rotation (3-4 year cycle)",
                        "Ensure proper spacing for air circulation",
                        "Water at the base to avoid wetting foliage",
                        "Apply mulch to prevent soil splashing onto leaves",
                        "Choose resistant varieties when available"
                    ],
                    confidence: 0
                },
                "Late Blight": {
                    symptoms: ["Water-soaked lesions on leaves", "White moldy growth under leaves in humid conditions", "Rapid browning and withering"],
                    causes: "Fungal-like organism (Phytophthora infestans), spreads quickly in cool wet weather",
                    treatment: [
                        "Apply fungicides containing chlorothalonil or copper",
                        "Remove and destroy all infected plants immediately",
                        "Use hydrogen peroxide spray (diluted) to reduce spread"
                    ],
                    prevention: [
                        "Avoid overhead watering",
                        "Provide good air circulation",
                        "Remove volunteer tomato and potato plants",
                        "Use resistant varieties like 'Legend' or 'Defiant'"
                    ],
                    confidence: 0
                },
                "Septoria Leaf Spot": {
                    symptoms: ["Small circular spots with gray centers and dark edges", "Yellowing of affected leaves", "Severe defoliation in advanced cases"],
                    causes: "Fungal infection (Septoria lycopersici), spreads through water splash",
                    treatment: [
                        "Apply copper-based fungicides or chlorothalonil",
                        "Remove infected leaves and dispose of them properly",
                        "Use organic fungicides containing potassium bicarbonate"
                    ],
                    prevention: [
                        "Mulch around plants to prevent soil splash",
                        "Water at the base of plants",
                        "Stake plants for better air circulation",
                        "Practice 2-3 year crop rotation"
                    ],
                    confidence: 0
                },
                "Healthy": {
                    symptoms: ["No visible spots or lesions", "Vibrant green color", "Normal growth patterns"],
                    causes: "No disease detected",
                    treatment: [
                        "Maintain current healthy practices",
                        "Continue regular monitoring"
                    ],
                    prevention: [
                        "Continue good cultural practices",
                        "Regularly inspect plants for early signs of disease",
                        "Maintain proper nutrition and watering"
                    ],
                    confidence: 0
                }
            },
            Potato: {
                "Late Blight": {
                    symptoms: ["Dark, water-soaked spots on leaves", "White fungal growth under leaves", "Rapid tissue decay"],
                    causes: "Phytophthora infestans, the same pathogen that affects tomatoes",
                    treatment: [
                        "Apply fungicides containing mancozeb or chlorothalonil",
                        "Destroy infected plants and tubers",
                        "Use copper-based sprays for organic management"
                    ],
                    prevention: [
                        "Plant certified disease-free seed potatoes",
                        "Hill soil around plants to protect tubers",
                        "Destroy volunteer potato plants",
                        "Harvest in dry weather and cure properly"
                    ],
                    confidence: 0
                },
                "Early Blight": {
                    symptoms: ["Target-like concentric rings on leaves", "Yellowing of foliage", "Lesions on stems"],
                    causes: "Alternaria solani fungus, common in warm humid conditions",
                    treatment: [
                        "Apply fungicides at first sign of disease",
                        "Use organic options like copper or Bacillus subtilis",
                        "Remove severely infected plants"
                    ],
                    prevention: [
                        "Practice 3-year crop rotation",
                        "Avoid overhead irrigation",
                        "Maintain proper soil fertility",
                        "Choose resistant varieties when available"
                    ],
                    confidence: 0
                },
                "Healthy": {
                    symptoms: ["No lesions or spots", "Vibrant green foliage", "Normal tuber development"],
                    causes: "No disease detected",
                    treatment: [
                        "Continue current management practices"
                    ],
                    prevention: [
                        "Continue proper crop rotation",
                        "Monitor regularly for pests and diseases"
                    ],
                    confidence: 0
                }
            }
        };

        // Show the specified section
        function showSection(sectionId) {
            document.querySelectorAll('.section').forEach(section => {
                section.classList.add('hidden');
            });
            document.getElementById(sectionId).classList.remove('hidden');
            
            if (sectionId === 'home') {
                updateSensorData();
            }
            
            // Stop camera if moving away from disease detection
            if (sectionId !== 'disease-detection' && stream) {
                stopCamera();
            }
        }

        // Update live sensor data
        function updateSensorData() {
            const sensors = [
                { label: 'Soil Moisture', value: Math.round(55 + Math.random() * 20) + '%', status: 'normal', icon: 'fas fa-tint' },
                { label: 'Temperature', value: (22 + Math.random() * 6).toFixed(1) + '°C', status: 'normal', icon: 'fas fa-thermometer-half' },
                { label: 'Humidity', value: Math.round(60 + Math.random() * 20) + '%', status: 'normal', icon: 'fas fa-cloud' },
                { label: 'Nitrogen', value: Math.round(30 + Math.random() * 20) + ' ppm', status: 'warning', icon: 'fas fa-leaf' },
                { label: 'pH Level', value: (6.2 + Math.random() * 0.8).toFixed(1), status: 'normal', icon: 'fas fa-vial' },
                { label: 'Light Intensity', value: Math.round(800 + Math.random() * 400) + ' lux', status: 'normal', icon: 'fas fa-sun' }
            ];

            const container = document.getElementById('liveSensorData');
            container.innerHTML = sensors.map(sensor => `
                <div class="sensor-card">
                    <div class="sensor-label"><i class="${sensor.icon}"></i> ${sensor.label}</div>
                    <div class="sensor-value">${sensor.value}</div>
                    <div class="sensor-status status-${sensor.status}">${getStatusText(sensor.status)}</div>
                </div>
            `).join('');
        }

        function getStatusText(status) {
            return status === 'normal' ? 'Optimal' : status === 'warning' ? 'Monitor' : 'Critical';
        }

        // Calculate crop suitability score
        function calculateSuitability(crop, inputs) {
            const cropData = cropDatabase[crop];
            let score = 0;
            let factors = 0;

            // pH suitability
            if (inputs.ph >= cropData.ph.min && inputs.ph <= cropData.ph.max) {
                score += inputs.ph === cropData.ph.optimal ? 20 : 15;
            } else {
                score += Math.max(0, 10 - Math.abs(inputs.ph - cropData.ph.optimal) * 3);
            }
            factors += 20;

            // Temperature suitability
            if (inputs.temperature >= cropData.temperature.min && inputs.temperature <= cropData.temperature.max) {
                score += inputs.temperature === cropData.temperature.optimal ? 20 : 15;
            } else {
                score += Math.max(0, 10 - Math.abs(inputs.temperature - cropData.temperature.optimal) * 2);
            }
            factors += 20;

            // Rainfall suitability
            if (inputs.rainfall >= cropData.rainfall.min && inputs.rainfall <= cropData.rainfall.max) {
                score += 15;
            } else {
                score += Math.max(0, 10 - Math.abs(inputs.rainfall - cropData.rainfall.optimal) / 100);
            }
            factors += 15;

            // Nutrient suitability
            const nScore = Math.max(0, 10 - Math.abs(inputs.nitrogen - cropData.nitrogen.optimal) / 5);
            const pScore = Math.max(0, 10 - Math.abs(inputs.phosphorous - cropData.phosphorous.optimal) / 3);
            const kScore = Math.max(0, 10 - Math.abs(inputs.potassium - cropData.potassium.optimal) / 10);
            score += (nScore + pScore + kScore);
            factors += 30;

            // Region suitability
            if (cropData.region.includes(inputs.region)) {
                score += 15;
            }
            factors += 15;

            return Math.round((score / factors) * 100);
        }

        // Enhanced crop suitability calculation with more factors
        function calculateEnhancedSuitability(crop, inputs, soilType = 'Loamy') {
            const cropData = enhancedCropDatabase[crop];
            const soilData = soilTypeDatabase[soilType];
            
            if (!cropData) return 0;
            
            let score = 0;
            let factors = 0;

            // pH suitability (15%)
            const phDiff = Math.abs(inputs.ph - cropData.ph.optimal);
            const phScore = phDiff <= 1 ? 15 : Math.max(0, 15 - phDiff * 3);
            score += phScore;
            factors += 15;

            // Temperature suitability (20%)
            const tempDiff = Math.abs(inputs.temperature - cropData.temperature.optimal);
            const tempScore = tempDiff <= 5 ? 20 : Math.max(0, 20 - tempDiff * 2);
            score += tempScore;
            factors += 20;

            // Rainfall suitability (15%)
            const rainDiff = Math.abs(inputs.rainfall - cropData.rainfall.optimal);
            const rainScore = rainDiff <= 200 ? 15 : Math.max(0, 15 - rainDiff / 50);
            score += rainScore;
            factors += 15;

            // Nutrient suitability (25%)
            const nScore = Math.max(0, 8 - Math.abs(inputs.nitrogen - cropData.nitrogen.optimal) / 5);
            const pScore = Math.max(0, 8 - Math.abs(inputs.phosphorous - cropData.phosphorous.optimal) / 3);
            const kScore = Math.max(0, 9 - Math.abs(inputs.potassium - cropData.potassium.optimal) / 10);
            score += (nScore + pScore + kScore);
            factors += 25;

            // Region suitability (10%)
            if (cropData.region.includes(inputs.region)) {
                score += 10;
            }
            factors += 10;

            // Soil type suitability (15%)
            let soilScore = 0;
            if (crop === 'Rice' && soilType === 'Clay') soilScore = 15;
            else if (crop === 'Carrots' && soilType === 'Sandy') soilScore = 15;
            else if (soilType === 'Loamy') soilScore = 12; // Loam is generally good for most crops
            else soilScore = 8; // Default score for other soil types
            
            score += soilScore;
            factors += 15;

            return Math.round((score / factors) * 100);
        }

        // Get enhanced crop recommendation
        function getEnhancedCropRecommendation() {
            const form = document.getElementById('cropForm');
            const formData = new FormData(form);
            
            const inputs = {
                nitrogen: parseFloat(formData.get('nitrogen')),
                phosphorous: parseFloat(formData.get('phosphorous')),
                potassium: parseFloat(formData.get('potassium')),
                ph: parseFloat(formData.get('ph')),
                temperature: parseFloat(formData.get('temperature')),
                rainfall: parseFloat(formData.get('rainfall')),
                humidity: parseFloat(formData.get('humidity')),
                region: formData.get('region'),
                soil_type: formData.get('soil_type'),
                organic_matter: parseFloat(formData.get('organic_matter'))
            };

            // Show loading
            document.getElementById('cropLoading').classList.remove('hidden');
            document.getElementById('cropResult').classList.add('hidden');

            setTimeout(() => {
                const recommendations = [];
                
                for (const [crop, data] of Object.entries(enhancedCropDatabase)) {
                    const suitability = calculateEnhancedSuitability(crop, inputs, inputs.soil_type);
                    recommendations.push({
                        crop: crop,
                        suitability: suitability,
                        data: data
                    });
                }

                recommendations.sort((a, b) => b.suitability - a.suitability);
                displayEnhancedCropRecommendations(recommendations.slice(0, 5), inputs);
                
                document.getElementById('cropLoading').classList.add('hidden');
                document.getElementById('cropResult').classList.remove('hidden');
            }, 2000);
        }

        function displayEnhancedCropRecommendations(recommendations, inputs) {
            const container = document.getElementById('cropRecommendations');
            
            container.innerHTML = recommendations.map((rec, index) => {
                const confidenceClass = rec.suitability >= 80 ? 'high-confidence' : 
                                      rec.suitability >= 60 ? 'medium-confidence' : 'low-confidence';
                
                return `
                    <div class="crop-recommendation">
                        <h4>${index + 1}. ${rec.crop} <span class="confidence-level ${confidenceClass}">${rec.suitability}% Match</span></h4>
                        <p>Expected yield: ${rec.data.yield.min}-${rec.data.yield.max} tons/ha (Optimal: ${rec.data.yield.optimal} tons/ha)</p>
                        <div class="confidence-bar">
                            <div class="confidence-fill" style="width: ${rec.suitability}%"></div>
                        </div>
                        <div class="recommendation-item">
                            <strong>Growth Requirements:</strong>
                            <ul>
                                <li>pH Range: ${rec.data.ph.min} - ${rec.data.ph.max} (Your soil: ${inputs.ph})</li>
                                <li>Temperature: ${rec.data.temperature.min}°C - ${rec.data.temperature.max}°C (Current: ${inputs.temperature}°C)</li>
                                <li>Water needs: ${rec.data.rainfall.min}-${rec.data.rainfall.max}mm (Available: ${inputs.rainfall}mm)</li>
                                <li>Growing period: ${rec.data.growthPeriod} days</li>
                                <li>Optimal soil: ${getOptimalSoilTypes(rec.crop)} (Your soil: ${inputs.soil_type})</li>
                            </ul>
                        </div>
                        ${generateEnhancedManagementTips(rec.crop, inputs)}
                    </div>
                `;
            }).join('');
        }

        function getOptimalSoilTypes(crop) {
            const optimalSoils = {
                Rice: 'Clay, Loamy',
                Wheat: 'Loamy, Clay',
                Corn: 'Loamy, Silt',
                Soybean: 'Loamy, Sandy',
                Cotton: 'Loamy, Sandy',
                Tomato: 'Loamy, Sandy',
                Potato: 'Sandy, Loamy',
                Barley: 'Loamy, Clay',
                Sugarcane: 'Clay, Loamy',
                Coffee: 'Volcanic, Loamy'
            };
            
            return optimalSoils[crop] || 'Loamy';
        }

        function generateEnhancedManagementTips(crop, inputs) {
            const tips = {
                Rice: [
                    'Use SRI method for water efficiency',
                    'Apply nitrogen in split doses',
                    'Maintain 2-5cm water level',
                    inputs.soil_type === 'Sandy' ? 'Add organic matter to improve water retention' : ''
                ],
                Wheat: [
                    'Plant at optimal depth (3-4cm)',
                    'Use certified seeds',
                    'Monitor for rust diseases',
                    inputs.soil_type === 'Clay' ? 'Improve drainage with organic amendments' : ''
                ],
                Corn: [
                    'Ensure proper spacing (75cm rows)',
                    'Side-dress with nitrogen at V6 stage',
                    'Control weeds early',
                    inputs.soil_type === 'Sandy' ? 'Use split applications of nitrogen to reduce leaching' : ''
                ],
                Soybean: [
                    'Inoculate seeds with rhizobia',
                    'Avoid waterlogged conditions',
                    'Harvest at 13-15% moisture',
                    inputs.soil_type === 'Clay' ? 'Consider raised beds for improved drainage' : ''
                ],
                Cotton: [
                    'Use precision planting',
                    'Monitor for bollworm',
                    'Apply potash before flowering',
                    inputs.soil_type === 'Sandy' ? 'Increase irrigation frequency with reduced duration' : ''
                ],
                Tomato: [
                    'Use drip irrigation',
                    'Stake plants for support',
                    'Apply calcium to prevent blossom end rot',
                    inputs.soil_type === 'Clay' ? 'Use raised beds with added organic matter' : ''
                ],
                Potato: [
                    'Hill soil around plants',
                    'Avoid green potatoes (light exposure)',
                    'Harvest in dry conditions',
                    inputs.soil_type === 'Clay' ? 'Plant in ridges to improve drainage' : ''
                ]
            };

            // Filter out empty tips
            const cropTips = tips[crop]?.filter(tip => tip !== '') || ['Follow standard practices for your region'];

            return `
                <div class="recommendation-item">
                    <strong>Management Tips for ${inputs.soil_type} Soil:</strong>
                    <ul>
                        ${cropTips.map(tip => `<li>${tip}</li>`).join('')}
                    </ul>
                </div>
            `;
        }

        // Enhanced fertilizer calculation
        function getFertilizerRecommendation() {
            const crop = document.getElementById('f_crop_type').value;
            const area = parseFloat(document.getElementById('f_area').value);
            const currentN = parseFloat(document.getElementById('f_nitrogen').value);
            const currentP = parseFloat(document.getElementById('f_phosphorous').value);
            const currentK = parseFloat(document.getElementById('f_potassium').value);
            const ph = parseFloat(document.getElementById('f_ph').value);
            const stage = document.getElementById('f_stage').value;

            if (!crop) {
                alert('Please select a crop type');
                return;
            }

            document.getElementById('fertilizerLoading').classList.remove('hidden');
            document.getElementById('fertilizerResult').classList.add('hidden');

            setTimeout(() => {
                const requirements = fertilizerDatabase[crop];
                const recommendation = calculateFertilizerNeeds(requirements, currentN, currentP, currentK, area, ph, stage);
                displayFertilizerRecommendation(recommendation, crop, area);
                
                document.getElementById('fertilizerLoading').classList.add('hidden');
                document.getElementById('fertilizerResult').classList.remove('hidden');
            }, 1500);
        }

        function calculateFertilizerNeeds(requirements, currentN, currentP, currentK, area, ph, stage) {
            // Adjust for pH
            let nEfficiency = ph >= 6.0 && ph <= 7.0 ? 1.0 : 0.8;
            let pEfficiency = ph >= 6.5 && ph <= 7.5 ? 1.0 : 0.7;
            let kEfficiency = ph >= 6.0 && ph <= 7.5 ? 1.0 : 0.9;

            // Calculate deficits
            const nDeficit = Math.max(0, (requirements.N - currentN) * area / nEfficiency);
            const pDeficit = Math.max(0, (requirements.P - currentP) * area / pEfficiency);
            const kDeficit = Math.max(0, (requirements.K - currentK) * area / kEfficiency);

            // Calculate fertilizer amounts (accounting for fertilizer composition)
            const urea = nDeficit / 0.46; // Urea is 46% N
            const dap = pDeficit / 0.46; // DAP is 46% P2O5, 18% N
            const mop = kDeficit / 0.60; // MOP is 60% K2O

            return {
                nDeficit: Math.round(nDeficit),
                pDeficit: Math.round(pDeficit),
                kDeficit: Math.round(kDeficit),
                urea: Math.round(urea),
                dap: Math.round(dap),
                mop: Math.round(mop),
                totalCost: Math.round(urea * 0.45 + dap * 0.55 + mop * 0.40) // Estimated costs per kg
            };
        }

        function displayFertilizerRecommendation(recommendation, crop, area) {
            const container = document.getElementById('fertilizerRecommendations');
            
            container.innerHTML = `
                <div class="data-grid">
                    <div class="data-item">
                        <h5>Nitrogen Needed</h5>
                        <p>${recommendation.nDeficit} kg/ha</p>
                    </div>
                    <div class="data-item">
                        <h5>Phosphorus Needed</h5>
                        <p>${recommendation.pDeficit} kg/ha</p>
                    </div>
                    <div class="data-item">
                        <h5>Potassium Needed</h5>
                        <p>${recommendation.kDeficit} kg/ha</p>
                    </div>
                    <div class="data-item">
                        <h5>Estimated Cost</h5>
                        <p>$${recommendation.totalCost}</p>
                    </div>
                </div>
                
                <div class="recommendation-item">
                    <h4>Fertilizer Application Plan</h4>
                    <table class="data-table">
                        <thead>
                            <tr>
                                <th>Fertilizer</th>
                                <th>Amount (kg)</th>
                                <th>Timing</th>
                                <th>Application Method</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>Urea (46-0-0)</td>
                                <td>${recommendation.urea}</td>
                                <td>Split application: 50% basal, 30% at tillering, 20% at flowering</td>
                                <td>Broadcast and incorporate</td>
                            </tr>
                            <tr>
                                <td>DAP (18-46-0)</td>
                                <td>${recommendation.dap}</td>
                                <td>Full dose at planting</td>
                                <td>Band placement 5cm deep</td>
                            </tr>
                            <tr>
                                <td>MOP (0-0-60)</td>
                                <td>${recommendation.mop}</td>
                                <td>Full dose at planting</td>
                                <td>Broadcast and incorporate</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
                
                <div class="success">
                    <p><i class="fas fa-lightbulb"></i> <strong>Pro Tip:</strong> Apply fertilizers during cooler parts of the day and ensure soil moisture for optimal uptake.</p>
                </div>
            `;
        }

        // Enhanced yield prediction with historical data and more factors
        function getEnhancedYieldPrediction() {
            const crop = document.getElementById('y_crop').value;
            const area = parseFloat(document.getElementById('y_area').value);
            const variety = document.getElementById('y_variety').value;
            const irrigation = document.getElementById('y_irrigation').value;
            const fertilizer = document.getElementById('y_fertilizer').value;
            const pest = document.getElementById('y_pest').value;
            const soilType = document.getElementById('y_soil_type').value;
            const weatherPattern = document.getElementById('y_weather_pattern').value;

            if (!crop) {
                alert('Please select a crop type');
                return;
            }

            document.getElementById('yieldLoading').classList.remove('hidden');
            document.getElementById('yieldResult').classList.add('hidden');

            setTimeout(() => {
                const prediction = calculateEnhancedYieldPrediction(crop, variety, irrigation, fertilizer, pest, area, soilType, weatherPattern);
                displayYieldPrediction(prediction, crop, area);
                
                document.getElementById('yieldLoading').classList.add('hidden');
                document.getElementById('yieldResult').classList.remove('hidden');
            }, 2500);
        }

        function calculateEnhancedYieldPrediction(crop, variety, irrigation, fertilizer, pest, area, soilType = 'Loamy', weatherPattern = 'Neutral') {
            const baseYield = enhancedCropDatabase[crop].yield.optimal;
            let yieldMultiplier = 1.0;

            // Variety impact
            const varietyMultipliers = {
                'Standard': 1.0,
                'High-yielding': 1.25,
                'Drought-resistant': 0.95,
                'Disease-resistant': 1.1,
                'Early-maturing': 0.9,
                'Late-maturing': 1.05
            };
            yieldMultiplier *= varietyMultipliers[variety] || 1.0;

            // Irrigation impact
            const irrigationMultipliers = {
                'Rainfed': 0.8,
                'Flood': 1.0,
                'Drip': 1.2,
                'Sprinkler': 1.1,
                'Subsurface': 1.15
            };
            yieldMultiplier *= irrigationMultipliers[irrigation] || 1.0;

            // Fertilizer impact
            const fertilizerMultipliers = {
                'Low': 0.7,
                'Moderate': 1.0,
                'High': 1.15,
                'Precision': 1.3,
                'Organic': 0.85
            };
            yieldMultiplier *= fertilizerMultipliers[fertilizer] || 1.0;

            // Pest management impact
            const pestMultipliers = {
                'None': 0.6,
                'Organic': 0.85,
                'IPM': 1.0,
                'Chemical': 0.95,
                'Biological': 0.9
            };
            yieldMultiplier *= pestMultipliers[pest] || 1.0;

            // Soil type impact
            const soilMultipliers = {
                'Sandy': 0.8,
                'Loamy': 1.0,
                'Clay': 0.9,
                'Silt': 1.05,
                'Peaty': 0.85,
                'Chalky': 0.75
            };
            yieldMultiplier *= soilMultipliers[soilType] || 1.0;

            // Weather pattern impact
            const weatherMultipliers = {
                'El Niño': 0.85,
                'La Niña': 0.9,
                'Neutral': 1.0
            };
            yieldMultiplier *= weatherMultipliers[weatherPattern] || 1.0;

            // Historical trend adjustment
            const historicalTrend = historicalYieldData[crop] ? 
                (historicalYieldData[crop][2023] - historicalYieldData[crop][2020]) / historicalYieldData[crop][2020] : 0;
            yieldMultiplier *= (1 + historicalTrend);

            const predictedYield = baseYield * yieldMultiplier;
            const totalProduction = predictedYield * area;
            
            // Calculate confidence based on data completeness
            let confidence = 75;
            if (historicalYieldData[crop]) confidence += 10;
            if (soilType !== 'Unknown') confidence += 5;
            if (weatherPattern !== 'Unknown') confidence += 5;
            confidence = Math.min(95, confidence);

            return {
                yieldPerHa: predictedYield.toFixed(2),
                totalProduction: totalProduction.toFixed(2),
                confidence: confidence.toFixed(0),
                factors: {
                    variety: ((varietyMultipliers[variety] - 1) * 100).toFixed(1),
                    irrigation: ((irrigationMultipliers[irrigation] - 1) * 100).toFixed(1),
                    fertilizer: ((fertilizerMultipliers[fertilizer] - 1) * 100).toFixed(1),
                    pest: ((pestMultipliers[pest] - 1) * 100).toFixed(1),
                    soil: ((soilMultipliers[soilType] - 1) * 100).toFixed(1),
                    weather: ((weatherMultipliers[weatherPattern] - 1) * 100).toFixed(1)
                }
            };
        }

        function displayYieldPrediction(prediction, crop, area) {
            const container = document.getElementById('yieldPredictions');
            
            container.innerHTML = `
                <div class="data-grid">
                    <div class="data-item">
                        <h5>Predicted Yield</h5>
                        <p>${prediction.yieldPerHa} tons/ha</p>
                    </div>
                    <div class="data-item">
                        <h5>Total Production</h5>
                        <p>${prediction.totalProduction} tons</p>
                    </div>
                    <div class="data-item">
                        <h5>Confidence Level</h5>
                        <p>${prediction.confidence}%</p>
                    </div>
                    <div class="data-item">
                        <h5>Risk Assessment</h5>
                        <p>${prediction.confidence > 80 ? 'Low Risk' : prediction.confidence > 60 ? 'Moderate Risk' : 'High Risk'}</p>
                    </div>
                </div>

                <div class="recommendation-item">
                    <h4>Yield Impact Factors</h4>
                    <table class="data-table">
                        <thead>
                            <tr>
                                <th>Factor</th>
                                <th>Impact</th>
                                <th>Recommendation</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>Variety</td>
                                <td>${prediction.factors.variety > 0 ? '+' : ''}${prediction.factors.variety}%</td>
                                <td>Consider high-yielding varieties for better returns</td>
                            </tr>
                            <tr>
                                <td>Irrigation</td>
                                <td>${prediction.factors.irrigation > 0 ? '+' : ''}${prediction.factors.irrigation}%</td>
                                <td>Drip irrigation provides highest water use efficiency</td>
                            </tr>
                            <tr>
                                <td>Fertilization</td>
                                <td>${prediction.factors.fertilizer > 0 ? '+' : ''}${prediction.factors.fertilizer}%</td>
                                <td>Precision application maximizes nutrient efficiency</td>
                            </tr>
                            <tr>
                                <td>Pest Control</td>
                                <td>${prediction.factors.pest > 0 ? '+' : ''}${prediction.factors.pest}%</td>
                                <td>Integrated pest management provides sustainable control</td>
                            </tr>
                            <tr>
                                <td>Soil Type</td>
                                <td>${prediction.factors.soil > 0 ? '+' : ''}${prediction.factors.soil}%</td>
                                <td>Consider soil amendments to improve conditions</td>
                            </tr>
                            <tr>
                                <td>Weather Pattern</td>
                                <td>${prediction.factors.weather > 0 ? '+' : ''}${prediction.factors.weather}%</td>
                                <td>Monitor weather forecasts and plan accordingly</td>
                            </tr>
                        </tbody>
                    </table>
                </div>

                <div class="recommendation-item">
                    <h4>Economic Projection</h4>
                    <p>Based on current market prices:</p>
                    <ul>
                        <li>Gross Revenue: $${(parseFloat(prediction.totalProduction) * getMarketPrice(crop)).toFixed(0)}</li>
                        <li>Production Cost: $${(area * getProductionCost(crop)).toFixed(0)}</li>
                        <li>Estimated Profit: $${(parseFloat(prediction.totalProduction) * getMarketPrice(crop) - area * getProductionCost(crop)).toFixed(0)}</li>
                    </ul>
                </div>

                <div class="warning">
                    <p><i class="fas fa-exclamation-triangle"></i> <strong>Note:</strong> Predictions are based on optimal growing conditions. Actual yields may vary due to weather, pests, and other unforeseen factors.</p>
                </div>
            `;
        }

        function getMarketPrice(crop) {
            const prices = {
                Rice: 420, Wheat: 280, Corn: 180, Soybean: 450, Cotton: 1200, Tomato: 600, Potato: 300,
                Barley: 220, Sugarcane: 50, Coffee: 1200
            };
            return prices[crop] || 300;
        }

        function getProductionCost(crop) {
            const costs = {
                Rice: 800, Wheat: 600, Corn: 700, Soybean: 500, Cotton: 1200, Tomato: 2000, Potato: 1500,
                Barley: 550, Sugarcane: 900, Coffee: 2500
            };
            return costs[crop] || 800;
        }

        // Weather data integration
        function getWeatherData() {
            const location = document.getElementById('location').value;
            if (!location) {
                alert('Please enter a location');
                return;
            }

            document.getElementById('weatherLoading').classList.remove('hidden');
            document.getElementById('weatherResult').classList.add('hidden');

            // Simulate API call with mock data
            setTimeout(() => {
                const mockWeatherData = generateMockWeatherData(location);
                displayWeatherData(mockWeatherData, location);
                
                document.getElementById('weatherLoading').classList.add('hidden');
                document.getElementById('weatherResult').classList.remove('hidden');
            }, 1500);
        }

        function generateMockWeatherData(location) {
            return {
                current: {
                    temperature: Math.round(20 + Math.random() * 15),
                    humidity: Math.round(50 + Math.random() * 30),
                    windSpeed: Math.round(5 + Math.random() * 10),
                    precipitation: Math.round(Math.random() * 5),
                    condition: ['Sunny', 'Partly Cloudy', 'Cloudy', 'Light Rain'][Math.floor(Math.random() * 4)]
                },
                forecast: Array.from({length: 7}, (_, i) => ({
                    day: new Date(Date.now() + i * 24 * 60 * 60 * 1000).toLocaleDateString('en-US', {weekday: 'short'}),
                    temperature: Math.round(18 + Math.random() * 12),
                    condition: ['Sunny', 'Partly Cloudy', 'Cloudy', 'Light Rain', 'Rain'][Math.floor(Math.random() * 5)],
                    rainChance: Math.round(Math.random() * 40)
                })),
                alerts: Math.random() > 0.7 ? ['Frost Warning'] : []
            };
        }

        function displayWeatherData(weatherData, location) {
            const container = document.getElementById('weatherData');
            
            container.innerHTML = `
                <div class="data-grid">
                    <div class="data-item">
                        <h5>Current Temperature</h5>
                        <p>${weatherData.current.temperature}°C</p>
                    </div>
                    <div class="data-item">
                        <h5>Humidity</h5>
                        <p>${weatherData.current.humidity}%</p>
                    </div>
                    <div class="data-item">
                        <h5>Wind Speed</h5>
                        <p>${weatherData.current.windSpeed} km/h</p>
                    </div>
                    <div class="data-item">
                        <h5>Precipitation</h5>
                        <p>${weatherData.current.precipitation} mm</p>
                    </div>
                </div>
                
                <div class="recommendation-item">
                    <h4>7-Day Forecast for ${location}</h4>
                    <div class="data-grid">
                        ${weatherData.forecast.map(day => `
                            <div class="data-item">
                                <h5>${day.day}</h5>
                                <p>${day.temperature}°C</p>
                                <p>${day.condition}</p>
                                <p>Rain: ${day.rainChance}%</p>
                            </div>
                        `).join('')}
                    </div>
                </div>
                
                ${weatherData.alerts.length > 0 ? `
                <div class="danger">
                    <h4><i class="fas fa-exclamation-triangle"></i> Weather Alerts</h4>
                    <ul>
                        ${weatherData.alerts.map(alert => `<li>${alert}</li>`).join('')}
                    </ul>
                </div>
                ` : ''}
                
                <div class="recommendation-item">
                    <h4>Agricultural Advisory</h4>
                    ${generateWeatherAdvisory(weatherData)}
                </div>
            `;
        }

        function generateWeatherAdvisory(weatherData) {
            let advisory = '';
            
            if (weatherData.current.temperature < 5) {
                advisory += '<p><i class="fas fa-temperature-low"></i> <strong>Frost Risk:</strong> Protect sensitive crops with covers or irrigation.</p>';
            }
            
            if (weatherData.current.precipitation > 20) {
                advisory += '<p><i class="fas fa-cloud-rain"></i> <strong>Heavy Rain:</strong> Delay field operations. Check drainage systems.</p>';
            } else if (weatherData.current.precipitation < 5 && weatherData.forecast.some(day => day.rainChance < 30)) {
                advisory += '<p><i class="fas fa-sun"></i> <strong>Dry Conditions:</strong> Consider irrigation for moisture-sensitive crops.</p>';
            }
            
            if (weatherData.current.windSpeed > 15) {
                advisory += '<p><i class="fas fa-wind"></i> <strong>High Winds:</strong> Secure structures and consider wind protection for tall crops.</p>';
            }
            
            if (!advisory) {
                advisory = '<p><i class="fas fa-check-circle"></i> <strong>Favorable Conditions:</strong> Good weather for most farming operations.</p>';
            }
            
            return advisory;
        }

        // Disease Detection Functions
        const uploadArea = document.getElementById('uploadArea');
        const fileInput = document.getElementById('fileInput');
        const imagePreview = document.getElementById('imagePreview');
        const analyzeBtn = document.getElementById('analyzeBtn');
        const diseaseCropType = document.getElementById('disease-crop-type');
        const useCameraBtn = document.getElementById('useCameraBtn');
        const cameraContainer = document.getElementById('cameraContainer');
        const cameraVideo = document.getElementById('cameraVideo');
        const captureBtn = document.getElementById('captureBtn');
        const switchCameraBtn = document.getElementById('switchCameraBtn');

        // Camera-related variables
        let stream = null;
        let facingMode = 'environment'; // Start with back camera

        // Event listeners for disease detection
        uploadArea.addEventListener('click', () => fileInput.click());
        uploadArea.addEventListener('dragover', (e) => {
            e.preventDefault();
            uploadArea.style.background = 'rgba(102, 126, 234, 0.15)';
        });
        uploadArea.addEventListener('dragleave', () => {
            uploadArea.style.background = 'rgba(102, 126, 234, 0.05)';
        });
        uploadArea.addEventListener('drop', (e) => {
            e.preventDefault();
            uploadArea.style.background = 'rgba(102, 126, 234, 0.05)';
            if (e.dataTransfer.files.length) {
                fileInput.files = e.dataTransfer.files;
                handleImageUpload(e.dataTransfer.files[0]);
            }
        });

        fileInput.addEventListener('change', (e) => {
            if (e.target.files.length) {
                handleImageUpload(e.target.files[0]);
            }
        });

        analyzeBtn.addEventListener('click', analyzeImage);
        useCameraBtn.addEventListener('click', initCamera);
        captureBtn.addEventListener('click', captureImage);

        // Function to handle image upload
        function handleImageUpload(file) {
            if (!file.type.match('image.*')) {
                alert('Please upload an image file');
                return;
            }

            if (file.size > 5 * 1024 * 1024) {
                alert('Please upload an image smaller than 5MB');
                return;
            }

            const reader = new FileReader();
            reader.onload = (e) => {
                imagePreview.src = e.target.result;
                imagePreview.style.display = 'block';
                analyzeBtn.disabled = false;
            };
            reader.readAsDataURL(file);
        }

        // Function to initialize camera
        async function initCamera() {
            try {
                stream = await navigator.mediaDevices.getUserMedia({
                    video: { facingMode: facingMode },
                    audio: false
                });
                
                cameraVideo.srcObject = stream;
                cameraContainer.style.display = 'block';
                useCameraBtn.style.display = 'none';
                uploadArea.style.display = 'none';
                
                // Show switch camera button if multiple cameras available
                const devices = await navigator.mediaDevices.enumerateDevices();
                const videoDevices = devices.filter(device => device.kind === 'videoinput');
                if (videoDevices.length > 1) {
                    switchCameraBtn.style.display = 'inline-block';
                    switchCameraBtn.onclick = switchCamera;
                }
            } catch (error) {
                console.error('Error accessing camera:', error);
                alert('Unable to access camera. Please check permissions and try again.');
            }
        }

        // Function to switch between front and back camera
        async function switchCamera() {
            if (stream) {
                stream.getTracks().forEach(track => track.stop());
            }
            
            facingMode = facingMode === 'environment' ? 'user' : 'environment';
            await initCamera();
        }

        // Function to stop camera
        function stopCamera() {
            if (stream) {
                stream.getTracks().forEach(track => track.stop());
                stream = null;
            }
            cameraContainer.style.display = 'none';
            useCameraBtn.style.display = 'inline-block';
            uploadArea.style.display = 'block';
        }

        // Function to capture image from camera
        function captureImage() {
            const canvas = document.createElement('canvas');
            canvas.width = cameraVideo.videoWidth;
            canvas.height = cameraVideo.videoHeight;
            const ctx = canvas.getContext('2d');
            ctx.drawImage(cameraVideo, 0, 0, canvas.width, canvas.height);
            
            // Stop camera stream
            stopCamera();
            
            // Display captured image
            imagePreview.src = canvas.toDataURL('image/png');
            imagePreview.style.display = 'block';
            analyzeBtn.disabled = false;
        }

        // Function to analyze image for diseases
        function analyzeImage() {
            const cropType = diseaseCropType.value;
            
            if (!cropType) {
                alert('Please select a crop type');
                return;
            }
            
            document.getElementById('diseaseLoading').classList.remove('hidden');
            document.getElementById('diseaseResult').classList.add('hidden');
            
            // Simulate AI processing delay
            setTimeout(() => {
                const results = simulateDiseaseDetection(cropType);
                displayDiseaseResults(results, cropType);
                
                document.getElementById('diseaseLoading').classList.add('hidden');
                document.getElementById('diseaseResult').classList.remove('hidden');
            }, 2500);
        }

        // Function to simulate disease detection (would be replaced with actual AI in production)
        function simulateDiseaseDetection(cropType) {
            const diseases = diseaseDatabase[cropType];
            if (!diseases) return null;
            
            // Generate random results for simulation
            const results = [];
            const diseaseKeys = Object.keys(diseases);
            
            // Always include healthy option
            for (let i = 0; i < diseaseKeys.length; i++) {
                const diseaseName = diseaseKeys[i];
                const confidence = Math.random() * 0.8 + 0.1; // Between 0.1 and 0.9
                
                results.push({
                    disease: diseaseName,
                    confidence: confidence,
                    details: diseases[diseaseName]
                });
            }
            
            // Sort by confidence (highest first)
            results.sort((a, b) => b.confidence - a.confidence);
            
            // Normalize confidence scores to sum to 1
            const totalConfidence = results.reduce((sum, result) => sum + result.confidence, 0);
            results.forEach(result => {
                result.confidence = result.confidence / totalConfidence;
            });
            
            return results;
        }

        // Function to display disease results
        function displayDiseaseResults(results, cropType) {
            const container = document.getElementById('diseaseAnalysis');
            
            if (!results || results.length === 0) {
                container.innerHTML = `
                    <div class="warning">
                        <p>No disease information available for ${cropType}. Please try another crop type.</p>
                    </div>
                `;
                return;
            }
            
            let html = `
                <p>Analysis for <strong>${cropType}</strong> based on uploaded image:</p>
            `;
            
            results.forEach(result => {
                const confidencePercent = Math.round(result.confidence * 100);
                const confidenceClass = confidencePercent >= 70 ? 'high-confidence' : 
                                      confidencePercent >= 40 ? 'medium-confidence' : 'low-confidence';
                
                html += `
                    <div class="disease-card">
                        <div class="disease-name">
                            ${result.disease} 
                            <span class="disease-confidence ${confidenceClass}">${confidencePercent}% confidence</span>
                        </div>
                        
                        ${result.disease !== 'Healthy' ? `
                            <p><strong>Symptoms:</strong> ${result.details.symptoms.join(', ')}</p>
                            <p><strong>Causes:</strong> ${result.details.causes}</p>
                            
                            <div class="recommendation-item">
                                <strong>Treatment:</strong>
                                <ul class="treatment-list">
                                    ${result.details.treatment.map(item => `<li>${item}</li>`).join('')}
                                </ul>
                            </div>
                            
                            <div class="recommendation-item">
                                <strong>Prevention:</strong>
                                <ul class="prevention-list">
                                    ${result.details.prevention.map(item => `<li>${item}</li>`).join('')}
                                </ul>
                            </div>
                        ` : `
                            <p>Your ${cropType} plant appears healthy with no signs of disease.</p>
                            <p><strong>Maintenance recommendations:</strong></p>
                            <ul class="prevention-list">
                                ${result.details.prevention.map(item => `<li>${item}</li>`).join('')}
                            </ul>
                        `}
                    </div>
                `;
            });
            
            container.innerHTML = html;
        }

        // Initialize the page
        document.addEventListener('DOMContentLoaded', function() {
            showSection('home');
            updateSensorData();
            
            // Update sensor data every 30 seconds
            setInterval(updateSensorData, 30000);
            
            // Pre-populate region based on geolocation (simulated)
            document.getElementById('region').value = 'Temperate';
        });
    </script>
</body>
</html>
