--- 
title: "Конфигурации магазинов для журналов операций розничной торговли"
description: "Эта процедура показывает процесс настройки параметров розничного магазина, которые влияют на то, как создаются и разносятся журналы операций розницы."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 441ba692f559f9966f3e2512c7760ad2f732b768
ms.contentlocale: ru-ru
ms.lasthandoff: 02/07/2018

---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="4084b-103">Конфигурации магазинов для журналов операций розничной торговли</span><span class="sxs-lookup"><span data-stu-id="4084b-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="4084b-104">Эта процедура показывает процесс настройки параметров розничного магазина, которые влияют на то, как создаются и разносятся журналы операций розницы.</span><span class="sxs-lookup"><span data-stu-id="4084b-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="4084b-105">Финансовые аналитики в розничных магазинах рассматриваются в другой процедуре.</span><span class="sxs-lookup"><span data-stu-id="4084b-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="4084b-106">В данной процедуре используется демонстрационная компания USRT.</span><span class="sxs-lookup"><span data-stu-id="4084b-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="4084b-107">Перейдите в раздел Розничная торговля и коммерция > Каналы > Магазины розничной торговли > Все розничные магазины.</span><span class="sxs-lookup"><span data-stu-id="4084b-107">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="4084b-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="4084b-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="4084b-109">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="4084b-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4084b-110">Параметры в разделе "Операция/закрытие" влияют на создание, проверку и разноску журнала операций для магазина.</span><span class="sxs-lookup"><span data-stu-id="4084b-110">The settings in the Statement/closing section affect the statement creation, validation, and posting for the store.</span></span>  <span data-ttu-id="4084b-111">Откройте раздел "Операция/закрытие".</span><span class="sxs-lookup"><span data-stu-id="4084b-111">Open the Statement/closing section.</span></span>  
    * <span data-ttu-id="4084b-112">Выберите метод, который будет использоваться для группировки строк журналов операций.</span><span class="sxs-lookup"><span data-stu-id="4084b-112">Select the method you want to use to group the statement lines by.</span></span>  
    * <span data-ttu-id="4084b-113">Выберите "Да", если при создании журналов операций с помощью пакетного задания нужно создавать только одну операцию на каждый день.</span><span class="sxs-lookup"><span data-stu-id="4084b-113">Select "Yes" if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
    * <span data-ttu-id="4084b-114">Поле "Создание декларации платежных средств" определяет, должны ли декларации платежных средств складываться или должна использоваться последняя из них.</span><span class="sxs-lookup"><span data-stu-id="4084b-114">The Tender declaration calculation field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
    * <span data-ttu-id="4084b-115">Выберите счет ГК для разноски расхождения при округлении.</span><span class="sxs-lookup"><span data-stu-id="4084b-115">Select the ledger account to post rounding differences into.</span></span>  
    * <span data-ttu-id="4084b-116">В поле максимального расхождения при округлении можно ввести максимально допустимое расхождение при округлении.</span><span class="sxs-lookup"><span data-stu-id="4084b-116">In the Maximum rounding difference field, you can enter the maximum rounding difference allowed.</span></span>  
    * <span data-ttu-id="4084b-117">В поле "Разноска" можно ввести максимальное полное расхождение разноски, разрешенное для операции.</span><span class="sxs-lookup"><span data-stu-id="4084b-117">In the Posting field, you can enter the maximum total posting difference allowed for a statement.</span></span>  
    * <span data-ttu-id="4084b-118">В поле "Смена" можно ввести максимальное полное расхождение разноски, разрешенное для операции в пределах смены.</span><span class="sxs-lookup"><span data-stu-id="4084b-118">In the Shift field, you can enter the maximum total difference within a shift in a statement.</span></span>  
    * <span data-ttu-id="4084b-119">В поле "Транзакция" можно ввести максимальное полное расхождение разноски, разрешенное для строки операции.</span><span class="sxs-lookup"><span data-stu-id="4084b-119">In the Transaction field, you can enter the maximum total difference in a statement line.</span></span>  
    * <span data-ttu-id="4084b-120">В поле "Способ закрытия" можно определить, должны ли транзакции, которые были включены в журнал операций, быть частью закрытой смены, или это могут быть либо транзакции в определенном диапазоне дат и времени.</span><span class="sxs-lookup"><span data-stu-id="4084b-120">In the Closing method field, you can define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
    * <span data-ttu-id="4084b-121">В поле "Конец рабочего дня" можно ввести время предыдущего дня, на которое должны разноситься транзакции, которые имеют место после полуночи.</span><span class="sxs-lookup"><span data-stu-id="4084b-121">In the End of business day field, you can enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
    * <span data-ttu-id="4084b-122">Выберите "Да", если транзакции, произошедшие после полуночи, должны быть разнесены как часть предыдущего дня.</span><span class="sxs-lookup"><span data-stu-id="4084b-122">Select "Yes" if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
    * <span data-ttu-id="4084b-123">Выберите "да", чтобы получить журналы операций, созданные для каждого из определенных методов агрегирования операций.</span><span class="sxs-lookup"><span data-stu-id="4084b-123">Select "Yes" to get statements created for each statement method defined.</span></span> <span data-ttu-id="4084b-124">Это может быть полезно, если требуется повысить производительность разноски для магазинов с высоким объемом проводок, т. к. в этом случае будет создаваться много небольших транзакций, которые можно обрабатывать параллельно.</span><span class="sxs-lookup"><span data-stu-id="4084b-124">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
    * <span data-ttu-id="4084b-125">В поле "Клиент по умолчанию" можно выбрать счет клиента, который будет использоваться для продаж клиентам "с улицы".</span><span class="sxs-lookup"><span data-stu-id="4084b-125">In the Default customer field, you can select the customer account to use for sales to walk-in customers.</span></span>  


