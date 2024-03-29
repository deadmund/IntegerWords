# IntegerWords
Converts integers to English words.  For example, convert 331002651 to "three hundred thirty one million two thousand six hundred fifty one".


## Installation
IntegerWords is available in the pypi repository: [https://pypi.org/project/IntegerWords/](https://pypi.org/project/IntegerWords/).  It can be easily installed using pip.

```
pip3 install IntegerWords
```


#### Alternative Installation
First install the 'build' module from pip:
```
pip3 install build
```

Then, assuming you have already cloned this repo, build IntegerWords manualy and install it from local that locally built package.

```
user@machine:~/IntegerWords$ python3 -m build
user@machine:~/IntegerWords$ pip3 install dist/*
```



## Bash / CLI Usage:
Use on the command line.

```
user@machine$ python3 -m IntegerWords 331002651
three hundred thirty one million two thousand six hundred fifty one 
user@machine$
```


## API Usage:
Use in your python programs by importing IntegerWords as a python3 module.

```
import IntegerWords


def main():
	num = 331002651
	print(IntegerWords.EnglishInteger(num))

```


## Python Interpreter Usage:
Use directly in the python3 interpreter.

```
user@machine$ python3
>>> from IntegerWords import intw
>>> intw(331002651)
three hundred thirty one million two thousand six hundred fifty one 
>>>
```


## Details
* Negative numbers are not yet supported.
* Integers only.
* Maximum supported value is 999,999,999,999,999,999,999,999,999,999,999,999 (i.e., 999 decillion followed by subsequent 9's)
* This program never outputs the word "and."  For example, when inputting 3001 the output is "three thousand one" not "three thousand and one"  This is acceptable grammar in the United States, but it may seem a bit odd in some cases.  For example, when inputting 3000001 the output is "three million one."  This may seem more awkward than the more colloquial "three million and one", but it is the intended output.
* For documentation about the API consider reading the source code in `IntegerWords.py`
* Inputs with delimiters other than commas are currently not supported (e.g., "331.002.651").


## Pull Requests
Don't like something?  Make a pull request.  This is a very simple project and should be accessible to even beginner programmers.
