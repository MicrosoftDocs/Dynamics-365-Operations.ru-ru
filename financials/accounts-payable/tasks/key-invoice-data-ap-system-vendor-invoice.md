--- 
title: "Ввод данных счета в модуль расчетов с поставщиками с использованием накладной поставщика"
description: "Этот проводник по задаче поможет вам создать накладную поставщика из заказа на покупку и просмотреть результаты сопоставления заказа на покупку, поступления и накладной (трехстороннее сопоставление)."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: a365c52af49a66d6af5bb38f0053bd9c0fd34301
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-a-vendor-invoice"></a>Ввод данных счета в модуль расчетов с поставщиками с использованием накладной поставщика

[!include[task guide banner](../../includes/task-guide-banner.md)]

Этот проводник по задаче поможет вам создать накладную поставщика из заказа на покупку и просмотреть результаты сопоставления заказа на покупку, поступления и накладной (трехстороннее сопоставление).


## <a name="create-a-purchase-order"></a>Создание заказа на покупку
1. Перейдите в раздел "Расчеты с поставщиками" > "Заказы на покупку" > "Все заказы на покупку".
2. Щелкните "Создать".
3. В поле "Счет поставщика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
4. Найдите поставщика для выбора. Например, прокрутите вниз до US-104.
5. Выберите поставщика US-104.
6. Нажмите кнопку OK.
7. В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
8. Выберите складируемую номенклатуру. Например, выберите код номенклатуры 1000.
9. Разверните или сверните раздел "Сведения о строке".
10. Перейдите на вкладку "Настройка".
    * Вы можете переопределить политику проверки соответствия, чтобы использовать двухстороннее сопоставление, трехстороннее сопоставление или полностью отключить сопоставление.  
11. Разверните или сверните раздел "Сведения о строке".
12. В области действий щелкните "Покупка".
13. Нажмите кнопку "Подтвердить".

## <a name="receive-the-products"></a>Получение продукции
1. В области действий щелкните "Получение".
2. Щелкните "Поступление продуктов".
3. В поле "Поступление продуктов" введите номер поступления продуктов. Например, введите "PR123".
4. Щелкните "ОК", чтобы выполнить разноску поступления продуктов.
5. Закройте страницу.

## <a name="create-a-vendor-invoice"></a>Создание накладной поставщика
1. Перейдите в раздел "Расчеты с поставщиками" > "Заказы на покупку" > "Полученные заказы на покупку без выставленных накладных".
2. Выберите созданный заказ на покупку.
3. В области действий щелкните "Накладная".
4. Щелкните "Накладная".
5. В поле "Номер" введите номер накладной.
6. В поле "Описание накладной" введите значение.
7. В поле "Дата накладной" введите дату.
8. В поле "Цена за единицу" введите 1200.
9. Щелкните "Добавить строку".
10. В поле "Код номенклатуры" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
11. В списке найдите код номенклатуры накладных расходов на установку. Например, S0001.
12. Выберите код номенклатуры накладных расходов на установку.
    * Обратите внимание, что сопоставление не выполнялось с момента внесения изменений.  
13. Щелкните "Обновить статус сопоставления".
14. В области действий щелкните "Просмотр".
15. Щелкните "Сведения о сопоставлении".
    * Новую строку со службами не требуется сопоставлять, поэтому статус останется прежним: "Не выполнено".  
16. Выберите поступление продуктов для полученной складируемой номенклатуры.
    * Строка с поступлением продуктов была сопоставлена, но имеется расхождение в количестве или цене, поэтому появляется ошибка.  
17. В поле "Цена за единицу" введите число.
    * Теперь, когда цена за единицу совпадает, статус обновится до значения "Выполнено". Если политика допускает расхождения или если результатом сопоставления является лишь предупреждение, накладную все равно можно разнести.  
18. Закройте страницу.
19. Щелкните "Разнести".
20. Закройте форму.
    * Обратите внимание, что заказ на покупку больше не указан как полученный, но без выставления в накладных.  

