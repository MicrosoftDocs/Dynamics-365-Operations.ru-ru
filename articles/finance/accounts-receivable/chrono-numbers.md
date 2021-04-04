---
title: Хронологическая нумерация документов и операций
description: В этой теме объясняется, как настроить и использовать хронологические номера для применимых документов и соответствующих операций.
author: ikond
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 4a27b6fdd1e244fb0cb8c5fcefc484494aeb88bd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254537"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a><span data-ttu-id="a159c-103">Хронологическая нумерация документов и операций</span><span class="sxs-lookup"><span data-stu-id="a159c-103">Numbering documents and vouchers chronologically</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="a159c-104">В некоторых странах имеется юридическое требование для нумерации документов и соответствующих операций в хронологическом порядке.</span><span class="sxs-lookup"><span data-stu-id="a159c-104">In some countries, there is a legal requirement to number documents and related vouchers in chronological order.</span></span> <span data-ttu-id="a159c-105">Хронология должна поддерживаться по периодам.</span><span class="sxs-lookup"><span data-stu-id="a159c-105">The chronology must be supported by periods.</span></span> <span data-ttu-id="a159c-106">Все номера, принадлежащие более ранним периодам, должны быть меньше, чем номера, принадлежащие более поздним периодам.</span><span class="sxs-lookup"><span data-stu-id="a159c-106">All of the numbers that belong to earlier periods must be less than the numbers that belong to later periods.</span></span> <span data-ttu-id="a159c-107">Для обеспечения этого требования реализована хронологическая нумерация.</span><span class="sxs-lookup"><span data-stu-id="a159c-107">To meet this requirement, chronological numbering functionality has been implemented.</span></span> <span data-ttu-id="a159c-108">В этой теме объясняется, как настроить и использовать хронологические номера для применимых документов и соответствующих операций.</span><span class="sxs-lookup"><span data-stu-id="a159c-108">This topic explains how to configure and use chronological numbers for applicable documents and related vouchers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a159c-109">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="a159c-109">Prerequisites</span></span>

<span data-ttu-id="a159c-110">В рабочей области управления функциями включите функцию **Хронологическая нумерация**.</span><span class="sxs-lookup"><span data-stu-id="a159c-110">In the Feature management workspace, turn on the **Chronological numbering** feature.</span></span> <span data-ttu-id="a159c-111">Дополнительные сведения см. в разделе [Обзор управления функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a159c-111">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-chronological-numbering"></a><span data-ttu-id="a159c-112">Настройка хронологической нумерации</span><span class="sxs-lookup"><span data-stu-id="a159c-112">Configure chronological numbering</span></span>

<span data-ttu-id="a159c-113">Хронологическая нумерация влияет на следующие документы.</span><span class="sxs-lookup"><span data-stu-id="a159c-113">Chronological numbering affects the following documents.</span></span>

<span data-ttu-id="a159c-114">**Расчеты с клиентами**</span><span class="sxs-lookup"><span data-stu-id="a159c-114">**Accounts receivable**</span></span>
- <span data-ttu-id="a159c-115">Накладная клиента</span><span class="sxs-lookup"><span data-stu-id="a159c-115">Customer invoice</span></span>
- <span data-ttu-id="a159c-116">Ваучер по накладной клиента</span><span class="sxs-lookup"><span data-stu-id="a159c-116">Customer invoice voucher</span></span>
- <span data-ttu-id="a159c-117">Кредит-нота по продаже</span><span class="sxs-lookup"><span data-stu-id="a159c-117">Sales credit note</span></span>
- <span data-ttu-id="a159c-118">Ваучер кредит-ноты по продажам</span><span class="sxs-lookup"><span data-stu-id="a159c-118">Sales credit note voucher</span></span>
- <span data-ttu-id="a159c-119">Накладная с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="a159c-119">Free text invoice</span></span>
- <span data-ttu-id="a159c-120">Ваучер по накладной с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="a159c-120">Free text invoice voucher</span></span>
- <span data-ttu-id="a159c-121">Кредит-нота с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="a159c-121">Free text credit note</span></span>
- <span data-ttu-id="a159c-122">Ваучер по кредит-ноте с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="a159c-122">Free text credit note voucher</span></span>
- <span data-ttu-id="a159c-123">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="a159c-123">Packing slip</span></span>
- <span data-ttu-id="a159c-124">Ваучер по отборочной накладной</span><span class="sxs-lookup"><span data-stu-id="a159c-124">Packing slip voucher</span></span>
- <span data-ttu-id="a159c-125">Ваучер сторно по отборочной накладной</span><span class="sxs-lookup"><span data-stu-id="a159c-125">Packing slip correction voucher</span></span>
- <span data-ttu-id="a159c-126">Ваучер по процент-ноте</span><span class="sxs-lookup"><span data-stu-id="a159c-126">Interest note voucher</span></span>
- <span data-ttu-id="a159c-127">Ваучер по письму-напоминанию</span><span class="sxs-lookup"><span data-stu-id="a159c-127">Collection letter voucher</span></span>

<span data-ttu-id="a159c-128">**Расчеты с поставщиками**</span><span class="sxs-lookup"><span data-stu-id="a159c-128">**Accounts payable**</span></span>
- <span data-ttu-id="a159c-129">Ваучер по накладной</span><span class="sxs-lookup"><span data-stu-id="a159c-129">Invoice voucher</span></span>
- <span data-ttu-id="a159c-130">Ваучер по кредит-ноте</span><span class="sxs-lookup"><span data-stu-id="a159c-130">Credit note voucher</span></span>
- <span data-ttu-id="a159c-131">Ваучер поступления продуктов</span><span class="sxs-lookup"><span data-stu-id="a159c-131">Product receipt voucher</span></span>

<span data-ttu-id="a159c-132">**Управление проектами**</span><span class="sxs-lookup"><span data-stu-id="a159c-132">**Project management**</span></span>
- <span data-ttu-id="a159c-133">Счет-фактура</span><span class="sxs-lookup"><span data-stu-id="a159c-133">Invoice</span></span>
- <span data-ttu-id="a159c-134">Ваучер по накладной</span><span class="sxs-lookup"><span data-stu-id="a159c-134">Invoice voucher</span></span>
- <span data-ttu-id="a159c-135">Кредит-нота</span><span class="sxs-lookup"><span data-stu-id="a159c-135">Credit note</span></span>
- <span data-ttu-id="a159c-136">Ваучер по кредит-ноте</span><span class="sxs-lookup"><span data-stu-id="a159c-136">Credit note voucher</span></span> 

### <a name="define-number-sequences"></a><span data-ttu-id="a159c-137">Определение номерных серий</span><span class="sxs-lookup"><span data-stu-id="a159c-137">Define number sequences</span></span>

<span data-ttu-id="a159c-138">Чтобы определить номерные серии, перейдите в раздел **Администрирование организации** > **Номерные серии** > **Номерные серии**.</span><span class="sxs-lookup"><span data-stu-id="a159c-138">To define number sequences, go to **Organization administration** > **Number sequences** > **Number sequences**.</span></span> <span data-ttu-id="a159c-139">Вы можете определить столько номерных серий, сколько требуется для покрытия соответствующих периодов для требуемых документов.</span><span class="sxs-lookup"><span data-stu-id="a159c-139">You can define as many number sequences as required to cover the affected periods for required documents.</span></span> 

<span data-ttu-id="a159c-140">Укажите компанию для каждой номерной серии.</span><span class="sxs-lookup"><span data-stu-id="a159c-140">Specify a company for each number sequence.</span></span> <span data-ttu-id="a159c-141">Сегменты номерных серий должны быть определены таким образом, чтобы они предоставляли хронологический порядок для периодов.</span><span class="sxs-lookup"><span data-stu-id="a159c-141">The segments of the number sequences must be defined so that they provide chronological order for periods.</span></span> <span data-ttu-id="a159c-142">Например, имена сегментов могут содержать специальный префикс, идентифицирующий конкретный период.</span><span class="sxs-lookup"><span data-stu-id="a159c-142">For example, the segment names can contain a special prefix that identifies a specific period.</span></span>

![Настройка номерных серий](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a><span data-ttu-id="a159c-144">Настройка групп номерных серий</span><span class="sxs-lookup"><span data-stu-id="a159c-144">Configure number sequence groups</span></span>

<span data-ttu-id="a159c-145">Чтобы настроить группы номерных серий, перейдите в раздел **Расчеты с клиентами** > **Настройка** > **Параметры модуля расчетов с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="a159c-145">To configure number sequence groups, go to **Accounts receivable** > **Setup** > **Accounts receivable parameters**.</span></span> <span data-ttu-id="a159c-146">На вкладке **Номерные серии** определите столько групп номерных серий, сколько необходимо для покрытия соответствующих периодов.</span><span class="sxs-lookup"><span data-stu-id="a159c-146">On the **Number sequences** tab, define as many number sequences groups as required to cover the affected periods.</span></span> 

<span data-ttu-id="a159c-147">Для каждой группы в разделе **Ссылка** выберите одну из поддерживаемых ссылок на документы, а в поле **Код номерной серии** укажите номерную серию, которая ранее была создана для связанного периода.</span><span class="sxs-lookup"><span data-stu-id="a159c-147">For each group, in the **Reference** section, select one of the supported document references, and in the **Number sequence code** field, refer to a number sequence that was previously created for the related period.</span></span>

![Настройка групп номерных серий](media/chrono-num-sequence-group.jpg)

<span data-ttu-id="a159c-149">Аналогичным образом настройте группы номерных серий в модулях **Расчеты с поставщиками** и **Управление и учет по проектам**.</span><span class="sxs-lookup"><span data-stu-id="a159c-149">Similarly, configure number sequence groups in **Accounts payable** and **Project management and accounting** modules.</span></span>

### <a name="configure-number-sequence-groups-chronology"></a><span data-ttu-id="a159c-150">Настройка хронологии групп номерных серий</span><span class="sxs-lookup"><span data-stu-id="a159c-150">Configure number sequence groups chronology</span></span>

<span data-ttu-id="a159c-151">Чтобы настроить хронологию групп номерных серий, перейдите в раздел **Администрирование организации** > **Номерные серии** > **Хронологические группы номерных серий**.</span><span class="sxs-lookup"><span data-stu-id="a159c-151">To configure number sequence groups chronology, go to **Organization administration** > **Number sequences** > **Chronological number sequence groups**.</span></span> <span data-ttu-id="a159c-152">Определите условия применимости для групп номерных серий.</span><span class="sxs-lookup"><span data-stu-id="a159c-152">Define the applicability conditions for number sequence groups.</span></span>

![Настройка хронологических номеров](media/chrono-num-sequence-group-period.jpg)

| <span data-ttu-id="a159c-154">Поле</span><span class="sxs-lookup"><span data-stu-id="a159c-154">Field</span></span>            | <span data-ttu-id="a159c-155">описание</span><span class="sxs-lookup"><span data-stu-id="a159c-155">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a159c-156">Действует</span><span class="sxs-lookup"><span data-stu-id="a159c-156">Effective</span></span>  | <span data-ttu-id="a159c-157">Дата начала применимости группы номерных серий.</span><span class="sxs-lookup"><span data-stu-id="a159c-157">The start date of number sequence group applicability.</span></span> |
| <span data-ttu-id="a159c-158">Истечение срока действия</span><span class="sxs-lookup"><span data-stu-id="a159c-158">Expiration</span></span>      | <span data-ttu-id="a159c-159">Дата окончания применимости группы номерных серий.</span><span class="sxs-lookup"><span data-stu-id="a159c-159">The end date of number sequence group applicability.</span></span> <span data-ttu-id="a159c-160">Если дата окончания не применяется, выберите **Никогда**.</span><span class="sxs-lookup"><span data-stu-id="a159c-160">If no end date is applied, select **Never**.</span></span> |
| <span data-ttu-id="a159c-161">Группа номерных серий</span><span class="sxs-lookup"><span data-stu-id="a159c-161">Number sequence group</span></span> | <span data-ttu-id="a159c-162">Группа номерных серий, которая будет использоваться для создания номеров документов в течение периода.</span><span class="sxs-lookup"><span data-stu-id="a159c-162">Number sequence group that will be used to generate document numbers during the period.</span></span> |
| <span data-ttu-id="a159c-163">Исходная группа номерных серий</span><span class="sxs-lookup"><span data-stu-id="a159c-163">Original number sequence group</span></span> | <span data-ttu-id="a159c-164">Этот код группы номерных серий используется для дополнительной фильтрации для случаев, когда для документов уже назначена определенная *постоянная* группа номерных серий.</span><span class="sxs-lookup"><span data-stu-id="a159c-164">This number sequence group code is used for additional filtering for the cases when documents already have a specific *permanent* number sequence group assigned.</span></span> <span data-ttu-id="a159c-165">Пустое значение рассматривается как конкретное значение.</span><span class="sxs-lookup"><span data-stu-id="a159c-165">An empty value is considered a specific value.</span></span> <span data-ttu-id="a159c-166">Если предварительно назначенная группа должна игнорироваться, следует использовать параметр **По умолчанию** для этой настройки.</span><span class="sxs-lookup"><span data-stu-id="a159c-166">If you need to ignore a preliminary assigned group, use the **Default** option for this setup.</span></span> |
| <span data-ttu-id="a159c-167">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="a159c-167">Default</span></span> | <span data-ttu-id="a159c-168">Если этот параметр включен, система игнорирует предварительно назначенную группу номерных серий документов и использует только даты начала и окончания периода для анализа применимости.</span><span class="sxs-lookup"><span data-stu-id="a159c-168">If turned on, the system ignores the preliminary assigned document number sequence group and uses only the periods start and end dates for applicability analysis.</span></span> <span data-ttu-id="a159c-169">Если этот параметр отключен, система использует полное сочетание **Вступает в силу** + **Истечение срока** + **Исходная группа номерных серий** для выбора.</span><span class="sxs-lookup"><span data-stu-id="a159c-169">If turned off, the system uses the full combination **Effective** + **Expiration** + **Original number sequence group** for selection.</span></span> |

## <a name="document-posting"></a><span data-ttu-id="a159c-170">Разноска документов</span><span class="sxs-lookup"><span data-stu-id="a159c-170">Document posting</span></span>
<span data-ttu-id="a159c-171">При разноске документа для него назначается соответствующая группа номерных серий, основанная на дате разноски документа, а затем используется для создания номера документа на основе обнаруженной номерной серии.</span><span class="sxs-lookup"><span data-stu-id="a159c-171">When you post a document, the appropriate number sequence group is assigned to the document, based on document's posting date, and then used to generate a document number based on the detected number sequence.</span></span> <span data-ttu-id="a159c-172">Система создает сообщение, относящееся к назначению группы номерных серий.</span><span class="sxs-lookup"><span data-stu-id="a159c-172">The system provides a message regarding the number sequence group assignment.</span></span>

![Номер документа](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> <span data-ttu-id="a159c-174">Для некоторых стран существует конкретная логика, уже реализованная для нумерации документов.</span><span class="sxs-lookup"><span data-stu-id="a159c-174">For some countries, there is a specific logic already implemented for document numbering.</span></span> <span data-ttu-id="a159c-175">В этом случае логика для определенной страны переопределяет функцию **Хронологическая нумерация**.</span><span class="sxs-lookup"><span data-stu-id="a159c-175">In this case, country-specific logic will override the **Chronological numbering** feature.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]