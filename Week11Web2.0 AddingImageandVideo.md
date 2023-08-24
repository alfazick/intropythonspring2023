
#Adding an image
You need to have structure

main.py
assets -> Folder
    image.jpg
templates -> Folder
    index.html 


index.html content
<!doctype html>
<html lang="en">
  <head>
    <title>Flask Image Display</title>
  </head>
  <body>
    <h1>Flask Image Display</h1>
    <img src="{{ image_path }}" alt="Your Image">
  </body>
</html>


! Don't forget to upload image as well

from flask import Flask, render_template

app = Flask(__name__, static_folder='assets')

@app.route('/')
def index():
    image_path = "/assets/your_image.jpg"
    return render_template('index.html', image_path=image_path)


if __name__ == '__main__':
    app.run(host='0.0.0.0')

#Embedding video

inde.html content

<!doctype html>
<html lang="en">
  <head>
    <title>Flask YouTube Video Display</title>
  </head>
  <body>
    <h1>Flask YouTube Video Display</h1>
    
    <h2>YouTube Video</h2>
    <div style="position: relative; padding-bottom: 30%; padding-top: 30px; height: 0; overflow: hidden;">
      <iframe src="https://www.youtube.com/embed/{{ youtube_video_id }}" frameborder="0" allowfullscreen
              style="position: absolute; top: 0; left: 0; width: 50%; height: 100%;"></iframe>
    </div>
  </body>
</html>


Your web server code main.py

from flask import Flask, render_template

app = Flask(__name__, static_folder='assets')

@app.route('/')
def index():
    youtube_video_id = "6ZZX9iIgFoo"
    return render_template('index.html', youtube_video_id=youtube_video_id)

if __name__ == '__main__':
    app.run(host='0.0.0.0')

