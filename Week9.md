API

#0 Basic Intro:

import requests

url = "https://example.com"

response = requests.get(url)

if response.status_code == 200:
    
    html_content = response.text
    print(html_content)
else:
    print(f"Request failed with status code {response.status_code}")

#1 Weather Example

import requests

location = "New York"
url = f"https://wttr.in/{location}?format=%C+%t+%w+%h"

response = requests.get(url)

if response.status_code == 200:
    weather_data = response.text
    print(f"Weather in {location}: {weather_data}")
else:
    print(f"Request failed with status code {response.status_code}")


#2 Jokes

import requests

url = "https://v2.jokeapi.dev/joke/Any"

response = requests.get(url)

if response.status_code == 200:
    joke_data = response.json()
    
    if joke_data["type"] == "single":
        print(joke_data["joke"])
    else:
        print(f"{joke_data['setup']} {joke_data['delivery']}")
else:
    print(f"Request failed with status code {response.status_code}")

#3 Jokes Fine-Tuning Example

https://jokeapi.dev # Documentation for API

import requests

url = "https://v2.jokeapi.dev/joke/Dark?blacklistFlags=religious&type=single"

response = requests.get(url)

if response.status_code == 200:
    joke_data = response.json()
    
    if joke_data["type"] == "single":
        print(joke_data["joke"])
    else:
        print(f"{joke_data['setup']} {joke_data['delivery']}")
else:
    print(f"Request failed with status code {response.status_code}")


Practice:

1) Assignment: Weather Information Program
Objective:
Write a program in Python that allows users to fetch the current weather information for a specified location using a public weather API.

Requirements:
Use the requests library to send HTTP requests to the weather API.
Implement error handling for potential issues like invalid locations or connectivity problems.
Display the weather information in a user-friendly format.

2) Jokes Program:
Write a program to generate jokes, ask a user in which genre he wants the joke be about.
Print 5 jokes on the screen.
And save jokes in TodayJokes.txt

