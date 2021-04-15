---
title: Отправка и подача статических файлов
description: Эта тема описывает, как отправить статический файл в конфигуратор сайта Microsoft Dynamics 365 Commerce, и как создать пользовательский URL-адрес и имя файла, которые могут быть использованы для запроса этого файла.
author: StuHarg
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d5f092042b3dda65b041ab2f25f7319dd8e158d1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801393"
---
# <a name="upload-and-serve-static-files"></a><span data-ttu-id="5f669-103">Отправка и подача статических файлов</span><span class="sxs-lookup"><span data-stu-id="5f669-103">Upload and serve static files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5f669-104">Эта тема описывает, как отправить статический файл в конфигуратор сайта Microsoft Dynamics 365 Commerce, и как создать пользовательский URL-адрес и имя файла, которые могут быть использованы для запроса этого файла.</span><span class="sxs-lookup"><span data-stu-id="5f669-104">This topic describes how to upload a static file into Microsoft Dynamics 365 Commerce site builder, and how to create a custom URL and file name that can be used to request that file.</span></span>

<span data-ttu-id="5f669-105">Некоторые сторонние соединители требуют, чтобы файл размещался и предоставлялся с сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="5f669-105">Some third-party connectors require that a file be hosted and served from the e-commerce site.</span></span> <span data-ttu-id="5f669-106">Эти соединители ожидают, что файл будет возвращен по запросам на определенный URL-путь обратного вызова и имя файла.</span><span class="sxs-lookup"><span data-stu-id="5f669-106">These connectors expect that the file will be returned by requests to a specific callback URL path and file name.</span></span> <span data-ttu-id="5f669-107">Таким образом, эта тема объясняет, как отправить и предоставить статический файл, который имеет определяемый пользователем URL-адрес и имя файла на сайте электронной коммерции Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5f669-107">Therefore, this topic explains how to upload and serve a static file that has a user-definable URL and file name on a Dynamics 365 Commerce e-commerce site.</span></span>

## <a name="create-a-site-url-that-returns-a-static-file"></a><span data-ttu-id="5f669-108">Создание URL-адреса сайта, который возвращает статический файл</span><span class="sxs-lookup"><span data-stu-id="5f669-108">Create a site URL that returns a static file</span></span>

<span data-ttu-id="5f669-109">Чтобы создать URL-адрес сайта, который возвращает статический файл в конфигураторе сайта Commerce, следуйте этим шагам.</span><span class="sxs-lookup"><span data-stu-id="5f669-109">To create a site URL that returns a static file in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="5f669-110">Перейдите в библиотеку мультимедиа вашего сайта и отправьте файл, который должен предоставляться по запросам на URL-адрес, который вы определите.</span><span class="sxs-lookup"><span data-stu-id="5f669-110">Go to your site's Media library, and upload the file that should be served by requests to the URL that you will define.</span></span> <span data-ttu-id="5f669-111">Если вы уже отправили файл, вы можете пропустить этот шаг.</span><span class="sxs-lookup"><span data-stu-id="5f669-111">If you've already uploaded the file, you can skip this step.</span></span>
1. <span data-ttu-id="5f669-112">Перейдите в раздел **URL-адреса** для вашего сайта.</span><span class="sxs-lookup"><span data-stu-id="5f669-112">Go to **URLs** for your site.</span></span>
1. <span data-ttu-id="5f669-113">Выберите **Создать \> Создать URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="5f669-113">Select **New \> New URL**.</span></span>
1. <span data-ttu-id="5f669-114">В диалоговом поле **Создать URL-адрес** выберите **Актив библиотеки мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="5f669-114">In the **New URL** dialog box, select **Media library asset**.</span></span>
1. <span data-ttu-id="5f669-115">В поле **URL-путь** введите URL-путь.</span><span class="sxs-lookup"><span data-stu-id="5f669-115">In the **URL path** field, enter the URL path.</span></span> <span data-ttu-id="5f669-116">Включите имя файла в путь.</span><span class="sxs-lookup"><span data-stu-id="5f669-116">Include the file name in the path.</span></span>
1. <span data-ttu-id="5f669-117">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5f669-117">Select **Next**.</span></span> <span data-ttu-id="5f669-118">Открывается библиотека мультимедиа и отображаются все ресурсы мультимедиа типа **документ**, которые были отправлены.</span><span class="sxs-lookup"><span data-stu-id="5f669-118">The Media library is opened and shows all media assets of the **document** type that have been uploaded.</span></span>
1. <span data-ttu-id="5f669-119">Выберите файл, который должен быть предоставлен для запросов на URL-адрес, который вы определили в шаге 5.</span><span class="sxs-lookup"><span data-stu-id="5f669-119">Select the file that should be served for requests to the URL that you defined in step 5.</span></span>
1. <span data-ttu-id="5f669-120">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="5f669-120">Select **Save**.</span></span>

<span data-ttu-id="5f669-121">На этом этапе URL-адрес, который вы создали, находится в состоянии черновика.</span><span class="sxs-lookup"><span data-stu-id="5f669-121">At this point, the URL that you created is in a draft state.</span></span> <span data-ttu-id="5f669-122">Файл, на который указывает URL-адрес, не будет возвращен до тех пор, пока вы не опубликуете URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="5f669-122">The file that the URL points to won't be returned until you publish the URL.</span></span> <span data-ttu-id="5f669-123">Перед публикацией URL-адреса можно подтвердить, что он возвращает правильные данные.</span><span class="sxs-lookup"><span data-stu-id="5f669-123">Before you publish the URL, you can validate that it returns the correct data.</span></span>

## <a name="validate-and-publish-a-url"></a><span data-ttu-id="5f669-124">Проверка и публикация URL-адреса</span><span class="sxs-lookup"><span data-stu-id="5f669-124">Validate and publish a URL</span></span>

<span data-ttu-id="5f669-125">Чтобы проверить URL-адрес перед его публикацией, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5f669-125">To validate an URL before you publish it, follow these steps.</span></span>

1. <span data-ttu-id="5f669-126">Перейдите в раздел **URL-адреса** для вашего сайта и выберите URL-адрес для предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="5f669-126">Go to **URLs** for your site, and select the URL to preview.</span></span>
2. <span data-ttu-id="5f669-127">На панели свойств справа под кнопкой **Изменить** выберите правильную ссылку URL.</span><span class="sxs-lookup"><span data-stu-id="5f669-127">In the properties pane on the right, below the **Edit** button, select the correct URL link.</span></span> <span data-ttu-id="5f669-128">Открывается новое окно браузера, и вы должны получить ошибку 404.</span><span class="sxs-lookup"><span data-stu-id="5f669-128">A new browser window is opened, and you should receive a 404 error.</span></span>
3. <span data-ttu-id="5f669-129">Добавьте строку запроса **?preview=inprogress** к URL-адресу (например, `https://yoursite.com/callback.html?preview=inprogress`) и перезагрузите страницу.</span><span class="sxs-lookup"><span data-stu-id="5f669-129">Append the **?preview=inprogress** query string to the URL (for example, `https://yoursite.com/callback.html?preview=inprogress`), and reload the page.</span></span> <span data-ttu-id="5f669-130">Файл, отправленный в библиотеку мультимедиа, должен быть возвращен в ответ.</span><span class="sxs-lookup"><span data-stu-id="5f669-130">The file that you uploaded to the Media library should be returned in the response.</span></span>

<span data-ttu-id="5f669-131">После проверки URL-адреса его можно опубликовать.</span><span class="sxs-lookup"><span data-stu-id="5f669-131">After you've validated the URL, you can publish it.</span></span>

1. <span data-ttu-id="5f669-132">Перейдите в раздел **URL-адреса** для вашего сайта и выберите URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="5f669-132">Go to **URLs** for your site, and select the URL.</span></span>
2. <span data-ttu-id="5f669-133">Выберите **Опубликовать** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="5f669-133">Select **Publish** on the command bar.</span></span>

## <a name="update-the-file-that-a-url-points-to"></a><span data-ttu-id="5f669-134">Обновление файла, на который указывает URL-адрес</span><span class="sxs-lookup"><span data-stu-id="5f669-134">Update the file that a URL points to</span></span>

<span data-ttu-id="5f669-135">После публикации URL-адреса можно обновить его так, чтобы он указывал на другой файл.</span><span class="sxs-lookup"><span data-stu-id="5f669-135">After a URL is published, you can update it so that it points to a different file.</span></span> <span data-ttu-id="5f669-136">Кроме того, можно обновить URL-адрес, чтобы он указывал на другой тип ресурса, как описано в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="5f669-136">Alternatively, you can update the URL so that it points to a different the type of resource, as described in the next section.</span></span> <span data-ttu-id="5f669-137">Например, можно задать, чтобы URL-адрес указывал на внутреннюю страницу или перенаправление.</span><span class="sxs-lookup"><span data-stu-id="5f669-137">For example, you can point the URL to an internal page or a redirect.</span></span>

<span data-ttu-id="5f669-138">Чтобы обновить файл, на который указывает URL-адрес, следуйте этим шагам.</span><span class="sxs-lookup"><span data-stu-id="5f669-138">To update the file that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="5f669-139">Перейдите в раздел **URL-адреса** для вашего сайта и выберите URL-адрес для обновления.</span><span class="sxs-lookup"><span data-stu-id="5f669-139">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="5f669-140">В области свойств справа выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="5f669-140">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="5f669-141">В разделе **Назначение URL-адреса** выберите поле **Шаг 2**, затем выберите новый документ из библиотеки мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="5f669-141">Under **URL assignment**, select the **Step 2** box, and then select a new document from the Media library.</span></span>
1. <span data-ttu-id="5f669-142">Выберите **Применить**.</span><span class="sxs-lookup"><span data-stu-id="5f669-142">Select **Apply**.</span></span>

## <a name="update-the-asset-type-that-a-url-points-to"></a><span data-ttu-id="5f669-143">Обновление типа ресурса, на который указывает URL-адрес</span><span class="sxs-lookup"><span data-stu-id="5f669-143">Update the asset type that a URL points to</span></span>

<span data-ttu-id="5f669-144">Можно также обновить URL-адрес, чтобы он указывал на другой тип актива (ресурса), например на внутреннюю страницу или перенаправление.</span><span class="sxs-lookup"><span data-stu-id="5f669-144">You can also update a URL so that it points to a different type of asset (resource), such as an internal page or a redirect.</span></span>

<span data-ttu-id="5f669-145">Чтобы обновить тип ресурса, на который указывает URL-адрес, следуйте этим шагам.</span><span class="sxs-lookup"><span data-stu-id="5f669-145">To update the asset type that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="5f669-146">Перейдите в раздел **URL-адреса** для вашего сайта и выберите URL-адрес для обновления.</span><span class="sxs-lookup"><span data-stu-id="5f669-146">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="5f669-147">В области свойств справа выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="5f669-147">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="5f669-148">В разделе **Назначение URL-адреса** в пункте **Шаг 1**, выберите другой тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="5f669-148">Under **URL assignment**, under **Step 1**, select a different asset type.</span></span>
1. <span data-ttu-id="5f669-149">Выберите поле **Шаг 2**, затем выберите новый актив.</span><span class="sxs-lookup"><span data-stu-id="5f669-149">Select the **Step 2** box, and then select the new asset.</span></span>
1. <span data-ttu-id="5f669-150">Выберите **Применить**.</span><span class="sxs-lookup"><span data-stu-id="5f669-150">Select **Apply**.</span></span>

## <a name="change-the-url-path"></a><span data-ttu-id="5f669-151">Изменение URL-пути</span><span class="sxs-lookup"><span data-stu-id="5f669-151">Change the URL path</span></span>

<span data-ttu-id="5f669-152">После создания URL-адреса его путь изменить нельзя.</span><span class="sxs-lookup"><span data-stu-id="5f669-152">After a URL is created, its path can't be changed.</span></span> <span data-ttu-id="5f669-153">Если необходимо изменить URL-путь, который предоставляет файл или любой другой тип ресурса, вы должны создать новый URL-адрес, сопоставить его с существующим файлом или другим ресурсом, а затем отменить публикацию и удалить старый URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="5f669-153">If you must change the URL path that serves a file or any other type of resource, you have to create a new URL, map it to the existing file or other resource, and then unpublish and delete the old URL.</span></span>

<span data-ttu-id="5f669-154">Чтобы изменить URL-путь, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5f669-154">To change the URL path, follow these steps.</span></span>

1. <span data-ttu-id="5f669-155">Чтобы создать новый URL-адрес и сопоставить его с существующим файлом или другим ресурсом, следуйте инструкциям в разделе [Создание URL-адреса сайта, который возвращает статический файл](#create-a-site-url-that-returns-a-static-file) ранее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="5f669-155">To create a new URL and map it to the existing file or another resource, follow the instructions in the [Create a site URL that returns a static file](#create-a-site-url-that-returns-a-static-file) section earlier in this topic.</span></span>
1. <span data-ttu-id="5f669-156">Выберите новый URL-адрес и выберите **Опубликовать** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="5f669-156">Select the new URL, and select **Publish** on the command bar.</span></span> <span data-ttu-id="5f669-157">Новый URL-адрес публикуется.</span><span class="sxs-lookup"><span data-stu-id="5f669-157">The new URL is published.</span></span>
1. <span data-ttu-id="5f669-158">Чтобы отменить публикацию старого URL-адреса, выберите его, затем выберите **Отменить публикацию** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="5f669-158">To unpublish the old URL, select it, and then select **Unpublish** on the command bar.</span></span> <span data-ttu-id="5f669-159">Теперь вы можете удалить старый URL-адрес, если хотите.</span><span class="sxs-lookup"><span data-stu-id="5f669-159">You can now delete the old URL if you want.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5f669-160">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5f669-160">Additional resources</span></span>

[<span data-ttu-id="5f669-161">Обзор управления цифровыми активами</span><span class="sxs-lookup"><span data-stu-id="5f669-161">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="5f669-162">Отправка изображений</span><span class="sxs-lookup"><span data-stu-id="5f669-162">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="5f669-163">Отправка видео</span><span class="sxs-lookup"><span data-stu-id="5f669-163">Upload videos</span></span>](dam-upload-video.md)

[<span data-ttu-id="5f669-164">Отправка файлов, отличных от изображений и видео</span><span class="sxs-lookup"><span data-stu-id="5f669-164">Upload files other than images and videos</span></span>](dam-upload-files.md)

[<span data-ttu-id="5f669-165">Кадрирование изображений</span><span class="sxs-lookup"><span data-stu-id="5f669-165">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="5f669-166">Настройка точек фокуса изображения</span><span class="sxs-lookup"><span data-stu-id="5f669-166">Customize image focal points</span></span>](dam-custom-focal-point.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]