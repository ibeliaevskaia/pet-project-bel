# Шпаргалка по командам MkDocs

## Основные команды

| Команда | Описание |
|---------|----------|
| `mkdocs --help` | Показать справку по всем командам |
| `mkdocs --version` | Показать версию MkDocs |
| `mkdocs new [название]` | Создать новый проект |
| `mkdocs serve` | Запустить локальный сервер (http://127.0.0.1:8000) |
| `mkdocs build` | Собрать статический сайт в папку `site/` |
| `mkdocs gh-deploy` | Опубликовать на GitHub Pages |

## Команды с параметрами

| Команда | Описание |
|---------|----------|
| `mkdocs serve -a [IP:PORT]` | Указать адрес и порт |
| `mkdocs serve -w [папка]` | Следить за изменениями в доп. папках |
| `mkdocs serve --verbose` | Подробный вывод (логи) |
| `mkdocs build --clean` | Очистить папку `site/` перед сборкой |
| `mkdocs build -d [папка]` | Указать другую папку для вывода |
| `mkdocs build --strict` | Превратить предупреждения в ошибки |
| `mkdocs gh-deploy --clean` | Очистить старые файлы перед деплоем |
| `mkdocs gh-deploy -b [ветка]` | Указать ветку для деплоя |

## Eсли `mkdocs` не распознан

| Команда | Описание |
|---------|----------|
| `python -m mkdocs serve` | Запуск сервера |
| `python -m mkdocs build` | Сборка сайта |
| `py -m mkdocs serve` | Альтернативный вариант |

## Управление плагинами и темами

| Команда | Описание |
|---------|----------|
| `pip install mkdocs-material` | Установить тему Material |
| `pip install GitPython` | Установить GitPython |
| `pip install mkdocs-git-revision-date-localized-plugin` | Установить плагин дат |
| `pip uninstall [пакет]` | Удалить пакет |
| `pip list \| findstr mkdocs` | Список пакетов MkDocs (Windows) |
| `pip list \| grep mkdocs` | Список пакетов MkDocs (Linux/Mac) |

## Примеры использования

| Что нужно | Команда |
|-----------|---------|
| Создать проект | `mkdocs new my-docs` |
| Запустить на порту 9000 | `mkdocs serve -a 127.0.0.1:9000` |
| Полная пересборка | `mkdocs build --clean` |
| Деплой с очисткой | `mkdocs gh-deploy --clean` |
| Собрать в папку `public` | `mkdocs build -d public` |

## Быстрая диагностика

| Команда | Что проверяет |
|---------|---------------|
| `mkdocs --version` | Установлен ли MkDocs |
| `python --version` | Установлен ли Python |
| `git --version` | Установлен ли Git |
| `pip list \| findstr mkdocs` | Какие плагины установлены |