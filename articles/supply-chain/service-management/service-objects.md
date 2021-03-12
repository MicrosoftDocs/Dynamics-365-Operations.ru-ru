---
title: Обзор объектов сервисного обслуживания
description: Объекты сервисного обслуживания — это основные средства и продукты клиента, сервисное обслуживание которых вы можете выполнить.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1e0a40d351150ce432164438cd9680cf80792e1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974318"
---
# <a name="service-objects-overview"></a><span data-ttu-id="c695f-103">Обзор объектов сервисного обслуживания</span><span class="sxs-lookup"><span data-stu-id="c695f-103">Service objects overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c695f-104">Объекты сервисного обслуживания — это основные средства и продукты клиента, сервисное обслуживание которых вы можете выполнить.</span><span class="sxs-lookup"><span data-stu-id="c695f-104">Service objects are a customer’s assets and products for which you can perform a service.</span></span> <span data-ttu-id="c695f-105">В зависимости от типа предоставляемых услуг объекты могут быть материальными и нематериальными:</span><span class="sxs-lookup"><span data-stu-id="c695f-105">Depending on the type of service you provide, objects can be tangible or intangible:</span></span>

-  <span data-ttu-id="c695f-106">Материальные объекты - это предметы, например, станок или здание, в отношении которого вы выполняете задачу физического обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c695f-106">Tangible objects are things, such as a machine or a building, on which you can perform a physical service task.</span></span>

    <span data-ttu-id="c695f-107">Материальным объектом сервисного обслуживания может быть складируемая номенклатура, которая создается в форме "Сведения об используемом продукте".</span><span class="sxs-lookup"><span data-stu-id="c695f-107">A tangible service object can also be an inventory item that you create in the Released product details form.</span></span> <span data-ttu-id="c695f-108">В зависимости от группы складских аналитик, присоединенной к номенклатуре, можно создать объект сервисного обслуживания с уровнем детализации, который включает серийный номер номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="c695f-108">Depending on the inventory dimension group that you attach to the item, you can create a service object to a level of detail that includes the item serial number.</span></span> <span data-ttu-id="c695f-109">Это полезно, когда требуется отслеживать точную номенклатуру, которую представляет объект сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c695f-109">This is useful when you must keep track of the exact item that the service object represents.</span></span>

    <span data-ttu-id="c695f-110">Материальным объектом сервисного обслуживания также может быть номенклатура, которая не связана напрямую с продукцией компании или ее цепочкой поставок.</span><span class="sxs-lookup"><span data-stu-id="c695f-110">A tangible service object can also be an item that is not directly related to a company's direct production or supply chain.</span></span> <span data-ttu-id="c695f-111">Например, набор инструментов, используемый для проведения ремонта по заказу на сервисное обслуживание, не включенный в запасы.</span><span class="sxs-lookup"><span data-stu-id="c695f-111">For example, a tool kit that is used for repairs in a service order can be a service object that is not included in inventory.</span></span> <span data-ttu-id="c695f-112">В этом случае он не регистрируется как складируемая номенклатура.</span><span class="sxs-lookup"><span data-stu-id="c695f-112">In this case, you don’t register it as an inventory item.</span></span>

-  <span data-ttu-id="c695f-113">К нематериальным объектам относятся нефизические сущности, такие как набор счетов или юридический документ, в отношении которых выполняется задача сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c695f-113">Intangible objects are nonphysical things, such as a set of accounts or a legal document, on which you can perform a service task.</span></span>

## <a name="example-of-an-intangible-service-object"></a><span data-ttu-id="c695f-114">Пример нематериального объекта сервисного обслуживания</span><span class="sxs-lookup"><span data-stu-id="c695f-114">Example of an intangible service object</span></span>

<span data-ttu-id="c695f-115">Компания A создает финансовые записи для нескольких небольших компаний.</span><span class="sxs-lookup"><span data-stu-id="c695f-115">Company A maintains the financial records for several small companies.</span></span> <span data-ttu-id="c695f-116">Одним из клиентов компании A является местная футбольная команда, для которой компания A еженедельно ведет бухгалтерию и проводит ежегодный аудит счетов клуба.</span><span class="sxs-lookup"><span data-stu-id="c695f-116">One of Company A's clients is the local football team, for which Company A does the weekly bookkeeping and annual audit of the club's accounts.</span></span> <span data-ttu-id="c695f-117">Счета клуба настраиваются в форме "Объекты обслуживания" и определяются как объект в соглашении о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="c695f-117">The club's accounts are set up in the Service objects form and specified as the object in the service agreement.</span></span> <span data-ttu-id="c695f-118">Существует две строки соглашения о сервисном обслуживании для объекта.</span><span class="sxs-lookup"><span data-stu-id="c695f-118">There are two service agreement lines for the object.</span></span> <span data-ttu-id="c695f-119">Строка 1 — это еженедельное ведение бухгалтерии с интервалом в одну неделю, назначенным строке, а строка 2 — ежегодный аудит с интервалом один год, назначенным строке.</span><span class="sxs-lookup"><span data-stu-id="c695f-119">Line 1 is weekly bookkeeping with a weekly interval assigned to the line, and line 2 is the annual audit with a yearly interval assigned to it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c695f-120">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="c695f-120">Related topics</span></span>

[<span data-ttu-id="c695f-121">Создание объектов обслуживания</span><span class="sxs-lookup"><span data-stu-id="c695f-121">Create service objects</span></span>](create-service-objects.md)

