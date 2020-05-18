---
title: Удаленные или устаревшие функции Dynamics 365 Commerce
description: В этом разделе описываются возможности, который удалены или которые планируется удалить из Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: c47c5430a8f5d67e13c95db609a95d5ad66933ae
ms.sourcegitcommit: a8b6cd799eddaf5be9aec9ea3c2b55e2c3231652
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2020
ms.locfileid: "3335284"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a><span data-ttu-id="304eb-103">Удаленные или устаревшие функции Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="304eb-103">Removed or deprecated features in Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="304eb-104">В этом разделе описываются возможности, который удалены или которые планируется удалить из Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="304eb-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Commerce.</span></span>

- <span data-ttu-id="304eb-105">*Удаленная* функция больше недоступна в продукте.</span><span class="sxs-lookup"><span data-stu-id="304eb-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="304eb-106">*Устаревшая* функция не находится в активной разработке и может быть удалена в следующем обновлении.</span><span class="sxs-lookup"><span data-stu-id="304eb-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="304eb-107">Этот список поможет вам учитывать эти удаления и устаревания при своем собственном планировании.</span><span class="sxs-lookup"><span data-stu-id="304eb-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="304eb-108">Подробные сведения об объектах в приложениях Finance and Operations можно найти в документе [Технический справочник по отчетам](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="304eb-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="304eb-109">Можно сравнить различные версии этих отчетов, чтобы получить сведения об объектах, которые были изменены или были исключены в каждой версии приложений Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="304eb-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a><span data-ttu-id="304eb-110">Функции, удаленные или устаревшие в выпуске Commerce 10.0.10</span><span class="sxs-lookup"><span data-stu-id="304eb-110">Features removed or deprecated in the Commerce 10.0.10 release</span></span>
### <a name="pos-operation-803---picking-and-receiving"></a><span data-ttu-id="304eb-111">Операций POS 803 — Комплектация и получение</span><span class="sxs-lookup"><span data-stu-id="304eb-111">POS operation 803 - Picking and receiving</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="304eb-112">**Причина устаревания/удаления**</span><span class="sxs-lookup"><span data-stu-id="304eb-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="304eb-113">Операции комплектации и получения устарели в связи с новой архитектурой операций.</span><span class="sxs-lookup"><span data-stu-id="304eb-113">Picking and receiving operations is being deprecated due to new operation redesign.</span></span> |
| <span data-ttu-id="304eb-114">**Заменена другой функцией?**</span><span class="sxs-lookup"><span data-stu-id="304eb-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="304eb-115">Да.</span><span class="sxs-lookup"><span data-stu-id="304eb-115">Yes.</span></span> <span data-ttu-id="304eb-116">Она заменяется двумя новыми операциями POS: Входящая операция (804) и исходящая операция (805).</span><span class="sxs-lookup"><span data-stu-id="304eb-116">It is replaced by two new POS operations: inbound operation (804) and outbound operation (805).</span></span>|
| <span data-ttu-id="304eb-117">**Затрагиваемые области продукта**</span><span class="sxs-lookup"><span data-stu-id="304eb-117">**Product areas affected**</span></span>         | <span data-ttu-id="304eb-118">Приложение POS</span><span class="sxs-lookup"><span data-stu-id="304eb-118">Point of sale (POS) application</span></span> |
| <span data-ttu-id="304eb-119">**Вариант развертывания**</span><span class="sxs-lookup"><span data-stu-id="304eb-119">**Deployment option**</span></span>              | <span data-ttu-id="304eb-120">Все</span><span class="sxs-lookup"><span data-stu-id="304eb-120">All</span></span> |
| <span data-ttu-id="304eb-121">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="304eb-121">**Status**</span></span>                         | <span data-ttu-id="304eb-122">Устарело: с выпуска 10.0.10 операции комплектации и получения больше не будут получать новые обновления.</span><span class="sxs-lookup"><span data-stu-id="304eb-122">Deprecated: As of release 10.0.10, the picking and receiving operation will no longer receive any new feature updates.</span></span> <span data-ttu-id="304eb-123">В будущих выпусках для этих операций будут только исправляться критические ошибки.</span><span class="sxs-lookup"><span data-stu-id="304eb-123">Only critical bug fixes will be done for this operation in future releases.</span></span> <span data-ttu-id="304eb-124">Всем клиентам рекомендуется перейти на новые [входящие операции](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) и [исходящие операции](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), которые еще долго будут поддерживаться в продукте.</span><span class="sxs-lookup"><span data-stu-id="304eb-124">All customers are encouraged to move to the new [Inbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) and [Outbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), which will continue to be part of our long-term product roadmap.</span></span> |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a><span data-ttu-id="304eb-125">Функции, удаленные или устаревшие в выпуске Commerce 10.0.7</span><span class="sxs-lookup"><span data-stu-id="304eb-125">Features removed or deprecated in the Commerce 10.0.7 release</span></span>
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a><span data-ttu-id="304eb-126">API Commerce GetProductAvailabilities и GetAvailableInventoryNearby</span><span class="sxs-lookup"><span data-stu-id="304eb-126">Commerce GetProductAvailabilities and GetAvailableInventoryNearby API's</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="304eb-127">**Причина устаревания/удаления**</span><span class="sxs-lookup"><span data-stu-id="304eb-127">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="304eb-128">Новые оптимизированные API созданы для замены API GetProductAvailabilities и GetAvailableInventoryNearby.</span><span class="sxs-lookup"><span data-stu-id="304eb-128">New optimized APIs have been created to replace the GetProductAvailabilities and GetAvailableInventoryNearby APIs.</span></span> |
| <span data-ttu-id="304eb-129">**Заменена другой функцией?**</span><span class="sxs-lookup"><span data-stu-id="304eb-129">**Replaced by another feature?**</span></span>   | <span data-ttu-id="304eb-130">Да: он заменен API GetEstimatedAvailabilty и GetEstimatedProductWarehouseAvailability.</span><span class="sxs-lookup"><span data-stu-id="304eb-130">Yes: It is replaced by GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs.</span></span> |
| <span data-ttu-id="304eb-131">**Затрагиваемые области продукта**</span><span class="sxs-lookup"><span data-stu-id="304eb-131">**Product areas affected**</span></span>         | <span data-ttu-id="304eb-132">SDK приложения электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="304eb-132">e-Commerce application SDK</span></span> |
| <span data-ttu-id="304eb-133">**Вариант развертывания**</span><span class="sxs-lookup"><span data-stu-id="304eb-133">**Deployment option**</span></span>              | <span data-ttu-id="304eb-134">Все</span><span class="sxs-lookup"><span data-stu-id="304eb-134">All</span></span> |
| <span data-ttu-id="304eb-135">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="304eb-135">**Status**</span></span>                         | <span data-ttu-id="304eb-136">Устарел: с выпуска 10.0.7 GetProductAvailabilities и GetAvailableInventoryNearby больше не будут развиваться.</span><span class="sxs-lookup"><span data-stu-id="304eb-136">Deprecated: As of release 10.0.7, there will no longer be engineering investments made for GetProductAvailabilities and GetAvailableInventoryNearby.</span></span> <span data-ttu-id="304eb-137">Организации, использующие эти API в развертываниях электронной коммерции, должны преобразовать их в новые API GetEstimatedAvailabilty и GetEstimatedProductWarehouseAvailability и включить [оптимизированную функцию расчета наличия продукта](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="304eb-137">Organizations that use these APIs in their e-Commerce deployments should convert to the new GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs and enable the [Optimized product availability calculation feature](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span></span>  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="304eb-138">Предыдущие объявления об удаленных или устаревших функциях</span><span class="sxs-lookup"><span data-stu-id="304eb-138">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="304eb-139">Для получения дополнительных сведений о функциях, которые были удалены или устарели в предыдущих выпусках, см [Удаленные или устаревшие функции в предыдущих выпусках](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="304eb-139">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span></span>
