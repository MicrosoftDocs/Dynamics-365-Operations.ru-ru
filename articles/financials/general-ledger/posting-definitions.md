---
title: "Определения разносок"
description: "В Этой статья представлена информация об определениях разноски, и способах их определения и связывания. Для поддерживаемых типов проводок и документов можно использовать определения разноски вместо профилей разноски для классификации счетов ГК и финансовых аналитик по записям учета."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0148bd65bad2b5c947287d18289c08c7ef7f476f
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="posting-definitions"></a><span data-ttu-id="fff33-104">Определения разносок</span><span class="sxs-lookup"><span data-stu-id="fff33-104">Posting definitions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fff33-105">В Этой статья представлена информация об определениях разноски, и способах их определения и связывания.</span><span class="sxs-lookup"><span data-stu-id="fff33-105">This article provides information about posting definitions, and how to define and link them.</span></span> <span data-ttu-id="fff33-106">Для поддерживаемых типов проводок и документов можно использовать определения разноски вместо профилей разноски для классификации счетов ГК и финансовых аналитик по записям учета.</span><span class="sxs-lookup"><span data-stu-id="fff33-106">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span>

<span data-ttu-id="fff33-107">Для поддерживаемых типов проводок и документов можно использовать определения разноски вместо профилей разноски для классификации счетов ГК и финансовых аналитик по записям учета.</span><span class="sxs-lookup"><span data-stu-id="fff33-107">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span> <span data-ttu-id="fff33-108">Можно просматривать поддерживаемые типы документов и проводок на странице **Определения разноски проводок**.</span><span class="sxs-lookup"><span data-stu-id="fff33-108">You can view the supported documents and posting types on the **Transaction posting definitions** page.</span></span> 

<span data-ttu-id="fff33-109">Для начала использования определений разноски выберите параметр **Использовать определения разносок** на странице **Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="fff33-109">To start using posting definitions, select the **Use posting definitions** option on the **General ledger parameters** page.</span></span> <span data-ttu-id="fff33-110">Даже когда вы используете определения разноски, вы все равно должны определить профили разноски для возникающих записей и неподдерживаемых типов разноски и документов.</span><span class="sxs-lookup"><span data-stu-id="fff33-110">Even when you use posting definitions, you must still define posting profiles for the originating entries and non-supported posting types and documents.</span></span> 

<span data-ttu-id="fff33-111">Необходимо использовать определения разноски для включения учета бюджетных обязательств для заказов на покупку и учета предварительных бюджетных обязательств для заявок на покупку.</span><span class="sxs-lookup"><span data-stu-id="fff33-111">You must use posting definitions in order to enable encumbrance accounting for purchase orders and pre-encumbrance accounting for purchase requisitions.</span></span>

## <a name="defining-posting-definitions"></a><span data-ttu-id="fff33-112">Установка определений разносок</span><span class="sxs-lookup"><span data-stu-id="fff33-112">Defining posting definitions</span></span>
<span data-ttu-id="fff33-113">Используйте странице **Определение разноски** для того, чтобы определить критерии сопоставления и определить записи, которые должны создаваться при возникновении соответствия.</span><span class="sxs-lookup"><span data-stu-id="fff33-113">Use the **Posting definitions** page to specify the match criteria and define the entries that should be generated when a match occurs.</span></span> <span data-ttu-id="fff33-114">Критерии сопоставления оцениваются для возникающих записей как распределения по бухгалтерским счетам.</span><span class="sxs-lookup"><span data-stu-id="fff33-114">The match criteria are evaluated for the originating entries as accounting distributions.</span></span> 

<span data-ttu-id="fff33-115">На странице **Определения разноски** можно также присвоить приоритетные номера для управления порядком оценки строк.</span><span class="sxs-lookup"><span data-stu-id="fff33-115">On the **Posting definitions** page, you can also assign priority numbers to entry lines to control the order in which the lines are evaluated.</span></span> <span data-ttu-id="fff33-116">Строки с наименьшим приоритетным номером оцениваются в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="fff33-116">The lines that have the lowest priority number are evaluated first.</span></span> <span data-ttu-id="fff33-117">Например, все строки с приоритетом 1 оцениваются, а затем оцениваются строки с приоритетом 2 и так далее.</span><span class="sxs-lookup"><span data-stu-id="fff33-117">For example, all lines that have a priority of 1 are evaluated, and then lines that have a priority of 2, and so on.</span></span> <span data-ttu-id="fff33-118">При обнаружении совпадения другие критерии соответствия игнорируется.</span><span class="sxs-lookup"><span data-stu-id="fff33-118">When a match is found, the other match criteria are ignored.</span></span> <span data-ttu-id="fff33-119">Кроме того, только критерии в группе, которые соответствуют исходной проводке, создают записи.</span><span class="sxs-lookup"><span data-stu-id="fff33-119">Additionally, only the criteria in the group that match the originating transaction create generated entries.</span></span> 

<span data-ttu-id="fff33-120">Вы можете проверить свои определения разноски с помощью мастера **Проверка определения разноски**.</span><span class="sxs-lookup"><span data-stu-id="fff33-120">You can validate your posting definitions by using the **Test posting definition** wizard.</span></span> <span data-ttu-id="fff33-121">После определения образца возникающей записи для определения разноски вы увидите созданные записи.</span><span class="sxs-lookup"><span data-stu-id="fff33-121">After you define a sample originating entry for a posting definition, you'll see the generated entries.</span></span> 

<span data-ttu-id="fff33-122">Можно использовать версии определения разноски вместе с датами действия.</span><span class="sxs-lookup"><span data-stu-id="fff33-122">You can use posting definition versions together with effective dates.</span></span> <span data-ttu-id="fff33-123">Например, можно создать будущую версию определения разноски для разноски на другой счет ГК в новом финансовом году.</span><span class="sxs-lookup"><span data-stu-id="fff33-123">For example, you can create a future version of a posting definition to post to a different ledger account in a new fiscal year.</span></span> 

<span data-ttu-id="fff33-124">Используйте страницу **Определения разноски проводок** для того, чтобы задать определения разноски для типов проводок.</span><span class="sxs-lookup"><span data-stu-id="fff33-124">Use the **Transaction posting definitions** page to assign posting definitions to transaction types.</span></span>

## <a name="linking-posting-definitions"></a><span data-ttu-id="fff33-125">Связывание определений разносок</span><span class="sxs-lookup"><span data-stu-id="fff33-125">Linking posting definitions</span></span>
<span data-ttu-id="fff33-126">При создании определений разноски можно создать связь от одного определения разноски к другому.</span><span class="sxs-lookup"><span data-stu-id="fff33-126">You can link from one posting definition to another when you create posting definitions.</span></span> <span data-ttu-id="fff33-127">Критерии для определения, к которому ведет связь, рассматриваются в дополнение к критериям для текущего определения разноски.</span><span class="sxs-lookup"><span data-stu-id="fff33-127">The criteria for the definition that you linked to are then considered in addition to the criteria for the current posting definition.</span></span> <span data-ttu-id="fff33-128">Это позволяет экономить время, так как нет необходимости в повторном вводе критериев на экспресс-вкладке **Записи** на странице **Определения разноски** для текущего определения разноски, если эти строки уже были введены для другого определения.</span><span class="sxs-lookup"><span data-stu-id="fff33-128">This feature helps save you time, because you don't have to reenter criteria on the **Entries** FastTab on the **Posting definitions** page for the current posting definition if you already entered those lines for another definition.</span></span> 

<span data-ttu-id="fff33-129">Ссылки, которые могут использоваться, должны быть включены на схемах или в таблицах.</span><span class="sxs-lookup"><span data-stu-id="fff33-129">In the diagrams or tables, include any links that you might use.</span></span> <span data-ttu-id="fff33-130">Убедитесь, что строки во всех определениях разноски, к которым ведет связь, являются уникальными для предотвращения конфликтов с текущим определением разноски.</span><span class="sxs-lookup"><span data-stu-id="fff33-130">To avoid conflicts with the current posting definition, make sure that the lines in any posting definitions that you link to are unique.</span></span> 

<span data-ttu-id="fff33-131">При создании ссылок в определениях разноски применяются следующие ограничения:</span><span class="sxs-lookup"><span data-stu-id="fff33-131">The following restrictions apply when you create links in posting definitions:</span></span>

-   <span data-ttu-id="fff33-132">Любое определение разноски может вести к другому определению разноски, или к нему может вести ссылка из другого определения разноски, но не оба варианта одновременно.</span><span class="sxs-lookup"><span data-stu-id="fff33-132">A given posting definition can either link to another posting definition or be linked to from another posting definition, but not both.</span></span> <span data-ttu-id="fff33-133">Однако определение разноски может вести к нескольким определениям разноски.</span><span class="sxs-lookup"><span data-stu-id="fff33-133">However, a posting definition can link to multiple posting definitions.</span></span>
-   <span data-ttu-id="fff33-134">Ссылки можно настроить только в определениях разноски, находящихся в одном модуле.</span><span class="sxs-lookup"><span data-stu-id="fff33-134">You can set up links only among posting definitions that are in the same module.</span></span>
-   <span data-ttu-id="fff33-135">Можно назначить определение разноски для любого типа проводок, однако тип проводки должен находиться в том же модуле, что и определение разноски.</span><span class="sxs-lookup"><span data-stu-id="fff33-135">You can assign a posting definition to any transaction type, but the transaction type must be in the same module as the posting definition.</span></span> <span data-ttu-id="fff33-136">Используйте страницу **Определения разноски проводок** для того, чтобы увидеть, в каком модуле находится тип проводки.</span><span class="sxs-lookup"><span data-stu-id="fff33-136">Use the **Transaction posting definitions** page to see what module a transaction type is in.</span></span>


<span data-ttu-id="fff33-137">Дополнительных сведений см. в разделе [Примеры определений разноски](example-posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="fff33-137">For more information, see [Posting definitions examples](example-posting-definitions.md).</span></span> 



