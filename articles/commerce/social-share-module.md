---
title: Модуль предоставления общего доступа через социальные сети
description: В этом разделе описываются модули предоставления общего доступа через социальные сети, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 0fd81aa1f4b1358528f0135c1334dc7b4ac4461f
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761419"
---
# <a name="social-share-module"></a><span data-ttu-id="2fdc6-103">Модуль предоставления общего доступа через социальные сети</span><span class="sxs-lookup"><span data-stu-id="2fdc6-103">Social share module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="2fdc6-104">В этом разделе описываются модули предоставления общего доступа через социальные сети, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2fdc6-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="2fdc6-105">Overview</span></span>

<span data-ttu-id="2fdc6-106">Модули предоставления общего доступа через социальные сети позволяют пользователям совместно использовать URL-адреса страниц сайта электронной коммерции в социальных сетях, таких как Facebook, Twitter, Pinterest и LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-106">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="2fdc6-107">URL-адреса страниц сайтов также могут использоваться совместно с помощью электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-107">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="2fdc6-108">Модули предоставления общего доступа через социальные сети обычно используются на страницах сведений о продуктах (PDP), чтобы помочь пользователям совместно использовать сведения о продукте.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-108">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="2fdc6-109">Каждый модуль предоставления общего доступа через социальные сети является контейнером для модулей предоставления общего доступа к номенклатурам в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-109">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="2fdc6-110">Каждый модуль предоставления общего доступа к номенклатуре в социальных сетях можно настроить так, чтобы он указывал на конкретный сайт социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-110">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="2fdc6-111">Интеграция с Facebook, Twitter, Pinterest, LinkedIn и электронной почтой поддерживается стандартно.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-111">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="2fdc6-112">Когда пользователь сайта выбирает символ социальных сетей, для соответствующего сайта социальных сетей запускается HTML-окно iFrame.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-112">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="2fdc6-113">В окне iFrame пользователь может входить в систему и публиковать просматриваемое им содержимое.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-113">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="2fdc6-114">На каждой платформе социальных сетей могут отслеживаться файлы cookie, поэтому для этого модуля необходимо, чтобы пользователи сайта приняли сообщение с уведомлением о согласии на получение файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-114">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="2fdc6-115">Если согласие не файлы cookie не принимается, модуль будет скрыт на странице.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-115">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="2fdc6-116">Дополнительные сведения см. в разделе [Соответствие файлов cookie](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="2fdc6-116">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="2fdc6-117">На следующем рисунке показан пример модуля предоставления общего доступа в социальных сетях, используемого на странице сведений о продукте.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-117">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![Пример модуля предоставления общего доступа в социальных сетях](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="2fdc6-119">Свойства модуля предоставления общего доступа в социальных сетях</span><span class="sxs-lookup"><span data-stu-id="2fdc6-119">Social share module properties</span></span>

| <span data-ttu-id="2fdc6-120">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="2fdc6-120">Property name</span></span>             | <span data-ttu-id="2fdc6-121">значение</span><span class="sxs-lookup"><span data-stu-id="2fdc6-121">Value</span></span>                 | <span data-ttu-id="2fdc6-122">описание</span><span class="sxs-lookup"><span data-stu-id="2fdc6-122">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="2fdc6-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2fdc6-123">Caption</span></span>                  | <span data-ttu-id="2fdc6-124">Текст</span><span class="sxs-lookup"><span data-stu-id="2fdc6-124">Text</span></span> | <span data-ttu-id="2fdc6-125">Это свойство задает подпись для модуля.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-125">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="2fdc6-126">Ориентация</span><span class="sxs-lookup"><span data-stu-id="2fdc6-126">Orientation</span></span> | <span data-ttu-id="2fdc6-127">**Горизонтальная** или **Вертикальная**</span><span class="sxs-lookup"><span data-stu-id="2fdc6-127">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="2fdc6-128">Это свойство определяет ориентацию макета для элементов социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-128">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="2fdc6-129">Свойства модуля элементов предоставления общего доступа в социальных сетях</span><span class="sxs-lookup"><span data-stu-id="2fdc6-129">Social share item module properties</span></span>
| <span data-ttu-id="2fdc6-130">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="2fdc6-130">Property name</span></span>             | <span data-ttu-id="2fdc6-131">значение</span><span class="sxs-lookup"><span data-stu-id="2fdc6-131">Value</span></span>                 | <span data-ttu-id="2fdc6-132">описание</span><span class="sxs-lookup"><span data-stu-id="2fdc6-132">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="2fdc6-133">Социальные сети</span><span class="sxs-lookup"><span data-stu-id="2fdc6-133">Social media</span></span>              | <span data-ttu-id="2fdc6-134">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Почта**</span><span class="sxs-lookup"><span data-stu-id="2fdc6-134">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span></span> | <span data-ttu-id="2fdc6-135">Раскрывающееся меню со списком платформ социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-135">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="2fdc6-136">Значок</span><span class="sxs-lookup"><span data-stu-id="2fdc6-136">Icon</span></span> |<span data-ttu-id="2fdc6-137">Изображение</span><span class="sxs-lookup"><span data-stu-id="2fdc6-137">Image</span></span>    | <span data-ttu-id="2fdc6-138">Это будет изображение, которое будет отображаться для соответствующей социальной сети.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-138">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="2fdc6-139">Рекомендуется обращаться к пакету SDK платформы социальных сетей для получения рекомендуемого изображения, используемого для каждой платформы.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-139">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="2fdc6-140">Добавление модуля предоставления общего доступа в социальных сетях в модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="2fdc6-140">Add a social share module to a buy box module</span></span>

<span data-ttu-id="2fdc6-141">Чтобы добавить модуль предоставления общего доступа в социальных сетях в модуль поля покупки, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-141">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="2fdc6-142">На сайте Fabrikam выберите **Страницы**, затем выберите страницу **DefaultPDP**, чтобы открыть страницу сведений о продукте.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-142">In the Fabrikam site, select **Pages**, and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="2fdc6-143">В ячейке **Поле покупки (обязательно)** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-143">In the **Buybox (required)** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2fdc6-144">В диалоговом окне **Добавить модуль** выберите модуль **Общий доступ в социальных сетях**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-144">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2fdc6-145">В ячейке **Общий доступ в социальных сетях** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-145">In the **Social Share** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2fdc6-146">В диалоговом окне **Добавить модуль** выберите модуль **SocialShare**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-146">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2fdc6-147">В области свойств модуля **SocialShare** в разделе **Ориентация** выберите **Горизонтальная**.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-147">In the properties pane of the **SocialShare** module, under **Orientation**, select **Horizontal**.</span></span> <span data-ttu-id="2fdc6-148">При необходимости добавьте подпись.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-148">Add a caption as needed.</span></span>
1. <span data-ttu-id="2fdc6-149">В ячейке **SocialShare** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-149">In the **SocialShare** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2fdc6-150">В диалоговом окне **Добавить модуль** выберите модуль **SocialShareItem**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-150">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2fdc6-151">В области свойств модуля **SocialShareItem** в разделе **Социальная сеть** выберите **Facebook**.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-151">In the properties pane of the **SocialShareItem** module, under **Social Media**, select **Facebook**.</span></span>
1. <span data-ttu-id="2fdc6-152">В области свойств модуля **SocialShareItem** в разделе **Значок** выберите **+ Добавить изображение**.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-152">In the properties pane of the **SocialShareItem** module, under **Icon**, select **+ Add an image**.</span></span>
1. <span data-ttu-id="2fdc6-153">В диалоговом окне **Выбор мультимедиа** выберите изображение логотипа Facebook, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-153">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="2fdc6-154">Если изображение логотипа Facebook отсутствует, выберите **Отправить новый файл мультимедиа** для его отправки.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-154">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="2fdc6-155">При необходимости добавьте и настройте дополнительные модули **SocialShareItem**.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-155">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="2fdc6-156">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="2fdc6-157">На странице будет показан модуль социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-157">The page will show the social share module.</span></span>
1. <span data-ttu-id="2fdc6-158">Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="2fdc6-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2fdc6-159">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2fdc6-159">Additional resources</span></span>

[<span data-ttu-id="2fdc6-160">Обзор начального набора</span><span class="sxs-lookup"><span data-stu-id="2fdc6-160">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2fdc6-161">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="2fdc6-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2fdc6-162">Соответствие файлов cookie</span><span class="sxs-lookup"><span data-stu-id="2fdc6-162">Cookie compliance</span></span>](cookie-compliance.md)
