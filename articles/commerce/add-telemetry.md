---
title: Добавление кода скрипта на страницы сайта для поддержки телеметрии
description: В этом разделе описывается добавление клиентского кода скрипта на страницы сайта для поддержки сбора телеметрии на стороне клиента.
author: bicyclingfool
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fb1773ab10b23a586eb6a8286f145181818585b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797439"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="e2aed-103">Добавление кода скрипта на страницы сайта для поддержки телеметрии</span><span class="sxs-lookup"><span data-stu-id="e2aed-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e2aed-104">В этом разделе описывается добавление клиентского кода скрипта на страницы сайта для поддержки сбора телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="e2aed-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

<span data-ttu-id="e2aed-105">Веб-аналитика является важным средством, когда необходимо понять, как клиенты взаимодействуют с вашим сайтом, и принимать решения, которые помогут оптимизировать работу по максимальной конверсии.</span><span class="sxs-lookup"><span data-stu-id="e2aed-105">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="e2aed-106">Доступно множество пакетов веб-аналитики, которые помогут достичь этих целей, такие как Google Analytics, Click, Moz Analytics и KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="e2aed-106">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="e2aed-107">Для большинства пакетов веб-аналитики требуется добавить клиентский код сценария в элемент **\<head\>** кода HTML для всех страниц сайта.</span><span class="sxs-lookup"><span data-stu-id="e2aed-107">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="e2aed-108">Инструкции, приведенные в этом разделе, применимы также к другим пользовательским функциям на стороне клиента, которые Microsoft Dynamics 365 Commerce изначально не предлагает.</span><span class="sxs-lookup"><span data-stu-id="e2aed-108">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="e2aed-109">Создание повторно используемого фрагмента кода сценария</span><span class="sxs-lookup"><span data-stu-id="e2aed-109">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="e2aed-110">Фрагмент позволяет повторно использовать код встроенного или внешнего сценария на всех страницах сайта, независимо от используемого шаблона.</span><span class="sxs-lookup"><span data-stu-id="e2aed-110">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="e2aed-111">Создание повторно используемого фрагмента для кода встроенного сценария</span><span class="sxs-lookup"><span data-stu-id="e2aed-111">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="e2aed-112">Чтобы создать повторно используемый фрагмент для кода встроенного сценария в средстве построения сайтов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e2aed-112">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="e2aed-113">Перейдите к разделу **Фрагменты**, и затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-113">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="e2aed-114">В диалоговом окне **Создать фрагмент** выберите **Встроенный сценарий**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-114">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="e2aed-115">В области **Имя фрагмента** введите имя фрагмента, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-115">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="e2aed-116">Под созданным фрагментом выберите модуль **Встроенный сценарий по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-116">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="e2aed-117">На панели свойств в правой части в разделе **Встроенный сценарий** введите клиентский сценарий.</span><span class="sxs-lookup"><span data-stu-id="e2aed-117">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="e2aed-118">Затем настройте другие параметры нужным образом.</span><span class="sxs-lookup"><span data-stu-id="e2aed-118">Then configure other options as you require.</span></span>
1. <span data-ttu-id="e2aed-119">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-119">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="e2aed-120">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-120">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="e2aed-121">Создание повторно используемого фрагмента для кода внешнего сценария</span><span class="sxs-lookup"><span data-stu-id="e2aed-121">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="e2aed-122">Чтобы создать повторно используемый фрагмент для кода внешнего сценария в средстве построения сайтов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e2aed-122">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="e2aed-123">Перейдите к разделу **Фрагменты**, и затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-123">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="e2aed-124">В диалоговом окне **Создать фрагмент** выберите **Внешний сценарий**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-124">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="e2aed-125">В области **Имя фрагмента** введите имя фрагмента, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-125">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="e2aed-126">Под созданным фрагментом выберите модуль **Внешний сценарий по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-126">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="e2aed-127">На панели свойств в правой части в области **Источник сценария** добавьте внешний или относительный URL-адрес для источника внешнего сценария.</span><span class="sxs-lookup"><span data-stu-id="e2aed-127">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="e2aed-128">Затем настройте другие параметры нужным образом.</span><span class="sxs-lookup"><span data-stu-id="e2aed-128">Then configure other options as you require.</span></span>
1. <span data-ttu-id="e2aed-129">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="e2aed-130">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-130">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="e2aed-131">Если для сайта активирована политика безопасности содержимого (CSP), убедитесь, что все внешние URL-адреса добавлены в директиву CSP **script-src** в конструкторе сайтов Commerce.</span><span class="sxs-lookup"><span data-stu-id="e2aed-131">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="e2aed-132">Дополнительные сведения см. в разделе [Управление политикой безопасности содержимого (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="e2aed-132">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="e2aed-133">Добавление фрагмента, включающего код сценария, в шаблон</span><span class="sxs-lookup"><span data-stu-id="e2aed-133">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="e2aed-134">Чтобы добавить фрагмент, включающий код сценария, в шаблон в средстве построения сайтов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e2aed-134">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="e2aed-135">Перейдите к разделу **Шаблоны** и откройте шаблон для страниц, к которым необходимо добавить код сценария.</span><span class="sxs-lookup"><span data-stu-id="e2aed-135">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="e2aed-136">В левой области разверните иерархию шаблонов, чтобы отобразить слот **Заголовок HTML**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-136">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="e2aed-137">В ячейке **Заголовок HTML** выберите кнопку с многоточием (**...**), затем выберите **Добавить фрагмент**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-137">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="e2aed-138">Выберите фрагмент, который был создан для кода сценария.</span><span class="sxs-lookup"><span data-stu-id="e2aed-138">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="e2aed-139">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-139">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="e2aed-140">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-140">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="e2aed-141">Добавление внешнего сценария или встроенного сценария непосредственно в шаблон</span><span class="sxs-lookup"><span data-stu-id="e2aed-141">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="e2aed-142">Если необходимо вставить встроенный или внешний сценарий непосредственно в набор страниц, управляемых одним шаблоном, не требуется сначала создавать фрагмент.</span><span class="sxs-lookup"><span data-stu-id="e2aed-142">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="e2aed-143">Добавление встроенного сценария непосредственно в шаблон</span><span class="sxs-lookup"><span data-stu-id="e2aed-143">Add an inline script directly to a template</span></span>

<span data-ttu-id="e2aed-144">Чтобы добавить встроенный сценарий непосредственно в шаблон в средстве построения сайтов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e2aed-144">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="e2aed-145">Перейдите к разделу **Шаблоны** и откройте шаблон для страниц, к которым необходимо добавить код сценария.</span><span class="sxs-lookup"><span data-stu-id="e2aed-145">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="e2aed-146">В левой области разверните иерархию шаблонов, чтобы отобразить слот **Заголовок HTML**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-146">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="e2aed-147">В ячейке **Заголовок HTML** выберите кнопку с многоточием (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-147">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e2aed-148">В диалоговом окне **Добавить модуль** выберите **Встроенный сценарий**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-148">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="e2aed-149">На панели свойств в правой части в разделе **Встроенный сценарий** введите клиентский сценарий.</span><span class="sxs-lookup"><span data-stu-id="e2aed-149">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="e2aed-150">Затем настройте другие параметры нужным образом.</span><span class="sxs-lookup"><span data-stu-id="e2aed-150">Then configure other options as you require.</span></span>
1. <span data-ttu-id="e2aed-151">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-151">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="e2aed-152">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-152">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="e2aed-153">Добавление внешнего сценария непосредственно в шаблон</span><span class="sxs-lookup"><span data-stu-id="e2aed-153">Add an external script directly to a template</span></span>

<span data-ttu-id="e2aed-154">Чтобы добавить внешний сценарий непосредственно в шаблон в средстве построения сайтов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e2aed-154">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="e2aed-155">Перейдите к разделу **Шаблоны** и откройте шаблон для страниц, к которым необходимо добавить код сценария.</span><span class="sxs-lookup"><span data-stu-id="e2aed-155">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="e2aed-156">В левой области разверните иерархию шаблонов, чтобы отобразить слот **Заголовок HTML**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-156">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="e2aed-157">В ячейке **Заголовок HTML** выберите кнопку с многоточием (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-157">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e2aed-158">В диалоговом окне **Добавить модуль** выберите **Внешний сценарий**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-158">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="e2aed-159">На панели свойств в правой части в области **Источник сценария** добавьте внешний или относительный URL-адрес для источника внешнего сценария.</span><span class="sxs-lookup"><span data-stu-id="e2aed-159">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="e2aed-160">Затем настройте другие параметры нужным образом.</span><span class="sxs-lookup"><span data-stu-id="e2aed-160">Then configure other options as you require.</span></span>
1. <span data-ttu-id="e2aed-161">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-161">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="e2aed-162">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="e2aed-162">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e2aed-163">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e2aed-163">Additional resources</span></span>

[<span data-ttu-id="e2aed-164">Добавление логотипа</span><span class="sxs-lookup"><span data-stu-id="e2aed-164">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="e2aed-165">Выбор темы сайта</span><span class="sxs-lookup"><span data-stu-id="e2aed-165">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="e2aed-166">Работа с переопределением файлов CSS</span><span class="sxs-lookup"><span data-stu-id="e2aed-166">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="e2aed-167">Добавление значка сайта</span><span class="sxs-lookup"><span data-stu-id="e2aed-167">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="e2aed-168">Добавление приветственного сообщения</span><span class="sxs-lookup"><span data-stu-id="e2aed-168">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="e2aed-169">Добавление уведомления об авторском праве</span><span class="sxs-lookup"><span data-stu-id="e2aed-169">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="e2aed-170">Добавление языков на сайт</span><span class="sxs-lookup"><span data-stu-id="e2aed-170">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
