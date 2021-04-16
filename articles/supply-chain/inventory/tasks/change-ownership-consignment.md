---
title: Изменение владельца консигнационных запасов на основе производственного спроса
description: Эта процедура показывает порядок изменения владельца запасов коносамента с поставщика на юридическое лицо, когда имеется спрос на запасы в производстве.
author: perlynne
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6385fba0b6288416a85f1b7de73d3bb4972a852a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834129"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="6a828-103">Изменение владельца консигнационных запасов на основе производственного спроса</span><span class="sxs-lookup"><span data-stu-id="6a828-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6a828-104">Эта процедура показывает порядок изменения владельца запасов коносамента с поставщика на юридическое лицо, когда имеется спрос на запасы в производстве.</span><span class="sxs-lookup"><span data-stu-id="6a828-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="6a828-105">Это изменение собственности осуществляется посредством создания и разноски журнала изменения владельца запасов.</span><span class="sxs-lookup"><span data-stu-id="6a828-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="6a828-106">Строки журнала изменения владельца можно создавать вручную или, как показано в этой записи, на основе существующего производственного спроса.</span><span class="sxs-lookup"><span data-stu-id="6a828-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="6a828-107">Обычно эту задачу выполняет начальник цеха.</span><span class="sxs-lookup"><span data-stu-id="6a828-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="6a828-108">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="6a828-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="6a828-109">При использовании собственных данных убедитесь, что выполнены следующие предварительные условия: имя журнала запасов настроено для изменения владельца запасов, физически записанные принадлежащие поставщику номенклатуры в наличии и одна или несколько строк производственного заказа для материала.</span><span class="sxs-lookup"><span data-stu-id="6a828-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="6a828-110">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="6a828-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

> [!NOTE]
> <span data-ttu-id="6a828-111">Процессы исходящего коносамента не поддерживаются в готовом виде, и автоматическая обработка журнала владения не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6a828-111">Outbound consignment processes are not supported out-of-the-box and automatic ownership journal processing is not supported.</span></span>

## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="6a828-112">Создание журнала владения запасами</span><span class="sxs-lookup"><span data-stu-id="6a828-112">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="6a828-113">Перейдите в раздел "Управление запасами" > "Записи журнала" > "Номенклатуры" > "Изменение владельца запасов".</span><span class="sxs-lookup"><span data-stu-id="6a828-113">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="6a828-114">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6a828-114">Click New.</span></span>
    * <span data-ttu-id="6a828-115">Журнал изменения владельца запасов используется для изменения владельца запасов коносамента с поставщика на текущее юридическое лицо.</span><span class="sxs-lookup"><span data-stu-id="6a828-115">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="6a828-116">Это изменение владельца производится путем отпуска запасов в наличии, принадлежащих поставщику, а затем получения этих запасов в текущем юридическом лице.</span><span class="sxs-lookup"><span data-stu-id="6a828-116">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="6a828-117">В поле "Имя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6a828-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="6a828-118">Можно выбрать только имена журналов запасов, которые имеют тип журнала "Изменение владельца".</span><span class="sxs-lookup"><span data-stu-id="6a828-118">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="6a828-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="6a828-119">Click OK.</span></span>
5. <span data-ttu-id="6a828-120">Щелкните Функции.</span><span class="sxs-lookup"><span data-stu-id="6a828-120">Click Functions.</span></span>
6. <span data-ttu-id="6a828-121">Щелкните "Создать строки журнала из производственных заказов".</span><span class="sxs-lookup"><span data-stu-id="6a828-121">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="6a828-122">Можно начать процесс изменения владения, запросив все строки производства, которые имеют спрос для потребления сырья.</span><span class="sxs-lookup"><span data-stu-id="6a828-122">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="6a828-123">В поле "Включаемые статусы расхода запасов" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="6a828-123">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="6a828-124">Этот параметр позволяет фильтровать по статусу расхода складских проводок.</span><span class="sxs-lookup"><span data-stu-id="6a828-124">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="6a828-125">Например, можно создать строки журнала для запасов со статусами "Скомплектовано" и "Физ. зарезервировано".</span><span class="sxs-lookup"><span data-stu-id="6a828-125">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="6a828-126">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="6a828-126">Expand the Records to include section.</span></span>
    * <span data-ttu-id="6a828-127">Этот раздел позволяет применять дополнительную фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="6a828-127">This section lets you apply additional filtering.</span></span> <span data-ttu-id="6a828-128">Например, можно выбрать определенную дату для сырья.</span><span class="sxs-lookup"><span data-stu-id="6a828-128">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="6a828-129">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="6a828-129">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="6a828-130">Разноска журнала изменения владельцев запасов</span><span class="sxs-lookup"><span data-stu-id="6a828-130">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="6a828-131">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="6a828-131">Click Post.</span></span>
    * <span data-ttu-id="6a828-132">При разноске журнала принадлежащие поставщику запасы выпускаются с помощью ссылки "Изменение владельца".</span><span class="sxs-lookup"><span data-stu-id="6a828-132">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="6a828-133">Затем запасы получаются как имеющиеся в наличии с помощью складской проводки, которая обновляется с использованием поступления продуктов заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="6a828-133">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="6a828-134">Обратите внимание, что создаются только проводки, относящиеся к разнесенному журналу.</span><span class="sxs-lookup"><span data-stu-id="6a828-134">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="6a828-135">Никакие ожидающиеся складские проводки не создаются.</span><span class="sxs-lookup"><span data-stu-id="6a828-135">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="6a828-136">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="6a828-136">Click OK.</span></span>
3. <span data-ttu-id="6a828-137">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6a828-137">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]