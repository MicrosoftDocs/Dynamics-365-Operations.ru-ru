---
title: Создание контролируемых рекомендаций вручную
description: В этой теме объясняется, как менеджер по сбыту может вручную создавать списки продуктов для клиентов Microsoft Dynamics 365 Commerce и управлять ими.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: 0b866704b419fb07dcf1ddd386af2f7d6cfa02e2
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404124"
---
# <a name="manually-create-curated-recommendations"></a><span data-ttu-id="8d920-103">Создание контролируемых рекомендаций вручную</span><span class="sxs-lookup"><span data-stu-id="8d920-103">Manually create curated recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8d920-104">В этой теме объясняется, как менеджер по сбыту может вручную создавать списки рекомендаций продуктов для клиентов Microsoft Dynamics 365 Commerce и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="8d920-104">This topic explains how merchandizers can manually create and manage product recommendations lists for Microsoft Dynamics 365 Commerce customers.</span></span>

<span data-ttu-id="8d920-105">Проверенные списки представляют собой наборы отдельных материалов, созданных и проверенных людьми.</span><span class="sxs-lookup"><span data-stu-id="8d920-105">Curated lists are collections of individual content, created and curated by people.</span></span>  

## <a name="create-a-new-list"></a><span data-ttu-id="8d920-106">Создание нового списка</span><span class="sxs-lookup"><span data-stu-id="8d920-106">Create a new list</span></span>

<span data-ttu-id="8d920-107">Для создания проверенного списка рекомендаций продуктов выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8d920-107">To create a curated product recommendation list, follow these steps.</span></span>

1. <span data-ttu-id="8d920-108">Выберите **Retail и Commerce &gt; Рекомендации продуктов &gt; Списки рекомендаций**.</span><span class="sxs-lookup"><span data-stu-id="8d920-108">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation lists**.</span></span>
1. <span data-ttu-id="8d920-109">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="8d920-109">Select **New**.</span></span>
1. <span data-ttu-id="8d920-110">В поле **Код списка** введите значение.</span><span class="sxs-lookup"><span data-stu-id="8d920-110">In the **List Id** field, enter a value.</span></span>
1. <span data-ttu-id="8d920-111">В поле **Имя списка** введите значение.</span><span class="sxs-lookup"><span data-stu-id="8d920-111">In the **List name** field, enter a value.</span></span>
    - <span data-ttu-id="8d920-112">**Имя списка** является названием списка, которое будет отображаться в разделе проверенных списков модуля **Семейство продуктов**.</span><span class="sxs-lookup"><span data-stu-id="8d920-112">The **List name** is the title of the list that will appear in the curated lists section of the **Product collection** module.</span></span>
1. <span data-ttu-id="8d920-113">Чтобы добавить продукты в список, выберите **Добавить продукты**.</span><span class="sxs-lookup"><span data-stu-id="8d920-113">To add products to the list, select **Add products**.</span></span>
1. <span data-ttu-id="8d920-114">Чтобы изменить порядок продуктов в списке, введите значение в столбец **Порядок просмотра**.</span><span class="sxs-lookup"><span data-stu-id="8d920-114">To change the order of the products in the list, enter a value in the **Display order** column.</span></span>
    - <span data-ttu-id="8d920-115">Если два продукта имеют одинаковое значение порядок отображения, то окончательный порядок этих двух результатов также будет зависит от серверной части.</span><span class="sxs-lookup"><span data-stu-id="8d920-115">If two products have the same display order value, then the final order of those two results may differ from the back office.</span></span>
1. <span data-ttu-id="8d920-116">Выберите **Сохранить**, чтобы сохранить список.</span><span class="sxs-lookup"><span data-stu-id="8d920-116">Select **Save** to save the list.</span></span>

## <a name="example-list"></a><span data-ttu-id="8d920-117">Пример списка</span><span class="sxs-lookup"><span data-stu-id="8d920-117">Example List</span></span>

![Пример проверенного списка в серверной части](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a><span data-ttu-id="8d920-119">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8d920-119">Additional resources</span></span>

[<span data-ttu-id="8d920-120">Обзор рекомендаций по продуктам</span><span class="sxs-lookup"><span data-stu-id="8d920-120">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="8d920-121">Включение Azure Data Lake Storage в среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8d920-121">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="8d920-122">Включить рекомендации по продуктам</span><span class="sxs-lookup"><span data-stu-id="8d920-122">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="8d920-123">Включение персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="8d920-123">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="8d920-124">Отказ от персонализированных рекомендаций</span><span class="sxs-lookup"><span data-stu-id="8d920-124">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="8d920-125">Добавление рекомендаций по продуктам в POS</span><span class="sxs-lookup"><span data-stu-id="8d920-125">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="8d920-126">Добавление рекомендаций на экран проводок</span><span class="sxs-lookup"><span data-stu-id="8d920-126">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="8d920-127">Корректировка результатов рекомендаций на основе искусственного интеллекта и машинного обучения</span><span class="sxs-lookup"><span data-stu-id="8d920-127">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="8d920-128">Создание рекомендаций с помощью демонстрационных данных</span><span class="sxs-lookup"><span data-stu-id="8d920-128">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="8d920-129">Вопросы и ответы по рекомендациям по продуктам</span><span class="sxs-lookup"><span data-stu-id="8d920-129">Product recommendations FAQ</span></span>](faq-recommendations.md)
