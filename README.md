# Python-
Python projects
here i have created a simple chat bot by importing gemini ai
thank you

import google.generativeai as genai
API_KEY ="AIzaSyDM2DwHrJA6iQOAuhNOTBZQ4Snm4tNhgA0"
genai.configure(api_key=API_KEY)

model=genai.GenerativeModel("gemini-2.0-flash")
chat=model.start_chat()

print("chat with Gemini! Type 'exit' to quit" )
while True:
    user_input = input("you: ")
    if user_input.lower()== 'exit':
        break
    respond= chat.send_message("hello")
    print("Gemini",respond.text)
