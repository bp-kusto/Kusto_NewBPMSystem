﻿[🏠 Головна](../README.MD) / [📕 Документи](./README.MD)  

# 📕 Реєстр угоди `KD_DealRegister`

# Використані типи даних
- [📘 Вложение](../../../Entities/Attachment.md) `Attachment` ⚠️
- [📘 Контрагент](../Entities/Contractor.md) `Contractor` ⚠️
- [📘 С/Х культура](../Entities/KO_AgriCulture.md) `KO_AgriCulture` ⚠️
- [📘 Способ доставки](../Entities/KO_DeliveryMethod.md) `KO_DeliveryMethod` ⚠️
- [📘 Пользователь](../Entities/User.md) `User` ⚠️
- [🎲 Тип валюты](../Enums/CurrencyType.md) `CurrencyType` ⚠️
- [🎲 Базис поставки](../Enums/DeliveryBasis.md) `DeliveryBasis` ⚠️
- [🎲 Статус документу](../Enums/EDocStatus.md) `EDocStatus` ⚠️
- [🎲 Наличие НДС](../Enums/KE_PresenceOfVAT.md) `KE_PresenceOfVAT` ⚠️

## Структура документу

| Пошук | Властивість </br> `Property` | Тип даних </br> `Data type` | Примітки |
| --- | --- | --- | --- |
| ✔️ | Статус документа </br> `DocStatus` | 🎲 Статус документу </br> `🎲 EDocStatus` |  |
| ✔️ | № реестра </br> `RegNumber` | Целое число </br> `Int64` |  |
| ✔️ | Дата реестра </br> `RegDate` | Дата / время </br> `DateTime` |  |
| ✔️ | Инициатор реестра </br> `RegInitiator` | 📘 Пользователь </br> `📘 User` |  |
|  | Примечания </br> `Rem` | Строка </br> `String` |  |
|  | Вложения (к примечаниям) </br> `RemAttachments` | Список<📘 Вложение> </br> `List<📘 Attachment> `|  |
| ✔️ | Контрагент </br> `Contractor` | 📘 Контрагент </br> `📘 Contractor` |  |
| ✔️ | Культура </br> `Culture` | 📘 С/Х культура </br> `📘 KO_AgriCulture` |  |
| ✔️ | Количество [тоннa] </br> `Amount__tonne` | Дробное число❓ </br> `Double❓` |  |
|  | Форма оплаты </br> `PaymentForm` | Строка </br> `String` |  |
|  | Толеранс </br> `Tolerans` | Строка </br> `String` |  |
|  | Качество (файл) </br> `Quality` | 📘 Вложение </br> `📘 Attachment` |  |
|  | Пункт / склад отгрузки </br> `PointOfShipping` | Строка </br> `String` |  |
|  | Пункт назначения </br> `PointOfDestination` | Строка </br> `String` |  |
|  | Срок поставки </br> `DeliveryDate` | Дата / время❓ </br> `DateTime❓` |  |
|  | Способ доставки </br> `DeliveryMethod` | 📘 Способ доставки </br> `📘 KO_DeliveryMethod` |  |
| ✔️ | Период поставки с ... </br> `DeliveryDateFrom` | Дата / время❓ </br> `DateTime❓` |  |
| ✔️ | Период поставки по ... </br> `DeliveryDateTill` | Дата / время❓ </br> `DateTime❓` |  |
|  | Базис поставки </br> `BasisOfDelivery` | 🎲 Базис поставки❓ </br> `🎲 DeliveryBasis❓` |  |
|  | НДС [%] </br> `VAT__percents` | Дробное число❓ </br> `Double❓` |  |
|  | Себестоимость EXW на элеваторе за 1т </br> `CostOfEXWatTheElevator__inDealCurrency` | Дробное число❓ </br> `Double❓` |  |
|  | Валюта сделки (CUR) </br> `DealCUR` | 🎲 Тип валюты❓ </br> `🎲 CurrencyType` |  |
|  | Расчетная стоимость логистики за 1т </br> `EstimatedCostOfLogistics__inDealCurrency` | Дробное число❓ </br> `Double❓` |  |
|  | Цена реализации за 1т </br> `SellingPricePer1ton__inDealCurrency` | Дробное число❓ </br> `Double❓` |  |
|  | Курс CUR к UAH </br> `CURtoUAH` | Дробное число❓ </br> `Double❓` |  |
|  | Наличие НДС </br> `PresenceOfVAT` | 🎲 Наличие НДС❓ </br> `🎲 KE_PresenceOfVAT❓` |  |
|  | Курс USD к UAH </br> `USDtoUAH` | Дробное число❓ </br> `Double❓` |  |
|  | Расчетная чистая прибыль за 1т </br> `EstimatedNetProfit__inDealCurrency` | Дробное число❓ </br> `Double❓` |  |
|  | Цена реализации за 1т [CUR] </br> `SellingPricePer1ton__CUR` | Дробное число❓ </br> `Double❓` |  |
|  | Рассчетная чистая прибыль за 1т [USD] </br> `EstimatedNetProfit__inUSD` | Дробное число❓ </br> `Double❓` |  |
|  | Цена реализации за 1т [UAH] </br> `SellingPricePer1ton__UAH` | Дробное число❓ </br> `Double❓` |  |
|  | Себестоимость EXW на элеваторе на 1т [CUR] </br> `CostOfEXWatTheElevator__CUR` | Дробное число❓ </br> `Double❓` |  |
|  | Себестоимость EXW на элеваторе на 1т [UAH] </br> `CostOfEXWatTheElevator__UAH` | Дробное число❓ </br> `Double❓` |  |
|  | Расчетная стоимость логистики на 1т [CUR] </br> `EstimatedCostOfLogistics__CUR` | Дробное число❓ </br> `Double❓` |  |
|  | Расчетная стоимость логистики на 1т [UAH] </br> `EstimatedCostOfLogistics__UAH` | Дробное число❓ </br> `Double❓` |  |
|  | Налоги на 1т [CUR] </br> `TaxPer1t__CUR` | Дробное число❓ </br> `Double❓` |  |
|  | Налоги на 1т [UAH] </br> `TaxPer1t__UAH` | Дробное число❓ </br> `Double❓` |  |
|  | Перевалка на 1т [CUR] </br> `TransshipmentPer1t__CUR` | Дробное число❓ </br> `Double❓` |  |
|  | Перевалка на 1т [UAH] </br> `TransshipmentPer1t__UAH` | Дробное число❓ </br> `Double❓` |  |
|  | Услуги элеватора (сбыт) на 1т [CUR] </br> `ElevatorServicesPer1t__CUR` | Дробное число❓ </br> `Double❓` |  |
|  | Услуги элеватора (сбыт) на 1т [UAH] </br> `ElevatorServicesPer1t__UAH` | Дробное число❓ </br> `Double❓` |  |
|  | Сопутствующие расходы на 1т [CUR] </br> `AssociatedExpensesPer1t__CUR` | Дробное число❓ </br> `Double❓` |  |
|  | Сопутствующие расходы на 1т [UAH] </br> `AssociatedExpensesPer1t__UAH` | Дробное число❓ </br> `Double❓` |  |
|  | Маржа на 1т [CUR] </br> `MarginPer1t__CUR` | Дробное число❓ </br> `Double❓` |  |
|  | Маржа на 1т [UAH] </br> `MarginPer1t__UAH` | Дробное число❓ </br> `Double❓` |  |
|  | Постоянные расходы на 1т [CUR] </br> `ConstantCostsPer1t__CUR` | Дробное число❓ </br> `Double❓` |  |
|  | Постоянные расходы на 1т [UAH] </br> `ConstantCostsPer1t__UAH` | Дробное число❓ </br> `Double❓` |  |
|  | Полная себестоимость на 1т. [CUR] </br> `FullCostsPer1t__CUR` | Дробное число❓ </br> `Double❓` |  |
|  | Полная себестоимость на 1т. [UAH] </br> `FullCostsPer1t__UAH` | Дробное число❓ </br> `Double❓` |  |
|  | Расчетная чистая прибыль на 1т [CUR] </br> `EstimatedNetProfitPer1t__CUR` | Дробное число❓ </br> `Double❓` |  |
|  | Расчетная чистая прибыль на 1т [UAH] </br> `EstimatedNetProfitPer1t__UAH` | Дробное число❓ </br> `Double❓` |  |
|  | Расчетная чистая прибыль по сделке [CUR] </br> `EstimatedNetProfit__CUR` | Дробное число❓ </br> `Double❓` |  |
|  | Расчетная чистая прибыль по сделке [UAH] </br> `EstimatedNetProfit__UAH` | Дробное число❓ </br> `Double❓` |  |
|  | Расчетная чистая прибыль по сделке [USD] </br> `EstimatedNetProfit__USD` | Дробное число❓ </br> `Double❓` |  |
