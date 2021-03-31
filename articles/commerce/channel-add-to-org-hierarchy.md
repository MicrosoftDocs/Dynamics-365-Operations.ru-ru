---
title: Добавление канала в организационную иерархию
description: В этом разделе описывается, как добавить канал в организационную иерархию в Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4212797d2959c4f8b0d60e6b45de76ffc3ee0dc2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216768"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a><span data-ttu-id="d4fb0-103">Добавление канала в организационную иерархию</span><span class="sxs-lookup"><span data-stu-id="d4fb0-103">Add a channel to an organizational hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d4fb0-104">В этом разделе описывается, как добавить канал в организационную иерархию в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d4fb0-104">This topic describes how to add a channel to an organizational hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d4fb0-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="d4fb0-105">Overview</span></span>

<span data-ttu-id="d4fb0-106">Каналы должны быть связаны с одной или несколькими организационными иерархиями.</span><span class="sxs-lookup"><span data-stu-id="d4fb0-106">Channels need to be associated with one or more organizational hierarchies.</span></span> <span data-ttu-id="d4fb0-107">Перед созданием каналов необходимо подтвердить настройку организационных иерархий.</span><span class="sxs-lookup"><span data-stu-id="d4fb0-107">Before creating channels, you need to confirm that your organizational hierarchies have been set up.</span></span>  

<span data-ttu-id="d4fb0-108">Дополнительные сведения о создании организационных иерархий см. [Организационные иерархии](channels-org-hierarchies.md).</span><span class="sxs-lookup"><span data-stu-id="d4fb0-108">See [Organizational hierarchies](channels-org-hierarchies.md) for more details on how to create organizational hierarchies.</span></span>

## <a name="select-a-hierarchy"></a><span data-ttu-id="d4fb0-109">Выберите иерархию</span><span class="sxs-lookup"><span data-stu-id="d4fb0-109">Select a hierarchy</span></span>

<span data-ttu-id="d4fb0-110">Чтобы выбрать иерархию, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d4fb0-110">To select a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="d4fb0-111">В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Организационные иерархии**.</span><span class="sxs-lookup"><span data-stu-id="d4fb0-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="d4fb0-112">В списке выберите организационную иерархию, к которой необходимо добавить канал.</span><span class="sxs-lookup"><span data-stu-id="d4fb0-112">From the list, select the organization hierarchy that you'll be adding the channel to.</span></span>
1. <span data-ttu-id="d4fb0-113">В области действий выберите **Вид** для просмотра данных иерархии.</span><span class="sxs-lookup"><span data-stu-id="d4fb0-113">On the action pane, select **View** to view hierarchy details.</span></span>

<span data-ttu-id="d4fb0-114">На следующем рисунке показаны данные организационной иерархии для выбранной иерархии.</span><span class="sxs-lookup"><span data-stu-id="d4fb0-114">The following image shows organizational hierarchy details for the selected hierarchy.</span></span>

![Данные организационной иерархии для выбранной иерархии](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a><span data-ttu-id="d4fb0-116">Добавление канала к узел иерархии</span><span class="sxs-lookup"><span data-stu-id="d4fb0-116">Add a channel to a hierachy node</span></span>

<span data-ttu-id="d4fb0-117">Чтобы добавить канал в узел иерархии, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d4fb0-117">To add a channel to a hierachy node, follow these steps.</span></span>

1. <span data-ttu-id="d4fb0-118">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="d4fb0-118">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="d4fb0-119">Выберите узел иерархии, к которому требуется добавить канал, затем в раскрывающемся списке **Вставка** выберите **Канал Retail**.</span><span class="sxs-lookup"><span data-stu-id="d4fb0-119">Select the hierachy node you want the channel added to, then from the **Insert** drop-down list, select **Retail Channel**.</span></span> 
1. <span data-ttu-id="d4fb0-120">Выберите добавляемый канал, затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d4fb0-120">Select the channel to add, then select the **OK** button.</span></span>
1. <span data-ttu-id="d4fb0-121">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d4fb0-121">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="d4fb0-122">В области действий выберите **Опубликовать** и укажите **Действует с** в прошлом, чтобы это действие сразу запустилось.</span><span class="sxs-lookup"><span data-stu-id="d4fb0-122">On the action pane, select **Publish** and provide an **Effective date** in the past to have this action go into effect immediately.</span></span>

<span data-ttu-id="d4fb0-123">На следующем рисунке показано, как выбрать канал для добавления в узел иерархии.</span><span class="sxs-lookup"><span data-stu-id="d4fb0-123">The following image shows how to select a channel to add to a hierarchy node.</span></span>

![Выбор канала для добавления в узел иерархии](media/channel-add-to-org-hierarchy-2.png)

<span data-ttu-id="d4fb0-125">На следующем рисунке показана иерархия с различными добавленными каналами.</span><span class="sxs-lookup"><span data-stu-id="d4fb0-125">The following image shows a hierarchy with various channels added.</span></span>

![Иерархия, в которую добавлены различные каналы](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="d4fb0-127">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d4fb0-127">Additional resources</span></span>

[<span data-ttu-id="d4fb0-128">Обзор каналов</span><span class="sxs-lookup"><span data-stu-id="d4fb0-128">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="d4fb0-129">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="d4fb0-129">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="d4fb0-130">Обзор организаций и организационных иерархий</span><span class="sxs-lookup"><span data-stu-id="d4fb0-130">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="d4fb0-131">Планирование организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="d4fb0-131">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="d4fb0-132">Организационные иерархии</span><span class="sxs-lookup"><span data-stu-id="d4fb0-132">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="d4fb0-133">Настройка канала розничной торговли</span><span class="sxs-lookup"><span data-stu-id="d4fb0-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="d4fb0-134">Настройка интернет-канала</span><span class="sxs-lookup"><span data-stu-id="d4fb0-134">Set up an online channel</span></span>](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]