---
title: Покупки по комиссии
description: В этой статье приводятся сведения о покупках, производимых на условиях комиссии.
author: AdamTrukawka
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: atrukawk
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 656dfeeb7b574c6e1a4d5a05c224aab48ea6ad34
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272934"
---
# <a name="purchases-on-commission"></a>Покупки по комиссии
[!include [banner](../includes/banner.md)]

Доверитель нанимает агента, чтобы найти, от собственного лица агента, но за счет доверителя, подходящего поставщика и согласовать поставку товаров (работ или услуг) для доверителя.

Счета-фактуры, получаемые агентом от поставщика, имеют следующие характеристики:

- Агент должен зарегистрировать их на листе **Получено** журнала учета счетов-фактур.
- Их не требуется вводиться в книгу покупок агента, потому что агент не имеет прав на удержание налога на добавленную стоимость (НДС).
- Они должны быть скопированы, а копии должны быть сертифицированы и переданы доверителю.
- Агент должен повторно выпустить их для доверителя.

Счета-фактуры, которые агент повторно впускает, имеют следующие характеристики:

- Они должны быть зарегистрированы на листе **Выпущены** журнала учета счетов-фактур.
- Их не требуется вводить в книгу продаж, потому что агент не имеет обязательств по начислению НДС.

На следующем рисунке показан бизнес-процесс регистрации сделок через посредника. В системе отражены прямоугольные элементы. Овальные элементы присутствуют в бизнес-процессе, но не отражаются в системе.

![Последовательность бизнес-процесса покупки по комиссии.](media/Purchases_on_commission_english.jpg)

## <a name="create-a-sales-agreement-for-a-purchase-by-an-agent"></a>Создание договора продажи для покупки агентом

1. Перейдите в раздел **Расчеты с клиентами** \> **Заказы** \> **Договоры продажи**.
2. Выберите **Создать**, чтобы открыть диалоговое окно **Создание договора продажи**.
3. На экспресс-вкладке **Клиент** укажите счет клиента, затем в поле **Классификация договоров продажи** выберите **Общий договор продажи**.
4. На экспресс-вкладке **Общие сведения** в разделе **Документ** в поле **Код договора продажи** укажите код договора продажи.
5. Укажите другие сведения, затем выберите **ОК**.

    ![Диалоговое окно создания классификаций договоров продажи.](media/3_Create_sales_agreement.jpg)

6. На странице **Договоры продажи** перейдите в представление **Заголовок**.
7. На Экспресс-вкладке **Общие сведения** в разделе **Документ** в поле **Комиссионное соглашение** выберите **Покупка комиссионером**.
8. На экспресс-вкладке **Финансы** в разделе **Профиль учета** укажите следующие сведения:

    - В поле **Вид деятельности** выберите **Комиссионер**.
    - В поле **Профиль учета** выберите профиль учета, созданный ранее.

    ![Страница договора продажи, экспресс-вкладка финансов.](media/4_Sales_agreements.jpg)

9. На панели операций на вкладке **Договор продажи** в группе **Создать** выберите **Подтверждение** для обновления статуса договора до **Действует**.

## <a name="create-inventory-owners-suppliers-for-a-commissioner"></a>Создание владельцев запасов (поставщиков) для комиссионера

1. Перейдите в раздел **Запасы** \> **Настройка** \> **Аналитики** \> **Владельцы запасов**.
2. Выберите **Создать**, чтобы создать владельца запасов.
3. В поле **Владелец** введите код для владельца.
4. В поле **Тип счета** выберите **Поставщик**.
5. В поле **Организация** выберите код для поставщика. Поле **Имя** заполняется автоматически.
6. Нажмите **Сохранить**.

![Страница владельцев запасов для поставщиков.](media/5_Inventory_owners.jpg)

## <a name="create-inventory-owners-principals-for-a-commissioner"></a>Создание владельцев запасов (доверителей) для комиссионера

1. Перейдите в раздел **Управление запасами** \> **Настройка** \> **Аналитики** \> **Владельцы запасов**.
2. Выберите **Создать**, чтобы создать владельца запасов.
3. В поле **Владелец** введите код для владельца.
4. В поле **Тип счета** выберите **Клиент**.
5. В поле **Организация** выберите код для доверителя. Поле **Имя** заполняется автоматически.
6. Нажмите **Сохранить**.

![Страница владельцев запасов для клиентов.](media/6_Inventory_owners.jpg)

## <a name="create-a-purchase-order-and-update-the-facture-on-goods-that-are-purchased-for-a-principal"></a>Создание заказа на покупку и обновление счета-фактуры на товары, приобретаемые для доверителя

1. Создание заказа на покупку.
2. В строке заказа на покупку выберите код номенклатуры.

> [!NOTE]
> В поле **Аналитика отслеживания** для данной номенклатуры должен быть указан профиль учета, созданный ранее.

3. На экспресс-вкладке **Сведения по строке** на вкладке **Продукт** в разделе **Аналитики отслеживания** в поле **Профиль учета** выберите профиль учета, созданный ранее.
4. Если разноска счета не планируется, в поле **Владелец** выберите владельца (поставщика), который был создан ранее. Таким образом, при повторном выдаче счета-фактуры в отчете для доверителя указывается поставщик.

    ![Страница "Заказ на покупку".](media/7_All_purchase_orders.jpg)

5. Укажите другие параметры заказа на покупку и создайте счет-фактуру.

## <a name="create-a-sales-order-and-generate-a-sales-invoice-for-goods-that-are-purchased-for-a-principal"></a>Создание заказа на продажу и создание накладной по продаже для товаров, приобретенных для доверителя

1. Создание нового заказа на продажу.
2. В поле **Код договора продажи** выберите договор для покупки агентом, созданный ранее.
3. В строке заказа на продажу выберите код номенклатуры, которая была куплена ранее.

   > [!NOTE]
   > В поле **Аналитика отслеживания** для данной номенклатуры должен быть указан профиль учета, созданный ранее.

4. На экспресс-вкладке **Сведения по строке** на вкладке **Настройка** в разделе **Запасы** в поле **Резервирование** выберите **Автоматически**.

    ![Страница заказа на продажу.](media/8_Sales_order.jpg)

5. На экспресс-вкладке **Сведения по строке** на вкладке **Продукт** в разделе **Аналитики отслеживания** убедитесь, что в поле **Профиль учета** автоматически задан профиль учета, созданный ранее.
6. В поле **Владелец** выберите владельца (доверителя), созданного ранее.
7. На экспресс-вкладке **Строки заказа на продажу** выберите **Запасы \> Маркировка**.
8. Выберите проводку покупки, выберите **Пометить**, затем выберите **ОК**.
9. Разноска накладной.

## <a name="create-and-print-a-report-for-a-principal-and-reissue-the-sellers-factures-to-the-principal"></a>Создание и печать отчета для доверителя и повторный выпуск счетов-фактур продавца для доверителя

1. Перейдите к пункту **Главная книга** \> **Периодические задачи** \> **Комиссионная торговля** \> **Отчет для доверителя**.
2. Выберите **Создать**, чтобы открыть **диалоговое окно** **Создание отчета для доверителя**.
3. В полях **Дата начала** и **Дата окончания** укажите период для отчета.

   > [!NOTE]
   > Поле **Дата начала** можно оставить пустым.

4. В поле **Тип доверителя** выберите **Клиент**.
5. В поле **Код партнера** выберите счет клиента.
6. В поле **Код договора** выберите договор продажи.
7. Нажмите **ОК**.

   > [!NOTE]
   > Для создания заголовков для всех отчетов по доверителю, которые необходимы в течение указанного периода, выберите **Функции \> Создать заголовки отчетов по отгрузкам**.

8. Выберите **Функции \> Обновить строки отгрузки**, чтобы открыть диалоговое окно **Создание отчета для доверителя по отгрузкам**, затем выберите **OK**, чтобы создать строки для каждого отчета.
9. Основываясь на счетах-фактурах, полученных от продавца (поставщика), вы в качестве агента должны повторно выпустить счета-фактуры по отгруженной части товаров доверителю (клиенту) от имени продавца. Эти новые счета-фактуры нумеруются в соответствии с номерной серией счетов-фактур.
10. На странице **Отчет для доверителя** используйте флажок **Утверждено**, чтобы утвердить соответствующие строки счетов-фактур продавца. Чтобы утвердить все строки отчета, выберите **Утверждение \> Утвердить все**.

    ![Страница отчета для доверителя.](media/9_Report_for_principal.jpg)

11. Выберите **Счет-фактура \> Обновить счет-фактуру**, чтобы создать повторно выпущенную счет-фактуру для доверителя.
12. На странице **Обновить счет-фактуру** в разделе **Комиссионная торговля** убедитесь, что поля **Продавец** и **Счет-фактура** настроены автоматически. Если они пусты, выберите поставщика в поле **Продавец** и номер счета-фактуры покупки, который был создан в поле **Счет-фактура**.
13. Укажите другие необходимые сведения и создайте счет-фактуру.

    ![Страница обновления счета-фактуры.](media/10_Update_facture.jpg)

14. На странице **Отчет для доверителя** выполните следующие действия:

    - Выберите **Доверитель** \> **Журнал накладных** для просмотра накладной доверителя.
    - Выберите **Доверитель** \> **Счет-фактура** для просмотра счета-фактуры доверителя.
    - Выберите **Запросы** \> **Журнал накладных** для просмотра исходной накладной продавца.
    - Выберите **Запросы** \> **Счет-фактура** для просмотра исходного счета-фактуры продавца.

15. Выберите **Печать**, чтобы открыть диалоговое окно **Отчет для доверителя в Microsoft Excel**, затем выберите **OK**, чтобы напечатать отчет для доверителя.

![Создание отчета для доверителя.](media/11_Report_for_a_principal.jpg)


## <a name="print-a-facture-accounting-journal"></a>Печать журнала учета счетов-фактур

1. Выберите **Главная книга** \> **Запросы и отчеты** \> **Отчеты журналов** \> **Счет-фактура**, чтобы открыть диалоговое окно **Журнал учета счетов-фактур**.
2. Укажите период для отчета, затем выберите **OK**, чтобы напечатать журнал учета счетов-фактур.

Лист **Выпущенные** журнала учета счетов-фактур показывает повторно выпущенные счета-фактуры поставщика. Сведения о продавцах представлены в столбцах с 10 по 12.

![Лист "Выпущенные" журнала учета счетов-фактур.](media/12_Facture_accounting_journal_Part_1.jpg)

На листе **Получено** журнала учета счетов-фактуры отображаются счета-фактуры исходного продавца, которые были утверждены в отчете для доверителя.

![Лист "Получено" журнала учета счетов-фактур.](media/13_Facture_accounting_journal_Part_2.jpg)

## <a name="prepayments"></a>Предоплаты

Предоплаты, полученные от доверителя, не являются источником для начисления НДС. Они должны быть повторно отправлены одному или нескольким продавцам. Эти повторно отправленные предоплаты должны быть включены в отчет для доверителя. Предоплаты, полученные от двух или более доверителей, могут быть повторно отправлены одному продавцу. Эти повторно отправленные предоплаты должны быть включены в отчеты для доверителей.

### <a name="create-prepayments-a-purchase-order-a-sales-order-and-a-report-for-a-principal"></a>Создание предоплат, заказа на покупку, заказа на продажу и отчета для доверителя

1. На странице **Журнал платежей клиентов** создайте предоплату клиента, затем выберите **Строки**.
2. На странице **Платежи клиентов** в столбце **Вид действия** выберите **Комиссионер**, чтобы указать, что предоплата будет повторно отправлена продавцам.

    > [!NOTE]
    > Если столбец **Вид действия** не отображается, щелкните правой кнопкой мыши в строке, содержащей названия столбцов, затем выберите **Добавить столбцы**. Установите флажок для столбца **Вид действия**, затем выберите **Вставить**.

      ![Страница журнала платежей поставщика.](media/14_Customer_payments.jpg)

3. На странице **Журнал платежей поставщикам** создайте предоплату поставщику, затем выберите **Строки**.
4. На странице **Платежи поставщикам** в столбце **Вид действия** выберите **Комиссионер**.

    ![Страница платежей поставщикам.](media/15_Vendor_payments.jpg)

5. Создайте счет-фактуру для предоплаты поставщику.
6. Создайте заказ на покупку и счет-фактуру.
7. Создайте заказ на продажу и счет.
8. Создайте отчет для доверителя и обновите строки в отгрузках.
9. В нижней части страницы **Отчет для доверителя** на вкладке **Предоплаты** в поле **Ваучер** выберите ваучер предоплаты поставщику, чтобы включить эту предоплату в отчет для доверителя.

    ![Страница отчета для доверителя, вкладка предоплаты.](media/16_Report_for_principal.jpg)

10. Выберите **Проводки** для просмотра распределенной суммы в поле **Сумма в валюте отчетности**.

    ![Страница проводок по поставщику.](media/17_Vendor_transactions.jpg)

11. На странице **Отчет для доверителя** утвердите строки на вкладке **Обзор** и ваучеры на вкладке **Предоплаты**.
12. Можно создать счет-фактуру и просмотреть счет доверителя (или счет-фактуру) или исходный счет (или счет-фактуру).

### <a name="print-a-report-for-the-principal"></a>Печать отчета для доверителя

Напечатайте отчет для доверителя. Отчет для доверителя имеет два раздела: один для отгрузок, другой для предоплат.


![Созданный отчет о покупке.](media/18_Purchase_report.jpg)

### <a name="create-a-prepayment-facture"></a>Создание счета-фактуры на предоплату

1. На странице **Отчет для доверителя** на вкладке **Предоплаты** установите флажок **Утвердить**, затем выберите **Создать счет-фактуру**, чтобы зарегистрировать счет-фактуру на предоплату для доверителя.
2. На странице **Создание счета-фактуры** используйте флажок **Отметить** для выбора соответствующих предоплат.
3. Выберите **Создать счет-фактуру**, чтобы открыть диалоговое окно **Создание счета-фактуры**.
4. Укажите дату регистрации, затем выберите **ОК**.

    ![Диалоговое окно создания счета-фактуры.](media/19_Facture_create.jpg)

5. На странице **Отчет для доверителя** на вкладке **Предоплаты** выберите **Доверитель \> Счет-фактура**, чтобы просмотреть зарегистрированный счет-фактуру доверителя для предоплаты.

    ![Страница журнала счетов-фактур.](media/20_Facture_journal.jpg)

6. Выберите **Печать \> Оригинал** для печати исходного счета-фактуры или выберите **Печать \> Копия**, чтобы напечатать копию счета-фактуры.


![Распечатанный счет-фактура.](media/21_Invoice-facture.jpg)

### <a name="create-a-facture-accounting-journal"></a>Создание журнала учета счетов-фактур

В журнале учета счетов-фактур отображаются утвержденные строки. Можно распечатать журнал учета счетов-фактур.

Предоплаты, полученные от доверителя, будут переведены продавцу. Когда продавец выдает для агента счет-фактуру на предоплату, агент регистрирует счета-фактуры продавца на листе **Получено** журнала учета счетов-фактур. Лист **Выдано** журнала учета счетов-фактур отражает счета-фактуры, которые были повторно выпущены для доверителя.

Оригинальные счета-фактуры на поставку товаров от продавцов могут быть распределены между доверителями. Лист **Получено** журнала учета счетов-фактур отражает исходные счета-фактуры.

![Журнал учета счетов-фактур, лист "Получено".](media/22_Facture_accounting_journal_Part_2.jpg)

Лист **Выдано** журнала учета счетов-фактур отражает повторно выпущенные счета-фактуры (т. е., выделенные части счетов-фактур продавцов). Сведения о продавцах представлены в столбцах с 10 по 12.

![Журнал учета счетов-фактур, лист "Выпущенные".](media/23_Facture_accounting_journal_Part_1.jpg)

Более подробную информацию см. в следующих разделах:

- [Проводки через посредников](rus-transactions-through-intermediary.md) 
- [Продажи по комиссии](rus-sales-on-commission.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
