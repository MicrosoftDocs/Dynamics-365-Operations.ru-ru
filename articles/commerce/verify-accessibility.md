---
title: Проверка доступности контента страницы
description: В этой теме описывается, как проверить специальные возможности конвента страницы в Microsoft Dynamics 365 Commerce.
author: arotkin
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: arotkin
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8e35b0f71ff41bade266fb177e4500c7d124ed1f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002667"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="0e2d0-103">Проверка доступности контента страницы</span><span class="sxs-lookup"><span data-stu-id="0e2d0-103">Verify page content accessibility</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0e2d0-104">В этой теме описывается, как проверить специальные возможности конвента страницы в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0e2d0-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="0e2d0-105">Overview</span></span>

<span data-ttu-id="0e2d0-106">После того, как вы закончите менять страницу, вы должны убедиться, что контент доступен для всех в Интернете.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-106">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="0e2d0-107">В инструментах разработки Commerce вы можете легко проверить специальные возможности контента страницы с помощью интегрированной службы [Microsoft Accessibility Insights](https://accessibilityinsights.io/).</span><span class="sxs-lookup"><span data-stu-id="0e2d0-107">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="0e2d0-108">Эта служба проверяет содержимое страницы в соответствии с последними руководящими принципами [Специальные возможности World Wide Web Consortium (W3C)](https://www.w3.org/standards/webdesign/accessibility).</span><span class="sxs-lookup"><span data-stu-id="0e2d0-108">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="0e2d0-109">Перед тем, как использовать ее, необходимо включить интеграцию [Microsoft Accessibility Insights](https://accessibilityinsights.io/) на уровне клиента или сайта.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-109">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="0e2d0-110">Включите Microsoft Accessibility Insights для всех сайтов вашего клиента</span><span class="sxs-lookup"><span data-stu-id="0e2d0-110">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="0e2d0-111">Чтобы включить интеграцию [Microsoft Accessibility Insights](https://accessibilityinsights.io/) для всех сайтов Commerce в вашем клиенте, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-111">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="0e2d0-112">Чтобы открыть настройки клиента, вы должны войти в Commerce как системный администратор.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-112">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="0e2d0-113">Войдите в Commerce в качестве системного администратора.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-113">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="0e2d0-114">В левой области переходов выберите **Настройки клиента** (рядом с символом шестеренки), чтобы развернуть его.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-114">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="0e2d0-115">В **Настройки клиента** выберите **Функции**.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-115">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="0e2d0-116">Установите параметр **Проверка специальных возможностей** как **Вкл**.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-116">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="0e2d0-117">Включите Microsoft Accessibility Insights для одного сайта</span><span class="sxs-lookup"><span data-stu-id="0e2d0-117">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="0e2d0-118">Чтобы включить интеграцию [Microsoft Accessibility Insights](https://accessibilityinsights.io/) для одного сайта Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-118">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="0e2d0-119">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="0e2d0-119">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="0e2d0-120">На левом панели навигации выберите **Настройки сайта**, чтобы развернуть.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-120">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="0e2d0-121">В **Настройки сайта** выберите **Функции**.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-121">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="0e2d0-122">Установите параметр **Проверка специальных возможностей** как **Вкл**.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-122">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="0e2d0-123">Проверить специальные возможности содержимого на главной странице</span><span class="sxs-lookup"><span data-stu-id="0e2d0-123">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="0e2d0-124">Чтобы использовать интегрированную службу [Microsoft Accessibility Insights](https://accessibilityinsights.io/) для сканирования и проверки содержимого вашей домашней страницы в Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-124">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="0e2d0-125">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="0e2d0-125">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="0e2d0-126">В левой области переходов выберите **Страницы**.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-126">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="0e2d0-127">Найдите и выберите домашнюю страницу для ее открытия в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-127">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="0e2d0-128">На панели команд выберите **Проверить специальные возможности**.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-128">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="0e2d0-129">Отображается страница **Проверка специальных возможностей**.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-129">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="0e2d0-130">После завершения сканирования просмотрите содержание отчета.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-130">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="0e2d0-131">Если какие-либо проверки не удались, выберите каждый элемент с ошибкой, чтобы развернуть его, чтобы просмотреть более подробную информацию.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-131">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="0e2d0-132">Чтобы закрыть отчет после его проверки, прокрутите в нижней части страницы **Проверить специальные возможности** и выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e2d0-132">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0e2d0-133">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0e2d0-133">Additional resources</span></span>

[<span data-ttu-id="0e2d0-134">Изменение существующей страницы сайта</span><span class="sxs-lookup"><span data-stu-id="0e2d0-134">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="0e2d0-135">Добавление новой страницы сайта</span><span class="sxs-lookup"><span data-stu-id="0e2d0-135">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="0e2d0-136">Выбор макета страницы</span><span class="sxs-lookup"><span data-stu-id="0e2d0-136">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="0e2d0-137">Управление метаданными для поисковой оптимизации</span><span class="sxs-lookup"><span data-stu-id="0e2d0-137">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="0e2d0-138">Сохранение, предварительный просмотр и публикация страницы</span><span class="sxs-lookup"><span data-stu-id="0e2d0-138">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="0e2d0-139">Расширение возможностей страницы продукта</span><span class="sxs-lookup"><span data-stu-id="0e2d0-139">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="0e2d0-140">Расширение возможностей целевой страницы категории</span><span class="sxs-lookup"><span data-stu-id="0e2d0-140">Enrich a category landing page</span></span>](enrich-category-page.md)
