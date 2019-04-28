---
title: Аналитические отчеты не обновляются
description: В этом разделе объясняется, что делать, если изменения данных клиента не отображаются ни в одной из рабочих областей клиента.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d6a6487b50908093f876237ffef840a3144b3fe6
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "857461"
---
# <a name="analytic-reports-are-not-updated"></a><span data-ttu-id="146cf-103">Аналитические отчеты не обновляются</span><span class="sxs-lookup"><span data-stu-id="146cf-103">Analytic reports are not updated</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="146cf-104">**Расход**</span><span class="sxs-lookup"><span data-stu-id="146cf-104">**Issue**</span></span>

<span data-ttu-id="146cf-105">Изменения данных клиента не отображаются на вкладках **Аналитики** ни одной из рабочих областей клиента.</span><span class="sxs-lookup"><span data-stu-id="146cf-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="146cf-106">**Причина**</span><span class="sxs-lookup"><span data-stu-id="146cf-106">**Cause**</span></span>

<span data-ttu-id="146cf-107">По умолчанию отчеты Microsoft Power BI обновляются каждые четыре часа согласно графику пакетного задания развертывания измерения.</span><span class="sxs-lookup"><span data-stu-id="146cf-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="146cf-108">**Разрешение**</span><span class="sxs-lookup"><span data-stu-id="146cf-108">**Resolution**</span></span>

<span data-ttu-id="146cf-109">Эта проблема может быть просто вопросом времени.</span><span class="sxs-lookup"><span data-stu-id="146cf-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="146cf-110">Выполните следующие шаги для запуска пакетного задания и обновления рабочих областей аналитик.</span><span class="sxs-lookup"><span data-stu-id="146cf-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="146cf-111">Откройте страницу **Пакетные задания** в меню **Администрирование системы \> Ссылки \> Пакетные задания \> Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="146cf-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="146cf-112">Можно также использовать поиск и ввести **Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="146cf-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="146cf-113">Найдите в списке задание **Развертывание измерения**.</span><span class="sxs-lookup"><span data-stu-id="146cf-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="146cf-114">Выберите **Изменить** в верхней части страницы, и задайте для запланированной даты и времени запуска значение, которое обновит аналитики ближе к текущему времени.</span><span class="sxs-lookup"><span data-stu-id="146cf-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Пакетные задания](media/batch-jobs.png)
