---
title: Настройка параметров управления персоналом (HR) для нескольких юридических лиц
description: Необходимо настроить общие параметры для записей, которые используются совместно несколькими компаниями, например записи должностей. В этой статье описывается, как настроить параметры модуля "Управление персоналом" в разных юридических лицах.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: a8167545864a1cc2fc22f044f7d16ca590d59b43
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "859214"
---
# <a name="set-up-human-resources-hr-parameters-across-legal-entities"></a><span data-ttu-id="8f7bb-104">Настройка параметров управления персоналом (HR) для нескольких юридических лиц</span><span class="sxs-lookup"><span data-stu-id="8f7bb-104">Set up Human resources (HR) parameters across legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8f7bb-105">Необходимо настроить общие параметры для записей, которые используются совместно несколькими компаниями, например записи должностей.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-105">You must set up shared parameters for records that are shared across companies, such as Position records.</span></span> <span data-ttu-id="8f7bb-106">В этой статье описывается, как настроить параметры модуля "Управление персоналом" в разных юридических лицах.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-106">This article explains how to set up Human resources parameters across legal entities.</span></span>

<span data-ttu-id="8f7bb-107">Некоторые типы записей, такие как записи "Должность", используются сразу несколькими компаниями.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-107">Some types of records, such as Position records, are shared across companies.</span></span> <span data-ttu-id="8f7bb-108">Для этих записей необходимо настроить общие параметры.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-108">For these records, you must set up shared parameters.</span></span> <span data-ttu-id="8f7bb-109">Например, страница **Совместно используемые параметры управления персоналом** используется для задания параметров модуля "Управление персоналом", общих для нескольких юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-109">For example, you use the **Human resources shared parameters** page to set up Human resources parameters across legal entities.</span></span> 

<span data-ttu-id="8f7bb-110">На странице **Совместно используемые параметры управления персоналом** параметры сгруппированы в разделы в зависимости от их функциональности.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-110">On the **Human resources shared parameters** page, parameters are grouped into areas, based on their functionality.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="8f7bb-111">Ранее выпущенная функциональность</span><span class="sxs-lookup"><span data-stu-id="8f7bb-111">Previously released functionality</span></span>
<span data-ttu-id="8f7bb-112">На вкладке **Идентификация** необходимо выбрать типы идентификации, представляющие идентификационные номера, перечисленные на странице.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-112">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="8f7bb-113">Перед вводом идентификационных сведений для работников можно настроить типы документов, удостоверяющих личность.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-113">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="8f7bb-114">Информация о номере социального обеспечения, идентификационном номере (для граждан и иностранцев) и коде удостоверения личности ведется на странице **Тип документа**.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-114">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="8f7bb-115">Чтобы определить новый тип удостоверяющего личность документа или просмотреть список существующих типов, выберите **Управление персоналом** &gt; **вкладка "Ссылки"** &gt; **Настройка** &gt; **Типы документов, удостоверяющих личность**.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-115">To define a new identification type or review the list of existing types, click **Personnel management** &gt; **Links tab** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="8f7bb-116">Можно ввести простой код и описание.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-116">You can enter a simple code and description.</span></span> 

### <a name="if-youre-using-dynamics-365-for-talent"></a><span data-ttu-id="8f7bb-117">При использовании Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="8f7bb-117">If you're using Dynamics 365 for Talent</span></span>
<span data-ttu-id="8f7bb-118">На вкладке **Идентификация** необходимо выбрать типы идентификации, представляющие идентификационные номера, перечисленные на странице.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-118">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="8f7bb-119">Перед вводом идентификационных сведений для работников можно настроить типы документов, удостоверяющих личность.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-119">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="8f7bb-120">Информация о номере социального обеспечения, идентификационном номере (для граждан и иностранцев) и коде удостоверения личности ведется на странице **Тип документа**.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-120">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="8f7bb-121">Чтобы определить новый тип удостоверяющего личность документа или просмотреть список существующих типов, выберите **Управление персоналом** &gt; **Настройка** &gt; **Типы документов, удостоверяющих личность**.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-121">To define a new identification type or review the list of existing types, click **Human resources** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="8f7bb-122">Можно ввести простой код и описание.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-122">You can enter a simple code and description.</span></span> 

<span data-ttu-id="8f7bb-123">На вкладке **Номерные серии** можно выбрать номерные серии, используемые для следующих записей: табельный номер, должность, код запроса пользователя, документ по форме I-9, кандидат, обсуждение, код льготы и действие персонала (если этот тип записи включен).</span><span class="sxs-lookup"><span data-stu-id="8f7bb-123">On the **Number sequences** tab, you can select the number sequences that are used for the following records: Personnel number, Position, User request ID, I-9 document, Applicant, Discussion, Benefit ID, and Personnel action (if this record type is enabled).</span></span> <span data-ttu-id="8f7bb-124">Для ведения ссылок и кодов номерных серий используется страница списка **Номерные серии**.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-124">To maintain number sequence references and codes, use the **Number sequences** list page.</span></span> <span data-ttu-id="8f7bb-125">Чтобы найти эту страницу, используйте функцию поиска страниц.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-125">To find this page, use the page search feature.</span></span> 

<span data-ttu-id="8f7bb-126">На вкладке **Должности** укажите, доступны ли новые должности для назначения по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="8f7bb-126">On the **Positions** tab, indicate whether new positions are available for assignment by default:</span></span>

-   <span data-ttu-id="8f7bb-127">**Всегда** — можно назначать работников на новые должности при создании должностей.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-127">**Always** – You can assign workers to new positions when positions are created.</span></span> <span data-ttu-id="8f7bb-128">При создании должностей в качестве даты и времени в поле **Доступна для назначения** на вкладке **Общее** страницы **Должность** автоматически устанавливаются дата и время создания.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-128">When positions are created, the **Available for assignment** date and time on the **General** tab of the **Position** page are automatically set to the creation date and time.</span></span>
-   <span data-ttu-id="8f7bb-129">**Никогда** — назначать работников на новые должности при создании должностей нельзя.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-129">**Never** – You can't assign workers to new positions when positions are created.</span></span> <span data-ttu-id="8f7bb-130">Если выбран этот параметр, вы должны открывать страницу **Должность** для каждой новой должности, когда она станет доступна, а затем на вкладке **Общее** ввести дату в поле **Доступна для назначения**, чтобы назначение работников на должность стало возможно.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-130">If you select this option, you must open the **Position** page for each new position as it becomes available, and then, on the **General** tab, enter the **Available for assignment** date to enable worker assignment.</span></span>


<a name="additional-resources"></a><span data-ttu-id="8f7bb-131">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8f7bb-131">Additional resources</span></span>
--------

[<span data-ttu-id="8f7bb-132">Настройка параметров управления персоналом для конкретной компании</span><span class="sxs-lookup"><span data-stu-id="8f7bb-132">Set up company specific HR parameters</span></span>](set-up-company-specific-hr-parameters.md)



