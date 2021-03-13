---
title: Устранение неполадок аналитических отчетов
description: В этой статье объясняется, что делать, если изменения данных клиента не отображаются ни в одной из рабочих областей клиента.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: c5e1a1d7044567a07acedf71e65ed244275acfd9
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114004"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="1106e-103">Устранение неполадок аналитических отчетов</span><span class="sxs-lookup"><span data-stu-id="1106e-103">Troubleshoot analytic reports</span></span>

<span data-ttu-id="1106e-104">**Выдать**</span><span class="sxs-lookup"><span data-stu-id="1106e-104">**Issue**</span></span>

<span data-ttu-id="1106e-105">Изменения данных клиента не отображаются на вкладках **Аналитики** ни одной из рабочих областей клиента.</span><span class="sxs-lookup"><span data-stu-id="1106e-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="1106e-106">**Причина**</span><span class="sxs-lookup"><span data-stu-id="1106e-106">**Cause**</span></span>

<span data-ttu-id="1106e-107">По умолчанию отчеты Microsoft Power BI обновляются каждые четыре часа согласно графику пакетного задания развертывания измерения.</span><span class="sxs-lookup"><span data-stu-id="1106e-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="1106e-108">**Разрешение**</span><span class="sxs-lookup"><span data-stu-id="1106e-108">**Resolution**</span></span>

<span data-ttu-id="1106e-109">Эта проблема может быть просто вопросом времени.</span><span class="sxs-lookup"><span data-stu-id="1106e-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="1106e-110">Выполните следующие шаги для запуска пакетного задания и обновления рабочих областей аналитик.</span><span class="sxs-lookup"><span data-stu-id="1106e-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="1106e-111">Откройте страницу **Пакетные задания** в меню **Администрирование системы \> Ссылки \> Пакетные задания \> Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="1106e-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="1106e-112">Можно также использовать поиск и ввести **Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="1106e-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="1106e-113">Найдите в списке задание **Развертывание измерения**.</span><span class="sxs-lookup"><span data-stu-id="1106e-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="1106e-114">Выберите **Изменить** в верхней части страницы, и задайте для запланированной даты и времени запуска значение, которое обновит аналитики ближе к текущему времени.</span><span class="sxs-lookup"><span data-stu-id="1106e-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Пакетные задания](media/batch-jobs.png)
