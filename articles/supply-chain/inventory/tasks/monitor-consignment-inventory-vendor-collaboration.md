---
title: Мониторинг консигнационных запасов в рамках совместной работы с поставщиком
description: Эта процедура показывает порядок использования совместной работы с поставщиками для просмотра сведений об уровне запасов продукта, который был помещен в коносамент у клиента.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8186b553e8518f3153bfd88b89121d4b0567501b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "329444"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a><span data-ttu-id="f2a9a-103">Мониторинг консигнационных запасов в рамках совместной работы с поставщиком</span><span class="sxs-lookup"><span data-stu-id="f2a9a-103">Monitor consignment inventory using vendor collaboration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2a9a-104">Эта процедура показывает порядок использования совместной работы с поставщиками для просмотра сведений об уровне запасов продукта, который был помещен в коносамент у клиента.</span><span class="sxs-lookup"><span data-stu-id="f2a9a-104">This procedure shows how to use vendor collaboration to see information about the stock level of product that you have placed in consignment with a customer.</span></span> <span data-ttu-id="f2a9a-105">Вы также можете контролировать потребление запасов, когда клиент принимает на себя владение запасами.</span><span class="sxs-lookup"><span data-stu-id="f2a9a-105">You can also monitor the consumption of the stock when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="f2a9a-106">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="f2a9a-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="f2a9a-107">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="f2a9a-107">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="view-consumed-inventory"></a><span data-ttu-id="f2a9a-108">Просмотр израсходованных запасов</span><span class="sxs-lookup"><span data-stu-id="f2a9a-108">View consumed inventory</span></span>
1. <span data-ttu-id="f2a9a-109">Перейдите в раздел "Совместная работа с поставщиками" > "Консигнационные запасы" > "Продукты, полученные из консигнационных запасов".</span><span class="sxs-lookup"><span data-stu-id="f2a9a-109">Go to Vendor collaboration > Consignment inventory > Products received from consignment inventory.</span></span>
    * <span data-ttu-id="f2a9a-110">В списке отображаются строки поступления продуктов, которые были созданы при изменении владельца консигнационных запасов с поставщика на клиента.</span><span class="sxs-lookup"><span data-stu-id="f2a9a-110">The list shows the product receipt lines that were generated when ownership of the consignment inventory was changed from the vendor to the customer.</span></span> <span data-ttu-id="f2a9a-111">Может потребоваться прокрутить вправо, чтобы просмотреть количества и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="f2a9a-111">You might have to scroll to the right to see quantities and other information.</span></span> <span data-ttu-id="f2a9a-112">Можно использовать сведения в этом списке для создании накладных для клиента.</span><span class="sxs-lookup"><span data-stu-id="f2a9a-112">You can use the information in this list to generate invoices for your customer.</span></span> <span data-ttu-id="f2a9a-113">Также можно экспортировать данные в Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="f2a9a-113">You can also export the data to Microsoft Excel.</span></span>   
2. <span data-ttu-id="f2a9a-114">Щелкните "Просмотр заказа на покупку".</span><span class="sxs-lookup"><span data-stu-id="f2a9a-114">Click View purchase order.</span></span>
3. <span data-ttu-id="f2a9a-115">Разверните раздел "Сведения о строке".</span><span class="sxs-lookup"><span data-stu-id="f2a9a-115">Expand the Line details section.</span></span>
    * <span data-ttu-id="f2a9a-116">Строка помечается как коносамент, и в разделе заголовка указывается, что заказ на покупку имеет статус "Получено".</span><span class="sxs-lookup"><span data-stu-id="f2a9a-116">The line is marked as Consignment, and the header section shows that the purchase order has a status of Received.</span></span>  
4. <span data-ttu-id="f2a9a-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f2a9a-117">Close the page.</span></span>

## <a name="view-on-hand-inventory"></a><span data-ttu-id="f2a9a-118">Просмотр запасов в наличии</span><span class="sxs-lookup"><span data-stu-id="f2a9a-118">View on-hand inventory</span></span>
1. <span data-ttu-id="f2a9a-119">Перейдите в раздел "Совместная работа с поставщиками" > "Консигнационные запасы" > "Консигнационные запасы в наличии".</span><span class="sxs-lookup"><span data-stu-id="f2a9a-119">Go to Vendor collaboration > Consignment inventory > On-hand consignment inventory.</span></span>
    * <span data-ttu-id="f2a9a-120">Страница "Консигнационные запасы в наличии" показывает запасы, принадлежащие вам на складе клиента.</span><span class="sxs-lookup"><span data-stu-id="f2a9a-120">The On-hand consignment inventory page shows the stock that you own at the customer’s warehouse.</span></span> <span data-ttu-id="f2a9a-121">Можно показать дополнительные аналитики, такие как сайт и склад, выбрав вкладку "Отобразить аналитики".</span><span class="sxs-lookup"><span data-stu-id="f2a9a-121">You can show additional dimensions, such as the site and warehouse, by clicking the Display dimensions tab.</span></span>   

