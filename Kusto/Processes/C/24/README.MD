[🏠 Головна](../../../README.MD) / [⚙️ Бізнес-процеси](../../README.MD) 

# `24` ⚙️ Реестр сделки

## Матеріали для скачування

- [📥 Автодокументація по процесу](./ForDownload/AutoDoc/)
- [📥 Шаблон для генерації документу процесу](./ForDownload/DocTemplate/)
- [📥 Шаблон для генерації HTML відображення даних процесу](./ForDownload/HtmlFormTemplate/)

## Короткий опис процесу

Процес призначений для створення і погодження документу `Реєстр угоди`, що пізніше буде використовуватись як підстава до договору продажам.

---

В процесі, після його запуску, використовується форма наповнення (для ініціатора процесу) в якій він задає всю необхідну інформацію, а далі форма узгодження на якій учасники погодження можуть переглянути задану ініціатором інформацію у вигляді HTML-розмітки або ж у вигляді документа.
Таким чином в процесі використовується (відносно складна) форма наповнення реєстру, HTML-відображення даних реєстру, електронний документ реєстру з друкованою формою, що генерується під час перебігу процесу.

## Діаграма процесу
![Діаграма процесу](./Images/map.png)

## Форма `[Z10T10] Наполнение реестра`
Після запуску процесу, його ініціатору відображається форма призначена для наповнення реєстру `[Z10T10] Наполнение реестра`.

### Форма `[Z10T10] Наполнение реестра` / Вкладка `Головна сторінка`

![Форма Z10T10 • Головна сторінка](./Images/Forms/Z10T10_main.png)

### Форма `[Z10T10] Наполнение реестра` / Вкладка `HTML`

![Форма Z10T10 • HTML](./Images/Forms/Z10T10_html.png)

**Вхідні переходи**:  
- `Z10T10_B10` — Процес прямує до одноіменного скрипту (див. діаграму процесу), де відбувається регенерація документу процесу, та HTML-форми для наглядного відображення даних процесу.

**При завантаженні форми виконується сценарій**:  
- `Z10T10_OnFormLoad(Context context, FormViewBuilder form)` - в якому відбуваєтсья переналаштування видимості, обов'язковості до заповнення та обрахунок полів, що входять до складу цієї форми.

**Вихідні переходи**:  
- `ОК` - При натисканні кнопки `На согласование` — Відображується спливаюча форма `Z10T10_A10__OK` з відображенням подальших учасників процесу (діалогове вікно по відношенню до основної форми). Після натискання кнопки `Сохранить` на цій формі, вона зникає, перевіряється заповнення всіх обов'язкових полей та процес переходить до наступного свого кроку (див. діаграму процесу)
- `Save` — При натисканні кнопки `Сохранить` — Процес переходить до наступного свого кроку (див. діаграму процесу), де відбувається регенерація документу процесу, та HTML-форми для наглядного відображення даних процесу. Перевірка обов'язковості заповнення даних не відбувається.
- `Abort`  — При натисканні кнопки `Прервать процесс` —  Відображується повідомлення чи користувач дійсно бажає перервати процес, після позитивної відповіді - процес прямує шляхом свого завершення. Перевірка обов'язковості заповнення даних не відбувається.
- `Автоматична ескалація` - По завершенню відведеного часу - процес прямує шляхом свого завершення (тобто аналогічно попередньому переходу тільки по сплинанню певного часу).



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
| `     ✏️❗` | Налоги на 1т [CUR] </br> `TaxPer1t__CUR` | Дробное число❓  </br> `Double❓` | `🔧` Z10T10_OnPrCh____TaxPer1t__CUR</br>(Context context, FormViewBuilder form) |  |
| `     ✏️ ` | Налоги на 1т [UAH] </br> `TaxPer1t__UAH` | Дробное число❓  </br> `Double❓` | `🔧` Z10T10_OnPrCh____TaxPer1t__UAH</br>(Context context, FormViewBuilder form) |  |
| `     ✏️❗` | Перевалка на 1т [CUR] </br> `TransshipmentPer1t__CUR` | Дробное число❓  </br> `Double❓` | `🔧` Z10T10_OnPrCh____TransshipmentPer1t__CUR</br>(Context context, FormViewBuilder form) |  |
| `     ✏️ ` | Перевалка на 1т [UAH] </br> `TransshipmentPer1t__UAH` | Дробное число❓  </br> `Double❓` | `🔧` Z10T10_OnPrCh____TransshipmentPer1t__UAH</br>(Context context, FormViewBuilder form) |  |
| `     ✏️❗` | Услуги элеватора (сбыт) на 1т [CUR] </br> `ElevatorServicesPer1t__CUR` | Дробное число❓  </br> `Double❓` | `🔧` Z10T10_OnPrCh____ElevatorServicesPer1t__CUR</br>(Context context, FormViewBuilder form) |  |
| `     ✏️ ` | Услуги элеватора (сбыт) на 1т [UAH] </br> `ElevatorServicesPer1t__UAH` | Дробное число❓  </br> `Double❓` | `🔧` Z10T10_OnPrCh____ElevatorServicesPer1t__UAH</br>(Context context, FormViewBuilder form) |  |
| `     ✏️❗` | Сопутствующие расходы на 1т [CUR] </br> `AssociatedExpensesPer1t__CUR` | Дробное число❓  </br> `Double❓` | `🔧` Z10T10_OnPrCh____AssociatedExpensesPer1t__CUR</br>(Context context, FormViewBuilder form)	 |  |
| `     ✏️ ` | Сопутствующие расходы на 1т [UAH] </br> `AssociatedExpensesPer1t__UAH` | Дробное число❓  </br> `Double❓` | `🔧` Z10T10_OnPrCh____AssociatedExpensesPer1t__UAH</br>(Context context, FormViewBuilder form) |  |
| `  👁️    ` | Маржа на 1т [CUR] </br> `MarginPer1t__CUR` | Дробное число❓  </br> `Double❓` |  |  |
| `  👁️    ` | Маржа на 1т [UAH] </br> `MarginPer1t__UAH` | Дробное число❓  </br> `Double❓` |  |  |
| `     ✏️ ` | Постоянные расходы на 1т [CUR] </br> `ConstantCostsPer1t__CUR` | Дробное число❓  </br> `Double❓` | Z10T10_OnPrCh____ConstantCostsPer1t__CUR</br>(Context context, FormViewBuilder form) |  |
| `     ✏️ ` | Постоянные расходы на 1т [UAH] </br> `ConstantCostsPer1t__UAH` | Дробное число❓  </br> `Double❓` | Z10T10_OnPrCh____ConstantCostsPer1t__UAH</br>(Context context, FormViewBuilder form) |  |
| `  👁️    ` | Полная себестоимость на 1т. [CUR] </br> `FullCostsPer1t__CUR` | Дробное число❓  </br> `Double❓` |  |  |
| `  👁️    ` | Полная себестоимость на 1т. [UAH] </br> `FullCostsPer1t__UAH` | Дробное число❓  </br> `Double❓` |  |  |
| `  👁️    ` | Расчетная чистая прибыль на 1т [CUR] </br> `EstimatedNetProfitPer1t__CUR` | Дробное число❓  </br> `Double❓` |  |  |
| `  👁️    ` | Расчетная чистая прибыль на 1т [UAH] </br> `EstimatedNetProfitPer1t__UAH` | Дробное число❓  </br> `Double❓` |  |  |
| `  👁️    ` | Расчетная чистая прибыль по сделке [UAH] </br> `EstimatedNetProfit__UAH` | Дробное число❓  </br> `Double❓` |  |  |
| `  👁️    ` | Расчетная чистая прибыль по сделке [USD] </br> `EstimatedNetProfit__USD` | Дробное число❓  </br> `Double❓` |  |  |
| `  👁️    ` | Total CUR </br> `LabelOfTotalCUR` | Строка </br> `String` |  |  |
| `  👁️    ` | DocAsHtml </br> `DocAsHtml` | HTML разметка  </br> `HtmlString` |  | Відображається на окремій вкладці задачі користувача |


#### Поведінка при зміні полів форми Z10T10


## Форма `[Z10T10_A10__OK] На согласование`

![Z10T10_A10__OK • На согласование](./Images/Forms/Z10T10_A10__OK.png)