---
title: Создание списков рекомендаций по продукту
description: В этой теме объясняется, как менеджер по сбыту может создавать списки продуктов вручную для клиентов Microsoft Dynamics 365 Commerce и управлять ими.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6d075635b7b986cc854550d15f7e941a9ea9cf72
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770421"
---
# <a name="create-curated-product-recommendation-lists"></a><span data-ttu-id="efab0-103">Создание списков рекомендаций по продукту</span><span class="sxs-lookup"><span data-stu-id="efab0-103">Create curated product recommendation lists</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="efab0-104">В этой теме объясняется, как менеджер по сбыту может создавать списки продуктов вручную для клиентов Microsoft Dynamics 365 Commerce и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="efab0-104">This topic explains how merchandizers can create and manage manual product lists for Microsoft Dynamics 365 Commerce customers.</span></span>

<span data-ttu-id="efab0-105">Проверенные списки представляют собой наборы отдельных материалов, созданных и проверенных людьми.</span><span class="sxs-lookup"><span data-stu-id="efab0-105">Curated lists are collections of individual content created and curated by people.</span></span>  

## <a name="create-a-new-list"></a><span data-ttu-id="efab0-106">Создание нового списка</span><span class="sxs-lookup"><span data-stu-id="efab0-106">Create a new list</span></span>

<span data-ttu-id="efab0-107">Для создания проверенного списка рекомендаций продуктов выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="efab0-107">To create a curated product recommendation list, follow these steps.</span></span>

1. <span data-ttu-id="efab0-108">Выберите **Retail** &gt; **Рекомендации продуктов** &gt; **Списки рекомендаций**.</span><span class="sxs-lookup"><span data-stu-id="efab0-108">Go to **Retail** &gt; **Product recommendations** &gt; **Recommendation lists**.</span></span>
1. <span data-ttu-id="efab0-109">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="efab0-109">Select **New**.</span></span>
1. <span data-ttu-id="efab0-110">В поле **Код списка** введите значение.</span><span class="sxs-lookup"><span data-stu-id="efab0-110">In the **List Id** field, enter a value.</span></span>
1. <span data-ttu-id="efab0-111">В поле **Имя списка** введите значение.</span><span class="sxs-lookup"><span data-stu-id="efab0-111">In the **List name** field, enter a value.</span></span>
    - <span data-ttu-id="efab0-112">**Имя списка** является названием списка, которое будет отображаться в разделе проверенных списков модуля **Семейство продуктов**.</span><span class="sxs-lookup"><span data-stu-id="efab0-112">The **List name** is the title of the list that will appear in the curated lists section of the **Product collection** module.</span></span>
1. <span data-ttu-id="efab0-113">Чтобы добавить продукты в список, выберите **Добавить продукты**.</span><span class="sxs-lookup"><span data-stu-id="efab0-113">To add products to the list, select **Add products**.</span></span>
1. <span data-ttu-id="efab0-114">Чтобы изменить порядок продуктов в списке, введите значение в столбец **Порядок просмотра**.</span><span class="sxs-lookup"><span data-stu-id="efab0-114">To change the order of the products in the list, enter a value in the **Display order** column.</span></span>
    - <span data-ttu-id="efab0-115">Если два продукта имеют одинаковое значение порядок отображения, то окончательный порядок этих двух результатов также будет зависит от серверной части.</span><span class="sxs-lookup"><span data-stu-id="efab0-115">If two products have the same display order value, then the final order of those two results may differ from the back office.</span></span>
1. <span data-ttu-id="efab0-116">Выберите **Сохранить**, чтобы сохранить список.</span><span class="sxs-lookup"><span data-stu-id="efab0-116">Select **Save** to save the list.</span></span>

## <a name="example-list"></a><span data-ttu-id="efab0-117">Пример списка</span><span class="sxs-lookup"><span data-stu-id="efab0-117">Example List</span></span>

![Пример проверенного списка в серверной части](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a><span data-ttu-id="efab0-119">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="efab0-119">Additional resources</span></span>

[<span data-ttu-id="efab0-120">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="efab0-120">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="efab0-121">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="efab0-121">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="efab0-122">Добавление списков рекомендации продуктов на страницы</span><span class="sxs-lookup"><span data-stu-id="efab0-122">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
