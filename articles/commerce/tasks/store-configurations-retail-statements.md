---
title: Конфигурации магазинов для журналов операций розничной торговли
description: Эта процедура показывает процесс настройки параметров розничного магазина, которые влияют на то, как создаются и разносятся журналы операций Commerce.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57081b9e737373641cd9d884919d03dcf62a2ffe
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140663"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="0e55f-103">Конфигурации магазинов для журналов операций розничной торговли</span><span class="sxs-lookup"><span data-stu-id="0e55f-103">Store configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e55f-104">Эта процедура показывает процесс настройки параметров розничного магазина, которые влияют на то, как создаются и разносятся журналы операций Commerce.</span><span class="sxs-lookup"><span data-stu-id="0e55f-104">This procedure walks through configurations for the store that affect how Commerce statements get created and posted.</span></span> <span data-ttu-id="0e55f-105">Финансовые аналитики рассматриваются в другой процедуре.</span><span class="sxs-lookup"><span data-stu-id="0e55f-105">Financial dimensions on stores are covered in another procedure.</span></span> <span data-ttu-id="0e55f-106">В данной процедуре используется демонстрационная компания USRT.</span><span class="sxs-lookup"><span data-stu-id="0e55f-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="0e55f-107">В области **Область переходов** выберите **Модули > Retail и Commerce > Каналы > Магазины > Все магазины**.</span><span class="sxs-lookup"><span data-stu-id="0e55f-107">In the **Navgiation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
2. <span data-ttu-id="0e55f-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="0e55f-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="0e55f-109">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="0e55f-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0e55f-110">Выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="0e55f-110">Click **Edit**.</span></span>
5. <span data-ttu-id="0e55f-111">Параметры на экспресс-вкладке **Операция/закрытие** влияют на создание, проверку и разноску журнала операций для магазина.</span><span class="sxs-lookup"><span data-stu-id="0e55f-111">The settings in the **Statement/closing** fastTab affect the statement creation, validation, and posting for the store.</span></span> <span data-ttu-id="0e55f-112">Разверните экспресс-вкладку **Операция/закрытие**.</span><span class="sxs-lookup"><span data-stu-id="0e55f-112">Expand the **Statement/closing** fastTab.</span></span>  
6. <span data-ttu-id="0e55f-113">В поле **Метод агрегирования операций** выберите метод, который будет использоваться для группировки строк журналов операций.</span><span class="sxs-lookup"><span data-stu-id="0e55f-113">In the **Statement method** field, select the method you want to use to to group the statement lines by.</span></span>  
7. <span data-ttu-id="0e55f-114">Выберите "Да" в параметре **Один журнал операций за день**, если при создании журналов операций с помощью пакетного задания нужно создавать только одну операцию на каждый день.</span><span class="sxs-lookup"><span data-stu-id="0e55f-114">Select "Yes" in **One statement per day** if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
8. <span data-ttu-id="0e55f-115">Поле **Создание декларации платежных средств** определяет, должны ли декларации платежных средств складываться или должна использоваться последняя из них.</span><span class="sxs-lookup"><span data-stu-id="0e55f-115">The **Tender declaration calculation** field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
9. <span data-ttu-id="0e55f-116">В поле **Округление** выберите счет ГК, на который требуется разносить значения разницы округления.</span><span class="sxs-lookup"><span data-stu-id="0e55f-116">In the **Rounding** field, select the ledger account to post rounding differences into.</span></span>  
10. <span data-ttu-id="0e55f-117">В поле **Максимальное расхождение при округлении** введите максимально допустимое расхождение при округлении.</span><span class="sxs-lookup"><span data-stu-id="0e55f-117">In the **Maximum rounding difference** field, enter the maximum rounding difference allowed.</span></span>
11. <span data-ttu-id="0e55f-118">В поле **Разноска** введите максимальное полное расхождение разноски, разрешенное для операции.</span><span class="sxs-lookup"><span data-stu-id="0e55f-118">In the **Posting** field, enter the maximum total posting difference allowed for a statement.</span></span>
12. <span data-ttu-id="0e55f-119">В поле **Смена** введите максимальное полное расхождение разноски, разрешенное для операции в пределах смены.</span><span class="sxs-lookup"><span data-stu-id="0e55f-119">In the **Shift** field, enter the maximum total difference within a shift in a statement.</span></span>  
13. <span data-ttu-id="0e55f-120">В поле **Транзакция** введите максимальное полное расхождение разноски, разрешенное для строки операции.</span><span class="sxs-lookup"><span data-stu-id="0e55f-120">In the **Transaction** field, enter the maximum total difference in a statement line.</span></span>  
14. <span data-ttu-id="0e55f-121">В поле **Способ закрытия** определите, должны ли транзакции, которые были включены в журнал операций, быть частью закрытой смены, или это могут быть либо транзакции в определенном диапазоне дат и времени.</span><span class="sxs-lookup"><span data-stu-id="0e55f-121">In the **Closing method** field, define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
15. <span data-ttu-id="0e55f-122">В поле **Конец рабочего дня** введите время предыдущего дня, на которое должны разноситься транзакции, которые имеют место после полуночи.</span><span class="sxs-lookup"><span data-stu-id="0e55f-122">In the **End of business day** field, enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
16. <span data-ttu-id="0e55f-123">Выберите "Да" в поле **Разнести как рабочий день**, если транзакции, произошедшие после полуночи, должны быть разнесены как часть предыдущего дня.</span><span class="sxs-lookup"><span data-stu-id="0e55f-123">Select "Yes" in **Post as business day** if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
17. <span data-ttu-id="0e55f-124">Выберите "Да" в поле **Разбить по методу агрегирования операций**, чтобы получить журналы операций, созданные для каждого из определенных методов агрегирования операций.</span><span class="sxs-lookup"><span data-stu-id="0e55f-124">Select "Yes" in **Split by Statement method** to get statements created for each statement method defined.</span></span> <span data-ttu-id="0e55f-125">Это может быть полезно, если требуется повысить производительность разноски для магазинов с высоким объемом проводок, т. к. в этом случае будет создаваться много небольших транзакций, которые можно обрабатывать параллельно.</span><span class="sxs-lookup"><span data-stu-id="0e55f-125">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
18. <span data-ttu-id="0e55f-126">На экспресс-вкладке **Общие** в поле **Клиент по умолчанию** можно выбрать счет клиента, который будет использоваться для продаж клиентам "с улицы".</span><span class="sxs-lookup"><span data-stu-id="0e55f-126">In the **General** fastTab, in the **Default customer** field, you can select the customer account to use for sales to walk-in customers.</span></span>  

