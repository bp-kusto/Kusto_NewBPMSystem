[🏠 Головна](../../../README.MD) / [⚙️ Бізнес-процеси](../../README.MD) 

# `24` ⚙️ Реестр сделки ([📥 автодокументація](./AutoDoc/))

Процес призначений для створення і погодження документу реєстру угоди, що пізніше буде використовуватись як підстава до договору продажам.

## Діаграма процесу
![Діаграма процесу](./Images/map.png)

## Форма Z10T10
Після запуску процесу, його ініціатору відображається форма призначена для наповнення реєстру `[Z10T10] Наполнение реестра`:  

![Форма Z10T10](./Images/Forms/Z10T10.png)

### Опис полів форми Z10T10

Опис колонки **На формі**:
- `🚫      ` — Приховано
- `  👁️    ` — Тільки для перегляду
- `     ✏️ ` — Для заповнення
- `     ✏️❗` — Для заповнення, **обов'язково**

| На формі | Назва на формі </br> `Змінна` | Тип даних </br> `Тип в коді` | Скрипт | Примітки |
| --- | --- | --- | --- | --- |
| `  👁️    ` | № реестра </br> `RegNumber` | Ціле </br> `Int64` |  | Генерується автоматично після запуску процесу у форматі 2405_0001 (рік, місяць, порядковий №) | |
| `  👁️    ` | Дата реестра </br> `Дата реестра` | Дата / время </br> `DateTime` |  | Присвоюється після запуску процесу |
| `  👁️    ` | Документ реестра </br> `RegDocument` | 📕 Реєстр угоди </br> `KD_DealRegister` |  |  |
| `  👁️    ` | Инициатор реестра </br> `ProcUsrZ10_RegInitiator` | 📘 Пользователь </br> `🔴 User` |  |  |
| `     ✏️❗` | Контрагент </br> `RegContractor` | 📘 Контрагент </br> `🔴 Contractor` |  |  |
| `     ✏️❗` | Форма оплаты </br> `PaymentForm` | Строка </br> `String` |  |  |
| `     ✏️❗` | Толеранс </br> `Tolerans` | Строка </br> `String` |  |  |
| `     ✏️❗` | Качество (файл)</br> `Quality` | 📘 Вложение </br> `Attachment` |  |  |
| `     ✏️❗` | Пункт / склад отгрузки </br> `PointOfShipping` | Строка </br> `String` |  |  |
| `     ✏️❗` | Пункт назначения </br> `PointOfDestination` | Строка </br> `String` |  |  |
| `     ✏️❗` | Способ доставки </br> `DeliveryMethod` | 📘 Способ доставки </br> `🔴 OBJ` |  |  |
| `     ✏️❗` | Период поставки от ... </br> `DeliveryDateFrom` | Дата / время </br> `DateTime` |  |  |
| `     ✏️❗` | Период поставки до ... </br> `DeliveryDateTill` | Дата / время </br> `DateTime` |  |  |
| `     ✏️❗` | Базис поставки </br> `BasisOfDelivery` | 🎲 Базис поставки  </br> `🔴 EDeliveryBasis` |  |  |
| `     ✏️ ` | Примечания </br> `Rem` | Строка </br> `String` |  | Багатострічковий текст |
| `     ✏️ ` | Вложения (к примечаниям) </br> `RemAttachments` | 🗃📘 Вложение </br> `ICollection<Attachment>` |  | Багатострічковий текст |
| `     ✏️❗` | Культура </br> `Culture` | 📘 С/Х культура  </br> `🔴 OBJ` |  |  |
| `     ✏️❗` | Количество [тоннa] </br> `Amount__tonne` | Дробное число❓  </br> `Double❓` | `🔧` Z10T10_OnPrCh____Amount__tonne</br>(Context context, FormViewBuilder form) |  |
| `     ✏️❗` | Валюта сделки (CUR) </br> `DealCUR` | 🎲 Тип валюты❓  </br> `🔴 ECurrencyType❓` | `🔧` Z10T10_OnPrCh____DealCurrency</br>(Context context, FormViewBuilder form) |  |
| `     ✏️❗` | Курс CUR к UAH </br> `CURtoUAH` | Дробное число❓  </br> `Double❓` | `🔧` Z10T10_OnPrCh____CURtoUAH</br>(Context context, FormViewBuilder form) |  |
| `     ✏️❗` | Курс USD к UAH </br> `USDtoUAH` | Дробное число❓  </br> `Double❓` | `🔧` Z10T10_OnPrCh____USDtoUAH</br>(Context context, FormViewBuilder form) |  |
| `     ✏️❗` | НДС [%] </br> `VAT__percents` | Дробное число❓  </br> `Double❓` | `🔧` 	Z10T10_OnPrCh____VAT__percents</br>(Context context, FormViewBuilder form) |  |
| `  👁️    ` | * CUR_Selected </br> `CUR_Selected` | Строка </br> `String` |  |  |
| `  👁️    ` | * CUR_UAH </br> `CUR_UAH` | Строка </br> `String` |  |  |
| `     ✏️❗` | Цена реализации за 1т [CUR] </br> `SellingPricePer1ton__CUR` | Дробное число❓  </br> `Double❓` | `🔧` Z10T10_OnPrCh____SellingPricePer1ton__CUR</br>(Context context, FormViewBuilder form) |  |
| `     ✏️ ` | Цена реализации за 1т [UAH] </br> `SellingPricePer1ton__UAH` | Дробное число❓  </br> `Double❓` | `🔧` Z10T10_OnPrCh____SellingPricePer1ton__UAH</br>(Context context, FormViewBuilder form) |  |
| `     ✏️❗` | Себестоимость EXW на элеваторе на 1т [CUR] </br> `CostOfEXWatTheElevator__CUR` | Дробное число❓  </br> `Double❓` | `🔧` Z10T10_OnPrCh____CostOfEXWatTheElevator__CUR</br>(Context context, FormViewBuilder form) |  |
| `     ✏️ ` | Себестоимость EXW на элеваторе на 1т [UAH] </br> `CostOfEXWatTheElevator__UAH` | Дробное число❓  </br> `Double❓` | `🔧` Z10T10_OnPrCh____CostOfEXWatTheElevator__UAH</br>(Context context, FormViewBuilder form) |  |
| `     ✏️❗` | Расчетная стоимость логистики на 1т [CUR] </br> `EstimatedCostOfLogistics__CUR` | Дробное число❓  </br> `Double❓` | `🔧` Z10T10_OnPrCh____EstimatedCostOfLogistics__CUR</br>(Context context, FormViewBuilder form) |  |
| `     ✏️ ` | Расчетная стоимость логистики на 1т [UAH] </br> `EstimatedCostOfLogistics__UAH` | Дробное число❓  </br> `Double❓` | `🔧` Z10T10_OnPrCh____EstimatedCostOfLogistics__UAH</br>(Context context, FormViewBuilder form) |  |


#### Поведінка при зміні полів форми Z10T10