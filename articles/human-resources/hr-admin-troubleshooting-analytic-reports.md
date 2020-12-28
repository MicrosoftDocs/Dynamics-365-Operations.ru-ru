---
title: Устранение неполадок аналитических отчетов
description: В этой статье объясняется, что делать, если изменения данных клиента не отображаются ни в одной из рабочих областей клиента.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
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
ms.openlocfilehash: 99d9eb3a16e6470820a2eb0a19c1d50e89bd3d36
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420273"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="50e1b-103">Устранение неполадок аналитических отчетов</span><span class="sxs-lookup"><span data-stu-id="50e1b-103">Troubleshoot analytic reports</span></span>

<span data-ttu-id="50e1b-104">**Выдать**</span><span class="sxs-lookup"><span data-stu-id="50e1b-104">**Issue**</span></span>

<span data-ttu-id="50e1b-105">Изменения данных клиента не отображаются на вкладках **Аналитики** ни одной из рабочих областей клиента.</span><span class="sxs-lookup"><span data-stu-id="50e1b-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="50e1b-106">**Причина**</span><span class="sxs-lookup"><span data-stu-id="50e1b-106">**Cause**</span></span>

<span data-ttu-id="50e1b-107">По умолчанию отчеты Microsoft Power BI обновляются каждые четыре часа согласно графику пакетного задания развертывания измерения.</span><span class="sxs-lookup"><span data-stu-id="50e1b-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="50e1b-108">**Разрешение**</span><span class="sxs-lookup"><span data-stu-id="50e1b-108">**Resolution**</span></span>

<span data-ttu-id="50e1b-109">Эта проблема может быть просто вопросом времени.</span><span class="sxs-lookup"><span data-stu-id="50e1b-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="50e1b-110">Выполните следующие шаги для запуска пакетного задания и обновления рабочих областей аналитик.</span><span class="sxs-lookup"><span data-stu-id="50e1b-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="50e1b-111">Откройте страницу **Пакетные задания** в меню **Администрирование системы \> Ссылки \> Пакетные задания \> Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="50e1b-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="50e1b-112">Можно также использовать поиск и ввести **Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="50e1b-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="50e1b-113">Найдите в списке задание **Развертывание измерения**.</span><span class="sxs-lookup"><span data-stu-id="50e1b-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="50e1b-114">Выберите **Изменить** в верхней части страницы, и задайте для запланированной даты и времени запуска значение, которое обновит аналитики ближе к текущему времени.</span><span class="sxs-lookup"><span data-stu-id="50e1b-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Пакетные задания](media/batch-jobs.png)
