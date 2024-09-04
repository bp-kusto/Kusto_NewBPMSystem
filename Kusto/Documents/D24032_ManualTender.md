[🏠 Головна](../README.MD) / [📕 Документи](./README.MD) / 📕 Протокол ручного тендеру `D24032_ManualTender`

# 📕 Протокол ручного тендеру `D24032_ManualTender`

## Структура документу

| Властивість </br> `Property` | Тип даних </br> `DataType` | Примітки |
| --- | --- | --- |
| Ініціатор </br> `Initiator` | 📘 [Користувач](../Entities/User.md) </br> `User` |  |
| `🔍` Найменування </br> `DocTitle` | Стрічка </br> `String` |  |
| `🔍` № документа </br> `DocNumber` | Ціле число </br> `Int64` |  |
| `🔍` Дата документа </br> `DocDate` | Дата / час </br> `DateTime` |  |
| `🔍` Предмет тендеру </br> `TenderSubject` | Стрічка </br> `String` |  |
| `🔍` ЦФВ </br> `CFR` | 📘 [ЦФВ (Центр Фінансової Відповідальності)](../Entities/CFR.md) </br> `CFR` |  |
| `🔍` Департамент </br> `Department` | 📘 [Департамент](../Entities/Department.md) </br> `Department` |  |
| `🔍` Підстава ручного тендеру </br> `ManualTenderBase` | 🎲 [Підстава ручного тендеру](../Enums/EManualTenderBase.md) </br> `EManualTenderBase` | 🚧 |
| Пов'язані заявки на закупку ТМЦ </br> `RelatedAppsForTMC` | 🗃 Колекція<📘 [Заявка на ТМЦ](../Entities/Request.md)> </br> `ICollection<Request>` | 🚧 |
| Службова записка по тривогам </br> `ServiceNoteByAlerts` | 📕 [Службова записка по тривогам (базовий)](../Documents/AppTMCv2Doc_UrgentByAlert.md) </br> `AppTMCv2Doc_UrgentByAlert` | 🚧 |
| Примітки </br> `Remarks` | Стрічка </br> `String` |  |
| Вкладення </br> `AttachmentsWithFiles` | 🗃 Колекція<📘 [Вкладення](../Entities/Attachment.md)> </br> `ICollection<Attachment>` |  |
| Статус документу </br> `DocStatus` | 🎲 [Статус документу](../Enums/EDocStatus.md) </br> `EDocStatus` | 🚧 |
| Пов'язані компанії </br> `RelatedOurCompanies` | 🗃 Колекція<📘 [Наша компанія](../Entities/OurCompany.md)> </br> `ICollection<OurCompany>` |  |