# 🧪 MarTech engineering hiring - Take-home exercises 

Welcome 👋  
This repository contains take-home exercises for candidates applying to engineering roles at **Electrolux Group** in **Bangalore, India**. These challenges reflect real-world scenarios from our global strategy around consumer data, personalization, and omnichannel activation.

Please read the instructions carefully and follow the submission guidelines at the end.

---

## 🔧 Available Exercises

Choose the exercise that corresponds to the role you're applying for:

### 1. Tech Lead – Consumer Engagement  
#### Exercise: Design and present a solution architecture diagram for sending a personalized SMS reminder after cart abandonment.

#### Understand the Use Case  
Briefly describe the user journey and the business goal behind the SMS reminder.  
- What should trigger the message?  
- What personalizations are relevant?

#### Identify Relevant Platforms  
Based on the job posting, identify which Electrolux platforms could be used in this scenario.
Explain the role of each platform in your proposed solution.

#### Design the Architecture  
Create a **solution architecture diagram** using your preferred tool (e.g., draw.io, Lucidchart, Miro).  
Your diagram should include:
- Data sources and events (e.g., cart abandonment detection)  
- Consent handling  
- Data activation logic  
- Messaging channel (SMS) and orchestration  
- Optional: error handling or fallback mechanisms

#### Explain Your Design  
Provide a short written explanation of:
- The end-to-end flow  
- Your design decisions and technology choices  
- Any assumptions made  
- How the solution would scale across regions or campaigns


### 2. Senior Engineer – Identity & Consent  
t.b.d 

### 3. Senior Engineer – Marketing Integrations & APIs  
#### Exercise: Develop an API that syncs user profile data to a mock third-party marketing platform with basic validation and transformation logic.

#### 1. Build the Profile Sync API  
Develop a simple REST API that accepts a **batch of user profiles** (e.g., JSON array) via a POST request. Each profile should contain fields such as:
- Email address  
- First name and last name  
- Optional metadata (e.g., tags, preferences)

#### 2. Implement Basic Logic  
Your API should include the following features:
- ✅ **Email validation**: Filter out invalid email addresses (e.g., missing `@` or domain)  
- ✅ **Name normalization**: Ensure first and last names are capitalized correctly (e.g., `john doe` → `John Doe`)  
- ✅ **Logging as mock integration**: Simulate a third-party API call by logging the outgoing transformed data (no real API call required)

#### 3. Document Your Work  
Provide documentation that is understandable by both:
- **Technical stakeholders**: Describe API design, structure, data flow, and any edge-case handling  
- **Non-technical stakeholders**: Explain the purpose of the API, the types of data it processes, and how it fits into a marketing use case

You can include this documentation as:
- A `README.md` section
- A separate `docs/` folder (if preferred)
- Diagrams or flowcharts (optional but welcome)


### 4. Engineer – Marketing Data & AI  
#### Exercise: Predict Optimal Send Time for a Marketing Campaign using a Python notebook

#### 1. Analyze the Dataset  
Use the provided dataset containing **email open and click events** per user. The data includes:
- Timestamps of sends, opens, and clicks  
- User IDs 

Explore behavioral patterns by:
- Day of the week  
- Hour of day  
- Frequency of interaction

#### 2. Write a Prediction Script  
Develop a **Python script or notebook** that predicts the best time of day to send marketing emails to each consumer or segment.  
You may use:
- Statistical rules (e.g., most frequent open hour)
- Basic machine learning (optional)
- Aggregations or heuristics

The script should output a list of users (or segments) with their recommended send times.

#### 3. Suggest Ecosystem Integration  
Explain how your output could be integrated into the Electrolux marketing and activation ecosystem.  
- Identify **relevant platforms** from the job posting
- Suggest how the predictions could be exported, activated, or used in real-time orchestration  
- Consider data flows or API usage if relevant

#### 4. Document Your Work  
Provide documentation suitable for:
- **Technical stakeholders**: Describe your data preparation, logic, modeling, and script structure  
- **Non-technical stakeholders**: Summarize what your solution does, how it adds value, and what assumptions were made

Include your documentation:
- In a `README.md` section or notebook cell  
- Or in a separate `docs/` folder

Optional: Add graphs or visuals to illustrate patterns or predictions.

---

## 📦 How to Submit

- Fork this repository or create a private repo and share access with us.
- Create a folder named after your role (e.g., `tech-lead-consumer-engagement`).
- Place all your code, scripts, diagrams, or notebooks inside the folder.
- Include a short `README.md` in your folder with:
  - An overview of your approach
  - Any assumptions made
  - Setup or run instructions
  - Optional: areas you would improve with more time

---

## 🧠 Use of Generative AI Tools (e.g., ChatGPT, GitHub Copilot)

You’re welcome to use Generative AI tools as long as you clearly indicate where and how they were used.

Please include:
- Which tools were used
- For which parts of the solution (e.g., code snippets, text drafting)
- What was directly generated vs. adapted or extended by you

Transparency helps us understand **your thinking**, not just the output.

---

## ⏱️ Time Expectation

Each exercise is designed to take **2-4 hours**. We value quality over completeness — focus on clarity, structure, and reasoning.

---

## 🙌 Good Luck!

We're excited to learn more about how you think and build.  
If you have any questions, feel free to reach out to your recruiting contact.

---
