# Bedrock-Knowledge-Base-Chatbot-RAG-AWS-EC2-Deployment-Streamlit-GenAI-App

## RAG Chatbot using AWS Bedrock & Streamlit

### Overview
This project is a Retrieval-Augmented Generation (RAG) Chatbot built using AWS Bedrock, Streamlit, and deployed on an EC2 instance. The application allows users to input queries and receive intelligent responses powered by Amazon's foundation models.

The system demonstrates how Generative AI can be integrated into real-world applications using cloud infrastructure.

### Key Features
🔹 Interactive chatbot UI using Streamlit

🔹 Integration with AWS Bedrock Runtime

🔹 Uses Amazon Titan Text Models

🔹 Cloud deployment using AWS EC2

🔹 Secure access using IAM Roles (No hardcoded credentials)

🔹 Scalable and production-ready architecture

### Tech Stack
Category
Tools/Services
Frontend
Streamlit
Backend
Python
Cloud
AWS EC2
AI/ML
AWS Bedrock
SDK
Boto3
Version Control
Git & GitHub

### Project Structure
rag-bedrock-app/
│
├── app.py               # Main Streamlit application
├── requirements.txt     # Dependencies
├── README.md            # Project documentation

### Installation & Setup
🔹 1. Clone the Repository
git clone https://github.com/your-username/rag-bedrock-app.git
cd rag-bedrock-app
🔹 2. Install Dependencies
pip install -r requirements.txt
🔹 3. Configure AWS
Ensure AWS credentials are configured:
aws configure
Or (Recommended for EC2): ✔ Attach IAM Role with:
AmazonBedrockFullAccess
AmazonS3FullAccess
🔹 4. Run the Application
streamlit run app.py

### Deployment on AWS EC2
Steps:
Launch EC2 Instance (Ubuntu recommended)
Connect via SSH
Install Python & dependencies
Clone repository
Run:
streamlit run app.py --server.port 8502 --server.address 0.0.0.0
Open browser:
http://99.79.50.114:8502/

### IAM Role Configuration
Ensure your EC2 instance has an IAM role with:
AmazonBedrockFullAccess
AmazonS3FullAccess
This avoids the need for access keys inside code.

### Challenges Faced
❌ Model availability issues across regions
❌ Credential errors (NoCredentialsError)
❌ Deployment differences between local and EC2

### Solutions
Used IAM roles instead of credentials
Verified model availability per region
Standardized environment between local and EC2

### Application Preview
User inputs a question
Model processes via AWS Bedrock
Response displayed instantly on UI

### Future Enhancements
🔹 Add document-based retrieval (true RAG pipeline)
🔹 Integrate vector databases (FAISS / OpenSearch)
🔹 Add chat history & memory
🔹 Improve UI/UX
🔹 Add authentication layer

## Author
BATHULA VENU GOPAL
Intern @ Innomatics Research Labs

### Acknowledgements
Special thanks to Innomatics Research Labs for guidance and support throughout this project.

### Note
This project is built using AWS Bedrock (Free Tier / Limited Access Models).
For production-level performance, upgraded model access or subscription may be required.

