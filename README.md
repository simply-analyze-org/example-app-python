# Example code for integrating a Python Application

This is a simple python application to show you how to integrate with the SimplyAnalyze 
service. The app sends a question to OpenAI and prints a response. Both the question and 
the LLM answer are sent to the SimplyAnalyze service by making a "fire and forget" API
call so that no latency is added to your LLM requests -- the api call is executed in a 
separate thread.

## Requirements to run this example code
Before you start you'll need a few things:
- A valid SimplyAnalyze bearer token and chatbot id. Head to simplyanalyze.ai to create a free account
- A valid OpenAI api key if you want to try it with their api output. Note that this is optional and you can also use different model by customizing the code provided
- We are also using Langchain and python-dotenv in this example. Note that these two are not requirements, just packages to quickly get you up and running in this example

## SimplyAnalyze Helper
The SimplyAnalyze helper includes a function to call our API using a separate thread.
Make sure to load the SA environment variables in this file.

