
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Free online image compression tool. Reduce image file size without losing quality. Supports JPG, PNG, and WebP formats.">
    <title>ImageCompress | Smart Image Optimization Tool</title>
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Google AdSense -->
    <!-- Publisher ID: pub-5616980337934821 | Customer ID: 384-337-6853 -->
    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-5616980337934821" crossorigin="anonymous"></script>
    
    <style>
        :root {
            --primary: #4361ee;
            --primary-light: #4895ef;
            --secondary: #3f37c9;
            --accent: #f72585;
            --dark: #212529;
            --light: #f8f9fa;
            --gray: #6c757d;
            --success: #4cc9f0;
            --border-radius: 12px;
            --shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #e2e8f0 100%);
            color: var(--dark);
            line-height: 1.6;
            min-height: 100vh;
            padding: 2rem 1rem;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        /* Header */
        header {
            text-align: center;
            margin-bottom: 3rem;
            animation: fadeIn 0.8s ease;
        }
        
        .logo {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.8rem;
            margin-bottom: 1rem;
        }
        
        .logo-icon {
            font-size: 2.5rem;
            color: var(--primary);
        }
        
        h1 {
            font-size: 2.5rem;
            font-weight: 700;
            background: linear-gradient(to right, var(--primary), var(--accent));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 0.5rem;
        }
        
        .subtitle {
            color: var(--gray);
            font-size: 1.1rem;
            max-width: 600px;
            margin: 0 auto;
        }
        
        .info-link {
            margin-top: 1rem;
            display: inline-block;
            color: var(--primary);
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
        }
        
        .info-link:hover {
            color: var(--secondary);
            text-decoration: underline;
        }
        
        /* Ad Container */
        .ad-container {
            background: white;
            border-radius: var(--border-radius);
            padding: 1rem;
            margin: 2rem 0;
            text-align: center;
            box-shadow: var(--shadow);
        }
        
        .ad-label {
            color: var(--gray);
            font-size: 0.75rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 0.5rem;
        }
        
        /* Main Tool */
        .tool-card {
            background: white;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            overflow: hidden;
            margin-bottom: 2rem;
            transition: var(--transition);
            animation: slideUp 0.8s ease;
        }
        
        .tool-header {
            background: linear-gradient(to right, var(--primary), var(--secondary));
            color: white;
            padding: 1.5rem;
            text-align: center;
        }
        
        .tool-header h2 {
            font-weight: 600;
            font-size: 1.5rem;
        }
        
        .tool-body {
            padding: 2rem;
        }
        
        /* Upload Area */
        .upload-area {
            border: 2px dashed #d1d5db;
            border-radius: var(--border-radius);
            padding: 3rem 2rem;
            text-align: center;
            cursor: pointer;
            transition: var(--transition);
            margin-bottom: 1.5rem;
            position: relative;
            overflow: hidden;
        }
        
        .upload-area:hover {
            border-color: var(--primary);
            background: rgba(67, 97, 238, 0.03);
        }
        
        .upload-area.active {
            border-color: var(--success);
            background: rgba(76, 201, 240, 0.05);
        }
        
        .upload-icon {
            font-size: 3.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
            transition: var(--transition);
        }
        
        .upload-area:hover .upload-icon {
            transform: translateY(-5px);
        }
        
        .upload-text h3 {
            font-size: 1.25rem;
            margin-bottom: 0.5rem;
            color: var(--dark);
        }
        
        .upload-text p {
            color: var(--gray);
            font-size: 0.9rem;
        }
        
        .file-input {
            display: none;
        }
        
        /* Options */
        .options-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin: 2rem 0;
        }
        
        .option-group {
            margin-bottom: 1rem;
        }
        
        .option-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
            color: var(--dark);
        }
        
        .select-wrapper, .range-wrapper {
            position: relative;
        }
        
        select, input[type="range"] {
            width: 100%;
            padding: 0.8rem 1rem;
            border: 1px solid #e2e8f0;
            border-radius: var(--border-radius);
            font-family: 'Poppins', sans-serif;
            font-size: 1rem;
            transition: var(--transition);
            appearance: none;
            background: white;
        }
        
        select:focus, input[type="range"]:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(67, 97, 238, 0.2);
        }
        
        .select-wrapper::after {
            content: '\f078';
            font-family: 'Font Awesome 6 Free';
            font-weight: 900;
            position: absolute;
            right: 1rem;
            top: 50%;
            transform: translateY(-50%);
            color: var(--gray);
            pointer-events: none;
        }
        
        input[type="range"] {
            padding: 0;
            height: 8px;
            -webkit-appearance: none;
            background: #e2e8f0;
            border: none;
        }
        
        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            background: var(--primary);
            border-radius: 50%;
            cursor: pointer;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
        }
        
        .range-labels {
            display: flex;
            justify-content: space-between;
            margin-top: 0.5rem;
            font-size: 0.8rem;
            color: var(--gray);
        }
        
        /* Buttons */
        .btn {
            display: inline-block;
            padding: 0.8rem 1.5rem;
            border-radius: var(--border-radius);
            font-weight: 600;
            text-align: center;
            cursor: pointer;
            transition: var(--transition);
            border: none;
            font-size: 1rem;
            width: 100%;
        }
        
        .btn-primary {
            background: linear-gradient(to right, var(--primary), var(--primary-light));
            color: white;
            box-shadow: 0 4px 6px rgba(67, 97, 238, 0.2);
        }
        
        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(67, 97, 238, 0.25);
        }
        
        .btn-primary:disabled {
            background: #e2e8f0;
            color: #94a3b8;
            cursor: not-allowed;
            transform: none;
            box-shadow: none;
        }
        
        .btn-accent {
            background: var(--accent);
            color: white;
            margin-top: 1.5rem;
        }
        
        .btn-accent:hover {
            background: #e5177b;
            transform: translateY(-2px);
        }
        
        /* Preview Section */
        .preview-section {
            display: none;
            margin-top: 2rem;
            animation: fadeIn 0.5s ease;
        }
        
        .preview-title {
            text-align: center;
            margin-bottom: 1.5rem;
            font-size: 1.5rem;
            color: var(--dark);
        }
        
        .comparison-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }
        
        .image-card {
            background: white;
            border-radius: var(--border-radius);
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }
        
        .image-card:hover {
            transform: translateY(-5px);
        }
        
        .image-header {
            padding: 1rem;
            text-align: center;
            border-bottom: 1px solid #f1f5f9;
            font-weight: 600;
        }
        
        .image-container {
            padding: 1.5rem;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 200px;
            background: #f8fafc;
        }
        
        .image-container img {
            max-width: 100%;
            max-height: 300px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        .image-footer {
            padding: 1rem;
            text-align: center;
            font-size: 0.9rem;
            color: var(--gray);
            border-top: 1px solid #f1f5f9;
        }
        
        .savings-banner {
            background: linear-gradient(to right, var(--success), #38bdf8);
            color: white;
            padding: 1.5rem;
            border-radius: var(--border-radius);
            text-align: center;
            margin: 2rem 0;
            display: none;
            animation: fadeIn 0.5s ease;
        }
        
        .savings-banner h3 {
            font-size: 1.25rem;
            margin-bottom: 0.5rem;
        }
        
        /* Footer */
        footer {
            text-align: center;
            margin-top: 3rem;
            color: var(--gray);
            font-size: 0.9rem;
        }
        
        .footer-links {
            margin-top: 1rem;
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            flex-wrap: wrap;
        }
        
        .footer-links a {
            color: var(--gray);
            text-decoration: none;
            transition: var(--transition);
        }
        
        .footer-links a:hover {
            color: var(--primary);
            text-decoration: underline;
        }
        
        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        @keyframes slideUp {
            from { 
                opacity: 0;
                transform: translateY(20px);
            }
            to { 
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            h1 {
                font-size: 2rem;
            }
            
            .tool-body {
                padding: 1.5rem;
            }
            
            .upload-area {
                padding: 2rem 1rem;
            }
            
            .comparison-grid {
                grid-template-columns: 1fr;
            }
            
            .footer-links {
                flex-direction: column;
                gap: 0.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <header>
            <div class="logo">
                <i class="fas fa-compress-alt logo-icon"></i>
                <h1>ImageCompress</h1>
            </div>
            <p class="subtitle">Optimize your images for web and mobile with our powerful compression tool</p>
            <a href="https://example.com/learn-more" class="info-link" target="_blank">
                <i class="fas fa-info-circle"></i> Learn more about image compression
            </a>
        </header>
        
        <!-- Top Ad -->
        <div class="ad-container">
            <div class="ad-label">Advertisement</div>
            <ins class="adsbygoogle"
                 style="display:block"
                 data-ad-client="ca-pub-5616980337934821"
                 data-ad-slot="YOUR_AD_SLOT_ID"
                 data-ad-format="auto"
                 data-full-width-responsive="true"></ins>
            <script>
                 (adsbygoogle = window.adsbygoogle || []).push({});
            </script>
        </div>
        
        <!-- Main Tool -->
        <div class="tool-card">
            <div class="tool-header">
                <h2>Compress Your Images</h2>
            </div>
            <div class="tool-body">
                <div class="upload-area" id="uploadArea">
                    <div class="upload-icon">
                        <i class="fas fa-cloud-upload-alt"></i>
                    </div>
                    <div class="upload-text">
                        <h3>Drag & Drop Your Image</h3>
                        <p>or click to browse files (JPG, PNG, WebP)</p>
                    </div>
                    <input type="file" id="fileInput" class="file-input" accept="image/*">
                </div>
                
                <div class="options-grid">
                    <div class="option-group">
                        <label for="compressionLevel">Compression Level</label>
                        <div class="select-wrapper">
                            <select id="compressionLevel">
                                <option value="0.6">High Compression</option>
                                <option value="0.8" selected>Medium (Recommended)</option>
                                <option value="0.9">Low Compression</option>
                            </select>
                        </div>
                    </div>
                    
                    <div class="option-group">
                        <label for="outputFormat">Output Format</label>
                        <div class="select-wrapper">
                            <select id="outputFormat">
                                <option value="original">Original Format</option>
                                <option value="jpeg">JPEG</option>
                                <option value="png">PNG</option>
                                <option value="webp">WebP (Recommended)</option>
                            </select>
                        </div>
                    </div>
                </div>
                
                <div class="option-group">
                    <label for="qualityRange">Quality: <span id="qualityValue">80</span>%</label>
                    <input type="range" id="qualityRange" min="10" max="100" value="80" step="5">
                    <div class="range-labels">
                        <span>Smaller</span>
                        <span>Balanced</span>
                        <span>Better</span>
                    </div>
                </div>
                
                <button class="btn btn-primary" id="compressBtn" disabled>
                    <i class="fas fa-compress-alt"></i> Compress Image
                </button>
                
                <!-- Preview Section -->
                <div class="preview-section" id="previewSection">
                    <h3 class="preview-title">Compression Results</h3>
                    
                    <div class="comparison-grid">
                        <div class="image-card">
                            <div class="image-header">Original Image</div>
                            <div class="image-container">
                                <img id="originalImg" src="#" alt="Original Image">
                            </div>
                            <div class="image-footer" id="originalInfo"></div>
                        </div>
                        
                        <div class="image-card">
                            <div class="image-header">Compressed Image</div>
                            <div class="image-container">
                                <img id="compressedImg" src="#" alt="Compressed Image">
                            </div>
                            <div class="image-footer" id="compressedInfo"></div>
                        </div>
                    </div>
                    
                    <div class="savings-banner" id="savingsBanner">
                        <h3>You saved <span id="savingsAmount">0 KB</span>!</h3>
                        <p>That's <span id="savingsPercent">0%</span> smaller than the original</p>
                    </div>
                    
                    <button class="btn btn-accent" id="downloadBtn">
                        <i class="fas fa-download"></i> Download Compressed Image
                    </button>
                </div>
            </div>
        </div>
        
        <!-- Middle Ad -->
        <div class="ad-container">
            <div class="ad-label">Advertisement</div>
            <ins class="adsbygoogle"
                 style="display:block"
                 data-ad-client="ca-pub-5616980337934821"
                 data-ad-slot="YOUR_AD_SLOT_ID"
                 data-ad-format="auto"
                 data-full-width-responsive="true"></ins>
            <script>
                 (adsbygoogle = window.adsbygoogle || []).push({});
            </script>
        </div>
        
        <!-- Footer -->
        <footer>
            <p>&copy; <span id="currentYear"></span> ImageCompress | All Rights Reserved</p>
            <div class="footer-links">
                <a href="https://yourwebsite.com" target="_blank">Our Website</a>
                <a href="privacy-policy.html" target="_blank">Privacy Policy</a>
                <a href="terms-of-service.html" target="_blank">Terms of Service</a>
                <a href="mailto:contact@yourwebsite.com">Contact Us</a>
            </div>
        </footer>
    </div>
    
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Set current year
            document.getElementById('currentYear').textContent = new Date().getFullYear();
            
            // Elements
            const uploadArea = document.getElementById('uploadArea');
            const fileInput = document.getElementById('fileInput');
            const compressBtn = document.getElementById('compressBtn');
            const previewSection = document.getElementById('previewSection');
            const originalImg = document.getElementById('originalImg');
            const compressedImg = document.getElementById('compressedImg');
            const originalInfo = document.getElementById('originalInfo');
            const compressedInfo = document.getElementById('compressedInfo');
            const downloadBtn = document.getElementById('downloadBtn');
            const savingsBanner = document.getElementById('savingsBanner');
            const savingsAmount = document.getElementById('savingsAmount');
            const savingsPercent = document.getElementById('savingsPercent');
            const qualityRange = document.getElementById('qualityRange');
            const qualityValue = document.getElementById('qualityValue');
            
            let originalFile = null;
            let compressedBlob = null;
            
            // Update quality value display
            qualityRange.addEventListener('input', function() {
                qualityValue.textContent = this.value;
            });
            
            // Handle drag & drop
            uploadArea.addEventListener('click', () => fileInput.click());
            
            ['dragover', 'dragenter'].forEach(event => {
                uploadArea.addEventListener(event, (e) => {
                    e.preventDefault();
                    uploadArea.classList.add('active');
                });
            });
            
            ['dragleave', 'dragend'].forEach(event => {
                uploadArea.addEventListener(event, () => {
                    uploadArea.classList.remove('active');
                });
            });
            
            uploadArea.addEventListener('drop', (e) => {
                e.preventDefault();
                uploadArea.classList.remove('active');
                
                if (e.dataTransfer.files.length) {
                    fileInput.files = e.dataTransfer.files;
                    handleFileSelect(e.dataTransfer.files[0]);
                }
            });
            
            // Handle file selection
            fileInput.addEventListener('change', () => {
                if (fileInput.files.length) {
                    handleFileSelect(fileInput.files[0]);
                }
            });
            
            function handleFileSelect(file) {
                if (!file.type.match('image.*')) {
                    alert('Please select an image file (JPG, PNG, WebP)');
                    return;
                }
                
                originalFile = file;
                compressBtn.disabled = false;
                
                // Display original image
                const reader = new FileReader();
                reader.onload = (e) => {
                    originalImg.src = e.target.result;
                    originalInfo.textContent = `${file.name} • ${formatFileSize(file.size)}`;
                };
                reader.readAsDataURL(file);
            }
            
            // Compress image
            compressBtn.addEventListener('click', compressImage);
            
            function compressImage() {
                if (!originalFile) return;
                
                const quality = qualityRange.value / 100;
                const outputFormat = document.getElementById('outputFormat').value;
                
                const reader = new FileReader();
                reader.onload = (e) => {
                    const img = new Image();
                    img.onload = () => {
                        const canvas = document.createElement('canvas');
                        const ctx = canvas.getContext('2d');
                        
                        // Calculate new dimensions (maintain aspect ratio)
                        let width = img.width;
                        let height = img.height;
                        
                        canvas.width = width;
                        canvas.height = height;
                        ctx.drawImage(img, 0, 0, width, height);
                        
                        // Determine output format
                        let mimeType = 'image/jpeg';
                        if (outputFormat === 'png') mimeType = 'image/png';
                        if (outputFormat === 'webp') mimeType = 'image/webp';
                        if (outputFormat === 'original') mimeType = originalFile.type;
                        
                        // Compress
                        canvas.toBlob((blob) => {
                            compressedBlob = blob;
                            const compressedUrl = URL.createObjectURL(blob);
                            
                            compressedImg.src = compressedUrl;
                            const format = outputFormat === 'original' ? originalFile.name.split('.').pop() : outputFormat;
                            compressedInfo.textContent = `compressed.${format} • ${formatFileSize(blob.size)}`;
                            
                            // Calculate savings
                            const savings = originalFile.size - blob.size;
                            const percent = Math.round((savings / originalFile.size) * 100);
                            
                            if (savings > 0) {
                                savingsAmount.textContent = formatFileSize(savings);
                                savingsPercent.textContent = `${percent}%`;
                                savingsBanner.style.display = 'block';
                            } else {
                                savingsBanner.style.display = 'none';
                            }
                            
                            // Show preview
                            previewSection.style.display = 'block';
                            previewSection.scrollIntoView({ behavior: 'smooth' });
                            
                        }, mimeType, quality);
                    };
                    img.src = e.target.result;
                };
                reader.readAsDataURL(originalFile);
            }
            
            // Download compressed image
            downloadBtn.addEventListener('click', () => {
                if (!compressedBlob) return;
                
                const a = document.createElement('a');
                const url = URL.createObjectURL(compressedBlob);
                const outputFormat = document.getElementById('outputFormat').value;
                let extension = outputFormat;
                
                if (outputFormat === 'original') {
                    extension = originalFile.name.split('.').pop();
                }
                
                a.href = url;
                a.download = `compressed.${extension}`;
                document.body.appendChild(a);
                a.click();
                document.body.removeChild(a);
                URL.revokeObjectURL(url);
            });
            
            // Helper function to format file size
            function formatFileSize(bytes) {
                if (bytes === 0) return '0 Bytes';
                const k = 1024;
                const sizes = ['Bytes', 'KB', 'MB', 'GB'];
                const i = Math.floor(Math.log(bytes) / Math.log(k));
                return parseFloat((bytes / Math.pow(k, i)).toFixed(2)) + ' ' + sizes[i];
            }
        });
    </script>
</body>
</html>
