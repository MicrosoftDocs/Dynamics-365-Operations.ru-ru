---
title: Улучшенная обработка номенклатур с отслеженными партиями
description: В этом разделе описываются улучшения обработки партий для номенклатур с отслеженными партиями в процессе разноски журнала операций розничной торговли.
author: josaw1
manager: AnnBe
ms.date: 05/28/2019
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
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4456fc3d5bc4547fa8211642b11ca6df455fa187
ms.sourcegitcommit: aec1dcd44274e9b8d0770836598fde5533b7b569
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2019
ms.locfileid: "1617397"
---
# <a name="improved-handling-of-batch-tracked-items"></a><span data-ttu-id="9700b-103">Улучшенная обработка номенклатур с отслеженными партиями</span><span class="sxs-lookup"><span data-stu-id="9700b-103">Improved handling of batch-tracked items</span></span>

<span data-ttu-id="9700b-104">В Microsoft Dynamics 365 for Retail POS номера партий не могут быть зафиксированы для номенклатур с отслеженными партиями в момент продажи.</span><span class="sxs-lookup"><span data-stu-id="9700b-104">In Microsoft Dynamics 365 for Retail Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</span></span> <span data-ttu-id="9700b-105">Однако для определенных конфигураций, когда продажи разносятся в головном офисе с помощью заказов клиентов или разноски журнала операций, система Microsoft Dynamics ожидает, что существуют действительные номера партий для номенклатур с отслеженными партиями и что они будут использоваться во время процесса выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="9700b-105">However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</span></span>

<span data-ttu-id="9700b-106">Если для продуктов доступны действительные номера партий, они будут использоваться в процессе выставления накладных по заказам клиентов и процессе выставления накладных по заказам на продажу в результате разноски журнала операций.</span><span class="sxs-lookup"><span data-stu-id="9700b-106">If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</span></span> <span data-ttu-id="9700b-107">В противном случае в процессе выставления накладных по заказам клиентов не может выполняться разноска, и пользователь POS получает сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9700b-107">Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</span></span> <span data-ttu-id="9700b-108">Разноска журнала операций переходит в состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="9700b-108">Statement posting then goes into an error state.</span></span> <span data-ttu-id="9700b-109">Это состояние ошибки возникает даже в том случае, когда для продуктов включены отрицательные запасы.</span><span class="sxs-lookup"><span data-stu-id="9700b-109">This error state occurs even when negative inventory has been turned on for the products.</span></span>

<span data-ttu-id="9700b-110">Усовершенствования, внесенные в Microsoft Dynamics for Retail версии 10.0.4 и более поздних версиях, помогают гарантировать, что при включении отрицательного запаса для номенклатур с отслеженными партиями выставление накладных по заказам клиентов и выставление накладных по заказам на продажу в результате разноски журнала операций не блокируется для этих номенклатур, если запасы равны нулю (0) или номер партии недоступен.</span><span class="sxs-lookup"><span data-stu-id="9700b-110">Improvements that have been made in Microsoft Dynamics for Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</span></span> <span data-ttu-id="9700b-111">Новая функциональность использует код партии по умолчанию для строк продажи, если номера партий недоступны.</span><span class="sxs-lookup"><span data-stu-id="9700b-111">The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</span></span>

<span data-ttu-id="9700b-112">Чтобы определить код партии по умолчанию, используемый для заказов клиентов, на странице **Параметры розничной торговли** на вкладке **Заказы клиентов** на экспресс-вкладке **Заказ** задайте значение в поле **Код партии по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="9700b-112">To define the default batch ID that is used for customer orders, on the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, set the **Default batch id** field.</span></span>

<span data-ttu-id="9700b-113">Чтобы определить код партии по умолчанию, используемый для выставления накладных по заказам на продажу в результате разноски журнала операций, на странице **Параметры розничной торговли** на вкладке **Разноска** на экспресс-вкладке **Обновление запасов** задайте значение в поле **Код партии по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="9700b-113">To define the default batch ID that is used for sales order invoicing through statement posting, on the **Retail parameters** page, on the **Posting** tab, on the **Inventory update** FastTab, set the **Default batch id** field.</span></span>

> [!NOTE]
> <span data-ttu-id="9700b-114">Эта функциональность доступна только в том случае, если включены расширенные складские процессы для склада и номенклатур определенного магазина.</span><span class="sxs-lookup"><span data-stu-id="9700b-114">This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</span></span> <span data-ttu-id="9700b-115">В более позднем выпуске эта функциональность также будет поддерживаться для сценариев, в которых расширенное управление складом не используется.</span><span class="sxs-lookup"><span data-stu-id="9700b-115">In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</span></span>
