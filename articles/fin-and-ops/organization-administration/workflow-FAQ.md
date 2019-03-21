---
title: Вопросы и ответы по workflow-процессу
description: В этом разделе содержатся ответы на часто задаваемые вопросы о системе workflow-процесса в Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/01/2019
ms.locfileid: "773229"
---
# <a name="workflow-system"></a>Система бизнес-правил

[!include [banner](../includes/banner.md)]

В этом разделе содержатся ответы на часто задаваемые вопросы о системе workflow-процесса в Microsoft Dynamics 365 for Finance and Operations.

## <a name="notifications"></a>Уведомления

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Почему поступает несколько уведомлений при отклонении рабочего элемента?
При отклонении рабочего элемента этот рабочий элемент завершается как отклоненный. Создается другой рабочий элемент и назначается инициатору. Это означает, что имеется уведомление инициатору для отклоненного рабочего элемента, а также отдельное уведомление для пользователя, которому назначен новый рабочий элемент "запрошено изменение". 

Каждое уведомление создается для другого рабочего элемента, но сходство может привести к путанице. Мы изучаем способы улучшения этого в будущих выпусках.
