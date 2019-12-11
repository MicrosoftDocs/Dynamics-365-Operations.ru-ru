---
title: Создание страниц ответов для ошибок с кодом состояния 4xx/5xx
description: В этом разделе описывается, как создавать настраиваемые страницы ответов для ошибок кода состояния 4xx и 5xx с помощью средств разработки в Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bcceeb1bc68c6432442c863ca06b7ba81d0abed8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697114"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="f2f17-103">Создание страниц ответов для ошибок с кодом состояния 4xx/5xx</span><span class="sxs-lookup"><span data-stu-id="f2f17-103">Build custom response pages for 4xx/5xx status code errors</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f2f17-104">В этом разделе описывается, как создавать настраиваемые страницы ответов для ошибок кода состояния 4xx и 5xx с помощью средств разработки в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f2f17-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f2f17-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="f2f17-105">Overview</span></span>

<span data-ttu-id="f2f17-106">Если запрос не выполнен, сервер выдает сообщения об ошибке кода состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="f2f17-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="f2f17-107">Код состояния 404 записывается и возвращается, если страница не найдена, а код состояния 500 фиксируется и возвращается в случае возникновения ошибки сервера.</span><span class="sxs-lookup"><span data-stu-id="f2f17-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="f2f17-108">В Dynamics 365 Commerce пользователи приложения могут создавать пользовательские страницы ответа с кодами состояний ошибки, которые отображаются пользователям для этих сообщений об ошибке кода состояния.</span><span class="sxs-lookup"><span data-stu-id="f2f17-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="f2f17-109">Создание страницы сообщения об ошибке кода состояния</span><span class="sxs-lookup"><span data-stu-id="f2f17-109">Build a status code error response page</span></span>

<span data-ttu-id="f2f17-110">Чтобы начать создание страницы сообщения об ошибке код состояния, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f2f17-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="f2f17-111">В предпочтительном веб-браузере выполните вход в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f2f17-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="f2f17-112">Выберите сайт, для которого требуется создать страницу сообщения об ошибке кода состояния 4xx/5xx</span><span class="sxs-lookup"><span data-stu-id="f2f17-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="f2f17-113">Создание шаблона</span><span class="sxs-lookup"><span data-stu-id="f2f17-113">Build the template</span></span>

<span data-ttu-id="f2f17-114">Чтобы создать шаблон для страницы сообщения об ошибке код состояния, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f2f17-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="f2f17-115">Перейдите в раздел **Шаблоны \> Создать шаблон**.</span><span class="sxs-lookup"><span data-stu-id="f2f17-115">Go to **Templates \> New template**.</span></span>
1. <span data-ttu-id="f2f17-116">Задайте имя нового шаблона.</span><span class="sxs-lookup"><span data-stu-id="f2f17-116">Name the new template.</span></span>
1. <span data-ttu-id="f2f17-117">Создайте шаблон на основе структуры, которую должна иметь страница сообщения об ошибке кода состояния.</span><span class="sxs-lookup"><span data-stu-id="f2f17-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="f2f17-118">Верните шаблон и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="f2f17-118">Check the template in, and publish it.</span></span>

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="f2f17-119">Создание страницы сообщения об ошибке кода состояния</span><span class="sxs-lookup"><span data-stu-id="f2f17-119">Build the status code error response page</span></span>

<span data-ttu-id="f2f17-120">Чтобы создать страницу сообщения об ошибке код состояния, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f2f17-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="f2f17-121">Перейти в раздел **Страницы \> Создать страницу**.</span><span class="sxs-lookup"><span data-stu-id="f2f17-121">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="f2f17-122">Присвойте имя странице сообщения об ошибке кода состояния, но **не** задавайте поле **URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="f2f17-122">Name the status code error response page, but do **not** set the **URL** field.</span></span>
1. <span data-ttu-id="f2f17-123">Создайте страницу.</span><span class="sxs-lookup"><span data-stu-id="f2f17-123">Build the page.</span></span>
1. <span data-ttu-id="f2f17-124">Верните страницу и опубликуйте его.</span><span class="sxs-lookup"><span data-stu-id="f2f17-124">Check the page in, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="f2f17-125">Можно создать отдельные страницы сообщений об ошибках кода состояния для ошибок кода состояния 4xx и 5xx.</span><span class="sxs-lookup"><span data-stu-id="f2f17-125">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="f2f17-126">В качестве альтернативы можно использовать одну и ту же страницу сообщения об ошибке кода состояния для обеих категорий ошибок.</span><span class="sxs-lookup"><span data-stu-id="f2f17-126">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="f2f17-127">Настройка перенаправления для страницы сообщения об ошибке кода состояния</span><span class="sxs-lookup"><span data-stu-id="f2f17-127">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="f2f17-128">Чтобы настроить перенаправление для страницы сообщения об ошибке код состояния, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f2f17-128">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="f2f17-129">Перейдите в раздел **URL-адреса \> Создать \> Создать псевдоним** и выберите страницу сообщения об ошибке кода состояния, созданную ранее.</span><span class="sxs-lookup"><span data-stu-id="f2f17-129">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="f2f17-130">В поле **Псевдоним** введите **default-4xx** или **default-5xx**, в зависимости от страницы сообщения об ошибке кода состояния, для которой выполняется настройка перенаправления.</span><span class="sxs-lookup"><span data-stu-id="f2f17-130">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="f2f17-131">Эти псевдонимы должны быть опубликованы.</span><span class="sxs-lookup"><span data-stu-id="f2f17-131">These aliases must be published.</span></span> <span data-ttu-id="f2f17-132">В противном случае перенаправление работать не будет.</span><span class="sxs-lookup"><span data-stu-id="f2f17-132">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="f2f17-133">Выберите **ОК**, чтобы подтвердить связывание.</span><span class="sxs-lookup"><span data-stu-id="f2f17-133">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="f2f17-134">Если для обеих категорий ошибок используется одна страница сообщения об ошибке кода состояния, повторите эту процедуру, чтобы связать псевдоним для другой категории ошибок с этой же страницей.</span><span class="sxs-lookup"><span data-stu-id="f2f17-134">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2f17-135">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f2f17-135">Additional resources</span></span>

[<span data-ttu-id="f2f17-136">Работа с шаблонами</span><span class="sxs-lookup"><span data-stu-id="f2f17-136">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="f2f17-137">Добавление новой страницы сайта</span><span class="sxs-lookup"><span data-stu-id="f2f17-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="f2f17-138">Создание URL-адреса страницы</span><span class="sxs-lookup"><span data-stu-id="f2f17-138">Create a page URL</span></span>](create-page-url.md)
