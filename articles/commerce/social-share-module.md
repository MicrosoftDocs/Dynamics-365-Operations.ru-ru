---
title: Модуль предоставления общего доступа через социальные сети
description: В этом разделе описываются модули предоставления общего доступа через социальные сети, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: c34410a8c817de9fed350bf2cd2dd918a37c230f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795365"
---
# <a name="social-share-module"></a><span data-ttu-id="42b8a-103">Модуль Social Share</span><span class="sxs-lookup"><span data-stu-id="42b8a-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="42b8a-104">В этом разделе описываются модули предоставления общего доступа через социальные сети, а также описывается, как добавлять их к страницам сайта в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="42b8a-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="42b8a-105">Модули предоставления общего доступа через социальные сети позволяют пользователям совместно использовать URL-адреса страниц сайта электронной коммерции в социальных сетях, таких как Facebook, Twitter, Pinterest и LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="42b8a-105">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="42b8a-106">URL-адреса страниц сайтов также могут использоваться совместно с помощью электронной почты.</span><span class="sxs-lookup"><span data-stu-id="42b8a-106">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="42b8a-107">Модули предоставления общего доступа через социальные сети обычно используются на страницах сведений о продуктах (PDP), чтобы помочь пользователям совместно использовать сведения о продукте.</span><span class="sxs-lookup"><span data-stu-id="42b8a-107">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="42b8a-108">Каждый модуль предоставления общего доступа через социальные сети является контейнером для модулей предоставления общего доступа к номенклатурам в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="42b8a-108">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="42b8a-109">Каждый модуль предоставления общего доступа к номенклатуре в социальных сетях можно настроить так, чтобы он указывал на конкретный сайт социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="42b8a-109">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="42b8a-110">Интеграция с Facebook, Twitter, Pinterest, LinkedIn и электронной почтой поддерживается стандартно.</span><span class="sxs-lookup"><span data-stu-id="42b8a-110">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="42b8a-111">Когда пользователь сайта выбирает символ социальных сетей, для соответствующего сайта социальных сетей запускается HTML-окно iFrame.</span><span class="sxs-lookup"><span data-stu-id="42b8a-111">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="42b8a-112">В окне iFrame пользователь может входить в систему и публиковать просматриваемое им содержимое.</span><span class="sxs-lookup"><span data-stu-id="42b8a-112">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="42b8a-113">На каждой платформе социальных сетей могут отслеживаться файлы cookie, поэтому для этого модуля необходимо, чтобы пользователи сайта приняли сообщение с уведомлением о согласии на получение файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="42b8a-113">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="42b8a-114">Если согласие не файлы cookie не принимается, модуль будет скрыт на странице.</span><span class="sxs-lookup"><span data-stu-id="42b8a-114">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="42b8a-115">Дополнительные сведения см. в разделе [Соответствие файлов cookie](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="42b8a-115">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="42b8a-116">На следующем рисунке показан пример модуля предоставления общего доступа в социальных сетях, используемого на странице сведений о продукте.</span><span class="sxs-lookup"><span data-stu-id="42b8a-116">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![Пример модуля предоставления общего доступа в социальных сетях](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="42b8a-118">Свойства модуля предоставления общего доступа в социальных сетях</span><span class="sxs-lookup"><span data-stu-id="42b8a-118">Social share module properties</span></span>

| <span data-ttu-id="42b8a-119">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="42b8a-119">Property name</span></span>             | <span data-ttu-id="42b8a-120">значение</span><span class="sxs-lookup"><span data-stu-id="42b8a-120">Value</span></span>                 | <span data-ttu-id="42b8a-121">описание</span><span class="sxs-lookup"><span data-stu-id="42b8a-121">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="42b8a-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="42b8a-122">Caption</span></span>                  | <span data-ttu-id="42b8a-123">Текст</span><span class="sxs-lookup"><span data-stu-id="42b8a-123">Text</span></span> | <span data-ttu-id="42b8a-124">Это свойство задает подпись для модуля.</span><span class="sxs-lookup"><span data-stu-id="42b8a-124">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="42b8a-125">Ориентация</span><span class="sxs-lookup"><span data-stu-id="42b8a-125">Orientation</span></span> | <span data-ttu-id="42b8a-126">**Горизонтальная** или **Вертикальная**</span><span class="sxs-lookup"><span data-stu-id="42b8a-126">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="42b8a-127">Это свойство определяет ориентацию макета для элементов социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="42b8a-127">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="42b8a-128">Свойства модуля элементов предоставления общего доступа в социальных сетях</span><span class="sxs-lookup"><span data-stu-id="42b8a-128">Social share item module properties</span></span>
| <span data-ttu-id="42b8a-129">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="42b8a-129">Property name</span></span>             | <span data-ttu-id="42b8a-130">значение</span><span class="sxs-lookup"><span data-stu-id="42b8a-130">Value</span></span>                 | <span data-ttu-id="42b8a-131">описание</span><span class="sxs-lookup"><span data-stu-id="42b8a-131">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="42b8a-132">Социальные сети</span><span class="sxs-lookup"><span data-stu-id="42b8a-132">Social media</span></span>              | <span data-ttu-id="42b8a-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Почта**</span><span class="sxs-lookup"><span data-stu-id="42b8a-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span></span> | <span data-ttu-id="42b8a-134">Раскрывающееся меню со списком платформ социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="42b8a-134">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="42b8a-135">Значок</span><span class="sxs-lookup"><span data-stu-id="42b8a-135">Icon</span></span> |<span data-ttu-id="42b8a-136">Изображение</span><span class="sxs-lookup"><span data-stu-id="42b8a-136">Image</span></span>    | <span data-ttu-id="42b8a-137">Это будет изображение, которое будет отображаться для соответствующей социальной сети.</span><span class="sxs-lookup"><span data-stu-id="42b8a-137">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="42b8a-138">Рекомендуется обращаться к пакету SDK платформы социальных сетей для получения рекомендуемого изображения, используемого для каждой платформы.</span><span class="sxs-lookup"><span data-stu-id="42b8a-138">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="42b8a-139">Добавление модуля предоставления общего доступа в социальных сетях в модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="42b8a-139">Add a social share module to a buy box module</span></span>

<span data-ttu-id="42b8a-140">Чтобы добавить модуль предоставления общего доступа в социальных сетях в модуль поля покупки, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="42b8a-140">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="42b8a-141">На сайте Fabrikam выберите **Страницы**, затем выберите страницу **DefaultPDP**, чтобы открыть страницу сведений о продукте.</span><span class="sxs-lookup"><span data-stu-id="42b8a-141">In the Fabrikam site, select **Pages**, and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="42b8a-142">В ячейке **Поле покупки (обязательно)** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="42b8a-142">In the **Buybox (required)** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="42b8a-143">В диалоговом окне **Добавить модуль** выберите модуль **Общий доступ в социальных сетях**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="42b8a-143">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="42b8a-144">В ячейке **Общий доступ в социальных сетях** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="42b8a-144">In the **Social Share** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="42b8a-145">В диалоговом окне **Добавить модуль** выберите модуль **SocialShare**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="42b8a-145">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="42b8a-146">В области свойств модуля **SocialShare** в разделе **Ориентация** выберите **Горизонтальная**.</span><span class="sxs-lookup"><span data-stu-id="42b8a-146">In the properties pane of the **SocialShare** module, under **Orientation**, select **Horizontal**.</span></span> <span data-ttu-id="42b8a-147">При необходимости добавьте подпись.</span><span class="sxs-lookup"><span data-stu-id="42b8a-147">Add a caption as needed.</span></span>
1. <span data-ttu-id="42b8a-148">В ячейке **SocialShare** выберите многоточие (**...**), затем выберите **Добавить модуль**.</span><span class="sxs-lookup"><span data-stu-id="42b8a-148">In the **SocialShare** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="42b8a-149">В диалоговом окне **Добавить модуль** выберите модуль **SocialShareItem**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="42b8a-149">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="42b8a-150">В области свойств модуля **SocialShareItem** в разделе **Социальная сеть** выберите **Facebook**.</span><span class="sxs-lookup"><span data-stu-id="42b8a-150">In the properties pane of the **SocialShareItem** module, under **Social Media**, select **Facebook**.</span></span>
1. <span data-ttu-id="42b8a-151">В области свойств модуля **SocialShareItem** в разделе **Значок** выберите **+ Добавить изображение**.</span><span class="sxs-lookup"><span data-stu-id="42b8a-151">In the properties pane of the **SocialShareItem** module, under **Icon**, select **+ Add an image**.</span></span>
1. <span data-ttu-id="42b8a-152">В диалоговом окне **Выбор мультимедиа** выберите изображение логотипа Facebook, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="42b8a-152">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="42b8a-153">Если изображение логотипа Facebook отсутствует, выберите **Отправить новый файл мультимедиа** для его отправки.</span><span class="sxs-lookup"><span data-stu-id="42b8a-153">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="42b8a-154">При необходимости добавьте и настройте дополнительные модули **SocialShareItem**.</span><span class="sxs-lookup"><span data-stu-id="42b8a-154">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="42b8a-155">Выберите **Сохранить**, затем выберите **Предварительный просмотр**, чтобы просмотреть страницу.</span><span class="sxs-lookup"><span data-stu-id="42b8a-155">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="42b8a-156">На странице будет показан модуль социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="42b8a-156">The page will show the social share module.</span></span>
1. <span data-ttu-id="42b8a-157">Выберите **Завершить редактирование** для возврата страницы, затем нажмите кнопку **Опубликовать**, чтобы опубликовать ее.</span><span class="sxs-lookup"><span data-stu-id="42b8a-157">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="42b8a-158">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="42b8a-158">Additional resources</span></span>

[<span data-ttu-id="42b8a-159">Обзор библиотеки модулей</span><span class="sxs-lookup"><span data-stu-id="42b8a-159">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="42b8a-160">Модуль поля покупки</span><span class="sxs-lookup"><span data-stu-id="42b8a-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="42b8a-161">Соответствие файлов cookie</span><span class="sxs-lookup"><span data-stu-id="42b8a-161">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]