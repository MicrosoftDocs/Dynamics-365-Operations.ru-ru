---
title: "Объекты обслуживания"
description: "Объекты сервисного обслуживания — это основные средства и продукты клиента, сервисное обслуживание которых вы можете выполнить."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0f7b63393085858c5ff4c64ebdf5d64b3c3ccdef
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---

# <a name="service-objects"></a><span data-ttu-id="0eb08-103">Объекты обслуживания</span><span class="sxs-lookup"><span data-stu-id="0eb08-103">Service objects</span></span> 

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="0eb08-104">Объекты сервисного обслуживания — это основные средства и продукты клиента, сервисное обслуживание которых вы можете выполнить.</span><span class="sxs-lookup"><span data-stu-id="0eb08-104">Service objects are a customer’s assets and products for which you can perform a service.</span></span> <span data-ttu-id="0eb08-105">В зависимости от типа предоставляемых услуг объекты могут быть материальными и нематериальными:</span><span class="sxs-lookup"><span data-stu-id="0eb08-105">Depending on the type of service you provide, objects can be tangible or intangible:</span></span>

-  <span data-ttu-id="0eb08-106">Материальные объекты - это предметы, например, станок или здание, в отношении которого вы выполняете задачу физического обслуживания.</span><span class="sxs-lookup"><span data-stu-id="0eb08-106">Tangible objects are things, such as a machine or a building, on which you can perform a physical service task.</span></span>

    <span data-ttu-id="0eb08-107">Материальным объектом сервисного обслуживания может быть складируемая номенклатура, которая создается в форме "Сведения об используемом продукте".</span><span class="sxs-lookup"><span data-stu-id="0eb08-107">A tangible service object can also be an inventory item that you create in the Released product details form.</span></span> <span data-ttu-id="0eb08-108">В зависимости от группы складских аналитик, присоединенной к номенклатуре, можно создать объект сервисного обслуживания с уровнем детализации, который включает серийный номер номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="0eb08-108">Depending on the inventory dimension group that you attach to the item, you can create a service object to a level of detail that includes the item serial number.</span></span> <span data-ttu-id="0eb08-109">Это полезно, когда требуется отслеживать точную номенклатуру, которую представляет объект сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="0eb08-109">This is useful when you must keep track of the exact item that the service object represents.</span></span>

    <span data-ttu-id="0eb08-110">Материальным объектом сервисного обслуживания также может быть номенклатура, которая не связана напрямую с продукцией компании или ее цепочкой поставок.</span><span class="sxs-lookup"><span data-stu-id="0eb08-110">A tangible service object can also be an item that is not directly related to a company's direct production or supply chain.</span></span> <span data-ttu-id="0eb08-111">Например, набор инструментов, используемый для проведения ремонта по заказу на сервисное обслуживание, не включенный в запасы.</span><span class="sxs-lookup"><span data-stu-id="0eb08-111">For example, a tool kit that is used for repairs in a service order can be a service object that is not included in inventory.</span></span> <span data-ttu-id="0eb08-112">В этом случае он не регистрируется как складируемая номенклатура.</span><span class="sxs-lookup"><span data-stu-id="0eb08-112">In this case, you don’t register it as an inventory item.</span></span>

-  <span data-ttu-id="0eb08-113">К нематериальным объектам относятся нефизические сущности, такие как набор счетов или юридический документ, в отношении которых выполняется задача сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="0eb08-113">Intangible objects are nonphysical things, such as a set of accounts or a legal document, on which you can perform a service task.</span></span>

## <a name="example-of-an-intangible-service-object"></a><span data-ttu-id="0eb08-114">Пример нематериального объекта сервисного обслуживания</span><span class="sxs-lookup"><span data-stu-id="0eb08-114">Example of an intangible service object</span></span>

<span data-ttu-id="0eb08-115">Компания A создает финансовые записи для нескольких небольших компаний.</span><span class="sxs-lookup"><span data-stu-id="0eb08-115">Company A maintains the financial records for several small companies.</span></span> <span data-ttu-id="0eb08-116">Одним из клиентов компании A является местная футбольная команда, для которой компания A еженедельно ведет бухгалтерию и проводит ежегодный аудит счетов клуба.</span><span class="sxs-lookup"><span data-stu-id="0eb08-116">One of Company A's clients is the local football team, for which Company A does the weekly bookkeeping and annual audit of the club's accounts.</span></span> <span data-ttu-id="0eb08-117">Счета клуба настраиваются в форме "Объекты обслуживания" и определяются как объект в соглашении о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="0eb08-117">The club's accounts are set up in the Service objects form and specified as the object in the service agreement.</span></span> <span data-ttu-id="0eb08-118">Существует две строки соглашения о сервисном обслуживании для объекта.</span><span class="sxs-lookup"><span data-stu-id="0eb08-118">There are two service agreement lines for the object.</span></span> <span data-ttu-id="0eb08-119">Строка 1 — это еженедельное ведение бухгалтерии с интервалом в одну неделю, назначенным строке, а строка 2 — ежегодный аудит с интервалом один год, назначенным строке.</span><span class="sxs-lookup"><span data-stu-id="0eb08-119">Line 1 is weekly bookkeeping with a weekly interval assigned to the line, and line 2 is the annual audit with a yearly interval assigned to it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0eb08-120">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="0eb08-120">Related topics</span></span>

[<span data-ttu-id="0eb08-121">Создание объектов обслуживания</span><span class="sxs-lookup"><span data-stu-id="0eb08-121">Create service objects</span></span>](create-service-objects.md)


