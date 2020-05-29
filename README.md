## Making a Package
* a setup.py file, which is required in order to use pip install
* a folder called 'distributions', which is the name of the Python package
* inside the 'distributions' folder, you'll need the Gaussiandistribution.py file, Generaldistribution.py and an __init__.py file.

Once everything is set up, open a new terminal window in the workspace by clicking 'NEW TERMINAL'. Then type:
```
cd 3a_python_package
pip install .
```

If everything is set up correctly, pip will install the distributions package into the workspace. You can then start the python interpreter from the terminal typing:
`python`

Then within the Python interpreter, you can use the distributions package:
```
from distributions import Gaussian
gaussian_one = Gaussian(25, 2)
gaussian_one.mean
gaussian_one + gaussian_one
```

## uploading a package to PyPi
# python-package
```
python setup.py sdist
pip install twine
```

# commands to upload to the pypi test repository
```
twine upload --repository-url https://test.pypi.org/legacy/ dist/*
pip install --index-url https://test.pypi.org/simple/ distributions
```

# command to upload to the pypi repository
```
twine upload dist/*
pip install distributions
```
