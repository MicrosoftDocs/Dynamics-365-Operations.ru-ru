---
title: Добавление уведомления об авторском праве
description: В этом разделе описывается, как добавить уведомление об авторском праве на веб-сайт электронной коммерции.
author: psimolin
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a2ed52dbd19508e07fcced92a7fad831180b1d1d
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269598"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="b1f67-103">Добавление уведомления об авторском праве</span><span class="sxs-lookup"><span data-stu-id="b1f67-103">Add a copyright notice</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b1f67-104">В этом разделе описывается, как добавить уведомление об авторском праве на веб-сайт электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="b1f67-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b1f67-105">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="b1f67-105">Prerequisites</span></span>

<span data-ttu-id="b1f67-106">Перед добавлением уведомления об авторском праве на сайт необходимо иметь следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="b1f67-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="b1f67-107">Шаблон, содержащий общий фрагмент нижнего колонтитула.</span><span class="sxs-lookup"><span data-stu-id="b1f67-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="b1f67-108">Страница, использующая этот шаблон.</span><span class="sxs-lookup"><span data-stu-id="b1f67-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="b1f67-109">Добавление уведомления об авторском праве</span><span class="sxs-lookup"><span data-stu-id="b1f67-109">Add a copyright notice</span></span>

<span data-ttu-id="b1f67-110">Чтобы добавить уведомление об авторских правах в нижнюю часть каждой страницы, использующей конкретный шаблон, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b1f67-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="b1f67-111">Перейдите к разделу **Фрагменты**, затем выберите **Создать фрагмент страницы**.</span><span class="sxs-lookup"><span data-stu-id="b1f67-111">Go to **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="b1f67-112">В диалоговом окне выберите модуль **Нижний колонтитул** и название фрагмента.</span><span class="sxs-lookup"><span data-stu-id="b1f67-112">In the dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="b1f67-113">Например, введите **Нижний колонтитул-авторские права**.</span><span class="sxs-lookup"><span data-stu-id="b1f67-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="b1f67-114">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b1f67-114">Select **OK**.</span></span>
1. <span data-ttu-id="b1f67-115">В области переходов выберите кнопку с многоточием (**...**) рядом с пунктом **Нижний колонтитул**, затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="b1f67-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="b1f67-116">В диалоговом окне выберите **Категория нижнего колонтитула**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b1f67-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="b1f67-117">В области переходов выберите кнопку с многоточием рядом с пунктом **Категория нижнего колонтитула**, затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="b1f67-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="b1f67-118">В диалоговом окне выберите **Блок текста**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b1f67-118">In the dialog box, select **Text block**, and then select **OK**.</span></span>
1. <span data-ttu-id="b1f67-119">В области переходов выберите **Блок текста**.</span><span class="sxs-lookup"><span data-stu-id="b1f67-119">In the navigation pane, select **Text block**.</span></span>
1. <span data-ttu-id="b1f67-120">В области свойств справа в поле **Абзац** добавьте сообщение об авторском праве.</span><span class="sxs-lookup"><span data-stu-id="b1f67-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="b1f67-121">Например, введите **(C) Fabrikam 2019**.</span><span class="sxs-lookup"><span data-stu-id="b1f67-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="b1f67-122">Выберите **Сохранить**, выберите **Завершить правку**, затем выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="b1f67-122">Select **Save**, select **Finish editing**, and then select **Publish**.</span></span>
1. <span data-ttu-id="b1f67-123">Перейдите к пункту **Шаблоны**, выберите шаблон, затем выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="b1f67-123">Go to **Templates**, select the template, and then select **Edit**.</span></span>
1. <span data-ttu-id="b1f67-124">В разделе **Структура страницы** разверните **Основной текст**, затем разверните пункт **Страница по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="b1f67-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="b1f67-125">Нажмите кнопку с многоточием рядом в пунктом **Слот нижнего колонтитула**, затем выберите **Добавить фрагмент**.</span><span class="sxs-lookup"><span data-stu-id="b1f67-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="b1f67-126">Выберите созданный ранее фрагмент, затем выберите **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="b1f67-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="b1f67-127">Выберите **Завершить редактирование** для возврата шаблона, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="b1f67-127">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="b1f67-128">Нижний колонтитул, содержащий уведомление об авторском праве, автоматически появляется внизу всех страниц, использующих выбранный шаблон.</span><span class="sxs-lookup"><span data-stu-id="b1f67-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1f67-129">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b1f67-129">Additional resources</span></span>

[<span data-ttu-id="b1f67-130">Добавление логотипа</span><span class="sxs-lookup"><span data-stu-id="b1f67-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="b1f67-131">Выбор темы сайта</span><span class="sxs-lookup"><span data-stu-id="b1f67-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="b1f67-132">Работа с переопределением файлов CSS</span><span class="sxs-lookup"><span data-stu-id="b1f67-132">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="b1f67-133">Добавление значка сайта</span><span class="sxs-lookup"><span data-stu-id="b1f67-133">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="b1f67-134">Добавление приветственного сообщения</span><span class="sxs-lookup"><span data-stu-id="b1f67-134">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="b1f67-135">Добавление языков на сайт</span><span class="sxs-lookup"><span data-stu-id="b1f67-135">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="b1f67-136">Добавление кода скрипта на страницы сайта для поддержки телеметрии</span><span class="sxs-lookup"><span data-stu-id="b1f67-136">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

