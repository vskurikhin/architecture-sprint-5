# Задание 4. Установка Rasa

## 1. Установите Rasa через pip:
```bash
$ pip3 install rasa
Collecting rasa
...
```

## 2. Установите библиотеку Transformers для работы с предобученными LLM моделями, такими как BERT, GPT:
```bash
$ pip install transformers
Collecting transformers
...
```

## Проверьте, что Rasa и окружение установлено, выполните команду: 
```bash
$ rasa --version
.../IdeaProjects/github.com/vskurikhin/architecture-sprint-5/rasa_env/lib/python3.10/site-packages/rasa/core/tracker_store.py:1044: MovedIn20Warning: Deprecated API features detected! These feature(s) are not compatible with SQLAlchemy 2.0. To prevent incompatible upgrades prior to updating applications, ensure requirements files are pinned to "sqlalchemy<2.0". Set environment variable SQLALCHEMY_WARN_20=1 to show all deprecation warnings.  Set environment variable SQLALCHEMY_SILENCE_UBER_WARNING=1 to silence this message. (Background on SQLAlchemy 2.0 at: https://sqlalche.me/e/b8d9)
  Base: DeclarativeMeta = declarative_base()
Rasa Version      :         3.6.20
Minimum Compatible Version: 3.5.0
Rasa SDK Version  :         3.6.2
Python Version    :         3.10.12
Operating System  :         Linux-6.8.0-48-generic-x86_64-with-glibc2.35
Python Path       :         .../IdeaProjects/github.com/vskurikhin/architecture-sprint-5/rasa_env/bin/python
```
