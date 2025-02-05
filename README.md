# resume-screening-using-ML-concepts
**AIcruiter** is an AI-powered recruitment automation tool designed to streamline the hiring process.  

### **How It Works:**  
1. **Input:** The system takes a **candidate’s resume** and the **job description** as input.  
2. **AI Processing:** It analyzes the resume, extracts key skills, experience, and qualifications.  
3. **Matching Algorithm:** The AI compares the resume with the job description to determine eligibility.  
4. **Decision Making:** Based on the match score, it decides if the candidate is a good fit for the role.  
5. **Email Notification:** AIcruiter automatically sends an email to the candidate.  

### **Key Features:**  
✔ **Automated Screening** – Reduces manual effort in candidate evaluation.  
✔ **Fast & Efficient** – Provides instant eligibility results.  
✔ **Accurate Matching** – Uses AI to assess skills and experience.  
✔ **Customizable Criteria** – Adjusts matching parameters as needed.  
✔ **Seamless Communication** – Sends clear eligibility emails to candidates.  

AIcruiter helps recruiters save time, improve efficiency, and make data-driven hiring decisions! 🚀

**Install required dependencies**
*PyPDF2:* Reads and extracts text from PDF documents.
*pydata-google-auth:* Simplifies logging in to Google.
*groq:* Helps us connect with AI models to analyze and process text.
*langchain:* Makes it easy to create tasks using AI by building smart text-based workflows.



**Imports and Their Functions**
*Authentication and Google API:*
pydata_google_auth, build, HttpError: These are used to handle Google login, manage authentication tokens, and connect with Google services like Gmail and Calendar.

*AI and Prompt Management:*
Groq, PromptTemplate: These are used to interact with AI models and create structured prompts (questions) for the AI to understand and process.

*File Handling:*
PdfReader, files: These help read text from PDF files and allow file uploads in Google Colab.

*Utilities:*
datetime, base64, os: These are used to work with dates and times, encode data (for example, in emails), and manage files and directories.


**Define Global Variables**
*api_key*: API key for the Groq AI service.
*SCOPES*: Permissions for accessing Google Calendar and Gmail APIs.


**Google Authentication:**
*Purpose:* Authenticate access to Google services using OAuth2.
*Key Steps:*
-Fetch user credentials for specified SCOPES.
-Return credentials for use in Gmail and Calendar API operations.


**Extract text from PDF**
*Purpose*: Extracts text content from a PDF.
*Key Steps:*
-Reads the PDF file.
-Concatenates text from all pages into a single string.


**Assess Suitability**
*Purpose:* Uses AI to determine if a candidate matches the job description.
*Key Steps:*
-Creates a structured prompt for the AI model.
-Sends the query to the Groq API.
-Returns a simple "YES" or "NO" decision.


**Send an email to specific email ID with given subject and body**
*Purpose:* Sends an email using Gmail API.
*Key Steps:*
-Encodes the email message.
-Sends it through the Gmail service.


**Schedule an invitation for the Interview if the candidate is shortlisted**
*Purpose:* Creates a calendar event and generates a Google Meet link.
*Key Steps:*
-Schedules a 30-minute interview for the next day.
-Sends event details to Google Calendar.


**Resume Screening**
*Purpose:* Coordinates the full process.
*Key Steps:*
-Authenticates Google APIs.
-Extracts text from PDFs.
-Uses AI to evaluate the candidate.
-Sends emails based on the decision.
-If selected, schedules an interview.


**User Interaction**
*Purpose:* Accepts user inputs and starts the screening process.
*Key Steps:*
-Prompts for job description and resume uploads.
-Collects candidate details.
-Initiates the resume_screening function.
