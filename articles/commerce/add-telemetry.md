---
title: Добавление кода скрипта на страницы сайта для поддержки телеметрии
description: В этом разделе описывается добавление клиентского кода скрипта на страницы сайта для поддержки сбора телеметрии на стороне клиента.
author: bicyclingfool
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: a88f4f920154aafaa15a48af67365152e21111f7
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761257"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="86d30-103">Добавление кода скрипта на страницы сайта для поддержки телеметрии</span><span class="sxs-lookup"><span data-stu-id="86d30-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="86d30-104">В этом разделе описывается добавление клиентского кода скрипта на страницы сайта для поддержки сбора телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="86d30-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="86d30-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="86d30-105">Overview</span></span>

<span data-ttu-id="86d30-106">Веб-аналитика является важным средством, когда необходимо понять, как клиенты взаимодействуют с вашим сайтом, и принимать решения, которые помогут оптимизировать работу по максимальной конверсии.</span><span class="sxs-lookup"><span data-stu-id="86d30-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="86d30-107">Доступно множество пакетов веб-аналитики, которые помогут достичь этих целей, такие как Google Analytics, Click, Moz Analytics и KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="86d30-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="86d30-108">Для большинства пакетов веб-аналитики требуется добавить клиентский код сценария в элемент **\<head\>** кода HTML для всех страниц сайта.</span><span class="sxs-lookup"><span data-stu-id="86d30-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="86d30-109">Инструкции, приведенные в этом разделе, применимы также к другим пользовательским функциям на стороне клиента, которые Microsoft Dynamics 365 Commerce изначально не предлагает.</span><span class="sxs-lookup"><span data-stu-id="86d30-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="86d30-110">Создание повторно используемого фрагмента кода сценария</span><span class="sxs-lookup"><span data-stu-id="86d30-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="86d30-111">Фрагмент позволяет повторно использовать код встроенного или внешнего сценария на всех страницах сайта, независимо от используемого шаблона.</span><span class="sxs-lookup"><span data-stu-id="86d30-111">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="86d30-112">Создание повторно используемого фрагмента для кода встроенного сценария</span><span class="sxs-lookup"><span data-stu-id="86d30-112">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="86d30-113">Чтобы создать повторно используемый фрагмент для кода встроенного сценария в средстве построения сайтов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="86d30-113">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="86d30-114">Перейдите к разделу **Фрагменты**, и затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="86d30-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="86d30-115">В диалоговом окне **Создать фрагмент** выберите **Встроенный сценарий**.</span><span class="sxs-lookup"><span data-stu-id="86d30-115">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="86d30-116">В области **Имя фрагмента** введите имя фрагмента, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="86d30-116">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="86d30-117">Под созданным фрагментом выберите модуль **Встроенный сценарий по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="86d30-117">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="86d30-118">На панели свойств в правой части в разделе **Встроенный сценарий** введите клиентский сценарий.</span><span class="sxs-lookup"><span data-stu-id="86d30-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="86d30-119">Затем настройте другие параметры нужным образом.</span><span class="sxs-lookup"><span data-stu-id="86d30-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="86d30-120">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="86d30-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="86d30-121">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="86d30-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="86d30-122">Создание повторно используемого фрагмента для кода внешнего сценария</span><span class="sxs-lookup"><span data-stu-id="86d30-122">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="86d30-123">Чтобы создать повторно используемый фрагмент для кода внешнего сценария в средстве построения сайтов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="86d30-123">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="86d30-124">Перейдите к разделу **Фрагменты**, и затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="86d30-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="86d30-125">В диалоговом окне **Создать фрагмент** выберите **Внешний сценарий**.</span><span class="sxs-lookup"><span data-stu-id="86d30-125">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="86d30-126">В области **Имя фрагмента** введите имя фрагмента, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="86d30-126">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="86d30-127">Под созданным фрагментом выберите модуль **Внешний сценарий по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="86d30-127">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="86d30-128">На панели свойств в правой части в области **Источник сценария** добавьте внешний или относительный URL-адрес для источника внешнего сценария.</span><span class="sxs-lookup"><span data-stu-id="86d30-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="86d30-129">Затем настройте другие параметры нужным образом.</span><span class="sxs-lookup"><span data-stu-id="86d30-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="86d30-130">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="86d30-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="86d30-131">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="86d30-131">Select **Publish**.</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="86d30-132">Добавление фрагмента, включающего код сценария, в шаблон</span><span class="sxs-lookup"><span data-stu-id="86d30-132">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="86d30-133">Чтобы добавить фрагмент, включающий код сценария, в шаблон в средстве построения сайтов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="86d30-133">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="86d30-134">Перейдите к разделу **Шаблоны** и откройте шаблон для страниц, к которым необходимо добавить код сценария.</span><span class="sxs-lookup"><span data-stu-id="86d30-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="86d30-135">В левой области разверните иерархию шаблонов, чтобы отобразить слот **Заголовок HTML**.</span><span class="sxs-lookup"><span data-stu-id="86d30-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="86d30-136">В ячейке **Заголовок HTML** выберите кнопку с многоточием (**...**), затем выберите **Добавить фрагмент**.</span><span class="sxs-lookup"><span data-stu-id="86d30-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="86d30-137">Выберите фрагмент, который был создан для кода сценария.</span><span class="sxs-lookup"><span data-stu-id="86d30-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="86d30-138">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="86d30-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="86d30-139">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="86d30-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="86d30-140">Добавление внешнего сценария или встроенного сценария непосредственно в шаблон</span><span class="sxs-lookup"><span data-stu-id="86d30-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="86d30-141">Если необходимо вставить встроенный или внешний сценарий непосредственно в набор страниц, управляемых одним шаблоном, не требуется сначала создавать фрагмент.</span><span class="sxs-lookup"><span data-stu-id="86d30-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="86d30-142">Добавление встроенного сценария непосредственно в шаблон</span><span class="sxs-lookup"><span data-stu-id="86d30-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="86d30-143">Чтобы добавить встроенный сценарий непосредственно в шаблон в средстве построения сайтов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="86d30-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="86d30-144">Перейдите к разделу **Шаблоны** и откройте шаблон для страниц, к которым необходимо добавить код сценария.</span><span class="sxs-lookup"><span data-stu-id="86d30-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="86d30-145">В левой области разверните иерархию шаблонов, чтобы отобразить слот **Заголовок HTML**.</span><span class="sxs-lookup"><span data-stu-id="86d30-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="86d30-146">В ячейке **Заголовок HTML** выберите кнопку с многоточием (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="86d30-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="86d30-147">В диалоговом окне **Добавить модуль** выберите **Встроенный сценарий**.</span><span class="sxs-lookup"><span data-stu-id="86d30-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="86d30-148">На панели свойств в правой части в разделе **Встроенный сценарий** введите клиентский сценарий.</span><span class="sxs-lookup"><span data-stu-id="86d30-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="86d30-149">Затем настройте другие параметры нужным образом.</span><span class="sxs-lookup"><span data-stu-id="86d30-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="86d30-150">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="86d30-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="86d30-151">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="86d30-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="86d30-152">Добавление внешнего сценария непосредственно в шаблон</span><span class="sxs-lookup"><span data-stu-id="86d30-152">Add an external script directly to a template</span></span>

<span data-ttu-id="86d30-153">Чтобы добавить внешний сценарий непосредственно в шаблон в средстве построения сайтов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="86d30-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="86d30-154">Перейдите к разделу **Шаблоны** и откройте шаблон для страниц, к которым необходимо добавить код сценария.</span><span class="sxs-lookup"><span data-stu-id="86d30-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="86d30-155">В левой области разверните иерархию шаблонов, чтобы отобразить слот **Заголовок HTML**.</span><span class="sxs-lookup"><span data-stu-id="86d30-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="86d30-156">В ячейке **Заголовок HTML** выберите кнопку с многоточием (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="86d30-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="86d30-157">В диалоговом окне **Добавить модуль** выберите **Внешний сценарий**.</span><span class="sxs-lookup"><span data-stu-id="86d30-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="86d30-158">На панели свойств в правой части в области **Источник сценария** добавьте внешний или относительный URL-адрес для источника внешнего сценария.</span><span class="sxs-lookup"><span data-stu-id="86d30-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="86d30-159">Затем настройте другие параметры нужным образом.</span><span class="sxs-lookup"><span data-stu-id="86d30-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="86d30-160">Выберите **Сохранить**, затем выберите **Завершить правку**.</span><span class="sxs-lookup"><span data-stu-id="86d30-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="86d30-161">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="86d30-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="86d30-162">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="86d30-162">Additional resources</span></span>

[<span data-ttu-id="86d30-163">Добавление логотипа</span><span class="sxs-lookup"><span data-stu-id="86d30-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="86d30-164">Выбор темы сайта</span><span class="sxs-lookup"><span data-stu-id="86d30-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="86d30-165">Работа с переопределением файлов CSS</span><span class="sxs-lookup"><span data-stu-id="86d30-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="86d30-166">Добавление значка сайта</span><span class="sxs-lookup"><span data-stu-id="86d30-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="86d30-167">Добавление приветственного сообщения</span><span class="sxs-lookup"><span data-stu-id="86d30-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="86d30-168">Добавление уведомления об авторском праве</span><span class="sxs-lookup"><span data-stu-id="86d30-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="86d30-169">Добавление языков на сайт</span><span class="sxs-lookup"><span data-stu-id="86d30-169">Add languages to your site</span></span>](add-languages-to-site.md)
