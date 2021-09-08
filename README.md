# Flask SetUp Guide

### Step 1 - Creating a new project

Navigate to the parent folder where you would like to save your project. Navigate into that folder and create a new folder / new directory. To navigate through folders using your CLI (command line interface such as Command Line, Commander, Terminal, etc.), use the ` cd ` command. You also can copy the path of the folder you want to navigate into and paste it into your CLI to move directly into the parent folder.

![Copy + Paste Path](https://github.com/kcwebers/FlaskSetUpGuide/blob/main/screencaps/nav0.png "Copy + Paste Path")

![Copy + Paste Path](https://github.com/kcwebers/FlaskSetUpGuide/blob/main/screencaps/nav1.png "Copy + Paste Path")

Once in your desired parent directory, you can create your project folder directly in your CLI with the ` mkdir ` command followed by a space and the desired name of your project.

![mkdir](https://github.com/kcwebers/FlaskSetUpGuide/blob/main/screencaps/mkdir.png "mkdir")

Once your project folder has been created, navigate into that folder using the ` cd ` command followed by the name of the project.

![cd into project folder](https://github.com/kcwebers/FlaskSetUpGuide/blob/main/screencaps/cdproject.png "cd into project folder")

### Step 2 - Creating a virtual environment in your project

Inside of the project folder, in this case the project name is ` sample_project ` we need to do our installs for our virtual environment! You can make sure ` pipenv ` is properly installed on your machine. _**If you have installed it once, you do not neet to install it again.**_

Windows
```text
pip install pipenv
```

iOS
```text
pip3 install pipenv
```

Once you have ` pipenv ` available, you can call on it to install for your virtual environment. _**The following commands need to happen for every project you create!**_

Windows & iOS
```text
pipenv install flask
```

For some people, this command will not work so you can run the alternative command as follows.

Windows
```text
python -m pipenv install flask
```

iOS
```text
python3 -m pipenv install flask
```

After completing the installation of Flask, a ` Pipfile ` and ` Pipfile.lock ` should appear in your project folder.

![pipfiles](https://github.com/kcwebers/FlaskSetUpGuide/blob/main/screencaps/pipfile.png "pipfiles")

Lastly, to activate your virtual environment, run the command ` pipenv shell `! Your environment will be activated and you should see some indicator at the start of the line in your CLI that has your project name in paranthese [may vary based on CLI]. _**If you had to use the alternative command for the installation of flask, you will need that same start of the command here**_

![installing and activating virtual environment](https://github.com/kcwebers/FlaskSetUpGuide/blob/main/screencaps/venv.png "installing and activating virtual environment")

To deactivate your virtual environment, run the command ` exit `. _**You should ` exit ` your virtual environment when you move onto a new project. Every environment should be unique to the project you are currently working on!**_

### Step 3 - Creating a server.py and templates folder

After you have properly installed everything needed and activated your virtual environment, you can open your project in your code editor. If you have the setting correct, you can open the project directly from your CLI using the command ` code . ` while in the project folder.

In your code editor, create the file ` server.py ` and the folder ` templates ` directly in the project folder [they should appear alongside eachother, next to the Pipfile and the Pipfile.lock].

![server and templates folder](https://github.com/kcwebers/FlaskSetUpGuide/blob/main/screencaps/server_templates.png "server and templates folder")

_**Important note: The folder that will hold your HTML files must be called ` templates ` otherwise you will get an error!**_

Next up, add this code to your ` server.py ` as a default:

```PY
from flask import Flask, render_template, redirect, session, request
app = Flask(__name__)


@app.route('/')
def index():
    return render_template('index.html')





if __name__=="__main__":
    app.run(debug=True)
```

Reminder that the first 2 lines _must_ occur first and the last 2 lines _must_ occur last.

Create a default HTML page to match the route that you have added to your ` server.py `. In this case we called it ` index.html `. Add ` index.html ` tot he previously created ` templates ` folder. You can use the code below as a simple HTML template that already includes the link for Bootstrap!

```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Index Default</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">

</head>
<body>
    <div class="container">

        <h1>Default HTML Page!</h1>


    </div>
</body>
</html>
```

Make sure you update the ` <title> ` tag for your project!

### Step 4 - Run your server!