--- 
title: "Ввод и сравнение предложений по запросу предложения и заключение контрактов"
description: "В этой процедуре показано, как ввести ответы на запрос предложения, поставить оценку и сравнить предложения, а затем присудить предложение одному из поставщиков."
author: mkirknel
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d7c76eab2cca4e15c13dd9f79432b9c6d81071a2
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>Ввод и сравнение предложений по запросу предложения и заключение контрактов

[!include[task guide banner](../../includes/task-guide-banner.md)]

В этой процедуре показано, как ввести ответы на запрос предложения, поставить оценку и сравнить предложения, а затем присудить предложение одному из поставщиков. Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF. Перед началом работы необходимо иметь запрос предложения с двумя строками, которое было отправлено хотя бы двум поставщикам. Можно выполнить процедуру "Создание запроса предложения" как необходимое условие для их создания. Перед выполнением этой процедуры необходимо настроить критерии оценки.


## <a name="enter-a-reply-from-a-vendor"></a>Ввод ответа поставщика
1. Перейдите в раздел "Закупки и источники" > "Запросы предложений" > "Все запросы предложений".
2. Выберите запрос предложения со статусом "Отправлено" и перейдите по ссылке в номере обращения "Запрос предложения".
    * Запрос предложения необходимо было отправить хотя бы 2 поставщикам.  
3. Щелкните заголовок, чтобы перейти к списку поставщиков.
4. Выберите поставщика, для которого требуется ввести ответ на запрос предложения.
5. Щелкните "Введите ответ".
6. В области действий щелкните "Ответ".
7. Щелкните "Копировать данные в ответ".
    * В результате этого действия будут скопированы выбранные данные, например количество из обращения по запросу предложения в ответ на запрос предложения. Либо можно пропустить это действие и заполнить все поля ответа вручную при изменении ответа.  
8. Щелкните "Изменить".
9. В поле "Цена за единицу" введите число.
10. Выберите другую строку предложения.
11. В поле "Цена за единицу" введите число.

## <a name="score-the-bid"></a>Оценка предложения
1. Щелкните заголовок, чтобы перейти к оценке предложения.
2. Разверните раздел "Оценка предложения".
3. В поле "Оценка" введите число для одного из критериев оценки.
    * При наведении указателя мыши на один из критериев оценки отобразится подсказка с диапазоном оценки. В этой демонстрации можно добавить число от 1 до 5 к любым критериям.  
4. Выберите другой критерий оценки.
5. В поле "Оценка" введите число.
6. Разверните раздел "Анкеты".
    * Если обращение по запросу предложения содержит анкету, которая была отправлена поставщикам, можно ввести их ответы в разделе анкеты.  
7. Закройте страницу.

## <a name="enter-a-reply-for-another-vendor"></a>Ввод ответа для другого поставщика
1. Выберите следующего поставщика, очистив поставщика, для которого только что был введен ответ, а затем выберите строку для следующего поставщика.
2. В списке найдите и выберите требуемую запись.
3. Щелкните "Введите ответ".
4. Щелкните "Копировать данные в ответ".
5. Щелкните "Изменить".
6. В поле "Цена за единицу" введите число.
7. Выберите другую строку предложения.
8. В поле "Цена за единицу" введите число.

## <a name="score-the-second-bid"></a>Оценка второго предложения
1. Щелкните заголовок, чтобы перейти к оценке предложения.
2. В поле "Оценка" введите число.
3. В списке найдите и выберите требуемую запись.
4. В поле "Оценка" введите число.

## <a name="compare-the-replies"></a>Сравнить ответы
1. В области действий щелкните "Общие".
2. Щелкните "Сравнить ответы".
3. В поле "Ранг" введите число.
    * На этой странице отображаются предложения с заголовком и строками, а также общая оценка на уровне заголовка. Вы можете сравнить строки, отсортировав их в сетке так, чтобы соответствующие строки располагались рядом друг с другом. Информация также включает:    Количество — количество, указанное поставщиком. Это количество может не совпадать с количеством, указанным в запросе предложения.   Чистая сумма — цена, указанная поставщиком после вычета всех скидок, для элементов строки.   Отклонение — количество дней, на которое дата поставки в строке или заголовке предложения отличается от запрошенной даты поставки, указанной в строке или заголовке запроса предложения.   Можно ввести ранг для каждого предложения.  
4. Выберите строку заголовка для другого предложения, которое требуется ранжировать.
5. В поле "Ранг" введите число.
6. Нажмите кнопку "Сохранить".

## <a name="reject-a-bid"></a>Отклонить предложение
1. Выберите строку заголовка для предложения, которое требуется отклонить.
    * Одновременно можно принять, отклонить или вернуть только одно предложение или строки в пределах одного предложения.  
2. Установите флажок "Пометка".
    * Если установить флажок "Пометить" в заголовке предложения, также будут помечены все строки. Также можно пометить подмножество строк в пределах предложения, чтобы отклонить или принять их. Можно принять одно предложение поставщика для определенных строк запроса предложения, а затем передать другие строки запроса предложения другому поставщику. Однако это необходимо выполнить за 2 шага, одно предложение за раз. Если присутствуют альтернативные строки, можно принять только исходную строку предложения или только альтернативные строки, но не оба типа строк одновременно.  
3. Щелкните "Отклонить".
4. Щелкните "Параметры", чтобы открыть раскрывающееся диалоговое окно.
5. В поле "Причина отклонения" введите или выберите значение.
    * Причина отклонения будет сохранена в ответе.  
6. Нажмите кнопку "OК".
7. Нажмите кнопку "OК".
8. Закройте страницу.
9. Закройте страницу.
10. Обновите страницу.

## <a name="accept-a-bid"></a>Принять предложение
1. Выберите предложение, которое требуется принять, и перейдите по ссылке в поле "Запрос предложения".
2. В области действий щелкните "Ответ".
3. Щелкните "Принять".
    * Если имеются помеченные строки, но не другие строки, действие принятия будет содержать только помеченные строки. Если требуется принять все строки в предложении, не следует помечать строки.  
4. Щелкните "Параметры", чтобы открыть раскрывающееся диалоговое окно.
    * Это позволяет записать причину принятия заявки. Причина будет сохранена в предложении.  
5. В поле "Причина принятия" введите или выберите значение.
6. Нажмите кнопку "OК".
7. Нажмите кнопку "OК".
    * При нажатии кнопки ОК создается заказ на покупку на основе строк, включенных в принятый запрос предложения. Если имеются другие предложения, которые не были обработаны (принято, отклонено или возвращено), система выдаст запрос на отклонение оставшихся предложений.  

## <a name="view-the-purchase-order-thats-been-generated"></a>Просмотр созданного заказа на покупку
1. В области действий щелкните "Общие".
2. Щелкните "Заказ на покупку".
    * Здесь можно просмотреть заказ на покупку, созданный при принятии предложения.  
3. Закройте страницу.
4. Закройте страницу.
5. Закройте страницу.
6. Закройте страницу.

