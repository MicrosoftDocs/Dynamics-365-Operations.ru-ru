---
title: Добавление канала в организационную иерархию
description: В этом разделе описывается, как добавить канал в организационную иерархию в Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c7ff6d8ee7e526e45975cfa500b5e6d6079054dc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800695"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a><span data-ttu-id="b7aa3-103">Добавление канала в организационную иерархию</span><span class="sxs-lookup"><span data-stu-id="b7aa3-103">Add a channel to an organizational hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b7aa3-104">В этом разделе описывается, как добавить канал в организационную иерархию в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-104">This topic describes how to add a channel to an organizational hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b7aa3-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="b7aa3-105">Overview</span></span>

<span data-ttu-id="b7aa3-106">Каналы должны быть связаны с одной или несколькими организационными иерархиями.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-106">Channels need to be associated with one or more organizational hierarchies.</span></span> <span data-ttu-id="b7aa3-107">Перед созданием каналов необходимо подтвердить настройку организационных иерархий.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-107">Before creating channels, you need to confirm that your organizational hierarchies have been set up.</span></span>  

<span data-ttu-id="b7aa3-108">Дополнительные сведения о создании организационных иерархий см. [Организационные иерархии](channels-org-hierarchies.md).</span><span class="sxs-lookup"><span data-stu-id="b7aa3-108">See [Organizational hierarchies](channels-org-hierarchies.md) for more details on how to create organizational hierarchies.</span></span>

## <a name="select-a-hierarchy"></a><span data-ttu-id="b7aa3-109">Выберите иерархию</span><span class="sxs-lookup"><span data-stu-id="b7aa3-109">Select a hierarchy</span></span>

<span data-ttu-id="b7aa3-110">Чтобы выбрать иерархию, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-110">To select a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="b7aa3-111">В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Организационные иерархии**.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="b7aa3-112">В списке выберите организационную иерархию, к которой необходимо добавить канал.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-112">From the list, select the organization hierarchy that you'll be adding the channel to.</span></span>
1. <span data-ttu-id="b7aa3-113">В области действий выберите **Вид** для просмотра данных иерархии.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-113">On the action pane, select **View** to view hierarchy details.</span></span>

<span data-ttu-id="b7aa3-114">На следующем рисунке показаны данные организационной иерархии для выбранной иерархии.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-114">The following image shows organizational hierarchy details for the selected hierarchy.</span></span>

![Данные организационной иерархии для выбранной иерархии](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a><span data-ttu-id="b7aa3-116">Добавление канала к узел иерархии</span><span class="sxs-lookup"><span data-stu-id="b7aa3-116">Add a channel to a hierachy node</span></span>

<span data-ttu-id="b7aa3-117">Чтобы добавить канал в узел иерархии, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-117">To add a channel to a hierachy node, follow these steps.</span></span>

1. <span data-ttu-id="b7aa3-118">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-118">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="b7aa3-119">Выберите узел иерархии, к которому требуется добавить канал, затем в раскрывающемся списке **Вставка** выберите **Канал Retail**.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-119">Select the hierachy node you want the channel added to, then from the **Insert** drop-down list, select **Retail Channel**.</span></span> 
1. <span data-ttu-id="b7aa3-120">Выберите добавляемый канал, затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-120">Select the channel to add, then select the **OK** button.</span></span>
1. <span data-ttu-id="b7aa3-121">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-121">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="b7aa3-122">В области действий выберите **Опубликовать** и укажите **Действует с** в прошлом, чтобы это действие сразу запустилось.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-122">On the action pane, select **Publish** and provide an **Effective date** in the past to have this action go into effect immediately.</span></span>

<span data-ttu-id="b7aa3-123">На следующем рисунке показано, как выбрать канал для добавления в узел иерархии.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-123">The following image shows how to select a channel to add to a hierarchy node.</span></span>

![Выбор канала для добавления в узел иерархии](media/channel-add-to-org-hierarchy-2.png)

<span data-ttu-id="b7aa3-125">На следующем рисунке показана иерархия с различными добавленными каналами.</span><span class="sxs-lookup"><span data-stu-id="b7aa3-125">The following image shows a hierarchy with various channels added.</span></span>

![Иерархия, в которую добавлены различные каналы](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="b7aa3-127">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b7aa3-127">Additional resources</span></span>

[<span data-ttu-id="b7aa3-128">Обзор каналов</span><span class="sxs-lookup"><span data-stu-id="b7aa3-128">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="b7aa3-129">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="b7aa3-129">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="b7aa3-130">Обзор организаций и организационных иерархий</span><span class="sxs-lookup"><span data-stu-id="b7aa3-130">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="b7aa3-131">Планирование организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="b7aa3-131">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="b7aa3-132">Организационные иерархии</span><span class="sxs-lookup"><span data-stu-id="b7aa3-132">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="b7aa3-133">Настройка канала розничной торговли</span><span class="sxs-lookup"><span data-stu-id="b7aa3-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="b7aa3-134">Настройка интернет-канала</span><span class="sxs-lookup"><span data-stu-id="b7aa3-134">Set up an online channel</span></span>](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]