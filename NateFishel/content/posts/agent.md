---
title: "Empowering Your Application: Crafting an AI Agent with OpenAI's GPT"
date: 2023-12-7T22:12:49-05:00
draft: false
tags:
- GPT
- AI
- Python
- API
type: post
---
## Preface
This post was originally going to be one long piece. However, due to the upcoming holidays and taking care of a sick child, 
it will be split into multiple parts. Part one will cover the usage of the OpenAI text completion API via Python. Part two will demonstrate how to parse the response to call our own API. 
Lastly, in part three, I will guide you through setting up an API to interact with our Python program and build a chat interface embeddable into a web app.

## Introduction
Unless you've been living under a rock for the last few years, you've likely encountered OpenAI’s ChatGPT. 
The GPT models provide responses so convincingly intelligent that they could be mistaken for real human responses. 
OpenAI enables developers to use the GPT models via their Chat Completions API, 
which allows the utilization of external functions to expand the capabilities of GPT models. 
In the field of AI, a bot that is capable of performing tasks is often referred to as an Agent.

## Objective
I currently have an application consisting of a Single Page App working alongside a backend REST API composed of multiple microservices. 
My goal is to integrate a chat interface into my app to facilitate users in achieving their objectives more efficiently. 
This chat interface will enable users to save time by simply asking our Agent to perform tasks on their behalf. 
I’ve designed a basic diagram to illustrate how this will function.

![alt text](/images/chat.png "Sequence diagram of chat interface working")

Users will input their commands into the text box, which will be received by our application. 
Our application will then forward the user's message to the GPT model and receive a response containing text and function parameters. 
We will utilize these parameters to invoke our application's API and execute the task. 
Finally, we will provide all this information back to the user in the form of a chat response.


### OpenAI integration
Let's delve into the most intriguing aspect of the project: OpenAI integration. 
OpenAI offers an excellent overview of function calling from models https://cookbook.openai.com/examples/how_to_call_functions_with_chat_models. 
Begin by installing the necessary libraries and selecting your model. Your Python file should start with something similar to the following:
```
import json
import openai
import requests
from tenacity import retry, wait_random_exponential, stop_after_attempt
from termcolor import colored

GPT_MODEL = "gpt-3.5-turbo-0613"
```
Next, our task is to define an array of objects to describe the tools available to the model. 
For the sake of this blog post, I'll add only one tool, but you have the flexibility to include as many as needed. 
It's important to note that OpenAI suggests a more efficient approach if you're defining multiple tools. 
Instead of passing the array with each API call, it's recommended to utilize a fine-tuned model.

```
tools = [
    {
        "type": "function",
        "function": {
            "name": "create_workout",
            "description": "Add a new workout to a players schedule",
            "parameters": {
                "type": "object",
                "properties": {
                    "start": {
                        "type": "string",
                        "description": "The start date and time of the workout, e.g. 2023-11-19T22:12:49-05:00",
                    },
                    "end": {
                        "type": "string",
                        "description": "The end date and time of the workout, e.g. 2023-11-19T22:12:49-05:00",
                    },
                    "name": {
                        "type": "string",
                        "description": "The name of the workout",
                    },
                    "name": {
                        "type": "string",
                        "description": "The name of the workout",
                    },
                    "intensity": {
                        "type": "string",
                        "enum": ["recovery", "low", "maintenance", "high", "extreme"],
                        "description": "The intensity of the workout",
                    },
                },
                "required": ["start", "end", "name", "intensity"],
            },
        }
    }
]

```
Lets add the a bit of code to allow us to call the api and pass in some messages

```
messages = []
messages.append({"role": "system", "content": "Don't make assumptions about what values to plug into functions. Ask for clarification if a user request is ambiguous."})
messages.append({"role": "user", "content": "Please create a new workout"})
chat_response = chat_completion_request(
    messages, tools=tools
)
assistant_message = chat_response.json()["choices"][0]["message"]
messages.append(assistant_message)
pretty_print_conversation(messages)
print(chat_response.json()["choices"][0])
```
Running this we get a response back from the model

```
system: Don't make assumptions about what values to plug into functions. Ask for clarification if a user request is ambiguous.

user: Please create a new workout

assistant: Sure, I can help you create a new workout. Could you please provide the following information:

1. Start date and time of the workout (e.g., 2023-11-19T22:12:49-05:00)
2. End date and time of the workout (e.g., 2023-11-19T22:12:49-05:00)
3. Name of the workout
4. Intensity of the workout (recovery, low, maintenance, high, extreme)

Please provide the values for these parameters.

```
And if we provide the values its asking for we get back

```
{
    'index': 0, 
    'message': {
        'role': 'assistant', 
        'content': None, 
        'tool_calls': [{
            'id': 'call_******', 
            'type': 'function', 
            'function': {
                'name': 'create_workout', 
                'arguments': '{\n  "start": "2023-11-19T22:12:49-05:00",\n  "end": "2023-11-19T22:12:49-05:00",\n  "intensity": "high",\n  "name": "Long Run"\n}'}}
        ]}, 
        'finish_reason': 'tool_calls'
}
```
Fantastic! With this setup, users can seamlessly interact with our API using natural language.
Moreover, we can prompt for multiple values, enabling the creation of an entire workout schedule effortlessly. 
In the upcoming section, we'll focus on parsing the returned arguments and leveraging them to trigger our API, 
further enhancing the functionality and usability of our system. Stay tuned for the next part!


