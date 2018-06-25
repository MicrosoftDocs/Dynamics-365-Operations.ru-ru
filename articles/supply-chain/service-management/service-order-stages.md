---
title: "Этапы заказа на обслуживание"
description: "Определив стадии заказа на сервисное обслуживание и назначив их работникам, можно управлять ходом выполнения заказа на сервисное обслуживание с помощью задач, которые выполняются различными работниками в сервисной организации."
author: YuyuScheller
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9aa90dfcfc4b30d6cb4fa7ed4e6faaf505548d41
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="service-order-stages"></a>Этапы заказа на обслуживание   

[!include [banner](../includes/banner.md)]


Можно настроить стадии заказа на сервисное обслуживание, чтобы определить задачи, которые должны быть выполнены, порядок их выполнения и работников, ответственных за их выполнение. Определив стадии заказа на сервисное обслуживание и назначив их работникам, можно управлять ходом выполнения заказа на сервисное обслуживание с помощью задач, которые выполняются различными работниками в сервисной организации. Последовательность стадий должна включать начальную стадию.

Можно также указать действия, которые можно выполнять на каждой стадии. Например, если снять флажок **Разнести** для всех стадий кроме финальной, заказы на сервисное облуживание будет невозможно разнести, пока не будут пройдены все стадии в последовательности.

## <a name="branching-in-service-order-stages"></a>Ветвление на стадиях заказа на сервисное обслуживание

При настройке стадии сервисного обслуживания можно создать несколько вариантов или ветвей, которые можно выбрать для перехода на следующую стадию сервисного обслуживания. Все созданные ветви будут доступны для выбора по завершении начальной стадии. Например, назначьте стадию **Планирование** как начальную стадию. Создайте две стадии **В работе** и **Отмена** и выберите **Планирование** как родительский объект для них. Назначьте стадию **Планирование** заказу на продажу. По завершении стадии планирования для заказа на продажу можно выбрать стадию **В работе**, если заказ на продажу готов к работе, или стадию **Отмена**, если заказ на продажу отменен.

## <a name="see-also"></a>См. также

[Настройка этапов заказа на обслуживания](set-up-service-order-stages.md)

[Изменение этапа заказа на обслуживание](change-service-order-stage.md)

  


