---
title: Добавление приветственного сообщения
description: В этом разделе описывается, как добавить приветственное сообщение на веб-сайт Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5910ab85b1b0b2df992a24ad3cf7a032e7b98ea9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980140"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="82a08-103">Добавление приветственного сообщения</span><span class="sxs-lookup"><span data-stu-id="82a08-103">Add a welcome message</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="82a08-104">В этом разделе описывается, как добавить приветственное сообщение на веб-сайт Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="82a08-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="82a08-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="82a08-105">Overview</span></span>

<span data-ttu-id="82a08-106">Приветственное сообщение на веб-сайте электронной коммерции может информировать посетителей о текущих распродажах, обновлениях сайта или доступности сезонных коллекций.</span><span class="sxs-lookup"><span data-stu-id="82a08-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="82a08-107">Приветственное сообщение устанавливается с помощью модуля оповещения.</span><span class="sxs-lookup"><span data-stu-id="82a08-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="82a08-108">Необходимо добавить модуль оповещения в слот **Сообщения об ошибках/информационные сообщения** в фрагменте заголовка.</span><span class="sxs-lookup"><span data-stu-id="82a08-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="82a08-109">Модуль оповещений позволяет указать отображаемый текст, цвет текста и выравнивание.</span><span class="sxs-lookup"><span data-stu-id="82a08-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="82a08-110">Он также позволяет указать, могут ли посетители сайта закрыть сообщение.</span><span class="sxs-lookup"><span data-stu-id="82a08-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="82a08-111">Когда приветственное сообщение добавляется в фрагмент общего заголовка, оно будет отображаться на каждой странице, использующей шаблон, в котором используется этот общий фрагмент заголовка.</span><span class="sxs-lookup"><span data-stu-id="82a08-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="82a08-112">Чтобы добавить приветственное сообщение на сайт, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="82a08-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="82a08-113">В конфигураторе сайта Commerce перейдите на свой сайт.</span><span class="sxs-lookup"><span data-stu-id="82a08-113">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="82a08-114">Выберите **Фрагменты**.</span><span class="sxs-lookup"><span data-stu-id="82a08-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="82a08-115">Выберите фрагмент заголовка, в который добавляется сообщение.</span><span class="sxs-lookup"><span data-stu-id="82a08-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="82a08-116">В дереве структуры разверните узел **Сообщения об ошибках/информационные сообщения**.</span><span class="sxs-lookup"><span data-stu-id="82a08-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="82a08-117">Выберите модуль оповещений, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="82a08-117">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="82a08-118">Если модуль оповещения еще не существует, сначала выберите кнопку с многоточием (**...**) рядом с пунктом **Сообщения об ошибках/информационные сообщения**, затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="82a08-118">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="82a08-119">На панели свойств справа на вкладке **Данные** выберите **Добавить источник данных**, затем выберите **Содержимое**.</span><span class="sxs-lookup"><span data-stu-id="82a08-119">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="82a08-120">В поле **Введите текст** введите текст приветственного сообщения.</span><span class="sxs-lookup"><span data-stu-id="82a08-120">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="82a08-121">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата фрагмента заголовка, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="82a08-121">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="82a08-122">Приветственное сообщение теперь появится в верхней части каждой страницы сайта, использующей выбранный фрагмент заголовка.</span><span class="sxs-lookup"><span data-stu-id="82a08-122">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="82a08-123">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="82a08-123">Additional resources</span></span>

[<span data-ttu-id="82a08-124">Добавление логотипа</span><span class="sxs-lookup"><span data-stu-id="82a08-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="82a08-125">Выбор темы сайта</span><span class="sxs-lookup"><span data-stu-id="82a08-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="82a08-126">Работа с переопределением файлов CSS</span><span class="sxs-lookup"><span data-stu-id="82a08-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="82a08-127">Добавление значка сайта</span><span class="sxs-lookup"><span data-stu-id="82a08-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="82a08-128">Добавление уведомления об авторском праве</span><span class="sxs-lookup"><span data-stu-id="82a08-128">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="82a08-129">Добавление языков на сайт</span><span class="sxs-lookup"><span data-stu-id="82a08-129">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="82a08-130">Добавление кода скрипта на страницы сайта для поддержки телеметрии</span><span class="sxs-lookup"><span data-stu-id="82a08-130">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

