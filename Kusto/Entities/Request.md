[🏠 Головна](../README.MD) / [📘 Довідники](./README.MD) / 📘 Заявка на ТМЦ `Request`

# 📘 Заявка на ТМЦ `Request` </br> `🚧 UnderConstruction`


## Структура довідника

| Властивість </br> `Property` | Тип даних </br> `DataType` | Примітки |
| --- | --- | --- |
| `🔍` Наименование </br> `Name` | Стрічка </br> `String` |  |
| `🔍` Дата </br> `Date` | `❓` Дата / час </br> `DateTime❓` |  |
| `🔍` Номер </br> `Number` | `❓` Ціле число </br> `Int64❓` |  |
| `🔍` Инициатор </br> `Iniciator` | Стрічка </br> `String` |  |
| `🔍` Подразделение-заказчик </br> `Customer` | 📘 [⛔ Підрозділ](../Entities/PodrazdelenieZakazchik.md) </br> `PodrazdelenieZakazchik` |  |
| `🔍` Срок поставки </br> `DeliveryDate` | `❓` Дата / час </br> `DateTime❓` |  |
| Утвержденные контрагенты </br> `Contractors` | 🗃 Колекція<📘 [Контрагент](../Entities/Contractor.md)> </br> `ICollection<Contractor>` |  |
| Тендер </br> `Tender` | 📘 [Тендер](../Entities/Tender.md) </br> `Tender` |  |
| Документация </br> `Docs` | 📘 [Папка](../Entities/Folder.md) </br> `Folder` | `🚧 UnderConstruction` |
| Документ заявки </br> `BidDocument` | 📘 [Документ](../Entities/Document.md) </br> `Document` | `🚧 UnderConstruction` |