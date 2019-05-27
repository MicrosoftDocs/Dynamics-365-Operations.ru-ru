---
title: Потребности в номенклатуре для заказа на обслуживание
description: Если необходимо зарезервировать определенные номенклатуры для Заказа на сервисное обслуживание, можно создать потребность в складской номенклатуре для него.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3dc7c721af4b25e1586e546392518648110a3fb6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562308"
---
# <a name="service-order-item-requirements"></a><span data-ttu-id="66b24-103">Потребности в номенклатуре для заказа на обслуживание</span><span class="sxs-lookup"><span data-stu-id="66b24-103">Service order item requirements</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="66b24-104">Можно создать заказ на сервисное обслуживание, чтобы отслеживать и управлять услугами, которые предоставляются вашим клиентам.</span><span class="sxs-lookup"><span data-stu-id="66b24-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="66b24-105">Если необходимо зарезервировать определенные номенклатуры для Заказа на сервисное обслуживание, можно создать потребность в складской номенклатуре для него.</span><span class="sxs-lookup"><span data-stu-id="66b24-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="66b24-106">Потребность в номенклатуре можно сразу потребить из запасов или она может запустить производственный заказ для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="66b24-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="66b24-107">Используя потребность в номенклатуре вместо проводки с номенклатурой, можно запланировать поставку перед самым моментом использования данной номенклатуры, создать заказ на покупку, включить номенклатуру в схему коммерческих соглашений, и использовать потребность в номенклатуре при планировании производства.</span><span class="sxs-lookup"><span data-stu-id="66b24-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="66b24-108">Потребности в номенклатуре для заказов на обслуживание обрабатываются с помощью проекта.</span><span class="sxs-lookup"><span data-stu-id="66b24-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="66b24-109">Для создания потребности в номенклатуре в заказе на сервисное обслуживание заказ на обслуживание необходимо присоединить к проекту.</span><span class="sxs-lookup"><span data-stu-id="66b24-109">To create an item requirement on a service order, the service order must be attached to a project.</span></span>

<span data-ttu-id="66b24-110">Как только создается потребность в номенклатуре для заказа на сервисное обслуживание, ее можно просмотреть в разделе **Проект** как отдельный заказ на сервисное обслуживание или через форму **Заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="66b24-110">As soon as an item requirement is created for a service order, it can be viewed from **Project** in the individual service order or through the **Sales order** form.</span></span>

## <a name="view-an-item-requirement-from-a-service-order"></a><span data-ttu-id="66b24-111">Просмотр потребности в номенклатуре из заказа на обслуживание</span><span class="sxs-lookup"><span data-stu-id="66b24-111">View an item requirement from a service order</span></span>

1.  <span data-ttu-id="66b24-112">Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Заказы на сервисное обслуживание** \> **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="66b24-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="66b24-113">Щелкните **Подготовить к отправке** и нажмите **Потребность в номенклатуре**, чтобы открыть форму **Потребности в номенклатуре**.</span><span class="sxs-lookup"><span data-stu-id="66b24-113">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span>

3.  <span data-ttu-id="66b24-114">Щелкните вкладку **Проект** и проверьте поле **Заказ на продажу**, чтобы просмотреть заказы на сервисное обслуживание потребности в номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="66b24-114">Click the **Project** tab, and check the **Service order** field to see the service orders of the item requirement.</span></span>

## <a name="delete-service-orders-with-item-requirements"></a><span data-ttu-id="66b24-115">Удаление заказов на обслуживание с потребностями в номенклатуре</span><span class="sxs-lookup"><span data-stu-id="66b24-115">Delete service orders with item requirements</span></span>

<span data-ttu-id="66b24-116">Если для заказа на обслуживание создана потребность в номенклатуре, удалить заказ на обслуживание невозможно.</span><span class="sxs-lookup"><span data-stu-id="66b24-116">If an item requirement is created on a service order, you cannot delete the service order.</span></span> <span data-ttu-id="66b24-117">Для удаления заказа на обслуживание необходимо предварительно удалить потребность в номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="66b24-117">You must delete the item requirement before you can delete the service order.</span></span>

1.  <span data-ttu-id="66b24-118">Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Заказы на сервисное обслуживание** \> **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="66b24-118">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="66b24-119">Щелкните **Подготовить к отправке** и нажмите **Потребность в номенклатуре**, чтобы открыть форму **Потребности в номенклатуре**.</span><span class="sxs-lookup"><span data-stu-id="66b24-119">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span> <span data-ttu-id="66b24-120">В этой форме перечислены потребности в номенклатуре, созданные по этому заказу на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="66b24-120">This form lists the item requirements that are created on the service order.</span></span>

3.  <span data-ttu-id="66b24-121">Выберите потребность в номенклатуре для удаления, а затем щелкните **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="66b24-121">Select the item requirement to delete, and then click **Delete**.</span></span>

<span data-ttu-id="66b24-122">– или –</span><span class="sxs-lookup"><span data-stu-id="66b24-122">–or–</span></span>

1.  <span data-ttu-id="66b24-123">Щелкните **Управление и учет по проектам** \> **Общее** \> **Проекты** \> **Все проекты**.</span><span class="sxs-lookup"><span data-stu-id="66b24-123">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="66b24-124">Откройте проект с заказом на сервисное обслуживание, в котором создается потребность в номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="66b24-124">Open the project that has the service order in which an item requirement is created.</span></span>

3.  <span data-ttu-id="66b24-125">В форме **Проекты** в правой области щелкните **Потребности в номенклатуре**.</span><span class="sxs-lookup"><span data-stu-id="66b24-125">In the **Projects** form, in the right pane, click **Item requirements**.</span></span> <span data-ttu-id="66b24-126">В форме **Потребности в номенклатуре** будут перечислены все потребности в номенклатуре, связанные с выбранным проектом.</span><span class="sxs-lookup"><span data-stu-id="66b24-126">The **Item requirements** form lists the item requirements that are associated with the selected project.</span></span>

4.  <span data-ttu-id="66b24-127">Выберите потребность в номенклатуре для удаления, а затем щелкните **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="66b24-127">Select the item requirement to delete, and then click **Delete**.</span></span>

## <a name="see-also"></a><span data-ttu-id="66b24-128">См. также</span><span class="sxs-lookup"><span data-stu-id="66b24-128">See also</span></span>

<span data-ttu-id="66b24-129">[Потребности в номенклатуре (форма)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="66b24-129">[Item requirements (form)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\))</span></span>

