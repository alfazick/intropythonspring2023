


Most of the code should be familiar
New IDEA:Intro to  Web Development : Usage of templates


Passing a variable to the template

=> html file
# Don't forget to create a templates folder

<!doctype html>
<html>
  <head>
    <title>Flask Template - Variable</title>
  </head>
  <body>
    <h1>Hello, {{ name }}!</h1>
  </body>
</html>

=> Python code
from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def index():
    return render_template('index.html', name='User')

if __name__ == '__main__':
    app.run(debug=True, host='0.0.0.0', port=8080)




Passing a dictionary to the template
<!doctype html>
<html>
  <head>
    <title>Flask Template - Dictionary</title>
  </head>
  <body>
    <h1>Hello, {{ user.name }}!</h1>
    <p>Age: {{ user.age }}</p>
    <p>City: {{ user.city }}</p>
  </body>
</html>

from flask import Flask, render_template
app = Flask(__name__)
@app.route('/')
def index():
    user_info = {
        'name': 'User',
        'age': 25,
        'city': 'San Francisco'
    }
    return render_template('index.html', user=user_info)

if __name__ == '__main__':
    app.run(debug=True, host='0.0.0.0', port=8080)





Passing the result of an API call to the template (using the JokeAPI)

<!doctype html>
<html>
  <head>
    <title>Flask Template - API Result</title>
  </head>
  <body>
    <h1>Joke of the Day</h1>
    <p>{{ joke }}</p>
  </body>
</html>

import requests
from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def index():
    response = requests.get('https://v2.jokeapi.dev/joke/Any?format=text')
    joke = response.text
    return render_template('index.html', joke=joke)

if __name__ == '__main__':
    app.run(debug=True, host='0.0.0.0', port=8080)



Assignment: Create a website which shows in real time
The weather at Edinburg
Price of Etherium in USD
Price of Bitcoin in USD
And joke of the day :)

Everytime I renew the page data should update accordingly
There you have it dynamic web page :)


