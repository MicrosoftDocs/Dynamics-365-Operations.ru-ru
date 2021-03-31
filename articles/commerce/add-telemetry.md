---
title: Добавление кода скрипта на страницы сайта для поддержки телеметрии
description: В этом разделе описывается добавление клиентского кода скрипта на страницы сайта для поддержки сбора телеметрии на стороне клиента.
author: bicyclingfool
manager: annbe
ms.date: 09/29/2020
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
ms.openlocfilehash: e035c767474cba19c3a31eafdefb08b422b564ba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209211"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="683ce-103">Добавление кода скрипта на страницы сайта для поддержки телеметрии</span><span class="sxs-lookup"><span data-stu-id="683ce-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="683ce-104">В этом разделе описывается добавление клиентского кода скрипта на страницы сайта для поддержки сбора телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="683ce-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="683ce-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="683ce-105">Overview</span></span>

<span data-ttu-id="683ce-106">Веб-аналитика является важным средством, когда необходимо понять, как клиенты взаимодействуют с вашим сайтом, и принимать решения, которые помогут оптимизировать работу по максимальной конверсии.</span><span class="sxs-lookup"><span data-stu-id="683ce-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="683ce-107">Доступно множество пакетов веб-аналитики, которые помогут достичь этих целей, такие как Google Analytics, Click, Moz Analytics и KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="683ce-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="683ce-108">Для большинства пакетов веб-аналитики требуется добавить клиентский код сценария в элемент **\<head\>** кода HTML для всех страниц сайта.</span><span class="sxs-lookup"><span data-stu-id="683ce-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="683ce-109">Инструкции, приведенные в этом разделе, применимы также к другим пользовательским функциям на стороне клиента, которые Microsoft Dynamics 365 Commerce изначально не предлагает.</span><span class="sxs-lookup"><span data-stu-id="683ce-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="683ce-110">Создание повторно используемого фрагмента кода сценария</span><span class="sxs-lookup"><span data-stu-id="683ce-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="683ce-111">Фрагмент позволяет повторно использовать код встроенного или внешнего сценария на всех страницах сайта, независимо от используемого шаблона.</span><span class="sxs-lookup"><span data-stu-id="683ce-111">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="683ce-112">Создание повторно используемого фрагмента для кода встроенного сценария</span><span class="sxs-lookup"><span data-stu-id="683ce-112">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="683ce-113">Чтобы создать повторно используемый фрагмент для кода встроенного сценария в средстве построения сайтов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="683ce-113">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="683ce-114">Перейдите к разделу **Фрагменты**, и затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="683ce-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="683ce-115">В диалоговом окне **Создать фрагмент** выберите **Встроенный сценарий**.</span><span class="sxs-lookup"><span data-stu-id="683ce-115">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="683ce-116">В области **Имя фрагмента** введите имя фрагмента, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="683ce-116">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="683ce-117">Под созданным фрагментом выберите модуль **Встроенный сценарий по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="683ce-117">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="683ce-118">На панели свойств в правой части в разделе **Встроенный сценарий** введите клиентский сценарий.</span><span class="sxs-lookup"><span data-stu-id="683ce-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="683ce-119">Затем настройте другие параметры нужным образом.</span><span class="sxs-lookup"><span data-stu-id="683ce-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="683ce-120">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="683ce-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="683ce-121">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="683ce-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="683ce-122">Создание повторно используемого фрагмента для кода внешнего сценария</span><span class="sxs-lookup"><span data-stu-id="683ce-122">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="683ce-123">Чтобы создать повторно используемый фрагмент для кода внешнего сценария в средстве построения сайтов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="683ce-123">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="683ce-124">Перейдите к разделу **Фрагменты**, и затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="683ce-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="683ce-125">В диалоговом окне **Создать фрагмент** выберите **Внешний сценарий**.</span><span class="sxs-lookup"><span data-stu-id="683ce-125">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="683ce-126">В области **Имя фрагмента** введите имя фрагмента, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="683ce-126">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="683ce-127">Под созданным фрагментом выберите модуль **Внешний сценарий по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="683ce-127">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="683ce-128">На панели свойств в правой части в области **Источник сценария** добавьте внешний или относительный URL-адрес для источника внешнего сценария.</span><span class="sxs-lookup"><span data-stu-id="683ce-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="683ce-129">Затем настройте другие параметры нужным образом.</span><span class="sxs-lookup"><span data-stu-id="683ce-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="683ce-130">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="683ce-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="683ce-131">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="683ce-131">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="683ce-132">Если для сайта активирована политика безопасности содержимого (CSP), убедитесь, что все внешние URL-адреса добавлены в директиву CSP **script-src** в конструкторе сайтов Commerce.</span><span class="sxs-lookup"><span data-stu-id="683ce-132">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="683ce-133">Дополнительные сведения см. в разделе [Управление политикой безопасности содержимого (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="683ce-133">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="683ce-134">Добавление фрагмента, включающего код сценария, в шаблон</span><span class="sxs-lookup"><span data-stu-id="683ce-134">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="683ce-135">Чтобы добавить фрагмент, включающий код сценария, в шаблон в средстве построения сайтов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="683ce-135">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="683ce-136">Перейдите к разделу **Шаблоны** и откройте шаблон для страниц, к которым необходимо добавить код сценария.</span><span class="sxs-lookup"><span data-stu-id="683ce-136">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="683ce-137">В левой области разверните иерархию шаблонов, чтобы отобразить слот **Заголовок HTML**.</span><span class="sxs-lookup"><span data-stu-id="683ce-137">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="683ce-138">В ячейке **Заголовок HTML** выберите кнопку с многоточием (**...**), затем выберите **Добавить фрагмент**.</span><span class="sxs-lookup"><span data-stu-id="683ce-138">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="683ce-139">Выберите фрагмент, который был создан для кода сценария.</span><span class="sxs-lookup"><span data-stu-id="683ce-139">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="683ce-140">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="683ce-140">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="683ce-141">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="683ce-141">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="683ce-142">Добавление внешнего сценария или встроенного сценария непосредственно в шаблон</span><span class="sxs-lookup"><span data-stu-id="683ce-142">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="683ce-143">Если необходимо вставить встроенный или внешний сценарий непосредственно в набор страниц, управляемых одним шаблоном, не требуется сначала создавать фрагмент.</span><span class="sxs-lookup"><span data-stu-id="683ce-143">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="683ce-144">Добавление встроенного сценария непосредственно в шаблон</span><span class="sxs-lookup"><span data-stu-id="683ce-144">Add an inline script directly to a template</span></span>

<span data-ttu-id="683ce-145">Чтобы добавить встроенный сценарий непосредственно в шаблон в средстве построения сайтов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="683ce-145">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="683ce-146">Перейдите к разделу **Шаблоны** и откройте шаблон для страниц, к которым необходимо добавить код сценария.</span><span class="sxs-lookup"><span data-stu-id="683ce-146">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="683ce-147">В левой области разверните иерархию шаблонов, чтобы отобразить слот **Заголовок HTML**.</span><span class="sxs-lookup"><span data-stu-id="683ce-147">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="683ce-148">В ячейке **Заголовок HTML** выберите кнопку с многоточием (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="683ce-148">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="683ce-149">В диалоговом окне **Добавить модуль** выберите **Встроенный сценарий**.</span><span class="sxs-lookup"><span data-stu-id="683ce-149">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="683ce-150">На панели свойств в правой части в разделе **Встроенный сценарий** введите клиентский сценарий.</span><span class="sxs-lookup"><span data-stu-id="683ce-150">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="683ce-151">Затем настройте другие параметры нужным образом.</span><span class="sxs-lookup"><span data-stu-id="683ce-151">Then configure other options as you require.</span></span>
1. <span data-ttu-id="683ce-152">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="683ce-152">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="683ce-153">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="683ce-153">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="683ce-154">Добавление внешнего сценария непосредственно в шаблон</span><span class="sxs-lookup"><span data-stu-id="683ce-154">Add an external script directly to a template</span></span>

<span data-ttu-id="683ce-155">Чтобы добавить внешний сценарий непосредственно в шаблон в средстве построения сайтов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="683ce-155">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="683ce-156">Перейдите к разделу **Шаблоны** и откройте шаблон для страниц, к которым необходимо добавить код сценария.</span><span class="sxs-lookup"><span data-stu-id="683ce-156">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="683ce-157">В левой области разверните иерархию шаблонов, чтобы отобразить слот **Заголовок HTML**.</span><span class="sxs-lookup"><span data-stu-id="683ce-157">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="683ce-158">В ячейке **Заголовок HTML** выберите кнопку с многоточием (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="683ce-158">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="683ce-159">В диалоговом окне **Добавить модуль** выберите **Внешний сценарий**.</span><span class="sxs-lookup"><span data-stu-id="683ce-159">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="683ce-160">На панели свойств в правой части в области **Источник сценария** добавьте внешний или относительный URL-адрес для источника внешнего сценария.</span><span class="sxs-lookup"><span data-stu-id="683ce-160">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="683ce-161">Затем настройте другие параметры нужным образом.</span><span class="sxs-lookup"><span data-stu-id="683ce-161">Then configure other options as you require.</span></span>
1. <span data-ttu-id="683ce-162">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="683ce-162">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="683ce-163">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="683ce-163">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="683ce-164">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="683ce-164">Additional resources</span></span>

[<span data-ttu-id="683ce-165">Добавление логотипа</span><span class="sxs-lookup"><span data-stu-id="683ce-165">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="683ce-166">Выбор темы сайта</span><span class="sxs-lookup"><span data-stu-id="683ce-166">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="683ce-167">Работа с переопределением файлов CSS</span><span class="sxs-lookup"><span data-stu-id="683ce-167">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="683ce-168">Добавление значка сайта</span><span class="sxs-lookup"><span data-stu-id="683ce-168">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="683ce-169">Добавление приветственного сообщения</span><span class="sxs-lookup"><span data-stu-id="683ce-169">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="683ce-170">Добавление уведомления об авторском праве</span><span class="sxs-lookup"><span data-stu-id="683ce-170">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="683ce-171">Добавление языков на сайт</span><span class="sxs-lookup"><span data-stu-id="683ce-171">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]