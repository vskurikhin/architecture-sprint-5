# Задание 3. Установка и настройка окружения
- [x] Python (3.7-3.10): Rasa работает с версиями Python 3.7 и выше, но ниже 3.11.
- [x] pip — менеджер пакетов Python, который будет использоваться для установки Rasa.
- [x] Virtualenv (рекомендуется): использование виртуальной среды для изоляции окружения и зависимостей проекта.

## 1. Убедитесь, что pip установлен. Выполните команду:
```bash
$ python -m ensurepip --upgrade
/usr/bin/python: No module named ensurepip
```

## 2. Установите virtualenv, если он ещё не установлен:
```bash
$ pip install virtualenv
Defaulting to user installation because normal site-packages is not writeable
Collecting virtualenv
  Downloading virtualenv-20.27.1-py3-none-any.whl.metadata (4.5 kB)
Collecting distlib<1,>=0.3.7 (from virtualenv)
  Downloading distlib-0.3.9-py2.py3-none-any.whl.metadata (5.2 kB)
Collecting filelock<4,>=3.12.2 (from virtualenv)
  Downloading filelock-3.16.1-py3-none-any.whl.metadata (2.9 kB)
Collecting platformdirs<5,>=3.9.1 (from virtualenv)
  Downloading platformdirs-4.3.6-py3-none-any.whl.metadata (11 kB)
Downloading virtualenv-20.27.1-py3-none-any.whl (3.1 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 3.1/3.1 MB 9.9 MB/s eta 0:00:00
Downloading distlib-0.3.9-py2.py3-none-any.whl (468 kB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 469.0/469.0 kB 9.3 MB/s eta 0:00:00
Downloading filelock-3.16.1-py3-none-any.whl (16 kB)
Downloading platformdirs-4.3.6-py3-none-any.whl (18 kB)
Installing collected packages: distlib, platformdirs, filelock, virtualenv
  WARNING: The script virtualenv is installed in '/home/vnsk/.local/bin' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
Successfully installed distlib-0.3.9 filelock-3.16.1 platformdirs-4.3.6 virtualenv-20.27.1

[notice] A new release of pip is available: 23.3.2 -> 24.3.1
[notice] To update, run: python3.10 -m pip install --upgrade pip
```

## Создайте виртуальное окружение: 
```bash
$ python -m venv rasa_env
$ echo $?
0
```

## Активируйте виртуальное окружение:
```bash
$ source rasa_env/bin/activate
(rasa_env) $ 
```
