---
title: Создать предложение по амортизации
description: В этой процедуре описывается, как работают предложения партий амортизации и как предложить амортизацию для основных средств.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07146adfe1ead2b6e06e3c323963f8c012381b76
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840009"
---
# <a name="create-depreciation-proposal"></a><span data-ttu-id="da806-103">Создать предложение по амортизации</span><span class="sxs-lookup"><span data-stu-id="da806-103">Create depreciation proposal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="da806-104">В этой процедуре описывается, как работают предложения партий амортизации и как предложить амортизацию для основных средств.</span><span class="sxs-lookup"><span data-stu-id="da806-104">This procedure describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="da806-105">В этой задаче используется демонстрационная компания USMF и роль бухгалтера.</span><span class="sxs-lookup"><span data-stu-id="da806-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-depreciation-proposal"></a><span data-ttu-id="da806-106">Создать предложение по амортизации</span><span class="sxs-lookup"><span data-stu-id="da806-106">Create depreciation proposal</span></span>
1. <span data-ttu-id="da806-107">Перейдите в раздел "Основные средства" > "Записи в журнале" > "Создать предложение по амортизации".</span><span class="sxs-lookup"><span data-stu-id="da806-107">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="da806-108">В поле "Наименование журнала" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="da806-108">In the Name of journal field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="da806-109">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="da806-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="da806-110">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="da806-110">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="da806-111">Установите флажок "Суммировать амортизацию", чтобы объединить ежемесячные амортизации в одну строку журнала.</span><span class="sxs-lookup"><span data-stu-id="da806-111">Select the Summarize depreciation option to summarize monthly depreciations into one journal line.</span></span>  
    * <span data-ttu-id="da806-112">Например, если значение параметра "До даты" — 31 марта 2015 г., формируется следующее сообщение: "Амортизация с 31 января 2015 г."</span><span class="sxs-lookup"><span data-stu-id="da806-112">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="da806-113">Значение в поле "Дата" в предлагаемых строках журнала в этом случае устанавливается равным 31 марта 2015 г.</span><span class="sxs-lookup"><span data-stu-id="da806-113">The Date field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    * <span data-ttu-id="da806-114">Предложение по амортизации можно отфильтровать по основному средству, группе основных средств или другим критериям с помощью параметра "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="da806-114">The depreciation proposal can be filtered by asset, asset group, or other criteria using the Filter option.</span></span>  
    * <span data-ttu-id="da806-115">При использовании формы "Создавать предложения по приобретению или амортизации для основных средств" можно предложить пакетную амортизацию.</span><span class="sxs-lookup"><span data-stu-id="da806-115">When you use the Create acquisition or depreciation proposals for fixed assets form, you can propose depreciation in batches.</span></span> <span data-ttu-id="da806-116">Этот способ рекомендуется для более крупных предложений, которые используют больше системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="da806-116">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="da806-117">При выборе параметра партии можно по-прежнему выполнять другие задачи в это время.</span><span class="sxs-lookup"><span data-stu-id="da806-117">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="da806-118">Если амортизация предлагается этим способом, она рассчитывается для моделей стоимости основных средств.</span><span class="sxs-lookup"><span data-stu-id="da806-118">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  
5. <span data-ttu-id="da806-119">Щелкните "Создать журнал".</span><span class="sxs-lookup"><span data-stu-id="da806-119">Click Create journal.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="da806-120">Проверка записей амортизации</span><span class="sxs-lookup"><span data-stu-id="da806-120">Review depreciation entries</span></span>
1. <span data-ttu-id="da806-121">Перейдите в раздел "Основные средства" > "Записи в журнале" > "Журнал основных средств".</span><span class="sxs-lookup"><span data-stu-id="da806-121">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="da806-122">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="da806-122">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="da806-123">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="da806-123">Click Lines.</span></span>
4. <span data-ttu-id="da806-124">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="da806-124">Click Post.</span></span>

