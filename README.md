# llm-chatbot-python
Simple chatbot using OpenAI API
# LLM Chatbot (Python)

This is a simple chatbot built using OpenAI API.

## Features
- Takes user input
- Generates AI response
- Runs in terminal

## Tech Used
- Python
- OpenAI API

## How to Run
1. Install openai
2. Add your API key
3. Run the script

## Note
Do not share your API key publicly.
from openai import OpenAI

client = OpenAI(api_key="YOUR_API_KEY")

while True:
    user_input = input("You: ")
    
    if user_input.lower() == "exit":
        break
    
    response = client.chat.completions.create(
        model="gpt-4o-mini",
        messages=[
            {"role": "user", "content": user_input}
        ]
    )
    
    print("Bot:", response.choices[0].message.content)
