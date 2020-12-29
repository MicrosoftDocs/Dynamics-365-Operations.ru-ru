---
title: Владельцы продукта
description: В этой теме содержится информация о владельцах продукта. Владелец продукта — это группа пользователей, ответственных за конкретные продукты. Только участники этой группы могут выпускать эти продукты. Владелец продукта также может использоваться в рабочем процессе утверждения.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4308020d66995d857e547be47216cb82caacf035
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/29/2020
ms.locfileid: "4436487"
---
# <a name="product-owners"></a><span data-ttu-id="bf0b6-106">Владельцы продукта</span><span class="sxs-lookup"><span data-stu-id="bf0b6-106">Product owners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf0b6-107">Владелец продукта — это группа пользователей, ответственных за конкретные продукты.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-107">The product owner is a group of users who are responsible for specific products.</span></span> <span data-ttu-id="bf0b6-108">Если группа владельцев продукта назначена продукту, только участники этой группы могут выпустить продукт.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-108">When a product owner group is assigned to a product, only the members of that group can release the product.</span></span> <span data-ttu-id="bf0b6-109">Владелец продукта также может использоваться в рабочем процессе утверждения в управлении техническими изменениями.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-109">The product owner can also be used in the approval workflow in engineering change management.</span></span>

<span data-ttu-id="bf0b6-110">Владельцы продуктов являются глобальными параметрами.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-110">Product owners are global settings.</span></span> <span data-ttu-id="bf0b6-111">Поэтому они доступны для всех юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-111">Therefore, they are available to all legal entities.</span></span>

## <a name="create-a-product-owner-group"></a><span data-ttu-id="bf0b6-112">Создание группы владельцев продукта</span><span class="sxs-lookup"><span data-stu-id="bf0b6-112">Create a product owner group</span></span>

<span data-ttu-id="bf0b6-113">Чтобы создать группу владельцев продукта и добавить в нее участников, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-113">To create a product owner group and add members to it, follow these steps.</span></span>

1. <span data-ttu-id="bf0b6-114">Перейдите в раздел **Управление техническими изменениями \> Настройка \> Владельцы продуктов**.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-114">Go to **Engineering change management \> Setup \> Product owners**.</span></span>
2. <span data-ttu-id="bf0b6-115">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="bf0b6-116">В поле **Владелец продукта** введите имя группы.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-116">In the **Product owner** field, enter a name for the group.</span></span>
4. <span data-ttu-id="bf0b6-117">В поле **Имя** введите описание группы.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-117">In the **Name** field, enter a description of the group.</span></span>
5. <span data-ttu-id="bf0b6-118">На экспресс-вкладке **Участники** добавьте работников, которые должны быть участниками группы.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-118">On the **Members** FastTab, add the workers who should be members of the group.</span></span>

## <a name="assign-a-product-owner-to-a-product"></a><span data-ttu-id="bf0b6-119">Назначение владельца продукта для продукта</span><span class="sxs-lookup"><span data-stu-id="bf0b6-119">Assign a product owner to a product</span></span>

<span data-ttu-id="bf0b6-120">Чтобы назначить владельца продукта продукту, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-120">To assign a product owner to a product, follow these steps.</span></span>

1. <span data-ttu-id="bf0b6-121">Откройте страницу **Сведения о продукте** для соответствующего продукта или шаблона продукта.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-121">Open the **Product details** page for the relevant product or product master.</span></span>
1. <span data-ttu-id="bf0b6-122">На экспресс-вкладке **Общие** задайте в поле **Владелец продукта** имя соответствующей группы владельцев продукта.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-122">On the **General** FastTab, set the **Product owner** field to the name of the relevant product owner group.</span></span>

<span data-ttu-id="bf0b6-123">Когда владелец продукта назначен продукту, только участники группы владельцев продукта могут редактировать параметр **Владелец продукта**.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-123">While a product owner is assigned to a product, only the members of the product owner group can edit the **Product owner** setting.</span></span>

<span data-ttu-id="bf0b6-124">Владелец продукта также отображается на странице **Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-124">The product owner is also visible on the **Released products** page.</span></span>

## <a name="product-owners-and-product-releases"></a><span data-ttu-id="bf0b6-125">Владельцы продуктов и выпуски продуктов</span><span class="sxs-lookup"><span data-stu-id="bf0b6-125">Product owners and product releases</span></span>

<span data-ttu-id="bf0b6-126">Только пользователи из группы владельцев продукта могут выпускать этот продукт.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-126">Only users from a product's product owner group can release that product.</span></span> <span data-ttu-id="bf0b6-127">Однако имеется исключение, когда продукт является дочерней номенклатурой, и его родительский продукт выпускается владельцем родительского продукта.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-127">However, there is an exception when the product is a child item, and its parent is released by the parent's owner.</span></span> <span data-ttu-id="bf0b6-128">Другими словами, если продукт является частью спецификации другого продукта, система не проверяет владельца продукта для каждой номенклатуры в спецификации.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-128">In other words, if the product is part of the BOM of another product, the system doesn't check the product owner of each item in the BOM.</span></span> <span data-ttu-id="bf0b6-129">Проверяется только владелец продукта родительской номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-129">It checks only the product owner of the parent item.</span></span>

<span data-ttu-id="bf0b6-130">Например, продукт X назначен группе владельцев продуктов *Дизайнерские корпуса*.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-130">For example, product X is assigned to the *Design cabinets* product owner group.</span></span> <span data-ttu-id="bf0b6-131">Продукт X также является частью спецификации продукта Y, назначенной группе владельцев продуктов *Дизайнерские динамики*.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-131">Product X is also part of the BOM of product Y, which is assigned to the *Design Speakers* product owner group.</span></span> <span data-ttu-id="bf0b6-132">Если пользователь из группы владельцев продуктов *Дизайнерские динамики* выпускает продукт Y и его спецификацию, продукт X будет выпущен вместе с продуктом Y.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-132">If a user from the *Design Speakers* product owner group releases product Y and its BOM, product X will be released together with product Y.</span></span>

## <a name="product-owners-and-approvals"></a><span data-ttu-id="bf0b6-133">Владельцы продуктов и утверждения</span><span class="sxs-lookup"><span data-stu-id="bf0b6-133">Product owners and approvals</span></span>

<span data-ttu-id="bf0b6-134">Поскольку владельцы продуктов знают, будут ли конкретные технические изменения приносить пользу их продуктам, часто имеет смысл включить их в процесс утверждения в управлении техническими изменениями.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-134">Because product owners know whether specific engineering changes will benefit their products, it often makes sense to include them as part of the approval process in engineering change management.</span></span> <span data-ttu-id="bf0b6-135">Этот подход можно реализовать, настроив владельцев продуктов как поставщиков-участников в рабочих процессах, которые используются для управления техническими изменениями.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-135">You can implement this approach by setting up the product owners as participant providers in the workflows that are used for engineering change management.</span></span> <span data-ttu-id="bf0b6-136">Затем система присвоит задачи утверждения в рабочих процессах, основанных на продуктах, которые имеются в запросах технических изменений и заказах на технические изменения.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-136">The system will then assign approval tasks in the workflows, based on the products that are in engineering change requests and engineering change orders.</span></span> <span data-ttu-id="bf0b6-137">Дополнительные сведения см. в разделе [Управления изменениями для технологических продуктов](engineering-change-management.md).</span><span class="sxs-lookup"><span data-stu-id="bf0b6-137">For more information, see [Manage changes to engineering products](engineering-change-management.md).</span></span>