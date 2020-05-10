# exotic-python 3.x :black_heart:

## Table of Contents

- [Python Dictionary Comprehension](#python-dictionary-comprehension)



### Python Dictionary Comprehension
[:arrow_up: TOP :arrow_up:](#table-of-contents) :link:
> Dictionary comprehension is an elegant and concise way to create dictionaries.
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
