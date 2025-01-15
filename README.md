# Reservation Chatbot Project

## Overview
The **Reservation Chatbot** project is a system designed to provide users with information about various events through a conversational interface. It integrates modern NLP techniques with a user-friendly web-based chat interface. The chatbot is capable of answering questions about event details such as dates, descriptions, locations, and organizers.

---

## Features
- **Event Data Preloading**: Preloads event details into the model's context for efficient querying.
- **Interactive Chatbot**: Answers user questions using a pretrained language model.
- **API Access**: Exposes chatbot functionality through a Flask API.
- **Web Interface**: Streamlit-based web interface for user interaction.
- **Public Accessibility**: Integration with Ngrok to make the API and interface accessible remotely.

---

## Technology Stack
### Backend:
- **Python**: Core programming language for logic and development.
- **Flask**: Lightweight framework for building APIs.
- **Transformers (Hugging Face)**: Pre-trained NLP models for text generation.
- **PyTorch**: Deep learning library for model inference.

### Frontend:
- **Streamlit**: Framework for building an interactive and visually appealing chat interface.

### Other Tools:
- **MySQL Connector**: (Optional) For dynamic database integration.
- **Ngrok**: To expose the API and web app to the internet.

---

## Installation
To run this project, ensure you have Python installed and set up a virtual environment.

### Step 1: Clone the Repository
```bash
git clone https://github.com/omy-younes/ML.git
cd ML
```

### Step 2: Install Dependencies
```bash
pip install -r requirements.txt
```
Ensure the following libraries are installed:
- `transformers`
- `torch`
- `mysql-connector-python`
- `streamlit`
- `flask`
- `pyngrok`

### Step 3: Run the Application
1. **Start the Flask API**:
   ```bash
   python app.py
   ```
   This will launch the chatbot API locally and expose it via Ngrok.

2. **Run the Streamlit Interface**:
   ```bash
   streamlit run app.py
   ```
   The Streamlit app will run on `http://localhost:8502`.

---

## Usage
1. Open the Streamlit app in your browser.
2. Type a query (e.g., "What events are happening in San Francisco?").
3. View the chatbot's response with relevant event details.

---

## Configuration
- **Model**: By default, the project uses `google/flan-t5-base`. To use a different model, update the `model_name` in the script.
- **Database Integration**: Replace the `fetch_reservations` function with a dynamic MySQL query for live data.
- **Ngrok Token**: Set your Ngrok authtoken to expose the API publicly.

---

## Example Queries
- "What events are happening in 2025?"
- "Tell me about events in London."
- "Which event is organized by organizer ID 205?"

---

## Project Structure
```
reservation-chatbot/
|
├── app.py                # Main Flask API script
├── chatbot.py            # Core chatbot logic
├── requirements.txt      # List of dependencies
├── static/               # Static files (if any)
├── templates/            # HTML templates for the web app
└── README.md             # Project documentation
```

---

## Future Enhancements
1. **Dynamic Database Integration**: Replace static event data with live database querying.
2. **Advanced NLP Models**: Use larger or more advanced models for improved responses (e.g., GPT-4, LLaMA2).
3. **User Authentication**: Add login functionality for personalized responses.
4. **Event Filtering**: Allow users to filter events based on criteria like location or date.

---

## License
This project is licensed under the MIT License. See the LICENSE file for more details.

---


