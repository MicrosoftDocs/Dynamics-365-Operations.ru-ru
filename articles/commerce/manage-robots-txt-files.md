---
title: Управление файлами robots.txt
description: В этой теме описано, как управлять файлами robots.txt в Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brishoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ce49f2968030ca4656a01c7646819c01635e12
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003495"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="b4b33-103">Управление файлами robots.txt</span><span class="sxs-lookup"><span data-stu-id="b4b33-103">Manage robots.txt files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b4b33-104">В этой теме описано, как управлять файлами robots.txt в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b4b33-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b4b33-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="b4b33-105">Overview</span></span>

<span data-ttu-id="b4b33-106">Стандарт исключения роботов, или robots.txt, является стандартом, который веб-сайты используют для связи с веб-роботами.</span><span class="sxs-lookup"><span data-stu-id="b4b33-106">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="b4b33-107">Он инструктирует веб-роботов о любых областях веб-сайта, которые не должны быть посещены.</span><span class="sxs-lookup"><span data-stu-id="b4b33-107">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="b4b33-108">Роботы часто используются поисковыми системами для индексирования веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="b4b33-108">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="b4b33-109">Чтобы исключить роботов с сервера, вы создаете файл на сервере.</span><span class="sxs-lookup"><span data-stu-id="b4b33-109">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="b4b33-110">В этом файле указывается политика доступа для роботов.</span><span class="sxs-lookup"><span data-stu-id="b4b33-110">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="b4b33-111">Файл должен быть доступен через HTTP по локальному URL-адресу **/robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="b4b33-111">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="b4b33-112">Файл robots.txt помогает поисковым системам индексировать содержимое вашего сайта.</span><span class="sxs-lookup"><span data-stu-id="b4b33-112">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="b4b33-113">Dynamics 365 Commerce позволяет загружать файл robots.txt для вашего домена.</span><span class="sxs-lookup"><span data-stu-id="b4b33-113">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="b4b33-114">Для каждого домена в вашей среде Commerce вы можете загрузить один файл robots.txt и связать его с этим доменом.</span><span class="sxs-lookup"><span data-stu-id="b4b33-114">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="b4b33-115">Для получения дополнительной информации о файле robots.txt см. [страницы о веб-роботах](https://www.robotstxt.org/).</span><span class="sxs-lookup"><span data-stu-id="b4b33-115">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="b4b33-116">Отправка файла robots.txt</span><span class="sxs-lookup"><span data-stu-id="b4b33-116">Upload a robots.txt file</span></span>

<span data-ttu-id="b4b33-117">После того, как вы создали и отредактировали свой файл robots.txt в соответствии со [стандартом исключения роботов](https://www.robotstxt.org/orig.html), убедитесь, что файл доступен на компьютере, где вы будете использовать инструменты авторизации Commerce.</span><span class="sxs-lookup"><span data-stu-id="b4b33-117">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="b4b33-118">Файл должен называться **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="b4b33-118">The file must be named **robots.txt**.</span></span> <span data-ttu-id="b4b33-119">Для достижения наилучших результатов он должен быть в формате, который указан в стандарте.</span><span class="sxs-lookup"><span data-stu-id="b4b33-119">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="b4b33-120">Каждый клиент Commerce несет ответственность за проверку и обслуживание содержимого своего файла robots.txt.</span><span class="sxs-lookup"><span data-stu-id="b4b33-120">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="b4b33-121">Чтобы отправить файл robots.txt, вы должны войти в Commerce как системный администратор.</span><span class="sxs-lookup"><span data-stu-id="b4b33-121">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="b4b33-122">Чтобы отправить файл robots.txt в Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b4b33-122">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b4b33-123">Войдите в Commerce в качестве системного администратора.</span><span class="sxs-lookup"><span data-stu-id="b4b33-123">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="b4b33-124">В левой области переходов выберите **Настройки клиента** (рядом с символом шестеренки), чтобы развернуть его.</span><span class="sxs-lookup"><span data-stu-id="b4b33-124">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="b4b33-125">В разделе **Настройки клиента** выберите **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="b4b33-125">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="b4b33-126">Список всех доменов, связанных с вашей средой, отображается в основной части окна.</span><span class="sxs-lookup"><span data-stu-id="b4b33-126">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="b4b33-127">Выберите **Управление**, чтобы отправить файл robots.txt для домена в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="b4b33-127">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="b4b33-128">В меню справа выберите кнопку **Отправить** (стрелка вверх) рядом с доменом, который связан с файлом robots.txt.</span><span class="sxs-lookup"><span data-stu-id="b4b33-128">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="b4b33-129">Появляется диалоговое окно браузера файлов.</span><span class="sxs-lookup"><span data-stu-id="b4b33-129">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="b4b33-130">В диалоговом окне найдите и выберите файл robots.txt, который вы хотите отправить для связанного домена, а затем выберите **Открыть** для завершения отправки.</span><span class="sxs-lookup"><span data-stu-id="b4b33-130">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="b4b33-131">Во время отправки Commerce проверяет, что файл является текстовым файлом, но он не проверяет содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="b4b33-131">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="b4b33-132">Загрузка файла robots.txt</span><span class="sxs-lookup"><span data-stu-id="b4b33-132">Download a robots.txt file</span></span>

<span data-ttu-id="b4b33-133">Чтобы загрузить файл robots.txt в Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b4b33-133">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b4b33-134">Войдите в Commerce в качестве системного администратора.</span><span class="sxs-lookup"><span data-stu-id="b4b33-134">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="b4b33-135">В левой области переходов выберите **Настройки клиента** (рядом с символом шестеренки), чтобы развернуть его.</span><span class="sxs-lookup"><span data-stu-id="b4b33-135">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="b4b33-136">В разделе **Настройки клиента** выберите **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="b4b33-136">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="b4b33-137">Список всех доменов, связанных с вашей средой, отображается в основной части окна.</span><span class="sxs-lookup"><span data-stu-id="b4b33-137">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="b4b33-138">Выберите **Управление**, чтобы загрузить файл robots.txt для домена в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="b4b33-138">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="b4b33-139">В меню справа выберите кнопку **Загрузить** (стрелка вниз) рядом с доменом, который связан с файлом robots.txt.</span><span class="sxs-lookup"><span data-stu-id="b4b33-139">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="b4b33-140">Появляется диалоговое окно браузера файлов.</span><span class="sxs-lookup"><span data-stu-id="b4b33-140">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="b4b33-141">В диалоговом окне перейдите в нужное место на локальном диске, подтвердите или введите имя файла, а затем выберите **Сохранить** для завершения загрузки.</span><span class="sxs-lookup"><span data-stu-id="b4b33-141">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="b4b33-142">Эта процедура может быть использована для загрузки только файлов robots.txt, которые ранее были загружены через инструменты разработки Commerce.</span><span class="sxs-lookup"><span data-stu-id="b4b33-142">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="b4b33-143">Удаление файла robots.txt</span><span class="sxs-lookup"><span data-stu-id="b4b33-143">Delete a robots.txt file</span></span>

<span data-ttu-id="b4b33-144">Чтобы удалить файл robots.txt в Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b4b33-144">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b4b33-145">Войдите в Commerce в качестве системного администратора.</span><span class="sxs-lookup"><span data-stu-id="b4b33-145">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="b4b33-146">В левой области переходов выберите **Настройки клиента** (рядом с символом шестеренки), чтобы развернуть его.</span><span class="sxs-lookup"><span data-stu-id="b4b33-146">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="b4b33-147">В разделе **Настройки клиента** выберите **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="b4b33-147">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="b4b33-148">Список всех доменов, связанных с вашей средой, отображается в основной части окна.</span><span class="sxs-lookup"><span data-stu-id="b4b33-148">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="b4b33-149">Выберите **Управление**, чтобы удалить файл robots.txt для домена в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="b4b33-149">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="b4b33-150">В меню справа выберите кнопку **Удалить** (символ корзины) рядом с доменом, который связан с файлом robots.txt.</span><span class="sxs-lookup"><span data-stu-id="b4b33-150">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="b4b33-151">Отображается окно браузера файлов.</span><span class="sxs-lookup"><span data-stu-id="b4b33-151">A file browser window appears.</span></span>
6. <span data-ttu-id="b4b33-152">В окне браузера фалов найдите и выберите файл robots.txt, который вы хотите удалить для домена, а затем выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="b4b33-152">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="b4b33-153">Появляется окно предупреждающих сообщений.</span><span class="sxs-lookup"><span data-stu-id="b4b33-153">A warning message box appears.</span></span>
7. <span data-ttu-id="b4b33-154">В поле сообщения выберите **Удалить**, чтобы подтвердить удаление файла robots.txt.</span><span class="sxs-lookup"><span data-stu-id="b4b33-154">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="b4b33-155">Эта процедура может быть использована для удаления только файлов robots.txt, которые ранее были загружены через инструменты разработки Commerce.</span><span class="sxs-lookup"><span data-stu-id="b4b33-155">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4b33-156">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b4b33-156">Additional resources</span></span>

[<span data-ttu-id="b4b33-157">Настройка доменного имени</span><span class="sxs-lookup"><span data-stu-id="b4b33-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="b4b33-158">Развертывание нового сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="b4b33-158">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="b4b33-159">Создание сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="b4b33-159">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="b4b33-160">Связывание веб-сайта с каналом</span><span class="sxs-lookup"><span data-stu-id="b4b33-160">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="b4b33-161">Настройка специальных страниц для входа пользователей</span><span class="sxs-lookup"><span data-stu-id="b4b33-161">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="b4b33-162">Добавление поддержки сети доставки контента (CDN)</span><span class="sxs-lookup"><span data-stu-id="b4b33-162">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="b4b33-163">Включение обнаружения магазинов на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="b4b33-163">Enable location-based store detection</span></span>](enable-store-detection.md)
