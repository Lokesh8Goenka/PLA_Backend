🧠 Personalized Learning Assistant (PLA) - Backend

FastAPI backend powering a personalized MCQ-based learning platform for adaptive assessments.

🚀 Project Overview

The Personalized Learning Assistant (PLA) backend serves as the core engine for adaptive, personalized MCQ-based testing.Students select a Subject → Topic → Sub-topic, and the system dynamically adjusts difficulty based on performance using a three-tier flow:

Easy ➔ Remedial ➔ Medium ➔ Remedial ➔ Hard

Weighted scoring and immediate feedback enhance the learning experience.

Designed for K-12 education, the system helps identify student strengths and areas for improvement.

✨ Features

🌟 Subject → Topic → Sub-topic based MCQ tests

📈 Adaptive difficulty progression (Easy → Medium → Hard)

🧪 Remedial questions for partial understanding

�� Weighted scoring system

⚡ Fast, async API built with FastAPI

📚 Organized for easy extension (new subjects, topics, MCQs)

🔒 Clean separation of logic for scalability

🛦️ Tech Stack

Python 3.10+

FastAPI

Uvicorn (for local server running)

Pydantic (for data validation)

CORS Middleware (for frontend-backend communication)

📦 Installation

# Clone the repository
git clone https://github.com/your-username/pla-backend.git
cd pla-backend

# (Optional) Create a virtual environment
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows

# Install dependencies
pip install -r requirements.txt

🚀 Running the Server Locally

# Run using Uvicorn
uvicorn main:app --reload

The API will be live at:

http://127.0.0.1:8000

You can access automatic API docs here:

http://127.0.0.1:8000/docs

🔥 API Endpoints

Method

Endpoint

Description

GET

/get-subjects/

Get all available subjects

GET

/get-topics/{subject}

Get topics for a selected subject

GET

/get-subtopics/{subject}/{topic}

Get subtopics for a selected topic

POST

/start-test/

Start a test for a selected sub-topic (Easy level)

POST

/submit-answers/

Submit answers and get next phase/remedials/results

🧠 Test Flow Summary

Start Test → 3 Easy-level main MCQs

Evaluate:

✅ All correct ➔ Next level (Medium)

❌ All wrong ➔ Test ends: "You need more practice"

⚠️ Some wrong ➔ 2 Easy-level remedial MCQs

Pass Criteria: 3/5 correct to move up

Medium Level → Same flow

Hard Level → Same flow

Final Score shown based on weighted scoring

🎯 Scoring System

Main Question (Easy/Medium/Hard): +2 points

Remedial Question: +1 point

Final Score =



🧑‍💻 Author

Lokesh GoenkaM.Sc. in Data Science & Computing🔬 Focused on AI for Education, Adaptive Testing, and Personalized Learning.🌐 Hugging Face Profile

🛡️ License

This project is licensed under the MIT License.Feel free to use, modify, and share! ✨

🚀 Future Improvements

Add user authentication

Expand MCQ database

Admin panel for adding new content

Dockerize deployment

Integration with Hugging Face hosted MCQ Generator Model

🎉 Happy Learning!
