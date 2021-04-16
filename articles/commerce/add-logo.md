---
title: Добавление логотипа
description: В этом разделе описывается, как добавить логотип для своего сайта в Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d9e1cba6bd07e0c3d9ed7d741d87e10837d8021c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797607"
---
# <a name="add-a-logo"></a><span data-ttu-id="d974d-103">Добавление логотипа</span><span class="sxs-lookup"><span data-stu-id="d974d-103">Add a logo</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d974d-104">В этом разделе описывается, как добавить логотип для своего сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d974d-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d974d-105">Когда вы создаете свой сайт, одна из первых вещей, которые вы, вероятно, хотите сделать, это добавить вашу компанию или логотип бренда в заголовок сайта.</span><span class="sxs-lookup"><span data-stu-id="d974d-105">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="d974d-106">Интернет-библиотека моделей Dynamics 365 Commerce содержит модуль, который делает эту задачу легкой.</span><span class="sxs-lookup"><span data-stu-id="d974d-106">The Dynamics 365 Commerce online module library provides a module that makes this task easy.</span></span>

<span data-ttu-id="d974d-107">Логотип можно добавить непосредственно в шаблон, макет или на страницу.</span><span class="sxs-lookup"><span data-stu-id="d974d-107">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="d974d-108">Таким образом, вы можете легко изменить логотип, который появляется на определенных страницах или группах страниц.</span><span class="sxs-lookup"><span data-stu-id="d974d-108">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="d974d-109">Тем не менее, эта тема охватывает наиболее частый сценарий, где вы добавляете свой логотип в фрагмент заголовка, который может быть повторно использован на всех страницах вашего сайта.</span><span class="sxs-lookup"><span data-stu-id="d974d-109">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d974d-110">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="d974d-110">Prerequisites</span></span>

<span data-ttu-id="d974d-111">Прежде чем вы сможете добавить логотип на все страницы вашего сайта, вы должны выполнить эти задачи.</span><span class="sxs-lookup"><span data-stu-id="d974d-111">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="d974d-112">Отправьте свой логотип в библиотеку мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d974d-112">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="d974d-113">Создайте фрагмент заголовка.</span><span class="sxs-lookup"><span data-stu-id="d974d-113">Create a header fragment.</span></span> <span data-ttu-id="d974d-114">Для получения дополнительной информации о том, как создавать и использовать фрагменты, см. [Работа с фрагментами](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="d974d-114">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="d974d-115">Включите фрагмент заголовка в шаблон, который страницы вашего сайта используют для параметров их макета и модуля.</span><span class="sxs-lookup"><span data-stu-id="d974d-115">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="d974d-116">Дополнительные сведения о шаблонах см. в разделе [Работа с шаблонами](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="d974d-116">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="d974d-117">Добавление логотипа во фрагмент заголовка</span><span class="sxs-lookup"><span data-stu-id="d974d-117">Add a logo to a header fragment</span></span>

<span data-ttu-id="d974d-118">Чтобы добавить логотип во фрагмент заголовка для вашего сайта, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d974d-118">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="d974d-119">В области переходов слева выберите **Фрагменты**.</span><span class="sxs-lookup"><span data-stu-id="d974d-119">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="d974d-120">Выберите созданный ранее заголовок, затем выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="d974d-120">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="d974d-121">Разверните модуль заголовка.</span><span class="sxs-lookup"><span data-stu-id="d974d-121">Expand the header module.</span></span>
1. <span data-ttu-id="d974d-122">В области свойств модуля заголовка укажите изображение и ссылку на логотип.</span><span class="sxs-lookup"><span data-stu-id="d974d-122">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="d974d-123">Сохраните заголовок, завершите его редактирование и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="d974d-123">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="d974d-124">После публикации отправленного фрагмента заголовка все страницы сайта, на которых используется шаблон, содержащий фрагмент заголовка, будут отображать ваш логотип.</span><span class="sxs-lookup"><span data-stu-id="d974d-124">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d974d-125">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d974d-125">Additional resources</span></span>

[<span data-ttu-id="d974d-126">Выбор темы сайта</span><span class="sxs-lookup"><span data-stu-id="d974d-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="d974d-127">Работа с переопределением файлов CSS</span><span class="sxs-lookup"><span data-stu-id="d974d-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="d974d-128">Добавление значка сайта</span><span class="sxs-lookup"><span data-stu-id="d974d-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="d974d-129">Добавление приветственного сообщения</span><span class="sxs-lookup"><span data-stu-id="d974d-129">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="d974d-130">Добавление уведомления об авторском праве</span><span class="sxs-lookup"><span data-stu-id="d974d-130">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="d974d-131">Добавление языков на сайт</span><span class="sxs-lookup"><span data-stu-id="d974d-131">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="d974d-132">Добавление кода скрипта на страницы сайта для поддержки телеметрии</span><span class="sxs-lookup"><span data-stu-id="d974d-132">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
