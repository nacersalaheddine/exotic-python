# exotic-python 3.x :black_heart:

## Table of Contents
- [Python Printing Techniques](#python-printing-techniques)
- [Python assertions](#python-assertions)
- [Python 3-Pilars Functions [map/filter/reduce]](#python-printing-techniques)
- [Python Anonymous/Lambda Functions](#python-anonymouslambda-functions)
- [Python Dictionary Comprehension](#python-dictionary-comprehension)

### Python Anonymous/Lambda Functions
[:arrow_up: TOP :arrow_up:](#table-of-contents) :link:
> *Lambda* functions in python are functions that are defined withought a name.
> *Lambda* functions are also called ~anonymous~ functions.
> Regular functions are defined using the `def` keyword lambda functions are defined using the `lambda` keyword
> *Lambda* functions can have any number of arguments,but can only have one expression.
#### Syntax
```python
lambda arguments : expression
```
#### Examples (Λ_λ)
```python
#Example 1

power = lambda number,p : number**p
print(power(10,2))
# >> 100

#Example 2
from datetime import date
#Get current Year 
current_year = date.today().year
age  = lambda birth_year : current_year - birth_year 
print(age(1994),'years')
# Written in 2020
# >> 26 years

#Example 3
#BMI returns an anonymous function that calculates the Body Mass Index
def BMI():
  return lambda height,weight : round(weight / (height * height), 2)

height = 1.75 # Height in meters
weight = 80 #Weight in kilograms

print("Your Body Mass Index:",BMI()(height,weight))
# >> Your Body Mass Index: 26.12

#Example 
fruits_basket = {'🍉':True,'🍇':False,'🍎':True,'🍌':True}
#Check for existing fruits in basket.
def existing_fruits(fruits,callback):
    for fruit,exists in fruits.items():
        if(callback(exists)):
            print(fruit,end=' ')

existing_fruits(fruits_basket,lambda itm:itm)

#Note: Lambda functions are mostly used as callbacks as an argument to a higher-order function (a function that takes in other functions as arguments). such as built-in map() or filter()
```
![Python Lambda Functions](https://user-images.githubusercontent.com/20127375/81593672-b436a600-93b7-11ea-933e-efff6ee2f51c.png)

### Python Dictionary Comprehension
[:arrow_up: TOP :arrow_up:](#table-of-contents) :link:
> Dictionary comprehension is an elegant and concise way to create dictionaries.
#### Syntax
```python
{key: value for vars in iterable}
```
#### Examples (❛ ᴗ❛)
```python
#Example 1
dictionary = {x:x*x  for x in range(10)}
# >> {0: 0, 1: 1, 2: 4, 3: 9, 4: 16, 5: 25, 6: 36, 7: 49, 8: 64, 9: 81}

#Example 2, People IQ dictionary, if Conditional Dictionary Comprehension
people_iq_dict = {'Salah eddine Nacer': 140, 'Mostafa Maryo': 100, 'Albert Einstein': 160, 'Donald Trump': 20}
people_low_iq_dict = {person:iq for (person,iq) in people_iq_dict.items() if iq < 100}
# >> {'Donald Trump': 20}

#Example 3, Programming languages birth year, if-else Conditional Dictionary Comprehension
programming_languages_year_dict = {'python': 1990, 'pascal': 1970, 'c': 1972, 'c++': 1980, 'java': 1995, 'javascript': 1995, 'dart': 2011, 'julia': 2012, 'c#': 2000, 'matlab': 1978, 'go': 2009, 'objective-c': 1983, 'swift': 2014, 'kotlin': 2011, 'php': 1995, 'ruby': 1993}

programming_languages_youth_dict = {lang: ('old' if year < 2000 else 'young') for (lang, year) in programming_languages_year_dict.items()}
# >> {'python': 'old', 'pascal': 'old', 'c': 'old', 'c++': 'old', 'java': 'old', 'javascript': 'old', 'dart': 'young', 'julia': 'young', 'c#': 'young', 'matlab': 'old', 'go': 'young', 'objective-c': 'old', 'swift': 'young', 'kotlin': 'young', 'php': 'old', 'ruby': 'old'}

#Example
dictionary = {x:x*x  for x in range(10) if x % 2 == 0}

#Equivalent code 
dictionary = {}
for x in range(10):
 if(x % 2 == 0):
  dictionary[x] = x*x
```


![Dictionary Comprehension](https://user-images.githubusercontent.com/20127375/81503402-559bfa00-92db-11ea-911f-fb4347bcc53b.png)
