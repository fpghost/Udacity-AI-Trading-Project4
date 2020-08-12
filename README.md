# Setup env

## Env setup with py 3.6.3 like udacity
```
pyenv local 3.6.3
virtualenv proj4venv363 -p python3.6.3
source proj4venv363/bin/activate
```

## Some prereqs (prevents a bunch of errors to do with cython and install_layout)

```
pip install -U setuptools cython
```

## Numpy and pandas

```
# Numpy first then pandas
pip install numpy==1.13.3
pip install pandas==0.18.1
```

# Remaining reqs

Six is commented out as we need a later version that this when using python 3.6.3 else
gets into an `ensure_str`error

```
# orig_reqs.txt
alphalens==0.3.2
colour==0.1.5
cvxpy==1.0.3
cycler==0.10.0
# numpy==1.13.3
# pandas==0.18.1
plotly==2.2.3
pyparsing==2.2.0
python-dateutil==2.6.1
pytz==2017.3
requests==2.18.4
scipy==1.0.0
scikit-learn==0.19.1
# six==1.11.0
tables==3.3.0
tqdm==4.19.5
zipline===1.2.0 
```

Then

```
pip install -r orig_reqs.txt
```

# Make kernel

pip install ipykernal ipython
ipython kernel install --name "proj4-363" --user

# Fix six 1.12 and numpy issue

Finally bump up numpy a little, but not too much (we need six >=1.12  in order to make this an jupyter lab kernel, but numpy 1.13 isn't going to work with that)

```
pip install numpy==1.16.1
```
