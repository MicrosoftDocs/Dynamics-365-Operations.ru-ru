---
title: Профили разноски запасов
description: В этой статье содержится обзор профилей разноски запасов.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cae5b39ef8e6e153fe522dee1874deae2a2cb86e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901352"
---
# <a name="inventory-posting-profiles"></a>Профили разноски запасов

[!include [banner](../includes/banner.md)]

Профили разноски запасов управляют разноской проводок субкниги запасов в главную книгу. Проводки субкниги запасов могут быть созданы из многих модулей, включая **Продажи и маркетинг**, **Закупки и источники**, **Управление производством** и т. д. Проводки субкниги запасов можно разносить каждый раз, когда номенклатура используется в заказе на продажу или в заказе на покупку. 

Дополнительные проводки субкниги запасов могут быть разнесены:
- каждый раз при обновлении документа;
- при разноске отборочной накладной или накладной по заказу на продажу;
- при создании поступления продуктов или накладной по заказу на продажу.

Для получения дополнительной информации перейдите в раздел "Проводки субкниги запасов".

## <a name="inventory-transaction-overview"></a>Просмотр складских проводок

Каждая проводка субкниги запасов включает:
 - Количество 
 - Цена 
 - Сайт 
 - Склад 
 - Расположение 

Проводки субкниги запасов создают две записи в главной книге с помощью физической разноски и финансовой разноски. Для получения дополнительных сведений перейдите в раздел [Физические и финансовые обновления](/supply-chain/cost-management/physical-financial-updates.md).
В следующем примере показан заказ на покупку с тремя строками. В данном примере предполагается, что весь заказ относится к отдельному сайту и складу. Каждая строка заказа на покупку имеет одну связанную запись InventTrans (также известную как складская проводка), и каждая строка относится к количеству 10. На следующей диаграмме показана связь заголовка одного заказа на покупку с тремя строками заказа на покупку, каждая с одной записью InventTrans.

![Схема отношений для заказа на покупку с тремя строками, каждая с одной записью InventTrans.](./media/InventTransRelationship.PNG)

Количество 5 получено в первой строке заказа на покупку. Полное количество для второй строки, а для третьей строки заказа на покупку количество не получено. Тут имеется вторая складская проводка, относящаяся к первой строке заказа на покупку. Проводка для второй строки заказа на покупку будет обновлена до состояния **Получено**, а третья проводка останется прежней. На следующей схеме показана связь с дополнительной записью InventTrans для строки заказа на покупку 1.

![Схема отношений для заказа на покупку с тремя строками. Одна строка получена частично и отображает две записи InventTrans.](./media/InventTransRelationshipPartialReceipt.PNG)

В этом примере операция будет разнесена в главную книгу; это физический ваучер. Группа номенклатурных моделей настроена для разноски физических запасов, и все номенклатуры используют одну и ту же группу номенклатурных моделей. Профиль разноски запасов использует один набор счетов ГК. Будет создан отдельный ваучер, и запись InventTrans будет связывать обе записи InventTrans 1 и InventTrans 2 с одним и тем же ваучером.

Затем для количества, полученного в строках 1 и 2, выдается накладная. Другой ваучер создается в главной книге; это финансовый ваучер. Группа номенклатурных моделей настроена для разноски финансовых запасов. Новый второй ваучер связан с InventTrans 1 и InventTrans 2.

В зависимости от модели затрат третья разноска главной книги может существовать для проводок субкниги запасов, относящихся к закрытию и сопоставлению запасов. Для получения дополнительных сведений перейдите в раздел [Закрытие запасов](/supply-chain/cost-management/inventory-close.md). Можно просмотреть сведения обо всех складских проводках, перейдя в меню **Управление запросами** > **Запросы и отчеты** > **Проводки**.

>[!Important]
> Складские проводки будут разделены для каждой уникальной комбинации складских аналитик и для каждого частичного обновления. Это было показано в предыдущем примере для частичного обновления.

### <a name="split-inventory-based-on-inventory-dimension-example"></a>Разбиение запасов на примере складской аналитики

Строка заказа на покупку 3 в данном примере является сериализованной номенклатурой. Десять серийных номеров зарегистрированы для заказа на покупку в процессе приемки. Складская проводка будет разбита на 10 складских проводок. На следующей схеме показаны отношения и дополнительные складские проводки, каждая со своим собственным серийным номером, связанная со строкой заказа на покупку 3.

![Схема отношений для заказа на покупку с тремя строками. Одна строка сериализована и отображает две дополнительные записи InventTrans.](./media/InventTransRelationshipSerialNumber.PNG)

В приведенном выше примере, если каждый серийный номер получен в одном поступлении продуктов, будет создан один дополнительный ваучер. Поле физического ваучера будет связано с каждым серийным номером. То же самое справедливо для финансового обновления при выставлении накладной по заказу на покупку.

## <a name="inventory-transactions"></a>Складские проводки

Можно просмотреть складские проводки на странице **Складские проводки** в модуле **Управление запасами и складами** или **Управление затратами**. Можно также просмотреть складские проводки, связанные с конкретной строкой документа-источника (например, строкой заказа на покупку или строкой заказа на продажу), путем выбора **Запасы** а затем — **Проводки**. 

Страница **Складские проводки** содержит следующие поля.

| Поле            | Описание                                 |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Код номенклатуры      | Код номенклатуры, связанный с проводкой.                                                                  |
| Физ. дата    | Дата прибытия запасов в склад, отпуска со склада, потребления в производстве или дата производства. Например, дата разноски
разноски отборочной накладной для заказа на продажу или разноски поступления продуктов для заказа на покупку.                             |
| Финанс. дата   | Дата закрытия складской проводки и записи затрат в главную книгу. Например, дата разноски при создании 
накладной для заказа на покупку. Обновления справочного документа не допускаются после заполнения финансовой даты. |
| Справка        | Указывает источник проводки и тип документа, который отображается в поле **Номер**. Например, заказ на продажу, заказ на покупку или приход по заказу на перемещение.                                                 |
| Номер           | Указывает код ссылки для проводки. Например, если в поле **Ссылка** указывается заказ на продажу, то в поле **Номер** указывается номер заказа на продажу.                                                       |
| Приход (статус) | Для складских проводок, которые являются приходами, это поле показывает статус прихода. Например, заказ на покупку является приходом, а статус может быть **Заказано** или **Куплено**.                                                            |
| Расход (статус)   | Для складских проводок, которые являются расходами, это поле показывает статус расхода. Например, заказ на продажу является расходом, а статус может быть **Заказано** или **Продано**.                         |
| Количество         | Количество в складской проводке. Положительные числа используются для приходов в запасы, в то время как отрицательные числа используются для расходов из запасов.                                                                                                                          |
| Единица измерения             | Единица измерения, в которой выражено количество.                                                                                   |
| Количество во вт. ед. изм.      | Количество учета в двух единицах измерения для проводки. Для получения дополнительных сведений перейдите в раздел [О номенклатуре с учетом в двух единицах измерения](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.).       |
| Вт. ед. изм.          | Единица измерения учета в двух единицах измерения в которой выражено количество учета в двух единицах измерения.                                                         |
| Сумма стоимости      | Окончательные затраты в складской проводке. Это поле заполняется, когда проводка финансово обновляется. В зависимости от методологии расчета себестоимости, закрытие запасов и процесс корректировки могут обновить это поле.                            |

## <a name="inventory-status"></a>Статус запасов

Каждая складская проводка имеет статус, который отображается в поле **Приход** или **Расход**. Используемое поле зависит от типа складских проводок. Приход — это проводки, увеличивающие запасы. Например, заказ на покупку с положительным количеством или возврат заказа на продажу с отрицательным количеством. Расход — это складские проводки, которые уменьшают запасы. Например, заказ на покупку с положительным количеством или возврат заказа на покупку с отрицательным количеством.

### <a name="receipt-status"></a>Статус прихода

В следующей таблице описываются статусы **Приход**.

| **Статус прихода** | **описание**       |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Занято            | Начальный статус любой складской проводки, которая представляет приход. Сюда входят заказы на покупку с положительным количеством, производственные заказы или возвраты по заказам на продажу с отрицательным количеством.                                                   |
| Зарегистрировано         | Этот статус используется, если выполняется двухэтапный процесс, или когда приход номенклатуры используется, чтобы указать, что продукт поступил. Он используется, когда для заказа выделены или зарегистрированы партия или серийные номера. Для получения дополнительных сведений о поступлении номенклатуры перейдите к разделу [Обзор прибытия](/supply-chain/inventory/arrival-overview.md). |
| Получено           | Этот статус используется, когда проводка физически обновляется. Для заказа на покупку это время разноски поступления продуктов. Для возврата по заказу на продажу это время разноски отборочной накладной.                                                                            |
| Куплено          | Этот статус используется, когда проводка финансово обновляется. Для заказа на покупку или возврата по заказу на продажу это время создания накладной.                                                                                             |

### <a name="issue-status"></a>Статус расхода

В следующей таблице описываются статусы **Расход**.

| **Статус расхода**  | **описание**            |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Заказано          | Начальный статус любой складской проводки, которая представляет расход. Сюда входят заказы на продажу с положительным количеством, строки спецификаций или формул производственных заказов или возвраты по заказам на продажу с отрицательным количеством.                                             |
| Зарезервировано в заказанных  | Этот статус запасов указывает на то, что запасы резервируются по заказу, который был создан, но еще физически не получен на склад. После получения запасов статус будет автоматически обновляться до состояния **Физ. зарезервировано**. Для получения дополнительных сведений о резервировании перейдите в раздел [Количество запасов резерва](/supply-chain/inventory/reserve-inventory-quantities.md). |
| Физ. зарезервировано | Этот статус указывает, что запасы были распределены или зарезервированы для определенного заказа. Когда запасы зарезервированы, они физически недоступны для других заказов.                                 |
| Скомплектовано         | Это означает, что запасы были скомплектованы со склада. Запасы все еще физически находятся на складе, не были удалены, но недоступны для других заказов.  |
| Отпущено          | Этот статус используется, когда проводка физически обновляется. Для заказа на продажу это время разноски отборочной накладной; для возврата по заказу на покупку это время разноски поступления продуктов.                                                                      |
| Продано              | Этот статус используется, когда проводка финансово обновляется. Для заказа на покупку или заказа на продажу это время создания накладной.|

Для получения дополнительных сведений о складских проводках перейдите в раздел [Сведения о складских проводках](/supply-chain/inventory/inventory-transactions-details.md).

## <a name="configure-an-inventory-posting-profile"></a>Настройка профиля разноски запасов

Чтобы настроить профиль разноски запасов, выполните следующие действия.

1.  Откройте **Управление запасами** > **Настройка** > **Разноска** > **Разноска**.
2.  Выберите вкладку для типа проводки. Например: выберите **Заказ на покупку**.
3.  Выберите переключатель для типа журнала разноски. Например, выберите **Расходы по закупкам для нескладируемой номенклатуры**.
4.  Выберите **Создать**.
5.  В поле **Код номенклатуры** выберите параметр для **Таблица**, **Группа**, **Все** или **Категория**. Например, чтобы настроить профиль разноски для конкретной номенклатурной группы, выберите **Группа**.
     - Если на шаге 5 был выбран параметр **Таблица**, выберите номер номенклатуры для профиля разноски в поле **Связь номенклатуры**.
     - Если на шаге 5 был выбран параметр **Группа**, выберите **Группа номенклатур** для профиля разноски в поле **Связь номенклатуры**.
     - Если на шаге 5 выбран параметр **Все**, поле **Связь номенклатуры** останется пустым.
     - Если на шаге 5 выбран параметр **Категория**, поле **Связь номенклатуры** останется пустым. Используйте поле **Связь категорий**, чтобы выбрать категорию, к которой относится профиль разноски.

6.  В поле **Код счета** выберите параметр для **Таблица**, **Группа** или **Все**. Например, чтобы применить профиль разноски ко всем поставщикам, выберите **Все**.
     - Если на шаге 5 был выбран параметр **Таблица**, выберите номер конкретного поставщика для профиля разноски в поле **Связь по контрагенту**.
     - Если на шаге 5 был выбран параметр **Группа**, выберите группу поставщиков для профиля разноски в поле **Связь по контрагенту**.
     - Если на шаге 5 выбран параметр **Все**, поле **Связь по контрагенту** будет пустым.

7.  Чтобы сопоставить определенную группу налогов с выбранным типом разноски, выберите **Налоговая группа**. Если это поле пустое, тип разноски применяется ко всем существующим налоговым группам. Разноска, указанная для налоговых групп, применяется только к проводкам по продажам и покупкам.
8.  В поле **Счет ГК** укажите номер счета, используемый для разноски типа счетов. Если номер счета, который используется в качестве типа учета, еще не создан, можно создать новый счет. Вы создаете новую учетную запись на странице **Сведения о счете ГК** в главной книге.

## <a name="additional-resources"></a>Дополнительные ресурсы

Каждая вкладка на странице **Профиль разноски запасов** относится к субкниге в Dynamics 365 Supply Chain Management. Дополнительные сведения см. в разделах:
-   [Разноска заказа на продажу](sales-order-posting.md)
-   [Разноска заказа на покупку](purchase-order-posting.md)
-   [Разноска запасов](inventory-posting.md)
-   [Разноска управления производством](production-posting.md)
-   [Разбивка стандартного отклонения стоимости](standard-cost-variance-posting.md)
