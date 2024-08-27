[🏠 Головна](../README.MD) / [📘 Довідники](./README.MD)  

# 📘 Контрагент `Contractor`

⚠️ ***Опис не завершено***

## Структура довідника

| Пошук | Властивість </br> `Property` | Тип даних </br> `Data type` | Примітки |
| --- | --- | --- | --- |
| ✔️ | Організаційно-правова форма </br> `LegalForm` | [📘 Організаційно-правова форма](./LegalForm.md) </br> `LegalForm` |  |
| ✔️ | Коротка назва </br> `ShortName` | Стрічка </br> `String` |  |
| ✔️ | Офіційна назва </br> `OfficialName` | Стрічка </br> `String` |  |
| ✔️ | Країна реєстрації контрагента </br> `RegistrationCountry` | [🎲 Країна реєстрації контрагента](../Enums/EContractorRegistrationCountry.md) </br> `Type` |  |
| ✔️ | Реєстраційний код (ЄДРПО, ІНН, ...) </br> `RegCode` | Стрічка </br> `String` | Має бути унікальним для резидентів |
| ✔️ | Відповідальний </br> `ResponsibleUser` | [📘 Користувач](./User.md) </br> `User` |  |
| ✔️ | Спеціальний контрагент </br> `SpecialContractor` | [🎲 Спеціальний контрагент](../Enums/ESpecialContractor.md)❓ </br> `ESpecialContractor❓` |  |
|  | Цей контрагент дублює </br> `ThisContractorIsDuplicateOf` | [📘 Контрагент](./Contractor.md) </br> `Contractor` | Посилання на контрагента якого дублює цей. Не дозволяти посилання на себе |
|  | 📦 НОМЕНКЛАТУРА </br> `BL_Nmc` | 📦 Номенклатура </br> `Contractor__BL_Nmc` |  |
| ✔️ | Заключення СЕБ </br> `SES_Conclusion` | [🎲 Статус СЕБ](../Enums/EStatusOfSES.md) </br> `EStatusOfSES` |  |
|  | Процес "Перевірка СЕБ" </br> `WorkflowInstance_SES_Check` | [📘 Екземпляр робочого процесу](./WorkflowInstance.md) </br> `WorkflowInstance` | Посилання на процес перевірки СЕБ. Якщо процес в активному стані не дозволяти ще один екземпляр |
|  | Процес "Валідація контрагента" </br> `WorkflowInstance_Validation` | [📘 Екземпляр робочого процесу](./WorkflowInstance.md) </br> `WorkflowInstance` | Посилання на процес валідації контрагента. Якщо процес в активному стані не дозволяти ще один екземпляр |
| ⚠️ | Властивість </br> `Property` | [📘 Тип](./Type.md) </br> `Type` |  |
| ⚠️ | Властивість </br> `Property` | [🎲 Перелік](../Enums/EType.md) </br> `EType` |  |


### Структура блоку 📦 Номенклатура `Contractor__BL_Nmc`

| Властивість </br> `Property` | Тип даних </br> `Data type` | Примітки |
|---|---|---|
| Номенклатура </br> `Nmc` | [📘 Номенклатура](./Nomenclature.md) </br> `Nomenclature` | |