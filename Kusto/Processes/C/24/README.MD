[🏠 Головна](../../../README.MD) / [⚙️ Бізнес-процеси](../../README.MD) 

# `24` ⚙️ Реестр сделки ([📥 автодокументація](./AutoDoc/))

Процес призначений для створення і погодження документу реєстру угоди, що пізніше буде використовуватись як підстава до договору продажам.

**Діаграма процесу**  
![Діаграма процесу](./Images/map.png)

Після запуску процесу, його ініціатору відображається форма призначена для наповнення реєстру `[Z10T10] Наполнение реестра`:  

![Форма Z10T10)](./Images/Forms/Z10T10.png)

## **Опис полів форми:**

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
| `     ✏️❗` | Культура </br> `Culture` | 📘 С/Х культура  </br> `🔴 OBJ` |  |  |
| `     ✏️❗` | Количество [тоннa] </br> `Amount__tonne` | Дробное число❓  </br> `Double❓` | `🔧` Z10T10_OnPrCh____Amount__tonne(Context context, FormViewBuilder form) |  |
| `     ✏️❗` | Валюта сделки (CUR) </br> `DealCUR` | 🎲 Тип валюты❓  </br> `🔴 ECurrencyType❓` | `🔧` Z10T10_OnPrCh____DealCurrency(Context context, FormViewBuilder form) |  |
| `     ✏️❗` | Курс CUR к UAH </br> `CURtoUAH` | Дробное число❓  </br> `Double❓` | `🔧` Z10T10_OnPrCh____CURtoUAH(Context context, FormViewBuilder form) |  |
| `     ✏️❗` | Курс USD к UAH </br> `USDtoUAH` | Дробное число❓  </br> `Double❓` | `🔧` Z10T10_OnPrCh____USDtoUAH(Context context, FormViewBuilder form) |  |
| `     ✏️❗` | НДС [%] </br> `VAT__percents` | Дробное число❓  </br> `Double❓` | `🔧` 	Z10T10_OnPrCh____VAT__percents(Context context, FormViewBuilder form) |  |


### Поведінка при зміні полів форми