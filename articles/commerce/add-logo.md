---
title: Добавление логотипа
description: В этом разделе описывается, как добавить логотип для своего сайта в Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914633"
---
# <a name="add-a-logo"></a><span data-ttu-id="f78e7-103">Добавление логотипа</span><span class="sxs-lookup"><span data-stu-id="f78e7-103">Add a logo</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f78e7-104">В этом разделе описывается, как добавить логотип для своего сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f78e7-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f78e7-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="f78e7-105">Overview</span></span>

<span data-ttu-id="f78e7-106">Когда вы создаете свой сайт, одна из первых вещей, которые вы, вероятно, хотите сделать, это добавить вашу компанию или логотип бренда в заголовок сайта.</span><span class="sxs-lookup"><span data-stu-id="f78e7-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="f78e7-107">Стартовый интернет-комплект Dynamics 365 Commerce содержит модуль, который делает эту задачу легкой.</span><span class="sxs-lookup"><span data-stu-id="f78e7-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="f78e7-108">Логотип можно добавить непосредственно в шаблон, макет или на страницу.</span><span class="sxs-lookup"><span data-stu-id="f78e7-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="f78e7-109">Таким образом, вы можете легко изменить логотип, который появляется на определенных страницах или группах страниц.</span><span class="sxs-lookup"><span data-stu-id="f78e7-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="f78e7-110">Тем не менее, эта тема охватывает наиболее частый сценарий, где вы добавляете свой логотип в фрагмент заголовка, который может быть повторно использован на всех страницах вашего сайта.</span><span class="sxs-lookup"><span data-stu-id="f78e7-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f78e7-111">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="f78e7-111">Prerequisites</span></span>

<span data-ttu-id="f78e7-112">Прежде чем вы сможете добавить логотип на все страницы вашего сайта, вы должны выполнить эти задачи.</span><span class="sxs-lookup"><span data-stu-id="f78e7-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="f78e7-113">Отправьте свой логотип в менеджер цифровых активов, к которому можно получить доступ на странице **Активы**.</span><span class="sxs-lookup"><span data-stu-id="f78e7-113">Upload your logo to the digital assets manager, which you can access from the **Assets** page.</span></span>
1. <span data-ttu-id="f78e7-114">Создайте фрагмент заголовка.</span><span class="sxs-lookup"><span data-stu-id="f78e7-114">Create a header fragment.</span></span> <span data-ttu-id="f78e7-115">Для получения дополнительной информации о том, как создавать и использовать фрагменты, см. [Работа с фрагментами](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="f78e7-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="f78e7-116">Включите фрагмент заголовка в шаблон, который страницы вашего сайта используют для параметров их макета и модуля.</span><span class="sxs-lookup"><span data-stu-id="f78e7-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="f78e7-117">Дополнительные сведения о шаблонах см. в разделе [Работа с шаблонами](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="f78e7-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="f78e7-118">Добавление логотипа во фрагмент заголовка</span><span class="sxs-lookup"><span data-stu-id="f78e7-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="f78e7-119">Чтобы добавить логотип во фрагмент заголовка для вашего сайта, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f78e7-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="f78e7-120">На панели навигации слева выберите **Фрагменты**, а затем выберите созданный фрагмент заголовка.</span><span class="sxs-lookup"><span data-stu-id="f78e7-120">In the navigation pane on the left, select **Fragments**, and then select the header fragment that you created.</span></span>
2. <span data-ttu-id="f78e7-121">Выберите **Извлечь**.</span><span class="sxs-lookup"><span data-stu-id="f78e7-121">Select **Check out**.</span></span>
3. <span data-ttu-id="f78e7-122">Разверните слот **Заголовок** и слот **Логотип**.</span><span class="sxs-lookup"><span data-stu-id="f78e7-122">Expand the **Header** slot and the **Logo** slot.</span></span>
4. <span data-ttu-id="f78e7-123">Нажмите кнопку с многоточием (**...**) для слота **Логотип**, затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="f78e7-123">Select the ellipsis button (**...**) for the **Logo** slot, and then select **Add module**.</span></span>
5. <span data-ttu-id="f78e7-124">Выберите модуль логотипа.</span><span class="sxs-lookup"><span data-stu-id="f78e7-124">Select the logo module.</span></span>
6. <span data-ttu-id="f78e7-125">В области свойств справа выполните настройку модуля логотипа, чтобы показывался ваш логотип.</span><span class="sxs-lookup"><span data-stu-id="f78e7-125">In the properties pane on the right, configure the logo module so that it shows your logo.</span></span>
7. <span data-ttu-id="f78e7-126">Сохраните фрагмент заголовка, верните его и опубликуйте.</span><span class="sxs-lookup"><span data-stu-id="f78e7-126">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="f78e7-127">После публикации отправленного фрагмента заголовка все страницы сайта, на которых используется шаблон, содержащий фрагмент заголовка, будут отображать ваш логотип.</span><span class="sxs-lookup"><span data-stu-id="f78e7-127">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f78e7-128">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f78e7-128">Additional resources</span></span>

[<span data-ttu-id="f78e7-129">Выбор темы сайта</span><span class="sxs-lookup"><span data-stu-id="f78e7-129">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="f78e7-130">Работа с переопределением файлов CSS</span><span class="sxs-lookup"><span data-stu-id="f78e7-130">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="f78e7-131">Добавление значка сайта</span><span class="sxs-lookup"><span data-stu-id="f78e7-131">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="f78e7-132">Добавление приветственного сообщения</span><span class="sxs-lookup"><span data-stu-id="f78e7-132">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="f78e7-133">Добавление уведомления об авторском праве</span><span class="sxs-lookup"><span data-stu-id="f78e7-133">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="f78e7-134">Добавление языков на сайт</span><span class="sxs-lookup"><span data-stu-id="f78e7-134">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="f78e7-135">Добавление кода скрипта на страницы сайта для поддержки телеметрии</span><span class="sxs-lookup"><span data-stu-id="f78e7-135">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

