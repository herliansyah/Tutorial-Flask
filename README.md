# Tutorial-Flask

Pada Tutorial kali ini diasumsikan anda menggunakan windows dan system anda sudah terinstal python

## Instalasi flask ##

#### Install Virtual environtment di system ####

`` pip install virtualenv ``

#### Buat Virtual Environtment untuk flask ####

```bash
$ mkdir myproject
$ cd myproject
$ virtualenv venv
New python executable in venv/bin/python
Installing setuptools, pip............done.
```

#### Aktifkan Virtualenv ####

```bash
$ venv\Scripts\activate
```

#### Untuk me Non Aktifkan Virtualenv ####

```bash
$ venv\Scripts\deactivate.bat
```

#### Install flask di Virtual Environtment ####

```bash
$ pip install Flask
```

#### Buat File Contoh Flask ###

hello.py

```python
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello_world():
    return 'Hello, World!'
```

#### Export Environtment #####

```bash
$ set FLASK_APP=hello.py
```

Untuk OS Linux/Mac gunakan perintah ``export``

#### Run Aplikasi #####

```bash
$ python -m flask run
 * Running on http://127.0.0.1:5000/
```

atau

```bash
$ flask run
 * Running on http://127.0.0.1:5000/
```

agar bisa di akses dari komputer lain mana gunakan perintah 

```bash
$ flask run --host=0.0.0.0
```

agar aplikasi otomatis reload jika ada perubahan maka tambahkan perintah berikut sebelum ``run``

```bash
$ set FLASK_DEBUG=1
```

Untuk OS Linux/Mac gunakan perintah ``export``
