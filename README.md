# exotic-python 3.x `:black_heart:`

## Table of Contents

- [Python Dictionary Comprehension](#python-dictionary-comprehension)



### Python Dictionary Comprehension
`[:arrow_up: TOP :arrow_up:](#table-of-contents)`
> Dictionary comprehension is an elegant and concise way to create dictionaries.
```python
dictionary = {x:x*x  for x in range(10) if x % 2 == 0}

#Equivalent code 
dictionary = {}
for x in range(10):
 if(x %2 == 0):
  dictionary[x] = x*x
```


![Dictionary Comprehension](https://user-images.githubusercontent.com/20127375/81503402-559bfa00-92db-11ea-911f-fb4347bcc53b.png)
