# smart-tasks-db

Заготовка Python-пакета для базы заданий и правил проекта [ctshink](https://t.me/ctshink_bot) — Telegram MiniApp для подготовки к ЦТ/ЦЭ.

## Статус

Сейчас здесь опубликован каркас проекта: метаданные пакета, зависимости и структура будущих модулей. Схема БД, загрузка данных, поиск, сборка заданий и оценка качества пока не реализованы. Единственная команда выводит приветственное сообщение.

## Что есть в репозитории

| Путь | Содержимое |
| --- | --- |
| `pyproject.toml`, `uv.lock` | Python ≥3.12, сборка через uv, зависимости httpx, psycopg и pgvector |
| `src/smart_tasks_db/__init__.py` | Точка входа команды `smart-tasks-db` |
| `src/smart_tasks_db/` | Пустые модули для конфигурации, БД, загрузки, поиска и сборки заданий |
| `sql/001_schema.sql` | Пустой файл будущей схемы |
| `eval/` | Пустые файлы сценария оценки и набора запросов |
| `compose.yaml`, `.env.example` | Пустые заготовки конфигурации |

## Проверить точку входа

Нужны Python ≥3.12 и [uv](https://docs.astral.sh/uv/).

```bash
git clone https://github.com/Kkkucher/smart-tasks-db.git
cd smart-tasks-db
uv sync --locked
uv run smart-tasks-db
```

Ожидаемый вывод текущей команды:

```text
Hello from smart-tasks-db!
```

Это запуск точки входа пакета. База данных не поднимается: `compose.yaml` и SQL-схема ещё пустые. Тестов в репозитории пока нет.

## Лицензия

[MIT](LICENSE).
