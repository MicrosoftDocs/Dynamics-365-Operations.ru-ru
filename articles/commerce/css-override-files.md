---
title: Работа с переопределением файлов CSS
description: В этой теме описывается, почему, когда и как использовать файлы переопределения каскадных таблиц стилей (CSS) переопределить файлы в Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ef96070fe77b46622667301c7c7c402909ee7dfc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799501"
---
# <a name="work-with-css-override-files"></a><span data-ttu-id="cbc8d-103">Работа с переопределением файлов CSS</span><span class="sxs-lookup"><span data-stu-id="cbc8d-103">Work with CSS override files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cbc8d-104">В этой теме описывается, почему, когда и как использовать файлы переопределения каскадных таблиц стилей (CSS) переопределить файлы в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-104">This topic describes why, when, and how to use Cascading Style Sheets (CSS) override files in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="cbc8d-105">Постоянные стили сайта, как правило, должны быть обработаны через тему сайта.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-105">Permanent site styles should usually be handled through a site's theme.</span></span> <span data-ttu-id="cbc8d-106">Темы обеспечивают основы CSS и настройки стиля для модулей на любой странице вашего сайта.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-106">Themes provide the foundational CSS and style settings for the modules on any page of your site.</span></span> <span data-ttu-id="cbc8d-107">Темы создаются с помощью онлайн-пакета средств разработки Dynamics 365 Commerce (SDK), и они развернуты на ваших веб-сайтах через Lifecycle Services Microsoft Dynamics (LCS).</span><span class="sxs-lookup"><span data-stu-id="cbc8d-107">Themes are created by using the Dynamics 365 Commerce online software development kit (SDK), and they are deployed to your websites through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="cbc8d-108">Возможности отладки тем и конфигурации интерфейса модуля в SDK помогают разработчикам сайтов создавать настраиваемые и связанные пакеты дизайна сайта.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-108">Theme debugging capabilities and module interface configurations in the SDK help site developers create customizable and cohesive site design packages.</span></span> <span data-ttu-id="cbc8d-109">Когда эти пакеты дизайна развертываются на сайте, авторы сайта могут сосредоточиться на создании, редактировании и публикации контента вместо разработки сайта.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-109">When these design packages are deployed to a site, site authors can focus on creating, editing, and publishing content instead of site development.</span></span>

<span data-ttu-id="cbc8d-110">Учитывая обычный жизненный цикл темы, зависимость от разработчиков в плане изменения стиля через конвейер развертывания SDK и LCS может быть непомерно высокой в некоторых сценариях.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-110">Given the usual lifecycle of a theme, the dependency on developers to make style changes through the SDK and LCS deployment pipeline can be prohibitive in some scenarios.</span></span> <span data-ttu-id="cbc8d-111">Прототипы или исправления ошибок сайта могут показаться громоздкими, если SDK не настроен или если у вас нет времени ждать развертывания LCS.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-111">Site prototypes or hotfixes can seem cumbersome if the SDK isn't configured, or if you don't have time to wait for an LCS deployment.</span></span>

<span data-ttu-id="cbc8d-112">В этих сценариях переопределение файлов CSS может помочь.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-112">In these scenarios, CSS override files can help.</span></span> <span data-ttu-id="cbc8d-113">В инструментах разработки Commerce аутентифицированные пользователи могут отправить файл CSS, просмотреть его, а затем активировать, чтобы переопределить тему сайта.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-113">In the Commerce authoring tools, authenticated users can upload a CSS file, preview it, and then activate it to override a site's theme.</span></span> <span data-ttu-id="cbc8d-114">Накладные расходы на развертывание SDK или LCS не требуются.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-114">The overhead of SDK or LCS deployment isn't required.</span></span> <span data-ttu-id="cbc8d-115">Переопределения, указанные в файле переопределения CSS, могут быть всего лишь изменением одного стиля текста или полной капитальной переделкой бренда.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-115">The overrides that are specified in a CSS override file can be as small as a change to a single text style or as wide-ranging as a complete brand overhaul.</span></span>

<span data-ttu-id="cbc8d-116">Прежде чем использовать переопределение файлов CSS, имейте в виду следующие ограничения:</span><span class="sxs-lookup"><span data-stu-id="cbc8d-116">Before you use CSS override files, be aware of the following limitations:</span></span>

- <span data-ttu-id="cbc8d-117">Только один файл переопределения CSS может быть активен на сайте одновременно.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-117">Only one CSS override file can be active on a site at a time.</span></span> <span data-ttu-id="cbc8d-118">Таким образом, все активные переопределения должны присутствовать в одном файле переопределения.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-118">Therefore, all active overrides must be present in a single override file.</span></span>
- <span data-ttu-id="cbc8d-119">Хотя вы можете просмотреть переопределения в инструментах разработки Commerce, нет специальных функций отладки, которые помогут определить ошибки в результате переопределения.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-119">Although you can preview the overrides in the Commerce authoring tools, there are no dedicated debugging features to help identify any bugs that the overrides introduce.</span></span> <span data-ttu-id="cbc8d-120">Другими словами, при использовании файлов переопределения CSS у вас нет того же набора инструментов, который предусмотрен SDK для проверки модуля и авторства.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-120">In other words, when you use CSS override files, you don't have the same toolset that the SDK provides for module and authoring validation.</span></span>

<span data-ttu-id="cbc8d-121">Тем не менее, файлы переопределения CSS обеспечивает быстрый способ прототипирования дизайна или устранения ошибок перед разработкой и развертыванием обновления всей темы сразу.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-121">Nevertheless, CSS override files provide a quick way to prototype a design or implement a hotfix before a full theme update is developed and deployed.</span></span>

## <a name="create-a-css-override-file"></a><span data-ttu-id="cbc8d-122">Создание файла переопределения CSS</span><span class="sxs-lookup"><span data-stu-id="cbc8d-122">Create a CSS override file</span></span>

<span data-ttu-id="cbc8d-123">Для создания файла переопределения CSS любую интегрированную среду разработки (IDE), текстовый редактор или редактор исходного кода.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-123">To create a CSS override file, you can use any integrated development environment (IDE), text editor, or source code editor.</span></span> <span data-ttu-id="cbc8d-124">Типичный подход заключается в использовании стандартных веб-отладчиков в браузере для определения селекторов стилей, свойств и значений на существующем сайте.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-124">A typical approach is to use standard web debuggers in your browser to identify style selectors, properties, and values on your existing site.</span></span> <span data-ttu-id="cbc8d-125">Большинство браузеров позволяют изменять значения и просматривать их в отладчике.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-125">Most browsers let you change values and preview them in the debugger.</span></span> <span data-ttu-id="cbc8d-126">После того как вы определили изменения, которые вы хотите внести, вы можете сохранить их в свой собственный файл CSS.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-126">After you've identified the changes that you want to make, you can save them to your own CSS file.</span></span>

## <a name="upload-a-css-override-file"></a><span data-ttu-id="cbc8d-127">Отправка файла переопределения CSS</span><span class="sxs-lookup"><span data-stu-id="cbc8d-127">Upload a CSS override file</span></span>

<span data-ttu-id="cbc8d-128">Чтобы отправить файл CSS на свой сайт в Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-128">To upload a CSS file to your site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="cbc8d-129">В средствах разработки перейдите на ваш сайт.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-129">In the authoring tools, go to your site.</span></span>
1. <span data-ttu-id="cbc8d-130">В области переходов слева выберите **Дизайн**.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-130">In the navigation pane on the left, select **Design**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cbc8d-131">В зависимости от версии инструментов разработки Commerce, которые вы используете, возможно, придется расширить **Настройки** в области перехода, прежде чем вы сможете выбрать **Дизайн**.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-131">Depending on the version of the Commerce authoring tools that you're using, you might have to expand **Settings** in the navigation pane before you can select **Design**.</span></span>

1. <span data-ttu-id="cbc8d-132">В верхней части основной панели дизайна выберите вкладку **Переопределение CSS**, если она еще не выбрана.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-132">At the top of the main design pane, select the **CSS override** tab, if it isn't already selected.</span></span>
1. <span data-ttu-id="cbc8d-133">В **Доступные переопределения CSS** выберите **Отправить файл CSS**.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-133">Under **Available CSS overrides**, select **Upload CSS file**.</span></span> <span data-ttu-id="cbc8d-134">Отображается окно проводника.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-134">A File Explorer window appears.</span></span>
1. <span data-ttu-id="cbc8d-135">В проводнике найдите и выберите файл CSS, а затем выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-135">In File Explorer, browse to and select a CSS file, and then select **Open**.</span></span> <span data-ttu-id="cbc8d-136">Отправленный файл CSS теперь отображается в **Доступные переопределения CSS**.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-136">The uploaded CSS file now appears under **Available CSS overrides**.</span></span>

## <a name="preview-a-css-override-file"></a><span data-ttu-id="cbc8d-137">Предварительный просмотр файла переопределения CSS</span><span class="sxs-lookup"><span data-stu-id="cbc8d-137">Preview a CSS override file</span></span>

<span data-ttu-id="cbc8d-138">Чтобы просмотреть файл переопределения CSS, прежде чем сделать его активным на своем активном сайте, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-138">To preview a CSS override file before you make it active on your live site, follow these steps.</span></span>

1. <span data-ttu-id="cbc8d-139">В области переходов слева выберите **Дизайн**, а затем на вкладке **Переопределение CSS** в **Доступные переопределенияCSS** найдите файл CSS, который вы хотите просмотреть.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-139">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to preview.</span></span>
1. <span data-ttu-id="cbc8d-140">Рядом с именем файла CSS выберите **Предварительный просмотр сайта**.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-140">Next to the CSS file name, select **Preview site**.</span></span>
1. <span data-ttu-id="cbc8d-141">В диалоговом окне **Выберите URL-адрес** выберите URL-адрес сайта, к которому необходимо применить переопределение, а затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-141">In the **Select a URL** dialog box, select the URL of the site that you want to see the override applied to, and then select **OK**.</span></span>
1. <span data-ttu-id="cbc8d-142">Если для выбранного URL-адреса существует несколько вариантов, выберите нужный вариант в отображаемом диалоговом окне **Варианты предварительного просмотра**.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-142">If there are multiple variants for the selected URL, select the desired variant in the **Preview variations** dialog box that appears.</span></span>

<span data-ttu-id="cbc8d-143">Открывается новая вкладка или окно браузера, где можно проверить переопределение на сайте.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-143">A new browser tab or window is opened, where you can validate your style overrides against your site.</span></span> <span data-ttu-id="cbc8d-144">Затем вы можете поделиться URL-адресом с другими аутентифицированными пользователями Commerce для анализа и обратной связи.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-144">You can then share the URL with other authenticated Commerce users for review and feedback.</span></span>

## <a name="activate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="cbc8d-145">Активация файла переопределения CSS на своем активном сайте</span><span class="sxs-lookup"><span data-stu-id="cbc8d-145">Activate a CSS override file on your live site</span></span>

<span data-ttu-id="cbc8d-146">После предварительного просмотра и утверждения файла переопределения CSS вы можете активировать его на своем активном сайте.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-146">After you've previewed and approved the CSS override file, you can activate it on your live site.</span></span>

> [!NOTE]
> <span data-ttu-id="cbc8d-147">Только один файл переопределения CSS может быть активен на сайте одновременно.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-147">Only one CSS override file can be active on your site at a time.</span></span> <span data-ttu-id="cbc8d-148">При активации нового файла переопределения предыдущий файл переопределения отключается.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-148">If you activate a new override file, the previous override file is inactivated.</span></span> <span data-ttu-id="cbc8d-149">Поэтому убедитесь, что все требуемые переопределения присутствуют в едином файле переопределения CSS.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-149">Therefore, make sure that all required overrides are present in a single CSS override file.</span></span>

<span data-ttu-id="cbc8d-150">Чтобы активировать файл переопределения CSS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-150">To activate a CSS override file, follow these steps.</span></span>

1. <span data-ttu-id="cbc8d-151">В области переходов слева выберите **Дизайн**, а затем на вкладке **Переопределение CSS** в **Доступные переопределенияCSS** найдите файл CSS, который вы хотите активировать.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-151">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to activate.</span></span>
1. <span data-ttu-id="cbc8d-152">Для имени файла CSS выберите **Активировать**.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-152">Under the CSS file name, select **Activate**.</span></span> <span data-ttu-id="cbc8d-153">Файл переопределения сразу же становится активным на вашем активном сайте.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-153">The override file immediately becomes active on your live site.</span></span>

## <a name="deactivate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="cbc8d-154">Отключение файла переопределения CSS на своем активном сайте</span><span class="sxs-lookup"><span data-stu-id="cbc8d-154">Deactivate a CSS override file on your live site</span></span>

<span data-ttu-id="cbc8d-155">Чтобы отключить файл переопределения CSS на своем сайте, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-155">To deactivate a CSS override file on your site, follow these steps.</span></span>

1. <span data-ttu-id="cbc8d-156">В области переходов слева выберите **Дизайн**, а затем на вкладке **Переопределение CSS** в **Доступные переопределенияCSS** найдите файл CSS, который вы хотите отключить.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-156">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to deactivate.</span></span>
1. <span data-ttu-id="cbc8d-157">Для имени файла CSS выберите **Отключить**.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-157">Under the CSS file name, select **Deactivate**.</span></span> <span data-ttu-id="cbc8d-158">Файл переопределения сразу же становится неактивным на вашем активном сайте.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-158">The override file immediately becomes inactive on your live site.</span></span>

> [!TIP]
> <span data-ttu-id="cbc8d-159">Чтобы получить доступ к дополнительным параметрам для файлов переопределения CSS, выберите многоточие (**...**) рядом с именем файла CSS.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-159">To access additional options for CSS override files, select the ellipsis (**...**) next to the CSS file name.</span></span> <span data-ttu-id="cbc8d-160">Параметры **Загрузить**, **Переименовать** и **Заменить** используются для внесения быстрых изменений в существующий файл переопределения CSS.</span><span class="sxs-lookup"><span data-stu-id="cbc8d-160">The **Download**, **Rename**, and **Replace** options are useful for quick changes to an existing CSS override file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cbc8d-161">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cbc8d-161">Additional resources</span></span>

[<span data-ttu-id="cbc8d-162">Добавление логотипа</span><span class="sxs-lookup"><span data-stu-id="cbc8d-162">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="cbc8d-163">Выбор темы сайта</span><span class="sxs-lookup"><span data-stu-id="cbc8d-163">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="cbc8d-164">Работа с предустановками стилей</span><span class="sxs-lookup"><span data-stu-id="cbc8d-164">Work with style presets</span></span>](style-presets.md)

[<span data-ttu-id="cbc8d-165">Добавление значка сайта</span><span class="sxs-lookup"><span data-stu-id="cbc8d-165">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="cbc8d-166">Добавление приветственного сообщения</span><span class="sxs-lookup"><span data-stu-id="cbc8d-166">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="cbc8d-167">Добавление уведомления об авторском праве</span><span class="sxs-lookup"><span data-stu-id="cbc8d-167">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="cbc8d-168">Добавление языков на сайт</span><span class="sxs-lookup"><span data-stu-id="cbc8d-168">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="cbc8d-169">Добавление кода скрипта на страницы сайта для поддержки телеметрии</span><span class="sxs-lookup"><span data-stu-id="cbc8d-169">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
