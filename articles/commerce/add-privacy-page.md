---
title: Добавление страницы политики конфиденциальности
description: В этом разделе описывается, как добавить страницу политики конфиденциальности для своего сайта в Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: 2ee361c2e99b79e503e8d94c12602f9427f1ed5c
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686703"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="82665-103">Добавление страницы политики конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="82665-103">Add a privacy policy page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="82665-104">В этом разделе описывается, как добавить страницу политики конфиденциальности для своего сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="82665-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="82665-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="82665-105">Overview</span></span>

<span data-ttu-id="82665-106">Соответствие конфиденциальности включает организационные меры, которые информируют пользователей сайтов о том, как их данные собираются и обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="82665-106">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="82665-107">Пользователи могут решить, как они хотят, чтобы их личные данные будут обрабатываться, и могут принять соответствующие меры.</span><span class="sxs-lookup"><span data-stu-id="82665-107">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="82665-108">См. заявление о конфиденциальности Майкрософт в Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="82665-108">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="82665-109">Чтобы просмотреть заявление о конфиденциальности Майкрософт после входа в инструменты разработки Dynamics 365 Commerce, выберите кнопку **Справка** (**?**) в правом верхнем углу, а затем выберите **Конфиденциальность и файлы cookie**.</span><span class="sxs-lookup"><span data-stu-id="82665-109">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="82665-110">Открывается новая вкладка с ссылкой на [Заявление о конфиденциальности Майкрософт](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="82665-110">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="82665-111">Создание страницы политики конфиденциальности для вашего сайта</span><span class="sxs-lookup"><span data-stu-id="82665-111">Build a privacy policy page for your site</span></span>

<span data-ttu-id="82665-112">В Dynamics 365 Commerce есть несколько способов, чтобы дать пользователям вашего сайта доступ к вашей политике конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="82665-112">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="82665-113">В этом разделе показано, как создать страницу политики конфиденциальности, а затем ссылку на страницу с помощью фрагмента колонтитула.</span><span class="sxs-lookup"><span data-stu-id="82665-113">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="82665-114">Ниже дан пример, который показывает, как создать общую страницу политики конфиденциальности для сайта Commerce.</span><span class="sxs-lookup"><span data-stu-id="82665-114">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="82665-115">Вы отвечаете за разработку и реализацию решения для страницы политики конфиденциальности, которое наилучшим образом отвечает юридическим требованиям вашей компании.</span><span class="sxs-lookup"><span data-stu-id="82665-115">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="82665-116">Для начала в средствах разработки перейдите на сайт, для которого вы хотите создать страницу политики конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="82665-116">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="82665-117">Создать шаблон</span><span class="sxs-lookup"><span data-stu-id="82665-117">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="82665-118">Если шаблон, который можно использовать для страницы политики конфиденциальности, уже создан, перейдите к разделу [Создание страницы политики конфиденциальности](#build-a-privacy-policy-page).</span><span class="sxs-lookup"><span data-stu-id="82665-118">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="82665-119">Чтобы создать шаблон, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="82665-119">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="82665-120">Перейдите к пункту **Шаблоны**, затем выберите **Создать**, чтобы создать шаблон страницы.</span><span class="sxs-lookup"><span data-stu-id="82665-120">Go to **Templates**, and then select **New** to create a page template.</span></span>
1. <span data-ttu-id="82665-121">В диалоговом окне **Создать шаблон** в разделе **Имя шаблона** введите **Шаблон рекламного баннера**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="82665-121">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="82665-122">В шаблоне добавьте все необходимые модули в требуемые слоты страниц.</span><span class="sxs-lookup"><span data-stu-id="82665-122">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="82665-123">В качестве примера наведите курсор на красные восклицательные знаки.</span><span class="sxs-lookup"><span data-stu-id="82665-123">For guidance, hover over the red exclamation marks.</span></span> <span data-ttu-id="82665-124">(Например, для слота **Заголовок HTML** может потребоваться модуль **Внешний сценарий по умолчанию**.)</span><span class="sxs-lookup"><span data-stu-id="82665-124">(For example, the **HTML Head** slot might require a **Default External Script** module.)</span></span>
1. <span data-ttu-id="82665-125">В слоте **Содержание** добавьте модуль **Страница по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="82665-125">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="82665-126">В модуле **Страница по умолчанию** в слоте **Главный** добавьте модуль **Блок насыщенного содержимого**.</span><span class="sxs-lookup"><span data-stu-id="82665-126">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="82665-127">В модуле **Блок насыщенного содержимого** добавьте **Элемент блока насыщенного содержимого**.</span><span class="sxs-lookup"><span data-stu-id="82665-127">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="82665-128">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="82665-128">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="82665-129">Создание страницы политики конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="82665-129">Build a privacy policy page</span></span>

<span data-ttu-id="82665-130">Чтобы создать страницу политики конфиденциальности, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="82665-130">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="82665-131">Перейдите к разделу **Страницы**, затем выберите **Создать**, чтобы создать страницу.</span><span class="sxs-lookup"><span data-stu-id="82665-131">Go to **Pages**, and then select **New** to create a page.</span></span>
1. <span data-ttu-id="82665-132">В диалоговом окне **Выбор шаблона** выберите шаблон для страницы политики конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="82665-132">In the **Choose a template** dialog box, select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="82665-133">Введите имя страницы и URL-адрес страницы, затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="82665-133">Enter a page name and page URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="82665-134">В слоте **Главный** новой страницы добавьте модуль **Блок насыщенного содержимого**.</span><span class="sxs-lookup"><span data-stu-id="82665-134">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="82665-135">В модуле **Блок насыщенного содержимого** добавьте **Элемент блока насыщенного содержимого**.</span><span class="sxs-lookup"><span data-stu-id="82665-135">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="82665-136">На панели свойств для модуля **Блок насыщенного содержимого** выберите **Добавить источник данных**, а затем выберите **Форматированный текст**.</span><span class="sxs-lookup"><span data-stu-id="82665-136">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="82665-137">В редакторе форматированного текста введите содержимое страницы политики конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="82665-137">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="82665-138">Разверните редактор форматированного на весь экран, как вам требуется.</span><span class="sxs-lookup"><span data-stu-id="82665-138">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="82665-139">Когда вы закончите ввод содержимого, выберите **Предварительный просмотр** для просмотра страницы в веб-браузере.</span><span class="sxs-lookup"><span data-stu-id="82665-139">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="82665-140">Внесите все оставшиеся дополнения в свойствах страницы и модуля.</span><span class="sxs-lookup"><span data-stu-id="82665-140">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="82665-141">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="82665-141">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="82665-142">Чтобы опубликовать URL-адрес и для страницы конфиденциальности и политики, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="82665-142">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="82665-143">Перейдите по **URL** и выберите URL-адрес для страницы политики конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="82665-143">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="82665-144">Выберите **Опубликовать**, чтобы опубликовать выбранный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="82665-144">Select **Publish** to publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="82665-145">Создание ссылки на страницу политики конфиденциальности в колонтитуле</span><span class="sxs-lookup"><span data-stu-id="82665-145">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="82665-146">Вы можете добавить ссылку на страницу политики конфиденциальности во фрагмент.</span><span class="sxs-lookup"><span data-stu-id="82665-146">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="82665-147">Таким образом, вы можете поделиться ссылкой и обновить ее на нескольких страницах сайта, ссылаясь на фрагмент.</span><span class="sxs-lookup"><span data-stu-id="82665-147">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="82665-148">В этом примере показано, как добавить ссылку на страницу политики конфиденциальности во фрагмент колонтитула.</span><span class="sxs-lookup"><span data-stu-id="82665-148">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="82665-149">Чтобы добавить ссылку на фрагмент колонтитула, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="82665-149">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="82665-150">Перейдите к разделу **Фрагменты**, затем выберите **Создать**, чтобы создать фрагмент страницы.</span><span class="sxs-lookup"><span data-stu-id="82665-150">Go to **Fragments**, and then select **New** to create a page fragment.</span></span>
1. <span data-ttu-id="82665-151">В диалоговом окне **Создать фрагмент страницы** выберите модуль **Нижний колонтитул**.</span><span class="sxs-lookup"><span data-stu-id="82665-151">In the **New page fragment** dialog box, select the **Footer** module.</span></span>
1. <span data-ttu-id="82665-152">В области **Имя фрагмента страницы** введите имя фрагмента, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="82665-152">Under **Page fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="82665-153">В слоте **Категория нижнего колонтитула** добавьте модуль **Элемент нижнего колонтитула**.</span><span class="sxs-lookup"><span data-stu-id="82665-153">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="82665-154">В области свойств справа выберите **Текст ссылки**.</span><span class="sxs-lookup"><span data-stu-id="82665-154">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="82665-155">В диалоговом окне **Текст ссылки** введите текст ссылки и цель ссылки страницы политики конфиденциальности, и после этого щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="82665-155">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>
1. <span data-ttu-id="82665-156">Чтобы получить URL-адрес страницы политики конфиденциальности, перейдите **Страницы**, перейдите на страницу политики конфиденциальности и скопируйте URL-адрес из панели свойств.</span><span class="sxs-lookup"><span data-stu-id="82665-156">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>
1. <span data-ttu-id="82665-157">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата фрагмента, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="82665-157">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="82665-158">Просмотрите фрагмент и проверьте ссылку на страницу политики конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="82665-158">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="82665-159">Теперь на фрагмент можно ссылаться в шаблоне для других страниц сайта.</span><span class="sxs-lookup"><span data-stu-id="82665-159">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="82665-160">Когда на этот фрагмент есть ссылка в модуле **Нижний колонтитул** шаблона, ссылка появится на всех страницах, которые построены с помощью этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="82665-160">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="82665-161">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="82665-161">Additional resources</span></span>

[<span data-ttu-id="82665-162">Обзор соответствия</span><span class="sxs-lookup"><span data-stu-id="82665-162">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="82665-163">Специальные возможности</span><span class="sxs-lookup"><span data-stu-id="82665-163">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="82665-164">Соответствие файлов cookie</span><span class="sxs-lookup"><span data-stu-id="82665-164">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="82665-165">Замена идентификаторов пользователей, связанных с отслеживаемыми изменениями содержимого</span><span class="sxs-lookup"><span data-stu-id="82665-165">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)
