﻿[🏠 Головна](../README.MD)  
[📘 Довідники](./README.MD)  

# 📘 Користувач `User`
**Системний користувач**. Структура довідника приблизна, в кожній системі вона буде дещо різною.

## Структура довідника
| Властивість | Тип даних | Примітки |
|---|---|---|
| Найменування </br> `Title` | Стрічка </br> 🔧 `String` | Відображувана назва. Складається із значка актуальності (якщо заблоковано) прізвища та імені  |
| Актуальність </br> `Actuality` | [🎲 Актуальність](../Enums/EActuality.md) </br> `EActuality` | За замовчуванням `✔️ Актуально` |
| Прізвище </br> `LastName` | Стрічка </br> `String` |  |
| Ім'я </br> `Name` | Стрічка </br> `String` |  |
| По-батькові </br> `MiddleName` | Стрічка </br> `String` |  |
| Email </br> `Email` | Стрічка </br> `String` |  |