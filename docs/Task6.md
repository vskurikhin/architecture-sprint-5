# Задание 6. Адаптация модели и платформы под русский язык

## Для обработки русского языка и использования предобученных моделей, таких как BERT, нужно правильно настроить пайплайн в config.yml. Мы используем модель BERT из ранее установленного пакета transformers.
- [x] Файл config.yml:

### 1. Замените настроенные конфигурации в соответствующих директориях:
- [x] stories.yml
- [x] rules.yml
- [x] nlu.yml
- [x] domain.yml

### 2. Выполните тренировку модели на новой конфигурации:
```bash
$  rasa train
.../IdeaProjects/github.com/vskurikhin/architecture-sprint-5/rasa_env/lib/python3.10/site-packages/rasa/core/tracker_store.py:1044: MovedIn20Warning: Deprecated API features detected! These feature(s) are not compatible with SQLAlchemy 2.0. To prevent incompatible upgrades prior to updating applications, ensure requirements files are pinned to "sqlalchemy<2.0". Set environment variable SQLALCHEMY_WARN_20=1 to show all deprecation warnings.  Set environment variable SQLALCHEMY_SILENCE_UBER_WARNING=1 to silence this message. (Background on SQLAlchemy 2.0 at: https://sqlalche.me/e/b8d9)
  Base: DeclarativeMeta = declarative_base()
...
```

### 3. Запустите ассистента:
```bash
$ rasa run --enable-api 
.../IdeaProjects/github.com/vskurikhin/architecture-sprint-5/rasa_env/lib/python3.10/site-packages/rasa/core/tracker_store.py:1044: MovedIn20Warning: Deprecated API features detected! These feature(s) are not compatible with SQLAlchemy 2.0. To prevent incompatible upgrades prior to updating applications, ensure requirements files are pinned to "sqlalchemy<2.0". Set environment variable SQLALCHEMY_WARN_20=1 to show all deprecation warnings.  Set environment variable SQLALCHEMY_SILENCE_UBER_WARNING=1 to silence this message. (Background on SQLAlchemy 2.0 at: https://sqlalche.me/e/b8d9)
  Base: DeclarativeMeta = declarative_base()
...
2024-11-13 18:48:11 INFO     root  - Starting Rasa server on http://0.0.0.0:5005
2024-11-13 18:48:11 INFO     rasa.core.processor  - Loading model models/20241113-182749-boolean-coda.tar.gz...
Some weights of the PyTorch model were not used when initializing the TF 2.0 model TFBertModel: ['cls.predictions.transform.dense.bias', 'cls.seq_relationship.bias', 'cls.predictions.transform.LayerNorm.weight', 'cls.predictions.transform.LayerNorm.bias', 'cls.predictions.bias', 'cls.seq_relationship.weight', 'cls.predictions.transform.dense.weight']
- This IS expected if you are initializing TFBertModel from a PyTorch model trained on another task or with another architecture (e.g. initializing a TFBertForSequenceClassification model from a BertForPreTraining model).
- This IS NOT expected if you are initializing TFBertModel from a PyTorch model that you expect to be exactly identical (e.g. initializing a TFBertForSequenceClassification model from a BertForSequenceClassification model).
All the weights of TFBertModel were initialized from the PyTorch model.
If your task is similar to the task the model of the checkpoint was trained on, you can already use TFBertModel for predictions without further training.
.../IdeaProjects/github.com/vskurikhin/architecture-sprint-5/rasa_env/lib/python3.10/site-packages/rasa/utils/train_utils.py:530: UserWarning: constrain_similarities is set to `False`. It is recommended to set it to `True` when using cross-entropy loss.
  rasa.shared.utils.io.raise_warning(
.../IdeaProjects/github.com/vskurikhin/architecture-sprint-5/rasa_env/lib/python3.10/site-packages/rasa/shared/utils/io.py:99: UserWarning: 'evaluate_every_number_of_epochs=20' is greater than 'epochs=1'. No evaluation will occur.
2024-11-13 18:48:24 INFO     root  - Rasa server is up and running.
```

```bash
$ rasa run --enable-api --cors "*"
.../IdeaProjects/github.com/vskurikhin/architecture-sprint-5/rasa_env/lib/python3.10/site-packages/rasa/core/tracker_store.py:1044: MovedIn20Warning: Deprecated API features detected! These feature(s) are not compatible with SQLAlchemy 2.0. To prevent incompatible upgrades prior to updating applications, ensure requirements files are pinned to "sqlalchemy<2.0". Set environment variable SQLALCHEMY_WARN_20=1 to show all deprecation warnings.  Set environment variable SQLALCHEMY_SILENCE_UBER_WARNING=1 to silence this message. (Background on SQLAlchemy 2.0 at: https://sqlalche.me/e/b8d9)
  Base: DeclarativeMeta = declarative_base()
...
2024-11-13 18:52:53 INFO     root  - Starting Rasa server on http://0.0.0.0:5005
2024-11-13 18:52:53 INFO     rasa.core.processor  - Loading model models/20241113-182749-boolean-coda.tar.gz...
Some weights of the PyTorch model were not used when initializing the TF 2.0 model TFBertModel: ['cls.seq_relationship.weight', 'cls.seq_relationship.bias', 'cls.predictions.transform.dense.weight', 'cls.predictions.transform.LayerNorm.weight', 'cls.predictions.transform.dense.bias', 'cls.predictions.transform.LayerNorm.bias', 'cls.predictions.bias']
- This IS expected if you are initializing TFBertModel from a PyTorch model trained on another task or with another architecture (e.g. initializing a TFBertForSequenceClassification model from a BertForPreTraining model).
- This IS NOT expected if you are initializing TFBertModel from a PyTorch model that you expect to be exactly identical (e.g. initializing a TFBertForSequenceClassification model from a BertForSequenceClassification model).
All the weights of TFBertModel were initialized from the PyTorch model.
If your task is similar to the task the model of the checkpoint was trained on, you can already use TFBertModel for predictions without further training.
.../IdeaProjects/github.com/vskurikhin/architecture-sprint-5/rasa_env/lib/python3.10/site-packages/rasa/utils/train_utils.py:530: UserWarning: constrain_similarities is set to `False`. It is recommended to set it to `True` when using cross-entropy loss.
  rasa.shared.utils.io.raise_warning(
.../IdeaProjects/github.com/vskurikhin/architecture-sprint-5/rasa_env/lib/python3.10/site-packages/rasa/shared/utils/io.py:99: UserWarning: 'evaluate_every_number_of_epochs=20' is greater than 'epochs=1'. No evaluation will occur.
2024-11-13 18:53:06 INFO     root  - Rasa server is up and running.
```