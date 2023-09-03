### Hexlet tests and linter status:
[![Actions Status](https://github.com/BRODER1CK/python-project-50/workflows/hexlet-check/badge.svg)](https://github.com/BRODER1CK/python-project-50/actions)
[![CI check](https://github.com/BRODER1CK/python-project-50/actions/workflows/main.yml/badge.svg)](https://github.com/BRODER1CK/python-project-50/actions/workflows/main.yml)
[![Maintainability](https://api.codeclimate.com/v1/badges/83862856fcca110a5c65/maintainability)](https://codeclimate.com/github/BRODER1CK/python-project-50/maintainability)
[![Test Coverage](https://api.codeclimate.com/v1/badges/83862856fcca110a5c65/test_coverage)](https://codeclimate.com/github/BRODER1CK/python-project-50/test_coverage)

# DESCRIPTION:

**Вычислитель отличий**

Запускается из командной строки и вычисляет отличия между двумя файлами. На данный момент работает с JSON и YAML.

**Требования к установке**

Python 3.8 и выше.

**Инструкция по установке**

1. git clone https://github.com/BRODER1CK/python-project-50
2. cd python-project-50
3. make package-install

**Описание для разработчиков**

Для добавления dev-зависимости (зависимости для разработки): 
poetry add pytest --dev
Запустить тесты:
pytest
Для работы линтера нужно просто указать файл или директорию, которые нужно проверять, например:
# проверить один файл
$ flake8 file.py
# проверить директорию рекурсивно
$ flake8 src/
# проверить текущую директорию рекурсивно
$ flake8 .

**Описание работы**

Программа сравнивает два конфигурационных файла. Это значит, что cli-утилита моожет принимать через командную строку два аргумента — пути до этих файлов.

Результат сравнения файлов может выводиться в разных форматах, например: plain ("плоский") или json ("JSON-формат"). Cli-утилита может принимать через командную строку опцию --format, которая отвечает за выбор формата.

Полную справку можно получить по следующей команде:
gendiff -h

Запуск скрипта c настройками по-умолчанию, может использоваться для сравнения двух плоских файлов JSON или двух плоских файлов YAML(YML):
gendiff <file_path1> <file_path2>

Сравнение двух файлов c рекурсивной структурой: YAML(YML) или JSON:
gendiff --format json <file_path1> <file_path2>

Плоский формат отображения - cравнение двух файлов c рекурсивной структурой YAML(YML) или JSON:
gendiff --format plain <file_path1> <file_path2>
