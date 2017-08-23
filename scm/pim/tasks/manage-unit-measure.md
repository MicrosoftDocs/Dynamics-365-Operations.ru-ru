--- 
title: "Управление единицей измерения"
description: "В этой процедуре показано, как определить единицу измерения, ввести переводы для единицы измерения и ее описание, а также определить правила преобразования для связанных единиц измерения."
author: sorenva
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: de5baa1e5c30ee998d113f7366c445a65723dfdc
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="manage-unit-of-measure"></a>Управление единицей измерения

[!include[task guide banner](../../includes/task-guide-banner.md)]

В этой процедуре показано, как определить единицу измерения, ввести переводы для единицы измерения и ее описание, а также определить правила преобразования для связанных единиц измерения. Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными или собственные данные.

1. Перейдите в раздел "Обслуживание выпущенного продукта".
2. Щелкните "Единицы измерения".

## <a name="create-a-unit-of-measure"></a>Создание единицы измерения
1. Щелкните "Создать".
2. В поле "Единица измерения" введите значение.
    * Введите код или символ, который будет использоваться при ссылке на единицу измерения.  
3. В поле "Описание" введите значение.
    * Введите описательное имя для единицы измерения на системном языке.  
4. В поле "Класс единиц измерения" выберите один их вариантов.
    * Класс единиц измерения определяет, к какому логическому группированию (такому как площадь, масса или количество) принадлежит единица измерения.  
5. В поле "Десятичная точность" введите число.
    * Укажите количество символов после запятой, до которого должна округляться пересчитанная единица измерения при выполнении вычислений для этой единицы измерения.  
6. Нажмите кнопку "Сохранить".

## <a name="define-unit-translations"></a>Определение переводов для единицы измерения
1. Щелкните "Тексты к единицам измерения".
2. Щелкните "Создать".
    * Используйте текст к единице измерения для создания перевода кода или символа, представляющего единицу измерения, для использования во внешних документах на языках клиентов или поставщиков.  
3. В поле "Язык" введите или выберите значение.
4. В поле "Текст" введите значение.
5. Нажмите кнопку "Сохранить".
6. Закройте страницу.
7. Щелкните "Описания пересчитанных единиц измерения".
8. Щелкните "Создать".
    * Определите описания единицы измерения для конкретных языков.  
9. В поле "Язык" введите или выберите значение.
10. В поле "Описание" введите значение.
11. Нажмите кнопку "Сохранить".
12. Закройте страницу.

## <a name="define-unit-conversion-rules"></a>Определение правил пересчета единицы измерения
1. Щелкните "Пересчеты единиц измерения".
    * Определите правила для пересчета единицы измерения в другие единицы измерения (и из них) в выбранном классе единиц измерения.  
2. Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.
3. В поле "Коэффициент" введите число.
    * Коэффициент пересчета между единицей измерения "Из" и единицей измерения "В". Например, коэффициент пересчета из сантиметров в метры равен 100, потому что в одном метре 100 сантиметров.  
4. В поле "В ед. изм." введите или выберите значение.
5. В поле "Округление" выберите вариант.
    * Определите, как должно округляться пересчитанное значение.  
6. Нажмите кнопку "OК".
7. Закройте страницу.

