[🏠 Головна](../README.MD) / [📘 Довідники](./README.MD)  / 

# 📘 Задача юристу `TaskToLavyer`


## Структура довідника

| Пошук | Властивість </br> `Property` | Тип даних </br> `Data type` | Примітки |
| :---: | --- | --- | --- |
|| Уникальный идентификатор </br> `Uid` | GUID </br> `Guid` ||
|| Найменувуання </br> `Title` | Стрічка </br> `String` ||
|| Стан </br> `State` | 🎲 [Статус задачі юристу](../Enums/ETaskToLawyerStatus.md) </br> `ETaskToLawyerStatus` ||
|| Процес юриста </br> `LawyerProcess` | 📘 [Екземпляр процесу Workflow](../Entities/WorkflowInstance.md) </br> `WorkflowInstance` ||
|| № задачі </br> `TaskNumber` | Ціле число </br> `Int64` ||
|| Дата задачі </br> `TaskDate` | Дата / час </br> `DateTime` ||
|| 👤 Автор задачі </br> `Usr_Initiator` | 📘 [Користувач](../Entities/User.md) </br> `User` ||
|| 👤 Юрист </br> `Usr_Lawyer` | 📘 [Користувач](../Entities/User.md) </br> `User` ||
|| Тип задачі юристу </br> `TypeOfTaskToLawyer` | 🎲 [Тип задачі юристу](../Enums/ETaskToLawyerType.md) </br> `ETaskToLawyerType` ||
|| Терміновість </br> `Urgency` | Стрічка </br> `String` ||
|| ЦФВ </br> `CFR` | 📘 [ЦФВ (Центр Фінансової Відповідальності)](../Entities/CFR.md) </br> `CFR` ||
|| Департамент </br> `Department` | 📘 [Департамент](../Entities/Department.md) </br> `Department` ||
|| Контрагент </br> `Contractor` | 📘 [Контрагент](../Entities/Contractor.md) </br> `Contractor` ||
|| Установчі документи контрагента </br> `ContractorFoundationDocs` | Список<Вложение (Объект)> (N-N) </br> `🚧` ||
|| Тип договору </br> `ContractType` | 🎲 Тип договору (Перечисление) </br> `🚧` ||
|| Шаблон договору </br> `ContractTemplateType` | 🎲 Тип шаблону договору (Перечисление) </br> `🚧` ||
|| Пов'язаний зі специфікацією договір </br> `SpecificationRelatedContract` | 📜 Договір (Документ) </br> `🚧` ||
|| Тип підстави </br> `BasementType` | 🎲 Тип підстави договору (Перечисление) </br> `🚧` ||
|| Підстава. Реєстр угоди </br> `Base_DealRegister` | 📜 Реєстр угоди (Документ) </br> `🚧` ||
|| Показники якості (д. договору по продажам) </br> `QualityIndicators` | Стрічка </br> `String` ||
|| Підстава. Заявка на ТМЦ </br> `Base_AppForTMC` | 📘 Заявка на ТМЦ (Объект) </br> `🚧` ||
|| Підстава. Тендер </br> `Base_Tender` | 📘 Тендер (Объект) </br> `🚧` ||
|| Підстава. Протокол ручного тендеру </br> `Base_TenderManual` | 📜 Протокол ручного тендеру (Документ) </br> `🚧` ||
|| Підстава. Службова записка по тривогам </br> `Base_ServiceNoteByAllerts` | 📜 Службова записка по тривогам (Документ) </br> `🚧` ||
|| Предмет </br> `Subject` | Стрічка </br> `String` ||
|| Ціна </br> `Price` | Дробне число </br> `Double` ||
|| Валюта </br> `Currency` | 🎲 Валюта (Перечисление) </br> `🚧` ||
|| Умови оплати </br> `PaymentConditions` | Стрічка </br> `String` ||
|| Термін поставки </br> `DeliveryTime` | Дата / час </br> `DateTime` ||
|| Місце поставки </br> `DeliveryPlace` | Стрічка </br> `String` ||
|| Базис поставки </br> `DeliveryBasis` | 🎲 Базис поставки (Перечисление) </br> `🚧` ||
|| Примітки юристу </br> `RemarksForLawyer` | Стрічка </br> `String` ||
|| 🧰 НАШІ КОМПАНІЇ </br> `BL10_OurCompanies` | Блок </br> `🚧` ||
||    Наша компанія </br> `BI_OurCompany` | 📘 Наша компанія (Объект) </br> `🚧` ||
||    Кількість </br> `BI_Amount` | Дробне число </br> `Double` ||
||    Сума </br> `BI_Sum` | Дробне число </br> `Double` ||