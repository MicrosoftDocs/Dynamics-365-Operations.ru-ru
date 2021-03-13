---
title: Настройка разделителя плана счетов как уникального
description: В этой теме объясняется, как не допускается одинаковый разделитель для плана счетов и значений аналитик. После обновления необходимо изменить значения разделителя.
author: panolte
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 72965e9c6182bdac123feb1bc5cc4b82d91cd588
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020112"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a><span data-ttu-id="dc8a9-104">Настройка разделителя плана счетов как уникального</span><span class="sxs-lookup"><span data-stu-id="dc8a9-104">Make the chart of accounts delimiter unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc8a9-105">В Microsoft Dynamics AX 2012 можно использовать одинаковые разделителя для вашего плана счетов и значений аналитик.</span><span class="sxs-lookup"><span data-stu-id="dc8a9-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="dc8a9-106">В текущих версиях Finance and Operations не допускается одинаковый разделитель для плана счетов и значений аналитик.</span><span class="sxs-lookup"><span data-stu-id="dc8a9-106">In current versions of Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="dc8a9-107">Если имеется дублирующий разделитель, его можно изменить после обновления.</span><span class="sxs-lookup"><span data-stu-id="dc8a9-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="dc8a9-108">Эта функция доступна в следующих версиях:</span><span class="sxs-lookup"><span data-stu-id="dc8a9-108">This feature is available in the following versions:</span></span>
- <span data-ttu-id="dc8a9-109">Finance and Operations версии 8.0</span><span class="sxs-lookup"><span data-stu-id="dc8a9-109">Finance and Operations version 8.0</span></span>
- <span data-ttu-id="dc8a9-110">Finance and Operations версии 7.1, KB 4094701, Невозможно ввести финансовые аналитики, когда значения аналитики содержат разделитель плана счетов</span><span class="sxs-lookup"><span data-stu-id="dc8a9-110">Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="dc8a9-111">Finance and Operations версии 7.2, KB 4092967 Невозможно выбрать подпроект как аналитику, когда формат подпроекта содержит разделитель аналитики</span><span class="sxs-lookup"><span data-stu-id="dc8a9-111">Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="dc8a9-112">Обновление разделителя</span><span class="sxs-lookup"><span data-stu-id="dc8a9-112">Update delimiter</span></span>
<span data-ttu-id="dc8a9-113">Если имеется конфликт с планом счетов, можно изменить разделитель плана счетов и формат кода проекта/подпроекта.</span><span class="sxs-lookup"><span data-stu-id="dc8a9-113">If there is a conflict with the chart of accounts, the chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="dc8a9-114">Никакие другие разделители аналитики изменить невозможно.</span><span class="sxs-lookup"><span data-stu-id="dc8a9-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="dc8a9-115">Разделитель плана счетов можно изменить после обновления в **Параметры главной книги** > **Планы счетов и аналитики** > **Изменить разделитель**.</span><span class="sxs-lookup"><span data-stu-id="dc8a9-115">You can change the chart of accounts delimiter after upgrade in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="dc8a9-116">Если имеется только конфликт с форматом кода проекта/подпроекта, можно изменить это значение в параметре **Параметры модуля "Управление и учет по проектам"** > **Общее** > **Изменить формат подпроекта**.</span><span class="sxs-lookup"><span data-stu-id="dc8a9-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="dc8a9-117">Как определить, требуется ли в вашей среде обновление разделителей</span><span class="sxs-lookup"><span data-stu-id="dc8a9-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="dc8a9-118">В случае конфликта разделители в обновленной среде возможна неустойчивая работа при вводе значений в элементе управление сегментированным вводом или элементе управления вводом аналитики.</span><span class="sxs-lookup"><span data-stu-id="dc8a9-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="dc8a9-119">Это означает, что необходимо будет всегда использовать поиск с подстановкой или всплывающее меню при вводе комбинаций счета и аналитики.</span><span class="sxs-lookup"><span data-stu-id="dc8a9-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>
