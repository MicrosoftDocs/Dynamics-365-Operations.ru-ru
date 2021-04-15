---
title: Добавление страницы политики конфиденциальности
description: В этом разделе описывается, как добавить страницу политики конфиденциальности для своего сайта в Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12cd0358279684ce1d3050348c37209ba3d29140
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797535"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="12e80-103">Добавление страницы политики конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="12e80-103">Add a privacy policy page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="12e80-104">В этом разделе описывается, как добавить страницу политики конфиденциальности для своего сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="12e80-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="12e80-105">Соответствие конфиденциальности включает организационные меры, которые информируют пользователей сайтов о том, как их данные собираются и обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="12e80-105">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="12e80-106">Пользователи могут решить, как они хотят, чтобы их личные данные будут обрабатываться, и могут принять соответствующие меры.</span><span class="sxs-lookup"><span data-stu-id="12e80-106">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="12e80-107">См. заявление о конфиденциальности Майкрософт в Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="12e80-107">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="12e80-108">Чтобы просмотреть заявление о конфиденциальности Майкрософт после входа в инструменты разработки Dynamics 365 Commerce, выберите кнопку **Справка** (**?**) в правом верхнем углу, а затем выберите **Конфиденциальность и файлы cookie**.</span><span class="sxs-lookup"><span data-stu-id="12e80-108">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="12e80-109">Открывается новая вкладка с ссылкой на [Заявление о конфиденциальности Майкрософт](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="12e80-109">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="12e80-110">Создание страницы политики конфиденциальности для вашего сайта</span><span class="sxs-lookup"><span data-stu-id="12e80-110">Build a privacy policy page for your site</span></span>

<span data-ttu-id="12e80-111">В Dynamics 365 Commerce есть несколько способов, чтобы дать пользователям вашего сайта доступ к вашей политике конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="12e80-111">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="12e80-112">В этом разделе показано, как создать страницу политики конфиденциальности, а затем ссылку на страницу с помощью фрагмента колонтитула.</span><span class="sxs-lookup"><span data-stu-id="12e80-112">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="12e80-113">Ниже дан пример, который показывает, как создать общую страницу политики конфиденциальности для сайта Commerce.</span><span class="sxs-lookup"><span data-stu-id="12e80-113">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="12e80-114">Вы отвечаете за разработку и реализацию решения для страницы политики конфиденциальности, которое наилучшим образом отвечает юридическим требованиям вашей компании.</span><span class="sxs-lookup"><span data-stu-id="12e80-114">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="12e80-115">Для начала в средствах разработки перейдите на сайт, для которого вы хотите создать страницу политики конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="12e80-115">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="12e80-116">Создать шаблон</span><span class="sxs-lookup"><span data-stu-id="12e80-116">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="12e80-117">Если шаблон, который можно использовать для страницы политики конфиденциальности, уже создан, перейдите к разделу [Создание страницы политики конфиденциальности](#build-a-privacy-policy-page).</span><span class="sxs-lookup"><span data-stu-id="12e80-117">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="12e80-118">Чтобы создать шаблон, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="12e80-118">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="12e80-119">Перейдите к пункту **Шаблоны**, затем выберите **Создать**, чтобы создать шаблон страницы.</span><span class="sxs-lookup"><span data-stu-id="12e80-119">Go to **Templates**, and then select **New** to create a page template.</span></span>
1. <span data-ttu-id="12e80-120">В диалоговом окне **Создать шаблон** в разделе **Имя шаблона** введите **Шаблон рекламного баннера**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="12e80-120">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="12e80-121">В шаблоне добавьте все необходимые модули в требуемые слоты страниц.</span><span class="sxs-lookup"><span data-stu-id="12e80-121">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="12e80-122">В качестве примера наведите курсор на красные восклицательные знаки.</span><span class="sxs-lookup"><span data-stu-id="12e80-122">For guidance, hover over the red exclamation marks.</span></span> <span data-ttu-id="12e80-123">(Например, для слота **Заголовок HTML** может потребоваться модуль **Внешний сценарий по умолчанию**.)</span><span class="sxs-lookup"><span data-stu-id="12e80-123">(For example, the **HTML Head** slot might require a **Default External Script** module.)</span></span>
1. <span data-ttu-id="12e80-124">В слоте **Содержание** добавьте модуль **Страница по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="12e80-124">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="12e80-125">В модуле **Страница по умолчанию** в слоте **Главный** добавьте модуль **Блок насыщенного содержимого**.</span><span class="sxs-lookup"><span data-stu-id="12e80-125">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="12e80-126">В модуле **Блок насыщенного содержимого** добавьте **Элемент блока насыщенного содержимого**.</span><span class="sxs-lookup"><span data-stu-id="12e80-126">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="12e80-127">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="12e80-127">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="12e80-128">Создание страницы политики конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="12e80-128">Build a privacy policy page</span></span>

<span data-ttu-id="12e80-129">Чтобы создать страницу политики конфиденциальности, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="12e80-129">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="12e80-130">Перейдите к разделу **Страницы**, затем выберите **Создать**, чтобы создать страницу.</span><span class="sxs-lookup"><span data-stu-id="12e80-130">Go to **Pages**, and then select **New** to create a page.</span></span>
1. <span data-ttu-id="12e80-131">В диалоговом окне **Выбор шаблона** выберите шаблон для страницы политики конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="12e80-131">In the **Choose a template** dialog box, select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="12e80-132">Введите имя страницы и URL-адрес страницы, затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="12e80-132">Enter a page name and page URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="12e80-133">В слоте **Главный** новой страницы добавьте модуль **Блок насыщенного содержимого**.</span><span class="sxs-lookup"><span data-stu-id="12e80-133">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="12e80-134">В модуле **Блок насыщенного содержимого** добавьте **Элемент блока насыщенного содержимого**.</span><span class="sxs-lookup"><span data-stu-id="12e80-134">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="12e80-135">На панели свойств для модуля **Блок насыщенного содержимого** выберите **Добавить источник данных**, а затем выберите **Форматированный текст**.</span><span class="sxs-lookup"><span data-stu-id="12e80-135">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="12e80-136">В редакторе форматированного текста введите содержимое страницы политики конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="12e80-136">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="12e80-137">Разверните редактор форматированного на весь экран, как вам требуется.</span><span class="sxs-lookup"><span data-stu-id="12e80-137">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="12e80-138">Когда вы закончите ввод содержимого, выберите **Предварительный просмотр** для просмотра страницы в веб-браузере.</span><span class="sxs-lookup"><span data-stu-id="12e80-138">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="12e80-139">Внесите все оставшиеся дополнения в свойствах страницы и модуля.</span><span class="sxs-lookup"><span data-stu-id="12e80-139">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="12e80-140">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="12e80-140">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="12e80-141">Чтобы опубликовать URL-адрес и для страницы конфиденциальности и политики, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="12e80-141">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="12e80-142">Перейдите по **URL** и выберите URL-адрес для страницы политики конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="12e80-142">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="12e80-143">Выберите **Опубликовать**, чтобы опубликовать выбранный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="12e80-143">Select **Publish** to publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="12e80-144">Создание ссылки на страницу политики конфиденциальности в колонтитуле</span><span class="sxs-lookup"><span data-stu-id="12e80-144">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="12e80-145">Вы можете добавить ссылку на страницу политики конфиденциальности во фрагмент.</span><span class="sxs-lookup"><span data-stu-id="12e80-145">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="12e80-146">Таким образом, вы можете поделиться ссылкой и обновить ее на нескольких страницах сайта, ссылаясь на фрагмент.</span><span class="sxs-lookup"><span data-stu-id="12e80-146">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="12e80-147">В этом примере показано, как добавить ссылку на страницу политики конфиденциальности во фрагмент колонтитула.</span><span class="sxs-lookup"><span data-stu-id="12e80-147">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="12e80-148">Чтобы добавить ссылку на фрагмент колонтитула, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="12e80-148">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="12e80-149">Перейдите к разделу **Фрагменты**, затем выберите **Создать**, чтобы создать фрагмент страницы.</span><span class="sxs-lookup"><span data-stu-id="12e80-149">Go to **Fragments**, and then select **New** to create a page fragment.</span></span>
1. <span data-ttu-id="12e80-150">В диалоговом окне **Создать фрагмент** выберите модуль **Нижний колонтитул**.</span><span class="sxs-lookup"><span data-stu-id="12e80-150">In the **New fragment** dialog box, select the **Footer** module.</span></span>
1. <span data-ttu-id="12e80-151">В области **Имя фрагмента** введите имя фрагмента, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="12e80-151">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="12e80-152">В слоте **Категория нижнего колонтитула** добавьте модуль **Элемент нижнего колонтитула**.</span><span class="sxs-lookup"><span data-stu-id="12e80-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="12e80-153">В области свойств справа выберите **Текст ссылки**.</span><span class="sxs-lookup"><span data-stu-id="12e80-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="12e80-154">В диалоговом окне **Текст ссылки** введите текст ссылки и цель ссылки страницы политики конфиденциальности, и после этого щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="12e80-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>
1. <span data-ttu-id="12e80-155">Чтобы получить URL-адрес страницы политики конфиденциальности, перейдите **Страницы**, перейдите на страницу политики конфиденциальности и скопируйте URL-адрес из панели свойств.</span><span class="sxs-lookup"><span data-stu-id="12e80-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>
1. <span data-ttu-id="12e80-156">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата фрагмента, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="12e80-156">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="12e80-157">Просмотрите фрагмент и проверьте ссылку на страницу политики конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="12e80-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="12e80-158">Теперь на фрагмент можно ссылаться в шаблоне для других страниц сайта.</span><span class="sxs-lookup"><span data-stu-id="12e80-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="12e80-159">Когда на этот фрагмент есть ссылка в модуле **Нижний колонтитул** шаблона, ссылка появится на всех страницах, которые построены с помощью этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="12e80-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="12e80-160">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="12e80-160">Additional resources</span></span>

[<span data-ttu-id="12e80-161">Обзор соответствия</span><span class="sxs-lookup"><span data-stu-id="12e80-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="12e80-162">Специальные возможности</span><span class="sxs-lookup"><span data-stu-id="12e80-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="12e80-163">Соответствие файлов cookie</span><span class="sxs-lookup"><span data-stu-id="12e80-163">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="12e80-164">Замена идентификаторов пользователей, связанных с отслеживаемыми изменениями содержимого</span><span class="sxs-lookup"><span data-stu-id="12e80-164">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
