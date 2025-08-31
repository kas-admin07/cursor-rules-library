
# Cursor Rules Library

Библиотека модульных правил и инструкций для AI-ассистентов (Cursor и других) под единым форматом.

## Назначение
Предоставляет централизованный репозиторий правил, облегчая:
- Версионирование и code review правил через GitHub
- Повторное использование и подключение как Git submodule или через CI
- Модульную загрузку только необходимых правил по контексту проекта

## Структура репозитория
```
.cursorrules               # Точка входа, содержит иерархию подключаемых модулей
.cursor/rules/
├── core/                  # Базовое поведение (always)
├── context/               # MVP/Production, языки
├── frontend/              # React, TypeScript, UI
├── backend/               # Flask, Python, MongoDB, Java, Node.js
├── architecture/          # Обсуждение дизайна и реализация
├── testing/               # Стратегии тестирования
├── legacy/                # Работа с legacy кодом
└── integration/           # CI/CD, GitHub Issues, инструменты
AGENTS.md                  # Инструкции для любых AI-агентов
README.md                  # Описание репозитория и подключение
CONTRIBUTING.md            # Правила внесения изменений и обзор PR

docs/                       # Дополнительные документы (по желанию)
```

## Быстрый старт

### Подключение в проект
1. Добавьте репозиторий как submodule:
   ```bash
git submodule add https://github.com/your-org/cursor-rules-library .cursor/rules
```2. В корне проекта создайте файл `.cursorrules` со следующим содержимым:
   ```yaml
include:
  - .cursor/rules/core/*.mdc
  - .cursor/rules/context/*.mdc
  - .cursor/rules/frontend/*.mdc
  - .cursor/rules/backend/*.mdc
  - .cursor/rules/testing/*.mdc
  - .cursor/rules/architecture/*.mdc
  - .cursor/rules/legacy/*.mdc
  - .cursor/rules/integration/*.mdc
hierarchy:
  - core
  - context
  - frontend
  - backend
  - architecture
  - testing
  - legacy
  - integration
``` 
3. Перезапустите агента, он сам подгрузит нужные правила.

## Внесение изменений
См. [CONTRIBUTING.md](CONTRIBUTING.md) для требований к PR и code review.

---

*Проект поддерживается вашей командой разработки.*
