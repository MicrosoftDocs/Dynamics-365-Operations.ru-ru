---
title: Политики приемлемости льготы
description: В Этой статья представлена информация о политиках по праву на льготы, которые помогают определить, кто подходит для конкретных льготыт
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 5bd11e5dceb831968c8458ec07d2aca8fb660763
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898488"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="62a16-103">Политики приемлемости льготы</span><span class="sxs-lookup"><span data-stu-id="62a16-103">Benefit eligibility policies</span></span>

<span data-ttu-id="62a16-104">В этом разделе представлена информация о политиках по праву на льготы, которые помогают определить, кто подходит для конкретных льгот.</span><span class="sxs-lookup"><span data-stu-id="62a16-104">This topic provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="62a16-105">При создании льгот вы решаете, какие льготы будут доступны для каких сотрудников.</span><span class="sxs-lookup"><span data-stu-id="62a16-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="62a16-106">В следующей таблице представлены примеры льгот, которые можно сделать доступными для определенных сотрудников.</span><span class="sxs-lookup"><span data-stu-id="62a16-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="62a16-107">Льгота</span><span class="sxs-lookup"><span data-stu-id="62a16-107">Benefit</span></span>          | <span data-ttu-id="62a16-108">Получатель льготы</span><span class="sxs-lookup"><span data-stu-id="62a16-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="62a16-109">Медицинское страхование</span><span class="sxs-lookup"><span data-stu-id="62a16-109">Health insurance</span></span> | <span data-ttu-id="62a16-110">Все сотрудники</span><span class="sxs-lookup"><span data-stu-id="62a16-110">All employees</span></span>                   |
| <span data-ttu-id="62a16-111">Мобильный телефон</span><span class="sxs-lookup"><span data-stu-id="62a16-111">Mobile phone</span></span>     | <span data-ttu-id="62a16-112">Торговый персонал, руководители</span><span class="sxs-lookup"><span data-stu-id="62a16-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="62a16-113">Парковочные пропуска</span><span class="sxs-lookup"><span data-stu-id="62a16-113">Parking passes</span></span>   | <span data-ttu-id="62a16-114">Администрация</span><span class="sxs-lookup"><span data-stu-id="62a16-114">Executives</span></span>                      |

<span data-ttu-id="62a16-115">Следующие компоненты используются для создания политик приемлемости:</span><span class="sxs-lookup"><span data-stu-id="62a16-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="62a16-116">Типы правил политики</span><span class="sxs-lookup"><span data-stu-id="62a16-116">Policy rule types</span></span>
-   <span data-ttu-id="62a16-117">Политики приемлемости льготы</span><span class="sxs-lookup"><span data-stu-id="62a16-117">Benefit eligibility policies</span></span>

<span data-ttu-id="62a16-118">Типы правил политики определяют параметры запроса, которые используются при разработке определенных правил политики.</span><span class="sxs-lookup"><span data-stu-id="62a16-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="62a16-119">После создания типов правил политики можно создать политики приемлемости льготы.</span><span class="sxs-lookup"><span data-stu-id="62a16-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="62a16-120">Политики позволяют создавать коллекции правил, которые применяются к одному или нескольким юридическим лицам.</span><span class="sxs-lookup"><span data-stu-id="62a16-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="62a16-121">В пределах каждой политики можно просмотреть типы правил политики приемлемости льготы, созданные ранее.</span><span class="sxs-lookup"><span data-stu-id="62a16-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="62a16-122">Вы определяете объем правила в пределах политики.</span><span class="sxs-lookup"><span data-stu-id="62a16-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="62a16-123">Например, при создании типа правила политики льготы с именем **Руководители** можно указать, что правило находится в пределах этой политики.</span><span class="sxs-lookup"><span data-stu-id="62a16-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="62a16-124">В этом примере правило может указывать, что любая должность со словом "руководитель" должна быть включена в правило.</span><span class="sxs-lookup"><span data-stu-id="62a16-124">In this example, the rule might state that any job title that contains the word "executive" should be included in the rule.</span></span> <span data-ttu-id="62a16-125">После определения параметров правила или правил, которые включены в политику, можно назначить конкретное правило льготе.</span><span class="sxs-lookup"><span data-stu-id="62a16-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>

<a name="additional-resources"></a><span data-ttu-id="62a16-126">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="62a16-126">Additional resources</span></span>
--------

[<span data-ttu-id="62a16-127">Определение и управление программой льгот</span><span class="sxs-lookup"><span data-stu-id="62a16-127">Define and manage a benefits program</span></span>](manage-benefit-program.md)



