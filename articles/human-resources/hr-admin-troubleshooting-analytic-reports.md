---
title: Устранение неполадок аналитических отчетов
description: В этой статье объясняется, что делать, если изменения данных клиента не отображаются ни в одной из рабочих областей клиента.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b500d519d61edfd20456355376e3fc81f16517a0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794981"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="1b24a-103">Устранение неполадок аналитических отчетов</span><span class="sxs-lookup"><span data-stu-id="1b24a-103">Troubleshoot analytic reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1b24a-104">**Выдать**</span><span class="sxs-lookup"><span data-stu-id="1b24a-104">**Issue**</span></span>

<span data-ttu-id="1b24a-105">Изменения данных клиента не отображаются на вкладках **Аналитики** ни одной из рабочих областей клиента.</span><span class="sxs-lookup"><span data-stu-id="1b24a-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="1b24a-106">**Причина**</span><span class="sxs-lookup"><span data-stu-id="1b24a-106">**Cause**</span></span>

<span data-ttu-id="1b24a-107">По умолчанию отчеты Microsoft Power BI обновляются каждые четыре часа согласно графику пакетного задания развертывания измерения.</span><span class="sxs-lookup"><span data-stu-id="1b24a-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="1b24a-108">**Разрешение**</span><span class="sxs-lookup"><span data-stu-id="1b24a-108">**Resolution**</span></span>

<span data-ttu-id="1b24a-109">Эта проблема может быть просто вопросом времени.</span><span class="sxs-lookup"><span data-stu-id="1b24a-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="1b24a-110">Выполните следующие шаги для запуска пакетного задания и обновления рабочих областей аналитик.</span><span class="sxs-lookup"><span data-stu-id="1b24a-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="1b24a-111">Откройте страницу **Пакетные задания** в меню **Администрирование системы \> Ссылки \> Пакетные задания \> Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="1b24a-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="1b24a-112">Можно также использовать поиск и ввести **Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="1b24a-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="1b24a-113">Найдите в списке задание **Развертывание измерения**.</span><span class="sxs-lookup"><span data-stu-id="1b24a-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="1b24a-114">Выберите **Изменить** в верхней части страницы, и задайте для запланированной даты и времени запуска значение, которое обновит аналитики ближе к текущему времени.</span><span class="sxs-lookup"><span data-stu-id="1b24a-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Пакетные задания](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]