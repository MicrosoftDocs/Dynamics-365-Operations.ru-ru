---
title: Потребности в номенклатуре для заказа на обслуживание
description: Если необходимо зарезервировать определенные номенклатуры для Заказа на сервисное обслуживание, можно создать потребность в складской номенклатуре для него.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e31f58cf8782c715b97bdae0e89f684b15a76d2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215087"
---
# <a name="service-order-item-requirements"></a><span data-ttu-id="a0810-103">Потребности в номенклатуре для заказа на обслуживание</span><span class="sxs-lookup"><span data-stu-id="a0810-103">Service order item requirements</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a0810-104">Можно создать заказ на сервисное обслуживание, чтобы отслеживать и управлять услугами, которые предоставляются вашим клиентам.</span><span class="sxs-lookup"><span data-stu-id="a0810-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="a0810-105">Если необходимо зарезервировать определенные номенклатуры для Заказа на сервисное обслуживание, можно создать потребность в складской номенклатуре для него.</span><span class="sxs-lookup"><span data-stu-id="a0810-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="a0810-106">Потребность в номенклатуре можно сразу потребить из запасов или она может запустить производственный заказ для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="a0810-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="a0810-107">Используя потребность в номенклатуре вместо проводки с номенклатурой, можно запланировать поставку перед самым моментом использования данной номенклатуры, создать заказ на покупку, включить номенклатуру в схему коммерческих соглашений, и использовать потребность в номенклатуре при планировании производства.</span><span class="sxs-lookup"><span data-stu-id="a0810-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="a0810-108">Потребности в номенклатуре для заказов на обслуживание обрабатываются с помощью проекта.</span><span class="sxs-lookup"><span data-stu-id="a0810-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="a0810-109">Для создания потребности в номенклатуре в заказе на сервисное обслуживание заказ на обслуживание необходимо присоединить к проекту.</span><span class="sxs-lookup"><span data-stu-id="a0810-109">To create an item requirement on a service order, the service order must be attached to a project.</span></span>

<span data-ttu-id="a0810-110">Как только создается потребность в номенклатуре для заказа на сервисное обслуживание, ее можно просмотреть в разделе **Проект** как отдельный заказ на сервисное обслуживание или через форму **Заказ на продажу**.</span><span class="sxs-lookup"><span data-stu-id="a0810-110">As soon as an item requirement is created for a service order, it can be viewed from **Project** in the individual service order or through the **Sales order** form.</span></span>

## <a name="view-an-item-requirement-from-a-service-order"></a><span data-ttu-id="a0810-111">Просмотр потребности в номенклатуре из заказа на обслуживание</span><span class="sxs-lookup"><span data-stu-id="a0810-111">View an item requirement from a service order</span></span>

1.  <span data-ttu-id="a0810-112">Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Заказы на сервисное обслуживание** \> **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="a0810-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="a0810-113">Щелкните **Подготовить к отправке** и нажмите **Потребность в номенклатуре**, чтобы открыть форму **Потребности в номенклатуре**.</span><span class="sxs-lookup"><span data-stu-id="a0810-113">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span>

3.  <span data-ttu-id="a0810-114">Щелкните вкладку **Проект** и проверьте поле **Заказ на продажу**, чтобы просмотреть заказы на сервисное обслуживание потребности в номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="a0810-114">Click the **Project** tab, and check the **Service order** field to see the service orders of the item requirement.</span></span>

## <a name="delete-service-orders-with-item-requirements"></a><span data-ttu-id="a0810-115">Удаление заказов на обслуживание с потребностями в номенклатуре</span><span class="sxs-lookup"><span data-stu-id="a0810-115">Delete service orders with item requirements</span></span>

<span data-ttu-id="a0810-116">Если для заказа на обслуживание создана потребность в номенклатуре, удалить заказ на обслуживание невозможно.</span><span class="sxs-lookup"><span data-stu-id="a0810-116">If an item requirement is created on a service order, you cannot delete the service order.</span></span> <span data-ttu-id="a0810-117">Для удаления заказа на обслуживание необходимо предварительно удалить потребность в номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="a0810-117">You must delete the item requirement before you can delete the service order.</span></span>

1.  <span data-ttu-id="a0810-118">Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Заказы на сервисное обслуживание** \> **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="a0810-118">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="a0810-119">Щелкните **Подготовить к отправке** и нажмите **Потребность в номенклатуре**, чтобы открыть форму **Потребности в номенклатуре**.</span><span class="sxs-lookup"><span data-stu-id="a0810-119">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span> <span data-ttu-id="a0810-120">В этой форме перечислены потребности в номенклатуре, созданные по этому заказу на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="a0810-120">This form lists the item requirements that are created on the service order.</span></span>

3.  <span data-ttu-id="a0810-121">Выберите потребность в номенклатуре для удаления, а затем щелкните **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="a0810-121">Select the item requirement to delete, and then click **Delete**.</span></span>

<span data-ttu-id="a0810-122">– или –</span><span class="sxs-lookup"><span data-stu-id="a0810-122">–or–</span></span>

1.  <span data-ttu-id="a0810-123">Щелкните **Управление и учет по проектам** \> **Общее** \> **Проекты** \> **Все проекты**.</span><span class="sxs-lookup"><span data-stu-id="a0810-123">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="a0810-124">Откройте проект с заказом на сервисное обслуживание, в котором создается потребность в номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="a0810-124">Open the project that has the service order in which an item requirement is created.</span></span>

3.  <span data-ttu-id="a0810-125">В форме **Проекты** в правой области щелкните **Потребности в номенклатуре**.</span><span class="sxs-lookup"><span data-stu-id="a0810-125">In the **Projects** form, in the right pane, click **Item requirements**.</span></span> <span data-ttu-id="a0810-126">В форме **Потребности в номенклатуре** будут перечислены все потребности в номенклатуре, связанные с выбранным проектом.</span><span class="sxs-lookup"><span data-stu-id="a0810-126">The **Item requirements** form lists the item requirements that are associated with the selected project.</span></span>

4.  <span data-ttu-id="a0810-127">Выберите потребность в номенклатуре для удаления, а затем щелкните **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="a0810-127">Select the item requirement to delete, and then click **Delete**.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0810-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a0810-128">See also</span></span>

<span data-ttu-id="a0810-129">[Потребности в номенклатуре (форма)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="a0810-129">[Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span></span>

