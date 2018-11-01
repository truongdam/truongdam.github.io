---
layout: post
title: Seleniumbase examples
comments: true
---

## Setup and run seleniumbase examples:
Setup seleniumbase project
-Clone project
git clone https://github.com/seleniumbase/SeleniumBase.git

- Install virtualenv in project:
cd Seleniumbase
virtualenv env 
virtualenv -p python3 env

- Install SeleniumBase:
cd SeleniumBase
pip install -U -r requirements.txt
python setup.py install

(Use python setup.py develop if configuring seleniumbase inside a virtual environment.)

-Install web driver to the seleniumbase/drivers folder:
seleniumbase install chromedriver
seleniumbase install geckodriver

-Setup path enviroment:
export PATH=$PATH:/home/truonghaingocdam/projects/SeleniumBase/seleniumbase/drivers/:/home/truonghaingocdam/software/firefox

-Run:
cd examples
pytest my_first_test.py --browser=firefox