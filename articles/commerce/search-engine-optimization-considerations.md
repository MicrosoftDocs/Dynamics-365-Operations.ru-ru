---
title: Особенности поисковой оптимизации (SEO) для вашего сайта
description: В этом разделе рассматриваются вопросы оптимизации поисковых систем (SEO) для вашего сайта от его разработки до ввода в эксплуатацию.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7c7afed8e4620d5fe49ead47eb6c17d97d7492ad
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002818"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a><span data-ttu-id="51d7e-103">Особенности поисковой оптимизации (SEO) для вашего сайта</span><span class="sxs-lookup"><span data-stu-id="51d7e-103">Search engine optimization (SEO) considerations for your site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="51d7e-104">В этом разделе рассматриваются вопросы оптимизации поисковых систем (SEO) для вашего сайта от его разработки до ввода в эксплуатацию.</span><span class="sxs-lookup"><span data-stu-id="51d7e-104">This topic covers earch engine optimization (SEO) considerations for your site from development to production.</span></span>

## <a name="a-site-that-is-under-development"></a><span data-ttu-id="51d7e-105">Сайт на стадии разработки</span><span class="sxs-lookup"><span data-stu-id="51d7e-105">A site that is under development</span></span>

<span data-ttu-id="51d7e-106">При разработке сайта все страницы сайта должны иметь мета-теги **NOINDEX** и **NOFOLLOW**, чтобы поисковые системы не могли индексировать страницы и хранить версии разработки сайта в своем кэше.</span><span class="sxs-lookup"><span data-stu-id="51d7e-106">While a site is under development, all site pages should have the **NOINDEX** and **NOFOLLOW** meta tags, so that search engines don't index the pages and store development versions of your site in their cache.</span></span> <span data-ttu-id="51d7e-107">Для выполнения этой конфигурации необходимо добавить модуль мета-тегов по умолчанию в шаблон страницы сайта.</span><span class="sxs-lookup"><span data-stu-id="51d7e-107">To do this configuration, you must add the default meta tags module to the site page template.</span></span> <span data-ttu-id="51d7e-108">Свойства мета-тегов по умолчанию будут затем доступны в разделе свойств SEO в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="51d7e-108">The default meta tags properties will then be available in the SEO properties section in the page editor.</span></span> <span data-ttu-id="51d7e-109">Эти свойства можно использовать для управления мета-тегами.</span><span class="sxs-lookup"><span data-stu-id="51d7e-109">You can use these properties to manage the meta tags.</span></span>

## <a name="soft-launch-of-a-site"></a><span data-ttu-id="51d7e-110">Мягкий запуск сайта</span><span class="sxs-lookup"><span data-stu-id="51d7e-110">Soft launch of a site</span></span>

<span data-ttu-id="51d7e-111">Во время "мягкого запуска" веб-сайт становится доступным для ограниченной аудитории или рынка до полного запуска.</span><span class="sxs-lookup"><span data-stu-id="51d7e-111">During a "soft launch," a website is made available to a limited audience or market before the full launch occurs.</span></span> <span data-ttu-id="51d7e-112">Если вы выполняете мягкий запуск веб-сайта, рекомендуется оставить мета-теги **NOINDEX**.</span><span class="sxs-lookup"><span data-stu-id="51d7e-112">If you do a soft launch of your website, you should consider leaving the **NOINDEX** meta tags in place.</span></span> <span data-ttu-id="51d7e-113">Таким образом, можно гарантировать, что мягкий запуск останется ограниченным для выбранной аудитории, к которой вы хотите обратиться.</span><span class="sxs-lookup"><span data-stu-id="51d7e-113">In this way, you help guarantee that the soft launch remains restricted to the limited audience that you want to reach.</span></span>

## <a name="a-site-that-is-in-production"></a><span data-ttu-id="51d7e-114">Сайт, который находится в эксплуатации</span><span class="sxs-lookup"><span data-stu-id="51d7e-114">A site that is in production</span></span>

<span data-ttu-id="51d7e-115">Если сайт находится в эксплуатации, следует убедиться, что все страницы сайта правильно помечены тегами.</span><span class="sxs-lookup"><span data-stu-id="51d7e-115">When a site is in production, you should make sure that all site pages are correctly tagged.</span></span> <span data-ttu-id="51d7e-116">Microsoft Dynamics 365 Commerce использует сведения, введенные для страницы, чтобы отобразить все сведения SEO на этой странице.</span><span class="sxs-lookup"><span data-stu-id="51d7e-116">Microsoft Dynamics 365 Commerce uses the information that is entered for a page to render all the SEO information on that page.</span></span> <span data-ttu-id="51d7e-117">Эта функция предусмотрена в следующих модулях: сводка страницы категории, сводка страницы списка и сводка страницы продукта.</span><span class="sxs-lookup"><span data-stu-id="51d7e-117">The following modules provide this functionality: category page summary, list page summary, and product page summary.</span></span>

<span data-ttu-id="51d7e-118">Для оптимизации индексации поисковых систем система визуализации использует как сведения из свойств SEO, которые настроены в Dynamics 365 Commerce, так и сведения, зависящие от модуля.</span><span class="sxs-lookup"><span data-stu-id="51d7e-118">To optimize search engine indexing, the rendering framework uses both information from the SEO properties that are configured in Dynamics 365 Commerce and module-specific information.</span></span> <span data-ttu-id="51d7e-119">Для сайта, который находится в эксплуатации, следует убедиться, что файл robots. txt поддерживает индексацию всего сайта и что он содержит ссылки на опубликованный документ карты сайта.</span><span class="sxs-lookup"><span data-stu-id="51d7e-119">For a site that is in production, you should make sure that the robots.txt file allows for indexing of your whole site, and that it contains links to your published site map document.</span></span> <span data-ttu-id="51d7e-120">Необходимо включить функцию создания карты сайта в пункте **Параметры сайта \> Карты сайта включены**.</span><span class="sxs-lookup"><span data-stu-id="51d7e-120">You should turn on the site map generation functionality at **Site Settings \> Site maps enabled**.</span></span>

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a><span data-ttu-id="51d7e-121">Страница параметров SEO для внутреннего предварительного просмотра, ограниченной аудитории и всей аудитории</span><span class="sxs-lookup"><span data-stu-id="51d7e-121">Page SEO settings for internal preview, limited audiences, and all audiences</span></span>

<span data-ttu-id="51d7e-122">Так как Dynamics 365 Commerce поддерживает предварительный просмотр "что видите, то и получаете" (WYSIWYG) с проверкой подлинности, авторы могут готовить свое содержимое страниц, не заботясь о том, что информация станет видимой для посетителей сайта.</span><span class="sxs-lookup"><span data-stu-id="51d7e-122">Because Dynamics 365 Commerce supports "what you see is what you get" (WYSIWYG) authenticated previews, authors can prepare their page content without having to worry that the information will become visible to site visitors.</span></span> <span data-ttu-id="51d7e-123">Если страница должна быть опубликована, но ее демонстрация должна быть ограничена, она должна иметь мета-тег **NOINDEX**, чтобы она не был проиндексирована поисковыми системами.</span><span class="sxs-lookup"><span data-stu-id="51d7e-123">If a page must be published, but its exposure must be limited, it should have the **NOINDEX** meta tag, so that it won't be indexed by search engines.</span></span> <span data-ttu-id="51d7e-124">Затем, когда страница готова для всей аудитории, должны присутствовать все базовые метаданные SEO, чтобы повысить эффективность индексирования поисковых систем.</span><span class="sxs-lookup"><span data-stu-id="51d7e-124">Then, when the page is ready for all audiences, all the basic SEO metadata should be present, to maximize the efficiency of search engine indexing.</span></span> <span data-ttu-id="51d7e-125">Кроме того, следует удалить мета-тег **NOLIMIT**.</span><span class="sxs-lookup"><span data-stu-id="51d7e-125">Additionally, the **NOLIMIT** meta tag should be removed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51d7e-126">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="51d7e-126">Additional resources</span></span>

[<span data-ttu-id="51d7e-127">Управление пользователями и ролями электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="51d7e-127">Manage e-Commerce users and roles</span></span>](manage-ecommerce-users-roles.md)

[<span data-ttu-id="51d7e-128">Добавление кода скрипта на страницы сайта для поддержки телеметрии</span><span class="sxs-lookup"><span data-stu-id="51d7e-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="51d7e-129">Управление политикой безопасности содержимого (CSP)</span><span class="sxs-lookup"><span data-stu-id="51d7e-129">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
