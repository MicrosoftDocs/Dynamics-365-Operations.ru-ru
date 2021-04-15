---
title: Подготовка юридического лица для процесса консолидации
description: Во время консолидации проводки из нескольких наборов счетов юридического лица собираются в единый набор счетов юридического лица. В этой теме объясняется, как подготовить юридическое лицо для консолидации.
author: jinniew
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 6f718bef3b1b07d3bb03dbf6acbf1cdf58aa7b8a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815484"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a><span data-ttu-id="9dc49-104">Подготовка юридического лица для процесса консолидации</span><span class="sxs-lookup"><span data-stu-id="9dc49-104">Prepare a legal entity for the consolidation process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9dc49-105">Во время консолидации проводки из нескольких наборов счетов юридического лица собираются в единый набор счетов юридического лица.</span><span class="sxs-lookup"><span data-stu-id="9dc49-105">During a consolidation, you gather transactions from several sets of legal entity accounts into a single set of legal entity accounts.</span></span> <span data-ttu-id="9dc49-106">В этой теме объясняется, как подготовить юридическое лицо для консолидации.</span><span class="sxs-lookup"><span data-stu-id="9dc49-106">This topic explains how to prepare a legal entity for a consolidation.</span></span>

> [!NOTE]
> <span data-ttu-id="9dc49-107">Рекомендуется использовать Management Reporter для Microsoft Dynamics 365 Finance для объединения финансовых результатов для нескольких юридических лиц в консолидированном формате.</span><span class="sxs-lookup"><span data-stu-id="9dc49-107">We recommend that you use Management Reporter for Microsoft Dynamics 365 Finance to combine the financial results for multiple legal entities in a consolidated format.</span></span> <span data-ttu-id="9dc49-108">Management Reporter позволяет создавать консолидированные финансовые отчеты для юридических лиц, использовать Excel для импорта данных консолидации из других источников и перевода сумм в любое количество валют отчетности без выполнения процесса консолидации в Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="9dc49-108">Management Reporter lets you create consolidated financial reports across legal entities, use Excel to import consolidation data from other sources, and translate amounts into any number of reporting currencies without having to run the consolidation process in Dynamics 365 Finance.</span></span>

<span data-ttu-id="9dc49-109">Из консолидированного юридического лица также можно напечатать отчеты, например финансовые отчеты.</span><span class="sxs-lookup"><span data-stu-id="9dc49-109">You can print reports, such as financial statements, from the consolidated legal entity.</span></span> <span data-ttu-id="9dc49-110">Однако консолидированное юридическое лицо нельзя использовать для ежедневных проводок.</span><span class="sxs-lookup"><span data-stu-id="9dc49-110">However, you can't use the consolidated legal entity for daily transactions.</span></span>

<span data-ttu-id="9dc49-111">Можно консолидировать данные из юридических лиц, использующих базы данных, отличные от консолидированного юридического лица.</span><span class="sxs-lookup"><span data-stu-id="9dc49-111">You can consolidate data from legal entities that use different databases than the consolidated legal entity.</span></span> <span data-ttu-id="9dc49-112">Этот процесс консолидации называется *консолидацией импорта*.</span><span class="sxs-lookup"><span data-stu-id="9dc49-112">This consolidation process is referred to as an *import consolidation*.</span></span> <span data-ttu-id="9dc49-113">Или же юридические лица могут использовать ту же базу данных, что и консолидированное юридическое лицо.</span><span class="sxs-lookup"><span data-stu-id="9dc49-113">Alternatively, the legal entities can use the same database as the consolidated legal entity.</span></span> <span data-ttu-id="9dc49-114">Этот процесс консолидации называется *консолидацией в интерактивном режиме*.</span><span class="sxs-lookup"><span data-stu-id="9dc49-114">This consolidation process is referred to as an *online consolidation*.</span></span>

<span data-ttu-id="9dc49-115">Консолидированное юридическое лицо собирает результаты и сальдо филиалов.</span><span class="sxs-lookup"><span data-stu-id="9dc49-115">The consolidated legal entity collects the results and balances of the subsidiaries.</span></span> <span data-ttu-id="9dc49-116">Чтобы подготовить консолидированное юридическое лицо к консолидации, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9dc49-116">To prepare a consolidated legal entity for a consolidation, follow these steps.</span></span>

1. <span data-ttu-id="9dc49-117">Перейдите в раздел **Главная книга \> Настройка \> Организация \> Юридические лица**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-117">Go to **General ledger \> Setup \> Organization \> Legal entities**.</span></span>
2. <span data-ttu-id="9dc49-118">Выберите **Создать**, чтобы создать юридическое лицо, которое будет консолидированным юридическим лицом.</span><span class="sxs-lookup"><span data-stu-id="9dc49-118">Select **New** to create the legal entity that will be the consolidated legal entity.</span></span>
3. <span data-ttu-id="9dc49-119">Выберите флажок **Использовать для процесса финансовой консолидации**, затем введите сведения о консолидированном юридическом лице.</span><span class="sxs-lookup"><span data-stu-id="9dc49-119">Select the **Use for financial consolidation process** check box, and then enter information about the consolidated legal entity.</span></span> <span data-ttu-id="9dc49-120">Обязательно введите эту информацию именно в том виде, в котором она будет отображаться в финансовых отчетах для консолидированного юридического лица.</span><span class="sxs-lookup"><span data-stu-id="9dc49-120">Be sure to enter this information exactly as you want it to appear on financial statements for the consolidated legal entity.</span></span>
4. <span data-ttu-id="9dc49-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9dc49-121">Close the page.</span></span>
5. <span data-ttu-id="9dc49-122">Выберите консолидированное юридическое лицо в поле в верхнем правом углу страницы, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-122">Select the consolidated legal entity in the field in the upper-right corner of the page, and then select **OK**.</span></span>
6. <span data-ttu-id="9dc49-123">Перейдите в раздел **Главная книга \> Настройка \> Книга учета**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-123">Go to **General ledger \> Setup \> Ledger**.</span></span>
7. <span data-ttu-id="9dc49-124">Выберите план счетов, финансовый календарь, валюту учета, дополнительную валюту отчетности и тип по умолчанию валютного курса для консолидированного юридического лица.</span><span class="sxs-lookup"><span data-stu-id="9dc49-124">Select the chart of accounts, the fiscal calendar, the accounting currency, an optional reporting currency, and the default type of exchange rate for the consolidated legal entity.</span></span> 
8. <span data-ttu-id="9dc49-125">Перейдите в раздел **Главная книга \> Настройка \> Валюта \> Валютные курсы**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-125">Go to **General ledger \> Setup \> Currency \> Currency exchange rates**.</span></span>
9. <span data-ttu-id="9dc49-126">Настройте курсы обмена валют за соответствующие периоды для валют дочерних юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="9dc49-126">Set up currency exchange rates in relevant periods for the currencies of the subsidiary legal entities.</span></span>
10. <span data-ttu-id="9dc49-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9dc49-127">Close the page.</span></span>
11. <span data-ttu-id="9dc49-128">Если у консолидированного юридического лица есть подразделения, в которых используется иностранная валюта, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="9dc49-128">If the consolidated legal entity has subsidiaries that use foreign currencies, follow these steps:</span></span>

    1. <span data-ttu-id="9dc49-129">Перейдите в раздел **Главная книга \> Настройка \> Разноска \> Счета для автоматических проводок**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-129">Go to **General ledger \> Setup \> Posting \> Accounts for automatic transactions**.</span></span>
    2. <span data-ttu-id="9dc49-130">В поле **Тип разноски** выберите соответствующий счет:</span><span class="sxs-lookup"><span data-stu-id="9dc49-130">In the **Posting type** field, select an appropriate account:</span></span>

        - <span data-ttu-id="9dc49-131">Если у юридического лица есть иностранные дочерние компании, которые финансово или операционно взаимосвязаны с родительским юридическим лицом, выберите соответствующий счет для типа разноски **Счет прибыли и убытка для разниц консолидации**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-131">If the legal entity has foreign subsidiaries that are financially or operationally interdependent with the parent legal entity, select an appropriate account for the **Profit and loss account for consolidation differences** posting type.</span></span>
        - <span data-ttu-id="9dc49-132">При консолидации подразделения, которое не зависит от родительского юридического лица в финансовом и операционном плане, или при консолидации юридического лица, имеющего результаты нескольких независимых подразделений, и при использовании методов трансляции для консолидации данных выберите соответствующий счет для типа разноски **Балансовый счет для разниц консолидации**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-132">If you're consolidating a subsidiary that is financially and operationally independent of the parent legal entity, or a legal entity that contains the results of several subsidiaries that are financially and operationally independent of the parent legal entity, and if you're using translation methods to consolidate the data, select an appropriate account for the **Balance account for consolidation differences** posting type.</span></span>

    3. <span data-ttu-id="9dc49-133">В поле **Счет ГК** введите счета ГК, которые должны использоваться для переоценок в иностранной валюте.</span><span class="sxs-lookup"><span data-stu-id="9dc49-133">In the **Main account** field, select the main accounts that should be used for foreign currency revaluation adjustments.</span></span>
    4. <span data-ttu-id="9dc49-134">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9dc49-134">Close the page.</span></span>

    <span data-ttu-id="9dc49-135">Если консолидированное юридическое лицо создается в начале периода, суммы в валюте можно переоценить, так как валютные курсы изменяются в течение периода консолидации.</span><span class="sxs-lookup"><span data-stu-id="9dc49-135">If you create the consolidated legal entity early in a period, you can revalue foreign currency amounts as exchange rates change during the consolidation period.</span></span>

<span data-ttu-id="9dc49-136">Теперь консолидированное юридическое лицо настроено для периодического задания **Консолидировать**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-136">The consolidated legal entity is now set up for the **Consolidate** periodic job.</span></span> <span data-ttu-id="9dc49-137">Можно выполнить консолидацию импорта или интерактивную консолидацию.</span><span class="sxs-lookup"><span data-stu-id="9dc49-137">You can do either an import consolidation or an online consolidation.</span></span>

- <span data-ttu-id="9dc49-138">Для выполнения консолидации импорта перейдите в раздел **Главная книга \> Периодические \> Консолидировать \> Консолидировать \[импорт из\]**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-138">To do an import consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Import from\]**.</span></span>
- <span data-ttu-id="9dc49-139">Для выполнения интерактивной консолидации перейдите в раздел **Главная книга \> Периодические \> Консолидировать \> Консолидировать \[в Интернете\]**.</span><span class="sxs-lookup"><span data-stu-id="9dc49-139">To do an online consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Online\]**.</span></span>

> [!NOTE]
> <span data-ttu-id="9dc49-140">Прежде чем можно будет обработать консолидацию, вы должны подготовить подразделения юридического лица к консолидации.</span><span class="sxs-lookup"><span data-stu-id="9dc49-140">Before you can process the consolidation, you must prepare the subsidiary legal entities for consolidation.</span></span> <span data-ttu-id="9dc49-141">Дополнительные сведения см. в разделе [Настройка дочернего юридического лица для консолидации](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="9dc49-141">For more information, see [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]