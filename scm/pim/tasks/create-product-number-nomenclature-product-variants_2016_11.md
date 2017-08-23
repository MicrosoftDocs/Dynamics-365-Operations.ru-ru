--- 
title: "Создание номера продукта для настроенных вариантов продукта"
description: "На этой процедуры показано, как настроить номенклатуру номера продукта для сконфигурированных вариантов продукта, и как ее можно добавить в конфигурируемый шаблон продукта."
author: BibiSp
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 8a9bf8241a0dc66f34715513d2d201569b810582
ms.contentlocale: ru-ru
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-product-number-for-configured-product-variants"></a>Создание номера продукта для настроенных вариантов продукта

[!include[task guide banner](../../includes/task-guide-banner.md)]

На этой процедуры показано, как настроить номенклатуру номера продукта для сконфигурированных вариантов продукта, и как ее можно добавить в конфигурируемый шаблон продукта. Эта процедура также демонстрирует, как можно создать конфигурацию номенклатуры для компонента модели конфигурации продукта. В качестве компании с демонстрационными данными для создания этой процедуры используется USMF. Новая номенклатура номера продукта назначена шаблону продукта D0004. Эта задача обычно выполняется конструктором продуктов.


## <a name="create-a-product-number-nomenclature"></a>Создание номенклатуры номеров продуктов
1. Щелкните "Определение модели вариантов продукта".
2. Щелкните "Номенклатура продуктов".
3. Щелкните "Создать".
4. В поле "Имя" введите значение.
5. В поле "Описание" введите значение.
6. Нажмите кнопку Добавить.
7. Щелкните "Номер шаблона продукта".
8. Нажмите кнопку Добавить.
9. Щелкните "Текстовая константа".
10. В списке пометьте выбранную строку.
11. В поле "Текст" введите значение.
12. Нажмите кнопку Добавить.
13. Щелкните "Конфигурация".
14. Закройте страницу.

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a>Назначение номенклатуры номеров продуктов шаблону продукта
1. Щелкните "Шаблоны продукта".
2. Используйте экспресс-фильтр для поиска записей. Например, отфильтруйте поле "Номер продукта" по значению "D".
3. В списке перейдите по ссылке в выбранной строке.
4. Выберите Изменить.
5. Выберите "Да" в поле "Использовать номенклатуру".
6. В поле "Номенклатура номеров вариантов продуктов" введите или выберите значение.
7. Закройте страницу.
8. Закройте страницу.

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a>Создание номенклатуры для компонента модели конфигурации продукта
1. Щелкните "Модели конфигурации продукта".
2. В списке найдите и выберите требуемую запись.
3. В списке перейдите по ссылке в выбранной строке.
4. Выберите Изменить.
5. Выберите "Да" в поле "Использовать номенклатуру конфигурации".
6. Нажмите кнопку Добавить.
7. Щелкните "Значение атрибута".
8. В списке пометьте выбранную строку.
9. В поле "Атрибут" введите или выберите значение.
10. Нажмите кнопку Добавить.
11. Щелкните "Текстовая константа".
12. В списке пометьте выбранную строку.
13. В поле "Текст" введите значение.
14. Нажмите кнопку Добавить.
15. Щелкните "Значение атрибута".
16. В списке пометьте выбранную строку.
17. В поле "Атрибут" введите или выберите значение.
18. Нажмите кнопку Добавить.
19. Щелкните "Текстовая константа".
20. В списке пометьте выбранную строку.
21. В поле "Текст" введите значение.
22. Нажмите кнопку Добавить.
23. Щелкните "Значение атрибута".
24. В списке пометьте выбранную строку.
25. В поле "Атрибут" введите или выберите значение.
26. Нажмите кнопку Добавить.
27. Щелкните "Текстовая константа".
28. В списке пометьте выбранную строку.
29. В поле "Текст" введите значение.
30. Нажмите кнопку Добавить.
31. Щелкните "Значение атрибута".
32. В списке пометьте выбранную строку.
33. В поле "Атрибут" введите или выберите значение.
34. Нажмите кнопку Добавить.
35. Щелкните "Текстовая константа".
36. В списке пометьте выбранную строку.
37. В поле "Текст" введите значение.
38. Нажмите кнопку Добавить.
39. Щелкните "Значение номерной серии".
40. В списке пометьте выбранную строку.
41. В поле "Номерная серия" введите или выберите значение.
42. Закройте страницу.
43. Закройте страницу.
44. Закройте страницу.

