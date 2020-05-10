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

#Example 2, People IQ dictionary
people_iq_dict = {'Salah eddine Nacer': 140, 'Mostafa Maryo': 100, 'Albert Einstein': 160, 'Donald Trump': 20}
people_low_iq_dict = {person:iq for (person,iq) in people_iq_dict.items() if iq < 100}
# >>{'Donald Trump': 20}

#Example
dictionary = {x:x*x  for x in range(10) if x % 2 == 0}

#Equivalent code 
dictionary = {}
for x in range(10):
 if(x % 2 == 0):
  dictionary[x] = x*x
```


![Dictionary Comprehension](https://user-images.githubusercontent.com/20127375/81503402-559bfa00-92db-11ea-911f-fb4347bcc53b.png)
