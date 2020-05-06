---
title: Создание страниц ответов для ошибок с кодом состояния 4xx/5xx
description: В этом разделе описывается, как создавать настраиваемые страницы ответов для ошибок кода состояния 4xx и 5xx с помощью средств разработки в Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: 060f5e5616624279711f61f582e6a898c7eb7785
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269552"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="3f5e1-103">Создание страниц ответов для ошибок с кодом состояния 4xx/5xx</span><span class="sxs-lookup"><span data-stu-id="3f5e1-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3f5e1-104">В этом разделе описывается, как создавать настраиваемые страницы ответов для ошибок кода состояния 4xx и 5xx с помощью средств разработки в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3f5e1-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="3f5e1-105">Overview</span></span>

<span data-ttu-id="3f5e1-106">Если запрос не выполнен, сервер выдает сообщения об ошибке кода состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="3f5e1-107">Код состояния 404 записывается и возвращается, если страница не найдена, а код состояния 500 фиксируется и возвращается в случае возникновения ошибки сервера.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="3f5e1-108">В Dynamics 365 Commerce пользователи приложения могут создавать пользовательские страницы ответа с кодами состояний ошибки, которые отображаются пользователям для этих сообщений об ошибке кода состояния.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="3f5e1-109">Создание страницы сообщения об ошибке кода состояния</span><span class="sxs-lookup"><span data-stu-id="3f5e1-109">Build a status code error response page</span></span>

<span data-ttu-id="3f5e1-110">Чтобы начать создание страницы сообщения об ошибке код состояния, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="3f5e1-111">В предпочтительном веб-браузере выполните вход в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="3f5e1-112">Выберите сайт, для которого требуется создать страницу сообщения об ошибке кода состояния 4xx/5xx</span><span class="sxs-lookup"><span data-stu-id="3f5e1-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="3f5e1-113">Создание шаблона</span><span class="sxs-lookup"><span data-stu-id="3f5e1-113">Build the template</span></span>

<span data-ttu-id="3f5e1-114">Чтобы создать шаблон для страницы сообщения об ошибке код состояния, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="3f5e1-115">Перейдите в пункт **Шаблоны**.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-115">Go to **Templates**.</span></span>
1. <span data-ttu-id="3f5e1-116">Выберите **Создать** для создания шаблона страницы.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-116">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="3f5e1-117">В диалоговом окне **Создать шаблон** в разделе **Имя шаблона** введите имя нового шаблона, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-117">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="3f5e1-118">Создайте шаблон на основе структуры, которую должна иметь страница сообщения об ошибке кода состояния.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-118">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="3f5e1-119">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-119">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="3f5e1-120">Создание страницы сообщения об ошибке кода состояния</span><span class="sxs-lookup"><span data-stu-id="3f5e1-120">Build the status code error response page</span></span>

<span data-ttu-id="3f5e1-121">Чтобы создать страницу сообщения об ошибке код состояния, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-121">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="3f5e1-122">Перейти к пункту **Страницы**.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-122">Go to **Pages**.</span></span>
1. <span data-ttu-id="3f5e1-123">Выберите **Создать** для создания страницы.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-123">Select **New** to create a page.</span></span>
1. <span data-ttu-id="3f5e1-124">В диалоговом окне **Выбор шаблона** выберите шаблон, затем в разделе **Имя страницы** введите имя страницы ответа при ошибке с кодом состояния.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-124">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="3f5e1-125">Не заполняйте поле **URL-адрес страницы**.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-125">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="3f5e1-126">Создайте страницу.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-126">Build the page.</span></span>
1. <span data-ttu-id="3f5e1-127">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-127">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="3f5e1-128">Можно создать отдельные страницы сообщений об ошибках кода состояния для ошибок кода состояния 4xx и 5xx.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-128">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="3f5e1-129">В качестве альтернативы можно использовать одну и ту же страницу сообщения об ошибке кода состояния для обеих категорий ошибок.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-129">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="3f5e1-130">Настройка перенаправления для страницы сообщения об ошибке кода состояния</span><span class="sxs-lookup"><span data-stu-id="3f5e1-130">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="3f5e1-131">Чтобы настроить перенаправление для страницы сообщения об ошибке код состояния, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-131">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="3f5e1-132">Перейдите в раздел **URL-адреса \> Создать \> Создать псевдоним** и выберите страницу сообщения об ошибке кода состояния, созданную ранее.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-132">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="3f5e1-133">В поле **Псевдоним** введите **default-4xx** или **default-5xx**, в зависимости от страницы сообщения об ошибке кода состояния, для которой выполняется настройка перенаправления.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-133">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="3f5e1-134">Эти псевдонимы должны быть опубликованы.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-134">These aliases must be published.</span></span> <span data-ttu-id="3f5e1-135">В противном случае перенаправление работать не будет.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-135">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="3f5e1-136">Выберите **ОК**, чтобы подтвердить связывание.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-136">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="3f5e1-137">Если для обеих категорий ошибок используется одна страница сообщения об ошибке кода состояния, повторите эту процедуру, чтобы связать псевдоним для другой категории ошибок с этой же страницей.</span><span class="sxs-lookup"><span data-stu-id="3f5e1-137">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3f5e1-138">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3f5e1-138">Additional resources</span></span>

[<span data-ttu-id="3f5e1-139">Работа с шаблонами</span><span class="sxs-lookup"><span data-stu-id="3f5e1-139">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="3f5e1-140">Добавление новой страницы сайта</span><span class="sxs-lookup"><span data-stu-id="3f5e1-140">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="3f5e1-141">Создание URL-адреса страницы</span><span class="sxs-lookup"><span data-stu-id="3f5e1-141">Create a page URL</span></span>](create-page-url.md)
