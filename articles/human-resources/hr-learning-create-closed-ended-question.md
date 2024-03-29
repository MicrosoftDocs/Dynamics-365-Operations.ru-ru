---
title: Создание закрытого вопроса
description: Закрытые вопросы позволяют предоставить варианты, из которых респонденту нужно будет выбрать свой ответ.
author: twheeloc
ms.date: 08/26/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 18b755675b97e608afccea2e48ea3cfca74c984f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686173"
---
# <a name="create-a-closed-ended-question"></a>Создание закрытого вопроса


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Закрытые вопросы позволяют предоставить варианты, из которых респонденту нужно будет выбрать свой ответ. Сначала необходимо создать группу ответов с ответами, а затем создать вопрос, в котором будет использоваться группа ответов. В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.


## <a name="create-an-answer-group"></a>Создание группы ответов
1. Перейдите в раздел **Анкета** > **Дизайн** > **Группы ответов**.
2. Нажмите кнопку **Создать**.
3. В поле **Группа ответов** введите значение.
4. В поле **Описание** введите значение.
    * С помощью функциональности **Случайный выбор** можно размещать ответы в новом случайном порядке всякий раз, когда группа ответов используется для вопроса.  
5. Щелкните **Ответ**.
6. Нажмите кнопку **Создать**.
    * Порядковый номер определяет порядок, в котором отображаются ответы, кроме случаев, когда для **группы ответов** выбран параметр **Случайный выбор**.  
    * Ответам могут быть присвоены баллы для использования при оценке анкеты.  
7. В поле **Баллы** введите число.
    * Правильный ответ можно пометить, чтобы указать, что выбранный ответ является правильным. Это можно использовать для оценки анкеты.  
8. В поле **Ответ** введите значение.
    * Продолжайте создавать варианты для выбора ответа для группы ответов.  
9. Нажмите кнопку **Создать**.
10. В поле **Баллы** введите число.
11. В поле **Ответ** введите значение.
12. Нажмите кнопку **Создать**.
13. В поле **Баллы** введите число.
14. В поле **Ответ** введите значение.
15. Нажмите кнопку **Создать**.
16. В поле **Баллы** введите число.
17. В поле **Ответ** введите значение.
18. Нажмите кнопку **Создать**.
19. В поле **Баллы** введите число.
20. В поле **Ответ** введите значение.
21. Закройте страницу.
22. Закройте страницу.

## <a name="create-the-question"></a>Создание вопроса
1. Перейдите в раздел **Анкета** > **Дизайн** > **Вопросы**.
2. Нажмите кнопку **Создать**.
3. С помощью поля **Тип** связанные вопросы можно сгруппировать вместе.
    * Для закрытых вопросов можно использовать типы ввода **Флажок**, **Переключатель** или **Поле со списком**.  
4. В поле **Тип ввода** выберите один из вариантов.
5. В поле **Группа ответов** введите или выберите значение.
6. В поле **Текст** введите значение.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
