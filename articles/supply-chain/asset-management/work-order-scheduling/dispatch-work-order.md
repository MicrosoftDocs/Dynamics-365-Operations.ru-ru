---
title: Отправка заказа на работу
description: В этом разделе описывается, как отправлять заказы на работу в модуле "Управление активами".
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetScheduledExecution
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bd3bea647698f76efa5831d0b8b34d3cb0ad479a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825550"
---
# <a name="dispatch-work-order"></a>Отправка заказа на работу

[!include [banner](../../includes/banner.md)]

 

Можно запланировать один заказ на работу или задания заказа на работу одному работнику, используя функцию **Подготовить к отправке**.

1. Щелкните **Управление активами** > **Общее** > **Заказы на работу** > **Все заказы на работу** или **Активные заказы на работу**.

2. Выберите заказ на работу в списке.

3. На вкладке **Общие** щелкните **Подготовить к отправке**.

4. В диалоговом окне **Запланировать заказ на работу** выберите работника в поле **Работник**.

5. В поле **Планирование времени** можно вставить ожидаемые рабочие часы в случае, когда количество ожидаемых рабочих часов отличается от прогнозируемых.

6. В поле **Спланированное начало** можно изменить дату и время начала, если необходимо.

7. Если процесс планирования должен учитывать ограничения по мощности для ресурсов, уже запланированных для других заданий, убедитесь, что для переключателей **Актив**, **Инструмент** и **Работник** выбрано значение **Да**. Если требуется просмотреть подробные сведения о процессе планирования, выберите **Да** на переключателе **Подробно**. Это означает, что подробные сведения о расчетных оценках для заказа на работу будут показаны в журнале Infolog.

8. Выберите **Да** на переключателе **Игнорировать расписание**, чтобы игнорировать закрытые дни в календаре (применяется к активу, работнику и инструментам). Выберите **Да** для переключателя **Пропустить запланированное выполнение**, чтобы игнорировать ограничения, которые могли быть выбраны в заказе на работу в отношении планирования. 

    Для получения дополнительных сведений о настройке запланированного выполнения см. в разделе [Запланированное выполнение](../setup-for-work-orders/scheduled-execution.md).

9. Щелкните **OK**. Состояние жизненного цикла заказа на работу автоматически обновляется до состояния жизненного цикла **Запланировано**, указанного в разделе **Управление активами** > **Настройка** > **Заказы на работу** > **Модели жизненного цикла**.

На рисунке, приведенном ниже, показан пример выбора диспетчеризации в диалоговом окне **Планирование заказа на работу**.

![Рисунок 1](media/04-work-order-scheduling.png)

[!NOTE]
Если необходимо удалить график в заказе на работу, выберите заказ на работу в разделе **Все заказы на работу**, и затем нажав **Удалить расписание** на вкладке **Общие**. Не забудьте вручную обновить состояние жизненного цикла заказа на работу, если удалили расписание.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]