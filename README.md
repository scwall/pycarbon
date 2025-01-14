﻿# Py Carbon

Based on the Carbon library on PHP
----------------------------------

Working on different project in laravel I discovered the Carbon library which helped me a lot by its speed to manage dates, I decided to port this library to python

Getting Started
---------------

#### Prerequisites

+ python 3.6
+ pip

Installing
----------

```
pip install git+https: https://github.com/scwall/pycarbon#egg=pycarbon
```

Use
---

````python
from pycarbon.pycarbon import PyCarbon
p = PyCarbon('first day of december')
# 2021-12-01, 01:54:59
p = PyCarbon('first day of december 2008')
# 2008-12-01, 01:56:35
p = PyCarbon()
p.now()
# 2021-11-12, 01:57:31
p.today()
# 2021-11-12, 00:00:00
p.yesterday()
# 2021-11-11, 00:00:00
p.tomorrow()
# 2021-11-13, 00:00:00
p.add_day()
# 2021-11-14, 00:00:00
p.add_days(10)
# 2021-11-24, 00:00:00
p.sub_day()
# 2021-11-23, 00:00:00
p.sub_days(10)
# 2021-11-13, 00:00:00
p.add_month()
# 2021-12-13, 00:00:00
p.add_months(2)
# 2022-02-13, 00:00:00
p.sub_month()
# 2022-01-13, 00:00:00
p.sub_month(2)
# 2021-11-13, 00:00:00
p.first_of_month()
# 2021-11-01, 00:00:00
p.start_of_month()
# 2021-11-01, 00:00:00
p.to_date_time_string
# 2021-11-01, 00:00:00
p.to_date_string
# 2021-11-01
p.now().add_days(2).add_month().to_date_time_string
# 2021-12-14, 02:08:42

````

Library used
------------

+ Pytz - [stub42/pytz: pytz Python historical timezone library and database (github.com)](https://github.com/stub42/pytz)
+ datetime
+ calendar
+ re

Authors
-------

Pascal de Sélys - Initial work - scwall

License
-------

This project is licensed under the MIT License
