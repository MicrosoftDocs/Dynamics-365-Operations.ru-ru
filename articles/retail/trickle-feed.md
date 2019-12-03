---
title: Поточное создание заказов по проводкам розничного магазина
description: В этом разделе описана процедура поточного создания заказов по проводкам розничного магазина в Microsoft Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: deb8399aa401af16b6fe123a433eb21864e178c6
ms.sourcegitcommit: 92322167f57b66d2accc134aaf862e6b9931ec94
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2019
ms.locfileid: "2693097"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a><span data-ttu-id="18e71-103">Поточное создание заказов по проводкам розничного магазина (общедоступная предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="18e71-103">Trickle feed-based order creation for retail store transactions (Public preview)</span></span>

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="18e71-104">В Dynamics 365 Retail 10.0.4 и более ранних версий разноска журналов операций розничной торговли выполняется в конце каждого дня.</span><span class="sxs-lookup"><span data-stu-id="18e71-104">In Dynamics 365 Retail versions 10.0.4 and earlier, retail statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="18e71-105">При этом большие проводки должны быть обработаны за ограниченное время, что иногда приводит к перегрузке, блокировкам и сбоям в процессе разноски.</span><span class="sxs-lookup"><span data-stu-id="18e71-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="18e71-106">Кроме того, при этом невозможно отслеживать доходы и платежи в бухгалтерских книгах в течение дня.</span><span class="sxs-lookup"><span data-stu-id="18e71-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="18e71-107">В общедоступной публичной версии Retail 10.0.5 появилась функция поточного создания заказов, позволяющая обрабатывать проводки в течение дня, а в конце дня выполнять только финансовую выверку платежных средств и других операций с наличными.</span><span class="sxs-lookup"><span data-stu-id="18e71-107">With the public preview of trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="18e71-108">Эта функция распределяет нагрузку по созданию заказов на продажу, накладных и платежей на весь день, упрощая отслеживание результатов и позволяя отражать доходы и платежи в книгах почти в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="18e71-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="18e71-109">Как использовать поточную разноску</span><span class="sxs-lookup"><span data-stu-id="18e71-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="18e71-110">Чтобы включить поточную разноску проводок розничной торговли, выберите **Администрирование системы > Настройка > Конфигурация лицензии** и отключите ключ **Журналы операций розничной торговли**.</span><span class="sxs-lookup"><span data-stu-id="18e71-110">To enable trickle feed-based posting of retail transactions, go to **System administration > Set up > License configuration** and disable the the **Retail statements** key.</span></span>

2. <span data-ttu-id="18e71-111">На той же странице включите ключ лицензии **Журналы операций розничной торговли (поточная разноска) — предварительная версия**.</span><span class="sxs-lookup"><span data-stu-id="18e71-111">On the same page, enable the **Retail statements (trickle feed) – Preview** license key.</span></span> <span data-ttu-id="18e71-112">При включении этого ключа убедитесь в отсутствии ожидающих разноски журналов операций.</span><span class="sxs-lookup"><span data-stu-id="18e71-112">When you enable this key, make sure there are no pending statements waiting to be posted.</span></span> 

> [!Important]
> <span data-ttu-id="18e71-113">Перед включением ключа лицензии **Журналы операций розничной торговли (поточная разноска) — предварительная версия** убедитесь в отсутствии ожидающих разноски журналов операций.</span><span class="sxs-lookup"><span data-stu-id="18e71-113">Before you enable the **Retail statements (trickle feed) – Preview** license key, make sure that no pending statements are waiting to be posted.</span></span>

3. <span data-ttu-id="18e71-114">Текущий журнал операций будет разбит на два: журнал проводок и финансовый отчет.</span><span class="sxs-lookup"><span data-stu-id="18e71-114">The current statement document will be split into two different types; transactional statement and financial statement.</span></span>

      - <span data-ttu-id="18e71-115">В журнале проводок будут собраны все неразнесенные и проверенные проводки розничной торговли для создания с заданной периодичностью заказов на продажу, накладных по продаже, журналов платежей и скидок и проводок по доходам/расходам.</span><span class="sxs-lookup"><span data-stu-id="18e71-115">The transactional statement will pick up all unposted and validated retail transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="18e71-116">Необходимо настроить этот процесс на частое выполнение, чтобы документы создавались при загрузке проводок розничной торговли в Retail Headquarters через P-задание.</span><span class="sxs-lookup"><span data-stu-id="18e71-116">You should configure this process to run at a high frequency so that documents are created when the retail transactions are uploaded into Retail Headquarters through the P-job.</span></span> <span data-ttu-id="18e71-117">Поскольку журнал проводок уже создает заказы на продажу и накладные по продаже, настраивать пакетное задание **Разнести запасы** больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="18e71-117">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="18e71-118">Однако его все равно можно использовать при необходимости.</span><span class="sxs-lookup"><span data-stu-id="18e71-118">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="18e71-119">Финансовый отчет должен создаваться в конце дня и поддерживает только способ закрытия **Смена**.</span><span class="sxs-lookup"><span data-stu-id="18e71-119">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="18e71-120">Это отчет служит только для финансовой выверки и создания журналов для разниц между суммами инвентаризации и суммами проводок по различным платежным средствам, а также журналов для других проводок управления кассой.</span><span class="sxs-lookup"><span data-stu-id="18e71-120">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

4. <span data-ttu-id="18e71-121">Чтобы сформировать журнал проводок, выберите **Розничная торговля > ИТ розничной торговли > Разноска POS > Пакетный расчет журналов проводок**.</span><span class="sxs-lookup"><span data-stu-id="18e71-121">To calculate the transactional statement, click **Retail > Retail IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="18e71-122">Чтобы разнести журналы проводок в пакетном режиме, выберите **Розничная торговля > ИТ розничной торговли > Разноска POS > Пакетная разноска журналов проводок**.</span><span class="sxs-lookup"><span data-stu-id="18e71-122">To post the transactional statement statements in batch, click **Retail > Retail IT > POS Posting > Post transactional statements in batch**.</span></span>

5. <span data-ttu-id="18e71-123">Чтобы сформировать финансовый отчет, выберите **Розничная торговля > ИТ розничной торговли > Разноска POS > Пакетный расчет финансовых отчетов**.</span><span class="sxs-lookup"><span data-stu-id="18e71-123">To calculate the financial statement, click **Retail > Retail IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="18e71-124">Чтобы разнести финансовые отчеты в пакетном режиме, выберите **Розничная торговля > ИТ розничной торговли > Разноска POS > Пакетная разноска финансовых отчетов**.</span><span class="sxs-lookup"><span data-stu-id="18e71-124">To post the financial statements in batch, click **Retail > Retail IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="18e71-125">Пункты меню **Розничная торговля > ИТ розничной торговли > Разноска POS > Пакетный расчет журналов операций** и **Розничная торговля > ИТ розничной торговли > Разноска POS > Пакетная разноска журналов операций** будут удалены с появлением этой новой функции.</span><span class="sxs-lookup"><span data-stu-id="18e71-125">The menu items **Retail > Retail IT > POS Posting > Calculate statements in batch** and **Retail > Retail IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="18e71-126">Кроме того, журналы проводок и финансовые отчеты можно создавать вручную.</span><span class="sxs-lookup"><span data-stu-id="18e71-126">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="18e71-127">Выберите **Розничная торговля > Каналы > Розничные магазины**, а затем — **Журналы операций розничной торговли**.</span><span class="sxs-lookup"><span data-stu-id="18e71-127">Go to **Retail > Channels > Retail stores** and click **Retail statements**.</span></span> <span data-ttu-id="18e71-128">Щелкните **Создать**, затем выберите тип журнала операций, который требуется создать.</span><span class="sxs-lookup"><span data-stu-id="18e71-128">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="18e71-129">В полях на странице **Журналы операций розничной торговли** и действиях раздела **Группа журналов** будут показаны данные и действия, соответствующие выбранному типу журнала.</span><span class="sxs-lookup"><span data-stu-id="18e71-129">Fields on the **Retail statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>
