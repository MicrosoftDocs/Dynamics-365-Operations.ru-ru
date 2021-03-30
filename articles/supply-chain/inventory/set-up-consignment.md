---
title: Настройка коносамента
description: В этом разделе описаны способы настройки входящих операций консигнационных запасов.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 00102f5c7a043c5ca22458a53b1445c57c61957c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209571"
---
# <a name="set-up-consignment"></a><span data-ttu-id="ee273-103">Настройка коносамента</span><span class="sxs-lookup"><span data-stu-id="ee273-103">Set up consignment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee273-104">В этом разделе описаны способы настройки входящих операций консигнационных запасов.</span><span class="sxs-lookup"><span data-stu-id="ee273-104">This topic explains how to configure inbound consignment inventory operations.</span></span>

<span data-ttu-id="ee273-105">Консигнационные запасы — это запасы, принадлежащие поставщику, но хранящиеся на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="ee273-105">Consignment inventory is inventory that’s owned by a vendor, but stored at your site.</span></span> <span data-ttu-id="ee273-106">Когда вы готовы потребить или использовать запасы, вы принимаете на себя владение запасами.</span><span class="sxs-lookup"><span data-stu-id="ee273-106">When you’re ready to consume or use the inventory, you take over the ownership of the inventory.</span></span> <span data-ttu-id="ee273-107">В этом разделе описывается настройка, необходимая для включения процессов коносамента.</span><span class="sxs-lookup"><span data-stu-id="ee273-107">This topic describes the setup needed to enable consignment processes.</span></span> <span data-ttu-id="ee273-108">Дополнительные сведения о процессах коносамента см. в разделе [Настройка консигнации](consignment.md).</span><span class="sxs-lookup"><span data-stu-id="ee273-108">For more information about consignment processes, see [Set up consignment](consignment.md).</span></span>

## <a name="inventory-owners"></a><span data-ttu-id="ee273-109">Владельцы запасов</span><span class="sxs-lookup"><span data-stu-id="ee273-109">Inventory owners</span></span>
<span data-ttu-id="ee273-110">Для записи физических входящих консигнационных запасов необходимо указать владельца поставщика.</span><span class="sxs-lookup"><span data-stu-id="ee273-110">In order to record physical inbound consignment inventory, you need to define a vendor owner.</span></span> <span data-ttu-id="ee273-111">Это выполняется на странице **Владелец запасов**.</span><span class="sxs-lookup"><span data-stu-id="ee273-111">This is done on the **Inventory owner** page.</span></span> <span data-ttu-id="ee273-112">При выборе параметра **Счет поставщика** это создает значения по умолчанию для полей **Наименование** и **Владелец**.</span><span class="sxs-lookup"><span data-stu-id="ee273-112">When you select a **Vendor account** this generates default values for the **Name** and **Owner** fields.</span></span> <span data-ttu-id="ee273-113">Значение в поле **Владелец** будет отображаться поставщику, поэтому возможно, потребуется изменить его, если ваши названия счетов поставщика непонятны внешним лицам.</span><span class="sxs-lookup"><span data-stu-id="ee273-113">The value in the **Owner** field will be visible to the vendor, so you might want to change it if your vendor account names aren’t easy for external people to recognize.</span></span> <span data-ttu-id="ee273-114">Можно изменить поле **Владелец**, но только до момента, когда вы сохраняете запись **Владелец запасов**.</span><span class="sxs-lookup"><span data-stu-id="ee273-114">It’s possible to edit the **Owner** field, but only up to the point when you save the **Inventory owner** record.</span></span> <span data-ttu-id="ee273-115">Поле **Наименование** заполняется именем субъекта, с которым связан счет поставщика, и это невозможно изменить.</span><span class="sxs-lookup"><span data-stu-id="ee273-115">The **Name** field is populated with the name of the party that the vendor account is associated with, and this cannot be changed.</span></span>

<span data-ttu-id="ee273-116">[![владельцы-запасов](./media/inventory-owners.png)](./media/inventory-owners.png)</span><span class="sxs-lookup"><span data-stu-id="ee273-116">[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)</span></span>

## <a name="tracking-dimension-group"></a><span data-ttu-id="ee273-117">Группа аналитик отслеживания</span><span class="sxs-lookup"><span data-stu-id="ee273-117">Tracking dimension group</span></span>
<span data-ttu-id="ee273-118">Номенклатуры, которые будут использоваться в процессе коносамента, необходимо связать с параметром **Группа аналитик отслеживания**, в которой для аналитики **Владелец** задано значение **Активна**.</span><span class="sxs-lookup"><span data-stu-id="ee273-118">Items that are going to be used in consignment processes must be associated with a **Tracking dimension group** where the **Owner** dimension is set to **Active**.</span></span> <span data-ttu-id="ee273-119">У аналитики "Владелец" всегда выбраны параметры **Физические запасы** и **Финансовые запасы**.</span><span class="sxs-lookup"><span data-stu-id="ee273-119">The Owner dimension always has the **Physical inventory** and **Financial inventory** options selected.</span></span> <span data-ttu-id="ee273-120">Параметр **План покрытия по аналитикам** никогда не выбран.</span><span class="sxs-lookup"><span data-stu-id="ee273-120">The **Coverage plan by dimension** is never selected.</span></span>

<span data-ttu-id="ee273-121">[![группа-аналитик-отслеживания](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span><span class="sxs-lookup"><span data-stu-id="ee273-121">[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span></span>

## <a name="inventory-ownership-change-journal"></a><span data-ttu-id="ee273-122">Журнал изменения владельца запасов</span><span class="sxs-lookup"><span data-stu-id="ee273-122">Inventory ownership change journal</span></span>
<span data-ttu-id="ee273-123">Журнал **Изменение владельца запасов** используется для регистрации передачи прав собственности на запасы коносамента от поставщика юридическому лицу, которое потребляет их.</span><span class="sxs-lookup"><span data-stu-id="ee273-123">The **Inventory ownership change** journal is used to record the transfer of ownership of consignment inventory from the vendor to the legal entity that’s consuming it.</span></span> <span data-ttu-id="ee273-124">Как и любой журнал запасов, его необходимо определить с именем журнала запасов.</span><span class="sxs-lookup"><span data-stu-id="ee273-124">Like any inventory journal, it must be identified with an Inventory journal name.</span></span> <span data-ttu-id="ee273-125">Эти имена создаются на странице **Имена журналов запасов**, а для параметра **Тип журнала** должно быть установлено значение **Изменение владельца**.</span><span class="sxs-lookup"><span data-stu-id="ee273-125">These names are created on the **Inventory journal names** page, and the **Journal type** must be set to **Ownership change**.</span></span>

<span data-ttu-id="ee273-126">[![журнал-изменения-владельца-запасов](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span><span class="sxs-lookup"><span data-stu-id="ee273-126">[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span></span>

## <a name="vendor-collaboration-in-consignment-processes"></a><span data-ttu-id="ee273-127">Совместная работа с поставщиками в процессах коносамента</span><span class="sxs-lookup"><span data-stu-id="ee273-127">Vendor collaboration in consignment processes</span></span>
<span data-ttu-id="ee273-128">Если поставщики используют интерфейс совместной работы с поставщиками, они могут использовать его, чтобы контролировать потребление запасов на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="ee273-128">If your vendors are using the vendor collaboration interface, they can use this to monitor the consumption of inventory at your site.</span></span> <span data-ttu-id="ee273-129">Дополнительные сведения о настройке поставщиков для использования совместной работы с поставщиками см. в разделе [Безопасность пользователя портала поставщика](../procurement/configure-security-vendor-portal-users.md).</span><span class="sxs-lookup"><span data-stu-id="ee273-129">For more information about setting up vendors to use vendor collaboration, see [Vendor portal user security](../procurement/configure-security-vendor-portal-users.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]