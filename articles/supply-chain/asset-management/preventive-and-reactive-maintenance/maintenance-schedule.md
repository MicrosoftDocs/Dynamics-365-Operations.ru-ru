---
title: График обслуживания
description: В этом разделе описываются графики обслуживания в управлении активами.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectCalendarCreateWO, EntAssetObjectCalendarListPagePoolsOpen, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePreviewPart, EntAssetObjectCalendarEdit, EntAssetObjectCalendarAdjust, EntAssetObjectCalendarDiscard, EntAssetObjectCalendarInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f7bed45ccf151a2667dcc8dddd5c0586a594ca58
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839591"
---
# <a name="maintenance-schedule"></a>График обслуживания

[!include [banner](../../includes/banner.md)]

 

График обслуживания содержит список всех ожидаемых планов профилактического обслуживания, запросов на обслуживание и циклов обслуживания. Некоторые строки графика могли быть преобразованы в заказы на работу.

Четыре представления графика обслуживания слегка различаются в зависимости от того, какие строки графика обслуживания нужно просмотреть.

| Пункт меню                  | Описание содержимого                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Весь график обслуживания       | Отображаются все строки графика обслуживания.     |
| Мой план активов        | Все строки графика обслуживания, содержащие активы, установленные в функциональных местоположениях, с которыми вы связаны в качестве работника (настраивается в разделе [Специалисты и группы специалистов по обслуживанию](../setup-for-objects/workers-and-worker-groups.md)), отображаются в этом списке. |
| Открытие строки графика обслуживания | В этом списке отображаются строки графика обслуживания со статусом "Создано" — означает, что они еще не преобразованы в заказ на работу или они не были удалены.                                            |
| Открытие пулов графика обслуживания | В этом списке отображаются строки графика обслуживания, имеющие отношение к пулу заказов на работу.                                                                                                                  |

>[!NOTE]
>Если строка графика обслуживания включена в несколько пулов заказов на работу (см. раздел [Пулы заказов на работу](../work-orders/work-order-pools.md)), то для каждого пула в разделе **Открыть пулы графика обслуживания** отображается одна запись. Это сделано для оптимизации параметров фильтрации в пулах заказов на работу.

Чтобы открыть график обслуживания:

1. Щелкните **Управление активами** > **Общее** > **График обслуживания** > **Весь график обслуживания**, **Открыть строки графика обслуживания** или **Открыть пулы графиков обслуживания**.

2. Для обновления графика обслуживания щелкните **План обслуживания** или **Циклы обслуживания**. 

3. Можно изменить строку графика обслуживания, выбрав ее и нажав **Правка**. Например, можно легко обновить уровень обслуживания или сотрудника, ответственного за задание. Можно редактировать только те строки графика обслуживания, которые еще не были связаны с заказом на работу.

4. Можно удалить строку графика обслуживания, выбрав ее на странице списка и нажав **Удалить**.

5. Можно отменить строку графика обслуживания, выбрав ее на странице списка и нажав **Отменить**. Эта функция полезна, если, например, актив имеет план обслуживания 2 000 км и план обслуживания 10 000 км. В этом случае может возникнуть необходимость отменить строку, созданную из плана обслуживания при пробеге 2 000 км, если она совпадает с обслуживанием при пробеге 10 000 км, 20 000 км, 30 000 км и так далее. При отмене строки графика обслуживания, имеющей отношение к плану обслуживания, эта строка никогда не будет больше отображаться при планировании этого плана обслуживания.

6. Можно выбрать несколько строк графика обслуживания в разделе **Все графики обслуживания** и щелкнуть **Пул заказов на работу**, если необходимо включить все выбранные строки в один и тот же пул заказов на работу.

7. Можно выбрать несколько строк графика обслуживания в разделе **Весь график обслуживания** или **Открыть строки графика обслуживания** или **Открыть пулы графиков обслуживания** и щелкнуть **Настроить расписание**, если необходимо выполнить одинаковые коррекции в нескольких строках. Можно изменить ожидаемые даты начала и завершения, уровень обслуживания и группу ответственных специалистов по обслуживанию или ответственного специалиста по обслуживанию для выбранных строк графика обслуживания.

- Когда строка графика обслуживания связана с заказом на работу, код заказа на работу будет отображен в поле **Заказ на работу**.  
- В представлении сведений **Все активы** > на экспресс-вкладке **Планы обслуживания актива** можно выбрать план обслуживания для актива. Если затем вы удалите строку плана обслуживания, связанную с активом в пункте **Все активы**, вы также автоматически удалите все строки графика обслуживания со статусом "Создано", которые были созданы на основе этого плана обслуживания. См. также [Создание актива](../objects/create-an-object.md).

На следующей иллюстрации показана страница списка **Весь график обслуживания**.

![Рисунок 1](media/16-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]