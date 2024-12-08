# Medical Test Explanation - AI Assistant

This project provides an interactive assistant for analyzing and explaining medical test reports from PDF documents. Users can upload a PDF medical report, and the AI assistant will help answer any queries regarding the report's content.

---

## Features

- **Upload PDF Medical Report**: Users can upload a PDF file containing medical test reports.
- **Extract Text**: The text from the uploaded PDF is extracted for processing.
- **AI Chat Interface**: A chat interface is provided to interact with the AI model to answer questions related to the medical report.
- **Groq API Integration**: The assistant uses Groq's AI models for generating responses based on the medical report's content.

---

## Installation

To run this project, you need to install the following dependencies:

### Prerequisites

1. Python 3.7+
2. Pip package manager

### Install Required Packages

Clone the repository and install the necessary packages by running the following command in your terminal:

```bash
git clone https://github.com/Osama-Abo-Bakr/Medical-Test-Analysis.git
cd Medical-Test-Analysis
pip install -r requirements.txt
```

The `requirements.txt` file includes the following packages:

- `PyPDF2` - For PDF file handling and text extraction.
- `streamlit` - For creating the web application interface.
- `python-dotenv` - For loading environment variables from a `.env` file.
- `langchain_groq` - For interaction with Groq AI models.
- `langchain_core` - For prompt and output parsing functionality.

### Set Up Environment Variables

Create a `.env` file in the project directory and include the following configuration:

```
API_KEY=<your_groq_api_key>
```

Replace `<your_groq_api_key>` with your actual Groq API key.

---

## How to Use

1. **Run the Streamlit App**:

   To start the app, run the following command:

   ```bash
   streamlit run app.py
   ```

2. **Upload Medical Test PDF**:

   Once the app is running, use the sidebar to upload a PDF document containing the medical test report. The system will extract text from the PDF.

3. **Ask Questions**:

   After uploading the PDF, use the chat interface to ask questions regarding the medical report. The AI assistant will generate responses based on the extracted text.

4. **Groq API Key**:

   If you're using Groq's models for AI responses, enter your API key in the settings section on the sidebar. Instructions for obtaining the API key are provided within the app.

---

## Code Explanation

### `extract_text_from_pdf`

This function extracts the text content from a PDF file using the `PyPDF2` library. It reads the content of each page and combines them into a single text string.

### `get_response`

This function generates a response from the AI model based on the extracted text from the PDF and the user's query. It uses Groq's `ChatGroq` model for generating responses. The prompt is customized to provide context about analyzing the medical test report.

### `main`

The main function runs the Streamlit app. It handles file uploads, extracts text from PDFs, and allows users to interact with the AI assistant. The chat history is saved in the session state, and the assistant's responses are displayed in the chat interface.

---

## API Integration

The app uses the **Groq API** to generate AI responses. To use the API, follow these steps:

1. Sign in to [Groq Cloud](https://console.groq.com/keys).
2. Create an API key and paste it in the app's settings section.

---

## License

This project is licensed under the MIT License.

---

## Acknowledgments

- **Groq** for providing the AI model used in this project.
- **Streamlit** for the easy-to-use framework for building the web app.

---

For further questions or support, please contact [Your Contact Information].