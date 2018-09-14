--- 
title: "Изменение владельца консигнационных запасов на основе производственного спроса"
description: "Эта процедура показывает порядок изменения владельца запасов коносамента с поставщика на юридическое лицо, когда имеется спрос на запасы в производстве."
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: d1324da6996230eb383e2f37d3a133ec35cb0f41
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="20117-103">Изменение владельца консигнационных запасов на основе производственного спроса</span><span class="sxs-lookup"><span data-stu-id="20117-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="20117-104">Эта процедура показывает порядок изменения владельца запасов коносамента с поставщика на юридическое лицо, когда имеется спрос на запасы в производстве.</span><span class="sxs-lookup"><span data-stu-id="20117-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="20117-105">Это изменение собственности осуществляется посредством создания и разноски журнала изменения владельца запасов.</span><span class="sxs-lookup"><span data-stu-id="20117-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="20117-106">Строки журнала изменения владельца можно создавать вручную или, как показано в этой записи, на основе существующего производственного спроса.</span><span class="sxs-lookup"><span data-stu-id="20117-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="20117-107">Обычно эту задачу выполняет начальник цеха.</span><span class="sxs-lookup"><span data-stu-id="20117-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="20117-108">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="20117-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="20117-109">При использовании собственных данных убедитесь, что выполнены следующие предварительные условия: имя журнала запасов настроено для изменения владельца запасов, физически записанные принадлежащие поставщику номенклатуры в наличии и одна или несколько строк производственного заказа для материала.</span><span class="sxs-lookup"><span data-stu-id="20117-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="20117-110">Эта процедура предназначена для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="20117-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="20117-111">Создание журнала владения запасами</span><span class="sxs-lookup"><span data-stu-id="20117-111">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="20117-112">Перейдите в раздел "Управление запасами" > "Записи журнала" > "Номенклатуры" > "Изменение владельца запасов".</span><span class="sxs-lookup"><span data-stu-id="20117-112">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="20117-113">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="20117-113">Click New.</span></span>
    * <span data-ttu-id="20117-114">Журнал изменения владельца запасов используется для изменения владельца запасов коносамента с поставщика на текущее юридическое лицо.</span><span class="sxs-lookup"><span data-stu-id="20117-114">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="20117-115">Это изменение владельца производится путем отпуска запасов в наличии, принадлежащих поставщику, а затем получения этих запасов в текущем юридическом лице.</span><span class="sxs-lookup"><span data-stu-id="20117-115">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="20117-116">В поле "Имя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="20117-116">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="20117-117">Можно выбрать только имена журналов запасов, которые имеют тип журнала "Изменение владельца".</span><span class="sxs-lookup"><span data-stu-id="20117-117">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="20117-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="20117-118">Click OK.</span></span>
5. <span data-ttu-id="20117-119">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="20117-119">Click Functions.</span></span>
6. <span data-ttu-id="20117-120">Щелкните "Создать строки журнала из производственных заказов".</span><span class="sxs-lookup"><span data-stu-id="20117-120">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="20117-121">Можно начать процесс изменения владения, запросив все строки производства, которые имеют спрос для потребления сырья.</span><span class="sxs-lookup"><span data-stu-id="20117-121">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="20117-122">В поле "Включаемые статусы расхода запасов" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="20117-122">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="20117-123">Этот параметр позволяет фильтровать по статусу расхода складских проводок.</span><span class="sxs-lookup"><span data-stu-id="20117-123">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="20117-124">Например, можно создать строки журнала для запасов со статусами "Скомплектовано" и "Физ. зарезервировано".</span><span class="sxs-lookup"><span data-stu-id="20117-124">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="20117-125">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="20117-125">Expand the Records to include section.</span></span>
    * <span data-ttu-id="20117-126">Этот раздел позволяет применять дополнительную фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="20117-126">This section lets you apply additional filtering.</span></span> <span data-ttu-id="20117-127">Например, можно выбрать определенную дату для сырья.</span><span class="sxs-lookup"><span data-stu-id="20117-127">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="20117-128">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="20117-128">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="20117-129">Разноска журнала изменения владельцев запасов</span><span class="sxs-lookup"><span data-stu-id="20117-129">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="20117-130">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="20117-130">Click Post.</span></span>
    * <span data-ttu-id="20117-131">При разноске журнала принадлежащие поставщику запасы выпускаются с помощью ссылки "Изменение владельца".</span><span class="sxs-lookup"><span data-stu-id="20117-131">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="20117-132">Затем запасы получаются как имеющиеся в наличии с помощью складской проводки, которая обновляется с использованием поступления продуктов заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="20117-132">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="20117-133">Обратите внимание, что создаются только проводки, относящиеся к разнесенному журналу.</span><span class="sxs-lookup"><span data-stu-id="20117-133">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="20117-134">Никакие ожидающиеся складские проводки не создаются.</span><span class="sxs-lookup"><span data-stu-id="20117-134">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="20117-135">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="20117-135">Click OK.</span></span>
3. <span data-ttu-id="20117-136">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="20117-136">Close the page.</span></span>


