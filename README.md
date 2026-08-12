# 📄 AI Resume Screener

An intelligent and user-friendly **AI Resume Screener** built with **Python and Streamlit**. The application analyzes a candidate's resume against a provided Job Description and generates a match score, verdict, matched skills, missing skills, suggestions, and a final recommendation.

---

## 🚀 Features

* 📄 Upload resumes in:

  * PDF
  * TXT
  * DOCX
* 💼 Paste a complete Job Description
* 🔍 Automatically analyze the resume
* 📊 Generate a **Resume Match Score**
* ✅ Identify **Matched Skills**
* ❌ Identify **Missing Skills**
* 📝 Generate an analysis summary
* 💡 Provide resume improvement suggestions
* ⭐ Generate a final recommendation
* 📥 Download the screening report as a `.txt` file
* 🎨 Modern dark-themed Streamlit interface
* 📱 Simple and easy-to-use UI

---

## 🖥️ Application Preview

The application provides a two-column interface:

**Left Side**

* Resume upload
* Supported file formats

**Right Side**

* Job Description input

After clicking **Analyze Resume**, the application displays:

* Match Score
* Verdict
* Analysis
* Matched Skills
* Missing Skills
* Suggestions
* Final Recommendation
* Downloadable Report

---

## 🧠 How It Works

The application follows a simple resume-screening workflow:

```text
        Resume Upload
              │
              ▼
       Extract Resume Text
              │
              ▼
       Job Description
              │
              ▼
        Skill Extraction
              │
              ▼
       Compare Skills
              │
              ▼
        Calculate Score
              │
              ▼
       Generate Verdict
              │
              ▼
      Display Analysis
              │
              ▼
       Download Report
```

The application maintains a predefined list of technical skills and checks which skills are present in both the resume and the Job Description.

---

## 📊 Verdict System

| Match Score | Verdict     |
| ----------- | ----------- |
| 70% - 100%  | 🟢 Strong   |
| 40% - 69%   | 🟡 Moderate |
| 0% - 39%    | 🔴 Weak     |

### Strong

The resume contains most of the skills required by the Job Description.

### Moderate

The resume contains several relevant skills but is missing some important requirements.

### Weak

The resume has limited overlap with the required skills.

---

## 🛠️ Technologies Used

* **Python**
* **Streamlit**
* **PyPDF2** – PDF text extraction
* **python-docx** – DOCX text extraction
* **Regular Expressions**
* **HTML/CSS** – UI customization

---

## 📁 Project Structure

```text
Resume_Screener_Project/
│
├── app.py
├── agent.py
├── task.py
├── job description.txt
├── resume.txt
├── .gitignore
└── README.md
```

### `app.py`

Main Streamlit application.

It handles:

* User interface
* Resume upload
* PDF/TXT/DOCX reading
* Job Description input
* Resume analysis
* Result visualization
* Report generation and download

### `agent.py`

Contains the `ResumeScreenerAgent` class.

It handles:

* Skill extraction
* Resume skill analysis
* Job Description skill extraction
* Matched skill detection
* Missing skill detection
* Match score calculation
* Strong / Moderate / Weak verdict generation

### `task.py`

Provides a command-line style resume screening workflow for reading resume and Job Description files and displaying the analysis.

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git
```

Move into the project folder:

```bash
cd Resume_Screener_Project
```

---

### 2. Create a Virtual Environment

Windows:

```bash
python -m venv venv
```

Activate it:

```bash
venv\Scripts\activate
```

---

### 3. Install Dependencies

```bash
pip install streamlit PyPDF2 python-docx
```

---

## ▶️ Run the Application

Start the Streamlit application using:

```bash
streamlit run app.py
```

The application will open in your browser, normally at:

```text
http://localhost:8501
```

---

## 📄 How to Use

### Step 1 — Upload Resume

Upload your resume using the file uploader.

Supported formats:

```text
PDF
TXT
DOCX
```

### Step 2 — Add Job Description

Paste the complete Job Description into the Job Description text area.

### Step 3 — Analyze

Click:

```text
🔍 Analyze Resume
```

### Step 4 — View Results

The application displays:

```text
Match Score
Verdict
Analysis
Matched Skills
Missing Skills
Suggestions
Final Recommendation
```

### Step 5 — Download Report

Click:

```text
📥 Download Report
```

to save the screening results as a text file.

---

## 🔎 Example

### Job Description

```text
We are looking for a Python Developer with experience in
Python, SQL, Flask, Git, Docker and Machine Learning.
```

### Resume

```text
Skills:
Python
SQL
Flask
Git
Machine Learning
```

### Example Result

```text
Match Score: 83%

Verdict: Strong

Matched Skills:
✓ Python
✓ SQL
✓ Flask
✓ Git
✓ Machine Learning

Missing Skills:
✗ Docker
```

---

## 💡 Suggestions Provided

If important skills are missing, the application recommends improving the resume by:

* Adding relevant technical skills
* Highlighting relevant projects
* Including practical experience
* Adding certifications or coursework
* Adding relevant GitHub projects

---

## 📥 Report Generation

The application can generate a downloadable report containing:

```text
AI RESUME SCREENER REPORT

Resume File

Match Score

Verdict

Analysis

Matched Skills

Missing Skills

Suggestions

Final Recommendation
```

---

## 🔐 Security

Do **not** upload or commit sensitive information such as:

* API keys
* Passwords
* Personal credentials
* Private resumes
* `.env` files containing secrets

If you use environment variables, add `.env` to `.gitignore`.

Example:

```text
.env
venv/
.venv/
__pycache__/
*.pyc
```

**Never upload your API keys to GitHub.**

---

## 🎯 Future Improvements

Possible future enhancements include:

* 🤖 LLM-powered resume analysis
* 📈 Advanced semantic matching
* 🎯 Job-specific resume recommendations
* 📊 Skill match visualization
* 🧑‍💼 Candidate ranking
* 📑 PDF report generation
* 🔗 LinkedIn profile analysis
* 🌐 Job-search integration
* 📚 Interview preparation recommendations
* 💬 AI-powered resume improvement assistant

---

## 🌟 Project Goal

The goal of this project is to make resume screening **faster, easier, and more accessible** by automatically comparing a candidate's skills with the requirements of a Job Description.

It can be useful for:

* Job seekers
* Students
* Recruiters
* HR teams
* Career guidance
* Resume optimization

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a new branch

```bash
git checkout -b feature/new-feature
```

3. Make your changes
4. Commit your changes

```bash
git commit -m "Add new feature"
```

5. Push the branch

```bash
git push origin feature/new-feature
```

6. Open a Pull Request

---

## 📜 License

This project is open-source and available for educational and personal use.

---

## 👨‍💻 Author

**Arun Naik**

Built with ❤️ using **Python and Streamlit**.

---

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub!
