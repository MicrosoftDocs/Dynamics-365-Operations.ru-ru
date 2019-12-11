---
title: Способы добавления содержимого
description: В этом разделе содержатся сведения о добавлении и управлении содержимым на вашем сайте Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3d91235837aee9ad06466ffe47727b435e39094f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770536"
---
# <a name="ways-to-add-content"></a><span data-ttu-id="01652-103">Способы добавления содержимого</span><span class="sxs-lookup"><span data-stu-id="01652-103">Ways to add content</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="01652-104">В этом разделе содержатся сведения о добавлении и управлении содержимым на вашем сайте Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="01652-104">This topic provides information about how to add and manage content on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="01652-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="01652-105">Overview</span></span>

<span data-ttu-id="01652-106">Есть много способов изменить вид, поведение и содержание сайта.</span><span class="sxs-lookup"><span data-stu-id="01652-106">There are many ways to change the look, feel, and content of your site.</span></span> <span data-ttu-id="01652-107">В зависимости от требуемого уровня настройки, многие из этих изменений могут быть реализованы пользователями, не являющимися разработчиками.</span><span class="sxs-lookup"><span data-stu-id="01652-107">Depending on the required level of customization, many of these changes can be implemented by non-developers.</span></span> <span data-ttu-id="01652-108">Например, не требуется писать код для создания шаблонов, выбора тем, а также выбора и настройки модулей.</span><span class="sxs-lookup"><span data-stu-id="01652-108">For example, no code has to be written to build templates, select themes, and select and configure modules.</span></span> <span data-ttu-id="01652-109">С другой стороны, навыки разработки необходимы для создания новой темы или модуля, так как необходимо использовать пакет средств разработки программного обеспечения (SDK) электронной коммерции и рабочий процесс развертывания Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="01652-109">By contrast, development skills are required to create a new theme or module, because the e-Commerce software development kit (SDK) and the Microsoft Dynamics Lifecycle Services (LCS) deployment workflow must be used.</span></span>

<span data-ttu-id="01652-110">В следующих разделах содержатся подробные сведения о добавлении и управлении содержимым сайта.</span><span class="sxs-lookup"><span data-stu-id="01652-110">The following topics provide detailed information about how to add and manage site content.</span></span> <span data-ttu-id="01652-111">Они фокусируются на областях узла, которым не требуется разработчик.</span><span class="sxs-lookup"><span data-stu-id="01652-111">They focus on areas of your site that don't require a developer.</span></span> <span data-ttu-id="01652-112">При необходимости они указывают задачи, требующие работы с пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="01652-112">As required, they point out tasks that require SDK work.</span></span>

- <span data-ttu-id="01652-113">Чтобы изменить текст, изображения или видео на существующей странице сайта, см. раздел [Работа с модулями](work-with-modules.md).</span><span class="sxs-lookup"><span data-stu-id="01652-113">To change the text, images, or video on an existing site page, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="01652-114">Для обеспечения защищенной от ошибок разработки веб-содержимого в соответствии с требования торговой марки см. раздел [Работа с шаблонами](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="01652-114">To help guarantee a foolproof, on-brand authoring experience for web content authors, see [Work with templates](work-with-templates.md).</span></span>
- <span data-ttu-id="01652-115">Чтобы изменить расположение разделов на странице сайта, см. раздел [Работа с макетами](work-with-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="01652-115">To rearrange sections on a site page, see [Work with layouts](work-with-layouts.md).</span></span>
- <span data-ttu-id="01652-116">Чтобы изменить шрифты, цвета и общий вид страниц сайта, см. раздел [Выбор темы сайта](select-site-theme.md).</span><span class="sxs-lookup"><span data-stu-id="01652-116">To change the fonts, colors, and general look of site pages, see [Select a site theme](select-site-theme.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="01652-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="01652-117">Additional resources</span></span>

[<span data-ttu-id="01652-118">Глоссарий модели страниц</span><span class="sxs-lookup"><span data-stu-id="01652-118">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="01652-119">Состояния и жизненный цикл документа</span><span class="sxs-lookup"><span data-stu-id="01652-119">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="01652-120">Работа с модулями</span><span class="sxs-lookup"><span data-stu-id="01652-120">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="01652-121">Работа с фрагментами</span><span class="sxs-lookup"><span data-stu-id="01652-121">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="01652-122">Обзор шаблонов и макетов</span><span class="sxs-lookup"><span data-stu-id="01652-122">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="01652-123">Настройка навигации по сайту</span><span class="sxs-lookup"><span data-stu-id="01652-123">Customize site navigation</span></span>](customize-site-navigation.md)
