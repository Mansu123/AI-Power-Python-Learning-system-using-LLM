# AI-Power-Python-Learning-system-using-Langchain
## This is the main app link: https://huggingface.co/spaces/Mansuba/AIpythonLearning2
This app was built in Hugging Face Space using the Gradio framework.
### To run this app, you need a Groq API key, which you can get from here:https://console.groq.com/keys



This system creates an adaptive learning experience for Python programming across a three-day curriculum. It utilizes the Groq LLM API (with LangChain integration) to dynamically generate content, assessments, and personalized feedback based on student performance.

## Core Components
LLMService: Handles all AI interactions using the Groq LLM API, with fallbacks to direct API calls if necessary.
ContentGenerator: Manages the creation and storage of learning modules, exam questions, and student responses.
LearningSystem: Orchestrates the entire learning experience, including day progression, exam timing, and progress tracking.

## Key Features

Adaptive Content: Questions adapt based on previous mistakes
Timed Exams: Enforces 1-hour time limits for realistic assessment
Detailed Feedback: Comprehensive explanations for correct/incorrect answers
Learning Progress: Tracks overall statistics and day-by-day improvement
Interactive Q&A: Allows students to get help on specific topics
Persistent Storage: All data is accessible for ongoing review

## Main Interface Sections & Buttons

# Day Navigation Section

Advance to Next Day Button: Calls advance_to_next_day() to progress from Day 1 to Day 2, and from Day 2 to Day 3
Current Day Display: Shows which day's content (1-3) the student is currently viewing
Progress Indicator: Visualizes how far along the student is in the curriculum



# 1. Content Generation Section

Generate Content Button: Calls generate_day_content() to create and display the day's learning materials
Content Display Area: Shows the Markdown-formatted learning module with:

Module title
Introduction
Multiple teaching sections
Code examples
Practice exercises
![image](https://github.com/user-attachments/assets/02b9a134-71dc-4acc-b47c-d0eb5e844fd2)




# 2. Exam Section

Start Exam Button: Calls start_exam() to begin the one-hour timed assessment
Timer Display: Shows time remaining in the exam (counting down from 1 hour)
Question Display: Shows the exam questions with:

Question type indicators (multiple-choice, short-answer, coding)
Multiple choice options where applicable
Text entry areas for answers

Submit Exam Button: Calls submit_exam(answers_text) to grade the completed exam

![image](https://github.com/user-attachments/assets/4f61472e-5544-4893-8529-cc7887c27331)

# 3. Feedback Section

Results Display: Shows the graded exam with:

Overall score
Question-by-question feedback
Correct/incorrect indicators
Explanations for each question
Correct solutions for missed questions
Improvement Suggestions: Displays personalized learning recommendations
![image](https://github.com/user-attachments/assets/b478474a-5f05-409f-bb3f-b7084a97d3a1)


 
 # 4.Q&A Sandbox Section

Question Input: Text area where students can type Python-related questions
Ask Question Button: Calls answer_sandbox_question(question) to get AI assistance
Answer Display: Shows AI responses with explanations and code examples
Chat History: Displays previous questions and answers for reference

![image](https://github.com/user-attachments/assets/0515b7ad-4a51-4db7-90b3-68853375eb35)
# 5.Progress Tracking Section

View Progress Button: Calls get_learning_progress() to show overall learning statistics
Progress Report: Displays:

Overall completion statistics
Day-by-day progress
Question type performance breakdown
Areas needing improvement
Adaptive learning indicators (showing reinforced topics)

![image](https://github.com/user-attachments/assets/871735ed-babc-4ef4-9c33-7163eb3f290f)




