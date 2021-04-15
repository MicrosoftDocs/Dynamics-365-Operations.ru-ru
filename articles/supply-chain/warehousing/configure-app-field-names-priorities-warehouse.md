---
title: Настройка полей для мобильного приложения "Управление складом"
description: В этой теме описывается, как определить и настроить имена полей и приоритеты для полей, отображаемых в мобильном приложении "Управление складом".
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c6ed726536085b836f4014c59ea8df4755577ab5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808830"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="1436a-103">Настройка полей для мобильного приложения "Управление складом"</span><span class="sxs-lookup"><span data-stu-id="1436a-103">Configure fields for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1436a-104">В этой теме описывается, как определить и настроить имена полей и приоритеты для полей, отображаемых в мобильном приложении "Управление складом".</span><span class="sxs-lookup"><span data-stu-id="1436a-104">This topic describes how to define and configure names and priorities of fields shown in the Warehouse Management mobile app.</span></span>

> [!NOTE]
> <span data-ttu-id="1436a-105">Этот раздел относится к функциям в модуле "Управление складом".</span><span class="sxs-lookup"><span data-stu-id="1436a-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="1436a-106">Он не применяется к функциям в модуле "Управление запасами".</span><span class="sxs-lookup"><span data-stu-id="1436a-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="1436a-107">Мобильное приложение "Управление складом" — это приложение, которое можно использовать для выполнения задач на складе.</span><span class="sxs-lookup"><span data-stu-id="1436a-107">The Warehouse Management mobile app is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="1436a-108">Можно определить и настроить имена полей, которые используются в приложении, а также настроить приоритет, который должен быть назначен именам полей.</span><span class="sxs-lookup"><span data-stu-id="1436a-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="1436a-109">В этой теме описывается, как определить и настроить эти имена полей и приоритеты мобильного приложения "Управление складом", а также как они используются.</span><span class="sxs-lookup"><span data-stu-id="1436a-109">This topic explains how to define and configure these Warehouse Management mobile app field names and priorities, and how they are used.</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="1436a-110">Настройка имен полей в приложении склада</span><span class="sxs-lookup"><span data-stu-id="1436a-110">Configure warehouse app field names</span></span>

<span data-ttu-id="1436a-111">При использовании приложения Warehousing на мобильном устройстве можно настроить способ отображения метаданных на устройстве на странице **Имена полей в приложении склада**.</span><span class="sxs-lookup"><span data-stu-id="1436a-111">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="1436a-112">В новой компании выберите **Создать настройку по умолчанию** для создания всех имен полей, которые будут использоваться в рабочих процессах работы со складом на мобильном устройстве, затем назначьте им предпочтительный режим ввода и тип входных данных.</span><span class="sxs-lookup"><span data-stu-id="1436a-112">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="1436a-113">После создания всех имен полей можно выбрать следующие параметры ввода.</span><span class="sxs-lookup"><span data-stu-id="1436a-113">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1436a-114">Параметр</span><span class="sxs-lookup"><span data-stu-id="1436a-114">Option</span></span></th>
<th><span data-ttu-id="1436a-115">описание</span><span class="sxs-lookup"><span data-stu-id="1436a-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1436a-116">Предпочтительный режим ввода</span><span class="sxs-lookup"><span data-stu-id="1436a-116">Preferred input mode</span></span></td>
<td><span data-ttu-id="1436a-117">Этот параметр определяет, будет ли для выбранного имени поля отображаться поле сканирования или поле ручного ввода.</span><span class="sxs-lookup"><span data-stu-id="1436a-117">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="1436a-118">Это полезно для различения полей в зависимости от того, используются ли штрих-коды для данного поля.</span><span class="sxs-lookup"><span data-stu-id="1436a-118">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="1436a-119"><strong>Примечание.</strong> Для имен полей с предпочтительным режимом ввода <strong>Сканирование</strong> можно ввести сведения вручную, если штрих-код не удается прочесть или он поврежден.</span><span class="sxs-lookup"><span data-stu-id="1436a-119"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1436a-120">Тип Ввода</span><span class="sxs-lookup"><span data-stu-id="1436a-120">Input type</span></span></td>
<td><span data-ttu-id="1436a-121">Этот параметр определяет, какой тип ввода должен использоваться для выбранного имени поля.</span><span class="sxs-lookup"><span data-stu-id="1436a-121">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="1436a-122">Доступные четыре варианта:</span><span class="sxs-lookup"><span data-stu-id="1436a-122">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="1436a-123"><strong>Выбор</strong> - содержит список вариантов для выбора.</span><span class="sxs-lookup"><span data-stu-id="1436a-123"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="1436a-124">Имена полей с этим параметром не могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="1436a-124">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="1436a-125"><strong>Дата</strong> - имена полей, указанных как даты, будут отображаться в формате даты с меткой.</span><span class="sxs-lookup"><span data-stu-id="1436a-125"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="1436a-126">Это помогает складским работникам увидеть, в каком формате следует вводить дату.</span><span class="sxs-lookup"><span data-stu-id="1436a-126">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="1436a-127">Имена полей с этим параметром не могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="1436a-127">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="1436a-128"><strong>Буквенное значение</strong> - если выбран этот вариант, при ручном вводе информации в приложении будет использоваться клавиатура устройства.</span><span class="sxs-lookup"><span data-stu-id="1436a-128"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="1436a-129">Функция клавиатуры может изменяться в зависимости от того, какое используется устройство.</span><span class="sxs-lookup"><span data-stu-id="1436a-129">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="1436a-130"><strong>Числовое значение</strong> - для имен полей, в которых используется только цифровой ввода, можно выбрать этот вариант для отображения специальной цифровой клавиатуры вместо клавиатуры устройства.</span><span class="sxs-lookup"><span data-stu-id="1436a-130"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="1436a-131">Настройка приоритета полей в приложении склада</span><span class="sxs-lookup"><span data-stu-id="1436a-131">Configure warehouse app field priority</span></span>

<span data-ttu-id="1436a-132">На странице **Приоритет полей в приложении склада** можно поместить имена полей в разные группы приоритета.</span><span class="sxs-lookup"><span data-stu-id="1436a-132">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="1436a-133">Это дает возможность определить, какие сведения должны отображаться на странице основной задачи, когда складские работники выполняют задачи с помощью приложения.</span><span class="sxs-lookup"><span data-stu-id="1436a-133">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="1436a-134">При нажатии кнопки **Создать настройку по умолчанию** создается набор групп приоритета по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1436a-134">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="1436a-135">Можно создавать столько групп приоритет, сколько требуется, но только три группы приоритета отображаются на странице задач.</span><span class="sxs-lookup"><span data-stu-id="1436a-135">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="1436a-136">Когда система отправляет метаданные в приложение, каждому полю назначается относительный приоритет в зависимости от его группы приоритета; приложение будет отображать первые три группы приоритета, содержащиеся в метаданных, на странице задач.</span><span class="sxs-lookup"><span data-stu-id="1436a-136">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="1436a-137">Остальная часть избыточных метаданных отображается на странице дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="1436a-137">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="1436a-138">В следующей таблице показан пример пять групп приоритетов.</span><span class="sxs-lookup"><span data-stu-id="1436a-138">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1436a-139">Группа приоритета</span><span class="sxs-lookup"><span data-stu-id="1436a-139">Priority group</span></span></th>
<th><span data-ttu-id="1436a-140">Назначенные поля</span><span class="sxs-lookup"><span data-stu-id="1436a-140">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="1436a-141">Приоритет 10</span><span class="sxs-lookup"><span data-stu-id="1436a-141">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="1436a-142">Раздел</span><span class="sxs-lookup"><span data-stu-id="1436a-142">Item</span></span></li>
<li><span data-ttu-id="1436a-143">Количество</span><span class="sxs-lookup"><span data-stu-id="1436a-143">Quantity</span></span></li>
<li><span data-ttu-id="1436a-144">Единица измерения</span><span class="sxs-lookup"><span data-stu-id="1436a-144">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="1436a-145">Приоритет 20</span><span class="sxs-lookup"><span data-stu-id="1436a-145">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="1436a-146">Положение кластера</span><span class="sxs-lookup"><span data-stu-id="1436a-146">Cluster position</span></span></li>
<li><span data-ttu-id="1436a-147">Кластер</span><span class="sxs-lookup"><span data-stu-id="1436a-147">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="1436a-148">Приоритет 30</span><span class="sxs-lookup"><span data-stu-id="1436a-148">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="1436a-149">Описание номенклатуры</span><span class="sxs-lookup"><span data-stu-id="1436a-149">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="1436a-150">Приоритет 40</span><span class="sxs-lookup"><span data-stu-id="1436a-150">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="1436a-151">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="1436a-151">Configuration</span></span></li>
<li><span data-ttu-id="1436a-152">Цвет</span><span class="sxs-lookup"><span data-stu-id="1436a-152">Color</span></span></li>
<li><span data-ttu-id="1436a-153">Размер</span><span class="sxs-lookup"><span data-stu-id="1436a-153">Size</span></span></li>
<li><span data-ttu-id="1436a-154">Стиль</span><span class="sxs-lookup"><span data-stu-id="1436a-154">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="1436a-155">Приоритет 50</span><span class="sxs-lookup"><span data-stu-id="1436a-155">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="1436a-156">Местоположение</span><span class="sxs-lookup"><span data-stu-id="1436a-156">Location</span></span></li>
<li><span data-ttu-id="1436a-157">Грузоместо</span><span class="sxs-lookup"><span data-stu-id="1436a-157">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1436a-158">Например, когда работник склада выполняет задачу на мобильном устройстве, если метаданные, которые будут отображаться в приложении, состоят из следующих полей:</span><span class="sxs-lookup"><span data-stu-id="1436a-158">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="1436a-159">Раздел</span><span class="sxs-lookup"><span data-stu-id="1436a-159">Item</span></span>
-   <span data-ttu-id="1436a-160">Количество</span><span class="sxs-lookup"><span data-stu-id="1436a-160">Quantity</span></span>
-   <span data-ttu-id="1436a-161">Единица измерения</span><span class="sxs-lookup"><span data-stu-id="1436a-161">Unit of measure</span></span>
-   <span data-ttu-id="1436a-162">Описание номенклатуры</span><span class="sxs-lookup"><span data-stu-id="1436a-162">Item description</span></span>
-   <span data-ttu-id="1436a-163">Размер и местонахождение</span><span class="sxs-lookup"><span data-stu-id="1436a-163">Size and Location</span></span>

<span data-ttu-id="1436a-164">На основании приоритета полей приложения склада, настроенного в приведенной выше таблице, на странице задачи будут отображаться следующие 3 строки данных:</span><span class="sxs-lookup"><span data-stu-id="1436a-164">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="1436a-165">Строка 1: номенклатура, количество, единица измерения</span><span class="sxs-lookup"><span data-stu-id="1436a-165">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="1436a-166">Строка 2: описание номенклатуры</span><span class="sxs-lookup"><span data-stu-id="1436a-166">Row 2: Item description</span></span>
-   <span data-ttu-id="1436a-167">Строка 3: размер</span><span class="sxs-lookup"><span data-stu-id="1436a-167">Row 3: Size</span></span>

<span data-ttu-id="1436a-168">Оставшиеся метаданные, например, местоположение, не будут отображаться на странице задачи, но будет отображаться на странице сведений.</span><span class="sxs-lookup"><span data-stu-id="1436a-168">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="1436a-169">Чтобы получить дополнительные сведения и посмотреть примеры интерфейса пользователя, см. запись блога [Представляем Finance and Operations — Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="1436a-169">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="1436a-170">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1436a-170">Additional resources</span></span>
--------

[<span data-ttu-id="1436a-171">Установка и подключение мобильного приложения "Управление складом"</span><span class="sxs-lookup"><span data-stu-id="1436a-171">Install and connect the Warehouse Management mobile app</span></span>](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]