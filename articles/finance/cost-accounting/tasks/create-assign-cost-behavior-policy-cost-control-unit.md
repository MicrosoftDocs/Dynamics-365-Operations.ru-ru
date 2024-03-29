---
title: Создание и назначение политик поведения затрат единицам управления затратами
description: Поведение затрат представляет собой отнесение затрат к постоянным или переменным.
author: twheeloc
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 653bfb69c4ca118c700755cb95a6b349d2c6bbad
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735152"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a>Создание и назначение политик поведения затрат единицам управления затратами

[!include [banner](../../includes/banner.md)]

Поведение затрат представляет собой отнесение затрат к постоянным или переменным. Для вступления политики в силу политика и соответствующие правила должны быть назначены единице управления затратами. Эта процедура используется для создания политики и ее назначения единице управления затратами.


## <a name="create-a-cost-behavior-hierarchy"></a>Создание иерархии поведения затрат
1. Перейдите в раздел **Учет затрат > Аналитики > Иерархии аналитик**.
2. Нажмите кнопку **Создать**.
3. Щелкните **Создать**.
4. В поле **Имя иерархии аналитик** введите «Иерархия поведения затрат».
5. В поле **Аналитика** введите или выберите значение.
    * Выберите "Элементы затрат".  
6. Нажмите кнопку **Сохранить**.
7. Щелкните **Просмотр иерархии**.
8. Нажмите кнопку **Создать**.
9. В поле **Имя узла** введите значение.
    * Введите "Постоянные затраты".  
10. В дереве выберите "Иерархия поведения затрат".
11. Нажмите кнопку **Создать**.
12. В поле **Имя узла** введите значение.
    * Введите "Переменные затраты".  
13. Нажмите кнопку **Сохранить**.
14. В дереве выберите "Иерархия поведения затрат\Постоянные затраты".
15. Нажмите кнопку **Создать**.
16. В списке пометьте выбранную строку.
17. В поле **Из элемента аналитики** введите или выберите значение.
    * Диапазон элементов аналитики может содержать промежутки, но элементы не могут перекрываться.  
18. В поле **В элемент аналитики** введите или выберите значение.
    * Диапазон элементов аналитики может содержать промежутки, но элементы не могут перекрываться.  
19. В дереве выберите "Иерархия поведения затрат\Переменные затраты".
20. Нажмите кнопку **Создать**.
21. В списке пометьте выбранную строку.
22. В поле **Из элемента аналитики** введите или выберите значение.
    * Диапазон элементов аналитики может содержать промежутки, но элементы не могут перекрываться.  
23. В поле **В элемент аналитики** введите или выберите значение.
    * Диапазон элементов аналитики может содержать промежутки, но элементы не могут перекрываться.  
24. Нажмите кнопку **Сохранить**.

## <a name="create-the-policy-and-rules"></a>Создание политики и правил
1. Перейдите в раздел **Учет затрат > Политики > Политики поведения затрат**.
2. Нажмите кнопку **Создать**.
3. В поле **Имя политики** введите значение.
4. В поле **Иерархия аналитик элементов затрат** введите или выберите значение.
    * Выберите только что созданную иерархию политик.  
5. В поле **Иерархия аналитик объектов затрат** введите или выберите значение.
    * Выберите "Организация".  
6. Нажмите кнопку **Сохранить**.
7. Нажмите кнопку **Создать**.
8. В списке пометьте выбранную строку.
9. В поле **Узел иерархии аналитик элементов затрат** введите или выберите значение.
    * Разверните иерархию, чтобы выбрать "Переменные затраты".  
10. В поле **Узел иерархии аналитик объектов затрат** введите или выберите значение.
    * По умолчанию процент переменной части равен 100%.  
11. Щелкните **Назначения политики для единицы управления затратами**.
12. Нажмите кнопку **Создать**.
13. В списке пометьте выбранную строку.
14. В поле **Действительно с даты учета** введите дату.
    * Правила вступают в силу по дате, и пользователь или система могут пометить правило как правило с истекшим сроком действия, если создана более новая версия.  
15. В поле **Единица управления затратами** введите или выберите значение.
16. Нажмите кнопку **Сохранить**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
