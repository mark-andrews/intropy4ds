Python can be installed and used in many different ways.
We will provide an overview of these various methods at the beginning of the course.
Below describes one way of installing and using Python, specically using Jupyter notebook and the pip package installer.

If you prefer to install Jupyter etc on your machine, read on.

There are many ways to install and set up Python and many ways to use Python. 
I will be following the one that I find the easiest and most reliable and best suited for scientific applications. 
I'll call this the pip-virtualenv-jupyter way.
Other ways of installing and using Python are possible, and I will mention them in the course, but it is best to stick to just one way for a course like this, and I think this is the best way.

In terms of setup, there are around five main steps. These steps are the same on Windows, MacOS, Linux.

1. Install Python 3.9
2. Pip install `virtualenv`
3. Create a virtual environment.
4. Install whatever packages are needed with pip, which can be done at any time from then onwards.
5. Launch jupyter notebook

Below I describe how to do this for Windows and MacOS now. 
Personally, I use Linux, but I won't describe the steps for Linux unless someone wants me to, because I will assume that almost everyone will be using Windows or Macs.


# Windows

## Step 1: Install Python 3.9

Go to https://www.python.org/downloads/ and download the Python 3.9 installer.
Strictly speaking, we don't need 3.9.
Python 3.8 would be just as sufficient. 
However, we might as well get the most recent version.

Download the `.exe` installer, and then you install that as normal, i.e. double click the installer.
On the opening dialog box, it might give you the option to 'Add Python 3.8 to PATH'. I said yes to this.

Now, open a DOS shell and type `where python`. You should see something like this.

```
C:\Users\psy3andrem> where python
C:\Users\psy3andrem\AppData\Local\Programs\Python\Python39\python.exe
```

The do `where pip` and you should see something like this.

```
C:\Users\psy3andrem> where pip
C:\Users\psy3andrem\AppData\Local\Programs\Python\Python39\Scripts\pip.exe
```

And check the version with `python --version`. You should see something like this.

```
C:\Users\psy3andrem>python --version
Python 3.9.0
```

## Step 2: Install virtualenv

Using the pip installer, install the virtualenv package by typing this command at the DOS command prompt. (The $ indicates the command prompt)

```
$ pip install virtualenv --user
```

## Step 3: Create a virtual environment

You can have as many virtual environments as you want. Each is a separate Python installation. We will create one for this course. We will call it `pyin01_venv`, but we can call it anything we want.

```
$ python -m venv pyin01_venv
```

This will create the virtual environment in the working directory of the DOS session. Unless you change it, it will be your home directory.
Now, we need to activate the virtual environment. You do this

```
$ pyin01_venv\Scripts\activate.bat
```

If that worked, your prompt should now look something like this.

```
(pyin01_venv) C:\Users\psy3andrem>
```

## Step 4: Install packages

Now, we will install some packages. There are tens of thousands to choose from. We will start with some key packages, which we will install with pip.

```
$ pip install jupyter numpy scipy pandas
```

## Step 5: Launch Jupyter

Now we launch a Jupyter notebook.

```
$ jupyter notebook
```

Doing that should open your browser with a Jupyter notebook session. What this is and how to use it is another matter.


# MacOs

## Step 1: Install Python 3.9

Go here https://www.python.org/downloads and get the installer.

Install that as usual on a Mac.

Now, in the Mac's terminal, check the installation. (The $ here means it is is terminal command prompt).

```
$ which python3
/usr/local/bin/python3
```

```
$ which pip3
/usr/local/bin/pip3
```

## Step 2: Install virtualenv

```
$ pip3 install virtualenv --user
```

## Step 3: Create a virtual environment

You can have as many virtual environments as you want. 
Each is a separate Python installation. We will create one for this course. 
We will call it `pyin01_venv`, but we can call it anything we want.

```
$ python3 -m venv pyin01_venv
```

Now activate that virtual environment.

```
$ source pyin01_venv/bin/activate
```

Now your prompt should look something like this.

```
(pyin01_venv) $
```

## Step 4: Install some packages

Now, we will install some packages. There are tens of thousands to choose from. We will start with some key packages, which we will install with pip.

```
$ pip install jupyter numpy scipy pandas
```

## Step 5: Launch Jupyter

Now we launch a Jupyter notebook.

```
$ jupyter notebook
```

Doing that should open your browser with a Jupyter notebook session. What this is and how to use it is another matter.

