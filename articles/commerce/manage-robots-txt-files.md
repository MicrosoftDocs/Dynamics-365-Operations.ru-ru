---
title: Управление файлами robots.txt
description: В этой теме описано, как управлять файлами robots.txt в Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 07/02/2020
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
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: ad87594b9c20d0c2b53e8d4e7c1170a78babe74b
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517460"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="25f31-103">Управление файлами robots.txt</span><span class="sxs-lookup"><span data-stu-id="25f31-103">Manage robots.txt files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="25f31-104">В этой теме описано, как управлять файлами robots.txt в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="25f31-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="25f31-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="25f31-105">Overview</span></span>

<span data-ttu-id="25f31-106">Стандарт исключения роботов, или robots.txt, является стандартом, который веб-сайты используют для связи с веб-роботами.</span><span class="sxs-lookup"><span data-stu-id="25f31-106">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="25f31-107">Он инструктирует веб-роботов о любых областях веб-сайта, которые не должны быть посещены.</span><span class="sxs-lookup"><span data-stu-id="25f31-107">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="25f31-108">Роботы часто используются поисковыми системами для индексирования веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="25f31-108">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="25f31-109">Чтобы исключить роботов с сервера, вы создаете файл на сервере.</span><span class="sxs-lookup"><span data-stu-id="25f31-109">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="25f31-110">В этом файле указывается политика доступа для роботов.</span><span class="sxs-lookup"><span data-stu-id="25f31-110">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="25f31-111">Файл должен быть доступен через HTTP по локальному URL-адресу **/robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="25f31-111">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="25f31-112">Файл robots.txt помогает поисковым системам индексировать содержимое вашего сайта.</span><span class="sxs-lookup"><span data-stu-id="25f31-112">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="25f31-113">Dynamics 365 Commerce позволяет загружать файл robots.txt для вашего домена.</span><span class="sxs-lookup"><span data-stu-id="25f31-113">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="25f31-114">Для каждого домена в вашей среде Commerce вы можете загрузить один файл robots.txt и связать его с этим доменом.</span><span class="sxs-lookup"><span data-stu-id="25f31-114">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="25f31-115">Для получения дополнительной информации о файле robots.txt см. [страницы о веб-роботах](https://www.robotstxt.org/).</span><span class="sxs-lookup"><span data-stu-id="25f31-115">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="25f31-116">Отправка файла robots.txt</span><span class="sxs-lookup"><span data-stu-id="25f31-116">Upload a robots.txt file</span></span>

<span data-ttu-id="25f31-117">После того, как вы создали и отредактировали свой файл robots.txt в соответствии со [стандартом исключения роботов](https://www.robotstxt.org/orig.html), убедитесь, что файл доступен на компьютере, где вы будете использовать инструменты авторизации Commerce.</span><span class="sxs-lookup"><span data-stu-id="25f31-117">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="25f31-118">Файл должен называться **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="25f31-118">The file must be named **robots.txt**.</span></span> <span data-ttu-id="25f31-119">Для достижения наилучших результатов он должен быть в формате, который указан в стандарте.</span><span class="sxs-lookup"><span data-stu-id="25f31-119">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="25f31-120">Каждый клиент Commerce несет ответственность за проверку и обслуживание содержимого своего файла robots.txt.</span><span class="sxs-lookup"><span data-stu-id="25f31-120">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="25f31-121">Чтобы отправить файл robots.txt, вы должны войти в Commerce как системный администратор.</span><span class="sxs-lookup"><span data-stu-id="25f31-121">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="25f31-122">Чтобы отправить файл robots.txt в Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="25f31-122">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="25f31-123">Войдите в Commerce в качестве системного администратора.</span><span class="sxs-lookup"><span data-stu-id="25f31-123">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="25f31-124">В левой области переходов выберите **Настройки клиента** (рядом с символом шестеренки), чтобы развернуть его.</span><span class="sxs-lookup"><span data-stu-id="25f31-124">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="25f31-125">В разделе **Настройки клиента** выберите **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="25f31-125">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="25f31-126">Список всех доменов, связанных с вашей средой, отображается в основной части окна.</span><span class="sxs-lookup"><span data-stu-id="25f31-126">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="25f31-127">Выберите **Управление**, чтобы отправить файл robots.txt для домена в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="25f31-127">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="25f31-128">В меню справа выберите кнопку **Отправить** (стрелка вверх) рядом с доменом, который связан с файлом robots.txt.</span><span class="sxs-lookup"><span data-stu-id="25f31-128">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="25f31-129">Появляется диалоговое окно браузера файлов.</span><span class="sxs-lookup"><span data-stu-id="25f31-129">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="25f31-130">В диалоговом окне найдите и выберите файл robots.txt, который вы хотите отправить для связанного домена, а затем выберите **Открыть** для завершения отправки.</span><span class="sxs-lookup"><span data-stu-id="25f31-130">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="25f31-131">Во время отправки Commerce проверяет, что файл является текстовым файлом, но он не проверяет содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="25f31-131">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="25f31-132">Загрузка файла robots.txt</span><span class="sxs-lookup"><span data-stu-id="25f31-132">Download a robots.txt file</span></span>

<span data-ttu-id="25f31-133">Чтобы загрузить файл robots.txt в Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="25f31-133">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="25f31-134">Войдите в Commerce в качестве системного администратора.</span><span class="sxs-lookup"><span data-stu-id="25f31-134">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="25f31-135">В левой области переходов выберите **Настройки клиента** (рядом с символом шестеренки), чтобы развернуть его.</span><span class="sxs-lookup"><span data-stu-id="25f31-135">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="25f31-136">В разделе **Настройки клиента** выберите **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="25f31-136">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="25f31-137">Список всех доменов, связанных с вашей средой, отображается в основной части окна.</span><span class="sxs-lookup"><span data-stu-id="25f31-137">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="25f31-138">Выберите **Управление**, чтобы загрузить файл robots.txt для домена в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="25f31-138">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="25f31-139">В меню справа выберите кнопку **Загрузить** (стрелка вниз) рядом с доменом, который связан с файлом robots.txt.</span><span class="sxs-lookup"><span data-stu-id="25f31-139">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="25f31-140">Появляется диалоговое окно браузера файлов.</span><span class="sxs-lookup"><span data-stu-id="25f31-140">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="25f31-141">В диалоговом окне перейдите в нужное место на локальном диске, подтвердите или введите имя файла, а затем выберите **Сохранить** для завершения загрузки.</span><span class="sxs-lookup"><span data-stu-id="25f31-141">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="25f31-142">Эта процедура может быть использована для загрузки только файлов robots.txt, которые ранее были загружены через инструменты разработки Commerce.</span><span class="sxs-lookup"><span data-stu-id="25f31-142">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="25f31-143">Удаление файла robots.txt</span><span class="sxs-lookup"><span data-stu-id="25f31-143">Delete a robots.txt file</span></span>

<span data-ttu-id="25f31-144">Чтобы удалить файл robots.txt в Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="25f31-144">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="25f31-145">Войдите в Commerce в качестве системного администратора.</span><span class="sxs-lookup"><span data-stu-id="25f31-145">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="25f31-146">В левой области переходов выберите **Настройки клиента** (рядом с символом шестеренки), чтобы развернуть его.</span><span class="sxs-lookup"><span data-stu-id="25f31-146">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="25f31-147">В разделе **Настройки клиента** выберите **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="25f31-147">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="25f31-148">Список всех доменов, связанных с вашей средой, отображается в основной части окна.</span><span class="sxs-lookup"><span data-stu-id="25f31-148">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="25f31-149">Выберите **Управление**, чтобы удалить файл robots.txt для домена в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="25f31-149">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="25f31-150">В меню справа выберите кнопку **Удалить** (символ корзины) рядом с доменом, который связан с файлом robots.txt.</span><span class="sxs-lookup"><span data-stu-id="25f31-150">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="25f31-151">Отображается окно браузера файлов.</span><span class="sxs-lookup"><span data-stu-id="25f31-151">A file browser window appears.</span></span>
6. <span data-ttu-id="25f31-152">В окне браузера фалов найдите и выберите файл robots.txt, который вы хотите удалить для домена, а затем выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="25f31-152">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="25f31-153">Появляется окно предупреждающих сообщений.</span><span class="sxs-lookup"><span data-stu-id="25f31-153">A warning message box appears.</span></span>
7. <span data-ttu-id="25f31-154">В поле сообщения выберите **Удалить**, чтобы подтвердить удаление файла robots.txt.</span><span class="sxs-lookup"><span data-stu-id="25f31-154">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="25f31-155">Эта процедура может быть использована для удаления только файлов robots.txt, которые ранее были загружены через инструменты разработки Commerce.</span><span class="sxs-lookup"><span data-stu-id="25f31-155">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="25f31-156">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="25f31-156">Additional resources</span></span>

[<span data-ttu-id="25f31-157">Настройка доменного имени</span><span class="sxs-lookup"><span data-stu-id="25f31-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="25f31-158">Развертывание нового клиента электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="25f31-158">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="25f31-159">Создание сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="25f31-159">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="25f31-160">Связывание сайта Dynamics 365 Commerce с интернет-каналом</span><span class="sxs-lookup"><span data-stu-id="25f31-160">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="25f31-161">Пакетная отправка перенаправлений URL-адресов</span><span class="sxs-lookup"><span data-stu-id="25f31-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="25f31-162">Настройка клиента B2C в модуле Commerce</span><span class="sxs-lookup"><span data-stu-id="25f31-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="25f31-163">Настройка специальных страниц для входа пользователей</span><span class="sxs-lookup"><span data-stu-id="25f31-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="25f31-164">Настройка нескольких клиентов B2C в среде Commerce</span><span class="sxs-lookup"><span data-stu-id="25f31-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="25f31-165">Добавление поддержки сети доставки контента (CDN)</span><span class="sxs-lookup"><span data-stu-id="25f31-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="25f31-166">Включение обнаружения магазинов на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="25f31-166">Enable location-based store detection</span></span>](enable-store-detection.md)
