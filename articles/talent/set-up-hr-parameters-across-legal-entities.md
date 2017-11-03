---
title: "Настройка параметров управления персоналом для нескольких юридических лиц"
description: "Необходимо настроить общие параметры для записей, которые используются совместно несколькими компаниями, например записи должностей. В этой статье описывается, как настроить параметры модуля \"Управление персоналом\" в разных юридических лицах."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 25d342272581abb96127d8761b3eac8d4f7695df
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-hr-parameters-across-legal-entities"></a><span data-ttu-id="24b3c-104">Настройка параметров управления персоналом для нескольких юридических лиц</span><span class="sxs-lookup"><span data-stu-id="24b3c-104">Set up HR parameters across legal entities</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="24b3c-105">Необходимо настроить общие параметры для записей, которые используются совместно несколькими компаниями, например записи должностей.</span><span class="sxs-lookup"><span data-stu-id="24b3c-105">You must set up shared parameters for records that are shared across companies, such as Position records.</span></span> <span data-ttu-id="24b3c-106">В этой статье описывается, как настроить параметры модуля "Управление персоналом" в разных юридических лицах.</span><span class="sxs-lookup"><span data-stu-id="24b3c-106">This article explains how to set up Human resources parameters across legal entities.</span></span>

<span data-ttu-id="24b3c-107">Некоторые типы записей, такие как записи "Должность", используются сразу несколькими компаниями.</span><span class="sxs-lookup"><span data-stu-id="24b3c-107">Some types of records, such as Position records, are shared across companies.</span></span> <span data-ttu-id="24b3c-108">Для этих записей необходимо настроить общие параметры.</span><span class="sxs-lookup"><span data-stu-id="24b3c-108">For these records, you must set up shared parameters.</span></span> <span data-ttu-id="24b3c-109">Например, страница **Совместно используемые параметры управления персоналом** используется для задания параметров модуля "Управление персоналом", общих для нескольких юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="24b3c-109">For example, you use the **Human resources shared parameters** page to set up Human resources parameters across legal entities.</span></span> 

<span data-ttu-id="24b3c-110">На странице **Совместно используемые параметры управления персоналом** параметры сгруппированы в разделы в зависимости от их функциональности.</span><span class="sxs-lookup"><span data-stu-id="24b3c-110">On the **Human resources shared parameters** page, parameters are grouped into areas, based on their functionality.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="24b3c-111">Ранее выпущенная функциональность</span><span class="sxs-lookup"><span data-stu-id="24b3c-111">Previously released functionality</span></span>
<span data-ttu-id="24b3c-112">На вкладке **Идентификация** необходимо выбрать типы идентификации, представляющие идентификационные номера, перечисленные на странице.</span><span class="sxs-lookup"><span data-stu-id="24b3c-112">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="24b3c-113">Перед вводом идентификационных сведений для работников можно настроить типы документов, удостоверяющих личность.</span><span class="sxs-lookup"><span data-stu-id="24b3c-113">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="24b3c-114">Информация о номере социального обеспечения, идентификационном номере (для граждан и иностранцев) и коде удостоверения личности ведется на странице **Тип документа**.</span><span class="sxs-lookup"><span data-stu-id="24b3c-114">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="24b3c-115">Чтобы определить новый тип удостоверяющего личность документа или просмотреть список существующих типов, выберите **Управление персоналом** &gt; **вкладка "Ссылки"** &gt; **Настройка** &gt; **Типы документов, удостоверяющих личность**.</span><span class="sxs-lookup"><span data-stu-id="24b3c-115">To define a new identification type or review the list of existing types, click **Personnel management** &gt; **Links tab** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="24b3c-116">Можно ввести простой код и описание.</span><span class="sxs-lookup"><span data-stu-id="24b3c-116">You can enter a simple code and description.</span></span> 

### <a name="if-youre-using-dynamics-365-for-talent"></a><span data-ttu-id="24b3c-117">Если вы используете Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="24b3c-117">If you're using Dynamics 365 for Talent</span></span>
<span data-ttu-id="24b3c-118">На вкладке **Идентификация** необходимо выбрать типы идентификации, представляющие идентификационные номера, перечисленные на странице.</span><span class="sxs-lookup"><span data-stu-id="24b3c-118">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="24b3c-119">Перед вводом идентификационных сведений для работников можно настроить типы документов, удостоверяющих личность.</span><span class="sxs-lookup"><span data-stu-id="24b3c-119">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="24b3c-120">Информация о номере социального обеспечения, идентификационном номере (для граждан и иностранцев) и коде удостоверения личности ведется на странице **Тип документа**.</span><span class="sxs-lookup"><span data-stu-id="24b3c-120">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="24b3c-121">Чтобы определить новый тип удостоверяющего личность документа или просмотреть список существующих типов, выберите **Управление персоналом** &gt; **Настройка** &gt; **Типы документов, удостоверяющих личность**.</span><span class="sxs-lookup"><span data-stu-id="24b3c-121">To define a new identification type or review the list of existing types, click **Human resources** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="24b3c-122">Можно ввести простой код и описание.</span><span class="sxs-lookup"><span data-stu-id="24b3c-122">You can enter a simple code and description.</span></span> 

<span data-ttu-id="24b3c-123">На вкладке **Номерные серии** можно выбрать номерные серии, используемые для следующих записей: табельный номер, должность, код запроса пользователя, документ по форме I-9, кандидат, обсуждение, код льготы и действие персонала (если этот тип записи включен).</span><span class="sxs-lookup"><span data-stu-id="24b3c-123">On the **Number sequences** tab, you can select the number sequences that are used for the following records: Personnel number, Position, User request ID, I-9 document, Applicant, Discussion, Benefit ID, and Personnel action (if this record type is enabled).</span></span> <span data-ttu-id="24b3c-124">Для ведения ссылок и кодов номерных серий используется страница списка **Номерные серии**.</span><span class="sxs-lookup"><span data-stu-id="24b3c-124">To maintain number sequence references and codes, use the **Number sequences** list page.</span></span> <span data-ttu-id="24b3c-125">Чтобы найти эту страницу, используйте функцию поиска страниц.</span><span class="sxs-lookup"><span data-stu-id="24b3c-125">To find this page, use the page search feature.</span></span> 

<span data-ttu-id="24b3c-126">На вкладке **Должности** укажите, доступны ли новые должности для назначения по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="24b3c-126">On the **Positions** tab, indicate whether new positions are available for assignment by default:</span></span>

-   <span data-ttu-id="24b3c-127">**Всегда** — можно назначать работников на новые должности при создании должностей.</span><span class="sxs-lookup"><span data-stu-id="24b3c-127">**Always** – You can assign workers to new positions when positions are created.</span></span> <span data-ttu-id="24b3c-128">При создании должностей в качестве даты и времени в поле **Доступна для назначения** на вкладке **Общее** страницы **Должность** автоматически устанавливаются дата и время создания.</span><span class="sxs-lookup"><span data-stu-id="24b3c-128">When positions are created, the **Available for assignment** date and time on the **General** tab of the **Position** page are automatically set to the creation date and time.</span></span>
-   <span data-ttu-id="24b3c-129">**Никогда** — назначать работников на новые должности при создании должностей нельзя.</span><span class="sxs-lookup"><span data-stu-id="24b3c-129">**Never** – You can't assign workers to new positions when positions are created.</span></span> <span data-ttu-id="24b3c-130">Если выбран этот параметр, вы должны открывать страницу **Должность** для каждой новой должности, когда она станет доступна, а затем на вкладке **Общее** ввести дату в поле **Доступна для назначения**, чтобы назначение работников на должность стало возможно.</span><span class="sxs-lookup"><span data-stu-id="24b3c-130">If you select this option, you must open the **Position** page for each new position as it becomes available, and then, on the **General** tab, enter the **Available for assignment** date to enable worker assignment.</span></span>


<a name="see-also"></a><span data-ttu-id="24b3c-131">См. также</span><span class="sxs-lookup"><span data-stu-id="24b3c-131">See also</span></span>
--------

[<span data-ttu-id="24b3c-132">Настройка параметров управления персоналом для конкретной компании</span><span class="sxs-lookup"><span data-stu-id="24b3c-132">Set up company specific HR parameters</span></span>](set-up-company-specific-hr-parameters.md)




