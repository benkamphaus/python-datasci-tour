# A Tour of the Python Data Science Ecosystem

---

Using:

* Python 3.5
* Jupyter


w/ Libraries:

* pandas
* numpy
* scikit-learn

---

Bonus:

* TensorFlow
* Keras
* XGBoost

---

I am:

Ben Kamphaus

Machine Learning/Software Engineer at [ThinkTopic](http://www.thinktopic.com/)

I split time between Python and Clojure.

---

Structure:

* salient features of Python (10 minutes)
* pandas module (10 minutes)
* numpy module (10 minutes)
* sklearn module (10 minutes)
* bonus material (10 minutes)

---

But first, demo!!!!

---

## Bird's Eye View of Python Features

---

Dependeny management:

```
pip install sklearn
```

---

++ quick and easy at the command line
-- native dependencies, system global

Docker, `virtualenv`, etc.

---

Multiparadigm

--- 

Object-Oriented

```python
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y
```

---

Functional (-ish)

```python
map(lambda x: x**2, range(10))

[x**2 for x in range(10)]
```

---

Typically imperative:

```python
l = []
for i in range(10):
    if i % 2:
        l.append(i)
```

---

But still, higher order functions!

```python
def add_to(x):
    def add(y):
        return x + y
    return add
```

---

And cool Pythonic things like generators:

```python
def geometric_series(a, r):
    power = 0
    yield a
    while True:
        power += 1
        yield a * r**power
```

---

## pandas

Elevator pitch:

Fast tabular data manipulation

---

When you use it:

* io or database access layer
* relational algebra operations
* basic statistics
* simple visualizations
* input to some machine learnig apis

---

pandas philosophy

* favor views for select, filter, slice (via numpy)
* mutation produces a copy (except with `inplace=True`)
* optimized in c or cython, so fast
* indexes and columns are labeled
