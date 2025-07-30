To run exploits written ages ago in Python2 you need to create a virtualenv with downgraded python versions. 
```
pip install virtualenv
virtualenv -p /usr/bin/python2.7 venv # or wherever your python2.7 resides
source venv/bin/activate.sh
```
you will encounter errors... see below:

`virtualenv` versions >= 20.22.0 dropped support for creating Python environments for Python versions <= 3.6, so you'll need to downgrade `virtualenv`, e.g.:
```
pip install virtualenv==20.21.1
```

now you can `pip install -r requirements.txt` and it will pull packages that are compliant with python2. enjoy older exploits! 
