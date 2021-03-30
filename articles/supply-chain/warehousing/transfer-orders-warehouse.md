---
title: Настройка складов для заказов на перемещение
description: В этом разделе описывается, как настроить склады для заказов на перемещение.
author: Mirzaab
manager: tfehr
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation,CustVendTransportPoint2Point
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e01629982bb383078e90ff3dad0592371f44bd1b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206855"
---
# <a name="set-up-warehouses-for-transfer-orders"></a><span data-ttu-id="6f799-103">Настройка складов для заказов на перемещение</span><span class="sxs-lookup"><span data-stu-id="6f799-103">Set up warehouses for transfer orders</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f799-104">Можно использовать уровни склада для создания иерархической структуры, поддерживающей перемещения между складами.</span><span class="sxs-lookup"><span data-stu-id="6f799-104">You can use warehouse levels to create a hierarchy that supports transfer orders between warehouses.</span></span> <span data-ttu-id="6f799-105">На основе этой настройки при сводном планировании рассчитывается требования номенклатуры на отдельном уровне склада и создаются спланированные заказы на перемещение из назначенного исходного склада для их выполнения.</span><span class="sxs-lookup"><span data-stu-id="6f799-105">Based on this setup, master scheduling calculates item requirements at the individual warehouse level and generates planned transfer orders from an assigned source warehouse to fulfill them.</span></span>

1.  <span data-ttu-id="6f799-106">Щелкните **Управление запасами > Настройка > Разделение запасов > Склады**.</span><span class="sxs-lookup"><span data-stu-id="6f799-106">Click **Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>

2.  <span data-ttu-id="6f799-107">Выберите склад, который необходимо пополнить.</span><span class="sxs-lookup"><span data-stu-id="6f799-107">Select the warehouse that you want to refill.</span></span>

3.  <span data-ttu-id="6f799-108">На экспресс-вкладке **Сводное планирование** установите флажок **Пополнение**.</span><span class="sxs-lookup"><span data-stu-id="6f799-108">On the **Master planning** FastTab, select the **Refilling** check box.</span></span>

4.  <span data-ttu-id="6f799-109">В поле **Главный склад** выберите склад, который необходимо назначить в качестве склада пополнения.</span><span class="sxs-lookup"><span data-stu-id="6f799-109">In the **Main warehouse** field, select the warehouse that you want to assign as the refilling warehouse.</span></span> <span data-ttu-id="6f799-110">Сводное планирование позволяет рассчитать требования перемещения для выбранного склада и создать спланированный заказ на перемещение из назначенного склада **Главный склад**.</span><span class="sxs-lookup"><span data-stu-id="6f799-110">Master scheduling calculates a transfer requirement for the selected warehouse and generates a planned transfer order from the assigned **Main warehouse**.</span></span>
   
    > [!NOTE]
    > <P><span data-ttu-id="6f799-111">Если снять флажок <STRONG>Пополнение</STRONG>, выбранному складу назначается уровень склада, связанный с <STRONG>Главным складом</STRONG>, но <STRONG>Главный склад</STRONG> не настраивается в качестве склада пополнения.</span><span class="sxs-lookup"><span data-stu-id="6f799-111">If you clear the <STRONG>Refilling</STRONG> check box, the selected warehouse is assigned a warehouse level in regard to the <STRONG>Main warehouse</STRONG>, but the <STRONG>Main warehouse</STRONG> is not set up as a refilling warehouse.</span></span></P>

5.  <span data-ttu-id="6f799-112">Чтобы применить новые настройки, закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6f799-112">Close the page to apply the new setup.</span></span>


> [!TIP]
> <P><span data-ttu-id="6f799-113">Если требуется назначить склад для пополнения, сначала нужно настроить склад как складскую аналитику на странице <STRONG>Группы аналитик хранения</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="6f799-113">If you want to assign a warehouse for refilling, you must first set up the warehouse as a storage dimension on the <STRONG>Storage dimension groups</STRONG> page.</span></span> <span data-ttu-id="6f799-114">На этой странице выберите поле <STRONG>Активен</STRONG> и поле <STRONG>План покрытия по аналитикам</STRONG> для склада.</span><span class="sxs-lookup"><span data-stu-id="6f799-114">On this page, select the <STRONG>Active</STRONG> field and the <STRONG>Coverage plan by dimension</STRONG> field for the warehouse.</span></span></P>

## <a name="set-up-transport-lead-time"></a><span data-ttu-id="6f799-115">Настройка времени упреждения для транспортировки</span><span class="sxs-lookup"><span data-stu-id="6f799-115">Set up transport lead time</span></span>

<span data-ttu-id="6f799-116">Также необходимо настроить время упреждения для транспортировки между складами на странице **Время транспортировки в днях**.</span><span class="sxs-lookup"><span data-stu-id="6f799-116">You must also set up the transport lead time between the warehouses on the **Transport days** page.</span></span> 
1. <span data-ttu-id="6f799-117">Выберите **Управление запасами > Настройка > Распределение > Время транспортировки в днях**.</span><span class="sxs-lookup"><span data-stu-id="6f799-117">Go to **Inventory management > Setup > Distribution > Transport days**.</span></span>
2. <span data-ttu-id="6f799-118">В поле **Пункт приемки** выберите **склад**.</span><span class="sxs-lookup"><span data-stu-id="6f799-118">In the **Receiving point** field, select **warehouse**.</span></span>
3. <span data-ttu-id="6f799-119">Выберите **Склад отгрузки**, **Склад приемки** и **Время транспортировки в днях**.</span><span class="sxs-lookup"><span data-stu-id="6f799-119">Select the **Shipping warehouse**, **Receiving warehouse**, and **Transport days**.</span></span> 
4. <span data-ttu-id="6f799-120">(Необязательно) Можно также задать время транспортировки, в зависимости от способа поставки, на вкладке **Время транспортировки в днях по способу поставки**.</span><span class="sxs-lookup"><span data-stu-id="6f799-120">(Optional) You can also set transport time, depending on the mode of delivery, under the **Transport days per mode of delivery** tab.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]