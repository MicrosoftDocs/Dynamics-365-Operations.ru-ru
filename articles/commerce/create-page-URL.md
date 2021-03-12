---
title: Создание URL-адреса страницы
description: В этом разделе рассматриваются основные принципы и процедуры создания URL-адресов страниц на сайте.
author: bicyclingfool
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 062a49df93e442dbe402ac9a78244c966958aaa2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965261"
---
# <a name="create-a-page-url"></a><span data-ttu-id="5f0ef-103">Создание URL-адреса страницы</span><span class="sxs-lookup"><span data-stu-id="5f0ef-103">Create a page URL</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5f0ef-104">В этом разделе рассматриваются основные принципы и процедуры создания URL-адресов страниц на сайте.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-104">This topic covers the basic concepts and procedures for creating a page URL on your site.</span></span>

## <a name="overview"></a><span data-ttu-id="5f0ef-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="5f0ef-105">Overview</span></span>

<span data-ttu-id="5f0ef-106">Полный, или абсолютный URL-адрес, который указывает на страницу сайта, состоит из различных частей.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-106">The full, or absolute, URL that points to a page on your site consists of distinct parts.</span></span> <span data-ttu-id="5f0ef-107">Например, URL-адрес `https://www.contoso.com/en-us/contactus` состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="5f0ef-107">For example, the URL `https://www.contoso.com/en-us/contactus` has the following parts:</span></span>

- <span data-ttu-id="5f0ef-108">`https://www.contoso.com`— протокол HTTP и домен сайта.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-108">`https://www.contoso.com` – The HTTP protocol and the site's domain.</span></span>
- <span data-ttu-id="5f0ef-109">`/en-us` — путь к языку сайта.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-109">`/en-us` – The site's language path.</span></span>
- <span data-ttu-id="5f0ef-110">`/contactus` — относительный URL-адрес страницы **Свяжитесь с нами**.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-110">`/contactus` – The relative URL for the **Contact Us** page.</span></span> <span data-ttu-id="5f0ef-111">Относительный URL-адрес также известен как *динамический* URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-111">A relative URL is also known as a URL *slug*.</span></span>

<span data-ttu-id="5f0ef-112">При настройке сайта необходимо задать домен сайта и необязательный путь к языку.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-112">You establish your site's domain and optional language path when you set up the site.</span></span> <span data-ttu-id="5f0ef-113">На сайте можно добавить дополнительные имена доменов и языки с помощью страницы интернет-магазина в настройках сайта.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-113">You can add more domains and language paths to your site through the online stores page in the site's settings.</span></span>

<span data-ttu-id="5f0ef-114">Динамический URL-адрес страницы существует как отдельная сущность в среде разработки сайта.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-114">The URL slug for a page exists as a standalone entity in the site authoring environment.</span></span> <span data-ttu-id="5f0ef-115">URL-адрес страницы состоит из двух частей: имени, которое представляет собой динамический URL-адрес, и указателя на страницу на вашем сайте или на внешнем сайте.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-115">A page URL consists of two parts: a name that represents the URL slug, and a pointer to a page on either your site or an external site.</span></span> <span data-ttu-id="5f0ef-116">URL-адрес страницы также можно настроить так, чтобы он мог выступать в качестве перенаправления на другую страницу на вашем сайте или на внешнем сайте.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-116">A page URL can also be configured to act as a redirect to another page on either your site or an external site.</span></span>

## <a name="create-a-page-url"></a><span data-ttu-id="5f0ef-117">Создание URL-адреса страницы</span><span class="sxs-lookup"><span data-stu-id="5f0ef-117">Create a page URL</span></span>

<span data-ttu-id="5f0ef-118">Существуют два способа создания URL-адресов страниц:</span><span class="sxs-lookup"><span data-stu-id="5f0ef-118">There are two ways to create page URLs:</span></span>

- <span data-ttu-id="5f0ef-119">Автоматически при создании страницы</span><span class="sxs-lookup"><span data-stu-id="5f0ef-119">Automatically, when you create a page</span></span>
- <span data-ttu-id="5f0ef-120">Вручную, со страницы **URL-адреса**</span><span class="sxs-lookup"><span data-stu-id="5f0ef-120">Manually, from the **URLs** page</span></span>

### <a name="create-a-page-url-when-you-create-a-page"></a><span data-ttu-id="5f0ef-121">Создание URL-адреса страницы при создании страницы</span><span class="sxs-lookup"><span data-stu-id="5f0ef-121">Create a page URL when you create a page</span></span>

<span data-ttu-id="5f0ef-122">Если при создании новой страницы ввести имя в поле **URL-адрес**, URL-адрес страницы, указывающий на эту страницу, автоматически создается на странице **URL-адреса**.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-122">If you provide a name in the **URL** field when you create a new page, a page URL that points to that page is automatically created on the **URLs** page.</span></span> <span data-ttu-id="5f0ef-123">После публикации URL-адреса и страницы, на которую он указывает, пользователи сайта (клиенты) смогут получить доступ к странице, связанной с этим URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-123">After you publish the URL and the page that it points to, site users (your customers) can access the page that is associated with the URL.</span></span>

> [!NOTE]
> <span data-ttu-id="5f0ef-124">При публикации URL-адреса без публикации страницы, на которую он указывает, при попытке доступа к странице пользователи сайта получат сообщение об ошибке 404.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-124">If you publish a URL without publishing the page that it points to, site users receive a 404 error when they try to access the page.</span></span> <span data-ttu-id="5f0ef-125">Если страница публикуется без публикации URL-адреса, указывающего на нее, доступ к странице с помощью URL-адреса невозможен.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-125">If you publish a page without publishing the URL that points to it, the page can't be accessed by using a URL.</span></span>

### <a name="manually-create-a-page-url"></a><span data-ttu-id="5f0ef-126">Создание URL-адреса страницы вручную</span><span class="sxs-lookup"><span data-stu-id="5f0ef-126">Manually create a page URL</span></span>

<span data-ttu-id="5f0ef-127">При создании новых страниц не требуется указывать URL-адрес страницы.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-127">When you create new pages, you aren't required to specify a page URL.</span></span> <span data-ttu-id="5f0ef-128">Если оставить поле URL-адреса пустым, страница будет создана без ссылки.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-128">If you leave the URL field blank, the page is created in an unlinked state.</span></span> <span data-ttu-id="5f0ef-129">В этом случае клиенты не смогут получить доступ к странице, даже если она опубликована.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-129">In this case, customers won't be able to access the page, even if it's published.</span></span> <span data-ttu-id="5f0ef-130">Чтобы сделать страницу доступной, необходимо вручную создать URL-адрес и связать его со страницей.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-130">To make the page accessible, you must manually create the URL and link it to the page.</span></span>

<span data-ttu-id="5f0ef-131">Чтобы вручную создать URL-адрес страницы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-131">To manually create the page URL for a page, follow these steps.</span></span>

1. <span data-ttu-id="5f0ef-132">На странице **URL-адреса** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-132">On the **URLs** page, select **New**.</span></span>
1. <span data-ttu-id="5f0ef-133">Выберите страницу сайта для связи с URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-133">Select the site page to associate with the URL.</span></span>
1. <span data-ttu-id="5f0ef-134">Введите динамический URL-адрес, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-134">Enter the URL slug, and then select **OK**.</span></span>

<span data-ttu-id="5f0ef-135">На этом этапе URL-адрес находится в состоянии черновика.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-135">At this point, the URL is in a draft state.</span></span> <span data-ttu-id="5f0ef-136">Он должен быть опубликована, прежде чем пользователи сайта смогут получить доступ к связанной странице.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-136">It must be published before site users can access the associated page.</span></span>

## <a name="update-a-page-url"></a><span data-ttu-id="5f0ef-137">Обновление URL-адреса страницы</span><span class="sxs-lookup"><span data-stu-id="5f0ef-137">Update a page URL</span></span>

<span data-ttu-id="5f0ef-138">Чтобы обновить целевую страницу URL-адреса страницы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-138">To update the target page of a page URL, follow these steps.</span></span>

1. <span data-ttu-id="5f0ef-139">На странице **URL-адреса** выберите URL-адрес для обновления.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-139">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="5f0ef-140">В правой панели свойств выберите кнопку с многоточием (**...**) рядом с полем целевой страницы.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-140">In the property pane on the right, select the ellipsis button (**...**) next to the target page field.</span></span>
1. <span data-ttu-id="5f0ef-141">В диалоговом окне выберите другую страницу, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-141">In the dialog box, select a different page, and then select **OK**.</span></span>
1. <span data-ttu-id="5f0ef-142">Сохраните и опубликуйте URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-142">Save and publish the URL.</span></span>

## <a name="redirect-a-page-url"></a><span data-ttu-id="5f0ef-143">Перенаправление URL-адреса страницы</span><span class="sxs-lookup"><span data-stu-id="5f0ef-143">Redirect a page URL</span></span>

<span data-ttu-id="5f0ef-144">Иногда вам необходимо, чтобы ваши клиенты видели другую страницу, когда они запрашивают определенный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-144">Sometimes, you might want your customers to view a different page when they request a specific URL.</span></span> <span data-ttu-id="5f0ef-145">В этих случаях часто лучший и самый простой подход заключается в том, чтобы изменить страницу, на которую указывает URL-адрес страницы.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-145">In these cases, the best and easiest approach is often to change the page that the page URL points to.</span></span> <span data-ttu-id="5f0ef-146">Однако могут быть законные причины для использования перенаправлений HTTP 301 или 3023 для перенаправления запросов URL-адреса на другой URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-146">However, you might have legitimate reasons for using HTTP 301 or 3023 redirects to redirect requests for a URL to a different URL.</span></span>

<span data-ttu-id="5f0ef-147">Чтобы переадресовать URL-адрес на другой URL-адрес, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-147">To redirect a URL to a different URL, follow these steps.</span></span>

1. <span data-ttu-id="5f0ef-148">На странице **URL-адреса** выберите URL-адрес для обновления.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-148">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="5f0ef-149">В области свойств справа выберите **Перенаправить**.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-149">In the property pane on the right, select **Redirect**.</span></span>
1. <span data-ttu-id="5f0ef-150">Выберите место назначения для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-150">Select a destination for the redirect:</span></span>

    - <span data-ttu-id="5f0ef-151">Чтобы указать на другую страницу сайта, выберите **Внутренний URL-адрес**, выберите кнопку с многоточием (**...**), затем выберите URL-адрес для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-151">To point to another page on your site, select **Internal URL**, select the ellipsis button (**...**), and then select the URL to redirect to.</span></span>
    - <span data-ttu-id="5f0ef-152">Чтобы указать на страницу на внешнем сайте, выберите **Внешний URL-адрес**, затем введите полный URL-адрес для этой страницы.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-152">To point to a page on an external site, select **External URL**, and then enter the full URL for that page.</span></span> <span data-ttu-id="5f0ef-153">Обязательно включите протокол.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-153">Be sure to include the protocol.</span></span> <span data-ttu-id="5f0ef-154">Например, введите `https://domain.com/new/page`.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-154">For example, enter `https://domain.com/new/page`.</span></span> <span data-ttu-id="5f0ef-155">Если URL-адрес уже перенаправляется на внутренний URL-адрес, необходимо выбрать **Очистить выбор**, прежде чем можно будет ввести внешний URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-155">If the URL already redirects to an internal URL, you must select **Clear selection** before you can enter an external URL.</span></span>

1. <span data-ttu-id="5f0ef-156">Выберите тип перенаправления:</span><span class="sxs-lookup"><span data-stu-id="5f0ef-156">Select a redirect type:</span></span>

    - <span data-ttu-id="5f0ef-157">**Постоянное перенаправление (301)** — выберите этот параметр, если вы знаете, что содержимое постоянно перемещается и не будет возвращено по предыдущему URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-157">**Permanent redirect (301)** – Select this option when you know that your content is moving permanently and won't revert to its previous URL.</span></span> <span data-ttu-id="5f0ef-158">Поисковые системы присвоят значение оптимизации поисковой системы (SEO) перенаправляющего URL-адреса URL-адресу, на который производится перенаправление, и обновят запись для отображения нового URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-158">Search engines will assign the search engine optimization (SEO) value of the redirecting URL to the URL that is being redirected to and update their record to show the new URL.</span></span> 
    - <span data-ttu-id="5f0ef-159">**Временное перенаправление ( 302)** — выберите этот параметр для перенаправления трафика без обновления поисковых систем.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-159">**Temporary redirect (302)** – Select this option to redirect traffic without updating search engines.</span></span> <span data-ttu-id="5f0ef-160">Этот подход обычно используется, если содержимое скоро вернется к предыдущему URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-160">This approach is typically used if the content will soon revert to its previous URL.</span></span>

1. <span data-ttu-id="5f0ef-161">Когда все готово к реализации перенаправления, сохраните и опубликуйте URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="5f0ef-161">When you're ready to implement the redirect, save and publish the URL.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5f0ef-162">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5f0ef-162">Additional resources</span></span>

[<span data-ttu-id="5f0ef-163">Настройка навигации по сайту</span><span class="sxs-lookup"><span data-stu-id="5f0ef-163">Customize site navigation</span></span>](customize-site-navigation.md)

[<span data-ttu-id="5f0ef-164">Добавление новой страницы сайта</span><span class="sxs-lookup"><span data-stu-id="5f0ef-164">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="5f0ef-165">Настройка доменного имени</span><span class="sxs-lookup"><span data-stu-id="5f0ef-165">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="5f0ef-166">Добавление языков на сайт</span><span class="sxs-lookup"><span data-stu-id="5f0ef-166">Add languages to your site</span></span>](add-languages-to-site.md)
