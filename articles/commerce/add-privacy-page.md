---
title: Добавление страницы политики конфиденциальности
description: В этом разделе описывается, как добавить страницу политики конфиденциальности для своего сайта в Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ee9a68f46c91299065732e5f65479906f9e06079
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001331"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="4e5c4-103">Добавление страницы политики конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="4e5c4-103">Add a privacy policy page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4e5c4-104">В этом разделе описывается, как добавить страницу политики конфиденциальности для своего сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4e5c4-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="4e5c4-105">Overview</span></span>

<span data-ttu-id="4e5c4-106">Соответствие конфиденциальности включает организационные меры, которые информируют пользователей сайтов о том, как их данные собираются и обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-106">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="4e5c4-107">Пользователи могут решить, как они хотят, чтобы их личные данные будут обрабатываться, и могут принять соответствующие меры.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-107">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="4e5c4-108">См. заявление о конфиденциальности Майкрософт в Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="4e5c4-108">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="4e5c4-109">Чтобы просмотреть заявление о конфиденциальности Майкрософт после входа в инструменты разработки Dynamics 365 Commerce, выберите кнопку **Справка** (**?**) в правом верхнем углу, а затем выберите **Конфиденциальность и файлы cookie**.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-109">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="4e5c4-110">Открывается новая вкладка с ссылкой на [Заявление о конфиденциальности Майкрософт](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="4e5c4-110">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="4e5c4-111">Создание страницы политики конфиденциальности для вашего сайта</span><span class="sxs-lookup"><span data-stu-id="4e5c4-111">Build a privacy policy page for your site</span></span>

<span data-ttu-id="4e5c4-112">В Dynamics 365 Commerce есть несколько способов, чтобы дать пользователям вашего сайта доступ к вашей политике конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-112">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="4e5c4-113">В этом разделе показано, как создать страницу политики конфиденциальности, а затем ссылку на страницу с помощью фрагмента колонтитула.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-113">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="4e5c4-114">Ниже дан пример, который показывает, как создать общую страницу политики конфиденциальности для сайта Commerce.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-114">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="4e5c4-115">Вы отвечаете за разработку и реализацию решения для страницы политики конфиденциальности, которое наилучшим образом отвечает юридическим требованиям вашей компании.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-115">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="4e5c4-116">Для начала в средствах разработки перейдите на сайт, для которого вы хотите создать страницу политики конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-116">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="4e5c4-117">Создать шаблон</span><span class="sxs-lookup"><span data-stu-id="4e5c4-117">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="4e5c4-118">Если шаблон, который можно использовать для страницы политики конфиденциальности, уже создан, перейдите к разделу [Создание страницы политики конфиденциальности](#build-a-privacy-policy-page).</span><span class="sxs-lookup"><span data-stu-id="4e5c4-118">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="4e5c4-119">Чтобы создать шаблон, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-119">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="4e5c4-120">Перейдите в раздел **Шаблоны \> Создать шаблон**.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-120">Go to **Templates \> New Template**.</span></span>
1. <span data-ttu-id="4e5c4-121">Введите имя шаблона, а затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-121">Enter the template name, and then select **OK**.</span></span>
1. <span data-ttu-id="4e5c4-122">В шаблоне добавьте все необходимые модули в требуемые слоты страниц.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-122">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="4e5c4-123">В качестве примера наведите курсор на красные восклицательные знаки.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-123">For guidance, hover over the red exclamation marks.</span></span>

    <span data-ttu-id="4e5c4-124">Например, для слота **Заголовок HTML** может потребоваться модуль **Внешний сценарий по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-124">For example, the **HTML Head** slot might require a **Default External Script** module.</span></span>

1. <span data-ttu-id="4e5c4-125">В слоте **Содержание** добавьте модуль **Страница по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-125">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="4e5c4-126">В модуле **Страница по умолчанию** в слоте **Главный** добавьте модуль **Блок насыщенного содержимого**.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-126">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="4e5c4-127">В модуле **Блок насыщенного содержимого** добавьте **Элемент блока насыщенного содержимого**.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-127">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="4e5c4-128">Верните шаблон и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-128">Check the template in, and publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="4e5c4-129">Создание страницы политики конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="4e5c4-129">Build a privacy policy page</span></span>

<span data-ttu-id="4e5c4-130">Чтобы создать страницу политики конфиденциальности, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-130">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="4e5c4-131">Перейти в раздел **Страницы \> Создать страницу**.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-131">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="4e5c4-132">Выберите шаблон для страницы политики конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-132">Select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="4e5c4-133">Введите имя страницы и URL-адрес, а затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-133">Enter a page name and URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="4e5c4-134">В слоте **Главный** новой страницы добавьте модуль **Блок насыщенного содержимого**.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-134">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="4e5c4-135">В модуле **Блок насыщенного содержимого** добавьте **Элемент блока насыщенного содержимого**.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-135">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="4e5c4-136">На панели свойств для модуля **Блок насыщенного содержимого** выберите **Добавить источник данных**, а затем выберите **Форматированный текст**.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-136">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="4e5c4-137">В редакторе форматированного текста введите содержимое страницы политики конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-137">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="4e5c4-138">Разверните редактор форматированного на весь экран, как вам требуется.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-138">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="4e5c4-139">Когда вы закончите ввод содержимого, выберите **Предварительный просмотр** для просмотра страницы в веб-браузере.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-139">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="4e5c4-140">Внесите все оставшиеся дополнения в свойствах страницы и модуля.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-140">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="4e5c4-141">Верните страницу политики конфиденциальности и опубликуйте ее.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-141">Check the privacy policy page in, and publish it.</span></span>

<span data-ttu-id="4e5c4-142">Чтобы опубликовать URL-адрес и для страницы конфиденциальности и политики, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-142">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="4e5c4-143">Перейдите по **URL** и выберите URL-адрес для страницы политики конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-143">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="4e5c4-144">Опубликуйте выбранный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-144">Publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="4e5c4-145">Создание ссылки на страницу политики конфиденциальности в колонтитуле</span><span class="sxs-lookup"><span data-stu-id="4e5c4-145">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="4e5c4-146">Вы можете добавить ссылку на страницу политики конфиденциальности во фрагмент.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-146">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="4e5c4-147">Таким образом, вы можете поделиться ссылкой и обновить ее на нескольких страницах сайта, ссылаясь на фрагмент.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-147">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="4e5c4-148">В этом примере показано, как добавить ссылку на страницу политики конфиденциальности во фрагмент колонтитула.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-148">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="4e5c4-149">Чтобы добавить ссылку на фрагмент колонтитула, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-149">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="4e5c4-150">Перейдите к пункту **Фрагменты страницы \> Создать фрагмент страницы**.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-150">Go to **Page Fragments \> New Page Fragment**.</span></span>
1. <span data-ttu-id="4e5c4-151">Выберите модуль **Нижний колонтитул**, а затем введите имя в поле **Имя фрагмента страницы**.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-151">Select the **Footer** module, and then enter a name in the **Page Fragment Name** field.</span></span>
1. <span data-ttu-id="4e5c4-152">В слоте **Категория нижнего колонтитула** добавьте модуль **Элемент нижнего колонтитула**.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="4e5c4-153">В области свойств справа выберите **Текст ссылки**.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="4e5c4-154">В диалоговом окне **Текст ссылки** введите текст ссылки и цель ссылки страницы политики конфиденциальности, и после этого щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>

    <span data-ttu-id="4e5c4-155">Чтобы получить URL-адрес страницы политики конфиденциальности, перейдите **Страницы**, перейдите на страницу политики конфиденциальности и скопируйте URL-адрес из панели свойств.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>

1. <span data-ttu-id="4e5c4-156">Сохраните фрагмент, верните его и опубликуйте.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-156">Save the fragment, check it in, and publish it.</span></span>
1. <span data-ttu-id="4e5c4-157">Просмотрите фрагмент и проверьте ссылку на страницу политики конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="4e5c4-158">Теперь на фрагмент можно ссылаться в шаблоне для других страниц сайта.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="4e5c4-159">Когда на этот фрагмент есть ссылка в модуле **Нижний колонтитул** шаблона, ссылка появится на всех страницах, которые построены с помощью этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="4e5c4-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4e5c4-160">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4e5c4-160">Additional resources</span></span>

[<span data-ttu-id="4e5c4-161">Обзор соответствия</span><span class="sxs-lookup"><span data-stu-id="4e5c4-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="4e5c4-162">Специальные возможности и функции</span><span class="sxs-lookup"><span data-stu-id="4e5c4-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="4e5c4-163">Соответствие cookie</span><span class="sxs-lookup"><span data-stu-id="4e5c4-163">Cookie compliance</span></span>](cookie-compliance.md)
