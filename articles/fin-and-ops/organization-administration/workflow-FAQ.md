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
# <a name="workflow-system"></a><span data-ttu-id="ef724-103">Система бизнес-правил</span><span class="sxs-lookup"><span data-stu-id="ef724-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef724-104">В этом разделе содержатся ответы на часто задаваемые вопросы о системе workflow-процесса в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ef724-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="ef724-105">Уведомления</span><span class="sxs-lookup"><span data-stu-id="ef724-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="ef724-106">Почему поступает несколько уведомлений при отклонении рабочего элемента?</span><span class="sxs-lookup"><span data-stu-id="ef724-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="ef724-107">При отклонении рабочего элемента этот рабочий элемент завершается как отклоненный.</span><span class="sxs-lookup"><span data-stu-id="ef724-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="ef724-108">Создается другой рабочий элемент и назначается инициатору.</span><span class="sxs-lookup"><span data-stu-id="ef724-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="ef724-109">Это означает, что имеется уведомление инициатору для отклоненного рабочего элемента, а также отдельное уведомление для пользователя, которому назначен новый рабочий элемент "запрошено изменение".</span><span class="sxs-lookup"><span data-stu-id="ef724-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="ef724-110">Каждое уведомление создается для другого рабочего элемента, но сходство может привести к путанице.</span><span class="sxs-lookup"><span data-stu-id="ef724-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="ef724-111">Мы изучаем способы улучшения этого в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="ef724-111">We are looking at ways to improve this in a future release.</span></span>
