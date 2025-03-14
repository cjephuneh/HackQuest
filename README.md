# Scholarship WhatsApp Chatbot

A WhatsApp chatbot built with Twilio that provides information about scholarships and grants for students, powered by Google's Gemini API for intelligent responses.

## Setup Instructions

1. Create a Twilio account at [twilio.com](https://www.twilio.com)
2. Set up a WhatsApp Sandbox in the Twilio console
3. Get a Gemini API key from [Google AI Studio](https://makersuite.google.com/)
4. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
5. Update the `.env` file with your Twilio credentials and Gemini API key
6. Run the application:
   ```
   python main.py
   ```
7. Use ngrok or a similar tool to create a public URL:
   ```
   ngrok http 5000
   ```
8. In the Twilio console, set your webhook URL to `{ngrok_url}/webhook`

## Usage

Users can text the WhatsApp bot with questions about:
- Undergraduate scholarships
- Graduate scholarships
- International scholarships
- Scholarships for minorities
- How to apply for scholarships
- Scholarship deadlines
- Any other scholarship or grant related questions (handled by Gemini AI)

The bot will respond with relevant information from its database or generate an intelligent response using Gemini API.

## Extending the Bot

- To add more structured scholarship information, update the `scholarship_info` dictionary in `main.py`.
- To modify the AI behavior, adjust the system prompt in the `get_gemini_response` function.
