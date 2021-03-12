---
title: Синхронизация даты и времени в заданиях импорта
description: Чтобы избежать проблем с преобразованием часового пояса, используйте часовые пояса в формате UTC в заданиях импорта.
author: Sunil-Garg
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae04b09a68e64d6d70c0329e689ab08c3903fca0
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798727"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a><span data-ttu-id="1871c-103">Синхронизация даты и времени в заданиях импорта</span><span class="sxs-lookup"><span data-stu-id="1871c-103">Synchronize date and time in import jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1871c-104">Важно задать для задания импорта часовой пояс с временем в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="1871c-104">It's important to set the time zone for your import job to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="1871c-105">При использовании других настроек в импортируемых данных могут отображаться неправильные даты и время.</span><span class="sxs-lookup"><span data-stu-id="1871c-105">You might see unexpected dates and times in your imported data if you use a different setting.</span></span> <span data-ttu-id="1871c-106">Без правильной настройки процесс импорта преобразует дату в формате UTC в локальный формат, а затем настройки системы снова преобразуют его.</span><span class="sxs-lookup"><span data-stu-id="1871c-106">Without the correct setting, the import process converts the UTC date to the local format, and then system settings converts it again.</span></span>

<span data-ttu-id="1871c-107">Это двойное преобразование приводит к изменению дат между приложениями.</span><span class="sxs-lookup"><span data-stu-id="1871c-107">This dual conversion causes dates to change between applications.</span></span> <span data-ttu-id="1871c-108">Например, двойное преобразование может привести к тому, что дата начала работы сотрудника будет разной в приложениях Dynamics 365 Human Resources и Dynamics 365 Finance в результате разницы в местных часовых поясах.</span><span class="sxs-lookup"><span data-stu-id="1871c-108">For example, the dual conversion could cause an employee's start date to be different between Dynamics 365 Human Resources and Dynamics 365 Finance due to differences in local time zones.</span></span> <span data-ttu-id="1871c-109">Настройка задания импорта в формате UTC разрешает эту проблему.</span><span class="sxs-lookup"><span data-stu-id="1871c-109">Setting the import job to UTC resolves this problem.</span></span>

1. <span data-ttu-id="1871c-110">В Dynamics 365 Finance and Operations выберите **Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="1871c-110">In Dynamics 365 Finance and Operations, select **Data management**.</span></span>

2. <span data-ttu-id="1871c-111">Выберите **Проекты импорта**, затем выберите проект.</span><span class="sxs-lookup"><span data-stu-id="1871c-111">Select **Import projects**, and then select the project.</span></span>

3. <span data-ttu-id="1871c-112">В пункте **Исходный формат даты** выберите **CSV-Unicode**.</span><span class="sxs-lookup"><span data-stu-id="1871c-112">Under **Source date format**, select **CSV-Unicode**.</span></span>

   <span data-ttu-id="1871c-113">[![Изменение исходного формата даты на UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span><span class="sxs-lookup"><span data-stu-id="1871c-113">[![Change source date format to UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span></span>

4. <span data-ttu-id="1871c-114">Измените **Часовой пояс** на **Часовой пояс UTC** и измените **Язык** на **En-US**.</span><span class="sxs-lookup"><span data-stu-id="1871c-114">Change **Timezone** to **Coordinated Universal Timezone**, and change **Language** to **En-US**.</span></span>


