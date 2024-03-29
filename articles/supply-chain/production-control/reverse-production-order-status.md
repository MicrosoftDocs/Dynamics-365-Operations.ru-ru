---
title: Отмена статуса производственного заказа
description: Эта статья описывает, как обратить статус производственного заказа.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdParmStatusDecrease, ProdSetupStatusDecrease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 70131
ms.assetid: b1e0df43-b388-4326-8fb7-501f30c89776
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d50cbcb4031d5c9f2c814883afd1fb38777d2ba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903966"
---
# <a name="reverse-the-production-order-status"></a>Отмена статуса производственного заказа

[!include [banner](../includes/banner.md)]

Эта статья описывает, как обратить статус производственного заказа. 

При реверсировании статуса производственного заказа сам заказ и все связанные с маршрутами операции возвращаются на предыдущий шаг жизненного цикла производства. Например, производственный заказ имеет статус **Запланировано**, и вы изменяете статус назад на **Создано**. В этом случае система должна сперва изменить статус на **Оценено**, который непосредственно предшествует статусу **Запланировано**. Затем он может изменить статус на требуемый статус **Создано**. **Примечание.** Если заказ получил статус **Приемка**, но его необходимо реверсировать на более раннюю стадию, это также можно сделать. Однако в этом случае необходимо заново произвести оценку и планирование операций или задания (или оба этих вида планирования), чтобы обновить сведения в заказе. Этот шаг обязателен, так как необходимо также сбросить данные потребления номенклатур и операционных ресурсов. В оставшейся части статьи объясняется, что происходит при реверсировании статуса следующими способами.

-   От статуса **Оценено** до статуса **Создано**
-   От статуса **Запланировано** до статуса **Оценено**
-   От статуса **Запущено в производство** до статуса **Запланировано**
-   От статуса **Начато** до статуса **Запущено в производство**

## <a name="from-estimated-to-created"></a>От статуса "Оценено" до статуса "Создано"
Когда вы обращаете статус производственного заказа с **Оценено** на **Создано**, потребление номенклатур, которое было высчитано для номенклатур в спецификации, удаляется. Складские проводки в строке производства удаляются, а поле **Статус недопоставленного** в строках спецификации производственного заказа сбрасывается в значение **Завершено**. Если выбраны параметры **Производные покупки** и **Производное производство**, нижележащие заказы на покупку или производственные заказы удаляются. Если производилась оценка стоимости производственного заказа или вручную резервировались номенклатуры, чтобы их можно было использовать в производстве, эти проводки удаляются.

## <a name="from-scheduled-to-estimated"></a>От статуса "Запланировано" до статуса "Оценено"
При реверсировании статуса производственного заказа с **Запланировано** на **Оценено** удаляются спланированные даты и время начала и окончания. Отменяется также резервирование мощностей, выполненное при планировании, и удаляются задания, созданные в процессе планирования заданий. Сбрасывается вся записанная информация о планировании операций и планировании заданий на странице **Сведения о производственном заказе**.

## <a name="from-released-to-scheduled"></a>От статуса "Запущено в производство" до статуса "Запланировано"
При реверсировании статуса производственного заказа от **Запущено в производство** до **Запланировано** изменяется только значение в поле статуса.

## <a name="from-started-to-released"></a>От статуса "Начато" до статуса "Запущено в производство"
При реверсировании статуса производственного заказа от **Начато** до **Запущено в производство** все номенклатуры, учтенные как принятые, также реверсируются. Если была произведена комплектация материалов или существуют входящие либо исходящие поставки в производство, реверсирование этих параметров также выполняется. Поле **Статус недопоставленного** в строках спецификаций производственного заказа изменяется с **Завершено** на **Материальное потребление**. Если для операций в маршруте производства производилась регистрация времени или количеств как завершенных, эти настройки также реверсируются. Поле **Статус недопоставленного** изменяется с **Завершено** на **Потребление на маршруте** в маршруте производства. Параметры для всех номенклатур, разнесенных как обрабатываемые или незавершенное производство, реверсируются. На странице **Сведения о производственном заказе** поля, которые показывают количество, которое было начато или принято, также сбрасываются. Даты для тех проводок также сбрасываются.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]