---
title: Создание активов на основе заказов на покупку
description: Эта тема объясняет, как можно создать список элементов активов, которые могут быть использованы в качестве основы для создания активов для заданий на обслуживание в управлении активами.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 536795ac8ac164a6cc16e9ba22b0aa7bf30ddfd8
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783559"
---
# <a name="create-assets-based-on-purchase-orders"></a><span data-ttu-id="018ed-103">Создание активов на основе заказов на покупку</span><span class="sxs-lookup"><span data-stu-id="018ed-103">Create assets based on purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="018ed-104">Эта тема объясняет, как можно создать список элементов активов, которые могут быть использованы в качестве основы для создания активов для заданий на обслуживание в управлении активами.</span><span class="sxs-lookup"><span data-stu-id="018ed-104">This topic explains how you can create a list of asset items that can be used as a basis for creating assets for maintenance jobs in Asset Management.</span></span> <span data-ttu-id="018ed-105">На основе номенклатур активов можно просмотреть список строк заказа на покупку, созданного на этих номенклатурах.</span><span class="sxs-lookup"><span data-stu-id="018ed-105">Based on the asset items, you are able to view a list of the purchase order lines that have been created on those items.</span></span> <span data-ttu-id="018ed-106">Цель этой функциональности заключается в том, чтобы легко создать актив в управлении активами на основе заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="018ed-106">The purpose of this functionality is to easily create an asset in Asset Management based on a purchase order.</span></span>

<span data-ttu-id="018ed-107">Сначала вы настраиваете номенклатуры, которые будут использоваться для создания активов из заказа на покупку, в разделе **Номенклатуры активов**.</span><span class="sxs-lookup"><span data-stu-id="018ed-107">First, you set up the items to be used for creating assets from a purchase order in **Asset items**.</span></span> <span data-ttu-id="018ed-108">После создания строки заказа на покупку вы создаете активы в разделе **Активы в ожидании**.</span><span class="sxs-lookup"><span data-stu-id="018ed-108">After creating a purchase order line, you create the assets in **Pending assets**.</span></span> <span data-ttu-id="018ed-109">Можно решить, на какой стадии заказа на покупку актив должен быть создан.</span><span class="sxs-lookup"><span data-stu-id="018ed-109">It is possible to decide at which stage of the purchase order the asset should be created.</span></span>


## <a name="select-asset-items"></a><span data-ttu-id="018ed-110">Выбор номенклатур активов</span><span class="sxs-lookup"><span data-stu-id="018ed-110">Select asset items</span></span>

1. <span data-ttu-id="018ed-111">Щелкните **Управление активами** > **Настройка** > **Активы** > **Номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="018ed-111">Click **Asset management** > **Setup** > **Assets** > **Items**.</span></span>
2. <span data-ttu-id="018ed-112">Щелкните **Создать**, чтобы создать новую номенклатуру актива.</span><span class="sxs-lookup"><span data-stu-id="018ed-112">Click **New** to create a new asset item.</span></span>
3. <span data-ttu-id="018ed-113">Выберите номенклатуру в поле **Код номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="018ed-113">Select the item in the **Item number** field.</span></span> <span data-ttu-id="018ed-114">При выходе из этого поля имя номенклатуры автоматически вставляется в поле **Наименование продукта**.</span><span class="sxs-lookup"><span data-stu-id="018ed-114">When you leave that field, the item name is automatically inserted in the **Product name** field.</span></span>
4. <span data-ttu-id="018ed-115">На экспресс-вкладке **Общее** выберите тип актива для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="018ed-115">On the **General** FastTab, select an asset type for the item.</span></span>
5. <span data-ttu-id="018ed-116">Выберите производителя и модель актива для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="018ed-116">Select asset manufacturer and model for the item.</span></span>
6. <span data-ttu-id="018ed-117">Сохраните номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="018ed-117">Save the item.</span></span>


## <a name="create-assets-from-pending-assets"></a><span data-ttu-id="018ed-118">Создание активов из отложенных активов</span><span class="sxs-lookup"><span data-stu-id="018ed-118">Create assets from pending assets</span></span>

1. <span data-ttu-id="018ed-119">Щелкните **Управление активами** > **Общие** > **Активы** > **Активы в ожидании**.</span><span class="sxs-lookup"><span data-stu-id="018ed-119">Click **Asset management** > **Common** > **Assets** > **Pending Assets**.</span></span>
2. <span data-ttu-id="018ed-120">Вы увидите обновленный список заказов на покупку на основе номенклатур, выбранных в разделе **Номенклатуры активов**.</span><span class="sxs-lookup"><span data-stu-id="018ed-120">You will see an updated list of the purchase orders based on the items selected in **Asset items**.</span></span>
3. <span data-ttu-id="018ed-121">Можно отфильтровать состояние заказов на покупку, чтобы выбрать, в каком состоянии жизненного цикла должен быть создан актив.</span><span class="sxs-lookup"><span data-stu-id="018ed-121">You can filter the status of purchase orders to select at which lifecycle state the asset should be created.</span></span> <span data-ttu-id="018ed-122">Например, вы можете создавать активы только в том случае, если поступление продуктов было разнесено по заказу на покупку.</span><span class="sxs-lookup"><span data-stu-id="018ed-122">For example, you may only want to create assets when a product receipt has been posted on a purchase order.</span></span>
4. <span data-ttu-id="018ed-123">Выберите ссылку **Номер ссылки** в строке заказа на покупку, чтобы просмотреть подробную информацию о товаре.</span><span class="sxs-lookup"><span data-stu-id="018ed-123">Select the **Reference number** link on a purchase order line to view detailed information about the item.</span></span>
5. <span data-ttu-id="018ed-124">Если вы хотите изменить аналитики, которые отображаются на экспресс-вкладке **Складские аналитики**, нажмите кнопку **Показать аналитики** и сделайте свой выбор.</span><span class="sxs-lookup"><span data-stu-id="018ed-124">If you want to edit which dimensions are displayed on the **Inventory dimensions** FastTab, click the **Display Dimensions** button, and make your selections.</span></span>
6. <span data-ttu-id="018ed-125">Если требуется создать актив на основе строки заказа на покупку, установите флажок в столбце **Пометка** для этой строки на странице списка и нажмите **Создать актив**.</span><span class="sxs-lookup"><span data-stu-id="018ed-125">If you want to create an asset based on a purchase order line, select the check box in the **Mark** column for that line on the list page, and click **Create assets**.</span></span> <span data-ttu-id="018ed-126">Отображается сообщение, информирующее вас об идентификаторе актива.</span><span class="sxs-lookup"><span data-stu-id="018ed-126">A message will be displayed informing you of the asset ID.</span></span>
7. <span data-ttu-id="018ed-127">Выберите актив в списке **Все активы** и нажмите кнопку **Изменить**, чтобы добавить дополнительную информацию в актив.</span><span class="sxs-lookup"><span data-stu-id="018ed-127">Select the asset in the **All assets** list and click **Edit** to add more information to the asset.</span></span>
8. <span data-ttu-id="018ed-128">Если в разделе **Активы в ожидании** вы хотите удалить строку, потому что не хотите создавать актив, установите флажок в столбце **Пометка** для этой строки и нажмите **Удалить активы в ожидании**.</span><span class="sxs-lookup"><span data-stu-id="018ed-128">In **Pending assets**, if you want to delete a line because you don't want to create an asset, select the check box in the **Mark** column for that line, and click **Discard pending assets**.</span></span> <span data-ttu-id="018ed-129">Отображается сообщение, информирующее вас об идентификаторе актива.</span><span class="sxs-lookup"><span data-stu-id="018ed-129">A message will be displayed informing you of the asset ID.</span></span> <span data-ttu-id="018ed-130">Вы не удаляете заказ на покупку или заказ на продажу, удаляется только запись, из которой вы могли бы создать актив в модуле **Управление активами**.</span><span class="sxs-lookup"><span data-stu-id="018ed-130">You are not deleting the purchase order or sales order, just the record from which you could have created an asset in **Asset Management**.</span></span>

>[!NOTE]
><span data-ttu-id="018ed-131">Все аналитики продукта (размер, цвет, конфигурация и т. д.) автоматически передаются атрибутам актива.</span><span class="sxs-lookup"><span data-stu-id="018ed-131">All product dimensions (size, color, configuration etc.) are automatically transferred to the asset attributes.</span></span> <span data-ttu-id="018ed-132">Аналитики отслеживания (серийный номер) хранятся непосредственно в активе при создании актива.</span><span class="sxs-lookup"><span data-stu-id="018ed-132">Tracking dimensions (serial number) are stored directly on the asset when the asset is created.</span></span>


## <a name="find-pending-assets"></a><span data-ttu-id="018ed-133">Поиск отложенных активов</span><span class="sxs-lookup"><span data-stu-id="018ed-133">Find pending assets</span></span>

<span data-ttu-id="018ed-134">Можно запустить **Подсчет активов в ожидании** для проверки ожидающих активов.</span><span class="sxs-lookup"><span data-stu-id="018ed-134">You can run a **Pending asset count** to check for pending assets.</span></span> <span data-ttu-id="018ed-135">Например, эта функция может использоваться для получения уведомления каждый раз, когда актив в ожидании готов к созданию в качестве актива.</span><span class="sxs-lookup"><span data-stu-id="018ed-135">For example, this function can be used for receiving a notification each time a pending asset is ready to be created as an asset.</span></span>

1. <span data-ttu-id="018ed-136">Щелкните **Управление активами** > **Периодические операции** > **Активы** > **Подсчет активов в ожидании**.</span><span class="sxs-lookup"><span data-stu-id="018ed-136">Click **Asset management** > **Periodic** > **Assets** > **Pending asset count**.</span></span>
2. <span data-ttu-id="018ed-137">Нажмите **OK**, чтобы запустить задание и обновить список **Активы в ожидании**.</span><span class="sxs-lookup"><span data-stu-id="018ed-137">Click **OK** to run the job and update the list in **Pending assets**.</span></span>
3. <span data-ttu-id="018ed-138">Можно настроить это задание для выполнения в качестве пакетного задания, например, один раз в день.</span><span class="sxs-lookup"><span data-stu-id="018ed-138">You can set up this job to run as a batch job, for example, once each day.</span></span>

<span data-ttu-id="018ed-139">**Внимание.** Если данные изменяются в заказе на покупку *после* создания актива на основе соответствующей номенклатуры, эти изменения не будут отражены в активе.</span><span class="sxs-lookup"><span data-stu-id="018ed-139">**Caution:** If data is changed on a purchase order *after* you have created an asset based on the appertaining item, those changes will not be reflected on the asset.</span></span>
