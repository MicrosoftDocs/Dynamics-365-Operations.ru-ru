---
title: Добавление приветственного сообщения
description: В этом разделе описывается, как добавить приветственное сообщение на веб-сайт Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e61f43eca7d1343d020e1c01b5b1140f07b63c6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797391"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="e3b5b-103">Добавление приветственного сообщения</span><span class="sxs-lookup"><span data-stu-id="e3b5b-103">Add a welcome message</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e3b5b-104">В этом разделе описывается, как добавить приветственное сообщение на веб-сайт Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

<span data-ttu-id="e3b5b-105">Приветственное сообщение на веб-сайте электронной коммерции может информировать посетителей о текущих распродажах, обновлениях сайта или доступности сезонных коллекций.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-105">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="e3b5b-106">Приветственное сообщение устанавливается с помощью модуля оповещения.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-106">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="e3b5b-107">Необходимо добавить модуль оповещения в слот **Сообщения об ошибках/информационные сообщения** в фрагменте заголовка.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-107">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="e3b5b-108">Модуль оповещений позволяет указать отображаемый текст, цвет текста и выравнивание.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-108">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="e3b5b-109">Он также позволяет указать, могут ли посетители сайта закрыть сообщение.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-109">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="e3b5b-110">Когда приветственное сообщение добавляется в фрагмент общего заголовка, оно будет отображаться на каждой странице, использующей шаблон, в котором используется этот общий фрагмент заголовка.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-110">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="e3b5b-111">Чтобы добавить приветственное сообщение на сайт, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-111">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="e3b5b-112">В конфигураторе сайта Commerce перейдите на свой сайт.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-112">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="e3b5b-113">Выберите **Фрагменты**.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-113">Select **Fragments**.</span></span>
1. <span data-ttu-id="e3b5b-114">Выберите фрагмент заголовка, в который добавляется сообщение.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-114">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="e3b5b-115">В дереве структуры разверните узел **Сообщения об ошибках/информационные сообщения**.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-115">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="e3b5b-116">Выберите модуль оповещений, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-116">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="e3b5b-117">Если модуль оповещения еще не существует, сначала выберите кнопку с многоточием (**...**) рядом с пунктом **Сообщения об ошибках/информационные сообщения**, затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-117">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="e3b5b-118">На панели свойств справа на вкладке **Данные** выберите **Добавить источник данных**, затем выберите **Содержимое**.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-118">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="e3b5b-119">В поле **Введите текст** введите текст приветственного сообщения.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-119">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="e3b5b-120">Выберите **Сохранить**, выберите **Завершить редактирование** для возврата фрагмента заголовка, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-120">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="e3b5b-121">Приветственное сообщение теперь появится в верхней части каждой страницы сайта, использующей выбранный фрагмент заголовка.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-121">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e3b5b-122">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e3b5b-122">Additional resources</span></span>

[<span data-ttu-id="e3b5b-123">Добавление логотипа</span><span class="sxs-lookup"><span data-stu-id="e3b5b-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="e3b5b-124">Выбор темы сайта</span><span class="sxs-lookup"><span data-stu-id="e3b5b-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="e3b5b-125">Работа с переопределением файлов CSS</span><span class="sxs-lookup"><span data-stu-id="e3b5b-125">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="e3b5b-126">Добавление значка сайта</span><span class="sxs-lookup"><span data-stu-id="e3b5b-126">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="e3b5b-127">Добавление уведомления об авторском праве</span><span class="sxs-lookup"><span data-stu-id="e3b5b-127">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="e3b5b-128">Добавление языков на сайт</span><span class="sxs-lookup"><span data-stu-id="e3b5b-128">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="e3b5b-129">Добавление кода скрипта на страницы сайта для поддержки телеметрии</span><span class="sxs-lookup"><span data-stu-id="e3b5b-129">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
