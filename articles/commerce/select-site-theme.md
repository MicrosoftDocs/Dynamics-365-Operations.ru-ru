---
title: Выбор темы сайта
description: В этом разделе описывается, как задать или изменить тему сайта в Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c54a3e9471fdeb56f27fe7c567c7cd7f0b7fd218
ms.sourcegitcommit: 2ef23dcd4e42362186b9951e675010d97d55c6bd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4556437"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="98c34-103">Выбор темы сайта</span><span class="sxs-lookup"><span data-stu-id="98c34-103">Select a site theme</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="98c34-104">В этом разделе описывается, как задать или изменить тему сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="98c34-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="98c34-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="98c34-105">Overview</span></span>

<span data-ttu-id="98c34-106">Макет и стиль сайта (например, шрифты, размеры и цвета) определяются темой, которая выбрана и применена для сайта.</span><span class="sxs-lookup"><span data-stu-id="98c34-106">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="98c34-107">Тема создается и развертывается разработчиком в компании.</span><span class="sxs-lookup"><span data-stu-id="98c34-107">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="98c34-108">Обзор тем см. в разделе [Обзор тем](e-commerce-extensibility/theming.md).</span><span class="sxs-lookup"><span data-stu-id="98c34-108">For an overview of themes, see [Theming overview](e-commerce-extensibility/theming.md).</span></span> <span data-ttu-id="98c34-109">Дополнительные сведения о создании и развертывание тем см. в разделе [Создание новой темы](e-commerce-extensibility/create-theme.md).</span><span class="sxs-lookup"><span data-stu-id="98c34-109">For more information about how to create and deploy themes, see [Create a new theme](e-commerce-extensibility/create-theme.md).</span></span>

<span data-ttu-id="98c34-110">По умолчанию при первом создании сайта используется тема, которая называется **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="98c34-110">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="98c34-111">Эта тема по умолчанию предоставляется в составе библиотеки модулей Commerce.</span><span class="sxs-lookup"><span data-stu-id="98c34-111">This default theme is provided as part of the Commerce module library.</span></span> <span data-ttu-id="98c34-112">После развертывания дополнительных тем для сайта можно настроить сайт так, чтобы он использовал одну из них.</span><span class="sxs-lookup"><span data-stu-id="98c34-112">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="98c34-113">Выбор темы сайта</span><span class="sxs-lookup"><span data-stu-id="98c34-113">Select the site theme</span></span>

<span data-ttu-id="98c34-114">Чтобы выбрать тему, применяемую к сайту, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="98c34-114">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="98c34-115">В среде разработки сайтов перейдите на ваш сайт.</span><span class="sxs-lookup"><span data-stu-id="98c34-115">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="98c34-116">Перейдите к пункту **Управление сайтом** \> **Расширяемость**.</span><span class="sxs-lookup"><span data-stu-id="98c34-116">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="98c34-117">В области **Тема** выберите тему в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="98c34-117">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="98c34-118">Чтобы применить выбранную тему к сайту, выберите **Сохранить и опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="98c34-118">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="98c34-119">Выбранная тема будет опубликована на сайте сразу после выбора пункта **Сохранить и опубликовать** на странице **Расширяемость**.</span><span class="sxs-lookup"><span data-stu-id="98c34-119">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="98c34-120">Чтобы предварительно просмотреть тему на сайте до ее применения, можно использовать среду разработки или песочницы.</span><span class="sxs-lookup"><span data-stu-id="98c34-120">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98c34-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="98c34-121">Additional resources</span></span>

[<span data-ttu-id="98c34-122">Добавление логотипа</span><span class="sxs-lookup"><span data-stu-id="98c34-122">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="98c34-123">Работа с переопределением файлов CSS</span><span class="sxs-lookup"><span data-stu-id="98c34-123">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="98c34-124">Добавление значка сайта</span><span class="sxs-lookup"><span data-stu-id="98c34-124">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="98c34-125">Добавление приветственного сообщения</span><span class="sxs-lookup"><span data-stu-id="98c34-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="98c34-126">Добавление уведомления об авторском праве</span><span class="sxs-lookup"><span data-stu-id="98c34-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="98c34-127">Добавление языков на сайт</span><span class="sxs-lookup"><span data-stu-id="98c34-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="98c34-128">Добавление кода скрипта на страницы сайта для поддержки телеметрии</span><span class="sxs-lookup"><span data-stu-id="98c34-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="98c34-129">Обзор тематического оформления</span><span class="sxs-lookup"><span data-stu-id="98c34-129">Theming overview</span></span>](e-commerce-extensibility/theming.md)

[<span data-ttu-id="98c34-130">Создание новой темы</span><span class="sxs-lookup"><span data-stu-id="98c34-130">Create a new theme</span></span>](e-commerce-extensibility/create-theme.md)

