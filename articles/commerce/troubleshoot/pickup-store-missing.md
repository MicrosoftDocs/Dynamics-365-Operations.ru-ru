---
title: Розничный магазин не отображается в списке магазинов, из которого будет осуществляться самовывоз
description: В этом разделе приведены инструкции по устранению неполадок, которые могут помочь в том случае, когда розничный магазин не появляется в списке магазинов, в котором можно забрать товары самовывозом.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 652f5f1a779a412c21c18814071ba0fb7dd2e155
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585508"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a><span data-ttu-id="0e7a9-103">Розничный магазин не отображается в списке магазинов, из которого будет осуществляться самовывоз</span><span class="sxs-lookup"><span data-stu-id="0e7a9-103">Retail store doesn't appear in the list of stores to pick up from</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0e7a9-104">В этом разделе приведены инструкции по устранению неполадок, которые могут помочь в том случае, когда розничный магазин не появляется в списке магазинов, в котором можно забрать товары самовывозом.</span><span class="sxs-lookup"><span data-stu-id="0e7a9-104">This topic provides troubleshooting guidance that can help when a retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="description"></a><span data-ttu-id="0e7a9-105">описание</span><span class="sxs-lookup"><span data-stu-id="0e7a9-105">Description</span></span>

<span data-ttu-id="0e7a9-106">Розничный магазин не отображается в списке магазинов, в которых можно забрать товары самовывозом.</span><span class="sxs-lookup"><span data-stu-id="0e7a9-106">A retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="resolution"></a><span data-ttu-id="0e7a9-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="0e7a9-107">Resolution</span></span>

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a><span data-ttu-id="0e7a9-108">Настройте долготу и широту для адреса магазина в Commerce headquarters</span><span class="sxs-lookup"><span data-stu-id="0e7a9-108">Configure the longitude and latitude for the store address in Commerce headquarters</span></span>

<span data-ttu-id="0e7a9-109">Чтобы настроить долготу и широту для адреса магазина в Commerce headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0e7a9-109">To configure the longitude and latitude for the store address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="0e7a9-110">Перейдите в раздел **Retail и Commerce \> Каналы \> Магазины \> Все магазины**.</span><span class="sxs-lookup"><span data-stu-id="0e7a9-110">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="0e7a9-111">Найдите магазин, который должен отображаться среди параметров самовывоза на сайте электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="0e7a9-111">Find the store that you want to appear among the pickup options on the e-commerce site.</span></span> <span data-ttu-id="0e7a9-112">Запишите значение **номера операционной единицы**.</span><span class="sxs-lookup"><span data-stu-id="0e7a9-112">Make a note of its **Operating unit number** value.</span></span>
1. <span data-ttu-id="0e7a9-113">Перейдите в раздел **Управление организацией \> Организации \> Операционные единицы**.</span><span class="sxs-lookup"><span data-stu-id="0e7a9-113">Go to **Organization administration \> Organizations \> Operating units**.</span></span>
1. <span data-ttu-id="0e7a9-114">Выполните поиск номера операционной единицы, которую вы упомянули ранее, а затем выберите операционную единицу в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="0e7a9-114">Search for the operating unit number that you noted earlier, and then select the operating unit in the search results.</span></span>
1. <span data-ttu-id="0e7a9-115">На экспресс-вкладке **Адреса** выберите **Дополнительные параметры**, а затем выберите **Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="0e7a9-115">On the **Addresses** FastTab, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="0e7a9-116">На экспресс-вкладке **Общие** убедитесь, что поля **Долгота** и **Широта** установлены правильно.</span><span class="sxs-lookup"><span data-stu-id="0e7a9-116">On the **General** FastTab, make sure that the **Longitude** and **Latitude** fields are correctly set.</span></span> <span data-ttu-id="0e7a9-117">В ходе этого шага убедитесь, что значения правильно указаны как положительные или отрицательные числа.</span><span class="sxs-lookup"><span data-stu-id="0e7a9-117">As part of this step, make sure that the values are correctly specified as positive or negative numbers.</span></span>

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a><span data-ttu-id="0e7a9-118">Настройка групп выполнения в Commerce headquarters</span><span class="sxs-lookup"><span data-stu-id="0e7a9-118">Configure fulfillment groups in Commerce headquarters</span></span>

<span data-ttu-id="0e7a9-119">Чтобы настроить групп выполнения в Commerce Headquarters, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="0e7a9-119">To configure fulfillment groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="0e7a9-120">Перейдите в раздел **Retail и Commerce \> Каналы \> Интернет-магазины**.</span><span class="sxs-lookup"><span data-stu-id="0e7a9-120">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="0e7a9-121">Выберите интернет-магазин для настройки.</span><span class="sxs-lookup"><span data-stu-id="0e7a9-121">Select the online store to configure.</span></span>
1. <span data-ttu-id="0e7a9-122">На панели операций выберите **Настройка**, а затем выберите **Назначение группы выполнения**.</span><span class="sxs-lookup"><span data-stu-id="0e7a9-122">On the Action Pane, select **Set up**, and then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="0e7a9-123">На странице **Назначение группы выполнения** выберите группу выполнения для интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="0e7a9-123">On the **Fulfillment group assignment** page, select the fulfillment group for the online store.</span></span>
1. <span data-ttu-id="0e7a9-124">Убедитесь, что в разделе **Настройка** розничный магазин настроен правильно для группы выполнения.</span><span class="sxs-lookup"><span data-stu-id="0e7a9-124">Under **Setup**, make sure that the retail store is correctly configured for the fulfillment group.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0e7a9-125">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0e7a9-125">Additional resources</span></span> 

[<span data-ttu-id="0e7a9-126">Создание операционной единицы</span><span class="sxs-lookup"><span data-stu-id="0e7a9-126">Create an operating unit</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit)

[<span data-ttu-id="0e7a9-127">Настройка канала онлайн-торговли</span><span class="sxs-lookup"><span data-stu-id="0e7a9-127">Set up an online channel</span></span>](../channel-setup-online.md)
