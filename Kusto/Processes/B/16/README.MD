[🏠 Головна](../../../README.MD) / [⚙️ Бізнес-процеси](../../README.MD) / `16` ⚙️ Задача юристу `🏷️ в розробці`

# Передмова

## Використані типи даних

| Використаний тип </br> `UsedType` | Мітки | Примітки |
| --- | --- | --- |
| [📘 Задача юристу](../../../Entities/TaskToLavyer.md) </br> `TaskToLavyer` | | |
| --- | --- | --- |
| [📕 Документ](../../../Documents/KD_DealRegister.md) </br> `TDoc` | | |
| [📘 Сутність](../../../Entities/TEntity.md) </br> `TUser` | | |
| [🎲 Перелік](../../../Enums/CurrencyType.md) </br> `TEnum` | | |

## Матеріали для скачування
*Відсутні**

---

# `Процес #16` ⚙️ Задача юристу `🏷️ в розробці`

## Короткий опис процесу

Процесс призначено для надання юристу інформації про договір, що необхідно запустити на погодження, замісь того щоб повідомляти юристу відповідну інформацію по телефону, email, месенджером, тощо.
Ініціатор цього процесу заповнює форму з ключовою інформацією про договір та відправляє на подальше опрацювання, після цього дані ініціатора копіюються в спеціальний об'єкт [`📘 Задача юристу`](../../../Entities/TaskToLavyer.md) запускається процес погодження договору в який під час запуску передається об'єкт в нього копіюється надана ініціатором інформація, батьківський процес заваршує своє виконання

## Діаграма процесу

**Діаграма процесу**  
![Діаграма процесу](./Pictures/ProcDiagram.png)

## Контекст процесу


|🛠️| Властивість </br> `Property` | Тип даних </br> `DataType` | Примітки |
|---|---|---|---|
|| Назва процесу </br> `ProcName` | Стрічка </br> `String` |  |
|| Статус процесу </br> `ProcStatus` | 🎲 [Статус задачі юристу](../../../Enums/ETaskToLawyerStatus.md) </br> `ETaskToLawyerStatus` |  |
|| № процесу </br> `ProcNumber` | Ціле число </br> `Int64` |  |
|| Дата процесу </br> `ProcDate` | Дата / час </br> `DateTime` |  |
|| 👤 Ініціатор процесу </br> `Z10Usr_Initiator` | 📘 [Користувач](../../../Entities/User.md) </br> `User` |  |
|| 👤 Юрист </br> `Usr_Lawyer` | 📘 [Користувач](../../../Entities/User.md) </br> `User` |  |
|| Тип задачі юристу </br> `TaskToLawyerType` | 🎲 [Тип задачі юристу](../../../Enums/ETaskToLawyerType.md) </br> `ETaskToLawyerType` |  |
|⛔| Терміновість </br> `Urgency` | Стрічка </br> `String` |  |
|| ЦФВ </br> `CFR` | 📘 [ЦФВ (Центр Фінансової Відповідальності)](../../../Entities/CFR.md) </br> `CFR` |  |
|| Департамент </br> `Department` | 📘 [Департамент](../../../Entities/Department.md) </br> `Department` |  |
|| Контрагент </br> `Contractor` | 📘 [Контрагент](../../../Entities/Contractor.md) </br> `Contractor` |  |
|| Установчі документи контрагента </br> `ContractorFoundationDocs` | 🗃 Колекція<📘 [Вкладення](../../../Entities/Attachment.md)> </br> `ICollection<Attachment>` |  |
|| Тип договору </br> `ContractType` | 🎲 [Тип договору](../../../Enums/EContractType.md) </br> `EContractType` |  |
|| Шаблон договору </br> `ContractTemplateType` | 🎲 [Тип шаблону договору](../../../Enums/EContractTemplateType.md) </br> `EContractTemplateType` |  |
|| Пов'язаний зі специфікацією договір </br> `SpecificationRelatedContract` | 📕 [Договір](../../../Documents/D24032_Contract.md) </br> `D24032_Contract` |  |
|| Тип підстави </br> `BasementType` | 🎲 [Тип підстави договору](../../../Enums/EContractBasementType.md) </br> `EContractBasementType` |  |
|| Підстава. Реєстр угоди </br> `Base_DealRegister` | 📕 [Реєстр угоди](../../../Documents/KD_DealRegister.md) </br> `KD_DealRegister` |  |
|⛔| Показники якості (д. договору по продажам) </br> `QualityIndicators` | Стрічка </br> `String` ||
|| Підстава. Заявка на ТМЦ </br> `Base_AppForTMC` | 📘 [Заявка на ТМЦ](../../../Entities/Request.md) </br> `Request` |  |
|| Підстава. Тендер </br> `Base_Tender` | 📘 [Тендер](../../../Entities/Tender.md) </br> `Tender` |  |
|| Підстава. Протокол ручного тендеру </br> `Base_TenderManual` | 📕 [Протокол ручного тендеру](../../../Documents/D24032_ManualTender.md) </br> `D24032_ManualTender` |  |
|| Підстава. Службова записка по тривогам </br> `Base_ServiceNoteByAllerts` | 📕 [Службова записка по тривогам](../../../Documents/AppTMCv2Doc_UrgentByAlert.md) </br> `AppTMCv2Doc_UrgentByAlert` |  |
|| Предмет </br> `Subject` | Стрічка </br> `String` |  |
|| Ціна </br> `Price` | Дробне число </br> `Double` |  |
|| Валюта </br> `Currency` | 🎲 [Валюта](../../../Enums/ECurrency.md) </br> `ECurrency` |  |
|| Умови оплати </br> `PaymentConditions` | Стрічка </br> `String` |  |
|| Термін поставки </br> `DeliveryTime` | Дата / час </br> `DateTime` |  |
|| Місце поставки </br> `DeliveryPlace` | Стрічка </br> `String` |  |
|| Базис поставки </br> `DeliveryBasis` | 🎲 [Базис поставки](../../../Enums/EDeliveryBasis.md) </br> `EDeliveryBasis` |  |
|| Примітки юристу </br> `RemarksForLawyer` | Стрічка </br> `String` |  |
|| Об'єкт процесу </br> `ProcObject` | 📘 [Задача юристу](../../../Entities/TaskToLawyer.md) </br> `TaskToLawyer` |  |
|🚧| 🧰 НАШІ КОМПАНІЇ </br> `BL10_OurCompanies` | 🚧 </br> `🚧` |  |
||    Наша компанія </br> `BI_OurCompany` | 📘 [Наша компанія](../../../Entities/OurCompany.md) </br> `OurCompany` |  |
||    Кількість </br> `BI_Amount` | Дробне число </br> `Double` |  |
||    Сума </br> `BI_Sum` | Дробне число </br> `Double` |  |

# Задачі процесу
## Z10T10 - Підготовка даних

![Z10T10 - Підготовка даних](./Pictures/Forms/Z10T10__PrepareData.png)

### Дані на формі

Опис колонки **На формі**:
- `🚫      ` — Приховано
- `  👁️    ` — Тільки для перегляду
- `     ✏️ ` — Для заповнення
- `     ✏️❗` — Для заповнення, **обов'язково**

|🛠️|На формі| Властивість </br> `Property` | Тип даних </br> `DataType` | Примітки |
|---|---|---|---|---|
||`  👁️    `| Об'єкт процесу </br> `ProcObject` | 📘 [Задача юристу](../../../Entities/TaskToLawyer.md) </br> `TaskToLawyer` |  |
||| ◤ ІДЕНТИФІКАЦІЯ |---|Блок на формі|
||`  👁️    `| 👤 Ініціатор процесу </br> `Z10Usr_Initiator` | 📘 [Користувач](../../../Entities/User.md) </br> `User` |  |
||`  👁️    `| № процесу </br> `ProcNumber` | Ціле число </br> `Int64` |  |
||`  👁️    `| Дата процесу </br> `ProcDate` | Дата / час </br> `DateTime` |  |
||| ◤ ЗАДАЧА ЮРИСТУ |---|Блок на формі|
||`     ✏️❗`| 👤 Юрист </br> `Usr_Lawyer` | 📘 [Користувач](../../../Entities/User.md) </br> `User` |  |
||`     ✏️❗`| Тип задачі юристу </br> `TaskToLawyerType` | 🎲 [Тип задачі юристу](../../../Enums/ETaskToLawyerType.md) </br> `ETaskToLawyerType` |  |
||| ◤ КОНТРАГЕНТ та ПРЕДМЕТ |---|Блок на формі|
||`     ✏️❗`| Контрагент </br> `Contractor` | 📘 [Контрагент](../../../Entities/Contractor.md) </br> `Contractor` |  |
||`     ✏️❗`| Установчі документи контрагента </br> `ContractorFoundationDocs` | 🗃 Колекція<📘 [Вкладення](../../../Entities/Attachment.md)> </br> `ICollection<Attachment>` |  |
||`     ✏️❗`| Предмет </br> `Subject` | Стрічка </br> `String` |  |
|❓⛔|`     ✏️❗`| Ціна </br> `Price` | Дробне число </br> `Double` | ❓ Перенести в блок `🧰 10 НАШІ КОМПАНІЇ` |
||`     ✏️❗`| Валюта </br> `Currency` | 🎲 [Валюта](../../../Enums/ECurrency.md) </br> `ECurrency` |  |
||| ◤ ПАРАМЕТРИ |---|Блок на формі|
||`     ✏️❗`| Тип договору </br> `ContractType` | 🎲 [Тип договору](../../../Enums/EContractType.md) </br> `EContractType` |  |
|⛔|`     ✏️❗`| Шаблон договору </br> `ContractTemplateType` | 🎲 [Тип шаблону договору](../../../Enums/EContractTemplateType.md) </br> `EContractTemplateType` | Не відображати на формі ініціатора |
||`     ✏️❗`| Пов'язаний зі специфікацією договір </br> `SpecificationRelatedContract` | 📕 [Договір](../../../Documents/D24032_Contract.md) </br> `D24032_Contract` |  |
||`     ✏️❗`| Тип підстави </br> `BasementType` | 🎲 [Тип підстави договору](../../../Enums/EContractBasementType.md) </br> `EContractBasementType` |  |
||`     ✏️❗`| Підстава. Реєстр угоди </br> `Base_DealRegister` | 📕 [Реєстр угоди](../../../Documents/KD_DealRegister.md) </br> `KD_DealRegister` |  |
||`     ✏️❗`| Підстава. Заявка на ТМЦ </br> `Base_AppForTMC` | 📘 [Заявка на ТМЦ](../../../Entities/Request.md) </br> `Request` |  |
||`     ✏️❗`| Підстава. Тендер </br> `Base_Tender` | 📘 [Тендер](../../../Entities/Tender.md) </br> `Tender` |  |
||`     ✏️❗`| Підстава. Протокол ручного тендеру </br> `Base_TenderManual` | 📕 [Протокол ручного тендеру](../../../Documents/D24032_ManualTender.md) </br> `D24032_ManualTender` |  |
||`     ✏️❗`| Підстава. Службова записка по тривогам </br> `Base_ServiceNoteByAllerts` | 📕 [Службова записка по тривогам](../../../Documents/AppTMCv2Doc_UrgentByAlert.md) </br> `AppTMCv2Doc_UrgentByAlert` |  |
||| ◤ НАШІ КОМПАНІЇ |---|Блок на формі|
|🚧|`     ✏️❗`| `🧰 10` НАШІ КОМПАНІЇ </br> `BL10_OurCompanies` | 🚧 </br> `🚧` |  |
||`     ✏️❗`| `🧰 10 🧩` Наша компанія </br> `BI_OurCompany` | 📘 [Наша компанія](../../../Entities/OurCompany.md) </br> `OurCompany` |  |
|❓|`     ✏️❗`| `🧰 10 🧩` Ціна </br> `BI_Price` | Дробне число </br> `Double` |  |
||`     ✏️❗`| ЦФВ </br> `CFR` | 📘 [ЦФВ (Центр Фінансової Відповідальності)](../../../Entities/CFR.md) </br> `CFR` |  |
||`     ✏️❗`| Департамент </br> `Department` | 📘 [Департамент](../../../Entities/Department.md) </br> `Department` |  |
||| ◤ ПОСТАВКА |---|Блок на формі|
||`     ✏️❗`| Умови оплати </br> `PaymentConditions` | Стрічка </br> `String` |  |
||`     ✏️❗`| Термін поставки </br> `DeliveryTime` | Дата / час </br> `DateTime` |  |
||`     ✏️❗`| Місце поставки </br> `DeliveryPlace` | Стрічка </br> `String` |  |
||`     ✏️❗`| Базис поставки </br> `DeliveryBasis` | 🎲 [Базис поставки](../../../Enums/EDeliveryBasis.md) </br> `EDeliveryBasis` |  |
||| ◤ ДОДАТКОВІ ПРИМІТКИ |---|Блок на формі|
||`     ✏️ `| Примітки юристу </br> `RemarksForLawyer` | Стрічка </br> `String` |  |