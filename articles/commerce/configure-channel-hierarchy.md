---
title: Настройка канала для использования навигационной иерархии канала
description: В этом разделе описывается, как настроить канал для использования навигационной иерархии канала в Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: ceb6aa65c2ed5bc8d4224bdaf7095fba769181e8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220590"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a><span data-ttu-id="3aa03-103">Настройка канала для использования навигационной иерархии канала</span><span class="sxs-lookup"><span data-stu-id="3aa03-103">Configure a channel to use a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3aa03-104">В этом разделе описывается, как настроить канал для использования навигационной иерархии канала в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3aa03-104">This topic describes how to configure a channel to use a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3aa03-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="3aa03-105">Overview</span></span>

<span data-ttu-id="3aa03-106">Навигационные иерархии канала объединяют продукты в категории, чтобы продукты могли просматриваться на веб-узле электронной коммерции или в POS-терминалах.</span><span class="sxs-lookup"><span data-stu-id="3aa03-106">Channel navigation hierarchies organize products into categories so that the products can be browsed on an e-Commerce site or at points of sale (POS).</span></span> <span data-ttu-id="3aa03-107">Розничные и интернет-каналы должны быть сконфигурированы с помощью навигационной иерархии канала.</span><span class="sxs-lookup"><span data-stu-id="3aa03-107">Retail and online channels must be configured with channel navigation hierarchies.</span></span>

## <a name="configure-the-channel"></a><span data-ttu-id="3aa03-108">Настройка канала</span><span class="sxs-lookup"><span data-stu-id="3aa03-108">Configure the channel</span></span>

<span data-ttu-id="3aa03-109">Чтобы настроить канал для использования навигационной иерархии канала, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3aa03-109">To configure a channel to use a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="3aa03-110">В области переходов выберите **Модули \> Розничная торговля и коммерция \> Настройка канала \> Категории канала и атрибуты продуктов**.</span><span class="sxs-lookup"><span data-stu-id="3aa03-110">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="3aa03-111">Выберите канал для настройки.</span><span class="sxs-lookup"><span data-stu-id="3aa03-111">Select the channel to configure.</span></span>
1. <span data-ttu-id="3aa03-112">В области действий выберите **Задать метаданные атрибута**.</span><span class="sxs-lookup"><span data-stu-id="3aa03-112">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="3aa03-113">В раскрывающемся списке **Иерархия категорий** выберите соответствующую навигационную иерархию канала.</span><span class="sxs-lookup"><span data-stu-id="3aa03-113">In the **Category hierarchy** drop-down list, select the appropriate channel navigation hierarchy.</span></span>
1. <span data-ttu-id="3aa03-114">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3aa03-114">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="3aa03-115">В **Группа атрибутов** добавьте любые группы атрибутов, которые будут глобальными атрибутами для всех узлов.</span><span class="sxs-lookup"><span data-stu-id="3aa03-115">Under **Attribute group**, add any attribute groups that will be global attributes for all nodes.</span></span>

<span data-ttu-id="3aa03-116">На следующем рисунке показано, как настроить канал для использования навигационной иерархии канала.</span><span class="sxs-lookup"><span data-stu-id="3aa03-116">The following image shows how to configure a channel to use a channel navigation hierarchy.</span></span>

![Пример конфигурации канала](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a><span data-ttu-id="3aa03-118">Задать метаданные атрибута</span><span class="sxs-lookup"><span data-stu-id="3aa03-118">Set attribute metadata</span></span>

<span data-ttu-id="3aa03-119">Задание метаданных атрибута разрешит настройку атрибутов на каждом узле.</span><span class="sxs-lookup"><span data-stu-id="3aa03-119">Setting the attribute metadata will allow configuration of attributes on each node.</span></span>

<span data-ttu-id="3aa03-120">Чтобы задать метаданные атрибутов, сделайте следующее.</span><span class="sxs-lookup"><span data-stu-id="3aa03-120">To set attribute metadata, follow these steps.</span></span>

1. <span data-ttu-id="3aa03-121">В области действий выберите **Задать метаданные атрибута**.</span><span class="sxs-lookup"><span data-stu-id="3aa03-121">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="3aa03-122">Для каждого узла выберите **Атрибуты продукта канала**.</span><span class="sxs-lookup"><span data-stu-id="3aa03-122">For each node select **Channel product attributes**.</span></span>
1. <span data-ttu-id="3aa03-123">Установите для **Показать атрибут для канала** значение **Да** и для **Возможно уточнение** значение **Да**, чтобы включить уточнения для этого канала.</span><span class="sxs-lookup"><span data-stu-id="3aa03-123">Set **Show attribute on channel** to **Yes** and **Can be refined** to **Yes**, to enable refiners on that channel.</span></span>
1. <span data-ttu-id="3aa03-124">После настройки каждого узла в **области действий** нажмите кнопку **Сохранить** для сохранения.</span><span class="sxs-lookup"><span data-stu-id="3aa03-124">After configuring each node as desired, on the **Action pane**, select the **Save** button to save.</span></span>
1. <span data-ttu-id="3aa03-125">Выберите **X** в верхнем правом углу, чтобы закрыть этот экран и вернуться назад на страницу **Категории каналов и атрибуты продукта**.</span><span class="sxs-lookup"><span data-stu-id="3aa03-125">Select the **X** in the top right corner to exit this screen back to the **Channel categories and product attributes** page.</span></span>

<span data-ttu-id="3aa03-126">На следующем рисунке показан пример набора атрибутов продукта канала, настроенных в узле категории канала.</span><span class="sxs-lookup"><span data-stu-id="3aa03-126">The following image shows an example set of channel product attributes configured on a channel category node.</span></span>

![Атрибуты канала в узле категории каналов](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a><span data-ttu-id="3aa03-128">Публикация изменений</span><span class="sxs-lookup"><span data-stu-id="3aa03-128">Publish changes</span></span>

<span data-ttu-id="3aa03-129">Чтобы изменения вступили в силу, необходимо опубликовать изменения.</span><span class="sxs-lookup"><span data-stu-id="3aa03-129">For changes to take effect, you will need to publish the changes.</span></span>

<span data-ttu-id="3aa03-130">Чтобы опубликовать изменения, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3aa03-130">To publish changes, follow these steps.</span></span>

1. <span data-ttu-id="3aa03-131">В области действий выберите **Опубликовать обновления канала**.</span><span class="sxs-lookup"><span data-stu-id="3aa03-131">On the action pane, select **Publish channel updates**.</span></span>
1. <span data-ttu-id="3aa03-132">В области **Опубликовать обновления канала** выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3aa03-132">In the **Publish channel updates** pane, select **OK**.</span></span>

<span data-ttu-id="3aa03-133">На следующем рисунке показано, как опубликовать обновления канала.</span><span class="sxs-lookup"><span data-stu-id="3aa03-133">The following image shows how to publish channel updates.</span></span>

![Опубликовать обновления канала](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="3aa03-135">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3aa03-135">Additional resources</span></span>

[<span data-ttu-id="3aa03-136">Создание навигационной иерархии канала</span><span class="sxs-lookup"><span data-stu-id="3aa03-136">Create a channel navigation hierarchy</span></span>](create-channel-hierarchy.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]