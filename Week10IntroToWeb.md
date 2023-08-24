
#"Code for our webserver"

from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def home():
    return render_template('index.html')

@app.route('/second_page')
def second_page():
    return render_template('second_page.html')


if __name__ == '__main__':
    app.run(host='0.0.0.0')


Create folder "templates"

#Part#1
#'index.html'
'''
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Flask One-Page Website</title>
</head>
<body>
    <h1>Welcome to Our One-Page Website!</h1>
</body>
</html>
'''

#Part#2
#'second_page.html'
'''
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Second Page</title>
</head>
<body>
    <h1>Welcome to the Second Page!</h1>
    <a href="/">Back to Home</a>
</body>
</html>
'''

Assignment:
Create a website about yourself
Create a 2 separate links Hobby's and ReadingList

