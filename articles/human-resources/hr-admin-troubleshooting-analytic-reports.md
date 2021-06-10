---
title: Устранение неполадок аналитических отчетов
description: В этой статье объясняется, что делать, если изменения данных клиента не отображаются ни в одной из рабочих областей клиента.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8dab12213e9730e72aede70c5b5d1368ef77664e
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053547"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="0d0bb-103">Устранение неполадок аналитических отчетов</span><span class="sxs-lookup"><span data-stu-id="0d0bb-103">Troubleshoot analytic reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0d0bb-104">**Выдать**</span><span class="sxs-lookup"><span data-stu-id="0d0bb-104">**Issue**</span></span>

<span data-ttu-id="0d0bb-105">Изменения данных клиента не отображаются на вкладках **Аналитики** ни одной из рабочих областей клиента.</span><span class="sxs-lookup"><span data-stu-id="0d0bb-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="0d0bb-106">**Причина**</span><span class="sxs-lookup"><span data-stu-id="0d0bb-106">**Cause**</span></span>

<span data-ttu-id="0d0bb-107">По умолчанию отчеты Microsoft Power BI обновляются каждые четыре часа согласно графику пакетного задания развертывания измерения.</span><span class="sxs-lookup"><span data-stu-id="0d0bb-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="0d0bb-108">**Разрешение**</span><span class="sxs-lookup"><span data-stu-id="0d0bb-108">**Resolution**</span></span>

<span data-ttu-id="0d0bb-109">Эта проблема может быть просто вопросом времени.</span><span class="sxs-lookup"><span data-stu-id="0d0bb-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="0d0bb-110">Выполните следующие шаги для запуска пакетного задания и обновления рабочих областей аналитик.</span><span class="sxs-lookup"><span data-stu-id="0d0bb-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="0d0bb-111">Откройте страницу **Пакетные задания** в меню **Администрирование системы \> Ссылки \> Пакетные задания \> Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="0d0bb-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="0d0bb-112">Можно также использовать поиск и ввести **Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="0d0bb-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="0d0bb-113">Найдите в списке задание **Развертывание измерения**.</span><span class="sxs-lookup"><span data-stu-id="0d0bb-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="0d0bb-114">Выберите **Изменить** в верхней части страницы, и задайте для запланированной даты и времени запуска значение, которое обновит аналитики ближе к текущему времени.</span><span class="sxs-lookup"><span data-stu-id="0d0bb-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Пакетные задания](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]