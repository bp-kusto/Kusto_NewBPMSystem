﻿[🏠 Головна](../README.MD) / [📘 Довідники](./README.MD) / 📘 ЦФВ (Центр Фінансової Відповідальності) `CFR`

# 📘 ЦФВ (Центр Фінансової Відповідальності) `CFR` </br> `🏷️ Базові`

## Структура довідника

|🛠️| Властивість </br> `Property` | Тип даних </br> `DataType` | Примітки |
|---|---|---|---|
|| Актуальність </br> `Actuality` | [🎲 Актуальність](../Enums/EActuality.md) </br> `EActuality` | За замовчуванням `✔️ Актуально` |
|| Найменування </br> `Title` | Стрічка </br> `🔧` `String` | Відображувана назва. Складається із значка актуальності (якщо заблоковано), внутрішнього коду та назви  |
|| Назва </br> `Name` | Стрічка </br> `String` |  |
|| Керівник по замовчуванню </br> `ChiefByDefault` | [📘 Посада](./UserPosition.md) </br> `Position` |  |
|| 📦 КЕРІВНИКИ ПО ДЕПАРТАМЕНТАМ </br> `BL_ChiefsByDepartments` | 📦 Керівник по департаменту </br> `CFR_ChiefByDepartment` |  |
|| Примітки </br> `Rem` | Стрічка </br> `String` |  |

### 📦 Керівник по департаменту </br> `CFR_ChiefByDepartment`
#### Структура блоку

|🛠️| Властивість </br> `Property` | Тип даних </br> `DataType` | Примітки |
|---|---|---|---|
|| Департамент </br> `Department` | [📘 Департамент](./Department.md) </br> `Department` | |
|| Керівник </br> `Chief` | [📘 Посада](./UserPosition.md) </br> `Position` |  |
|| Примітки </br> `Rem` | Стрічка </br> `String` |  |

## Наповнення довідника
| Актуальність | Найменування | Назва | Керівник по замовчуванню | 📦 КЕРІВНИКИ ПО ДЕПАРТАМЕНТАМ | Примітки |
|---|---|---|---|---|---|
| `✔️` | `🔧` | IT| Керівник IT департаменту| `Ent_01`|  |
| `✔️` | `🔧` |Автологістика| Директор відділу логістики| `Ent_02`|  |
| `✔️` | `🔧` | АГД (Адміністративно Господарська Діяльність) | Керівник господарського відділу |`Ent_03`|  |
| `✔️` | `🔧` | Агрономія | Керівник управління агрономічних процесів |`Ent_04`|  |
| `✔️` | `🔧` | Бджільництво | Керівник Липненського кластеру |`Ent_05`|  |
| `✔️` | `🔧` | Безпека | Директор департаменту безпеки |`Ent_06`|  |
| `✔️` | `🔧` | Бізнес аналітика | Начальник відділу бізнес-аналітикии |`Ent_07`|  |
| `✔️` | `🔧` | Бухгалтерія | Головний бухгалтер холдингу |`Ent_08`|  |
| `✔️` | `🔧` | Виробництво ел | Керівник виробничого відділу |`Ent_09`|  |
| `✔️` | `🔧` | Виробництво с/г | Керівник сервісного відділу |`Ent_10`|  |
| `✔️` | `🔧` | Диспетчеризація | Директор відділу диспетчеризації |`Ent_11`|  |
| `✔️` | `🔧` | Закупки | Начальник управління закупівель |`Ent_12`|  |
| `✔️` | `🔧` | Зв'язки з громадскістю та GR | Керівник відділу зв'язків з громадкістю і GR |`Ent_13`|  |
| `✔️` | `🔧` | З-д логістика | Директор відділу логістики |`Ent_14`|  |
| `✔️` | `🔧` | Земельний банк | Керівник департаменту ТПМР |`Ent_15`|  |
| `✔️` | `🔧` | Інженерія ел | Керівник технічного відділу |`Ent_16`|  |
| `✔️` | `🔧` | Інженерія с/х | Керівник сервісного відділу |`Ent_17`|  |
| `✔️` | `🔧` | Інженерія техн. ел | Керівник сервісного відділу |`Ent_18`|  |
| `✔️` | `🔧` | Комунікації та PR | Керівник відділу комунікації і PR |`Ent_19`|  |
| `✔️` | `🔧` | Кредити | Керівник кредитного відділу |`Ent_20`|  |
| `✔️` | `🔧` | Лабораторія | Керівник відділу лабораторії |`Ent_21`|  |
| `✔️` | `🔧` | Моніторинг технологій | Керівник управління ТПМР |`Ent_22`|  |
| `✔️` | `🔧` | Навчання та розвиток | Заступник ген. директора з навчання та розвитку |`Ent_23`|  |
| `✔️` | `🔧` | Охорона праці | Керівник відділу охорони праці <агровиробничого департаменту> |`Ent_24`|  |
| `✔️` | `🔧` | Персонал | Керівник департаменту управління персоналом |`Ent_25`|  |
| `✔️` | `🔧` | Продажі | Керівник відділу продаж |`Ent_26`|  |
| `✔️` | `🔧` | Складська логістика | Керівник відділу складської логістики |`Ent_27`|  |
| `✔️` | `🔧` | Технології та процессинг | Керівник департаменту ТПМР |`Ent_28`|  |
| `✔️` | `🔧` | Точне землеробство | Керівник відділу точного землеробства |`Ent_29`|  |
| `✔️` | `🔧` | Транспорт | Керівник відділу автотранспорту |`Ent_30`|  |
| `✔️` | `🔧` | Фінанси | Керівник управління фінансового контролю |`Ent_31`|  |
| `✔️` | `🔧` | Футбол | Керівник футбольного клубу |`Ent_32`|  |
| `✔️` | `🔧` | Харчування | Керівник відділу охорони праці <департаменту доробки і зберігання зерна> |`Ent_33`|  |
| `✔️` | `🔧` | Юристи | Керівник юридичного департаменту |`Ent_34`|  |

## Наповнення блоку `📦 КЕРІВНИКИ ПО ДЕПАРТАМЕНТАМ`
| `ParentId` | Департамент | Керівник | Примітки |
| ---: | --- | --- | --- |
| `Ent_01` |  IT департамент |  | IT |
| `Ent_02` | Комерційний департамент | | Автологістика |
| `Ent_03` | Адміністративний департамент |  | АГД (Адміністративно Господарська Діяльність) |
| `Ent_04` | Агровиробничий департамент |  | Агрономія |
| `Ent_05` | Агровиробничий департамент |  | Бджільництво |
| `Ent_06` | Департамент безпеки |  | Безпека |
| `Ent_07` | Фінансовий департамент |  | Бізнес аналітика |
| `Ent_08` | Фінансовий департамент |  | Бухгалтерія |
| `Ent_09` | Департамент доробки і зберігання зерна |  | Виробництво ел |
| `Ent_10` | Агровиробничий департамент |  | Виробництво с/г |
| `Ent_11` | Департамент ТПМР (технологій, процесів та моніторингу ресурсів) |  | Диспетчеризація |
| `Ent_12` | Комерційний департамент |  | Закупки |
| `Ent_13` | Адміністративний департамент |  | Зв'язки з громадскістю та GR |
| `Ent_14` | Комерційний департамент |  | З-д логістика |
| `Ent_15` | Департамент ТПМР (технологій, процесів та моніторингу ресурсів) |  | Земельний банк |
| `Ent_16` | Департамент доробки і зберігання зерна |  | Інженерія ел |
| `Ent_17` | Агровиробничий департамент |  | Інженерія с/х |
| `Ent_18` | Департамент доробки і зберігання зерна |  | Інженерія техн. ел |
| `Ent_19` | Адміністративний департамент |  | Комунікації та PR |
| `Ent_20` | Фінансовий департамент |  | Кредити |
| `Ent_21` | Департамент доробки і зберігання зерна |  | Лабораторія |
| `Ent_22` | Департамент ТПМР (технологій, процесів та моніторингу ресурсів) |  | Моніторинг технологій |
| `Ent_23` | Навчання та розвиток |  | Навчання та розвиток |
| `Ent_24` | Агровиробничий департамент |  | Охорона праці |
| `Ent_24` | Департамент доробки і зберігання зерна | Іванов Іван | Охорона праці |
| `Ent_25` | Адміністративний департамент |  | Персонал |
| `Ent_26` | Комерційний департамент |  | Продажі |
| `Ent_27` | Комерційний департамент |  | Складська логістика |
| `Ent_28` | Департамент ТПМР (технологій, процесів та моніторингу ресурсів) |  | Технології та процессинг |
| `Ent_29` | Департамент ТПМР (технологій, процесів та моніторингу ресурсів) |  | Точне землеробство |
| `Ent_30` | Адміністративний департамент |  | Транспорт |
| `Ent_31` | Фінансовий департамент |  | Фінанси |
| `Ent_32` | Адміністративний департамент |  | Футбол |
| `Ent_33` | Адміністративний департамент |  | Харчування |
| `Ent_34` | Юридичний департамент |  | Юристи |