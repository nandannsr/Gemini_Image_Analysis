
<html lang="en">
<body>
  <h1>Vehicle Image Analysis App</h1>
  <p>
    This repository contains a <strong>Streamlit</strong>-based application that analyzes vehicle images using
    <strong>Google GENAI</strong>'s Gemini model. The app accepts exactly 4 images of a vehicle (front, rear, left, and right),
    performs quality checks, looks for structural damage, and attempts to identify the vehicle's number plate.
  </p>

  <h2>Table of Contents</h2>
  <ul>
    <li><a href="#file-structure">File Structure</a></li>
    <li><a href="#features">Features</a></li>
    <li><a href="#prerequisites">Prerequisites</a></li>
    <li><a href="#installation">Installation</a></li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#environment-variables">Environment Variables</a></li>
  </ul>

  <h2 id="file-structure">File Structure</h2>
  <pre>
.
├── .gitignore
├── ai_engine.py
├── README.md
├── requirements.txt
└── ui.py
  </pre>
  <p>
    <strong>Description of Key Files:</strong>
  </p>
  <ul>
    <li><strong>ui.py</strong>: The main Streamlit application that handles file uploads and user interaction.</li>
    <li><strong>ai_engine.py</strong>: Contains the logic for sending images to Google GENAI's Gemini model for analysis.</li>
    <li><strong>requirements.txt</strong>: Lists Python dependencies needed to run the application.</li>
    <li><strong>.gitignore</strong>: Specifies files and directories ignored by Git.</li>
    <li><strong>README.md</strong>: Project documentation (this file, in HTML form).</li>
  </ul>

  <h2 id="features">Features</h2>
  <ul>
    <li>Uploads exactly 4 vehicle images (front, rear, left, right).</li>
    <li>Performs quality checks on uploaded images (clarity, lighting, resolution).</li>
    <li>Inspects the vehicle for structural damages (scratches, dents, broken parts).</li>
    <li>Attempts to detect and return the vehicle's number plate.</li>
    <li>Displays analysis results in a clean, table-like format.</li>
  </ul>

  <h2 id="prerequisites">Prerequisites</h2>
  <ul>
    <li>Python 3.7 or higher</li>
    <li>pip or another Python package manager</li>
    <li>A valid Google GENAI API key (set as an environment variable)</li>
  </ul>

  <h2 id="installation">Installation</h2>
  <ol>
    <li>
      <p>Clone this repository:</p>
      <pre><code>git clone https://github.com/your-username/vehicle-image-analysis.git
cd vehicle-image-analysis
      </code></pre>
    </li>
    <li>
      <p>Install the required dependencies:</p>
      <pre><code>pip install -r requirements.txt</code></pre>
    </li>
    <li>
      <p>Set your Google GENAI API key (see <a href="#environment-variables">Environment Variables</a> below).</p>
    </li>
  </ol>

  <h2 id="usage">Usage</h2>
  <ol>
    <li>
      <p>Run the Streamlit application:</p>
      <pre><code>streamlit run ui.py</code></pre>
    </li>
    <li>
      <p>
        Once the app launches in your browser, click <strong>Browse files</strong> and upload exactly 4 images of the same
        vehicle (front, rear, left, right).
      </p>
    </li>
    <li>
      <p>
        Click the <strong>Analyze Vehicle</strong> button to send the images to the Gemini model for analysis.
      </p>
    </li>
    <li>
      <p>
        View the analysis results displayed in a table format, including image quality feedback, detected structural damage,
        and the identified number plate (if any).
      </p>
    </li>
    <li>
      <p>
        Use the <strong>🔄 Start New Analysis</strong> button to reset the app and upload a new set of images.
      </p>
    </li>
  </ol>

  <h2 id="environment-variables">Environment Variables</h2>
  <p>
    The application uses an environment variable <code>API_KEY</code> for the Google GENAI Gemini model.
    Create a <code>.env</code> file in the project root (or export the variable directly in your shell) containing:
  </p>
  <pre><code>API_KEY=your_google_genai_api_key_here
  </code></pre>
  <p>
    If you're creating a <code>.env</code> file, make sure you have <code>python-dotenv</code> installed (it is
    already in <code>requirements.txt</code>) and that your file is in the same directory as <code>ai_engine.py</code>.
  </p>

  <p>
    <em>For any issues, suggestions, or improvements, please open an issue or submit a pull request.</em>
  </p>
</body>
</html>
