# Python Code Formatting and Style Guide

## Introduction

1. **Black**: Форматтер кода, который автоматически форматирует ваш Python-код в соответствии с рекомендациями PEP 8.
2. **isort**: Инструмент для последовательной и организованной сортировки импорта Python.
3. **flake8**: Инструмент для линтинга кода, который проверяет ваш код на соответствие PEP 8 и выявляет потенциальные проблемы.
4. **Pre-commit Hooks**: Механизм для автоматического выполнения проверок перед каждым коммитом.

---

## 1. Using Black
Для использования Black:

1. Install Black:
   ```
   pip install black
   ```

2. Format your code:
   ```
   black Example_my_file.py
   ```

## 2. Sorting Imports with isort
Для использования isort:

1. Install isort:
   ```
   pip install isort
   ```

2. Sort your imports:
   ```
   isort Example_my_file.py
   ```

## 3. Code Linting with flake8
Для использования flake8:

1. Install flake8:
   ```
   pip install flake8
   ```

2. Run flake8 on your code:
   ```
   flake8 Example_my_file.py
   ```

## 4. Pre-commit Hooks
Для настройки pre-commit hooks для вашего проекта:

1. Install the `pre-commit` package:
   ```
   pip install pre-commit
   ```

2. Создайте в каталоге проекта файл `.pre-commit-config.yaml` со следующим содержимым:

   ```yaml
   repos:
    - repo: https://github.com/psf/black
        rev: 23.7.0
        hooks:
        - id: black

    - repo: https://github.com/pycqa/isort
        rev: 5.13.2
        hooks:
        - id: isort

    - repo: https://github.com/pycqa/flake8
        rev: 6.0.0
        hooks:
        - id: flake8
   ```

3. Выполните следующую команду, чтобы установить pre-commit hooks:
   ```
   pre-commit install
   ```

4. Теперь каждый раз, когда вы фиксируете изменения, pre-commit hooks будут автоматически форматировать ваш код, сортировать импорты и проверять нарушения стиля.
---