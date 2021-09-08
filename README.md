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