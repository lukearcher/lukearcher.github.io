# Deploying Jupyter Notebook Apps with Heroku

These are my own notes for this process

#### Step 1 - Pick a project

#### Step 2 - Create a local folder
* use the anaconda prompt
* mkdir project_name
* cd project_name

#### Step 3 - Create a virtual environment
* choose a supported python version: https://devcenter.heroku.com/articles/python-support#specifying-a-python-version
* create the environment: conda create -n myenv python=3.9
* activate the environment: conda activate herokutest
* install voila: pip install voila
* install jupyter + any other packages: pip install jupyter numpy matplotlib

#### Step 4 - Open a jupyter notebook
* open jupyter: jupyter notebook
* create a new notebook - rename it: app
* add some content and save it
* close it
* stop jupyter: ctrl + c

#### Step 5 - Test voila locally
* run voila: voila app.ipynb
* stop voila: ctrl + c

#### Step 6 - Create the github repo
* no template
* name it
* give it a description
* add a README file
* add a gitignore ... use python template
* use a license if appropriate (I didn't for this example)
* click Create Repository
* rename the main branch to master

#### Step 7 - Add files to github
* Procfile
  web: voila --port=$PORT --Voila.ip=0.0.0.0 --no-browser --enable_nbextensions=True app.ipynb
* app.ipynb
* requirements.txt
  voila
  jupyter
  numpy
  matplotlib
* runtime.txt
  python=3.9

#### Step 8 - Clone the github repo to local
can use either github desktop or gitbash... but i prefer github desktop

#### Step 9 - Build it on heroku
* use the anaconda prompt
* cd into the cloned github directory (parent folder)
* heroku login -i
* enter username and password
* heroku create
* take note of the app name... because we are going to rename it
* heroku apps:rename heroku-test-la --app shielded-falls-06619
* heroku git:remote -a heroku-test-la
* git push heroku master

#### Step 10 - verify it on heroku
can go straight to the url in a browser:
https://heroku-test-la.herokuapp.com

