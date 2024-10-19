Legal Predict IQ

Legal Predict IQ is an AI-driven platform designed to assist legal professionals and students with case law analysis and legal outcome predictions. Powered by advanced NLP models, the system provides accurate and context-aware responses to legal queries based on uploaded legal documents. Key features include:

AI-Powered Case Analysis: Legal Predict IQ utilizes machine learning to analyze case laws, predict outcomes, and offer actionable insights.
Chatbot for Legal Queries: Users can access the platform's chatbot to query legal topics and receive responses derived from case law databases and legal documents.
Admin-Controlled Data Uploads: Only admins have access to upload and update legal documents (PDFs, text files) on a regular basis, ensuring the data remains accurate and up-to-date.
User Access: Regular users, including lawyers, legal researchers, and students, can only interact with the chatbot to retrieve information from the available data.
By automating legal research and offering predictive insights, Legal Predict IQ reduces manual work, making legal information easily accessible to users through an intuitive chatbot interface

This highlights that users can only interact with the chatbot, while data management is strictly handled by admins.

Technologies Used
Streamlit: For building the interactive web application.
SQLite: For storing the uploaded files.
Hugging Face Transformers: For text and code summarization using the BART model.
Replicate API: For generating image summaries.
scikit-learn: For calculating the similarity between user queries and file summaries using TF-IDF and cosine similarity.

Models
BART (Bidirectional and Auto-Regressive Transformers): Used for summarizing text and code files. It is pre-trained on a large corpus of text and fine-tuned for summarization tasks.
Setup and Installation
Clone the Repository:

bash
git clone <repository_url>
cd onboardmate
Create a Virtual Environment:

bash
python3 -m venv venv
source venv/bin/activate
Install Dependencies:

bash
pip install -r requirements.txt
Set Up Database:
Ensure the database directory exists and create the SQLite database.

bash
mkdir -p database
python -c 'from chatbot import create_database; create_database()'
Add Replicate API Token:
Update the chatbot.py file with your Replicate API token.

python
client = replicate.Client(api_token="Your-Replicate-API-Token")
Run the Application:

bash
streamlit run app.py


Future Enhancements
We plan to continuously evolve Legal Predict IQ with the following potential enhancements:
Advanced NLP Models: Integrating more sophisticated legal-specific NLP models to improve the accuracy of legal predictions and responses.

Multi-Language Support: Expanding the platform to support multiple languages, enabling legal analysis in various jurisdictions.

Real-Time Legal Updates: Automating the ingestion of the latest case law and legal updates to ensure that users always have access to the most current information.

Legal Citation Generator: Adding a feature to generate citations for legal cases and documents in various formats (e.g., Bluebook, MLA, etc.).

Collaborative Research Tools: Introducing tools for users to collaborate on case studies and legal research projects directly within the platform.

Mobile Application: Developing a mobile version of Legal Predict IQ for on-the-go access to legal insights and chatbot functionality.

Integrations with Legal Databases: Connecting to external legal databases like LexisNexis and Westlaw to enhance the scope and depth of data.

Analytics Dashboard: Providing detailed analytics for users, including case law trends, prediction accuracy, and insights into legal research patterns.

These enhancements aim to make Legal Predict IQ even more robust, user-friendly, and valuable for legal professionals and researcher
