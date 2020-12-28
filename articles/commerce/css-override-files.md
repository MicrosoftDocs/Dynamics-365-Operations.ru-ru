---
title: Работа с переопределением файлов CSS
description: В этой теме описывается, почему, когда и как использовать файлы переопределения каскадных таблиц стилей (CSS) переопределить файлы в Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3ec43b16b1df07400cffe597378ad4035e4d07e0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415241"
---
# <a name="work-with-css-override-files"></a><span data-ttu-id="9e06b-103">Работа с переопределением файлов CSS</span><span class="sxs-lookup"><span data-stu-id="9e06b-103">Work with CSS override files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9e06b-104">В этой теме описывается, почему, когда и как использовать файлы переопределения каскадных таблиц стилей (CSS) переопределить файлы в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9e06b-104">This topic describes why, when, and how to use Cascading Style Sheets (CSS) override files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9e06b-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="9e06b-105">Overview</span></span>

<span data-ttu-id="9e06b-106">Постоянные стили сайта, как правило, должны быть обработаны через тему сайта.</span><span class="sxs-lookup"><span data-stu-id="9e06b-106">Permanent site styles should usually be handled through a site's theme.</span></span> <span data-ttu-id="9e06b-107">Темы обеспечивают основы CSS и настройки стиля для модулей на любой странице вашего сайта.</span><span class="sxs-lookup"><span data-stu-id="9e06b-107">Themes provide the foundational CSS and style settings for the modules on any page of your site.</span></span> <span data-ttu-id="9e06b-108">Темы создаются с помощью онлайн-пакета средств разработки Dynamics 365 Commerce (SDK), и они развернуты на ваших веб-сайтах через Lifecycle Services Microsoft Dynamics (LCS).</span><span class="sxs-lookup"><span data-stu-id="9e06b-108">Themes are created by using the Dynamics 365 Commerce online software development kit (SDK), and they are deployed to your websites through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="9e06b-109">Возможности отладки тем и конфигурации интерфейса модуля в SDK помогают разработчикам сайтов создавать настраиваемые и связанные пакеты дизайна сайта.</span><span class="sxs-lookup"><span data-stu-id="9e06b-109">Theme debugging capabilities and module interface configurations in the SDK help site developers create customizable and cohesive site design packages.</span></span> <span data-ttu-id="9e06b-110">Когда эти пакеты дизайна развертываются на сайте, авторы сайта могут сосредоточиться на создании, редактировании и публикации контента вместо разработки сайта.</span><span class="sxs-lookup"><span data-stu-id="9e06b-110">When these design packages are deployed to a site, site authors can focus on creating, editing, and publishing content instead of site development.</span></span>

<span data-ttu-id="9e06b-111">Учитывая обычный жизненный цикл темы, зависимость от разработчиков в плане изменения стиля через конвейер развертывания SDK и LCS может быть непомерно высокой в некоторых сценариях.</span><span class="sxs-lookup"><span data-stu-id="9e06b-111">Given the usual lifecycle of a theme, the dependency on developers to make style changes through the SDK and LCS deployment pipeline can be prohibitive in some scenarios.</span></span> <span data-ttu-id="9e06b-112">Прототипы или исправления ошибок сайта могут показаться громоздкими, если SDK не настроен или если у вас нет времени ждать развертывания LCS.</span><span class="sxs-lookup"><span data-stu-id="9e06b-112">Site prototypes or hotfixes can seem cumbersome if the SDK isn't configured, or if you don't have time to wait for an LCS deployment.</span></span>

<span data-ttu-id="9e06b-113">В этих сценариях переопределение файлов CSS может помочь.</span><span class="sxs-lookup"><span data-stu-id="9e06b-113">In these scenarios, CSS override files can help.</span></span> <span data-ttu-id="9e06b-114">В инструментах разработки Commerce аутентифицированные пользователи могут отправить файл CSS, просмотреть его, а затем активировать, чтобы переопределить тему сайта.</span><span class="sxs-lookup"><span data-stu-id="9e06b-114">In the Commerce authoring tools, authenticated users can upload a CSS file, preview it, and then activate it to override a site's theme.</span></span> <span data-ttu-id="9e06b-115">Накладные расходы на развертывание SDK или LCS не требуются.</span><span class="sxs-lookup"><span data-stu-id="9e06b-115">The overhead of SDK or LCS deployment isn't required.</span></span> <span data-ttu-id="9e06b-116">Переопределения, указанные в файле переопределения CSS, могут быть всего лишь изменением одного стиля текста или полной капитальной переделкой бренда.</span><span class="sxs-lookup"><span data-stu-id="9e06b-116">The overrides that are specified in a CSS override file can be as small as a change to a single text style or as wide-ranging as a complete brand overhaul.</span></span>

<span data-ttu-id="9e06b-117">Прежде чем использовать переопределение файлов CSS, имейте в виду следующие ограничения:</span><span class="sxs-lookup"><span data-stu-id="9e06b-117">Before you use CSS override files, be aware of the following limitations:</span></span>

- <span data-ttu-id="9e06b-118">Только один файл переопределения CSS может быть активен на сайте одновременно.</span><span class="sxs-lookup"><span data-stu-id="9e06b-118">Only one CSS override file can be active on a site at a time.</span></span> <span data-ttu-id="9e06b-119">Таким образом, все активные переопределения должны присутствовать в одном файле переопределения.</span><span class="sxs-lookup"><span data-stu-id="9e06b-119">Therefore, all active overrides must be present in a single override file.</span></span>
- <span data-ttu-id="9e06b-120">Хотя вы можете просмотреть переопределения в инструментах разработки Commerce, нет специальных функций отладки, которые помогут определить ошибки в результате переопределения.</span><span class="sxs-lookup"><span data-stu-id="9e06b-120">Although you can preview the overrides in the Commerce authoring tools, there are no dedicated debugging features to help identify any bugs that the overrides introduce.</span></span> <span data-ttu-id="9e06b-121">Другими словами, при использовании файлов переопределения CSS у вас нет того же набора инструментов, который предусмотрен SDK для проверки модуля и авторства.</span><span class="sxs-lookup"><span data-stu-id="9e06b-121">In other words, when you use CSS override files, you don't have the same toolset that the SDK provides for module and authoring validation.</span></span>

<span data-ttu-id="9e06b-122">Тем не менее, файлы переопределения CSS обеспечивает быстрый способ прототипирования дизайна или устранения ошибок перед разработкой и развертыванием обновления всей темы сразу.</span><span class="sxs-lookup"><span data-stu-id="9e06b-122">Nevertheless, CSS override files provide a quick way to prototype a design or implement a hotfix before a full theme update is developed and deployed.</span></span>

## <a name="create-a-css-override-file"></a><span data-ttu-id="9e06b-123">Создание файла переопределения CSS</span><span class="sxs-lookup"><span data-stu-id="9e06b-123">Create a CSS override file</span></span>

<span data-ttu-id="9e06b-124">Для создания файла переопределения CSS любую интегрированную среду разработки (IDE), текстовый редактор или редактор исходного кода.</span><span class="sxs-lookup"><span data-stu-id="9e06b-124">To create a CSS override file, you can use any integrated development environment (IDE), text editor, or source code editor.</span></span> <span data-ttu-id="9e06b-125">Типичный подход заключается в использовании стандартных веб-отладчиков в браузере для определения селекторов стилей, свойств и значений на существующем сайте.</span><span class="sxs-lookup"><span data-stu-id="9e06b-125">A typical approach is to use standard web debuggers in your browser to identify style selectors, properties, and values on your existing site.</span></span> <span data-ttu-id="9e06b-126">Большинство браузеров позволяют изменять значения и просматривать их в отладчике.</span><span class="sxs-lookup"><span data-stu-id="9e06b-126">Most browsers let you change values and preview them in the debugger.</span></span> <span data-ttu-id="9e06b-127">После того как вы определили изменения, которые вы хотите внести, вы можете сохранить их в свой собственный файл CSS.</span><span class="sxs-lookup"><span data-stu-id="9e06b-127">After you've identified the changes that you want to make, you can save them to your own CSS file.</span></span>

## <a name="upload-a-css-override-file"></a><span data-ttu-id="9e06b-128">Отправка файла переопределения CSS</span><span class="sxs-lookup"><span data-stu-id="9e06b-128">Upload a CSS override file</span></span>

<span data-ttu-id="9e06b-129">Чтобы отправить файл CSS на свой сайт в Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9e06b-129">To upload a CSS file to your site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="9e06b-130">В средствах разработки перейдите на ваш сайт.</span><span class="sxs-lookup"><span data-stu-id="9e06b-130">In the authoring tools, go to your site.</span></span>
1. <span data-ttu-id="9e06b-131">В области переходов слева выберите **Дизайн**.</span><span class="sxs-lookup"><span data-stu-id="9e06b-131">In the navigation pane on the left, select **Design**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9e06b-132">В зависимости от версии инструментов разработки Commerce, которые вы используете, возможно, придется расширить **Настройки** в области перехода, прежде чем вы сможете выбрать **Дизайн**.</span><span class="sxs-lookup"><span data-stu-id="9e06b-132">Depending on the version of the Commerce authoring tools that you're using, you might have to expand **Settings** in the navigation pane before you can select **Design**.</span></span>

1. <span data-ttu-id="9e06b-133">В верхней части основной панели дизайна выберите вкладку **Переопределение CSS**, если она еще не выбрана.</span><span class="sxs-lookup"><span data-stu-id="9e06b-133">At the top of the main design pane, select the **CSS override** tab, if it isn't already selected.</span></span>
1. <span data-ttu-id="9e06b-134">В **Доступные переопределения CSS** выберите **Отправить файл CSS**.</span><span class="sxs-lookup"><span data-stu-id="9e06b-134">Under **Available CSS overrides**, select **Upload CSS file**.</span></span> <span data-ttu-id="9e06b-135">Отображается окно проводника.</span><span class="sxs-lookup"><span data-stu-id="9e06b-135">A File Explorer window appears.</span></span>
1. <span data-ttu-id="9e06b-136">В проводнике найдите и выберите файл CSS, а затем выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="9e06b-136">In File Explorer, browse to and select a CSS file, and then select **Open**.</span></span> <span data-ttu-id="9e06b-137">Отправленный файл CSS теперь отображается в **Доступные переопределения CSS**.</span><span class="sxs-lookup"><span data-stu-id="9e06b-137">The uploaded CSS file now appears under **Available CSS overrides**.</span></span>

## <a name="preview-a-css-override-file"></a><span data-ttu-id="9e06b-138">Предварительный просмотр файла переопределения CSS</span><span class="sxs-lookup"><span data-stu-id="9e06b-138">Preview a CSS override file</span></span>

<span data-ttu-id="9e06b-139">Чтобы просмотреть файл переопределения CSS, прежде чем сделать его активным на своем активном сайте, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9e06b-139">To preview a CSS override file before you make it active on your live site, follow these steps.</span></span>

1. <span data-ttu-id="9e06b-140">В области переходов слева выберите **Дизайн**, а затем на вкладке **Переопределение CSS** в **Доступные переопределенияCSS** найдите файл CSS, который вы хотите просмотреть.</span><span class="sxs-lookup"><span data-stu-id="9e06b-140">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to preview.</span></span>
1. <span data-ttu-id="9e06b-141">Рядом с именем файла CSS выберите **Предварительный просмотр сайта**.</span><span class="sxs-lookup"><span data-stu-id="9e06b-141">Next to the CSS file name, select **Preview site**.</span></span>
1. <span data-ttu-id="9e06b-142">В диалоговом окне **Выберите URL-адрес** выберите URL-адрес сайта, к которому необходимо применить переопределение, а затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e06b-142">In the **Select a URL** dialog box, select the URL of the site that you want to see the override applied to, and then select **OK**.</span></span>
1. <span data-ttu-id="9e06b-143">Если для выбранного URL-адреса существует несколько вариантов, выберите нужный вариант в отображаемом диалоговом окне **Варианты предварительного просмотра**.</span><span class="sxs-lookup"><span data-stu-id="9e06b-143">If there are multiple variants for the selected URL, select the desired variant in the **Preview variations** dialog box that appears.</span></span>

<span data-ttu-id="9e06b-144">Открывается новая вкладка или окно браузера, где можно проверить переопределение на сайте.</span><span class="sxs-lookup"><span data-stu-id="9e06b-144">A new browser tab or window is opened, where you can validate your style overrides against your site.</span></span> <span data-ttu-id="9e06b-145">Затем вы можете поделиться URL-адресом с другими аутентифицированными пользователями Commerce для анализа и обратной связи.</span><span class="sxs-lookup"><span data-stu-id="9e06b-145">You can then share the URL with other authenticated Commerce users for review and feedback.</span></span>

## <a name="activate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="9e06b-146">Активация файла переопределения CSS на своем активном сайте</span><span class="sxs-lookup"><span data-stu-id="9e06b-146">Activate a CSS override file on your live site</span></span>

<span data-ttu-id="9e06b-147">После предварительного просмотра и утверждения файла переопределения CSS вы можете активировать его на своем активном сайте.</span><span class="sxs-lookup"><span data-stu-id="9e06b-147">After you've previewed and approved the CSS override file, you can activate it on your live site.</span></span>

> [!NOTE]
> <span data-ttu-id="9e06b-148">Только один файл переопределения CSS может быть активен на сайте одновременно.</span><span class="sxs-lookup"><span data-stu-id="9e06b-148">Only one CSS override file can be active on your site at a time.</span></span> <span data-ttu-id="9e06b-149">При активации нового файла переопределения предыдущий файл переопределения отключается.</span><span class="sxs-lookup"><span data-stu-id="9e06b-149">If you activate a new override file, the previous override file is inactivated.</span></span> <span data-ttu-id="9e06b-150">Поэтому убедитесь, что все требуемые переопределения присутствуют в едином файле переопределения CSS.</span><span class="sxs-lookup"><span data-stu-id="9e06b-150">Therefore, make sure that all required overrides are present in a single CSS override file.</span></span>

<span data-ttu-id="9e06b-151">Чтобы активировать файл переопределения CSS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9e06b-151">To activate a CSS override file, follow these steps.</span></span>

1. <span data-ttu-id="9e06b-152">В области переходов слева выберите **Дизайн**, а затем на вкладке **Переопределение CSS** в **Доступные переопределенияCSS** найдите файл CSS, который вы хотите активировать.</span><span class="sxs-lookup"><span data-stu-id="9e06b-152">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to activate.</span></span>
1. <span data-ttu-id="9e06b-153">Для имени файла CSS выберите **Активировать**.</span><span class="sxs-lookup"><span data-stu-id="9e06b-153">Under the CSS file name, select **Activate**.</span></span> <span data-ttu-id="9e06b-154">Файл переопределения сразу же становится активным на вашем активном сайте.</span><span class="sxs-lookup"><span data-stu-id="9e06b-154">The override file immediately becomes active on your live site.</span></span>

## <a name="deactivate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="9e06b-155">Отключение файла переопределения CSS на своем активном сайте</span><span class="sxs-lookup"><span data-stu-id="9e06b-155">Deactivate a CSS override file on your live site</span></span>

<span data-ttu-id="9e06b-156">Чтобы отключить файл переопределения CSS на своем сайте, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9e06b-156">To deactivate a CSS override file on your site, follow these steps.</span></span>

1. <span data-ttu-id="9e06b-157">В области переходов слева выберите **Дизайн**, а затем на вкладке **Переопределение CSS** в **Доступные переопределенияCSS** найдите файл CSS, который вы хотите отключить.</span><span class="sxs-lookup"><span data-stu-id="9e06b-157">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to deactivate.</span></span>
1. <span data-ttu-id="9e06b-158">Для имени файла CSS выберите **Отключить**.</span><span class="sxs-lookup"><span data-stu-id="9e06b-158">Under the CSS file name, select **Deactivate**.</span></span> <span data-ttu-id="9e06b-159">Файл переопределения сразу же становится неактивным на вашем активном сайте.</span><span class="sxs-lookup"><span data-stu-id="9e06b-159">The override file immediately becomes inactive on your live site.</span></span>

> [!TIP]
> <span data-ttu-id="9e06b-160">Чтобы получить доступ к дополнительным параметрам для файлов переопределения CSS, выберите многоточие (**...**) рядом с именем файла CSS.</span><span class="sxs-lookup"><span data-stu-id="9e06b-160">To access additional options for CSS override files, select the ellipsis (**...**) next to the CSS file name.</span></span> <span data-ttu-id="9e06b-161">Параметры **Загрузить**, **Переименовать** и **Заменить** используются для внесения быстрых изменений в существующий файл переопределения CSS.</span><span class="sxs-lookup"><span data-stu-id="9e06b-161">The **Download**, **Rename**, and **Replace** options are useful for quick changes to an existing CSS override file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9e06b-162">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9e06b-162">Additional resources</span></span>

[<span data-ttu-id="9e06b-163">Добавление логотипа</span><span class="sxs-lookup"><span data-stu-id="9e06b-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="9e06b-164">Выбор темы сайта</span><span class="sxs-lookup"><span data-stu-id="9e06b-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="9e06b-165">Работа с предустановками стилей</span><span class="sxs-lookup"><span data-stu-id="9e06b-165">Work with style presets</span></span>](style-presets.md)

[<span data-ttu-id="9e06b-166">Добавление значка сайта</span><span class="sxs-lookup"><span data-stu-id="9e06b-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="9e06b-167">Добавление приветственного сообщения</span><span class="sxs-lookup"><span data-stu-id="9e06b-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="9e06b-168">Добавление уведомления об авторском праве</span><span class="sxs-lookup"><span data-stu-id="9e06b-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="9e06b-169">Добавление языков на сайт</span><span class="sxs-lookup"><span data-stu-id="9e06b-169">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="9e06b-170">Добавление кода скрипта на страницы сайта для поддержки телеметрии</span><span class="sxs-lookup"><span data-stu-id="9e06b-170">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)
