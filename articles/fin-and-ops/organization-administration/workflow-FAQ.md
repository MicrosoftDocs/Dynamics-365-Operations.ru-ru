---
title: Вопросы и ответы по workflow-процессу
description: В этом разделе содержатся ответы на часто задаваемые вопросы о системе workflow-процесса в Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509299"
---
# <a name="workflow-system"></a>Система бизнес-правил

[!include [banner](../includes/banner.md)]

В этом разделе содержатся ответы на часто задаваемые вопросы о системе workflow-процесса в Microsoft Dynamics 365 for Finance and Operations.

## <a name="notifications"></a>Уведомления

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Почему поступает несколько уведомлений при отклонении рабочего элемента?
При отклонении рабочего элемента этот рабочий элемент завершается как отклоненный. Создается другой рабочий элемент и назначается инициатору. Это означает, что имеется уведомление инициатору для отклоненного рабочего элемента, а также отдельное уведомление для пользователя, которому назначен новый рабочий элемент "запрошено изменение". 

Каждое уведомление создается для другого рабочего элемента, но сходство может привести к путанице. Мы изучаем способы улучшения этого в будущих выпусках.

### <a name="why-are-my-workflow-exports-failing"></a>Почему происходит сбой экспорта моего рабочего процесса?
В данный момент имеется ограничение в функции экспорта рабочего процесса, которое не допускает названия рабочих процессов длиной более 48 знаков. Использование имени, длина которого превышает 48 знаков, может привести к ошибке "Серверу не удалось выполнить проверку подлинности запроса" и/или к тому, что файл не может быть экспортирован без типа файла. Следующая запись в блоге содержит дополнительные сведения [об устранении неполадок при экспорте рабочего процесса](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).
