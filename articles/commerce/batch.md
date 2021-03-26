---
title: Улучшенная обработка номенклатур с отслеженными партиями
description: В этом разделе описываются улучшения обработки партий для номенклатур с отслеженными партиями в процессе разноски журнала операций.
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 00e1fcb36d685798f3ad7d667805c97bddcceb36
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211161"
---
# <a name="improved-handling-of-batch-tracked-items"></a><span data-ttu-id="e5eae-103">Улучшенная обработка номенклатур с отслеженными партиями</span><span class="sxs-lookup"><span data-stu-id="e5eae-103">Improved handling of batch-tracked items</span></span>


[!include [banner](includes/banner.md)]


<span data-ttu-id="e5eae-104">В POS номера партий не могут быть зафиксированы для номенклатур с отслеженными партиями в момент продажи.</span><span class="sxs-lookup"><span data-stu-id="e5eae-104">In Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</span></span> <span data-ttu-id="e5eae-105">Однако для определенных конфигураций, когда продажи разносятся в головном офисе с помощью заказов клиентов или разноски журнала операций, система Microsoft Dynamics ожидает, что существуют действительные номера партий для номенклатур с отслеженными партиями и что они будут использоваться во время процесса выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="e5eae-105">However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</span></span>

<span data-ttu-id="e5eae-106">Если для продуктов доступны действительные номера партий, они будут использоваться в процессе выставления накладных по заказам клиентов и процессе выставления накладных по заказам на продажу в результате разноски журнала операций.</span><span class="sxs-lookup"><span data-stu-id="e5eae-106">If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</span></span> <span data-ttu-id="e5eae-107">В противном случае в процессе выставления накладных по заказам клиентов не может выполняться разноска, и пользователь POS получает сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="e5eae-107">Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</span></span> <span data-ttu-id="e5eae-108">Разноска журнала операций переходит в состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="e5eae-108">Statement posting then goes into an error state.</span></span> <span data-ttu-id="e5eae-109">Это состояние ошибки возникает даже в том случае, когда для продуктов включены отрицательные запасы.</span><span class="sxs-lookup"><span data-stu-id="e5eae-109">This error state occurs even when negative inventory has been turned on for the products.</span></span>

<span data-ttu-id="e5eae-110">Усовершенствования, внесенные в Retail версии 10.0.4 и более поздних версий нужны, чтобы гарантировать, что при включении отрицательного запаса для номенклатур с отслеженными партиями выставление накладных по заказам клиентов и выставление накладных по заказам на продажу в результате разноски журнала операций не блокируется для этих номенклатур, если запасы равны 0 (нулю) или номер партии недоступен.</span><span class="sxs-lookup"><span data-stu-id="e5eae-110">Improvements that have been made in Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</span></span> <span data-ttu-id="e5eae-111">Новая функциональность использует код партии по умолчанию для строк продажи, если номера партий недоступны.</span><span class="sxs-lookup"><span data-stu-id="e5eae-111">The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</span></span>

<span data-ttu-id="e5eae-112">Чтобы определить код партии по умолчанию, используемый для заказов клиентов, на странице **Параметры Commerce** на вкладке **Заказы клиентов** на экспресс-вкладке **Заказ** задайте значение в поле **Код партии по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="e5eae-112">To define the default batch ID that is used for customer orders, on the **Commerce parameters** page, on the **Customer orders** tab, on the **Order** FastTab, set the **Default batch id** field.</span></span>

<span data-ttu-id="e5eae-113">Чтобы определить код партии по умолчанию, используемый для выставления накладных по заказам на продажу в результате разноски журнала операций, на странице **Параметры Commerce** на вкладке **Разноска** на экспресс-вкладке **Обновление запасов** задайте значение в поле **Код партии по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="e5eae-113">To define the default batch ID that is used for sales order invoicing through statement posting, on the **Commerce parameters** page, on the **Posting** tab, on the **Inventory update** FastTab, set the **Default batch id** field.</span></span>

> [!NOTE]
> <span data-ttu-id="e5eae-114">Эта функциональность доступна только в том случае, если включены расширенные складские процессы для склада и номенклатур определенного магазина.</span><span class="sxs-lookup"><span data-stu-id="e5eae-114">This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</span></span> <span data-ttu-id="e5eae-115">В более позднем выпуске эта функциональность также будет поддерживаться для сценариев, в которых расширенное управление складом не используется.</span><span class="sxs-lookup"><span data-stu-id="e5eae-115">In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</span></span>

> [!NOTE]
> <span data-ttu-id="e5eae-116">Поддержка улучшенной обработки номенклатур с отслеженными партиями при разноске журнала операций для простых процессов управления складом, появившихся в Retail версии 10.0.5.</span><span class="sxs-lookup"><span data-stu-id="e5eae-116">Support for improved handling of batch-tracked items during statement posting for non-advanced warehouse management scenarios was introduced in Retail version 10.0.5.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]