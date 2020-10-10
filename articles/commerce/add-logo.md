---
title: Добавление логотипа
description: В этом разделе описывается, как добавить логотип для своего сайта в Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 09/15/2020
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
ms.openlocfilehash: f15680deb0eab763ba68f2897139c915d1f8a6a3
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817338"
---
# <a name="add-a-logo"></a><span data-ttu-id="c015d-103">Добавление логотипа</span><span class="sxs-lookup"><span data-stu-id="c015d-103">Add a logo</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c015d-104">В этом разделе описывается, как добавить логотип для своего сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c015d-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c015d-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="c015d-105">Overview</span></span>

<span data-ttu-id="c015d-106">Когда вы создаете свой сайт, одна из первых вещей, которые вы, вероятно, хотите сделать, это добавить вашу компанию или логотип бренда в заголовок сайта.</span><span class="sxs-lookup"><span data-stu-id="c015d-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="c015d-107">Интернет-библиотека моделей Dynamics 365 Commerce содержит модуль, который делает эту задачу легкой.</span><span class="sxs-lookup"><span data-stu-id="c015d-107">The Dynamics 365 Commerce online module library provides a module that makes this task easy.</span></span>

<span data-ttu-id="c015d-108">Логотип можно добавить непосредственно в шаблон, макет или на страницу.</span><span class="sxs-lookup"><span data-stu-id="c015d-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="c015d-109">Таким образом, вы можете легко изменить логотип, который появляется на определенных страницах или группах страниц.</span><span class="sxs-lookup"><span data-stu-id="c015d-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="c015d-110">Тем не менее, эта тема охватывает наиболее частый сценарий, где вы добавляете свой логотип в фрагмент заголовка, который может быть повторно использован на всех страницах вашего сайта.</span><span class="sxs-lookup"><span data-stu-id="c015d-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c015d-111">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="c015d-111">Prerequisites</span></span>

<span data-ttu-id="c015d-112">Прежде чем вы сможете добавить логотип на все страницы вашего сайта, вы должны выполнить эти задачи.</span><span class="sxs-lookup"><span data-stu-id="c015d-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="c015d-113">Отправьте свой логотип в библиотеку мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c015d-113">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="c015d-114">Создайте фрагмент заголовка.</span><span class="sxs-lookup"><span data-stu-id="c015d-114">Create a header fragment.</span></span> <span data-ttu-id="c015d-115">Для получения дополнительной информации о том, как создавать и использовать фрагменты, см. [Работа с фрагментами](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="c015d-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="c015d-116">Включите фрагмент заголовка в шаблон, который страницы вашего сайта используют для параметров их макета и модуля.</span><span class="sxs-lookup"><span data-stu-id="c015d-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="c015d-117">Дополнительные сведения о шаблонах см. в разделе [Работа с шаблонами](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="c015d-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="c015d-118">Добавление логотипа во фрагмент заголовка</span><span class="sxs-lookup"><span data-stu-id="c015d-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="c015d-119">Чтобы добавить логотип во фрагмент заголовка для вашего сайта, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c015d-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="c015d-120">В области переходов слева выберите **Фрагменты**.</span><span class="sxs-lookup"><span data-stu-id="c015d-120">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="c015d-121">Выберите созданный ранее заголовок, затем выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="c015d-121">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="c015d-122">Разверните модуль заголовка.</span><span class="sxs-lookup"><span data-stu-id="c015d-122">Expand the header module.</span></span>
1. <span data-ttu-id="c015d-123">В области свойств модуля заголовка укажите изображение и ссылку на логотип.</span><span class="sxs-lookup"><span data-stu-id="c015d-123">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="c015d-124">Сохраните заголовок, завершите его редактирование и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="c015d-124">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="c015d-125">После публикации отправленного фрагмента заголовка все страницы сайта, на которых используется шаблон, содержащий фрагмент заголовка, будут отображать ваш логотип.</span><span class="sxs-lookup"><span data-stu-id="c015d-125">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c015d-126">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c015d-126">Additional resources</span></span>

[<span data-ttu-id="c015d-127">Выбор темы сайта</span><span class="sxs-lookup"><span data-stu-id="c015d-127">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="c015d-128">Работа с переопределением файлов CSS</span><span class="sxs-lookup"><span data-stu-id="c015d-128">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="c015d-129">Добавление значка сайта</span><span class="sxs-lookup"><span data-stu-id="c015d-129">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="c015d-130">Добавление приветственного сообщения</span><span class="sxs-lookup"><span data-stu-id="c015d-130">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="c015d-131">Добавление уведомления об авторском праве</span><span class="sxs-lookup"><span data-stu-id="c015d-131">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="c015d-132">Добавление языков на сайт</span><span class="sxs-lookup"><span data-stu-id="c015d-132">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="c015d-133">Добавление кода скрипта на страницы сайта для поддержки телеметрии</span><span class="sxs-lookup"><span data-stu-id="c015d-133">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

