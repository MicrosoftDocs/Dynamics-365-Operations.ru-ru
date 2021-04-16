---
title: Расширение возможностей страницы продукта
description: В этом разделе описывается, как расширить возможности страницы продукта в Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6c1a9474ed514426386b1d7b4a72b62129cdb8a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799060"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="f2984-103">Расширение возможностей страницы продукта</span><span class="sxs-lookup"><span data-stu-id="f2984-103">Enrich a product page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f2984-104">В этом разделе описывается, как расширить возможности страницы продукта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f2984-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f2984-105">По умолчанию сайт использует универсальную страницу для отображения данных о продукте.</span><span class="sxs-lookup"><span data-stu-id="f2984-105">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="f2984-106">На этой странице содержатся основные сведения о продукте и об элементах управления, которые необходимы для продажи продукта.</span><span class="sxs-lookup"><span data-stu-id="f2984-106">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="f2984-107">Однако можно дополнить сведения, поступающие из Commerce Scale Unit, с дополнительными изображениями или текстом для конкретного продукта.</span><span class="sxs-lookup"><span data-stu-id="f2984-107">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="f2984-108">Этот процесс называется обогащением страницы продукта.</span><span class="sxs-lookup"><span data-stu-id="f2984-108">This process is known as enriching the product page.</span></span>

<span data-ttu-id="f2984-109">Во многих случаях потребуется использовать специфическое дополнительное содержимое для ваших продуктов.</span><span class="sxs-lookup"><span data-stu-id="f2984-109">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="f2984-110">При переходе в модуль **Retail и Commerce** в инструменте разработки будет отображен список продуктов из канала, назначенного сайту.</span><span class="sxs-lookup"><span data-stu-id="f2984-110">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="f2984-111">В этом списке столбец **Обогащенная** указывает, является ли страница продукта для продукта обогащенной.</span><span class="sxs-lookup"><span data-stu-id="f2984-111">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="f2984-112">Если в столбце имеется галочка, для продукта существует обогащенная страница продукта.</span><span class="sxs-lookup"><span data-stu-id="f2984-112">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="f2984-113">Если не отображается галочка, для продукта используются страница продукта и содержимое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f2984-113">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="f2984-114">Можно просмотреть как обогащенные, так и необогащенные страницы продукта, выбрав название продукта в списке.</span><span class="sxs-lookup"><span data-stu-id="f2984-114">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="f2984-115">Расширение возможностей страницы продукта</span><span class="sxs-lookup"><span data-stu-id="f2984-115">Enrich a product page</span></span>

<span data-ttu-id="f2984-116">Чтобы обогатить страницу продукта, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f2984-116">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="f2984-117">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="f2984-117">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="f2984-118">В области переходов слева выберите **Продукты**.</span><span class="sxs-lookup"><span data-stu-id="f2984-118">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="f2984-119">Выберите любой продукт, у которого нет обогащенной страницы продукта.</span><span class="sxs-lookup"><span data-stu-id="f2984-119">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="f2984-120">В области панели операций выберите **Обогатить страницу продукта**.</span><span class="sxs-lookup"><span data-stu-id="f2984-120">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="f2984-121">Выберите **Шаблон PDP**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f2984-121">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="f2984-122">В структуре дерева страниц слева разверните слот **Главный**.</span><span class="sxs-lookup"><span data-stu-id="f2984-122">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="f2984-123">Нажмите кнопку с многоточием (**...**) для слота **Главный**, затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="f2984-123">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="f2984-124">Выберите **Контейнер 2**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f2984-124">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="f2984-125">Нажмите кнопку с многоточием для модуля **Контейнер 2**, затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="f2984-125">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="f2984-126">Выберите **Компонент**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f2984-126">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="f2984-127">В области свойств справа в поле **Форматированный текст** введите обновленное описание продукта.</span><span class="sxs-lookup"><span data-stu-id="f2984-127">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="f2984-128">В поле **Заголовок** введите текст заголовка, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f2984-128">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="f2984-129">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="f2984-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="f2984-130">В поле **Комментарии** введите **Обогащен продукт**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f2984-130">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="f2984-131">Выберите **Предварительный просмотр**, чтобы просмотреть обогащенную страницу продукта.</span><span class="sxs-lookup"><span data-stu-id="f2984-131">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="f2984-132">По завершении закройте вкладку предварительного просмотра, чтобы вернуться к инструменту разработки.</span><span class="sxs-lookup"><span data-stu-id="f2984-132">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="f2984-133">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="f2984-133">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2984-134">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f2984-134">Additional resources</span></span>

[<span data-ttu-id="f2984-135">Изменение существующей страницы сайта</span><span class="sxs-lookup"><span data-stu-id="f2984-135">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="f2984-136">Добавление новой страницы сайта</span><span class="sxs-lookup"><span data-stu-id="f2984-136">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="f2984-137">Выбор макета страницы</span><span class="sxs-lookup"><span data-stu-id="f2984-137">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="f2984-138">Управление метаданными для поисковой оптимизации</span><span class="sxs-lookup"><span data-stu-id="f2984-138">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="f2984-139">Сохранение, предварительный просмотр и публикация страницы</span><span class="sxs-lookup"><span data-stu-id="f2984-139">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="f2984-140">Расширение возможностей целевой страницы категории</span><span class="sxs-lookup"><span data-stu-id="f2984-140">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="f2984-141">Проверка доступности контента страницы</span><span class="sxs-lookup"><span data-stu-id="f2984-141">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="f2984-142">Создание динамических страниц электронной коммерции на основе параметров URL-адреса</span><span class="sxs-lookup"><span data-stu-id="f2984-142">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
