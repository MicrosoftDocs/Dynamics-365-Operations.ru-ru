---
title: Добавление приветственного сообщения
description: В этом разделе описывается, как добавить приветственное сообщение на веб-сайт Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: ca10b01268b5dcd4c6fe448d90cd0ebd65a2673b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001262"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="dfc0b-103">Добавление приветственного сообщения</span><span class="sxs-lookup"><span data-stu-id="dfc0b-103">Add a welcome message</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="dfc0b-104">В этом разделе описывается, как добавить приветственное сообщение на веб-сайт Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dfc0b-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="dfc0b-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="dfc0b-105">Overview</span></span>

<span data-ttu-id="dfc0b-106">Приветственное сообщение на веб-сайте электронной коммерции может информировать посетителей о текущих распродажах, обновлениях сайта или доступности сезонных коллекций.</span><span class="sxs-lookup"><span data-stu-id="dfc0b-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="dfc0b-107">Приветственное сообщение устанавливается с помощью модуля оповещения.</span><span class="sxs-lookup"><span data-stu-id="dfc0b-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="dfc0b-108">Необходимо добавить модуль оповещения в слот **Сообщения об ошибках/информационные сообщения** в фрагменте заголовка.</span><span class="sxs-lookup"><span data-stu-id="dfc0b-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="dfc0b-109">Модуль оповещений позволяет указать отображаемый текст, цвет текста и выравнивание.</span><span class="sxs-lookup"><span data-stu-id="dfc0b-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="dfc0b-110">Он также позволяет указать, могут ли посетители сайта закрыть сообщение.</span><span class="sxs-lookup"><span data-stu-id="dfc0b-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="dfc0b-111">Когда приветственное сообщение добавляется в фрагмент общего заголовка, оно будет отображаться на каждой странице, использующей шаблон, в котором используется этот общий фрагмент заголовка.</span><span class="sxs-lookup"><span data-stu-id="dfc0b-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="dfc0b-112">Чтобы добавить приветственное сообщение на сайт, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="dfc0b-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="dfc0b-113">В Dynamics 365 Commerce перейдите на сайт.</span><span class="sxs-lookup"><span data-stu-id="dfc0b-113">In Dynamics 365 Commerce, go to your site.</span></span>
1. <span data-ttu-id="dfc0b-114">Выберите **Фрагменты**.</span><span class="sxs-lookup"><span data-stu-id="dfc0b-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="dfc0b-115">Выберите фрагмент заголовка, в который добавляется сообщение.</span><span class="sxs-lookup"><span data-stu-id="dfc0b-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="dfc0b-116">В дереве структуры разверните узел **Сообщения об ошибках/информационные сообщения**.</span><span class="sxs-lookup"><span data-stu-id="dfc0b-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="dfc0b-117">Выберите модуль оповещений.</span><span class="sxs-lookup"><span data-stu-id="dfc0b-117">Select the alert module.</span></span>

    <span data-ttu-id="dfc0b-118">Если модуль оповещения еще не существует, нажмите кнопку с многоточием (**...**) рядом с пунктом **Сообщения об ошибках/информационные сообщения**, затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="dfc0b-118">If an alert module doesn't yet exist, select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span> <span data-ttu-id="dfc0b-119">Выберите модуль оповещений, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="dfc0b-119">Select the alert module, and then select **OK**.</span></span>

1. <span data-ttu-id="dfc0b-120">На панели свойств справа на вкладке **Данные** выберите **Добавить источник данных**, затем выберите **Содержимое**.</span><span class="sxs-lookup"><span data-stu-id="dfc0b-120">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="dfc0b-121">В поле **Введите текст** введите текст приветственного сообщения.</span><span class="sxs-lookup"><span data-stu-id="dfc0b-121">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="dfc0b-122">Сохраните фрагмент заголовка, верните его и опубликуйте.</span><span class="sxs-lookup"><span data-stu-id="dfc0b-122">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="dfc0b-123">Приветственное сообщение теперь появится в верхней части каждой страницы сайта, использующей выбранный фрагмент заголовка.</span><span class="sxs-lookup"><span data-stu-id="dfc0b-123">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dfc0b-124">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dfc0b-124">Additional resources</span></span>

[<span data-ttu-id="dfc0b-125">Добавление логотипа</span><span class="sxs-lookup"><span data-stu-id="dfc0b-125">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="dfc0b-126">Выбор темы сайта</span><span class="sxs-lookup"><span data-stu-id="dfc0b-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="dfc0b-127">Работа с переопределением файлов CSS</span><span class="sxs-lookup"><span data-stu-id="dfc0b-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="dfc0b-128">Добавление значка сайта</span><span class="sxs-lookup"><span data-stu-id="dfc0b-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="dfc0b-129">Добавление уведомления об авторском праве</span><span class="sxs-lookup"><span data-stu-id="dfc0b-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="dfc0b-130">Добавление языков на сайт</span><span class="sxs-lookup"><span data-stu-id="dfc0b-130">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="dfc0b-131">Добавление кода скрипта на страницы сайта для поддержки телеметрии</span><span class="sxs-lookup"><span data-stu-id="dfc0b-131">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

