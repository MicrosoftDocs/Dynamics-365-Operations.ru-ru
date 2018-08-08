---
title: "Настройка имен полей приложения в приложении склада"
description: "В этом разделе описывается, как определить и настроить имена полей и приоритеты приложения склада в Finance and Operations."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 0162014189ed6bffb17e6718a67eecfd55c334a5
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---

# <a name="configure-app-field-names-in-warehousing-app"></a><span data-ttu-id="6b445-103">Настройка имен полей приложения в приложении склада</span><span class="sxs-lookup"><span data-stu-id="6b445-103">Configure app field names in Warehousing app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b445-104">В этом разделе описывается, как определить и настроить имена полей и приоритеты приложения склада в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6b445-104">This topic describes how to define and configure warehouse app field names and priorities in Finance and Operations.</span></span> 

<span data-ttu-id="6b445-105">**Примечание.** Этот раздел относится к функциям в модуле "Управление складом".</span><span class="sxs-lookup"><span data-stu-id="6b445-105">**Note:** This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="6b445-106">Он не применяется к функциям в модуле "Управление запасами".</span><span class="sxs-lookup"><span data-stu-id="6b445-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="6b445-107">Finance and Operations — Warehousing — это приложение, которое можно использовать для выполнения задач на складе.</span><span class="sxs-lookup"><span data-stu-id="6b445-107">Finance and Operations - Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="6b445-108">Можно определить и настроить имена полей, которые используются в приложении, а также настроить приоритет, который должен быть назначен именам полей.</span><span class="sxs-lookup"><span data-stu-id="6b445-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="6b445-109">В этом разделе описывается, как определить и настроить эти имена полей и приоритеты приложения склада, а также как они используются в приложении Finance and Operations — Warehousing.</span><span class="sxs-lookup"><span data-stu-id="6b445-109">This topic explains how to define and configure these warehouse app field names and priorities, and how they are used in Finance and Operations - Warehousing.</span></span> <span data-ttu-id="6b445-110">Подробные сведения о порядке настройки подключения к Finance and Operations — Warehousing см. в руководстве [Установка и настройка Finance and Operations — Warehousing](install-configure-warehousing-app.md).</span><span class="sxs-lookup"><span data-stu-id="6b445-110">For detailed information about how to configure the connection to Finance and Operations  - Warehousing, refer to the tutorial [Install and configure Finance and Operations - Warehousing](install-configure-warehousing-app.md).</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="6b445-111">Настройка имен полей в приложении склада</span><span class="sxs-lookup"><span data-stu-id="6b445-111">Configure warehouse app field names</span></span>

<span data-ttu-id="6b445-112">При использовании Finance and Operations — Warehousing на мобильном устройстве можно настроить способ отображения метаданных на устройстве на странице **Имена полей в приложении склада**.</span><span class="sxs-lookup"><span data-stu-id="6b445-112">When you use Finance and Operations - Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="6b445-113">В новой компании в Finance and Operations выберите **Создать настройку по умолчанию** для создания всех имен полей, которые будут использоваться в workflow-процессах работы со складом на мобильном устройстве, затем назначьте им предпочтительный режим ввода и тип входных данных.</span><span class="sxs-lookup"><span data-stu-id="6b445-113">In a new company in Finance and Operations, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="6b445-114">После создания всех имен полей можно выбрать следующие параметры ввода.</span><span class="sxs-lookup"><span data-stu-id="6b445-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b445-115">Параметр</span><span class="sxs-lookup"><span data-stu-id="6b445-115">Option</span></span></th>
<th><span data-ttu-id="6b445-116">описание</span><span class="sxs-lookup"><span data-stu-id="6b445-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b445-117">Предпочтительный режим ввода</span><span class="sxs-lookup"><span data-stu-id="6b445-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="6b445-118">Этот параметр определяет, будет ли для выбранного имени поля отображаться поле сканирования или поле ручного ввода.</span><span class="sxs-lookup"><span data-stu-id="6b445-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="6b445-119">Это полезно для различения полей в зависимости от того, используются ли штрих-коды для данного поля.</span><span class="sxs-lookup"><span data-stu-id="6b445-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="6b445-120"><strong>Примечание.</strong> Для имен полей с предпочтительным режимом ввода <strong>Сканирование</strong> можно ввести сведения вручную, если штрих-код не удается прочесть или он поврежден.</span><span class="sxs-lookup"><span data-stu-id="6b445-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b445-121">Тип Ввода</span><span class="sxs-lookup"><span data-stu-id="6b445-121">Input type</span></span></td>
<td><span data-ttu-id="6b445-122">Этот параметр определяет, какой тип ввода должен использоваться для выбранного имени поля.</span><span class="sxs-lookup"><span data-stu-id="6b445-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="6b445-123">Доступные четыре варианта:</span><span class="sxs-lookup"><span data-stu-id="6b445-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="6b445-124"><strong>Выбор</strong> - содержит список вариантов для выбора.</span><span class="sxs-lookup"><span data-stu-id="6b445-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="6b445-125">Имена полей с этим параметром не могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="6b445-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="6b445-126"><strong>Дата</strong> - имена полей, указанных как даты, будут отображаться в формате даты с меткой.</span><span class="sxs-lookup"><span data-stu-id="6b445-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="6b445-127">Это помогает складским работникам увидеть, в каком формате следует вводить дату.</span><span class="sxs-lookup"><span data-stu-id="6b445-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="6b445-128">Имена полей с этим параметром не могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="6b445-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="6b445-129"><strong>Буквенное значение</strong> - если выбран этот вариант, при ручном вводе информации в приложении будет использоваться клавиатура устройства.</span><span class="sxs-lookup"><span data-stu-id="6b445-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="6b445-130">Функция клавиатуры может изменяться в зависимости от того, какое используется устройство.</span><span class="sxs-lookup"><span data-stu-id="6b445-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="6b445-131"><strong>Числовое значение</strong> - для имен полей, в которых используется только цифровой ввода, можно выбрать этот вариант для отображения специальной цифровой клавиатуры вместо клавиатуры устройства.</span><span class="sxs-lookup"><span data-stu-id="6b445-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="6b445-132">Настройка приоритета полей в приложении склада</span><span class="sxs-lookup"><span data-stu-id="6b445-132">Configure warehouse app field priority</span></span>

<span data-ttu-id="6b445-133">На странице **Приоритет полей в приложении склада** можно поместить имена полей в разные группы приоритета.</span><span class="sxs-lookup"><span data-stu-id="6b445-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="6b445-134">Это дает возможность определить, какие сведения должны отображаться на странице основной задачи, когда складские работники выполняют задачи с помощью приложения.</span><span class="sxs-lookup"><span data-stu-id="6b445-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="6b445-135">При нажатии кнопки **Создать настройку по умолчанию** создается набор групп приоритета по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6b445-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="6b445-136">Можно создавать столько групп приоритет, сколько требуется, но только три группы приоритета отображаются на странице задач.</span><span class="sxs-lookup"><span data-stu-id="6b445-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="6b445-137">Когда Finance and Operations отправляет метаданные в приложение, каждому полю назначается относительный приоритет в зависимости от его группы приоритета; приложение будет отображать первые три группы приоритета, содержащиеся в метаданных, на странице задач.</span><span class="sxs-lookup"><span data-stu-id="6b445-137">When Finance and Operations sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="6b445-138">Остальная часть избыточных метаданных отображается на странице дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="6b445-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="6b445-139">В следующей таблице показан пример пять групп приоритетов.</span><span class="sxs-lookup"><span data-stu-id="6b445-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b445-140">Группа приоритета</span><span class="sxs-lookup"><span data-stu-id="6b445-140">Priority group</span></span></th>
<th><span data-ttu-id="6b445-141">Назначенные поля</span><span class="sxs-lookup"><span data-stu-id="6b445-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="6b445-142">Приоритет 10</span><span class="sxs-lookup"><span data-stu-id="6b445-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="6b445-143">Раздел</span><span class="sxs-lookup"><span data-stu-id="6b445-143">Item</span></span></li>
<li><span data-ttu-id="6b445-144">Количество</span><span class="sxs-lookup"><span data-stu-id="6b445-144">Quantity</span></span></li>
<li><span data-ttu-id="6b445-145">Единица измерения</span><span class="sxs-lookup"><span data-stu-id="6b445-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="6b445-146">Приоритет 20</span><span class="sxs-lookup"><span data-stu-id="6b445-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="6b445-147">Положение кластера</span><span class="sxs-lookup"><span data-stu-id="6b445-147">Cluster position</span></span></li>
<li><span data-ttu-id="6b445-148">Кластер</span><span class="sxs-lookup"><span data-stu-id="6b445-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="6b445-149">Приоритет 30</span><span class="sxs-lookup"><span data-stu-id="6b445-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="6b445-150">Описание номенклатуры</span><span class="sxs-lookup"><span data-stu-id="6b445-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="6b445-151">Приоритет 40</span><span class="sxs-lookup"><span data-stu-id="6b445-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="6b445-152">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="6b445-152">Configuration</span></span></li>
<li><span data-ttu-id="6b445-153">Цвет</span><span class="sxs-lookup"><span data-stu-id="6b445-153">Color</span></span></li>
<li><span data-ttu-id="6b445-154">Размер</span><span class="sxs-lookup"><span data-stu-id="6b445-154">Size</span></span></li>
<li><span data-ttu-id="6b445-155">Стиль</span><span class="sxs-lookup"><span data-stu-id="6b445-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="6b445-156">Приоритет 50</span><span class="sxs-lookup"><span data-stu-id="6b445-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="6b445-157">Местоположение</span><span class="sxs-lookup"><span data-stu-id="6b445-157">Location</span></span></li>
<li><span data-ttu-id="6b445-158">Грузоместо</span><span class="sxs-lookup"><span data-stu-id="6b445-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6b445-159">Например, когда работник склада выполняет задачу на мобильном устройстве, если метаданные, которые будут отображаться в приложении, состоят из следующих полей:</span><span class="sxs-lookup"><span data-stu-id="6b445-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="6b445-160">Раздел</span><span class="sxs-lookup"><span data-stu-id="6b445-160">Item</span></span>
-   <span data-ttu-id="6b445-161">Количество</span><span class="sxs-lookup"><span data-stu-id="6b445-161">Quantity</span></span>
-   <span data-ttu-id="6b445-162">Единица измерения</span><span class="sxs-lookup"><span data-stu-id="6b445-162">Unit of measure</span></span>
-   <span data-ttu-id="6b445-163">Описание номенклатуры</span><span class="sxs-lookup"><span data-stu-id="6b445-163">Item description</span></span>
-   <span data-ttu-id="6b445-164">Размер и местонахождение</span><span class="sxs-lookup"><span data-stu-id="6b445-164">Size and Location</span></span>

<span data-ttu-id="6b445-165">На основании приоритета полей приложения склада, настроенного в приведенной выше таблице, на странице задачи будут отображаться следующие 3 строки данных:</span><span class="sxs-lookup"><span data-stu-id="6b445-165">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="6b445-166">Строка 1: номенклатура, количество, единица измерения</span><span class="sxs-lookup"><span data-stu-id="6b445-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="6b445-167">Строка 2: описание номенклатуры</span><span class="sxs-lookup"><span data-stu-id="6b445-167">Row 2: Item description</span></span>
-   <span data-ttu-id="6b445-168">Строка 3: размер</span><span class="sxs-lookup"><span data-stu-id="6b445-168">Row 3: Size</span></span>

<span data-ttu-id="6b445-169">Оставшиеся метаданные, например, местоположение, не будут отображаться на странице задачи, но будет отображаться на странице сведений.</span><span class="sxs-lookup"><span data-stu-id="6b445-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="6b445-170">Чтобы получить дополнительные сведения и посмотреть примеры интерфейса пользователя, см. запись блога [Представляем Finance and Operations — Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="6b445-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="6b445-171">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6b445-171">Additional resources</span></span>
--------

[<span data-ttu-id="6b445-172">Установка и настройка Microsoft Dynamics 365 for Finance and Operations — Warehousing</span><span class="sxs-lookup"><span data-stu-id="6b445-172">Install and configure Microsoft Dynamics 365 for Finance and Operations – Warehousing</span></span>](install-configure-warehousing-app.md)




