[🏠 Головна](../README.MD) / [📘 Довідники](./README.MD)  / 

# 📘 Задача юристу `TaskToLavyer`


## Структура довідника

| Властивість </br> `Property` | Тип даних </br> `DataType` | Примітки |
| --- | --- | --- |
| `🔍` Найменувуання </br> `Title` | Стрічка </br> `String` |  |
| `🔍` Стан </br> `State` | `❓` 🎲 [Статус задачі юристу](../Enums/ETaskToLawyerStatus.md) </br> `ETaskToLawyerStatus❓` |  |
| Процес юриста </br> `LawyerProcess` | 📘 [Екземпляр процесу Workflow](../Entities/WorkflowInstance.md) </br> `WorkflowInstance` |  |
| `🔍` № задачі </br> `TaskNumber` | Ціле число </br> `Int64` |  |
| `🔍` Дата задачі </br> `TaskDate` | Дата / час </br> `DateTime` |  |
| `🔍` 👤 Автор задачі </br> `Usr_Initiator` | 📘 [Користувач](../Entities/User.md) </br> `User` |  |
| `🔍` 👤 Юрист </br> `Usr_Lawyer` | 📘 [Користувач](../Entities/User.md) </br> `User` |  |
| `🔍` Тип задачі юристу </br> `TypeOfTaskToLawyer` | `❓` 🎲 [Тип задачі юристу](../Enums/ETaskToLawyerType.md) </br> `ETaskToLawyerType❓` |  |
| Терміновість </br> `Urgency` | Стрічка </br> `String` |  |
| `🔍` ЦФВ </br> `CFR` | 📘 [ЦФВ (Центр Фінансової Відповідальності)](../Entities/CFR.md) </br> `CFR` |  |
| `🔍` Департамент </br> `Department` | 📘 [Департамент](../Entities/Department.md) </br> `Department` |  |
| `🔍` Контрагент </br> `Contractor` | 📘 [Контрагент](../Entities/Contractor.md) </br> `Contractor` |  |
| Установчі документи контрагента </br> `ContractorFoundationDocs` | 🗃 Колекція<📘 [Вкладення](../Entities/Attachment.md)> </br> `ICollection<Attachment>` |  |
| `🔍` Тип договору </br> `ContractType` | `❓` 🎲 [Тип договору](../Enums/EContractType.md) </br> `EContractType❓` | 🚧 |
| `🔍` Шаблон договору </br> `ContractTemplateType` | `❓` 🎲 [Тип шаблону договору](../Enums/EContractTemplateType.md) </br> `EContractTemplateType❓` | 🚧 |
| Пов'язаний зі специфікацією договір </br> `SpecificationRelatedContract` | 📕 [Договір](../Documents/D24032_Contract.md) </br> `D24032_Contract` | 🚧 |
| `🔍` Тип підстави </br> `BasementType` | `❓` 🎲 [Тип підстави договору](../Enums/EContractBasementType.md) </br> `EContractBasementType❓` | 🚧 |
| Підстава. Реєстр угоди </br> `Base_DealRegister` | 📕 [Реєстр угоди](../Documents/KD_DealRegister.md) </br> `KD_DealRegister` | 🚧 |
| Показники якості (д. договору по продажам) </br> `QualityIndicators` | Стрічка </br> `String` |  |
| Підстава. Заявка на ТМЦ </br> `Base_AppForTMC` | 📕 [Заявка на ТМЦ](../Documents/D24142a_AppForTMC.md) </br> `D24142a_AppForTMC` | 🚧 |
| Підстава. Тендер </br> `Base_Tender` | 📘 [Тендер](../Entities/Tender.md) </br> `Tender` | 🚧 |
| Підстава. Протокол ручного тендеру </br> `Base_TenderManual` | 📕 [Протокол ручного тендеру](../Documents/D24032_ManualTender.md) </br> `D24032_ManualTender` | 🚧 |
| Підстава. Службова записка по тривогам </br> `Base_ServiceNoteByAllerts` | 📕 [Службова записка по тривогам](../Documents/AppTMCv2Doc_UrgentByAlert.md) </br> `AppTMCv2Doc_UrgentByAlert` | 🚧 |
| `🔍` Предмет </br> `Subject` | Стрічка </br> `String` |  |
| `🔍` Ціна </br> `Price` | `❓` Дробне число </br> `Double❓` |  |
| `🔍` Валюта </br> `Currency` | `❓` 🎲 [Валюта](../Enums/ECurrency.md) </br> `ECurrency❓` | 🚧 |
| Умови оплати </br> `PaymentConditions` | Стрічка </br> `String` |  |
| Термін поставки </br> `DeliveryTime` | `❓` Дата / час </br> `DateTime❓` |  |
| `🔍` Місце поставки </br> `DeliveryPlace` | Стрічка </br> `String` |  |
| `🔍` Базис поставки </br> `DeliveryBasis` | `❓` 🎲 [Базис поставки](../Enums/EDeliveryBasis.md) </br> `EDeliveryBasis❓` | 🚧 |
| Примітки юристу </br> `RemarksForLawyer` | Стрічка </br> `String` |  |
| 🧰 НАШІ КОМПАНІЇ </br> `BL10_OurCompanies` | Блок </br> `🚧` |  |
|    Наша компанія </br> `BI_OurCompany` | 📘 [Наша компанія](../Entities/OurCompany.md) </br> `OurCompany` | 🚧 |
|    Кількість </br> `BI_Amount` | Дробне число </br> `Double` |  |
|    Сума </br> `BI_Sum` | Дробне число </br> `Double` |  |