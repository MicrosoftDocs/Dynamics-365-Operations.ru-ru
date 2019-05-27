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
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518975"
---
# <a name="analytic-reports-are-not-updated"></a><span data-ttu-id="17766-103">Аналитические отчеты не обновляются</span><span class="sxs-lookup"><span data-stu-id="17766-103">Analytic reports are not updated</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="17766-104">**Расход**</span><span class="sxs-lookup"><span data-stu-id="17766-104">**Issue**</span></span>

<span data-ttu-id="17766-105">Изменения данных клиента не отображаются на вкладках **Аналитики** ни одной из рабочих областей клиента.</span><span class="sxs-lookup"><span data-stu-id="17766-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="17766-106">**Причина**</span><span class="sxs-lookup"><span data-stu-id="17766-106">**Cause**</span></span>

<span data-ttu-id="17766-107">По умолчанию отчеты Microsoft Power BI обновляются каждые четыре часа согласно графику пакетного задания развертывания измерения.</span><span class="sxs-lookup"><span data-stu-id="17766-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="17766-108">**Разрешение**</span><span class="sxs-lookup"><span data-stu-id="17766-108">**Resolution**</span></span>

<span data-ttu-id="17766-109">Эта проблема может быть просто вопросом времени.</span><span class="sxs-lookup"><span data-stu-id="17766-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="17766-110">Выполните следующие шаги для запуска пакетного задания и обновления рабочих областей аналитик.</span><span class="sxs-lookup"><span data-stu-id="17766-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="17766-111">Откройте страницу **Пакетные задания** в меню **Администрирование системы \> Ссылки \> Пакетные задания \> Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="17766-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="17766-112">Можно также использовать поиск и ввести **Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="17766-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="17766-113">Найдите в списке задание **Развертывание измерения**.</span><span class="sxs-lookup"><span data-stu-id="17766-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="17766-114">Выберите **Изменить** в верхней части страницы, и задайте для запланированной даты и времени запуска значение, которое обновит аналитики ближе к текущему времени.</span><span class="sxs-lookup"><span data-stu-id="17766-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Пакетные задания](media/batch-jobs.png)
