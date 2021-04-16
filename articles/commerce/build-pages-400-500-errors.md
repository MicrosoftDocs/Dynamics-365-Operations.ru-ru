---
title: Создание страниц ответов для ошибок с кодом состояния 4xx/5xx
description: В этом разделе описывается, как создавать настраиваемые страницы ответов для ошибок кода состояния 4xx и 5xx с помощью средств разработки в Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b35b3c07b1edd41e6a3763c0001529e125e4636
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799663"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="40364-103">Создание страниц ответов для ошибок с кодом состояния 4xx/5xx</span><span class="sxs-lookup"><span data-stu-id="40364-103">Build custom response pages for 4xx/5xx status code errors</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="40364-104">В этом разделе описывается, как создавать настраиваемые страницы ответов для ошибок кода состояния 4xx и 5xx с помощью средств разработки в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="40364-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="40364-105">Если запрос не выполнен, сервер выдает сообщения об ошибке кода состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="40364-105">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="40364-106">Код состояния 404 записывается и возвращается, если страница не найдена, а код состояния 500 фиксируется и возвращается в случае возникновения ошибки сервера.</span><span class="sxs-lookup"><span data-stu-id="40364-106">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="40364-107">В Dynamics 365 Commerce пользователи приложения могут создавать пользовательские страницы ответа с кодами состояний ошибки, которые отображаются пользователям для этих сообщений об ошибке кода состояния.</span><span class="sxs-lookup"><span data-stu-id="40364-107">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="40364-108">Создание страницы сообщения об ошибке кода состояния</span><span class="sxs-lookup"><span data-stu-id="40364-108">Build a status code error response page</span></span>

<span data-ttu-id="40364-109">Чтобы начать создание страницы сообщения об ошибке код состояния, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="40364-109">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="40364-110">В предпочтительном веб-браузере выполните вход в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="40364-110">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="40364-111">Выберите сайт, для которого требуется создать страницу сообщения об ошибке кода состояния 4xx/5xx</span><span class="sxs-lookup"><span data-stu-id="40364-111">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="40364-112">Создание шаблона</span><span class="sxs-lookup"><span data-stu-id="40364-112">Build the template</span></span>

<span data-ttu-id="40364-113">Чтобы создать шаблон для страницы сообщения об ошибке код состояния, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="40364-113">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="40364-114">Перейдите в пункт **Шаблоны**.</span><span class="sxs-lookup"><span data-stu-id="40364-114">Go to **Templates**.</span></span>
1. <span data-ttu-id="40364-115">Выберите **Создать** для создания шаблона страницы.</span><span class="sxs-lookup"><span data-stu-id="40364-115">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="40364-116">В диалоговом окне **Создать шаблон** в разделе **Имя шаблона** введите имя нового шаблона, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="40364-116">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="40364-117">Создайте шаблон на основе структуры, которую должна иметь страница сообщения об ошибке кода состояния.</span><span class="sxs-lookup"><span data-stu-id="40364-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="40364-118">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="40364-118">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="40364-119">Создание страницы сообщения об ошибке кода состояния</span><span class="sxs-lookup"><span data-stu-id="40364-119">Build the status code error response page</span></span>

<span data-ttu-id="40364-120">Чтобы создать страницу сообщения об ошибке код состояния, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="40364-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="40364-121">Перейти к пункту **Страницы**.</span><span class="sxs-lookup"><span data-stu-id="40364-121">Go to **Pages**.</span></span>
1. <span data-ttu-id="40364-122">Выберите **Создать** для создания страницы.</span><span class="sxs-lookup"><span data-stu-id="40364-122">Select **New** to create a page.</span></span>
1. <span data-ttu-id="40364-123">В диалоговом окне **Выбор шаблона** выберите шаблон, затем в разделе **Имя страницы** введите имя страницы ответа при ошибке с кодом состояния.</span><span class="sxs-lookup"><span data-stu-id="40364-123">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="40364-124">Не заполняйте поле **URL-адрес страницы**.</span><span class="sxs-lookup"><span data-stu-id="40364-124">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="40364-125">Создайте страницу.</span><span class="sxs-lookup"><span data-stu-id="40364-125">Build the page.</span></span>
1. <span data-ttu-id="40364-126">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="40364-126">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="40364-127">Можно создать отдельные страницы сообщений об ошибках кода состояния для ошибок кода состояния 4xx и 5xx.</span><span class="sxs-lookup"><span data-stu-id="40364-127">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="40364-128">В качестве альтернативы можно использовать одну и ту же страницу сообщения об ошибке кода состояния для обеих категорий ошибок.</span><span class="sxs-lookup"><span data-stu-id="40364-128">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="40364-129">Настройка перенаправления для страницы сообщения об ошибке кода состояния</span><span class="sxs-lookup"><span data-stu-id="40364-129">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="40364-130">Чтобы настроить перенаправление для страницы сообщения об ошибке код состояния, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="40364-130">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="40364-131">Перейдите в раздел **URL-адреса \> Создать \> Создать псевдоним** и выберите страницу сообщения об ошибке кода состояния, созданную ранее.</span><span class="sxs-lookup"><span data-stu-id="40364-131">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="40364-132">В поле **Псевдоним** введите **default-4xx** или **default-5xx**, в зависимости от страницы сообщения об ошибке кода состояния, для которой выполняется настройка перенаправления.</span><span class="sxs-lookup"><span data-stu-id="40364-132">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="40364-133">Эти псевдонимы должны быть опубликованы.</span><span class="sxs-lookup"><span data-stu-id="40364-133">These aliases must be published.</span></span> <span data-ttu-id="40364-134">В противном случае перенаправление работать не будет.</span><span class="sxs-lookup"><span data-stu-id="40364-134">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="40364-135">Выберите **ОК**, чтобы подтвердить связывание.</span><span class="sxs-lookup"><span data-stu-id="40364-135">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="40364-136">Если для обеих категорий ошибок используется одна страница сообщения об ошибке кода состояния, повторите эту процедуру, чтобы связать псевдоним для другой категории ошибок с этой же страницей.</span><span class="sxs-lookup"><span data-stu-id="40364-136">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40364-137">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="40364-137">Additional resources</span></span>

[<span data-ttu-id="40364-138">Работа с шаблонами</span><span class="sxs-lookup"><span data-stu-id="40364-138">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="40364-139">Добавление новой страницы сайта</span><span class="sxs-lookup"><span data-stu-id="40364-139">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="40364-140">Создание URL-адреса страницы</span><span class="sxs-lookup"><span data-stu-id="40364-140">Create a page URL</span></span>](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
