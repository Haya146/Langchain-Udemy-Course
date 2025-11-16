🚀 LangChain Demo with LLaMA 3 & Streamlit

This repository contains a simple interactive demo built with Streamlit, leveraging LLaMA 3 through Ollama and powered by LangChain for prompt handling and chaining.
The project also integrates LangSmith for experiment tracing and monitoring.

✨ Features

🧠 Uses LLaMA 3 through Ollama

🔗 Prompt & chain management with LangChain

📊 Built-in tracing via LangSmith

🎨 Clean and interactive Streamlit UI

⚙️ Simple and extensible project structure

📦 Requirements

Make sure you have the following before running the project:

Python 3.10+

Ollama installed locally
Download: https://ollama.com/download

The LLaMA 3 model pulled locally:

ollama pull llama3

🛠 Installation

Clone the repository:

git clone <your-repo-url>
cd <project-folder>


Install dependencies:

pip install -r requirements.txt


If you don’t have a requirements file yet, use:

pip install streamlit langchain langchain-community python-dotenv

🔐 Environment Variables

Create a .env file in the project root and add:

LANGCHAIN_API_KEY=your_langchain_api_key
LANGCHAIN_PROJECT=your_project_name


These enable LangSmith tracing.

▶️ Run the Application

Start Streamlit:

streamlit run app.py


Make sure your Python file is named app.py, or update the command accordingly.

🧠 How It Works

The app uses:

ChatPromptTemplate to build dynamic prompts

Ollama(LLaMA3) as the local LLM

StrOutputParser to clean LLM output

A simple LangChain pipeline:

chain = prompt | llm | output_parser
response = chain.invoke({"question": input_text})


Streamlit displays the result to the user in real time.

📁 Project Structure (Suggested)
.
├── app.py
├── .env
├── README.md
└── requirements.txt

🎯 Usage

Open the Streamlit UI

Enter any question in the text box

LLaMA 3 generates and displays the answer

Logs and traces appear in LangSmith

📜 License

This project is open-source. You may modify and use it freely.