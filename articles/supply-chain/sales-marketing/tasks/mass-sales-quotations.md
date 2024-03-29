---
title: Создать предложения по продажам
description: Эта процедура демонстрирует, как эффективно создавать предложения, предлагающие набор продуктов или услуг, которые должны быть отправлены нескольким клиентам.
author: Henrikan
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm, SalesQuickQuote
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: acb2b49c7cb2024aec1140d04150bd1ab9d75c14
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573377"
---
# <a name="mass-create-sales-quotations"></a>Создать предложения по продажам

[!include [banner](../../includes/banner.md)]

Эта процедура демонстрирует, как эффективно создавать предложения, предлагающие набор продуктов или услуг, которые должны быть отправлены нескольким клиентам. Это массовое создание предложений основано на шаблонах предложений. Эту процедуру можно выполнить со своими данными или с демонстрационными данными USMF.


## <a name="create-a-quotation-template"></a>Создание шаблона предложений
1. Перейдите в раздел "Продажи и маркетинг" > "Настройка" > "Предложения" > "Группы шаблонов".
2. Щелкните "Создать".
3. В поле "Код группы" введите код.
4. В поле "Описание" введите значение.
5. Нажмите кнопку "Сохранить".
6. Закройте страницу.
7. Перейдите в раздел "Продажи и маркетинг" > "Предложение по продажам" > "Все предложения".
8. Щелкните "Создать".
9. В поле "Тип счета" выберите "Клиент".
10. В поле "Счет клиента" введите или выберите значение.
11. Нажмите кнопку "OК".
    * Чтобы предложение стало шаблоном, требуется выполнить этап настройки в заголовке предложения. Это необходимо сделать перед добавлением строк в предложение.   
12. В области действий щелкните "Параметры".
13. Щелкните "Изменить режим просмотра".
14. Щелкните Вид заголовка.
15. Разверните раздел "Настройка".
16. В поле "Код группы" введите или выберите значение.
17. В поле "Имя шаблона" введите значение.
18. Выберите значение "Да" в поле "Активно".
    * Только активные шаблоны можно использовать при применении шаблона в новом предложении по продаже.  
19. В области действий щелкните "Параметры".
20. Щелкните "Изменить режим просмотра".
21. Щелкните Линейное представление.
22. В поле "Номенклатура" введите или выберите значение.
23. В поле "Номенклатура" введите значение.
24. Закройте страницу.
25. В поле "Процент скидки" введите число.
26. Щелкните "Добавить строку".
27. В поле "Номенклатура" введите или выберите значение.
28. В поле "Номенклатура" введите значение.
29. Закройте страницу.
30. В поле "Цена за единицу" введите новую цену или измените текущую.
31. Щелкните "Добавить строку".
32. В поле "Номенклатура" введите или выберите значение.
33. В поле "Номенклатура" введите значение.
34. Закройте страницу.
35. В поле "Количество" введите число.
36. В поле "Скидка" введите число.
37. Нажмите кнопку "Сохранить".

## <a name="apply-the-template-to-create-a-single-quotation"></a>Применение шаблона для создания одного предложения
1. Перейдите в раздел "Продажи и маркетинг" > "Предложение по продажам" > "Все предложения".
    * Обратите внимание, что предложение, только что созданное, отмечено как шаблон.  
2. Щелкните "Создать".
3. В поле "Тип счета" выберите "Клиент".
4. В поле "Счет клиента" введите или выберите значение.
5. Разверните раздел "Шаблон".
6. В поле "Код группы" введите или выберите значение.
7. В поле "Имя шаблона" введите или выберите значение.
8. В поле "Способ расчета" выберите "Основано на значениях шаблона".
9. Нажмите кнопку "OК".
    * Теперь новое предложение создано на основе данных и условий шаблона.  
10. Закройте страницу.
11. Закройте страницу.

## <a name="apply-the-template-to-mass-create-quotations"></a>Применение шаблона для массового создания предложений
1. Перейдите в раздел "Продажи и маркетинг" > "Предложения по продажам" > "Обновление предложения" > "Массовое создание предложений".
2. В поле "Тип счета" выберите "Клиент".
3. В поле "Код группы" введите или выберите значение.
4. В поле "Имя шаблона" введите или выберите значение.
5. В поле "Способ расчета" выберите "Основано на значениях шаблона".
6. Разверните раздел "Записи для добавления".
7. Щелкните "Фильтр".
8. В поле "Критерии" установите фильтр для покрытия диапазон клиентов, которых требуется включить в это массовое создание предложения. Используйте следующий формат "Customer1..CustomerN".
    * Например, можно установить фильтр для: US-001..US-004  
9. Нажмите кнопку "OК".
10. Нажмите кнопку "OК".
11. Перейдите в раздел "Продажи и маркетинг" > "Предложение по продажам" > "Все предложения".
    * Убедитесь, что предложения были созданы для всех клиентов, указанных в процедуре массового обновления, как основанные на выбранном шаблоне.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]