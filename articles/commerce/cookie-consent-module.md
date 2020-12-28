---
title: Модуль согласия на файлы cookie
description: В этом разделе описываются модули согласия на получение файлов cookie, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 60ce530575841c22355e4a14e8b0bbec6c0e35ab
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415137"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="24ce6-103">Модуль согласия на файлы cookie</span><span class="sxs-lookup"><span data-stu-id="24ce6-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="24ce6-104">В этом разделе описываются модули согласия на получение файлов cookie, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="24ce6-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="24ce6-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="24ce6-105">Overview</span></span>

<span data-ttu-id="24ce6-106">Модуль согласия на прием файлов cookie запрашивает у пользователей сайта разрешение на файлы cookie для любой функции или модуля, отслеживающего файлы cookie браузера.</span><span class="sxs-lookup"><span data-stu-id="24ce6-106">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="24ce6-107">Разрешение необходимо при первом просмотре сайта пользователем в новом сеансе веб-браузера.</span><span class="sxs-lookup"><span data-stu-id="24ce6-107">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="24ce6-108">Когда согласие получено, оно отслеживается, и пользователю сайта не выдается повторный запрос на согласие.</span><span class="sxs-lookup"><span data-stu-id="24ce6-108">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="24ce6-109">Дополнительные сведения см. в разделе [Соответствие файлов cookie](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="24ce6-109">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="24ce6-110">Если согласие пользователя на файлы cookie не получено, все функции или модули, требующие согласия на файлы cookie, не будут отображаться на странице.</span><span class="sxs-lookup"><span data-stu-id="24ce6-110">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="24ce6-111">Например, модуль оформления, модуль социальных сетей и предпочтительная функция магазина все требуют согласия на файлы cookie и не будут отображены, если согласие пользователя сайта не получено.</span><span class="sxs-lookup"><span data-stu-id="24ce6-111">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="24ce6-112">Модуль согласия на файлы cookie может быть настроен на фрагменте заголовка страницы, чтобы его можно было применять при загрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="24ce6-112">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="24ce6-113">Модуль согласия на файлы cookie должен иметь четкое сообщение, которое информирует пользователя сайта об использовании файлов cookie на сайте и должна предоставить ссылку на страницу конфиденциальности этого сайта.</span><span class="sxs-lookup"><span data-stu-id="24ce6-113">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="24ce6-114">На следующем рисунке показан пример сообщения о согласии на файлы cookie со ссылкой на страницу политики конфиденциальности сайта, которая отображается в заголовке страницы сайта.</span><span class="sxs-lookup"><span data-stu-id="24ce6-114">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="24ce6-115">![Пример модуля получения согласия на файлы cookie](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="24ce6-115">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="24ce6-116">Свойства модуля согласия на файлы cookie</span><span class="sxs-lookup"><span data-stu-id="24ce6-116">Cookie consent module properties</span></span>

| <span data-ttu-id="24ce6-117">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="24ce6-117">Property name</span></span>             | <span data-ttu-id="24ce6-118">значение</span><span class="sxs-lookup"><span data-stu-id="24ce6-118">Value</span></span>                 | <span data-ttu-id="24ce6-119">описание</span><span class="sxs-lookup"><span data-stu-id="24ce6-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="24ce6-120">Форматированный текст</span><span class="sxs-lookup"><span data-stu-id="24ce6-120">Rich Text</span></span>                  | <span data-ttu-id="24ce6-121">Форматированный текст</span><span class="sxs-lookup"><span data-stu-id="24ce6-121">Rich Text</span></span> | <span data-ttu-id="24ce6-122">Задает оповещение с форматированным текстом пользователям сайта, когда сайт использует файлы cookie браузера, которое сообщает, что пользователи должны согласиться на использование файлов cookie, чтобы обеспечить полную функциональность этого сайта.</span><span class="sxs-lookup"><span data-stu-id="24ce6-122">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="24ce6-123">Ссылки</span><span class="sxs-lookup"><span data-stu-id="24ce6-123">Links</span></span> | <span data-ttu-id="24ce6-124">URL</span><span class="sxs-lookup"><span data-stu-id="24ce6-124">URL</span></span> | <span data-ttu-id="24ce6-125">Одну или несколько ссылок можно добавить на страницу конфиденциальности сайта, на которой описаны типы файлов cookie, отслеживаемых на данном сайте.</span><span class="sxs-lookup"><span data-stu-id="24ce6-125">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="24ce6-126">Добавление модуля согласия на файлы cookie на страницы сайта</span><span class="sxs-lookup"><span data-stu-id="24ce6-126">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="24ce6-127">Чтобы эффективно добавить модуль разрешения файлов cookie к нескольким страницам сайта, его можно добавить в фрагмент заголовка общей страницы.</span><span class="sxs-lookup"><span data-stu-id="24ce6-127">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="24ce6-128">После того как фрагмент заголовка добавляется ко всем страницам сайта, уведомление о согласии на файлы cookie автоматически выводится при первом переходе пользователя сайта на страницу сайта.</span><span class="sxs-lookup"><span data-stu-id="24ce6-128">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="24ce6-129">Дополнительные сведения о фрагментах заголовков и модулях см. в разделе [Модуль заголовка](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="24ce6-129">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="24ce6-130">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="24ce6-130">Additional resources</span></span>

[<span data-ttu-id="24ce6-131">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="24ce6-131">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="24ce6-132">Модуль верхнего колонтитула</span><span class="sxs-lookup"><span data-stu-id="24ce6-132">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="24ce6-133">Соответствие файлов cookie</span><span class="sxs-lookup"><span data-stu-id="24ce6-133">Cookie compliance</span></span>](cookie-compliance.md)
