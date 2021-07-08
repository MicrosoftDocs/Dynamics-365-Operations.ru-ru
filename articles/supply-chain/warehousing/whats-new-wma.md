---
title: Что нового или что изменено в мобильном приложении Warehouse Management
description: В этой теме перечислены новые и измененные функции для каждой выпущенной версии мобильного приложения Warehouse Management для Microsoft Dynamics 365 Supply Chain Management.
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261796"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="414f5-103">Что нового или что изменено в мобильном приложении Warehouse Management</span><span class="sxs-lookup"><span data-stu-id="414f5-103">What's new or changed in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="414f5-104">В этой теме перечислены новые функции, исправления, улучшения и известные проблемы для каждой выпущенной версии мобильного приложения Warehouse Management для Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="414f5-104">This topic lists new features, fixes, improvements, and known issues for each released version of the Warehouse Management mobile app for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="version-2060"></a><span data-ttu-id="414f5-105">Версия 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="414f5-105">Version 2.0.6.0</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2060"></a><span data-ttu-id="414f5-106">Новые функции, исправления и улучшения в 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="414f5-106">New features, fixes, and improvements in version 2.0.6.0</span></span>

<span data-ttu-id="414f5-107">Эта версия вводит следующие новые функции, исправления и улучшения:</span><span class="sxs-lookup"><span data-stu-id="414f5-107">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="414f5-108">Демонстрационный режим теперь показывает все метки на языке устройства.</span><span class="sxs-lookup"><span data-stu-id="414f5-108">Demo mode now shows all labels in the device language.</span></span>
- <span data-ttu-id="414f5-109">Вы реже получаете следующее сообщение об ошибке: "Не удается найти подходящее представление для указанного размера".</span><span class="sxs-lookup"><span data-stu-id="414f5-109">You're less likely to receive the following error message: "Cannot find a suitable view for the specified size."</span></span>
- <span data-ttu-id="414f5-110">Минимальная высота карточек работы была увеличена (для случаев, когда в списке работы настроены три или меньше полей).</span><span class="sxs-lookup"><span data-stu-id="414f5-110">The minimum height for work cards has been increased (for cases where three or fewer fields are configured to appear in the work list).</span></span>
- <span data-ttu-id="414f5-111">Границы (обесцвечивание) в нижней части карточек сведений были улучшены.</span><span class="sxs-lookup"><span data-stu-id="414f5-111">Margins (fade out) at the bottom of details cards have been improved.</span></span>
- <span data-ttu-id="414f5-112">Недопустимые символы в файлах XML, которыми система обменивается с сервером, теперь обрабатываются правильно.</span><span class="sxs-lookup"><span data-stu-id="414f5-112">Invalid symbols in XML files that are exchanged with the server are now handled gracefully.</span></span> <span data-ttu-id="414f5-113">(Например, непечатаемые символы теперь обрабатываются правильно и больше не приводят к тому, что приложение перестало отвечать.)</span><span class="sxs-lookup"><span data-stu-id="414f5-113">(For example, non-printable characters are now handled gracefully and no longer cause the app to stop responding.)</span></span>
- <span data-ttu-id="414f5-114">Ошибки HTTP (например, "ошибка 503") при отправлении запроса на сервер теперь обрабатываются правильно.</span><span class="sxs-lookup"><span data-stu-id="414f5-114">HTTP errors (such as "error 503") when a server request is submitted are now handled gracefully.</span></span>
- <span data-ttu-id="414f5-115">Показывается ошибка, список параметров больше не отображается автоматически для элементов управления полей со списком.</span><span class="sxs-lookup"><span data-stu-id="414f5-115">While an error is being shown, the options list is no longer automatically shown for combo box controls.</span></span>
- <span data-ttu-id="414f5-116">Приложение больше не перестает отвечать из-за ориентации дисплея, которая выбрана в настройках пользователя.</span><span class="sxs-lookup"><span data-stu-id="414f5-116">The app no longer stops responding because of the display orientation that is selected in user settings.</span></span>
- <span data-ttu-id="414f5-117">Изображения продуктов теперь отображаются в средах самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="414f5-117">Product images are now shown in self-service environments.</span></span> <span data-ttu-id="414f5-118">(Это изменение распространяется только на версии с низким разрешением.</span><span class="sxs-lookup"><span data-stu-id="414f5-118">(This change applies to low-resolution versions only.</span></span> <span data-ttu-id="414f5-119">Служба управления файлами не поддерживает полноразмерные изображения в средах самообслуживания.)</span><span class="sxs-lookup"><span data-stu-id="414f5-119">The file management service doesn't support full-sized images in self-service environments.)</span></span>
- <span data-ttu-id="414f5-120">Исправлена проблема, связанная с короткими комплектациями с нулевым количеством.</span><span class="sxs-lookup"><span data-stu-id="414f5-120">An issue that involved zero-quantity short picks has been fixed.</span></span>
- <span data-ttu-id="414f5-121">Приложение больше не перестает отвечать, когда карточка сведений показывает несколько одинаковых полей.</span><span class="sxs-lookup"><span data-stu-id="414f5-121">The app no longer stops responding when a details card shows multiple identical fields.</span></span>

### <a name="known-issues-in-version-2060"></a><span data-ttu-id="414f5-122">Известные проблемы в версии 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="414f5-122">Known issues in version 2.0.6.0</span></span>

<span data-ttu-id="414f5-123">В этой версии существуют следующие известные проблемы:</span><span class="sxs-lookup"><span data-stu-id="414f5-123">The following known issues exist in this version:</span></span>

- <span data-ttu-id="414f5-124">Приложение (особенно список работ) становится медленнее с течением времени.</span><span class="sxs-lookup"><span data-stu-id="414f5-124">The app (especially the work list) becomes slower over time.</span></span>
- <span data-ttu-id="414f5-125">**Версия для Windows:** когда USB используется для сканирования в Windows, несоответствующие результаты вызывают смешивание отсканированных символов.</span><span class="sxs-lookup"><span data-stu-id="414f5-125">**Windows version:** When a USB gun is used for scanning on Windows, inconsistent results cause scanned symbols to be mixed up.</span></span>

## <a name="version-2050"></a><span data-ttu-id="414f5-126">Версия 2.0.5.0</span><span class="sxs-lookup"><span data-stu-id="414f5-126">Version 2.0.5.0</span></span>

<span data-ttu-id="414f5-127">Эта версия вводит следующие новые функции, исправления и улучшения:</span><span class="sxs-lookup"><span data-stu-id="414f5-127">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="414f5-128">Секрет клиента больше не скрыт в настройке параметров соединения.</span><span class="sxs-lookup"><span data-stu-id="414f5-128">The client secret is no longer hidden in the connection settings setup.</span></span>
- <span data-ttu-id="414f5-129">Теперь вы можете долго нажимать на любой текст, чтобы увидеть его полностью.</span><span class="sxs-lookup"><span data-stu-id="414f5-129">You can now long-press on any text to see it fully.</span></span>
- <span data-ttu-id="414f5-130">Сообщение об ошибке при отсутствии разрешений на хранение улучшено.</span><span class="sxs-lookup"><span data-stu-id="414f5-130">The error message when storage permissions are missing has been improved.</span></span>
- <span data-ttu-id="414f5-131">Для некоторых потоков были добавлены новые последовательности управления.</span><span class="sxs-lookup"><span data-stu-id="414f5-131">New control sequences have been added for some flows.</span></span>
- <span data-ttu-id="414f5-132">Кнопка отправки больше не становится доступной (что неправильно) из-за размера окна.</span><span class="sxs-lookup"><span data-stu-id="414f5-132">The submit button no longer incorrectly becomes available because of the window size.</span></span>
- <span data-ttu-id="414f5-133">Ползунки теперь могут работать на меньших экранах при использовании больших размеров кнопок.</span><span class="sxs-lookup"><span data-stu-id="414f5-133">Sliders can now proceed on smaller screens when larger button sizes are used.</span></span>
- <span data-ttu-id="414f5-134">Наложение из четырех кнопок больше не обрезано.</span><span class="sxs-lookup"><span data-stu-id="414f5-134">The four-button overlay is no longer cut off.</span></span>
- <span data-ttu-id="414f5-135">Клавиатура теперь поддерживает кнопку удаления.</span><span class="sxs-lookup"><span data-stu-id="414f5-135">The keyboard now supports the delete button.</span></span>
- <span data-ttu-id="414f5-136">Исправлена проблема яркости, которая может возникнуть при нажатии клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="414f5-136">A brightness issue that could occur when the keyboard is pressed has been fixed.</span></span>
- <span data-ttu-id="414f5-137">Исправлены различные проблемы с демонстрационными данными.</span><span class="sxs-lookup"><span data-stu-id="414f5-137">Various demo data issues have been fixed.</span></span>
- <span data-ttu-id="414f5-138">Исправлена проблема, которая затронула числовые поля на странице сведений.</span><span class="sxs-lookup"><span data-stu-id="414f5-138">An issue that affected numeric fields on the details page has been fixed.</span></span>
- <span data-ttu-id="414f5-139">Экранная клавиатура больше не исчезает на некоторых устройствах.</span><span class="sxs-lookup"><span data-stu-id="414f5-139">The screen keyboard no longer occasionally disappears on some devices.</span></span>
- <span data-ttu-id="414f5-140">Исправлены различные ошибки пользовательского интерфейса (UI), такие как ошибки, влияющие на цвет фона и позиционирование.</span><span class="sxs-lookup"><span data-stu-id="414f5-140">Various user interface (UI) bugs have been fixed, such as bugs that affected the background color and positioning.</span></span>
- <span data-ttu-id="414f5-141">Улучшен русский пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="414f5-141">The Russian-language UI has been improved.</span></span>
- <span data-ttu-id="414f5-142">Исправлены различные проблемы, из-за которых система перестала отвечать.</span><span class="sxs-lookup"><span data-stu-id="414f5-142">Various issues that caused the system to stop responding have been fixed.</span></span>
- <span data-ttu-id="414f5-143">Проблема, связанная с повторным открытием калькулятора, устранена.</span><span class="sxs-lookup"><span data-stu-id="414f5-143">An issue that was related to reopening the calculator has been fixed.</span></span>
- <span data-ttu-id="414f5-144">**Версия для Android:** исправлена проблема, из-за которой Android 4.4 переставал отвечать при запуске.</span><span class="sxs-lookup"><span data-stu-id="414f5-144">**Android version:** An issue that caused Android 4.4 to stop responding on startup has been fixed.</span></span>
- <span data-ttu-id="414f5-145">**Версия для Android:** минимальный масштаб был сокращен до 50 процентов.</span><span class="sxs-lookup"><span data-stu-id="414f5-145">**Android version:** Minimum scaling has been reduced to 50 percent.</span></span>

## <a name="version-2040"></a><span data-ttu-id="414f5-146">Версия 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="414f5-146">Version 2.0.4.0</span></span>

<span data-ttu-id="414f5-147">Версия 2.0.4.0 стала первой общедоступной версией мобильного приложения Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="414f5-147">Version 2.0.4.0 was the first generally available release of the Warehouse Management mobile app.</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2040"></a><span data-ttu-id="414f5-148">Новые функции, исправления и улучшения в 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="414f5-148">New features, fixes, and improvements in version 2.0.4.0</span></span>

<span data-ttu-id="414f5-149">Эта версия содержит следующие новые функции, исправления и улучшения, которые не были доступны в предварительной версии:</span><span class="sxs-lookup"><span data-stu-id="414f5-149">This version introduces the following new features, fixes, and improvements that weren't available in the preview version:</span></span>

- <span data-ttu-id="414f5-150">Если карточка сведений включает в себя две метки, которые имеют одинаковые данные, одна из меток скрыта.</span><span class="sxs-lookup"><span data-stu-id="414f5-150">If a details card includes two labels that have identical data, one of the labels is hidden.</span></span>
- <span data-ttu-id="414f5-151">Специальные символы теперь отображаются по умолчанию, и возможность скрыть их была удалена из настроек пользователя.</span><span class="sxs-lookup"><span data-stu-id="414f5-151">Special characters are now shown by default, and the option to hide them has been removed from user settings.</span></span>
- <span data-ttu-id="414f5-152">Отключенные кнопки отправки теперь показаны как недоступные в компактном представлении для портативных устройств.</span><span class="sxs-lookup"><span data-stu-id="414f5-152">Disabled submit buttons are now shown as unavailable in compact arm-held view.</span></span>
- <span data-ttu-id="414f5-153">Изменение логики последовательности элементов управления обеспечивает более плавное масштабирование на устройствах.</span><span class="sxs-lookup"><span data-stu-id="414f5-153">A change to the sequencing logic for controls ensures smoother scaling across devices.</span></span> <span data-ttu-id="414f5-154">Поэтому меньше необходимости в настройке масштабирования шрифтов или кнопок.</span><span class="sxs-lookup"><span data-stu-id="414f5-154">Therefore, there is less need to adjust the scaling of fonts or buttons.</span></span>
- <span data-ttu-id="414f5-155">Тема цвета по умолчанию была изменена на *Темная*.</span><span class="sxs-lookup"><span data-stu-id="414f5-155">The default color theme has been changed to *Dark*.</span></span>
- <span data-ttu-id="414f5-156">Отсутствующий значок для отключенной кнопки отправки добавлен в представлении ленты.</span><span class="sxs-lookup"><span data-stu-id="414f5-156">The missing icon for the disabled submit button has been added in ribbon view.</span></span>
- <span data-ttu-id="414f5-157">Исключения тайм-аута теперь переводят на страницу соединения вместо того, чтобы показывать ошибку в строке.</span><span class="sxs-lookup"><span data-stu-id="414f5-157">Time-out exceptions now take you to the connection page instead of showing an in-line error.</span></span>
- <span data-ttu-id="414f5-158">Если нет действия отправки (например, **OK**, **Да**, **Принять**, **Готово** или **Завершено**), кнопка представления будет отключена.</span><span class="sxs-lookup"><span data-stu-id="414f5-158">If no submit action is available (such as **OK**, **Yes**, **Accept**, **Done**, or **Finished**), the submit button will be disabled.</span></span>
- <span data-ttu-id="414f5-159">Стабильность приложений была улучшена.</span><span class="sxs-lookup"><span data-stu-id="414f5-159">App stability has been improved.</span></span>
- <span data-ttu-id="414f5-160">Существует исправление уязвимости безопасности [CVE--2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span><span class="sxs-lookup"><span data-stu-id="414f5-160">There is a fix for security vulnerability [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span></span>
- <span data-ttu-id="414f5-161">**Версия для Windows:** исправлена проблема в Windows, когда меню не отвечало после того, как размер окна был изменен.</span><span class="sxs-lookup"><span data-stu-id="414f5-161">**Windows version:** An issue on Windows, where menus were unresponsive after the window was resized, has been fixed.</span></span>

### <a name="known-issue-in-version-2040"></a><span data-ttu-id="414f5-162">Известные проблемы в версии 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="414f5-162">Known issue in version 2.0.4.0</span></span>

<span data-ttu-id="414f5-163">В этой версии существуют следующие известные проблемы:</span><span class="sxs-lookup"><span data-stu-id="414f5-163">The following known issue exists in this version:</span></span>

- <span data-ttu-id="414f5-164">Эта версия имеет проблемы с устройствами, которые используют Android 4.4.</span><span class="sxs-lookup"><span data-stu-id="414f5-164">This version has an issue with devices that use Android 4.4.</span></span> <span data-ttu-id="414f5-165">Могут возникнуть проблемы при использовании приложения в этой версии Android.</span><span class="sxs-lookup"><span data-stu-id="414f5-165">You might experience issues when you use the app on this Android version.</span></span>
