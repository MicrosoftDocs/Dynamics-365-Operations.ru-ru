---
title: Проверка доступности контента страницы
description: В этой теме описывается, как проверить специальные возможности конвента страницы в Microsoft Dynamics 365 Commerce.
author: josaw1
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
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: fc3dca673510e1636f497bb7d5c295bebe025677
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4415364"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="ae5b4-103">Проверка доступности контента страницы</span><span class="sxs-lookup"><span data-stu-id="ae5b4-103">Verify page content accessibility</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ae5b4-104">В этой теме описывается, как проверить специальные возможности конвента страницы в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ae5b4-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ae5b4-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="ae5b4-105">Overview</span></span>

<span data-ttu-id="ae5b4-106">После того, как вы закончите менять страницу, вы должны убедиться, что контент доступен для всех в Интернете.</span><span class="sxs-lookup"><span data-stu-id="ae5b4-106">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="ae5b4-107">В инструментах разработки Commerce вы можете легко проверить специальные возможности контента страницы с помощью интегрированной службы [Microsoft Accessibility Insights](https://accessibilityinsights.io/).</span><span class="sxs-lookup"><span data-stu-id="ae5b4-107">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="ae5b4-108">Эта служба проверяет содержимое страницы в соответствии с последними руководящими принципами [Специальные возможности World Wide Web Consortium (W3C)](https://www.w3.org/standards/webdesign/accessibility).</span><span class="sxs-lookup"><span data-stu-id="ae5b4-108">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="ae5b4-109">Перед тем, как использовать ее, необходимо включить интеграцию [Microsoft Accessibility Insights](https://accessibilityinsights.io/) на уровне клиента или сайта.</span><span class="sxs-lookup"><span data-stu-id="ae5b4-109">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="ae5b4-110">Включите Microsoft Accessibility Insights для всех сайтов вашего клиента</span><span class="sxs-lookup"><span data-stu-id="ae5b4-110">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="ae5b4-111">Чтобы включить интеграцию [Microsoft Accessibility Insights](https://accessibilityinsights.io/) для всех сайтов Commerce в вашем клиенте, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ae5b4-111">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="ae5b4-112">Чтобы открыть настройки клиента, вы должны войти в Commerce как системный администратор.</span><span class="sxs-lookup"><span data-stu-id="ae5b4-112">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="ae5b4-113">Войдите в Commerce в качестве системного администратора.</span><span class="sxs-lookup"><span data-stu-id="ae5b4-113">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="ae5b4-114">В левой области переходов выберите **Настройки клиента** (рядом с символом шестеренки), чтобы развернуть его.</span><span class="sxs-lookup"><span data-stu-id="ae5b4-114">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="ae5b4-115">В **Настройки клиента** выберите **Функции**.</span><span class="sxs-lookup"><span data-stu-id="ae5b4-115">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="ae5b4-116">Установите параметр **Проверка специальных возможностей** как **Вкл**.</span><span class="sxs-lookup"><span data-stu-id="ae5b4-116">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="ae5b4-117">Включите Microsoft Accessibility Insights для одного сайта</span><span class="sxs-lookup"><span data-stu-id="ae5b4-117">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="ae5b4-118">Чтобы включить интеграцию [Microsoft Accessibility Insights](https://accessibilityinsights.io/) для одного сайта Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ae5b4-118">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="ae5b4-119">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="ae5b4-119">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="ae5b4-120">На левом панели навигации выберите **Настройки сайта**, чтобы развернуть.</span><span class="sxs-lookup"><span data-stu-id="ae5b4-120">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="ae5b4-121">В **Настройки сайта** выберите **Функции**.</span><span class="sxs-lookup"><span data-stu-id="ae5b4-121">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="ae5b4-122">Установите параметр **Проверка специальных возможностей** как **Вкл**.</span><span class="sxs-lookup"><span data-stu-id="ae5b4-122">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="ae5b4-123">Проверить специальные возможности содержимого на главной странице</span><span class="sxs-lookup"><span data-stu-id="ae5b4-123">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="ae5b4-124">Чтобы использовать интегрированную службу [Microsoft Accessibility Insights](https://accessibilityinsights.io/) для сканирования и проверки содержимого вашей домашней страницы в Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ae5b4-124">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="ae5b4-125">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="ae5b4-125">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="ae5b4-126">В левой области переходов выберите **Страницы**.</span><span class="sxs-lookup"><span data-stu-id="ae5b4-126">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="ae5b4-127">Найдите и выберите домашнюю страницу для ее открытия в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="ae5b4-127">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="ae5b4-128">На панели команд выберите **Проверить специальные возможности**.</span><span class="sxs-lookup"><span data-stu-id="ae5b4-128">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="ae5b4-129">Отображается страница **Проверка специальных возможностей**.</span><span class="sxs-lookup"><span data-stu-id="ae5b4-129">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="ae5b4-130">После завершения сканирования просмотрите содержание отчета.</span><span class="sxs-lookup"><span data-stu-id="ae5b4-130">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="ae5b4-131">Если какие-либо проверки не удались, выберите каждый элемент с ошибкой, чтобы развернуть его, чтобы просмотреть более подробную информацию.</span><span class="sxs-lookup"><span data-stu-id="ae5b4-131">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="ae5b4-132">Чтобы закрыть отчет после его проверки, прокрутите в нижней части страницы **Проверить специальные возможности** и выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae5b4-132">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ae5b4-133">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ae5b4-133">Additional resources</span></span>

[<span data-ttu-id="ae5b4-134">Изменение существующей страницы сайта</span><span class="sxs-lookup"><span data-stu-id="ae5b4-134">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="ae5b4-135">Добавление новой страницы сайта</span><span class="sxs-lookup"><span data-stu-id="ae5b4-135">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="ae5b4-136">Выбор макета страницы</span><span class="sxs-lookup"><span data-stu-id="ae5b4-136">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="ae5b4-137">Управление метаданными SEO</span><span class="sxs-lookup"><span data-stu-id="ae5b4-137">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="ae5b4-138">Сохранение, предварительный просмотр и публикация страницы</span><span class="sxs-lookup"><span data-stu-id="ae5b4-138">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="ae5b4-139">Расширение возможностей страницы продукта</span><span class="sxs-lookup"><span data-stu-id="ae5b4-139">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="ae5b4-140">Расширение возможностей целевой страницы категории</span><span class="sxs-lookup"><span data-stu-id="ae5b4-140">Enrich a category landing page</span></span>](enrich-category-page.md)
