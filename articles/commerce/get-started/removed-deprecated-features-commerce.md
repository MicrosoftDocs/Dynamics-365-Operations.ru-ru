---
title: Удаленные или устаревшие функции Dynamics 365 Commerce
description: В этом разделе описываются возможности, который удалены или которые планируется удалить из Dynamics 365 Commerce.
author: josaw
manager: AnnBe
ms.date: 06/10/2020
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
ms.openlocfilehash: 64241ef1c25359c7b3b305c4e8f2b24de7e8f5e4
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443926"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a><span data-ttu-id="c93e0-103">Удаленные или устаревшие функции Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c93e0-103">Removed or deprecated features in Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c93e0-104">В этом разделе описываются возможности, который удалены или которые планируется удалить из Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c93e0-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Commerce.</span></span>

- <span data-ttu-id="c93e0-105">*Удаленная* функция больше недоступна в продукте.</span><span class="sxs-lookup"><span data-stu-id="c93e0-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="c93e0-106">*Устаревшая* функция не находится в активной разработке и может быть удалена в следующем обновлении.</span><span class="sxs-lookup"><span data-stu-id="c93e0-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="c93e0-107">Этот список поможет вам учитывать эти удаления и устаревания при своем собственном планировании.</span><span class="sxs-lookup"><span data-stu-id="c93e0-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="c93e0-108">Подробные сведения об объектах в приложениях Finance and Operations можно найти в документе [Технический справочник по отчетам](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="c93e0-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="c93e0-109">Можно сравнить различные версии этих отчетов, чтобы получить сведения об объектах, которые были изменены или были исключены в каждой версии приложений Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c93e0-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a><span data-ttu-id="c93e0-110">Функции, удаленные или устаревшие в выпуске Commerce 10.0.11</span><span class="sxs-lookup"><span data-stu-id="c93e0-110">Features removed or deprecated in the Commerce 10.0.11 release</span></span>
### <a name="data-action-hooks"></a><span data-ttu-id="c93e0-111">Обработчики действий с данными</span><span class="sxs-lookup"><span data-stu-id="c93e0-111">Data action hooks</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="c93e0-112">**Причина устаревания/удаления**</span><span class="sxs-lookup"><span data-stu-id="c93e0-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="c93e0-113">Функция перехватчиков действий с данными устарела из-за проблем с производительностью.</span><span class="sxs-lookup"><span data-stu-id="c93e0-113">The data action hooks feature has been deprecated due to performance issues.</span></span> |
| <span data-ttu-id="c93e0-114">**Заменена другой функцией?**</span><span class="sxs-lookup"><span data-stu-id="c93e0-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="c93e0-115">Рекомендуется вместо этого использовать [переопределения действий данных](../e-commerce-extensibility/data-action-overrides.md) для изменения бизнес-логики на уровне действий с данными.</span><span class="sxs-lookup"><span data-stu-id="c93e0-115">It is recommended to instead use [data action overrides](../e-commerce-extensibility/data-action-overrides.md) to modify business logic in the data action layer.</span></span>|
| <span data-ttu-id="c93e0-116">**Затрагиваемые области продукта**</span><span class="sxs-lookup"><span data-stu-id="c93e0-116">**Product areas affected**</span></span>         | <span data-ttu-id="c93e0-117">Действия данных расширяемости электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="c93e0-117">E-Commerce extensibility data actions</span></span> |
| <span data-ttu-id="c93e0-118">**Вариант развертывания**</span><span class="sxs-lookup"><span data-stu-id="c93e0-118">**Deployment option**</span></span>              | <span data-ttu-id="c93e0-119">Все</span><span class="sxs-lookup"><span data-stu-id="c93e0-119">All</span></span> |
| <span data-ttu-id="c93e0-120">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="c93e0-120">**Status**</span></span>                         | <span data-ttu-id="c93e0-121">Устарело: на момент выпуска 10.0.11</span><span class="sxs-lookup"><span data-stu-id="c93e0-121">Deprecated: As of release 10.0.11</span></span> |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a><span data-ttu-id="c93e0-122">Функции, удаленные или устаревшие в выпуске Commerce 10.0.10</span><span class="sxs-lookup"><span data-stu-id="c93e0-122">Features removed or deprecated in the Commerce 10.0.10 release</span></span>
### <a name="pos-operation-803---picking-and-receiving"></a><span data-ttu-id="c93e0-123">Операций POS 803 — Комплектация и получение</span><span class="sxs-lookup"><span data-stu-id="c93e0-123">POS operation 803 - Picking and receiving</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="c93e0-124">**Причина устаревания/удаления**</span><span class="sxs-lookup"><span data-stu-id="c93e0-124">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="c93e0-125">Операции комплектации и получения устарели в связи с новой архитектурой операций.</span><span class="sxs-lookup"><span data-stu-id="c93e0-125">Picking and receiving operations is being deprecated due to new operation redesign.</span></span> |
| <span data-ttu-id="c93e0-126">**Заменена другой функцией?**</span><span class="sxs-lookup"><span data-stu-id="c93e0-126">**Replaced by another feature?**</span></span>   | <span data-ttu-id="c93e0-127">Да.</span><span class="sxs-lookup"><span data-stu-id="c93e0-127">Yes.</span></span> <span data-ttu-id="c93e0-128">Она заменяется двумя новыми операциями POS: Входящая операция (804) и исходящая операция (805).</span><span class="sxs-lookup"><span data-stu-id="c93e0-128">It is replaced by two new POS operations: inbound operation (804) and outbound operation (805).</span></span>|
| <span data-ttu-id="c93e0-129">**Затрагиваемые области продукта**</span><span class="sxs-lookup"><span data-stu-id="c93e0-129">**Product areas affected**</span></span>         | <span data-ttu-id="c93e0-130">Приложение POS</span><span class="sxs-lookup"><span data-stu-id="c93e0-130">Point of sale (POS) application</span></span> |
| <span data-ttu-id="c93e0-131">**Вариант развертывания**</span><span class="sxs-lookup"><span data-stu-id="c93e0-131">**Deployment option**</span></span>              | <span data-ttu-id="c93e0-132">Все</span><span class="sxs-lookup"><span data-stu-id="c93e0-132">All</span></span> |
| <span data-ttu-id="c93e0-133">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="c93e0-133">**Status**</span></span>                         | <span data-ttu-id="c93e0-134">Устарело: с выпуска 10.0.10 операции комплектации и получения больше не будут получать новые обновления.</span><span class="sxs-lookup"><span data-stu-id="c93e0-134">Deprecated: As of release 10.0.10, the picking and receiving operation will no longer receive any new feature updates.</span></span> <span data-ttu-id="c93e0-135">В будущих выпусках для этих операций будут только исправляться критические ошибки.</span><span class="sxs-lookup"><span data-stu-id="c93e0-135">Only critical bug fixes will be done for this operation in future releases.</span></span> <span data-ttu-id="c93e0-136">Всем клиентам рекомендуется перейти на новые [входящие операции](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) и [исходящие операции](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), которые еще долго будут поддерживаться в продукте.</span><span class="sxs-lookup"><span data-stu-id="c93e0-136">All customers are encouraged to move to the new [Inbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) and [Outbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), which will continue to be part of our long-term product roadmap.</span></span> |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a><span data-ttu-id="c93e0-137">Функции, удаленные или устаревшие в выпуске Commerce 10.0.7</span><span class="sxs-lookup"><span data-stu-id="c93e0-137">Features removed or deprecated in the Commerce 10.0.7 release</span></span>
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a><span data-ttu-id="c93e0-138">API Commerce GetProductAvailabilities и GetAvailableInventoryNearby</span><span class="sxs-lookup"><span data-stu-id="c93e0-138">Commerce GetProductAvailabilities and GetAvailableInventoryNearby API's</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="c93e0-139">**Причина устаревания/удаления**</span><span class="sxs-lookup"><span data-stu-id="c93e0-139">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="c93e0-140">Новые оптимизированные API созданы для замены API GetProductAvailabilities и GetAvailableInventoryNearby.</span><span class="sxs-lookup"><span data-stu-id="c93e0-140">New optimized APIs have been created to replace the GetProductAvailabilities and GetAvailableInventoryNearby APIs.</span></span> |
| <span data-ttu-id="c93e0-141">**Заменена другой функцией?**</span><span class="sxs-lookup"><span data-stu-id="c93e0-141">**Replaced by another feature?**</span></span>   | <span data-ttu-id="c93e0-142">Да: он заменен API GetEstimatedAvailabilty и GetEstimatedProductWarehouseAvailability.</span><span class="sxs-lookup"><span data-stu-id="c93e0-142">Yes: It is replaced by GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs.</span></span> |
| <span data-ttu-id="c93e0-143">**Затрагиваемые области продукта**</span><span class="sxs-lookup"><span data-stu-id="c93e0-143">**Product areas affected**</span></span>         | <span data-ttu-id="c93e0-144">SDK приложения электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="c93e0-144">e-Commerce application SDK</span></span> |
| <span data-ttu-id="c93e0-145">**Вариант развертывания**</span><span class="sxs-lookup"><span data-stu-id="c93e0-145">**Deployment option**</span></span>              | <span data-ttu-id="c93e0-146">Все</span><span class="sxs-lookup"><span data-stu-id="c93e0-146">All</span></span> |
| <span data-ttu-id="c93e0-147">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="c93e0-147">**Status**</span></span>                         | <span data-ttu-id="c93e0-148">Устарел: с выпуска 10.0.7 GetProductAvailabilities и GetAvailableInventoryNearby больше не будут развиваться.</span><span class="sxs-lookup"><span data-stu-id="c93e0-148">Deprecated: As of release 10.0.7, there will no longer be engineering investments made for GetProductAvailabilities and GetAvailableInventoryNearby.</span></span> <span data-ttu-id="c93e0-149">Организации, использующие эти API в развертываниях электронной коммерции, должны преобразовать их в новые API GetEstimatedAvailabilty и GetEstimatedProductWarehouseAvailability и включить [оптимизированную функцию расчета наличия продукта](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="c93e0-149">Organizations that use these APIs in their e-Commerce deployments should convert to the new GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs and enable the [Optimized product availability calculation feature](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span></span>  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="c93e0-150">Предыдущие объявления об удаленных или устаревших функциях</span><span class="sxs-lookup"><span data-stu-id="c93e0-150">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="c93e0-151">Для получения дополнительных сведений о функциях, которые были удалены или устарели в предыдущих выпусках, см [Удаленные или устаревшие функции в предыдущих выпусках](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="c93e0-151">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span></span>
