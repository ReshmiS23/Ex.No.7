# Exno.7-Develop a prompt-based application tailored to their personal needs, fostering creativity and practical problem-solving skills while leveraging the capabilities of large language models.

# Date:17-11-2025
# Register no:212223060224
# Aim: To develop a prompt-based application using ChatGPT - To demonstrate how to create a prompt-based application to organize daily tasks, showing the progression from simple to more advanced prompt designs and their corresponding outputs.

# AI Tools Required: 
ChatGPT / Any Large Language Model (LLM)

(Optional) Python or command-line interface for simulation

(Optional) Memory-enabled LLM features


# Explanation: 
Prompt:
"Design a personal productivity assistant that can help manage daily tasks, schedule reminders, suggest wellness tips, and answer general queries. The assistant should interact using natural language and be adaptable to the user’s changing preferences over time."
# Procedure:
## 1.Define Core Requirements

Identify what the assistant should do (task management, scheduling, wellness tips, queries).

## 2.Decide how the assistant should interact (friendly, simple, human-like).

Construct Appropriate Prompts

## 3.Create basic prompts for each function.

Example:

“Add a task to my list.”

“Give me a wellness tip.”

“Schedule a reminder at 5 PM.”

Refine prompts to improve the output quality.

Simulate User Interaction

Use ChatGPT or a command-line interface to simulate conversation.

Test different inputs and observe how the assistant responds.

## 4.Collect Feedback & Adapt Responses

Note which prompts give good results and which need modification.

Adjust prompt structure to improve clarity and consistency.

## 5.(Optional) Integrate Memory / Preferences

Add instructions like:
“Remember my preferred wellness tips are related to hydration and stretching.”

Simulate how the assistant adapts over time.
# Expected Output

(This section explains what the LLM-generated assistant should ideally produce.)

Example Response by LLM – Personal Productivity Assistant Features
## 1. Daily Task Manager

Accepts tasks via natural language
Example: “Remind me to call mom at 6 PM.”

Organizes tasks by priority, deadline, and category

Provides daily summaries, pending tasks, and overdue items

## 2. Smart Scheduler

Schedules events with contextual understanding

Sets reminders for both short-term and long-term tasks

Warns about overlapping events, or suggests free time slots

## 3. Wellness Tips Generator

Suggests daily wellness tips

Hydration reminders

Exercise suggestions

Screen-time breaks

Adapts based on user preferences
Example: If the user likes yoga, tips include stretching or breathing exercises.
## Flowchart:
<img width="1024" height="1536" alt="image" src="https://github.com/user-attachments/assets/ec35081d-755f-4346-be81-61c8120e8f12" />

## ✅Python Code – Simple CLI Productivity Assistant

This example uses OpenAI’s API style.
### code:
          import os
     from openai import OpenAI

     client = OpenAI(api_key="YOUR_API_KEY")

     def ask_assistant(prompt):
    response = client.chat.completions.create(
        model="gpt-4o-mini",
        messages=[
            {"role": "system", "content": "You are a helpful personal productivity assistant."},
            {"role": "user", "content": prompt}
        ]
    )
    return response.choices[0].message["content"]

    def main():
    print("\n=== Personal Productivity Assistant (CLI) ===")
    print("Type 'exit' to quit.\n")

    while True:
        user_input = input("You: ")

        if user_input.lower() == "exit":
            print("Goodbye! Stay productive!")
            break

        # Build a structured prompt for the model
        full_prompt = f"""
        Act as my personal productivity assistant.
        Tasks:
        - Manage tasks
        - Schedule reminders
        - Suggest wellness tips
        - Answer general queries

        User request:
        {user_input}

        Provide simple and clear responses.
        """

        output = ask_assistant(full_prompt)
        print("\nAssistant:", output, "\n")

     if __name__ == "__main__":
    main()


# Result: 
The lab exercise resulted in the creation of a prototype concept for a personal assistant powered by large language models. Students were able to:
 Understand how to tailor LLM prompts to real-life applications.
 Foster creativity by designing features suited to their personal or academic lives.
 Learn prompt engineering techniques for optimal interaction with AI tools.
 Experience the versatility and utility of generative AI in solving everyday problems.
