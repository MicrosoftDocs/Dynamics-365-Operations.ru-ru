---
title: Создание графиков выставления счетов
description: В этой статье объясняется, как создавать, удалять и изменять графики выставления счетов.
author: JodiChristiansen
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 1248799f92dc6cbce8528a53cc8a3012d2a67b3c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903402"
---
# <a name="create-billing-schedules"></a>Создание графиков выставления счетов

[!include [banner](../includes/banner.md)]

На странице **График выставления счетов** можно создавать, удалять или изменять графики выставления счетов. Также можно просмотреть список графиков выставления счетов. При создании графика выставления счетов значения по умолчанию для него определяются связанной с ним группой выставления счетов. Дополнительные сведения настраиваются на странице **Параметры повторяющегося выставления счетов по контракту**.

## <a name="create-a-billing-schedule"></a>Создание графика выставления счетов

Для создания графика выставления счетов выполните следующие действия.

1. На странице **График выставления счетов** выберите **Создать**.
2. В диалоговом окне **Создание графика выставления счетов** в поле **Группа графиков выставления счетов** выберите группу графиков выставления счетов.
3. Выберите счет клиента в поле **Счет клиента**.
4. В поле **Дата начала** выберите начальную дату, затем в поле **Число периодов** введите количество периодов. Поле **Дата окончания** обновляется в соответствии с числом введенных периодов. При обновлении поля **Дата окончания выставления счетов** поле **Число периодов** обновляется до значения **0** (ноль).
5. Нажмите **ОК**.
6. На странице **График выставления счетов** на вкладке **Общие** в поле **Описание** введите описание графика выставления счетов.
7. В поле **Шаблон этапа** выберите шаблон этапа для пункта **Выставление счетов по этапам**.

Такие поля, как **Счет для накладной** и **Код валюты**, обновляются информацией из клиента.

Поля **Частота выставления счетов** и **Интервал выставления счетов** устанавливаются автоматически на основе выбранной группы графиков выставления счетов.

8. Для создания отдельных накладных установите для параметра **Выставлять накладные отдельно** значение **Да**.
9. Чтобы автоматически обновлять график выставления счетов после окончательного периода выставления счетов, установите для параметра **Возобновлять автоматически** значение **Да**, затем установите поле **Строки, добавляемые при каждом возобновлении**.

Поля **Параметры** задаются автоматически на основе значений на странице **Параметры повторяющегося выставления счетов по контракту**.

10. Для пропорционального расчета суммы графика выставления счетов установите для параметра **Пропорционально для неполных периодов** значение **Да**.
11. Чтобы выровнять строки со сведениями о расписании выставления счетов с окончанием месяца, установите для параметра **Выровнять по месяцам** значение **Да**.
12. В полях **Дата начала контракта** и **Дата окончания контракта** введите начальную и конечную даты контракта. Эти даты предназначены только для информации.

В поле **Платеж** отображаются сведения о платежах клиента из клиента. Если номенклатура строки заблокирована или завершена, сведения об оплате не могут быть изменены.

> [!NOTE]
> При консолидации накладных по номенклатурам значения полей **Условия платежей**, **Метод** и **График выставления счетов** должны совпадать. В противном случае накладные не могут быть консолидированы.

13. На вкладке **Адрес** можно просмотреть и обновить поля **Адрес поставки** и **Адрес выставления счетов**.
14. На вкладке **Контактная информация** можно связать учетную запись конечного пользователя с графиком выставления счетов.
15. В полях **Контактная информация** можно ввести контакт, адрес электронной почты и адрес в Интернете.
16. Чтобы отследить информацию о комиссиях партнеров, задайте поля **Счет партнера** и **Ставка комиссии партнера**. Эти поля предназначены только для информации.
17. На вкладке **Итого** можно просмотреть различные итоговые суммы, рассчитанные для графика выставления счетов.
18. На вкладке **Блокировка** можно просмотреть сведения аудита о том, когда график выставления счетов был помещен в режим блокировки и когда блокировка была снята.
19. На вкладке **Завершение** можно просмотреть историю завершений, которые были применены к графику выставления счетов или удалены из него.
20. Нажмите **Сохранить**.
21. На экспресс-вкладке **Строки графика выставления счетов** выберите **Добавить строку**.
22. В поле **Код номенклатуры** выберите код номенклатуры. Если добавляемая номенклатура является родительской номенклатурой в разделении выручки, строки автоматически обновляются с учетом дочерних номенклатур. Редактировать можно только родительскую номенклатуру в разбиении выручки. Все дочерние номенклатуры соответственно обновляются.
23. В поле **Тип номенклатуры** выберите тип номенклатуры.
24. Обновите даты начала и окончания.
25. Перед созданием накладных можно изменить частоту выставления счетов, обновив поле **Частота выставления счетов**. Частота выставления счетов не может быть изменена после создания первой накладной для графика выставления счетов.
26. В поле **Единица** выберите единицу измерения для номенклатуры.
27. В поле **Метод ценообразования** выберите метод ценообразования для номенклатуры.

Поле **Цена за единицу** устанавливается автоматически из запасов. Однако его можно обновить, если изменить метод ценообразования на **Фиксированная**.

## <a name="remove-a-line-item"></a>Удаление номенклатуры строки

Чтобы удалить номенклатуру из графика выставления счетов, выполните следующие действия.

1. На странице **График выставления счетов** в поле **Номер графика** выберите номер графика выставления счетов, который требуется изменить.
2. На Экспресс-вкладке **Строки графика выставления счетов** выберите удаляемую строку и выберите **Удалить**.
3. Нажмите **Сохранить**.

В оставшейся части этой статьи описываются действия и подробные сведения, доступные для строк на экспресс-вкладке **Строки графика выставления счетов**.

## <a name="billing-schedule-line-actions"></a>Действия строки графика выставления счетов

Кнопки на экспресс-вкладке **Строки графика выставления счетов** позволяют применить действия к отдельным строкам.

| Кнопка | Описание |
|--------|-------------|
| Добавить строку | Добавление строки в график выставления счетов. |
| Добавить из списка номенклатур | Добавьте несколько номенклатур к графику выставления счетов, выбрав их в списке. |
| Удалить | <p>Удаление выбранной строки из графика выставления счетов.</p><p>Для номенклатур, которые являются частью разделения выручки, можно удалить только родительскую номенклатуру. Все связанные дочерние номенклатуры автоматически удаляются.</p> |
| Просмотр сведений о выставлении счетов | Просмотр сведений о выставлении счетов. |
| Увольнение | <p>Завершение выделенных строк. Эта кнопка доступна только в том случае, если выбранные строки имеют статус **Активно**.</p><p>Для номенклатур, которые являются частью разделения выручки, можно завершить только родительскую номенклатуру.</p> |
| Удалить завершение | <p>Удаление завершения из выбранных строк. Эта кнопка доступна только в том случае, если выбранные строки имеют статус **Завершено**.</p><p>Для номенклатур, которые являются частью разделения выручки, завершение можно удалить только из родительской номенклатуры.</p> |
| Заблокировать | <p>Выберите сведения для помещения выбранной строки на блокировку.</p><p>Для номенклатур, которые являются частью разделения выручки, на блокировку можно поместить только родительскую номенклатуру.</p> |
| Снять блокировку | <p>Снятие блокировки с выбранной строки.</p><p>Для номенклатур, которые являются частью разделения выручки, блокировку можно снять только из родительской номенклатуры.</p> |
| Эскалация и скидка | Эта кнопка недоступна для номенклатур, которые являются частью разбиения выручки, за исключением родительских номенклатур, для которых разбиение выручки использует метод распределения **Нулевая сумма**. |
| Отсрочки | <p>Введите параметров РБП для выбранной строки.</p><p>Эта кнопка недоступна для родительских номенклатур в разбиении выручки.</p> |
| Распределение этапа | <p>Просмотр и обновление сведений о распределении этапов для выбранной строки.</p><p>Эта кнопка доступна только в том случае, если номенклатура строки графика выставления счетов является номенклатурой этапа.</p> |
| Поддержка и возобновление | <p>Просмотр и обновление сведений о поддержке и возобновлении для выбранной строки.</p><p>Эта кнопка доступна только в том случае, если номенклатура строки графика выставления счетов является номенклатурой поддержки или возобновления.</p> |
| Отобразить аналитики | Отображение или скрытие столбцов аналитики, которые отображаются в сетке **Строки графика выставления счетов**. |
| Рассчитать цену за единицу | <p>Расчет цены за единицу для номенклатуры, чтобы клиент мог заплатить сумму контракта частями (например, ежедневно, ежемесячно, ежеквартально, раз в полгода или ежегодно). Можно выбрать цену контракта и ценовую частоту.</p><p>Можно просмотреть аудиторский след изменений: старую цену и частоту контракта, новую цену и частоту контракта, пользователя, который внес изменение, а также дату и время изменения.</p> |
| Дата сопоставления | <p>Указывается дата сопоставления для обновляемых номенклатур.</p><p>Если в поле **Группа номенклатур** выбрана группа номенклатур, все номенклатуры используют дату выравнивания первой номенклатуры в графике выставления счетов. Если поле **Группа номенклатур** пусто, можно указать дату выравнивания, которая будет использоваться для всех номенклатур.</p><p>Эта кнопка доступна только в том случае, когда в поле **Частота выставления счетов** установлено значение **Ежегодно**.</p> |
| Выручка по невыставленным счетам | <p>Задайте номенклатуру для использования функции выручки без выставления счетов. Затем можно указать счета невыставленных счетов выручки и невыставленных счетов скидок для номенклатуры.</p><p>Эта кнопка доступна только для номенклатур, для которых в поле **Тип номенклатуры** установлено значение **Стандартный**. Она недоступна для существующих графиков выставления счетов или для строк графика выставления счетов, когда накладная уже была создана.</p> |
| Добавить дочерний объект разделения выручки | <p>Выберите дочернюю номенклатуру для добавления в заказ на продажу.</p><p>Эта кнопка доступна только для родительских номенклатур в разбиении выручки.</p> |
| Параметры расширенного ценообразования | Измените параметры ценообразования для номенклатуры. |

## <a name="billing-schedule-line-details"></a>Сведения строки графика выставления счетов

При выборе строки на экспресс-вкладке **Строки графика выставления счетов** можно просмотреть подробные сведения по этой строке. Эти детали делятся между различными вкладками.

### <a name="general-tab"></a>Вкладка "Общие"

На вкладке **Общие** доступна следующая информация.

| Поле или раздел | Описание |
|------------------|-------------|
| Использование | <p>В этом разделе представлены сведения об использовании номенклатур. Он содержит следующие поля:</p><ul><li>**Идентификатор использования** — идентификатор измерительного прибора или номенклатуры использования.</li><li>**Параметр чтения** — параметр чтения использования: **Чтение** или **Потребление**.</li><li>**Оценка потребления** — укажите оценку потребления для номенклатуры использования с периодами, когда накладная не была создана. На странице **Сведения о выставлении счетов** можно просмотреть строки сведений о выставлении счетов для оценки потребления.</li></ul> |
| Внешние ссылки\* | В этом разделе содержатся поля **Внешний** и **Номер строки**, в которых можно указать информацию о внешних ссылках. |
| Этап | <p>В этом разделе представлены сведения о номенклатурах этапов. Он содержит поле **Предполагаемая дата завершения**, в которой отображается дата завершения номенклатуры.</li></ul> |
| Текст | Комментарий для строки. Текст переводится на язык по умолчанию клиента или юридического лица. |
| Группа номенклатур | Группа номенклатур для номенклатуры строки. |
| Дата сопоставления | Дата выравнивания для графика выставления счетов. |

\* При консолидации накладных по номенклатуре на странице **Создать накладную** поля **Внешние ссылки** должны совпадать. Если отличается хотя бы один символ, номенклатуры не будут консолидироваться по накладной. Проверка не выполняется ни в одном из полей в разделе **Внешние ссылки**, а значение в поле **Номер строки** должно быть положительным целым числом.

### <a name="address-tab"></a>Вкладка «Адрес»

На вкладке **Адрес** доступна следующая информация.

| Поле | Описание |
|-------|-------------|
| Адрес доставки | <p>Выберите адрес поставки для номенклатуры строки. Адрес доставки по умолчанию является основным адресом поставки с экспресс-вкладки **Адрес**.</p><p>При изменении адреса можно выбрать следующие параметры адреса:</p><ul><li>**Адреса** — выберите адрес для текущего клиента.</li><li>**Используется** — выберите адрес, который в настоящее время используется для текущего клиента.</li><li>**Другой адрес** — выберите адрес для любой записи клиента.</li></ul><p>Для номенклатур, использующих разбиение выручки, можно изменить только адрес родительской номенклатуры. Адрес для дочерних номенклатур совпадает с адресом родительской номенклатуры и не может быть изменен отдельно.</p> |
| Адрес плательщика | <p>Выберите адрес плательщика для номенклатуры строки. Адрес доставки по умолчанию является основным адресом поставки с экспресс-вкладки **Адрес**. Можно изменить адрес на нужный в соответствии с целью доступных адресов:</p><ul><li>Если ни один из адресов не имеет цели **Накладная**, адрес плательщика по умолчанию является основным адресом клиента, независимо от назначения.</li><li>Если один или несколько адресов имеют назначение **Накладная**, адресом по умолчанию является адрес, который был введен последним.</li><li>Если один или несколько адресов имеют назначение **Накладная**, а один из адресов накладной задан в качестве первичного адреса, адресом по умолчанию для выставления счетов является адрес с назначением **Накладная**, который устанавливается в качестве первичного адреса.</li><li>Для номенклатур, использующих разбиение выручки, можно изменить только адрес родительской номенклатуры. Адрес для дочерних номенклатур совпадает с адресом родительской номенклатуры и не может быть изменен отдельно.</li></ul> |

### <a name="product-tab"></a>Вкладка "Продукт"

На вкладке **Продукт** доступна следующая информация.

| Поле или раздел | Описание |
|------------------|-------------|
| Аналитики хранения | <p>В этом разделе отображаются сведения о хранении для номенклатуры. Он содержит поле **Серийный номер**, в котором отображается серийный номер номенклатуры.</p><p>Серийный номер копируется из исходного заказа на продажу в процессе поддержки и возобновления. Для номенклатур, использующих разбиение выручки, серийный номер родительской номенклатуры копируется во все дочерние номенклатуры. Серийный номер копируется, когда для параметра **Копировать серийный номер** задано значение **Да** на странице **Параметры повторяющегося выставления счетов по контракту**.</li></ul> |
| Аналитики продуктов | Сведения о продукте для номенклатуры и значения автоматически обновляются на основе значения **Номер варианта**, выбранного для строки графика выставления счетов. |

### <a name="account-tab"></a>Вкладка "Счет"

На вкладке **Счет** доступна следующая информация.

| Поле | Описание |
|-------|-------------|
| Счет ГК | Счет ГК, который создается в строке продаж. Значение по умолчанию берется из заказа на продажу. Это поле может быть пустым. |
| Финансовые аналитики номенклатуры | <p>Значения финансовой аналитики по умолчанию на основе записи клиента и номенклатуры.</p><p>Для номенклатур, использующих разбиение выручки, дочерние номенклатуры используют значения финансовой аналитики записей клиента и номенклатуры, как описано выше. Если необходимо обновить значения финансовой аналитики дочерних номенклатур, можно импортировать сущность данных.</p> |

### <a name="renewals-tab"></a>Вкладка «Возобновления»

На вкладке **Возобновления** доступна следующая информация.

| Поле | Описание |
|-------|-------------|
| Возобновить автоматически | <p>Значение, указывающее, будет ли строка графика выставления счетов автоматически возобновлена для следующего периода выставления счетов:</p><ul><li>**Да** — строка графика выставления счетов автоматически возобновляется для следующего периода выставления счетов, когда вы создаете накладную.</li><li>**Нет** — строка графика выставления счетов не возобновляется автоматически. Необходимо возобновить график выставления счетов вручную.</li></ul> |
| Строки для добавления по возобновлению | Число строк, добавляемых к возобновлению графика выставления счетов. |

Дополнительно на вкладке **Возобновления** доступны следующие кнопки.

| Кнопка | Описание |
|--------|-------------|
| Аудит записи невыставленной выручки в журнале | Просмотр всех изменений для номенклатур, использующих функцию выручки без выставленных счетов. |
| Добавить условие возобновления | Добавьте срок возобновления для номенклатуры. Дата начала нового срока возобновления — это следующая дата после даты окончания предыдущего срока. Поля **Дата окончания возобновления**, **Дата начала РБП**, **Дата окончания РБП**, **Количество номенклатуры** и **Цена за единицу** могут быть обновлены. |
| Изменить условие возобновления | <p>Изменение условия возобновления. Для начального условия можно изменить даты начала и окончания РБП перед созданием исходной записи журнала. Для последующих условий дата начала не может быть изменена. Она всегда будет следующей датой после окончания предыдущего условия.</p><p>Если после изменяемого условия существует условие возобновления, даты этого условия изменить нельзя. В этом случае можно обновить только поля **Количество** и **Цена за единицу** для возобновляемой номенклатуры.</p><p>Например, существует три условия. <ul><li>Первый срок не может быть изменен, поскольку он уже начался.</li><li>Для второго срока можно изменить только количество и цену за единицу.</li><li>Для третьего срока можно изменить все значения, кроме даты начала. Кроме того, параметр **График из шаблона** позволяет создать график РБП, основанный на шаблоне для номенклатуры выручки, по которой не выставлен счет. Если для этого параметра установлено значение **Да**, выберите шаблон РБП в поле **Шаблон** и измените даты начала и окончания РБП так, как это требуется. Последующие условия возобновления используют один и тот же шаблон РБП. Однако шаблон РБП можно изменить.</p></li></ul> |

### <a name="termination-tab"></a>Вкладка "Завершение"

На вкладке **Завершение** доступна следующая информация.

| Поле | Описание |
|-------|-------------|
| Дата увольнения | Дата, когда строка графика выставления счетов завершается. Значение по умолчанию берется из поля **Дата завершения** в заголовке. Если требуется, это значение можно изменить. |
| Тип завершения | Тип завершения. Значение по умолчанию берется из поля **Тип завершения** в заголовке. |

### <a name="hold-tab"></a>Вкладка "Блокировка"

Если используются выручка и расходы будущих периодов, на вкладке **Блокировка** отображается дата РБП.

### <a name="escalation-and-discount-tab"></a>Вкладка "Эскалация и скидка"

На вкладке **Эскалация и скидка** доступна следующая информация.

| Поле | Описание |
|-------|-------------|
| Увеличение | <p>Выберите, разрешены ли эскалации для строки графика выставления счетов. При создании строки графика выставления счетов применяется любая строка эскалации из заголовка.</p><ul><li>**Да** — эскалации могут быть применены к строке. Если выбран этот параметр, можно настроить эскалации для строк графика выставления счетов на странице **Эскалация и скидка**.</li><li>**Нет** — эскалации не могут быть применены к строке.</li></ul><p>Значение по умолчанию основывается на выбранной **Группе графиков выставления счетов**.</p> |

### <a name="price-changes-tab"></a>Вкладка "Изменения цены"

Для строк, измененных с цены **Стандартная** на **Фиксированная**, сетка на вкладке **Изменения цены** содержит следующие столбцы:

- Изменить дату
- Изменено пользователем
- Стандартная цена
- Фиксированная цена
- Обновить цену
