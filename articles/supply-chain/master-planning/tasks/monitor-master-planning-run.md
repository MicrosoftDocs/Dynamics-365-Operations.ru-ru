---
title: Мониторинг выполнения сводного планирования
description: Планировщик производства хочет просмотреть, выполняется ли сводное планирование.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c2e158d8cbad1f5d4f377f6a8eb43487b34ffdc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565625"
---
# <a name="monitor-a-master-planning-run"></a>Мониторинг выполнения сводного планирования

[!include [task guide banner](../../includes/task-guide-banner.md)]

Планировщик производства хочет просмотреть, выполняется ли сводное планирование. Для выполнения этой процедуры используйте компанию с демонстрационными данными USMF.


## <a name="run-master-planning"></a>Запуск сводного планирования
1. Щелкните "Сводное планирование".
    * Эти сведения можно просмотреть на панели мониторинга по умолчанию.  
2. В поле "План" введите или выберите значение.
    * Пример: StaticPlan  
3. Щелкните "Выполнить".
4. Выберите значение "Да" в поле "Отслеживать время обработки".
    * Если поле уже выбрано, пропустите этот шаг.  
5. В поле "Количество потоков" введите число.
6. Разверните раздел "Записи для добавления".
7. Щелкните "Фильтр".
8. В списке пометьте выбранную строку.
    * Пометьте строку, в которой поле = код номенклатуры.  
9. В поле "Критерии" введите или выберите значение.
    * Пример: T0001  
10. Нажмите кнопку "OК".
11. Нажмите кнопку "OК".

## <a name="monitor-the-master-planning-run"></a>Мониторинг выполнения сводного планирования
1. Щелкните "История".
2. Щелкните Запросы.
3. Щелкните "Длительность задачи процесса".
4. В списке найдите и выберите требуемую запись.
    * Для каждой номенклатуры можно просмотреть, сколько времени необходимого для выполнения каждого шага планирования.  

