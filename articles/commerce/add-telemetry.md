---
title: Добавление кода скрипта на страницы сайта для поддержки телеметрии
description: В этом разделе описывается добавление клиентского кода скрипта на страницы сайта для поддержки сбора телеметрии на стороне клиента.
author: bicyclingfool
manager: annbe
ms.date: 03/20/2020
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4f26ed5b6674566f579e801f4b7be63c2d0dc38d
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686822"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="eb877-103">Добавление кода скрипта на страницы сайта для поддержки телеметрии</span><span class="sxs-lookup"><span data-stu-id="eb877-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="eb877-104">В этом разделе описывается добавление клиентского кода скрипта на страницы сайта для поддержки сбора телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="eb877-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="eb877-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="eb877-105">Overview</span></span>

<span data-ttu-id="eb877-106">Веб-аналитика является важным средством, когда необходимо понять, как клиенты взаимодействуют с вашим сайтом, и принимать решения, которые помогут оптимизировать работу по максимальной конверсии.</span><span class="sxs-lookup"><span data-stu-id="eb877-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="eb877-107">Доступно множество пакетов веб-аналитики, которые помогут достичь этих целей, такие как Google Analytics, Click, Moz Analytics и KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="eb877-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="eb877-108">Для большинства пакетов веб-аналитики требуется добавить клиентский код сценария в элемент **\<head\>** кода HTML для всех страниц сайта.</span><span class="sxs-lookup"><span data-stu-id="eb877-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="eb877-109">Инструкции, приведенные в этом разделе, применимы также к другим пользовательским функциям на стороне клиента, которые Microsoft Dynamics 365 Commerce изначально не предлагает.</span><span class="sxs-lookup"><span data-stu-id="eb877-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a><span data-ttu-id="eb877-110">Создание повторно используемого фрагмента страницы для кода сценария</span><span class="sxs-lookup"><span data-stu-id="eb877-110">Create a reusable page fragment for your script code</span></span>

<span data-ttu-id="eb877-111">Фрагмент страницы позволяет повторно использовать код встроенного или внешнего сценария на всех страницах сайта, независимо от используемого шаблона.</span><span class="sxs-lookup"><span data-stu-id="eb877-111">A page fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a><span data-ttu-id="eb877-112">Создание повторно используемого фрагмента страницы для кода встроенного сценария</span><span class="sxs-lookup"><span data-stu-id="eb877-112">Create a reusable page fragment for your inline script code</span></span>

<span data-ttu-id="eb877-113">Чтобы создать повторно используемый фрагмент страницы для кода встроенного сценария в средстве построения сайтов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="eb877-113">To create a reusable page fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="eb877-114">Перейдите к разделу **Фрагменты**, и затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="eb877-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="eb877-115">В диалоговом окне **Создать фрагмент страницы** выберите **Встроенный сценарий**.</span><span class="sxs-lookup"><span data-stu-id="eb877-115">In the **New page fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="eb877-116">В области **Имя фрагмента страницы** введите имя фрагмента, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="eb877-116">Under **Page fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="eb877-117">Под созданным фрагментом страницы выберите модуль **Встроенный сценарий по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="eb877-117">Under the page fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="eb877-118">На панели свойств в правой части в разделе **Встроенный сценарий** введите клиентский сценарий.</span><span class="sxs-lookup"><span data-stu-id="eb877-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="eb877-119">Затем настройте другие параметры нужным образом.</span><span class="sxs-lookup"><span data-stu-id="eb877-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="eb877-120">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="eb877-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="eb877-121">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="eb877-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a><span data-ttu-id="eb877-122">Создание повторно используемого фрагмента страницы для кода внешнего сценария</span><span class="sxs-lookup"><span data-stu-id="eb877-122">Create a reusable page fragment for your external script code</span></span>

<span data-ttu-id="eb877-123">Чтобы создать повторно используемый фрагмент страницы для кода внешнего сценария в средстве построения сайтов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="eb877-123">To create a reusable page fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="eb877-124">Перейдите к разделу **Фрагменты**, и затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="eb877-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="eb877-125">В диалоговом окне **Создать фрагмент страницы** выберите **Внешний сценарий**.</span><span class="sxs-lookup"><span data-stu-id="eb877-125">In the **New page fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="eb877-126">В области **Имя фрагмента страницы** введите имя фрагмента, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="eb877-126">Under **Page fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="eb877-127">Под созданным фрагментом страницы выберите модуль **Внешний сценарий по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="eb877-127">Under the page fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="eb877-128">На панели свойств в правой части в области **Источник сценария** добавьте внешний или относительный URL-адрес для источника внешнего сценария.</span><span class="sxs-lookup"><span data-stu-id="eb877-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="eb877-129">Затем настройте другие параметры нужным образом.</span><span class="sxs-lookup"><span data-stu-id="eb877-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="eb877-130">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="eb877-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="eb877-131">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="eb877-131">Select **Publish**.</span></span>

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="eb877-132">Добавление фрагмента страницы, включающего код сценария, в шаблон</span><span class="sxs-lookup"><span data-stu-id="eb877-132">Add a page fragment that includes script code to a template</span></span>

<span data-ttu-id="eb877-133">Чтобы добавить фрагмент страницы, включающий код сценария, в шаблон в средстве построения сайтов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="eb877-133">To add a page fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="eb877-134">Перейдите к разделу **Шаблоны** и откройте шаблон для страниц, к которым необходимо добавить код сценария.</span><span class="sxs-lookup"><span data-stu-id="eb877-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="eb877-135">В левой области разверните иерархию шаблонов, чтобы отобразить слот **Заголовок HTML**.</span><span class="sxs-lookup"><span data-stu-id="eb877-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="eb877-136">В ячейке **Заголовок HTML** выберите кнопку с многоточием (**...**), затем выберите **Добавить фрагмент страницы**.</span><span class="sxs-lookup"><span data-stu-id="eb877-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="eb877-137">Выберите фрагмент, который был создан для кода сценария.</span><span class="sxs-lookup"><span data-stu-id="eb877-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="eb877-138">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="eb877-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="eb877-139">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="eb877-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="eb877-140">Добавление внешнего сценария или встроенного сценария непосредственно в шаблон</span><span class="sxs-lookup"><span data-stu-id="eb877-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="eb877-141">Если необходимо вставить встроенный или внешний сценарий непосредственно в набор страниц, управляемых одним шаблоном, не требуется сначала создавать фрагмент страницы.</span><span class="sxs-lookup"><span data-stu-id="eb877-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a page fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="eb877-142">Добавление встроенного сценария непосредственно в шаблон</span><span class="sxs-lookup"><span data-stu-id="eb877-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="eb877-143">Чтобы добавить встроенный сценарий непосредственно в шаблон в средстве построения сайтов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="eb877-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="eb877-144">Перейдите к разделу **Шаблоны** и откройте шаблон для страниц, к которым необходимо добавить код сценария.</span><span class="sxs-lookup"><span data-stu-id="eb877-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="eb877-145">В левой области разверните иерархию шаблонов, чтобы отобразить слот **Заголовок HTML**.</span><span class="sxs-lookup"><span data-stu-id="eb877-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="eb877-146">В ячейке **Заголовок HTML** выберите кнопку с многоточием (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="eb877-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="eb877-147">В диалоговом окне **Добавить модуль** выберите **Встроенный сценарий**.</span><span class="sxs-lookup"><span data-stu-id="eb877-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="eb877-148">На панели свойств в правой части в разделе **Встроенный сценарий** введите клиентский сценарий.</span><span class="sxs-lookup"><span data-stu-id="eb877-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="eb877-149">Затем настройте другие параметры нужным образом.</span><span class="sxs-lookup"><span data-stu-id="eb877-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="eb877-150">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="eb877-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="eb877-151">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="eb877-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="eb877-152">Добавление внешнего сценария непосредственно в шаблон</span><span class="sxs-lookup"><span data-stu-id="eb877-152">Add an external script directly to a template</span></span>

<span data-ttu-id="eb877-153">Чтобы добавить внешний сценарий непосредственно в шаблон в средстве построения сайтов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="eb877-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="eb877-154">Перейдите к разделу **Шаблоны** и откройте шаблон для страниц, к которым необходимо добавить код сценария.</span><span class="sxs-lookup"><span data-stu-id="eb877-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="eb877-155">В левой области разверните иерархию шаблонов, чтобы отобразить слот **Заголовок HTML**.</span><span class="sxs-lookup"><span data-stu-id="eb877-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="eb877-156">В ячейке **Заголовок HTML** выберите кнопку с многоточием (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="eb877-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="eb877-157">В диалоговом окне **Добавить модуль** выберите **Внешний сценарий**.</span><span class="sxs-lookup"><span data-stu-id="eb877-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="eb877-158">На панели свойств в правой части в области **Источник сценария** добавьте внешний или относительный URL-адрес для источника внешнего сценария.</span><span class="sxs-lookup"><span data-stu-id="eb877-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="eb877-159">Затем настройте другие параметры нужным образом.</span><span class="sxs-lookup"><span data-stu-id="eb877-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="eb877-160">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="eb877-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="eb877-161">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="eb877-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eb877-162">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="eb877-162">Additional resources</span></span>

[<span data-ttu-id="eb877-163">Добавление логотипа</span><span class="sxs-lookup"><span data-stu-id="eb877-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="eb877-164">Выбор темы сайта</span><span class="sxs-lookup"><span data-stu-id="eb877-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="eb877-165">Работа с переопределением файлов CSS</span><span class="sxs-lookup"><span data-stu-id="eb877-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="eb877-166">Добавление значка сайта</span><span class="sxs-lookup"><span data-stu-id="eb877-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="eb877-167">Добавление приветственного сообщения</span><span class="sxs-lookup"><span data-stu-id="eb877-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="eb877-168">Добавление уведомления об авторском праве</span><span class="sxs-lookup"><span data-stu-id="eb877-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="eb877-169">Добавление языков на сайт</span><span class="sxs-lookup"><span data-stu-id="eb877-169">Add languages to your site</span></span>](add-languages-to-site.md)
