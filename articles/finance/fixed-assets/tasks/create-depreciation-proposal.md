---
title: Создание предложения по амортизации
description: В этом разделе описывается, как работают предложения партий амортизации и как предложить амортизацию для основных средств.
author: abruer
manager: AnnBe
ms.date: 08/01/2019
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
ms.openlocfilehash: 07337063c01f146c72ca6d9e0f9096907cdc9638
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142831"
---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="b440d-103">Создание предложения по амортизации</span><span class="sxs-lookup"><span data-stu-id="b440d-103">Create a depreciation proposal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b440d-104">В этом разделе описывается, как работают предложения партий амортизации и как предложить амортизацию для основных средств.</span><span class="sxs-lookup"><span data-stu-id="b440d-104">This topic describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="b440d-105">В этой задаче используется демонстрационная компания USMF и роль бухгалтера.</span><span class="sxs-lookup"><span data-stu-id="b440d-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-a-depreciation-proposal"></a><span data-ttu-id="b440d-106">Создание предложения по амортизации</span><span class="sxs-lookup"><span data-stu-id="b440d-106">Create a depreciation proposal</span></span>
1. <span data-ttu-id="b440d-107">В области перехода, перейдите к **Модули > Основные средства > Записи журнала > Создать предложение по амортизации**.</span><span class="sxs-lookup"><span data-stu-id="b440d-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Create depreciation proposal**.</span></span>
2. <span data-ttu-id="b440d-108">В поле **Название журнала** выберите вариант в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="b440d-108">In the **Name of journal** field, select an option from the drop-down menu.</span></span>
3. <span data-ttu-id="b440d-109">В поле **Дата окончания** введите дату.</span><span class="sxs-lookup"><span data-stu-id="b440d-109">In the **To date** field, enter a date.</span></span>

    - <span data-ttu-id="b440d-110">Установите флажок **Суммировать амортизацию**, чтобы объединить ежемесячные амортизации в одну строку журнала.</span><span class="sxs-lookup"><span data-stu-id="b440d-110">Select the **Summarize depreciation** option to summarize monthly depreciations into one journal line.</span></span>  
    - <span data-ttu-id="b440d-111">Например, если значение параметра "До даты" — 31 марта 2015 г., формируется следующее сообщение: "Амортизация с 31 января 2015 г."</span><span class="sxs-lookup"><span data-stu-id="b440d-111">For example, if the To date value is March 31, 2015, the following description is generated: "Depreciation since January 31, 2015."</span></span> <span data-ttu-id="b440d-112">Значение в поле **Дата** в предлагаемых строках журнала в этом случае устанавливается равным 31 марта 2015 г.</span><span class="sxs-lookup"><span data-stu-id="b440d-112">The **Date** field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    - <span data-ttu-id="b440d-113">Предложение по амортизации можно отфильтровать по основному средству, группе основных средств или другим критериям с помощью параметра **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="b440d-113">The depreciation proposal can be filtered by asset, asset group, or other criteria using the **Filter** option.</span></span>  
    - <span data-ttu-id="b440d-114">При использовании формы **Создавать предложения по приобретению или амортизации для основных средств** можно предложить пакетную амортизацию.</span><span class="sxs-lookup"><span data-stu-id="b440d-114">When you use the **Create acquisition or depreciation proposals for fixed assets** form, you can propose depreciation in batches.</span></span> <span data-ttu-id="b440d-115">Этот способ рекомендуется для более крупных предложений, которые используют больше системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b440d-115">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="b440d-116">При выборе параметра партии можно по-прежнему выполнять другие задачи в это время.</span><span class="sxs-lookup"><span data-stu-id="b440d-116">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="b440d-117">Если амортизация предлагается этим способом, она рассчитывается для моделей стоимости основных средств.</span><span class="sxs-lookup"><span data-stu-id="b440d-117">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  

4. <span data-ttu-id="b440d-118">Выберите **Создать журнал**.</span><span class="sxs-lookup"><span data-stu-id="b440d-118">Select **Create journal**.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="b440d-119">Проверка записей амортизации</span><span class="sxs-lookup"><span data-stu-id="b440d-119">Review depreciation entries</span></span>
1. <span data-ttu-id="b440d-120">В области перехода, перейдите к **Модули > Основные средства > Записи журнала > Журнал основных средств**.</span><span class="sxs-lookup"><span data-stu-id="b440d-120">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="b440d-121">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="b440d-121">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b440d-122">Выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="b440d-122">Select **Lines**.</span></span>
4. <span data-ttu-id="b440d-123">Выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="b440d-123">Select **Post**.</span></span>

