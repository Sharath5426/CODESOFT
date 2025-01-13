# CODESOFT CHATBOT WITH RULE-BASED RESPONSES

import re
from datetime import datetime

def chatbot():
    print("Simple Chatbot: Hi! I'm here to help. Type 'exit' to end the chat.")
    
    while True:
        user_input = input("You: ").lower().strip()

        # Exit condition
        if user_input in ["exit", "quit", "bye"]:
            print("Simple Chatbot: Goodbye! Have a great day!")
            break

        # Greetings
        elif re.search(r'\bhello\b|\bhi\b|\bhey\b', user_input):
            print("Simple Chatbot: Hello! How can I assist you today?")

        # Asking about the chatbot
        elif re.search(r'\bwho are you\b|\bwhat are you\b', user_input):
            print("Simple Chatbot: I'm a simple chatbot created to assist with basic queries.")

        # Weather-related queries
        elif re.search(r'\bweather\b', user_input):
            print("Simple Chatbot: I can't fetch live weather updates, but it's always good to check online!")

        # Time-related queries
        elif re.search(r'\btime\b|\bdate\b', user_input):
            now = datetime.now()
            print(f"Simple Chatbot: The current date and time is {now.strftime('%Y-%m-%d %H:%M:%S')}.")

        # Asking for jokes
        elif re.search(r'\bjoke\b|\bfunny\b', user_input):
            print("Simple Chatbot: Why don't scientists trust atoms? Because they make up everything!")

        # Health-related queries
        elif re.search(r'\bhealth\b|\bexercise\b', user_input):
            print("Simple Chatbot: Staying active and eating balanced meals is the key to good health!")

        # Study tips
        elif re.search(r'\bstudy\b|\bexam\b', user_input):
            print("Simple Chatbot: Break your study sessions into smaller chunks, take regular breaks, and stay hydrated!")

        # Food-related queries
        elif re.search(r'\bfood\b|\brecipe\b', user_input):
            print("Simple Chatbot: I'm not a chef, but pasta is always a great choice! Need a recipe?")

        # Programming help
        elif re.search(r'\bpython\b|\bprogramming\b', user_input):
            print("Simple Chatbot: Python is a versatile programming language. Need help with code? Let me know!")

        # Travel advice
        elif re.search(r'\btravel\b|\btrip\b', user_input):
            print("Simple Chatbot: Traveling is exciting! Always plan ahead and keep a checklist of essentials.")

        # Generic fallback
        else:
            print("Simple Chatbot: I'm not sure how to respond to that. Can you try rephrasing?")

if __name__ == "__main__":
    chatbot()

