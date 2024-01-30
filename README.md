# CatScan - Приложение для Благотворительного фонда поддержки котиков

CatScan - это веб-приложение, разработанное для Благотворительного фонда поддержки котиков. Фонд собирает пожертвования на различные целевые проекты, связанные с поддержкой кошачьей популяции. В этом README.md файле вы найдете информацию о функциональности приложения, его основных возможностях и ролях пользователей.

## Описание проекта

### Фонд CatScan выполняет следующие основные задачи:

* **Создание целевых проектов**: Администраторы сайта могут создавать целевые 
проекты, каждый из которых имеет название, описание и сумму, которую 
планируется собрать. Проекты могут быть связаны с медицинским 
обслуживанием кошек, обустройством кошачьих колоний, закупкой корма 
для бездомных кошек и другими целями, связанными с поддержкой кошачьей 
популяции.


* **Сбор пожертвований**: Зарегистрированные пользователи могут сделать 
пожертвования в фонд. Пожертвования не привязаны к конкретному проекту и 
автоматически добавляются в первый открытый проект, который ещё не набрал 
необходимую сумму. Если пожертвование превышает требуемую сумму проекта или 
нет открытых проектов, оставшиеся средства ожидают создания следующего проекта
и автоматически вложатся в него при его создании.


* **Управление проектами**: Пожертвования в проекты распределяются по принципу
"First In, First Out". Как только проект набирает необходимую сумму, он 
закрывается, и новые пожертвования начинают идти в следующий открытый проект.
Это обеспечивает равномерное распределение средств между проектами.


* **Просмотр информации о проектах**: Любой пользователь, включая 
незарегистрированных, может просматривать список всех проектов,
включая информацию о требуемых и уже внесенных суммах. Это позволяет всем 
заинтересованным лицам следить за состоянием проектов и уровнем сбора средств.


* **Учет пожертвований**: Зарегистрированные пользователи могут видеть список
своих собственных пожертвований, что обеспечивает прозрачность их взносов.

## Роли пользователей
* **Администраторы сайта**: Эти пользователи могут создавать и управлять 
целевыми проектами, а также вести общий учет собранных средств.


* **Зарегистрированные пользователи**: Эти пользователи могут совершать 
пожертвования в фонд, просматривать список своих пожертвований и следить за 
состоянием проектов.


* **Незарегистрированные пользователи**: Эти пользователи могут просматривать 
информацию о проектах, но не могут совершать пожертвования.


# Стек
* FastAPI
* FastAPI-Users
* GoogleCloudPlatform
* SQLite
* Uvicorn
* GIT
* Postman

## Запуск проекта

* Клонировать репозиторий
```bash
git clone git@github.com:normalisht/CatScan.git
```

* Создать и активировать виртуальную среду, установить зависимости
#### Версия python = 3.9

```bash
python -m venv venv
if [ -e "venv/bin/activate" ]; then
    source venv/bin/activate
else
    source venv/Scripts/activate
fi
pip install -r requirements.txt
```

* Выполнить миграции
```bash
alembic upgrade head
```

* Запустить FastAPi
```bash
uvicorn app.main:app
```

Открыть документацию проекта
```http request
GET http://127.0.0.1:8000/docs
```
