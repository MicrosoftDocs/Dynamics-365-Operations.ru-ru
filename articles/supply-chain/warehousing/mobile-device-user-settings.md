---
title: Параметры пользователя мобильного устройства
description: В этой теме объясняется, как управлять настройками пользователя мобильного устройства для складских работников.
author: MarkusFogelberg
manager: tfehr
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppDeviceBrand,WHSMobileAppUserDisplaySettings
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: mafoge
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8090305c1b296d8a8a64df444abb1d1f2235aeee
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501206"
---
# <a name="mobile-device-user-settings"></a><span data-ttu-id="54567-103">Параметры пользователя мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="54567-103">Mobile device user settings</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="54567-104">В новом мобильном приложении "Управление складом" есть набор параметров, относящихся к приложению, которые помогают адаптировать взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="54567-104">The new Warehouse Management mobile app has a set of app-specific settings that help tailor the user experience.</span></span> <span data-ttu-id="54567-105">Так как приложение может использоваться на устройствах различных размеров и конфигураций экрана (например, планшеты, телефоны и др.), может быть полезно централизованно управлять этими параметрами в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="54567-105">Because the app can be used on devices of different screen sizes and configurations (such as tablet, phone, or arm-held), it can be useful to centrally manage these settings from Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="54567-106">Функция *настроек пользователя мобильного устройства* позволяет определить глобальные параметры пользователя, которые будут использоваться на всех устройствах.</span><span class="sxs-lookup"><span data-stu-id="54567-106">The *mobile device user settings* feature lets you define global user settings that will be used on all devices.</span></span> <span data-ttu-id="54567-107">Кроме того, можно определить более детализированные пользовательские настройки для отдельных торговых марок устройств, моделей устройств и/или сотрудников.</span><span class="sxs-lookup"><span data-stu-id="54567-107">You can also define more granular user settings for individual device brands, device models, and/or workers.</span></span> <span data-ttu-id="54567-108">Когда работник выполняет вход в мобильное приложение "Управление складом", приложение получает и применяет наиболее подходящий профиль параметров, который хранится в Supply Chain Management для соответствующих торговой марки, устройства и/или ИД пользователя.</span><span class="sxs-lookup"><span data-stu-id="54567-108">When a worker signs in to the Warehouse Management mobile app, the app fetches and applies the most specific settings profile that is stored in Supply Chain Management for the matching brand, device, and/or user ID.</span></span>

<span data-ttu-id="54567-109">Эта функция помогает сотрудникам быстрее начать работу, когда они начинают использовать новое устройство.</span><span class="sxs-lookup"><span data-stu-id="54567-109">This feature can help workers get started more quickly whenever they begin to use a new device.</span></span> <span data-ttu-id="54567-110">Далее приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="54567-110">Here are some examples:</span></span>

- <span data-ttu-id="54567-111">Администраторы могут установить стандартный набор предпочтений, которые наилучшим образом подходят для устройств от конкретного производителя и/или для конкретной модели устройств.</span><span class="sxs-lookup"><span data-stu-id="54567-111">Admins can establish a standard set of preferences that work best for devices from a specific manufacturer and/or for specific device models.</span></span> <span data-ttu-id="54567-112">Таким образом, работники могут начать работу с новым устройством без изменения настроек.</span><span class="sxs-lookup"><span data-stu-id="54567-112">Therefore, workers can get started with a new device without necessarily having to change the settings.</span></span>
- <span data-ttu-id="54567-113">Если у вашей компании есть набор идентичных устройств, которые являются общими для работников, работники будут видеть предпочитаемую настройку каждый раз, когда они выполняют вход, даже если они никогда не использовали определенное физическое устройство, выбранное в данный день.</span><span class="sxs-lookup"><span data-stu-id="54567-113">If your company has a pool of identical devices that are shared among workers, workers will see their preferred setup every time that they sign in, even if they have never used the specific physical device that they selected on a given day.</span></span>
- <span data-ttu-id="54567-114">В Supply Chain Management администраторы могут просматривать и редактировать все сохраненные настройки, даже для отдельных работников.</span><span class="sxs-lookup"><span data-stu-id="54567-114">In Supply Chain Management, admins can view and edit all stored settings, even for individual workers.</span></span> <span data-ttu-id="54567-115">Эта возможность может помочь в устранении неполадок или тонкой настройке новых функций.</span><span class="sxs-lookup"><span data-stu-id="54567-115">This capability can help them troubleshoot or fine-tune new features.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="54567-116">Функция *пользовательских настроек мобильного устройства* применяется только к новому мобильному приложению "Управление складом".</span><span class="sxs-lookup"><span data-stu-id="54567-116">The *mobile device user settings* feature applies only to the new Warehouse Management mobile app.</span></span> <span data-ttu-id="54567-117">Она не работает со старым приложением склада.</span><span class="sxs-lookup"><span data-stu-id="54567-117">It doesn't work with the old warehouse app.</span></span>

## <a name="turn-on-the-mobile-device-user-settings-feature"></a><span data-ttu-id="54567-118">Включите функцию пользовательских настроек мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="54567-118">Turn on the mobile device user settings feature</span></span>

<span data-ttu-id="54567-119">Прежде чем использовать эту функцию, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="54567-119">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="54567-120">Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения.</span><span class="sxs-lookup"><span data-stu-id="54567-120">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="54567-121">В рабочей области **Управление функциями** эта функция перечисляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="54567-121">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="54567-122">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="54567-122">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="54567-123">**Название компонента:** *Параметры пользователя, значки и названия шагов для нового приложения склада*</span><span class="sxs-lookup"><span data-stu-id="54567-123">**Feature name:** *User settings, icons, and step titles for the new warehouse app*</span></span>

## <a name="create-and-manage-user-settings"></a><span data-ttu-id="54567-124">Создание пользовательских настроек и управление ими</span><span class="sxs-lookup"><span data-stu-id="54567-124">Create and manage user settings</span></span>

<span data-ttu-id="54567-125">Страница **Пользовательские настройки мобильного устройства** используется для создания, просмотра и управления профилями настроек на всех уровнях детализации.</span><span class="sxs-lookup"><span data-stu-id="54567-125">Use the **Mobile device user settings** page to create, view, and manage settings profiles at all levels of granularity.</span></span> <span data-ttu-id="54567-126">При первом изменении пользователем своих пользовательских настроек на новом устройстве автоматически добавляется новый профиль на этой странице, если он еще не существует.</span><span class="sxs-lookup"><span data-stu-id="54567-126">The first time that a worker edits their user settings on a new device, a new profile is automatically added on this page, if it doesn't already exist.</span></span> <span data-ttu-id="54567-127">Затем этот профиль обновляется каждый раз, когда работник вносит изменения.</span><span class="sxs-lookup"><span data-stu-id="54567-127">That profile is then updated every time that the worker makes a change.</span></span>

<span data-ttu-id="54567-128">Кроме того, можно определить профиль настроек для всех торговых марок устройств, моделей устройств и/или сотрудников.</span><span class="sxs-lookup"><span data-stu-id="54567-128">You can also define a settings profile that applies to all device brands, device models, and/or workers.</span></span> <span data-ttu-id="54567-129">Затем можно увеличить детализацию, применяя более конкретные настройки для отдельных торговых марок, моделей и/или сотрудников.</span><span class="sxs-lookup"><span data-stu-id="54567-129">You can then increase the granularity by applying more specific settings for individual brands, models, and/or workers.</span></span>

<span data-ttu-id="54567-130">Выполните следующие действия, чтобы создать пользовательские настройки для мобильных устройств и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="54567-130">Follow these steps to create and manage user settings for your mobile devices.</span></span>

1. <span data-ttu-id="54567-131">Перейдите в раздел **Управление складом \> Мобильное устройство \> Пользовательские параметры мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="54567-131">Go to **Warehouse management \> Mobile device \> Mobile device user settings**.</span></span>
1. <span data-ttu-id="54567-132">Выберите существующий профиль пользовательских параметров в области списка, чтобы открыть его запись.</span><span class="sxs-lookup"><span data-stu-id="54567-132">Select an existing user settings profile in the list pane to open its record.</span></span> <span data-ttu-id="54567-133">Или выберите **Создать** в области действий, чтобы создать новый профиль.</span><span class="sxs-lookup"><span data-stu-id="54567-133">Alternatively, select **New** on the Action Pane to create a new profile.</span></span>

    <span data-ttu-id="54567-134">Каждый профиль в панели списка помечен для обозначения торговой марки, модели и/или ИД пользователя, к которым применяется данный профиль.</span><span class="sxs-lookup"><span data-stu-id="54567-134">Each profile in the list pane is labeled to indicate the brand, model, and/or user ID that the profile applies to.</span></span> <span data-ttu-id="54567-135">У более общих профилей есть значение *Все* для некоторых или всех этих характеристик.</span><span class="sxs-lookup"><span data-stu-id="54567-135">More general profiles have a value of *All* for some or all of these characteristics.</span></span>

1. <span data-ttu-id="54567-136">В разделе заголовков записи для нового или выбранного профиля настроек задайте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="54567-136">In the header section of the record for the new or selected settings profile, set the following fields:</span></span>

    - <span data-ttu-id="54567-137">**Название торговой марки устройства** — выберите название торговой марки устройства, к которому должен применяться данный профиль.</span><span class="sxs-lookup"><span data-stu-id="54567-137">**Device brand name** – Select the device brand name that the profile should apply to.</span></span> <span data-ttu-id="54567-138">Если профиль должен применяться ко всем торговым маркам, оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="54567-138">If the profile should apply to all brands, leave this field blank.</span></span> <span data-ttu-id="54567-139">Список значений включает все торговые марки, которые были определены в системе.</span><span class="sxs-lookup"><span data-stu-id="54567-139">The list of values includes all the brands that have been defined in your system.</span></span> <span data-ttu-id="54567-140">Сведения об определении списка торговых марок см. в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="54567-140">For information about how to define the list of brands, see the next section.</span></span>
    - <span data-ttu-id="54567-141">**Код модели устройства** — выберите модель устройства, к которому должен применяться данный профиль.</span><span class="sxs-lookup"><span data-stu-id="54567-141">**Device model ID** – Select the device model that the profile should apply to.</span></span> <span data-ttu-id="54567-142">Если профиль должен применяться ко моделям выбранной торговой марки, оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="54567-142">If the profile should apply to all models of the selected brand, leave this field blank.</span></span> <span data-ttu-id="54567-143">Список значений включает все модели, которые были определены для торговой марки, выбранной в поле **Название торговой марки устройства**.</span><span class="sxs-lookup"><span data-stu-id="54567-143">The list of values includes all the models that have been defined for the brand that is selected in the **Device brand name** field.</span></span> <span data-ttu-id="54567-144">Сведения об определении списка моделей для каждой торговой марки см. в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="54567-144">For information about how to define the list of models for each brand, see the next section.</span></span>
    - <span data-ttu-id="54567-145">**ИД пользователя** — выберите ИД пользователя складского работника, к которому должен применяться этот профиль настройки.</span><span class="sxs-lookup"><span data-stu-id="54567-145">**User ID** – Select the user ID of the warehouse worker that the setting profile should apply to.</span></span> <span data-ttu-id="54567-146">Если профиль должен применяться ко всем сотрудникам, оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="54567-146">If the profile should apply to all workers, leave this field blank.</span></span>

1. <span data-ttu-id="54567-147">На экспресс-вкладке **Общие** настройте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="54567-147">On the **General** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="54567-148">**Положение кнопки** — выберите способ расположения кнопок на устройстве.</span><span class="sxs-lookup"><span data-stu-id="54567-148">**Button position** – Select how buttons should be positioned on the device.</span></span> <span data-ttu-id="54567-149">Элементы в приложении будут перемещены, чтобы лучше соответствовать предпочтению или удобству работника.</span><span class="sxs-lookup"><span data-stu-id="54567-149">Elements in the app will be moved to better fit the preference or handedness of the worker.</span></span> <span data-ttu-id="54567-150">Доступные параметры — *Нижний правый (по умолчанию)*, *Нижний левый*, *Верхний правый* и *Верхний левый*.</span><span class="sxs-lookup"><span data-stu-id="54567-150">The available options are *Bottom right (default)*, *Bottom left*, *Top right*, and *Top left*.</span></span>
    - <span data-ttu-id="54567-151">**Ориентация дисплея** — выберите ориентацию дисплея, которая должна применяться по умолчанию в приложении.</span><span class="sxs-lookup"><span data-stu-id="54567-151">**Display orientation** – Select the display orientation that should be applied by default in the app.</span></span>
    - <span data-ttu-id="54567-152">**Сканировать камерой** — установите этот параметр как *Да*, чтобы использовать камеру устройства для сканирования полей ввода, если предпочтительным режимом ввода является *Сканирование*.</span><span class="sxs-lookup"><span data-stu-id="54567-152">**Scan with camera** – Set this option to *Yes* to use the device camera to scan input fields where the preferred input mode is set to *Scanning*.</span></span> <span data-ttu-id="54567-153">Если устройство оснащено встроенным сканером, установите для этого параметра значение *Нет*, чтобы использовать сканер.</span><span class="sxs-lookup"><span data-stu-id="54567-153">If your device has a built-in scanner, set this option to *No* to use the scanner instead.</span></span>
    - <span data-ttu-id="54567-154">**Показать фотографию продукта** — выберите, должны ли отображаться фотографии продуктов, если они доступны для выпущенного продукта.</span><span class="sxs-lookup"><span data-stu-id="54567-154">**Show product photo** – Select whether product photos should be shown if they are available for the released product.</span></span> <span data-ttu-id="54567-155">Дополнительные сведения о добавлении изображений продуктов см. в разделе [Добавление изображения к продукту](../pim/tasks/add-image-product.md).</span><span class="sxs-lookup"><span data-stu-id="54567-155">For more information about how to add product images, see [Add an image to a product](../pim/tasks/add-image-product.md).</span></span>
    - <span data-ttu-id="54567-156">**Цветовая тема дисплея** — выберите цветовую тему для устройства.</span><span class="sxs-lookup"><span data-stu-id="54567-156">**Display color theme** – Select a color theme for the device.</span></span>
    - <span data-ttu-id="54567-157">**Уровень громкости** — выберите уровень громкости для устройства.</span><span class="sxs-lookup"><span data-stu-id="54567-157">**Sound level** – Select the sound level for the device.</span></span> <span data-ttu-id="54567-158">Выберите значение от 0 (ноль) до 10.</span><span class="sxs-lookup"><span data-stu-id="54567-158">Select a value between 0 (zero) and 10.</span></span> <span data-ttu-id="54567-159">Значение *0* означает "без звука", а значение *10* — максимальная громкость.</span><span class="sxs-lookup"><span data-stu-id="54567-159">A value of *0* represents no sound, and a value of *10* represents maximum volume.</span></span> <span data-ttu-id="54567-160">Значение по умолчанию — *4*.</span><span class="sxs-lookup"><span data-stu-id="54567-160">The default value is *4*.</span></span>
    - <span data-ttu-id="54567-161">**Уровень вибрации** — выберите уровень вибрации для устройства.</span><span class="sxs-lookup"><span data-stu-id="54567-161">**Vibration level** – Select the vibration level for the device.</span></span> <span data-ttu-id="54567-162">Выберите значение от 0 (ноль) до 5.</span><span class="sxs-lookup"><span data-stu-id="54567-162">Select a value between 0 (zero) and 5.</span></span> <span data-ttu-id="54567-163">Значение *0* означает "без вибрации", а значение *5* — максимальная вибрация.</span><span class="sxs-lookup"><span data-stu-id="54567-163">A value of *0* represents no vibration, and a value of *5* represents maximum vibration.</span></span> <span data-ttu-id="54567-164">Значение по умолчанию — *1*.</span><span class="sxs-lookup"><span data-stu-id="54567-164">The default value is *1*.</span></span>
    - <span data-ttu-id="54567-165">**Процент масштабирования текста** — укажите размер текста в процентах от стандартного размера.</span><span class="sxs-lookup"><span data-stu-id="54567-165">**Text scale percentage** – Specify the text size as a percentage of the standard size.</span></span> <span data-ttu-id="54567-166">Введите значение от 70 до 400.</span><span class="sxs-lookup"><span data-stu-id="54567-166">Enter a value between 70 and 400.</span></span> <span data-ttu-id="54567-167">Значение *70* означает наименьший масштаб текста, а значение *400* — наибольший масштаб текста.</span><span class="sxs-lookup"><span data-stu-id="54567-167">A value of *70* represents the smallest text scale, and a value of *400* represents the largest text scale.</span></span> <span data-ttu-id="54567-168">Значение по умолчанию — *100*.</span><span class="sxs-lookup"><span data-stu-id="54567-168">The default value is *100*.</span></span>
    - <span data-ttu-id="54567-169">**Процент масштабирования кнопок** — укажите размер кнопок в процентах от стандартного размера.</span><span class="sxs-lookup"><span data-stu-id="54567-169">**Button scale percentage** – Specify the button size as a percentage of the standard size.</span></span> <span data-ttu-id="54567-170">Введите значение от 50 до 200.</span><span class="sxs-lookup"><span data-stu-id="54567-170">Enter a value between 50 and 200.</span></span> <span data-ttu-id="54567-171">Значение *50* означает наименьший масштаб кнопок, а значение *200* — наибольший масштаб кнопок.</span><span class="sxs-lookup"><span data-stu-id="54567-171">A value of *50* represents the smallest button scale, and a value of *200* represents the largest button scale.</span></span> <span data-ttu-id="54567-172">Значение по умолчанию — *100*.</span><span class="sxs-lookup"><span data-stu-id="54567-172">The default value is *100*.</span></span>

## <a name="create-and-manage-mobile-device-brands"></a><span data-ttu-id="54567-173">Создание торговых марок мобильных устройств и управление ими</span><span class="sxs-lookup"><span data-stu-id="54567-173">Create and manage mobile device brands</span></span>

<span data-ttu-id="54567-174">Страница **Торговые марки мобильного устройства** предназначена для просмотра, создания и управления торговыми марками и моделями устройств, которые могут использоваться с профилями настроек.</span><span class="sxs-lookup"><span data-stu-id="54567-174">Use the **Mobile device brands** page to view, create, and manage the device brands and models that can be used with your settings profiles.</span></span> <span data-ttu-id="54567-175">Мобильное приложение автоматически получает и передает имя локальной торговой марки и код модели при первом изменении параметров на данном устройстве работником.</span><span class="sxs-lookup"><span data-stu-id="54567-175">The mobile app automatically fetches and submits the local brand name and model ID the first time that a worker edits their settings on a given device.</span></span> <span data-ttu-id="54567-176">Поэтому большая часть этих записей обычно будет создаваться автоматически.</span><span class="sxs-lookup"><span data-stu-id="54567-176">Therefore, most of these records will usually be automatically generated.</span></span> <span data-ttu-id="54567-177">Однако можно также управлять всеми записями на этой странице.</span><span class="sxs-lookup"><span data-stu-id="54567-177">However, you can also manage all the records on this page.</span></span> <span data-ttu-id="54567-178">Например, можно присвоить более подробное описание каждой торговой марки и модели, чтобы отличать аналогичные и криптографически закрытые коды моделей.</span><span class="sxs-lookup"><span data-stu-id="54567-178">For example, you can give more useful descriptions to each brand and model to help distinguish similar or cryptic model IDs.</span></span>

<span data-ttu-id="54567-179">Выполните следующие действия, чтобы создать пользовательские торговые марки и модели мобильных устройств и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="54567-179">Follow these steps to create and manage your mobile device brands and models.</span></span>

1. <span data-ttu-id="54567-180">Перейдите в раздел **Управление складом \> Мобильное устройство \> Торговые марки мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="54567-180">Go to **Warehouse management \> Mobile device \> Mobile device brands**.</span></span>
1. <span data-ttu-id="54567-181">В области списка выберите торговую марку мобильного устройства, чтобы открыть его запись.</span><span class="sxs-lookup"><span data-stu-id="54567-181">In the list pane, select a mobile device brand to open its record.</span></span> <span data-ttu-id="54567-182">Или выберите **Создать** в области действий, чтобы создать новую торговую марку.</span><span class="sxs-lookup"><span data-stu-id="54567-182">Alternatively, select **New** on the Action Pane to create a new brand.</span></span>
1. <span data-ttu-id="54567-183">В разделе заголовков записи для новой или выбранной торговой марки устройства задайте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="54567-183">In the header section of the record for the new or selected device brand, set the following fields:</span></span>

    - <span data-ttu-id="54567-184">**Торговая марка устройства** — название торговой марки устройства, например, *корпорация Майкрософт*.</span><span class="sxs-lookup"><span data-stu-id="54567-184">**Device brand name** – The brand name of the device, such as *Microsoft Corporation*.</span></span>
    - <span data-ttu-id="54567-185">**Описание** — можно ввести описание, которое поможет различать названия торговой марки.</span><span class="sxs-lookup"><span data-stu-id="54567-185">**Description** – You can enter a description to help distinguish brand names.</span></span>

1. <span data-ttu-id="54567-186">На экспресс-вкладке **Модели мобильных устройств** отображаются все модели для выбранной торговой марки устройства.</span><span class="sxs-lookup"><span data-stu-id="54567-186">The **Mobile device models** FastTab shows all the models for the selected device brand.</span></span> <span data-ttu-id="54567-187">Используйте кнопки на панели инструментов, чтобы добавить строки в сетку или удалить строки.</span><span class="sxs-lookup"><span data-stu-id="54567-187">Use the buttons on the toolbar to add rows to the grid or remove rows.</span></span> <span data-ttu-id="54567-188">Для каждой строки установите следующие поля:</span><span class="sxs-lookup"><span data-stu-id="54567-188">For each row, you can set the following fields:</span></span>

    - <span data-ttu-id="54567-189">**Код модели устройства** — код модели устройства, такой как *Surface Book 2*.</span><span class="sxs-lookup"><span data-stu-id="54567-189">**Device model ID** – The device model ID, such as *Surface Book 2*.</span></span>
    - <span data-ttu-id="54567-190">**Описание** — можно ввести описание, которое поможет различать коды моделей.</span><span class="sxs-lookup"><span data-stu-id="54567-190">**Description** – You can enter a description to help distinguish model IDs.</span></span>