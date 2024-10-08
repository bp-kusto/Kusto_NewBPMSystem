﻿[🏠 Головна](../README.MD) / [📘 Довідники](./README.MD) / 📘 Департамент `Department`

# 📘 Департамент `Department` </br> `🏷️ Базові`

## Структура довідника

|🛠️| Властивість </br> `Property` | Тип даних </br> `DataType` | Примітки |
|---|---|---|---|
|| Актуальність </br> `Actuality` | [🎲 Актуальність](../Enums/EActuality.md) </br> `EActuality` | За замовчуванням `✔️ Актуально` |
|| Найменування </br> `Title` | Стрічка </br> `🔧` `String` | Відображувана назва. Складається із значка актуальності (якщо заблоковано), внутрішнього коду та назви  |
|| Назва </br> `Name` | Стрічка </br> `String` |  |
|| Керівник </br> `Chief` | [📘 Посада](./UserPosition.md) </br> `Position` |  |
|| Примітки </br> `Rem` | Стрічка </br> `String` |  |

## Наповнення довідника
| Актуальність | Найменування | Назва | Керівник | Примітки |
| --- | --- | --- | --- | --- |
| `✔️` | `🔧` | IT департамент | Керівник IT департаменту (ПІБ користувача) |  |
| `✔️` | `🔧` | Агровиробничий департамент | Керівник агровиробничого департаменту (ПІБ користувача) |  |
| `✔️` | `🔧` | Адміністративний департамент | Керівник адміністративного департаменту (ПІБ користувача) |  |
| `✔️` | `🔧` | Департамент безпеки | Директор департаменту безпеки (ПІБ користувача) |  |
| `✔️` | `🔧` | Департамент доробки і зберігання зерна | Керівник департаменту доробки і зберігання зерна (ПІБ користувача) |  |
| `✔️` | `🔧` | Департамент ТПМР (технологій, процесів та моніторингу ресурсів) | Керівник департаменту ТПМР (ПІБ користувача) |  |
| `✔️` | `🔧` | Комерційний департамент | Керівник комерційного департаменту (ПІБ користувача) |  |
| `✔️` | `🔧` | Фінансовий департамент | Керівник фінансового департаменту (ПІБ користувача) |  |
| `✔️` | `🔧` | Юридичний департамент | Керівник юридичного департаменту (ПІБ користувача) |  |