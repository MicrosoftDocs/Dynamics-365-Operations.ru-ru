--- 
title: "Создание сырья (только для версии от февраля 2016 г.)"
description: "Эта задача рассматривает создание компонентов готовой продукции и полуфабрикатов."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: a20a2c720af7c981cced231c0f863a1bd8283f2c
ms.contentlocale: ru-ru
ms.lasthandoff: 07/28/2017

---
# <a name="create-raw-materials-february-2016-only"></a>Создание сырья (только для версии от февраля 2016 г.)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Эта задача рассматривает создание компонентов готовой продукции и полуфабрикатов. Это третья задача в серии расчетов спецификации. В качестве компании с демонстрационными данными для создания этой задачи используется USMF.


## <a name="create-the-first-material"></a>Создание первого материала
1. Щелкните "Управление сведениями о продукте" > "Продукты" > "Выпущенные продукты".
2. Щелкните "Создать".
3. В поле "Номер продукта" введите значение.
    * В этом примере введите "ITEM_A".  
4. В поле "Группа номенклатурных моделей" введите или выберите значение.
    * Выберите STD. STD означает "стандартная себестоимость" и является наиболее часто используемой моделью при работе с расчетами затрат.  
5. В поле "Номенклатурная группа" введите или выберите значение.
    * Например, выберите "Аудио". Это не окажет влияния на расчеты затрат.  
6. В поле "Группа аналитик хранения" введите или выберите значение.
    * Выберите SiteWH. Только сайт и склад будут использоваться для демонстрации.  
7. В поле "Группа аналитик отслеживания" введите или выберите значение.
    * Аналитики отслеживания не будут использоваться для данного примера. Выберите "Нет".  
8. Нажмите кнопку "OК".
9. В области действий щелкните "Управление запасами".
10. Щелкните "Параметры заказа по умолчанию".
11. В поле "Сайт покупок" введите или выберите значение.
    * В этом примере выберите "Cайт 1".  
12. В поле "Сайт запасов" введите или выберите значение.
    * В этом примере выберите "Cайт 1".  
13. В поле "Сайт продаж" введите или выберите значение.
    * В этом примере выберите "Cайт 1".  
14. Закройте страницу.
15. Закройте страницу.
16. В списке перейдите по ссылке в выбранной строке.
    * Щелкните ITEM_A.  
17. Разверните раздел "Управление затратами".
18. В поле "Группа затрат" введите значение.
    * В этом примере введите "M2".  
19. В области действий щелкните "Управление затратами".
20. Щелкните "Цена номенклатуры".
21. Щелкните "Создать".
22. В поле "Версия" введите или выберите значение.
    * В этом примере выберите 10 — тип цены стандартной себестоимости.  
23. В поле "Сайт" введите или выберите значение.
    * В этом примере выберите "Cайт 1".  
24. В поле "Цена" введите число.
    * В этом примере введите "10".  
25. Нажмите кнопку "Сохранить".
26. Щелкните "Активировать ожидающие цены".
27. Закройте страницу.
28. Закройте страницу.

## <a name="create-the-second-material"></a>Создание второго материала
1. Щелкните "Создать".
2. В поле "Номер продукта" введите значение.
    * В этом примере введите "ITEM_B".  
3. В поле "Группа номенклатурных моделей" введите или выберите значение.
    * Выберите STD. STD означает "стандартная себестоимость" и является наиболее часто используемой моделью при работе с расчетами затрат.  
4. В поле "Номенклатурная группа" введите или выберите значение.
    * Например, выберите "Аудио". Это не окажет влияния на расчеты затрат.  
5. В поле "Группа аналитик хранения" введите или выберите значение.
    * Выберите SiteWH. Только сайт и склад будут использоваться в этом примере.  
6. В поле "Группа аналитик отслеживания" введите или выберите значение.
    * Аналитики отслеживания не будут использоваться для данного примера. Выберите "Нет".  
7. Нажмите кнопку "OК".
8. В области действий щелкните "Управление запасами".
9. Щелкните "Параметры заказа по умолчанию".
10. В поле "Сайт покупок" введите или выберите значение.
    * В этом примере выберите "Cайт 1".  
11. В поле "Сайт запасов" введите или выберите значение.
    * В этом примере выберите "Cайт 1".  
12. В поле "Сайт продаж" введите или выберите значение.
    * В этом примере выберите "Cайт 1".  
13. Закройте страницу.
14. Закройте страницу.
15. В списке перейдите по ссылке в выбранной строке.
    * Щелкните ITEM_B.  
16. Разверните раздел "Управление затратами".
17. В поле "Группа затрат" введите значение.
    * В этом примере введите "M2".  
18. В области действий щелкните "Управление затратами".
19. Щелкните "Цена номенклатуры".
20. Щелкните "Создать".
21. В поле "Версия" введите или выберите значение.
    * В этом примере выберите "10". Это тип цены стандартной себестоимости.  
22. В поле "Сайт" введите или выберите значение.
    * В этом примере выберите "Cайт 1".  
23. В поле "Цена" введите число.
    * В целя демонстрации введите 10.  
24. Нажмите кнопку "Сохранить".
25. Щелкните "Активировать ожидающие цены".
26. Закройте страницу.
27. Закройте страницу.

## <a name="create-the-third-material"></a>Создание третьего материала
1. Щелкните "Создать".
2. В поле "Номер продукта" введите значение.
    * В целя демонстрации введите ITEM_C.  
3. В поле "Группа номенклатурных моделей" введите или выберите значение.
    * Выберите STD. STD означает "стандартная себестоимость" и является наиболее часто используемой моделью при работе с расчетами затрат.  
4. В поле "Номенклатурная группа" введите или выберите значение.
    * Например, выберите "Аудио". Это не окажет влияния на расчеты затрат.  
5. В поле "Группа аналитик хранения" введите или выберите значение.
    * Выберите SiteWH. Только сайт и склад будут использоваться для демонстрации.  
6. В поле "Группа аналитик отслеживания" введите или выберите значение.
    * Аналитики отслеживания не будут использоваться для данного примера. Выберите "Нет".  
7. Нажмите кнопку "OК".
8. В области действий щелкните "Управление запасами".
9. Щелкните "Параметры заказа по умолчанию".
10. В поле "Сайт покупок" введите или выберите значение.
    * В этом примере выберите "Cайт 1".  
11. В поле "Сайт запасов" введите или выберите значение.
    * В этом примере выберите "Cайт 1".  
12. В поле "Сайт продаж" введите или выберите значение.
    * В этом примере выберите "Cайт 1".  
13. Закройте страницу.
14. Закройте страницу.
15. В списке перейдите по ссылке в выбранной строке.
    * Щелкните ITEM_C.  
16. Разверните раздел "Управление затратами".
17. В поле "Группа затрат" введите значение.
    * В этом примере введите "M1".  
18. В области действий щелкните "Управление затратами".
19. Щелкните "Цена номенклатуры".
20. Щелкните "Создать".
21. В поле "Версия" введите или выберите значение.
    * В этом примере выберите "10". Это тип цены стандартной себестоимости.  
22. В поле "Сайт" введите или выберите значение.
    * В этом примере выберите "Cайт 1".  
23. В поле "Цена" введите число.
    * В этом примере введите "10".  
24. Нажмите кнопку "Сохранить".
25. Щелкните "Активировать ожидающие цены".
26. Закройте страницу.
27. Закройте страницу.

