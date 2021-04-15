---
title: Проверка доступности контента страницы
description: В этой теме описывается, как проверить специальные возможности конвента страницы в Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 885696c13b0e5353e6dbd9dc21cf075d5e301786
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791639"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="4619f-103">Проверка доступности контента страницы</span><span class="sxs-lookup"><span data-stu-id="4619f-103">Verify page content accessibility</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4619f-104">В этой теме описывается, как проверить специальные возможности конвента страницы в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4619f-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4619f-105">После того, как вы закончите менять страницу, вы должны убедиться, что контент доступен для всех в Интернете.</span><span class="sxs-lookup"><span data-stu-id="4619f-105">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="4619f-106">В инструментах разработки Commerce вы можете легко проверить специальные возможности контента страницы с помощью интегрированной службы [Microsoft Accessibility Insights](https://accessibilityinsights.io/).</span><span class="sxs-lookup"><span data-stu-id="4619f-106">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="4619f-107">Эта служба проверяет содержимое страницы в соответствии с последними руководящими принципами [Специальные возможности World Wide Web Consortium (W3C)](https://www.w3.org/standards/webdesign/accessibility).</span><span class="sxs-lookup"><span data-stu-id="4619f-107">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="4619f-108">Перед тем, как использовать ее, необходимо включить интеграцию [Microsoft Accessibility Insights](https://accessibilityinsights.io/) на уровне клиента или сайта.</span><span class="sxs-lookup"><span data-stu-id="4619f-108">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="4619f-109">Включите Microsoft Accessibility Insights для всех сайтов вашего клиента</span><span class="sxs-lookup"><span data-stu-id="4619f-109">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="4619f-110">Чтобы включить интеграцию [Microsoft Accessibility Insights](https://accessibilityinsights.io/) для всех сайтов Commerce в вашем клиенте, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4619f-110">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="4619f-111">Чтобы открыть настройки клиента, вы должны войти в Commerce как системный администратор.</span><span class="sxs-lookup"><span data-stu-id="4619f-111">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="4619f-112">Войдите в Commerce в качестве системного администратора.</span><span class="sxs-lookup"><span data-stu-id="4619f-112">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="4619f-113">В левой области переходов выберите **Настройки клиента** (рядом с символом шестеренки), чтобы развернуть его.</span><span class="sxs-lookup"><span data-stu-id="4619f-113">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="4619f-114">В **Настройки клиента** выберите **Функции**.</span><span class="sxs-lookup"><span data-stu-id="4619f-114">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="4619f-115">Установите параметр **Проверка специальных возможностей** как **Вкл**.</span><span class="sxs-lookup"><span data-stu-id="4619f-115">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="4619f-116">Включите Microsoft Accessibility Insights для одного сайта</span><span class="sxs-lookup"><span data-stu-id="4619f-116">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="4619f-117">Чтобы включить интеграцию [Microsoft Accessibility Insights](https://accessibilityinsights.io/) для одного сайта Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4619f-117">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="4619f-118">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="4619f-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="4619f-119">На левом панели навигации выберите **Настройки сайта**, чтобы развернуть.</span><span class="sxs-lookup"><span data-stu-id="4619f-119">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="4619f-120">В **Настройки сайта** выберите **Функции**.</span><span class="sxs-lookup"><span data-stu-id="4619f-120">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="4619f-121">Установите параметр **Проверка специальных возможностей** как **Вкл**.</span><span class="sxs-lookup"><span data-stu-id="4619f-121">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="4619f-122">Проверить специальные возможности содержимого на главной странице</span><span class="sxs-lookup"><span data-stu-id="4619f-122">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="4619f-123">Чтобы использовать интегрированную службу [Microsoft Accessibility Insights](https://accessibilityinsights.io/) для сканирования и проверки содержимого вашей домашней страницы в Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4619f-123">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="4619f-124">В области **Сайты** выберите **Fabrikam** (или имя вашего сайта).</span><span class="sxs-lookup"><span data-stu-id="4619f-124">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="4619f-125">В левой области переходов выберите **Страницы**.</span><span class="sxs-lookup"><span data-stu-id="4619f-125">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="4619f-126">Найдите и выберите домашнюю страницу для ее открытия в редакторе страниц.</span><span class="sxs-lookup"><span data-stu-id="4619f-126">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="4619f-127">На панели команд выберите **Проверить специальные возможности**.</span><span class="sxs-lookup"><span data-stu-id="4619f-127">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="4619f-128">Отображается страница **Проверка специальных возможностей**.</span><span class="sxs-lookup"><span data-stu-id="4619f-128">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="4619f-129">После завершения сканирования просмотрите содержание отчета.</span><span class="sxs-lookup"><span data-stu-id="4619f-129">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="4619f-130">Если какие-либо проверки не удались, выберите каждый элемент с ошибкой, чтобы развернуть его, чтобы просмотреть более подробную информацию.</span><span class="sxs-lookup"><span data-stu-id="4619f-130">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="4619f-131">Чтобы закрыть отчет после его проверки, прокрутите в нижней части страницы **Проверить специальные возможности** и выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="4619f-131">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4619f-132">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4619f-132">Additional resources</span></span>

[<span data-ttu-id="4619f-133">Изменение существующей страницы сайта</span><span class="sxs-lookup"><span data-stu-id="4619f-133">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="4619f-134">Добавление новой страницы сайта</span><span class="sxs-lookup"><span data-stu-id="4619f-134">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="4619f-135">Выбор макета страницы</span><span class="sxs-lookup"><span data-stu-id="4619f-135">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="4619f-136">Управление метаданными SEO</span><span class="sxs-lookup"><span data-stu-id="4619f-136">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="4619f-137">Сохранение, предварительный просмотр и публикация страницы</span><span class="sxs-lookup"><span data-stu-id="4619f-137">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="4619f-138">Расширение возможностей страницы продукта</span><span class="sxs-lookup"><span data-stu-id="4619f-138">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="4619f-139">Расширение возможностей целевой страницы категории</span><span class="sxs-lookup"><span data-stu-id="4619f-139">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="4619f-140">Создание динамических страниц электронной коммерции на основе параметров URL-адреса</span><span class="sxs-lookup"><span data-stu-id="4619f-140">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
