# Задание 5. Настройка Rasa и подключение модели

## После установки Rasa инициализируйте новый проект Rasa, который создаст структуру вашего проекта:
```bash
$ rasa init
.../IdeaProjects/github.com/vskurikhin/architecture-sprint-5/rasa_env/lib/python3.10/site-packages/rasa/core/tracker_store.py:1044: MovedIn20Warning: Deprecated API features detected! These feature(s) are not compatible with SQLAlchemy 2.0. To prevent incompatible upgrades prior to updating applications, ensure requirements files are pinned to "sqlalchemy<2.0". Set environment variable SQLALCHEMY_WARN_20=1 to show all deprecation warnings.  Set environment variable SQLALCHEMY_SILENCE_UBER_WARNING=1 to silence this message. (Background on SQLAlchemy 2.0 at: https://sqlalche.me/e/b8d9)
  Base: DeclarativeMeta = declarative_base()
┌────────────────────────────────────────────────────────────────────────────────┐
│ Rasa Open Source reports anonymous usage telemetry to help improve the product │
│ for all its users.                                                             │
│                                                                                │
│ If you'd like to opt-out, you can use `rasa telemetry disable`.                │
│ To learn more, check out https://rasa.com/docs/rasa/telemetry/telemetry.       │
└────────────────────────────────────────────────────────────────────────────────┘
.../IdeaProjects/github.com/vskurikhin/architecture-sprint-5/rasa_env/lib/python3.10/site-packages/rasa/shared/utils/validation.py:134: DeprecationWarning: pkg_resources is deprecated as an API. See https://setuptools.pypa.io/en/latest/pkg_resources.html
  import pkg_resources
...
```
