def get_bot_response(user_message):
    """
    Takes user input, processes it, and returns the appropriate bot response.
    Uses simple if-elif-else keyword matching.
    """
    message = user_message.lower().strip()
    if "hello" in message or "hi" in message:
        return "Hello! How can I help you today?"
        
    elif "your name" in message:
        return "I am ChatBot, your friendly neighborhood Python script!"
        
    elif "how are you" in message:
        return "I'm doing great, thank you!"
        
    elif "weather" in message:
        return "I can't check the sky right now, but I hope it's sunny where you are!"
        
    elif "help" in message:
        return "You can ask me about my name, how I'm doing, or say hello!"
        
    else:
        return "I'm sorry, I don't quite understand"


def start_chat():
    """
    Main function that manages the input/output loop and exit conditions.
    """
    print("=========================================")
    print("🤖 ChatBot: Hello! I am a simple chatbot.")
    print("Type 'exit' or 'bye' at any time to quit.")
    print("=========================================\n")

    while True:
        user_input = input("You: ")
        if user_input.lower().strip() in ["exit", "bye", "quit"]:
            print("ChatBot: Goodbye! Have a fantastic day!")
            break 
        bot_reply = get_bot_response(user_input)
        print(f"ChatBot: {bot_reply}\n")
if __name__ == "__main__":
    start_chat()
