[🏠 Головна](../../../README.MD) / [⚙️ Бізнес-процеси](../../README.MD) / `16` ⚙️ Задача юристу

# `Процес #16` ⚙️ Задача юристу

Це приблизний опис процесу, виключно для його розуміння

## Короткий опис процесу

Процесс призначено для надання юристу інформації про договір, що необхідно запустити на погодження, замісь того щоб повідомляти юристу відповідну інформацію по телефону, email, месенджером, тощо.
Ініціатор цього процесу заповнює форму з ключовою інформацією про договір та відправляє на подальше опрацювання, після цього дані ініціатора копіюються в спеціальний об'єкт [`📘 Задача юристу`](../../../Entities/TaskToLawyer.md) запускається процес погодження договору в який під час запуску передається об'єкт в нього копіюється надана ініціатором інформація, батьківський процес заваршує своє виконання

## Діаграма процесу

**Діаграма процесу**  
![Діаграма процесу](./Pictures/ProcDiagram.png)

## Контекст процесу


|🛠️| Властивість </br> `Property` | Тип даних </br> `DataType` | Примітки |
|---|---|---|---|
|| Назва процесу </br> `ProcName` | Стрічка </br> `String` |  |
|| Статус процесу </br> `ProcStatus` | 🎲 [Статус задачі юристу](../../../Enums/ETaskToLawyerStatus.md) </br> `ETaskToLawyerStatus` |  |
|| Об'єкт процесу </br> `ProcObject` | 📘 [Задача юристу](../../../Entities/TaskToLawyer.md) </br> `TaskToLawyer` |  |
|| 👤 Ініціатор процесу </br> `Z10Usr_Initiator` | 📘 [Користувач](../../../Entities/User.md) </br> `User` |  |
|| № процесу </br> `ProcNumber` | Ціле число </br> `Int64` |  |
|| Дата процесу </br> `ProcDate` | Дата / час </br> `DateTime` |  |
|| 👤 Юрист </br> `Usr_Lawyer` | 📘 [Користувач](../../../Entities/User.md) </br> `User` |  |
|| Тип задачі юристу </br> `TaskToLawyerType` | 🎲 [Тип задачі юристу](../../../Enums/ETaskToLawyerType.md) </br> `ETaskToLawyerType` |  |
|| Контрагент </br> `Contractor` | 📘 [Контрагент](../../../Entities/Contractor.md) </br> `Contractor` |  |
|| Установчі документи контрагента </br> `ContractorFoundationDocs` | 🗃 Колекція<📘 [Вкладення](../../../Entities/Attachment.md)> </br> `ICollection<Attachment>` |  |
|| Предмет </br> `Subject` | Стрічка </br> `String` |  |
|| Валюта </br> `Currency` | 🎲 [Валюта](../../../Enums/ECurrency.md) </br> `ECurrency` |  |
|🚧| Тип і підстава договору </br> `ContractKindAndBasement` | 📘 [Тип і підстава договору](../../../Entities/ContractKindAndBasement.md) </br> `ContractKindAndBasement` |  |
|| Пов'язаний зі специфікацією договір </br> `SpecificationRelatedContract` | 📕 [Договір](../../../Documents/D24032_Contract.md) </br> `D24032_Contract` |  |
|| 🔗 Паспорт угоди </br> `Base_DealRegister` | 📕 [Реєстр угоди](../../../Documents/KD_DealRegister.md) </br> `KD_DealRegister` |  |
|| 🔗 Заявка на ТМЦ </br> `Base_AppForTMC` | 📘 [Заявка на ТМЦ](../../../Entities/Request.md) </br> `Request` |  |
|| 🔗 Тендер </br> `Base_Tender` | 📘 [Тендер](../../../Entities/Tender.md) </br> `Tender` |  |
|| 🔗 Протокол ручного тендеру </br> `Base_TenderManual` | 📕 [Протокол ручного тендеру](../../../Documents/D24032_ManualTender.md) </br> `D24032_ManualTender` |  |
|| 🔗 Службова записка по тривогам </br> `Base_ServiceNoteByAllerts` | 📕 [Службова записка по тривогам](../../../Documents/AppTMCv2Doc_UrgentByAlert.md) </br> `AppTMCv2Doc_UrgentByAlert` |  |
|🚧| 🔗 Службова записка </br> `Base_ServiceNote` | 📕 [Службова записка](../../../Documents/ServiceNote.md) </br> `ServiceNote` |  |
|| ░ 🧰 НАШІ КОМПАНІЇ </br> `BL10_OurCompanies` | Блок </br> `TablePart` |  |
|| ░  ├ Наша компанія </br> `BI_OurCompany` | 📘 [Наша компанія](../../../Entities/OurCompany.md) </br> `OurCompany` |  |
|| ░  └ Ціна </br> `BI_Price` | Дробне число </br> `Double` |  |
|| ЦФВ </br> `CFR` | 📘 [ЦФВ (Центр Фінансової Відповідальності)](../../../Entities/CFR.md) </br> `CFR` |  |
|| Департамент </br> `Department` | 📘 [Департамент](../../../Entities/Department.md) </br> `Department` |  |
|| Умови оплати </br> `PaymentConditions` | Стрічка </br> `String` |  |
|| Термін поставки </br> `DeliveryTime` | Дата / час </br> `DateTime` |  |
|| Місце поставки </br> `DeliveryPlace` | Стрічка </br> `String` |  |
|| Базис поставки </br> `DeliveryBasis` | 🎲 [Базис поставки](../../../Enums/EDeliveryBasis.md) </br> `EDeliveryBasis` |  |
|| Примітки юристу </br> `RemarksForLawyer` | Стрічка </br> `String` |  |

# Задачі процесу
## Z10T10 - Підготовка даних

![Z10T10 - Підготовка даних](./Pictures/Forms/Z10T10__PrepareData.png)

### Дані на формі

Опис колонки **На формі**:
- `🚫      ` — Приховано
- `  👁️    ` — Тільки для перегляду
- `     ✏️ ` — Для заповнення
- `     ✏️❗` — Для заповнення, **обов'язково**

|На формі|🛠️| Властивість </br> `Property` | Тип даних </br> `DataType` | Примітки |
|---|---|---|---|---|
|`  👁️    `|| Об'єкт процесу </br> `ProcObject` | 📘 [Задача юристу](../../../Entities/TaskToLawyer.md) </br> `TaskToLawyer` |  |
|`  👁️    `|| 👤 Ініціатор процесу </br> `Z10Usr_Initiator` | 📘 [Користувач](../../../Entities/User.md) </br> `User` |  |
|`  👁️    `|| № процесу </br> `ProcNumber` | Ціле число </br> `Int64` |  |
|`  👁️    `|| Дата процесу </br> `ProcDate` | Дата / час </br> `DateTime` |  |
|`     ✏️❗`|| Предмет </br> `Subject` | Стрічка </br> `String` |  |
|`     ✏️❗`|| Валюта </br> `Currency` | 🎲 [Валюта](../../../Enums/ECurrency.md) </br> `ECurrency` |  |
|`     ✏️❗`|| 👤 Юрист </br> `Usr_Lawyer` | 📘 [Користувач](../../../Entities/User.md) </br> `User` |  |
|`     ✏️❗`|| Тип задачі юристу </br> `TaskToLawyerType` | 🎲 [Тип задачі юристу](../../../Enums/ETaskToLawyerType.md) </br> `ETaskToLawyerType` |  |
|`     ✏️❗`|| Пов'язаний зі специфікацією договір </br> `SpecificationRelatedContract` | 📕 [Договір](../../../Documents/D24032_Contract.md) </br> `D24032_Contract` |  |
|`     ✏️❗`|🚧| Тип і підстава договору </br> `ContractKindAndBasement` | 📘 [Тип і підстава договору](../../../Entities/ContractKindAndBasement.md) </br> `ContractKindAndBasement` |  |
|`     ✏️❗`|| 🔗 Паспорт угоди </br> `Base_DealRegister` | 📕 [Реєстр угоди](../../../Documents/KD_DealRegister.md) </br> `KD_DealRegister` |  |
|`     ✏️❗`|| 🔗 Заявка на ТМЦ </br> `Base_AppForTMC` | 📘 [Заявка на ТМЦ](../../../Entities/Request.md) </br> `Request` |  |
|`     ✏️❗`|| 🔗 Тендер </br> `Base_Tender` | 📘 [Тендер](../../../Entities/Tender.md) </br> `Tender` |  |
|`     ✏️❗`|| 🔗 Протокол ручного тендеру </br> `Base_TenderManual` | 📕 [Протокол ручного тендеру](../../../Documents/D24032_ManualTender.md) </br> `D24032_ManualTender` |  |
|`     ✏️❗`|| 🔗 Службова записка по тривогам </br> `Base_ServiceNoteByAllerts` | 📕 [Службова записка по тривогам](../../../Documents/AppTMCv2Doc_UrgentByAlert.md) </br> `AppTMCv2Doc_UrgentByAlert` |  |
|`     ✏️❗`|🚧| 🔗 Службова записка </br> `Base_ServiceNote` | 📕 [Службова записка](../../../Documents/ServiceNote.md) </br> `ServiceNote` |  |
|`     ✏️❗`|| Контрагент </br> `Contractor` | 📘 [Контрагент](../../../Entities/Contractor.md) </br> `Contractor` |  |
|`     ✏️❗`|| Установчі документи контрагента </br> `ContractorFoundationDocs` | 🗃 Колекція<📘 [Вкладення](../../../Entities/Attachment.md)> </br> `ICollection<Attachment>` |  |
|`     ✏️❗`|| ░ 🧰 НАШІ КОМПАНІЇ </br> `BL10_OurCompanies` | Блок </br> `TablePart` |  |
|`     ✏️❗`|| ░  ├ Наша компанія </br> `BI_OurCompany` | 📘 [Наша компанія](../../../Entities/OurCompany.md) </br> `OurCompany` |  |
|`     ✏️❗`|| ░  └ Ціна </br> `BI_Price` | Дробне число </br> `Double` |  |
|`     ✏️❗`|| ЦФВ </br> `CFR` | 📘 [ЦФВ (Центр Фінансової Відповідальності)](../../../Entities/CFR.md) </br> `CFR` |  |
|`     ✏️❗`|| Департамент </br> `Department` | 📘 [Департамент](../../../Entities/Department.md) </br> `Department` |  |
|`     ✏️❗`|| Умови оплати </br> `PaymentConditions` | Стрічка </br> `String` |  |
|`     ✏️❗`|| Термін поставки </br> `DeliveryTime` | Дата / час </br> `DateTime` |  |
|`     ✏️❗`|| Місце поставки </br> `DeliveryPlace` | Стрічка </br> `String` |  |
|`     ✏️ `|| Базис поставки </br> `DeliveryBasis` | 🎲 [Базис поставки](../../../Enums/EDeliveryBasis.md) </br> `EDeliveryBasis` |  |
|`     ✏️ `|| Примітки юристу </br> `RemarksForLawyer` | Стрічка </br> `String` |  |