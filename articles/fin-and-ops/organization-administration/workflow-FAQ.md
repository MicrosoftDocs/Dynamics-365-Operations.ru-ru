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
# <a name="workflow-system"></a><span data-ttu-id="e3590-103">Система бизнес-правил</span><span class="sxs-lookup"><span data-stu-id="e3590-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3590-104">В этом разделе содержатся ответы на часто задаваемые вопросы о системе workflow-процесса в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e3590-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="e3590-105">Уведомления</span><span class="sxs-lookup"><span data-stu-id="e3590-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="e3590-106">Почему поступает несколько уведомлений при отклонении рабочего элемента?</span><span class="sxs-lookup"><span data-stu-id="e3590-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="e3590-107">При отклонении рабочего элемента этот рабочий элемент завершается как отклоненный.</span><span class="sxs-lookup"><span data-stu-id="e3590-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="e3590-108">Создается другой рабочий элемент и назначается инициатору.</span><span class="sxs-lookup"><span data-stu-id="e3590-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="e3590-109">Это означает, что имеется уведомление инициатору для отклоненного рабочего элемента, а также отдельное уведомление для пользователя, которому назначен новый рабочий элемент "запрошено изменение".</span><span class="sxs-lookup"><span data-stu-id="e3590-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="e3590-110">Каждое уведомление создается для другого рабочего элемента, но сходство может привести к путанице.</span><span class="sxs-lookup"><span data-stu-id="e3590-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="e3590-111">Мы изучаем способы улучшения этого в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="e3590-111">We are looking at ways to improve this in a future release.</span></span>

### <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="e3590-112">Почему происходит сбой экспорта моего рабочего процесса?</span><span class="sxs-lookup"><span data-stu-id="e3590-112">Why are my workflow exports failing?</span></span>
<span data-ttu-id="e3590-113">В данный момент имеется ограничение в функции экспорта рабочего процесса, которое не допускает названия рабочих процессов длиной более 48 знаков.</span><span class="sxs-lookup"><span data-stu-id="e3590-113">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="e3590-114">Использование имени, длина которого превышает 48 знаков, может привести к ошибке "Серверу не удалось выполнить проверку подлинности запроса" и/или к тому, что файл не может быть экспортирован без типа файла.</span><span class="sxs-lookup"><span data-stu-id="e3590-114">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="e3590-115">Следующая запись в блоге содержит дополнительные сведения [об устранении неполадок при экспорте рабочего процесса](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="e3590-115">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>
