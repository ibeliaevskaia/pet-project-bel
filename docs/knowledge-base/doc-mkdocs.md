        # Шпаргалка по MkDocs 📝

Быстрый справочник по основным командам и настройкам MkDocs — генератора статических сайтов документации из Markdown.

---

## 📦 Установка

```bash
# Установка MkDocs
pip install mkdocs

# Установка с Material темой (рекомендуется)
pip install mkdocs mkdocs-material

# Проверка установки
mkdocs --version

# Создать новый проект
mkdocs new my-project
cd my-project

# Запустить сервер для предпросмотра
mkdocs serve ИЛИ python -m git serve

# Открыть в браузере: http://127.0.0.1:8000/

# Остановить сервер: Ctrl + C

my-project/
├── mkdocs.yml      # Конфигурационный файл
└── docs/
    └── index.md    # Главная страница

    # ---- Обязательные настройки ----
site_name: Моя документация

# ---- Опциональные настройки ----
site_url: https://example.com/
site_description: Описание вашего проекта
site_author: Ваше имя

# ---- Навигация ----
nav:
  - Главная: index.md
  - О проекте: about.md
  - Руководство:
    - Установка: guide/installation.md
    - Использование: guide/usage.md
    - API: guide/api.md

# ---- Тема оформления ----
theme:
  name: material              # material, readthedocs, mkdocs
  language: ru                # Русский язык интерфейса
  features:                   # Доп. функции (для material)
    - navigation.tabs
    - navigation.sections
    - search.highlight

# ---- Расширения Markdown ----
markdown_extensions:
  - admonitions               # !!! note "Заметка"
  - codehilite                # Подсветка кода
  - tables                    # Таблицы
  - toc:
      permalink: True         # Якоря у заголовков

# ---- Плагины ----
plugins:
  - search                    # Поиск (встроенный)
  - mkdocstrings              # Автодокументация из кода (опционально)

# ---- Дополнительно ----
docs_dir: docs                # Папка с исходниками (по умолчанию)
site_dir: site                # Папка для собранного сайта
extra_css:
  - css/extra.css             # Дополнительные стили
extra_javascript:
  - js/extra.js               # Дополнительные скрипты

  project/
├── mkdocs.yml
├── docs/
│   ├── index.md              # Главная
│   ├── about.md              # О проекте
│   ├── guide/
│   │   ├── index.md          # Обзор руководства
│   │   ├── installation.md
│   │   └── configuration.md
│   ├── api/
│   │   └── endpoints.md
│   └── images/               # Изображения
│       ├── logo.png
│       └── screenshot.png
├── site/                     # Собранный сайт (не коммитить)
└── .gitignore

site/
__pycache__/
*.pyc
.venv/
venv/

