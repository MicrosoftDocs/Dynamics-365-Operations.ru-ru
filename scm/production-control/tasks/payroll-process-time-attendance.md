--- 
title: "Включение процесса обработки зарплаты по посещаемости и времени присутствия"
description: "Следующая процедура используется для включения обработки зарплаты по времени присутствия и посещаемости."
author: johanhoffmann
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
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: d83f58f860f64b03c0a27d43e3f0695968d0699b
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a>Включение процесса обработки зарплаты по посещаемости и времени присутствия

[!include[task guide banner](../../includes/task-guide-banner.md)]

Следующая процедура используется для включения обработки зарплаты по времени присутствия и посещаемости. В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.


## <a name="create-a-pay-type-with-a-related-pay-rate"></a>Создание вида оплаты со связанной ставкой оплаты
1. "Посещаемость и время присутствия" > "Настройка" > "Заработная плата" > "Виды оплаты"
2. Щелкните "Создать".
3. В поле "Вид оплаты" введите значение.
4. В поле "Описание" введите значение.
5. Нажмите кнопку "Сохранить".
6. Щелкните "Ставки".
    * Ставки для типов оплаты настраиваются для определенных интервалов времени и для отдельных работников могут быть назначены индивидуальные ставки. Не всегда требуется создать ставки для типов оплаты по времени и посещаемости. Эта информация может уже существовать в системе зарплаты, которая используется для генерирования зарплат.  
7. Щелкните "Создать".
8. В списке пометьте выбранную строку.
9. В поле "Ставка" введите число.
10. Нажмите кнопку "Сохранить".

## <a name="create-a-pay-agreement"></a>Создание соглашения по зарплате
1. Закройте страницу.
2. Закройте страницу.
3. Перейдите в раздел "Соглашения по оплате".
    * "Посещаемость и время присутствия" > "Настройка" > "Соглашения по оплате"  
4. Щелкните "Создать".
5. В поле "Соглашение по оплате" введите значение.
6. В поле "Описание" введите значение.
7. Нажмите кнопку "Сохранить".
8. Щелкните "Строки соглашения".
9. Щелкните "Создать".
10. В списке пометьте выбранную строку.
11. В поле "Тип профиля" введите или выберите значение.
12. В поле "Вид оплаты" введите или выберите значение.

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a>Настройка соглашения по оплате по времени присутствия и регистрации работника
1. Закройте страницу.
2. Закройте страницу.
3. Перейдите в раздел "Регистрация времени - работники".
    * "Посещаемость и время присутствия" > "Настройка" > "Регистрация времени — работники"  
4. В списке перейдите по ссылке в выбранной строке.
5. Перейдите на вкладку "Занятость".
6. Разверните раздел "Регистрация времени".
7. Щелкните "Изменить".
8. В поле "Соглашение по оплате" введите или выберите значение.

