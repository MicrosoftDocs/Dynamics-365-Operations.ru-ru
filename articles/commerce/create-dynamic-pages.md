---
title: Создание динамических страниц электронной коммерции на основе параметров URL-адреса
description: В этом разделе описывается, как настроить страницу электронной коммерции Microsoft Dynamics 365 Commerce, которая может отображать динамическое содержимое на основе параметров URL-адреса.
author: StuHarg
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8d6b4756fc81dc99786da251d5d9a575a71ccc49
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208023"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a><span data-ttu-id="c6fb8-103">Создание динамических страниц электронной коммерции на основе параметров URL-адреса</span><span class="sxs-lookup"><span data-stu-id="c6fb8-103">Create dynamic e-commerce pages based on URL parameters</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="c6fb8-104">В этом разделе описывается, как настроить страницу электронной коммерции Microsoft Dynamics 365 Commerce, которая может отображать динамическое содержимое на основе параметров URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-104">This topic describes how to set up a Microsoft Dynamics 365 Commerce e-commerce page that can serve dynamic content, based on URL parameters.</span></span>

<span data-ttu-id="c6fb8-105">Страница электронной коммерции может быть настроена для обслуживания различного содержимого на основе сегмента в пути URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-105">An e-commerce page can be configured to serve different content, based on a segment in the URL path.</span></span> <span data-ttu-id="c6fb8-106">Таким образом, страница называется динамической страницей.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-106">Therefore, the page is known as a dynamic page.</span></span> <span data-ttu-id="c6fb8-107">Сегмент используется в качестве параметра для извлечения содержимого страницы.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-107">The segment is used as a parameter to retrieve the page content.</span></span> <span data-ttu-id="c6fb8-108">Например, страница, которая называется **blog\_viewer**, создается и связывается с URL-адресом `https://fabrikam.com/blog`.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-108">For example, a page that is named **blog\_viewer** is created and associated with the URL `https://fabrikam.com/blog`.</span></span> <span data-ttu-id="c6fb8-109">Затем эту страницу можно использовать для отображения различного содержимого на основе последнего сегмента URL-пути.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-109">This page can then be used to show different content, based on the last segment in the URL path.</span></span> <span data-ttu-id="c6fb8-110">Например, последним сегментом в URL-адресе `https://fabrikam.com/blog/article-1` является **article-1**.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-110">For example, the last segment in the URL `https://fabrikam.com/blog/article-1` is **article-1**.</span></span>

<span data-ttu-id="c6fb8-111">Отдельные пользовательские страницы, переопределяющие динамическую страницу, также могут быть связаны с сегментами в URL-пути.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-111">Separate custom pages that override the dynamic page can also be associated with segments in the URL path.</span></span> <span data-ttu-id="c6fb8-112">Например, страница, которая называется **blog\_summary**, создается и связывается с URL-адресом `https://fabrikam.com/blog/about-this-blog`.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-112">For example, a page that is named **blog\_summary** is created and associated with the URL `https://fabrikam.com/blog/about-this-blog`.</span></span> <span data-ttu-id="c6fb8-113">При запросе этого URL-адреса страница **blog\_summary**, связанная с параметром **/about-this-blog**, возвращается вместо страницы **blog\_viewer**.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-113">When this URL is requested, the **blog\_summary** page that is associated with the **/about-this-blog** parameter is returned instead of the **blog\_viewer** page.</span></span>

> [!NOTE]
> <span data-ttu-id="c6fb8-114">Функции размещения, извлечения и отображения содержимого динамической страницы реализуются с помощью настраиваемого модуля.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-114">The functionality for hosting, retrieving, and showing dynamic page content is implemented by using a custom module.</span></span> <span data-ttu-id="c6fb8-115">Дополнительные сведения см. в разделе [Расширяемость интернет-канала](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="c6fb8-115">For more information, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="set-up-a-dynamic-e-commerce-page"></a><span data-ttu-id="c6fb8-116">Настройка динамической страницы электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="c6fb8-116">Set up a dynamic e-commerce page</span></span>

<span data-ttu-id="c6fb8-117">Чтобы настроить динамическую страницу электронной коммерции, необходимо создать динамическую страницу, создать базовый URL-адрес и настроить маршрут к динамической странице.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-117">To set up a dynamic e-commerce page, you must create the dynamic page, create the base URL, and configure the route to the dynamic page.</span></span>

### <a name="create-the-page-that-will-serve-dynamic-content"></a><span data-ttu-id="c6fb8-118">Создание страницы, которая будет обслуживать динамическое содержимое</span><span class="sxs-lookup"><span data-stu-id="c6fb8-118">Create the page that will serve dynamic content</span></span>

<span data-ttu-id="c6fb8-119">Чтобы создать страницу, которая будет обслуживать динамическое содержимое, выполните шаги, описанные в разделе [Добавление новой страницы сайта](add-new-page.md).</span><span class="sxs-lookup"><span data-stu-id="c6fb8-119">To create a page that will serve dynamic content, follow the steps in [Add a new site page](add-new-page.md).</span></span> <span data-ttu-id="c6fb8-120">Для создаваемой страницы потребуется реализация модуля, который использует последний сегмент в пути URL-адреса для извлечения содержимого из внешнего источника данных.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-120">The page that you create will require implementation of a module that uses the last segment in the URL path to retrieve content from an external data source.</span></span> <span data-ttu-id="c6fb8-121">Дополнительные сведения о разработке настраиваемого модуля см. в разделе [Расширяемость интернет-канала](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="c6fb8-121">For more information about custom module development, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

### <a name="create-the-base-url-for-the-dynamic-page"></a><span data-ttu-id="c6fb8-122">Создание базового URL-адреса для динамической страницы</span><span class="sxs-lookup"><span data-stu-id="c6fb8-122">Create the base URL for the dynamic page</span></span>

<span data-ttu-id="c6fb8-123">Чтобы создать базовый URL-адрес для динамической страницы в конструкторе сайтов Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-123">To create the base URL for the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c6fb8-124">Перейдите к разделу **URL-адреса** и выберите **Создать \> Создать URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-124">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="c6fb8-125">В диалоговом окне **Создание нового URL-адреса** выберите **Внутренняя страница**.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-125">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="c6fb8-126">В поле **URL-путь** введите путь, который будет служить корнем для динамической страницы (в данном примере — **/blog**).</span><span class="sxs-lookup"><span data-stu-id="c6fb8-126">Under **URL path**, enter the path that will serve as the root for the dynamic page (in this example, **/blog**).</span></span> <span data-ttu-id="c6fb8-127">Затем выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-127">Then select **Next**.</span></span>
1. <span data-ttu-id="c6fb8-128">В диалоговом окне **Выберите страницу** выберите страницу, созданную для работы в качестве динамической страницы, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-128">In the **Select a page** dialog box, select the page that you created to serve as the dynamic page, and then select **Save**.</span></span>
1. <span data-ttu-id="c6fb8-129">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-129">Select **Publish**.</span></span>

### <a name="configure-the-route-to-the-dynamic-page"></a><span data-ttu-id="c6fb8-130">Настройка маршрута к динамической странице</span><span class="sxs-lookup"><span data-stu-id="c6fb8-130">Configure the route to the dynamic page</span></span>

<span data-ttu-id="c6fb8-131">Чтобы настроить маршрут к динамической странице в конструкторе сайтов Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-131">To configure the route to the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c6fb8-132">Перейдите к разделу **Параметры сайта \> Расширения**.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-132">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="c6fb8-133">В области **Параметризованные URL-пути** выберите **Добавить**, затем введите URL-путь, введенный при создании URL-адреса (в данном примере **/blog**).</span><span class="sxs-lookup"><span data-stu-id="c6fb8-133">Under **Parameterized URL paths**, select **Add**, and then enter the URL path that you entered when you created the URL (in this example, **/blog**).</span></span>
1. <span data-ttu-id="c6fb8-134">Выберите **Сохранить и опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-134">Select **Save and publish**.</span></span>

<span data-ttu-id="c6fb8-135">После настройки маршрута все запросы к пути параметризованного URL-адреса будут возвращать страницу, связанную с этим URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-135">After the route is configured, all requests to the parameterized URL path will return the page that is associated with that URL.</span></span> <span data-ttu-id="c6fb8-136">Если какие-либо запросы содержат дополнительный сегмент, будет возвращена соответствующая страница, и содержимое страницы будет извлечено с помощью сегмента в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-136">If any requests contain an additional segment, the associated page will be returned, and the page content will be retrieved by using the segment as a parameter.</span></span> <span data-ttu-id="c6fb8-137">Например, `https://fabrikam.com/blog/article-1` возвращает страницу **blog\_summary**, и содержимое страницы будет извлечено с помощью параметра **/article-1**.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-137">For example, `https://fabrikam.com/blog/article-1` will return the **blog\_summary** page, and the page content will be retrieved by using the **/article-1** parameter.</span></span>

## <a name="override-a-parameterized-url-with-a-custom-page"></a><span data-ttu-id="c6fb8-138">Переопределение параметризованного URL-адреса с помощью настраиваемой страницы</span><span class="sxs-lookup"><span data-stu-id="c6fb8-138">Override a parameterized URL with a custom page</span></span>

<span data-ttu-id="c6fb8-139">Чтобы переопределить параметризованный URL-адрес с помощью пользовательской страницы в конструкторе сайтов Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-139">To override a parameterized URL with a custom page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c6fb8-140">Перейдите к разделу **URL-адреса** и выберите **Создать \> Создать URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-140">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="c6fb8-141">В диалоговом окне **Создание нового URL-адреса** выберите **Внутренняя страница**.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-141">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="c6fb8-142">В поле **URL-путь** введите путь, который включает сегмент для переопределения (в данном примере — **/blog/about-this-blog**).</span><span class="sxs-lookup"><span data-stu-id="c6fb8-142">Under **URL path**, enter the path that includes the segment to override (in this example, **/blog/about-this-blog**).</span></span> <span data-ttu-id="c6fb8-143">Затем выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-143">Then select **Next**.</span></span>
1. <span data-ttu-id="c6fb8-144">В диалоговом окне **Выбор страницы** выберите настраиваемую страницу, а затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-144">In the **Select a page** dialog box, select the custom page, and then select **Save**.</span></span>
1. <span data-ttu-id="c6fb8-145">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-145">Select **Publish**.</span></span>
1. <span data-ttu-id="c6fb8-146">Если настраиваемая страница еще не была опубликована, перейдите в раздел **Страницы**, выберите настраиваемую страницу и затем выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-146">If the custom page hasn't yet been published, go to **Pages**, select the custom page, and then select **Publish**.</span></span>

<span data-ttu-id="c6fb8-147">После публикации пользовательской страницы она будет работать вместо динамической страницы, которая имеет параметризованное содержимое.</span><span class="sxs-lookup"><span data-stu-id="c6fb8-147">After the custom page is published, it will be served instead of the dynamic page that has parameterized content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6fb8-148">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c6fb8-148">Additional resources</span></span>

[<span data-ttu-id="c6fb8-149">Изменение существующей страницы сайта</span><span class="sxs-lookup"><span data-stu-id="c6fb8-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="c6fb8-150">Добавление новой страницы сайта</span><span class="sxs-lookup"><span data-stu-id="c6fb8-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="c6fb8-151">Выбор макета страницы</span><span class="sxs-lookup"><span data-stu-id="c6fb8-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="c6fb8-152">Управление метаданными SEO</span><span class="sxs-lookup"><span data-stu-id="c6fb8-152">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="c6fb8-153">Сохранение, предварительный просмотр и публикация страницы</span><span class="sxs-lookup"><span data-stu-id="c6fb8-153">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="c6fb8-154">Расширение возможностей страницы продукта</span><span class="sxs-lookup"><span data-stu-id="c6fb8-154">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="c6fb8-155">Расширение возможностей целевой страницы категории</span><span class="sxs-lookup"><span data-stu-id="c6fb8-155">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="c6fb8-156">Проверка доступности контента страницы</span><span class="sxs-lookup"><span data-stu-id="c6fb8-156">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="c6fb8-157">Расширяемость канала продаж через Интернет</span><span class="sxs-lookup"><span data-stu-id="c6fb8-157">Online channel extensibility</span></span>](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]