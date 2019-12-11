---
title: Добавление значка сайта
description: В этой теме объясняется, как добавить значок сайта к сайту.
author: bicyclingfool
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 58cb6c592351a96876532ef53d5d477ff93fafa1
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696999"
---
# <a name="add-a-favicon"></a><span data-ttu-id="3df14-103">Добавление значка сайта</span><span class="sxs-lookup"><span data-stu-id="3df14-103">Add a favicon</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="3df14-104">В этой теме объясняется, как добавить значок сайта к сайту.</span><span class="sxs-lookup"><span data-stu-id="3df14-104">This topic explains how to add a favicon to your site.</span></span>

## <a name="overview"></a><span data-ttu-id="3df14-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="3df14-105">Overview</span></span>

<span data-ttu-id="3df14-106">Значок сайта — это небольшой графический файл, который отображается на вкладке веб-браузера, в адресной строке, в журнале просмотра и в закладках или избранном, а также в других местах.</span><span class="sxs-lookup"><span data-stu-id="3df14-106">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="3df14-107">Рекомендуется добавить значок сайта к сайту, так как он представляет и подкрепляет вашу торговую марку и помогает отличать веб-сайт от других сайтов, которые посещает клиент.</span><span class="sxs-lookup"><span data-stu-id="3df14-107">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="3df14-108">Хотя на сайт можно добавлять несколько значков сайта различных размеров и типов файлов, в этом разделе показано, как добавить один значок сайта.</span><span class="sxs-lookup"><span data-stu-id="3df14-108">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="3df14-109">Однако этот же процесс и место используются для добавления дополнительных значков сайта.</span><span class="sxs-lookup"><span data-stu-id="3df14-109">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="3df14-110">Отправка значка сайта в коллекцию активов вашего сайта</span><span class="sxs-lookup"><span data-stu-id="3df14-110">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="3df14-111">Чтобы отправить значок сайта в коллекцию активов вашего сайта, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3df14-111">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="3df14-112">Перейти в раздел **Активы \> Отправить \> Отправить активы**.</span><span class="sxs-lookup"><span data-stu-id="3df14-112">Go to **Assets \> Upload \> Upload assets**.</span></span>
1. <span data-ttu-id="3df14-113">Найдите и выберите значок сайта в локальной файловой системе.</span><span class="sxs-lookup"><span data-stu-id="3df14-113">Find and select the favicon on your local file system.</span></span>
1. <span data-ttu-id="3df14-114">Введите заголовок, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3df14-114">Enter a title, and then select **OK**.</span></span> 
1. <span data-ttu-id="3df14-115">На панели свойств в правой части скопируйте общедоступный URL-адрес значка сайта.</span><span class="sxs-lookup"><span data-stu-id="3df14-115">In the property pane on the right, copy the public URL of the favicon.</span></span>

> [!NOTE]
> <span data-ttu-id="3df14-116">Если не выбран параметр **Опубликовать активы после отправки**, необходимо вернуться в страницу **Активы** и вручную опубликовать значок сайта позже.</span><span class="sxs-lookup"><span data-stu-id="3df14-116">If you don't select the **Publish assets after upload** option, you must return to **Assets** page and manually publish the favicon later.</span></span>

## <a name="create-the-html-for-the-favicon"></a><span data-ttu-id="3df14-117">Создание кода HTML для значка сайта</span><span class="sxs-lookup"><span data-stu-id="3df14-117">Create the HTML for the favicon</span></span>

<span data-ttu-id="3df14-118">Чтобы создать код HTML для значка сайта, используйте следующий фрагмент HTML.</span><span class="sxs-lookup"><span data-stu-id="3df14-118">To create the HTML for the favicon, use the following HTML snippet.</span></span> <span data-ttu-id="3df14-119">Для атрибута **href** замените **"Public\_URL\_for\_your\_favicon"** на общедоступный URL-адрес, который был скопирован ранее.</span><span class="sxs-lookup"><span data-stu-id="3df14-119">For the **href** attribute, replace **"Public\_URL\_for\_your\_favicon"** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a><span data-ttu-id="3df14-120">Добавление HTML-кода для значка сайта в элемент \<головной\> ваших страниц</span><span class="sxs-lookup"><span data-stu-id="3df14-120">Add the HTML for the favicon to the \<head\> element of your pages</span></span>

<span data-ttu-id="3df14-121">Чтобы добавить значок сайта на сайт, используйте ту же процедуру, которая используется для добавления любого типа HTML или сценариев в элемент **\<head\>** страниц сайта.</span><span class="sxs-lookup"><span data-stu-id="3df14-121">To add a favicon to your site, use the same procedure that is used to add any type of HTML or script to the **\<head\>** element of your site pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3df14-122">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3df14-122">Additional resources</span></span>

[<span data-ttu-id="3df14-123">Добавление логотипа</span><span class="sxs-lookup"><span data-stu-id="3df14-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="3df14-124">Выбор темы сайта</span><span class="sxs-lookup"><span data-stu-id="3df14-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="3df14-125">Добавление приветственного сообщения</span><span class="sxs-lookup"><span data-stu-id="3df14-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="3df14-126">Добавление уведомления об авторском праве</span><span class="sxs-lookup"><span data-stu-id="3df14-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="3df14-127">Добавление языков на сайт</span><span class="sxs-lookup"><span data-stu-id="3df14-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="3df14-128">Добавление кода скрипта на страницы сайта для поддержки телеметрии</span><span class="sxs-lookup"><span data-stu-id="3df14-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

