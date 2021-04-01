---
title: Создание потребностей в номенклатуре для заказов на обслуживание
description: Если необходимо зарезервировать определенные номенклатуры для Заказа на сервисное обслуживание, можно создать потребность в складской номенклатуре для него.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b342b20cc11addc53fc6ea4e1a23d3b449eb9ee
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257953"
---
# <a name="create-item-requirements-for-service-orders"></a><span data-ttu-id="3ebb1-103">Создание потребностей в номенклатуре для заказов на обслуживание</span><span class="sxs-lookup"><span data-stu-id="3ebb1-103">Create item requirements for service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3ebb1-104">Можно создать заказ на сервисное обслуживание, чтобы отслеживать и управлять услугами, которые предоставляются вашим клиентам.</span><span class="sxs-lookup"><span data-stu-id="3ebb1-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="3ebb1-105">Если необходимо зарезервировать определенные номенклатуры для Заказа на сервисное обслуживание, можно создать потребность в складской номенклатуре для него.</span><span class="sxs-lookup"><span data-stu-id="3ebb1-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="3ebb1-106">Потребность в номенклатуре можно сразу потребить из запасов или она может запустить производственный заказ для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3ebb1-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="3ebb1-107">Используя потребность в номенклатуре вместо проводки с номенклатурой, можно запланировать поставку перед самым моментом использования данной номенклатуры, создать заказ на покупку, включить номенклатуру в схему коммерческих соглашений, и использовать потребность в номенклатуре при планировании производства.</span><span class="sxs-lookup"><span data-stu-id="3ebb1-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="3ebb1-108">Потребности в номенклатуре для заказов на обслуживание обрабатываются с помощью проекта.</span><span class="sxs-lookup"><span data-stu-id="3ebb1-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="3ebb1-109">Для создания потребности в номенклатуре в заказе на сервисное обслуживание заказ на обслуживание необходимо назначить проекту.</span><span class="sxs-lookup"><span data-stu-id="3ebb1-109">To create an item requirement on a service order, the service order must be assigned to a project.</span></span> <span data-ttu-id="3ebb1-110">После создания потребности в номенклатуре для заказа на сервисное обслуживание можно просмотреть потребность в номенклатуре в форме **Проекты** для выбранного проекта.</span><span class="sxs-lookup"><span data-stu-id="3ebb1-110">After you create an item requirement for a service order, you can view the item requirement in the **Projects** form for the selected project.</span></span>

## <a name="create-an-item-requirement-for-a-service-order"></a><span data-ttu-id="3ebb1-111">Создание потребности в номенклатуре для заказа на сервисное обслуживание</span><span class="sxs-lookup"><span data-stu-id="3ebb1-111">Create an item requirement for a service order</span></span>

1.  <span data-ttu-id="3ebb1-112">Щелкните **Управление сервисным обслуживанием** \> **Общий** \> **Заказы на сервисное обслуживание** \> **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="3ebb1-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="3ebb1-113">Выберите заказ на сервисное обслуживание, для которого необходимо создать потребность в номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="3ebb1-113">Select the service order that you want to create an item requirement for.</span></span>

3.  <span data-ttu-id="3ebb1-114">В разделе **Панель операций** на вкладке **Отправка** выберите **Потребность в номенклатуре**.</span><span class="sxs-lookup"><span data-stu-id="3ebb1-114">On the **Action Pane**, on the **Dispatch** tab, click **Item requirement**.</span></span>

4.  <span data-ttu-id="3ebb1-115">В форме **Потребности в номенклатуре** введите сведения для требуемой номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3ebb1-115">In the **Item requirements** form, enter information for the required item.</span></span> <span data-ttu-id="3ebb1-116">Дополнительные сведения об отдельных полях см. в разделе [Потребности в номенклатуре (форма)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="3ebb1-116">For more information about the specific fields, see [Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).</span></span>

## <a name="create-an-item-requirement-for-a-service-agreement"></a><span data-ttu-id="3ebb1-117">Создание потребности в номенклатуре для соглашения о сервисном обслуживании</span><span class="sxs-lookup"><span data-stu-id="3ebb1-117">Create an item requirement for a service agreement</span></span>

1.  <span data-ttu-id="3ebb1-118">Щелкните **Управление сервисным обслуживанием** \> **Общее** \> **Соглашения на обслуживание** \> **Соглашения на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="3ebb1-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="3ebb1-119">Откройте соглашение о сервисном обслуживании, для которого необходимо создать потребность в номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="3ebb1-119">Open the service agreement for which you want to create an item requirement.</span></span>

3.  <span data-ttu-id="3ebb1-120">На экспресс-вкладке **Строки** щелкните **Добавить**, чтобы создать новую строку.</span><span class="sxs-lookup"><span data-stu-id="3ebb1-120">On the **Lines** FastTab, click **Add** to create a new line.</span></span>

4.  <span data-ttu-id="3ebb1-121">В поле **Тип проводки** выберите **Номенклатура**.</span><span class="sxs-lookup"><span data-stu-id="3ebb1-121">In the **Transaction type** field, select **Item**.</span></span>

5.  <span data-ttu-id="3ebb1-122">В поле **Настройка номенклатуры** выберите **Потребность в номенклатуре**.</span><span class="sxs-lookup"><span data-stu-id="3ebb1-122">In the **Item setup** field, select **Item requirement**.</span></span>

6.  <span data-ttu-id="3ebb1-123">В поле **Код номенклатуры** выберите номенклатуру, которая требуется для соглашения о сервисном обслуживании обслуживание.</span><span class="sxs-lookup"><span data-stu-id="3ebb1-123">In the **Item number** field, select the item that is required for the service agreement.</span></span>

7.  <span data-ttu-id="3ebb1-124">На экспресс-вкладке **Сведения о строке** на вкладке **Аналитики продуктов** в поле **Сайт** выберите сайт запасов для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="3ebb1-124">On the **Line details** FastTab, on the **Product dimensions** tab, in the **Site** field, select the inventory site for the item.</span></span>

8.  <span data-ttu-id="3ebb1-125">Чтобы создать заказ на сервисное обслуживание из данной строки соглашения, на экспресс-вкладке **Строки** щелкните **Создать заказы на сервисное обслуживание** и введите необходимую информацию в форму **Создать заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="3ebb1-125">To create a service order from the agreement line, on the **Lines** FastTab, click **Create service orders**, and then enter the relevant information in the **Create service orders** form.</span></span> 


## <a name="see-also"></a><span data-ttu-id="3ebb1-126">См. также</span><span class="sxs-lookup"><span data-stu-id="3ebb1-126">See also</span></span>

<span data-ttu-id="3ebb1-127">[Автоматическое создание заказов на обслуживание](create-service-orders-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="3ebb1-127">[Create service orders automatically](create-service-orders-automatically.md).</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]