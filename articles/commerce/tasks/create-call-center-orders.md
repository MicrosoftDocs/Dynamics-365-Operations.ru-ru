---
title: Создание заказов центра обработки вызовов
description: Эта процедура демонстрирует поиск клиента, создание нового заказа, поиск продукта и получение платежа от клиента.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1675d21f1e4176839feace76359afdbdc336c99
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023806"
---
# <a name="create-call-center-orders"></a>Создание заказов центра обработки вызовов

[!include[task guide banner](../includes/task-guide-banner.md)]

Эта процедура демонстрирует поиск клиента, создание нового заказа, поиск продукта и получение платежа от клиента. Эта процедура использует демонстрационные данные компании USRT и предназначена для сотрудника, занимающегося заказами на продажу. Предварительные условия: пользователь, выполняющий эту процедуру, настроен как пользователь центра обработки вызовов, и полугодовой каталог Fabrikam опубликован и содержит по крайней мере один исходный код.

1. Перейдите в раздел "Retail и Commerce" > "Клиенты" > "Обслуживание клиентов".
2. В поле SearchText введите условия поиска для поиска клиента.
    * Для этой демонстрационной процедуры введите "karen" и нажмите TAB.  
3. Щелкните "Поиск".
    * Поскольку в демонстрационных данных есть только один клиент с именем Karen, он будет выбран автоматически.  
4. Щелкните "Новый заказ на продажу".
5. Разверните или сверните раздел "Заголовок заказа на продажу".
6. Выберите код источника для каталога
    * Если нет активных кодов источника, можно закрыть поле "Источник" и пропустить этот шаг.  
7. Щелкните "Добавить строку".
8. В поле "Код номенклатуры" введите поисковый запрос для номенклатуры.
    * Для этой демонстрационной процедуры введите частичный код номенклатуры "8111" и нажмите TAB. Появится окно поиска номенклатуры.  
9. Выберите продукта для добавления в заказ на продажу.
10. Введите количество продаваемого продукта.
11. Щелкните Создать.
12. Щелкните "Завершить", чтобы зафиксировать платеж клиента.
13. Нажмите кнопку Добавить.
    * Команда "Добавить ссылку" находится на вкладке "Платежи". Разверните вкладку "Платежи", если она свернута.  
14. Выберите способ оплаты.
    * Для этой процедуры выберите способ оплаты наличными.  
15. Закройте страницу.
16. Введите сумму.
    * Для этой процедуры введите сумму, равную сальдо заказа, которую можно видеть на странице сводке заказ на продажу слева от поля суммы. Это позволит вам завершить заказ как полностью оплаченный.  
17. Нажмите кнопку "OК".
18. Щелкните Отправить.
