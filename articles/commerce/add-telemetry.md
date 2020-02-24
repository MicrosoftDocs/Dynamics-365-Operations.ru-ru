---
title: Добавление кода скрипта на страницы сайта для поддержки телеметрии
description: В этом разделе описывается добавление клиентского кода скрипта на страницы сайта для поддержки сбора телеметрии на стороне клиента.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 674d00faf1b30f87a0b0062129e1b9fbff955dd4
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001285"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="ae60f-103">Добавление кода скрипта на страницы сайта для поддержки телеметрии</span><span class="sxs-lookup"><span data-stu-id="ae60f-103">Add script code to site pages to support telemetry</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ae60f-104">В этом разделе описывается добавление клиентского кода скрипта на страницы сайта для поддержки сбора телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="ae60f-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="ae60f-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="ae60f-105">Overview</span></span>

<span data-ttu-id="ae60f-106">Веб-аналитика является важным средством, когда необходимо понять, как клиенты взаимодействуют с вашим сайтом, и принимать решения, которые помогут оптимизировать работу по максимальной конверсии.</span><span class="sxs-lookup"><span data-stu-id="ae60f-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="ae60f-107">Доступно множество пакетов веб-аналитики, которые помогут достичь этих целей, такие как Google Analytics, Click, Moz Analytics и KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="ae60f-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="ae60f-108">Для большинства пакетов веб-аналитики требуется добавить клиентский код сценария в элемент **\<head\>** кода HTML для всех страниц сайта.</span><span class="sxs-lookup"><span data-stu-id="ae60f-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="ae60f-109">Инструкции, приведенные в этом разделе, применимы также к другим пользовательским функциям на стороне клиента, которые Microsoft Dynamics 365 Commerce изначально не предлагает.</span><span class="sxs-lookup"><span data-stu-id="ae60f-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="ae60f-110">Создание повторно используемого фрагмента кода сценария</span><span class="sxs-lookup"><span data-stu-id="ae60f-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="ae60f-111">После создания фрагмента для кода сценария его можно повторно использовать на всех страницах сайта.</span><span class="sxs-lookup"><span data-stu-id="ae60f-111">After you create a fragment for your script code, it can be reused across all pages on your site.</span></span>

1. <span data-ttu-id="ae60f-112">Перейдите к пункту **Фрагменты \> Создать фрагмент страницы**.</span><span class="sxs-lookup"><span data-stu-id="ae60f-112">Go to **Fragments \> New page fragment**.</span></span>
2. <span data-ttu-id="ae60f-113">Выберите **Внешний сценарий**, введите имя для фрагмента, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ae60f-113">Select **External Script**, enter a name for the fragment, and then select **OK**.</span></span>
3. <span data-ttu-id="ae60f-114">В иерархии фрагментов выберите дочерний модуль **средство введения сценария** только что созданного фрагмента.</span><span class="sxs-lookup"><span data-stu-id="ae60f-114">In the fragment hierarchy, select the **script injector** module child of the fragment that you just created.</span></span>
4. <span data-ttu-id="ae60f-115">В правой панели свойств добавьте клиентский сценарий и задайте другие параметры настройки, как требуется.</span><span class="sxs-lookup"><span data-stu-id="ae60f-115">In the property pane on the right, add your client-side script, and set other configuration options as you require.</span></span>

## <a name="add-the-fragment-to-templates"></a><span data-ttu-id="ae60f-116">Добавление фрагмента к шаблонам</span><span class="sxs-lookup"><span data-stu-id="ae60f-116">Add the fragment to templates</span></span>

1. <span data-ttu-id="ae60f-117">Перейдите к разделу **Шаблоны** и откройте шаблон для страниц, к которым необходимо добавить код сценария.</span><span class="sxs-lookup"><span data-stu-id="ae60f-117">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
2. <span data-ttu-id="ae60f-118">В левой области разверните иерархию шаблонов, чтобы отобразить слот **Заголовок HTML**.</span><span class="sxs-lookup"><span data-stu-id="ae60f-118">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
3. <span data-ttu-id="ae60f-119">Нажмите кнопку с многоточием (**...**) для слота **Заголовок**, затем выберите **Добавить фрагмент**.</span><span class="sxs-lookup"><span data-stu-id="ae60f-119">Select the ellipsis button (**...**) for the **HTML Head** slot, and then select **Add fragment**.</span></span>
4. <span data-ttu-id="ae60f-120">Выберите фрагмент, который был создан для кода сценария.</span><span class="sxs-lookup"><span data-stu-id="ae60f-120">Select the fragment that you created for your script code.</span></span>
5. <span data-ttu-id="ae60f-121">Сохраните шаблон и верните его.</span><span class="sxs-lookup"><span data-stu-id="ae60f-121">Save the template, and check it in.</span></span>

> [!NOTE]
> <span data-ttu-id="ae60f-122">После завершения необходимо опубликовать фрагмент и главный шаблон.</span><span class="sxs-lookup"><span data-stu-id="ae60f-122">After you've finished, you must publish the fragment and the master template.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="ae60f-123">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ae60f-123">Additional resources</span></span>

[<span data-ttu-id="ae60f-124">Добавление логотипа</span><span class="sxs-lookup"><span data-stu-id="ae60f-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="ae60f-125">Выбор темы сайта</span><span class="sxs-lookup"><span data-stu-id="ae60f-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="ae60f-126">Работа с переопределением файлов CSS</span><span class="sxs-lookup"><span data-stu-id="ae60f-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="ae60f-127">Добавление значка сайта</span><span class="sxs-lookup"><span data-stu-id="ae60f-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="ae60f-128">Добавление приветственного сообщения</span><span class="sxs-lookup"><span data-stu-id="ae60f-128">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="ae60f-129">Добавление уведомления об авторском праве</span><span class="sxs-lookup"><span data-stu-id="ae60f-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="ae60f-130">Добавление языков на сайт</span><span class="sxs-lookup"><span data-stu-id="ae60f-130">Add languages to your site</span></span>](add-languages-to-site.md)

