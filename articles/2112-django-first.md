---
title: "2112-django-first"
emoji: "🐕"
type: "tech"
topics: ['python, djang']
published: false
reviewed: false

---

# 2112-django-first

## installation

```cmd
(dj) G:\workspace\djnote>pip install django
Collecting django
  Downloading Django-4.0-py3-none-any.whl (8.0 MB)
     |████████████████████████████████| 8.0 MB 930 kB/s
Collecting tzdata
  Downloading tzdata-2021.5-py2.py3-none-any.whl (339 kB)
     |████████████████████████████████| 339 kB 1.6 MB/s
Collecting asgiref<4,>=3.4.1
  Downloading asgiref-3.4.1-py3-none-any.whl (25 kB)
Collecting sqlparse>=0.2.2
  Downloading sqlparse-0.4.2-py3-none-any.whl (42 kB)
     |████████████████████████████████| 42 kB 394 kB/s
Installing collected packages: tzdata, sqlparse, asgiref, django
Successfully installed asgiref-3.4.1 django-4.0 sqlparse-0.4.2 tzdata-2021.5

(dj) G:\workspace\djnote>dir
 Volume in drive G is New Volume
 Volume Serial Number is A0B0-51B7

 Directory of G:\workspace\djnote

30/12/2021  14:43    <DIR>          .
30/12/2021  14:43    <DIR>          ..
30/12/2021  14:47               184 requirements.txt
               1 File(s)            184 bytes
               2 Dir(s)  98,245,718,016 bytes free

(dj) G:\workspace\djnote>python
Python 3.9.7 (default, Sep 16 2021, 16:59:28) [MSC v.1916 64 bit (AMD64)] :: Anaconda, Inc. on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> import django
>>> print(django.get_version())
4.0
>>> exit()

(dj) G:\workspace\djnote>
```

## python manage-admin.py startproject
