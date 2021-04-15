---
title: Электронная отчетность — Обновление формата путем принятия новой базовой версии данного формата
description: В этой теме объясняется, как поддерживать конфигурацию формата электронной отчетности (ER).
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05f8562bcab50a303b58174d177c6058f9417294
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744947"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a><span data-ttu-id="74098-103">Электронная отчетность — Обновление формата путем принятия новой базовой версии данного формата</span><span class="sxs-lookup"><span data-stu-id="74098-103">ER Upgrade your format by adopting a new, base version of that format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="74098-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может вести конфигурацию формата "Электронная отчетность (ER)".</span><span class="sxs-lookup"><span data-stu-id="74098-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can maintain an Electronic reporting (ER) format configuration.</span></span> <span data-ttu-id="74098-105">В этой процедуре описывается, как можно создать пользовательскую версию формата на основе формата, полученного от поставщика конфигурации.</span><span class="sxs-lookup"><span data-stu-id="74098-105">This procedure explains how a custom version of a format can be created based on the format received from a configuration provider (CP).</span></span> <span data-ttu-id="74098-106">В ней также описывается, как настроить новую базовую версию данного формата.</span><span class="sxs-lookup"><span data-stu-id="74098-106">It also explains how to adopt a new, base version of that format.</span></span>

<span data-ttu-id="74098-107">Для выполнения этих шагов сначала необходимо выполнить шаги в процедурах "Создание поставщика конфигурации и пометка его как активного" и "Использование созданного формата для создания электронных документов для платежей".</span><span class="sxs-lookup"><span data-stu-id="74098-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" and "Use created format to generate electronic documents for payments" procedures.</span></span> <span data-ttu-id="74098-108">Эти шаги можно выполнить в компании GBSI.</span><span class="sxs-lookup"><span data-stu-id="74098-108">These steps can be performed in the GBSI company.</span></span>

## <a name="select-format-configuration-for-customization"></a><span data-ttu-id="74098-109">Выбор конфигурации формата для настройки</span><span class="sxs-lookup"><span data-stu-id="74098-109">Select format configuration for customization</span></span>
1. <span data-ttu-id="74098-110">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="74098-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="74098-111">В этом примере демонстрационная компания Litware, Inc. (https://www.litware.com) будет выступать в роли поставщика конфигурации, который поддерживает конфигурации форматов для электронных платежей для определенной страны.</span><span class="sxs-lookup"><span data-stu-id="74098-111">In this example, sample company Litware, Inc. (https://www.litware.com) will act as a configuration provider that supports format configurations for electronic payments for a particular country.</span></span>    <span data-ttu-id="74098-112">Демонстрационная компания Proseware, Inc. (http://www.proseware.com) будет выступать в роли потребителя конфигурации формата, предоставленной Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="74098-112">Sample company Proseware, Inc. (http://www.proseware.com) will act as a consumer of the format configuration that Litware, Inc. provided.</span></span> <span data-ttu-id="74098-113">Proseware, Inc. использует форматы в определенных регионах данной страны.</span><span class="sxs-lookup"><span data-stu-id="74098-113">Proseware, Inc. uses formats in certain regions of that country.</span></span>  
2. <span data-ttu-id="74098-114">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="74098-114">Click Reporting configurations.</span></span>
3. <span data-ttu-id="74098-115">Щелкните "Показать фильтры".</span><span class="sxs-lookup"><span data-stu-id="74098-115">Click Show filters.</span></span>
4. <span data-ttu-id="74098-116">Примените следующие фильтры: введите значение фильтра "BACS (Соединенное Королевство, вымышленный)" в поле "Имя", используя оператор фильтра "начинается с".</span><span class="sxs-lookup"><span data-stu-id="74098-116">Apply the following filters: Enter a filter value of "BACS (UK fictitious)" on the "Name" field using the "begins with" filter operator.</span></span>
  
    <span data-ttu-id="74098-117">Выбранная конфигурация формата BACS (Соединенное Королевство, вымышленный) принадлежит поставщику Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="74098-117">The selected format configuration BACS (UK fictitious) is owned by provider Litware, Inc.</span></span>  

5. <span data-ttu-id="74098-118">Щелкните "Показать фильтры".</span><span class="sxs-lookup"><span data-stu-id="74098-118">Click Show filters.</span></span>
6. <span data-ttu-id="74098-119">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="74098-119">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="74098-120">Версия формата со статусом "Завершено" будет использоваться компанией Proseware, Inc. для пользовательской настройки.</span><span class="sxs-lookup"><span data-stu-id="74098-120">The version of the format with the status of Completed will be used by Proseware, Inc. for customization.</span></span>  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a><span data-ttu-id="74098-121">Создание новой конфигурации для пользовательского формата электронного документа</span><span class="sxs-lookup"><span data-stu-id="74098-121">Create a new configuration for your custom format of electronic document</span></span>
<span data-ttu-id="74098-122">Proseware, Inc.получила версию 1.1 конфигурации BACS (Соединенное Королевство, вымышленный), которая содержит исходный формат для создания электронных платежных документов, от Litware, Inc. в соответствии со своей подпиской на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="74098-122">Proseware, Inc. received version 1.1 of BACS (UK fictitious) configuration that contains the initial format to generate electronic payment documents from Litware, Inc. in accordance to their service subscription.</span></span> <span data-ttu-id="74098-123">Proseware, Inc. желает начать использовать ее как стандарт для своей страны, но требуется некоторая настройка для поддержки определенных региональных требований.</span><span class="sxs-lookup"><span data-stu-id="74098-123">Proseware, Inc. wants to start using this as a standard for their country but some customization is required to support specific regional requirements.</span></span> <span data-ttu-id="74098-124">Proseware, Inc. также желает сохранить возможность обновления пользовательского формата после выпуска его новой версии (с изменениями для поддержки новых требований, существующих в конкретной стране) компанией Litware, Inc., и при этом проводить эти обновления с минимальными затратами.</span><span class="sxs-lookup"><span data-stu-id="74098-124">Proseware, Inc. also wants to keep the ability to upgrade a custom format as soon as a new version of it (with changes to support new country-specific requirements) comes from Litware, Inc. and they want to perform this upgrade with the lowest cost.</span></span>  

<span data-ttu-id="74098-125">Для этого Proseware, Inc. необходимо создать конфигурацию, используя конфигурацию BACS (Соединенное Королевство, вымышленный) в качестве основы.</span><span class="sxs-lookup"><span data-stu-id="74098-125">To do this, Proseware, Inc. needs to create a configuration using the Litware, Inc. configuration BACS (UK fictitious) as a base.</span></span>  

1. <span data-ttu-id="74098-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="74098-126">Close the page.</span></span>
2. <span data-ttu-id="74098-127">Выберите Proseware, Inc., чтобы сделать эту компанию активным поставщиком.</span><span class="sxs-lookup"><span data-stu-id="74098-127">Select Proseware, Inc. to make it an active provider.</span></span>
3. <span data-ttu-id="74098-128">Щелкните "Установить как активное".</span><span class="sxs-lookup"><span data-stu-id="74098-128">Click Set active.</span></span>
4. <span data-ttu-id="74098-129">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="74098-129">Click Reporting configurations.</span></span>
5. <span data-ttu-id="74098-130">В дереве разверните узел "Платежи (упрощенная модель)".</span><span class="sxs-lookup"><span data-stu-id="74098-130">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="74098-131">В дереве выберите "Платежи (упрощенная модель)\BACS (Соединенное Королевство, вымышленный)".</span><span class="sxs-lookup"><span data-stu-id="74098-131">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="74098-132">Выберите конфигурацию BACS (Соединенное Королевство, вымышленный) от Litware, Inc. Proseware, Inc. будет использовать в качестве основы для своей версии версию 1.1.</span><span class="sxs-lookup"><span data-stu-id="74098-132">Select the BACS (UK fictitious) configuration from Litware, Inc. Proseware, Inc. will use version 1.1 as a base for the custom version.</span></span>  

7. <span data-ttu-id="74098-133">Щелкните "Создать конфигурацию", чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="74098-133">Click Create configuration to open the drop dialog.</span></span>

    <span data-ttu-id="74098-134">Это позволяет создать новую конфигурацию для пользовательского формата платежей.</span><span class="sxs-lookup"><span data-stu-id="74098-134">This lets you create a new configuration for a custom payment format.</span></span>  

8. <span data-ttu-id="74098-135">В поле "Создать" выберите "Производное от имени: BACS (Соединенное Королевство, вымышленный), Litware, Inc.".</span><span class="sxs-lookup"><span data-stu-id="74098-135">In the New field, enter 'Derive from Name: BACS (UK fictitious), Litware, Inc.'.</span></span>

    <span data-ttu-id="74098-136">Выберите параметр "Получить", чтобы подтвердить использование BACS (Соединенное Королевство, вымышленный) как базу для создания пользовательской версии.</span><span class="sxs-lookup"><span data-stu-id="74098-136">Select the Derive option to confirm the usage of BACS (UK fictitious) as the base for creating the custom version.</span></span>  

9. <span data-ttu-id="74098-137">В поле "Имя" введите "BACS (Соединенное Королевство, вымышленный, пользовательский)".</span><span class="sxs-lookup"><span data-stu-id="74098-137">In the Name field, type 'BACS (UK fictitious custom)'.</span></span>
10. <span data-ttu-id="74098-138">В поле "Описание" введите "Формат платежа поставщикам BACS (Соединенное Королевство, вымышленный, пользовательский)".</span><span class="sxs-lookup"><span data-stu-id="74098-138">In the Description field, type 'BACS vendor payment (UK fictitious custom)'.</span></span>

    <span data-ttu-id="74098-139">Активный поставщик конфигурации (Proseware, Inc.) вводится здесь автоматически.</span><span class="sxs-lookup"><span data-stu-id="74098-139">The active configuration provider (Proseware, Inc.) is automatically entered here.</span></span> <span data-ttu-id="74098-140">Этот поставщик сможет обновлять эту конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="74098-140">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="74098-141">Другие поставщики могут использовать эту конфигурация, но не смогут ее обновлять.</span><span class="sxs-lookup"><span data-stu-id="74098-141">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

11. <span data-ttu-id="74098-142">Нажмите Создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="74098-142">Click Create configuration.</span></span>

## <a name="customize-your-format-for-the-electronic-document"></a><span data-ttu-id="74098-143">Настройка формата электронного документа</span><span class="sxs-lookup"><span data-stu-id="74098-143">Customize your format for the electronic document</span></span>
1. <span data-ttu-id="74098-144">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="74098-144">Click Designer.</span></span>
2. <span data-ttu-id="74098-145">Щелкните "Развернуть/свернуть".</span><span class="sxs-lookup"><span data-stu-id="74098-145">Click Expand/collapse.</span></span>
3. <span data-ttu-id="74098-146">Щелкните "Развернуть/свернуть".</span><span class="sxs-lookup"><span data-stu-id="74098-146">Click Expand/collapse.</span></span>
4. <span data-ttu-id="74098-147">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Поставщик\Банк".</span><span class="sxs-lookup"><span data-stu-id="74098-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="74098-148">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="74098-148">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="74098-149">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="74098-149">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="74098-150">В поле "Имя" введите "IBAN".</span><span class="sxs-lookup"><span data-stu-id="74098-150">In the Name field, type 'IBAN'.</span></span>
8. <span data-ttu-id="74098-151">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="74098-151">Click OK.</span></span>
9. <span data-ttu-id="74098-152">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Поставщик\Банк\IBAN".</span><span class="sxs-lookup"><span data-stu-id="74098-152">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\IBAN'.</span></span>
10. <span data-ttu-id="74098-153">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="74098-153">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="74098-154">В дереве выберите "Текст\строка".</span><span class="sxs-lookup"><span data-stu-id="74098-154">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="74098-155">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="74098-155">Click OK.</span></span>
13. <span data-ttu-id="74098-156">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Поставщик\Имя\Строка".</span><span class="sxs-lookup"><span data-stu-id="74098-156">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="74098-157">В поле "Максимальная длина" введите "60".</span><span class="sxs-lookup"><span data-stu-id="74098-157">In the Maximum length field, enter '60'.</span></span>
15. <span data-ttu-id="74098-158">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="74098-158">Click the Mapping tab.</span></span>
16. <span data-ttu-id="74098-159">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="74098-159">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="74098-160">В дереве разверните узел "model\Payments".</span><span class="sxs-lookup"><span data-stu-id="74098-160">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="74098-161">В дереве разверните узел "модель\Платежи\Кредитор".</span><span class="sxs-lookup"><span data-stu-id="74098-161">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="74098-162">В дереве разверните узел "модель\Платежи\Кредитор\Счет".</span><span class="sxs-lookup"><span data-stu-id="74098-162">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
20. <span data-ttu-id="74098-163">В дереве выберите "модель\Платежи\Кредитор\Счет\IBAN".</span><span class="sxs-lookup"><span data-stu-id="74098-163">In the tree, select 'model\Payments\Creditor\Account\IBAN'.</span></span>
21. <span data-ttu-id="74098-164">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура = модель.Платежи\Поставщик\Банк\IBAN\Строка".</span><span class="sxs-lookup"><span data-stu-id="74098-164">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\IBAN\String'.</span></span>
22. <span data-ttu-id="74098-165">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="74098-165">Click Bind.</span></span>
23. <span data-ttu-id="74098-166">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="74098-166">Click Save.</span></span>

## <a name="validate-the-customized-format"></a><span data-ttu-id="74098-167">Проверка настроенного формата</span><span class="sxs-lookup"><span data-stu-id="74098-167">Validate the customized format</span></span>
1. <span data-ttu-id="74098-168">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="74098-168">Click Validate.</span></span>

    <span data-ttu-id="74098-169">Проверьте настроенный макет формата и изменения сопоставления данных, чтобы убедиться, что все привязки работают правильно.</span><span class="sxs-lookup"><span data-stu-id="74098-169">Validate the customized format layout and data mapping changes to make sure that all bindings are okay.</span></span>  

2. <span data-ttu-id="74098-170">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="74098-170">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a><span data-ttu-id="74098-171">Изменение статуса текущей версии конфигурации пользовательского формата</span><span class="sxs-lookup"><span data-stu-id="74098-171">Change the status of the current version of the custom format configuration</span></span>
<span data-ttu-id="74098-172">Измените статус созданной конфигурации формата с "Черновик" на "Завершено", чтобы сделать ее доступной для создания платежных документов.</span><span class="sxs-lookup"><span data-stu-id="74098-172">Change the status of the designed format configuration from Draft to Completed to make it available for payment document generation.</span></span>  

1. <span data-ttu-id="74098-173">Щелкните "Изменить статус".</span><span class="sxs-lookup"><span data-stu-id="74098-173">Click Change status.</span></span>

    <span data-ttu-id="74098-174">Обратите внимание, что текущая версия выбранной конфигурации имеет статус "Черновик".</span><span class="sxs-lookup"><span data-stu-id="74098-174">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="74098-175">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="74098-175">Click Complete.</span></span>
3. <span data-ttu-id="74098-176">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="74098-176">In the Description field, type a value.</span></span>
4. <span data-ttu-id="74098-177">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="74098-177">Click OK.</span></span>
5. <span data-ttu-id="74098-178">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="74098-178">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="74098-179">Обратите внимание, что созданная конфигурация сохраняется как завершенная версия 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="74098-179">Note that the created configuration is saved as completed version 1.1.1.</span></span> <span data-ttu-id="74098-180">Это означает, что это версия 1 пользовательского формата BACS (Соединенное Королевство, вымышленный, пользовательский), которая основана на версии 1 формата BACS (Соединенное Королевство, вымышленный), которая основана на версии 1 модели данных платежей (упрощенной модели).</span><span class="sxs-lookup"><span data-stu-id="74098-180">This means it is version 1 of the custom BACS (UK fictitious custom) format, which is based on version 1 of the BACS (UK fictitious) format, which is based on version 1 of the Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-to-generate-payment-files"></a><span data-ttu-id="74098-181">Проверка настроенного формата для создания файлов платежей</span><span class="sxs-lookup"><span data-stu-id="74098-181">Test the customized format to generate payment files</span></span>
<span data-ttu-id="74098-182">Выполните шаги, описанные в процедуре "Использование созданного формата для создания электронных документов для платежей", в параллельном сеансе Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="74098-182">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in a parallel Finance and Operations session.</span></span> <span data-ttu-id="74098-183">Выберите формат BACS (Соединенное Королевство, вымышленный, пользовательский) в параметрах метода электронного платежа.</span><span class="sxs-lookup"><span data-stu-id="74098-183">Select the BACS (UK fictitious custom) format in electronic payment method parameters.</span></span> <span data-ttu-id="74098-184">Убедитесь, что созданный файл платежа содержит недавно введенный узел XML, представляющий код IBAN в соответствии с региональными требованиями.</span><span class="sxs-lookup"><span data-stu-id="74098-184">Make sure that the created payment file contains the recently introduced XML node presenting IBAN code in accordance to regional requirements.</span></span>  

## <a name="update-the-existing-country-specific-configuration"></a><span data-ttu-id="74098-185">Обновление существующей конфигурации для определенной страны</span><span class="sxs-lookup"><span data-stu-id="74098-185">Update the existing country-specific configuration</span></span>
<span data-ttu-id="74098-186">Litware, Inc. желает обновить конфигурацию BACS (Соединенное Королевство, вымышленный) и принять новые страновые требования для управления форматом электронных документов.</span><span class="sxs-lookup"><span data-stu-id="74098-186">Litware, Inc. needs to update the BACS (UK fictitious) configuration and adopt new country requirements for managing the format of the electronic document.</span></span> <span data-ttu-id="74098-187">Позже этот будет включено в новую версию этой конфигурации, которая будет предлагаться подписчикам службы, включая Proseware, Inc.</span><span class="sxs-lookup"><span data-stu-id="74098-187">Later, this will be enclosed in a new version of this configuration that will be offered for service subscribers, including Proseware, Inc.</span></span>  

<span data-ttu-id="74098-188">В реальных процессах, связанных с предоставлением услуг, каждая новая версия BACS (Соединенное Королевство, вымышленный) может быть импортирована компанией Proseware, Inc. из репозитория конфигураций Litware, Inc. в LCS.</span><span class="sxs-lookup"><span data-stu-id="74098-188">In real service provision related processes, each new version of BACS (UK fictitious) can be imported by Proseware, Inc. from Litware, Inc. configurations' LCS repository.</span></span> <span data-ttu-id="74098-189">В этой процедуре мы смоделируем это, обновив BACS (Соединенное Королевство, вымышленный) от имени поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="74098-189">In this procedure we will simulate this by updating BACS (UK fictitious) on behalf of a service provider.</span></span>  

1. <span data-ttu-id="74098-190">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="74098-190">Close the page.</span></span>
2. <span data-ttu-id="74098-191">Выберите поставщика Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="74098-191">Select Litware, inc. provider.</span></span>
3. <span data-ttu-id="74098-192">Щелкните "Установить как активное".</span><span class="sxs-lookup"><span data-stu-id="74098-192">Click Set active.</span></span>
4. <span data-ttu-id="74098-193">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="74098-193">Click Reporting configurations.</span></span>
5. <span data-ttu-id="74098-194">В дереве разверните узел "Платежи (упрощенная модель)".</span><span class="sxs-lookup"><span data-stu-id="74098-194">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="74098-195">В дереве выберите "Платежи (упрощенная модель)\BACS (Соединенное Королевство, вымышленный)".</span><span class="sxs-lookup"><span data-stu-id="74098-195">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="74098-196">Черновая версия, которой владеет поставщик BACS (Соединенное Королевство, вымышленный) Litware, Inc., выбирается для внесения изменений для поддержки новых требований для определенной страны.</span><span class="sxs-lookup"><span data-stu-id="74098-196">The draft version owned by Litware, Inc. provider BACS (UK fictitious) is selected to bring in changes to support new country-specific requirements.</span></span>  

## <a name="localize-the-base-format-of-the-electronic-document"></a><span data-ttu-id="74098-197">Локализация базового формата электронного документа</span><span class="sxs-lookup"><span data-stu-id="74098-197">Localize the base format of the electronic document</span></span>
<span data-ttu-id="74098-198">Предположим, что имеются новые характерные для данной страны особенности, которые должны поддерживаться Litware, Inc.:</span><span class="sxs-lookup"><span data-stu-id="74098-198">Assume that there are new country-specific requirements to be supported by Litware, Inc.:</span></span>  

- <span data-ttu-id="74098-199">Значение для кода SWIFT счета кредитора в каждой проводке по оплате.</span><span class="sxs-lookup"><span data-stu-id="74098-199">A value for the creditor's bank SWIFT code in each payment transaction.</span></span>
- <span data-ttu-id="74098-200">Ограничение в 100 символов для длины текста имени поставщика при создании файла.</span><span class="sxs-lookup"><span data-stu-id="74098-200">A limit of 100 characters for the length of text for the vendor's name in a generating file.</span></span>  
- <span data-ttu-id="74098-201">Новые требования для определенной страны</span><span class="sxs-lookup"><span data-stu-id="74098-201">New country-specific requirements</span></span>  
- <span data-ttu-id="74098-202">Выберите черновую версию необходимой конфигурации, чтобы применить необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="74098-202">Select the draft version of the desired configuration to introduce required changes.</span></span>  


1. <span data-ttu-id="74098-203">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="74098-203">Click Designer.</span></span>
2. <span data-ttu-id="74098-204">Щелкните "Развернуть/свернуть".</span><span class="sxs-lookup"><span data-stu-id="74098-204">Click Expand/collapse.</span></span>
3. <span data-ttu-id="74098-205">Щелкните "Развернуть/свернуть".</span><span class="sxs-lookup"><span data-stu-id="74098-205">Click Expand/collapse.</span></span>
4. <span data-ttu-id="74098-206">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Поставщик\Банк".</span><span class="sxs-lookup"><span data-stu-id="74098-206">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="74098-207">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="74098-207">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="74098-208">В дереве выберите "XML\Элемент".</span><span class="sxs-lookup"><span data-stu-id="74098-208">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="74098-209">В поле "Имя" введите "SWIFT".</span><span class="sxs-lookup"><span data-stu-id="74098-209">In the Name field, type 'SWIFT'.</span></span>
8. <span data-ttu-id="74098-210">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="74098-210">Click OK.</span></span>
9. <span data-ttu-id="74098-211">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Поставщик\Банк\SWIFT".</span><span class="sxs-lookup"><span data-stu-id="74098-211">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\SWIFT'.</span></span>
10. <span data-ttu-id="74098-212">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="74098-212">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="74098-213">В дереве выберите "Текст\строка".</span><span class="sxs-lookup"><span data-stu-id="74098-213">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="74098-214">Нажмите кнопку OK.</span><span class="sxs-lookup"><span data-stu-id="74098-214">Click OK.</span></span>
13. <span data-ttu-id="74098-215">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Поставщик\Имя\Строка".</span><span class="sxs-lookup"><span data-stu-id="74098-215">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="74098-216">В поле "Максимальная длина" введите "100".</span><span class="sxs-lookup"><span data-stu-id="74098-216">In the Maximum length field, enter '100'.</span></span>
15. <span data-ttu-id="74098-217">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="74098-217">Click the Mapping tab.</span></span>
16. <span data-ttu-id="74098-218">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="74098-218">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="74098-219">В дереве разверните узел "model\Payments".</span><span class="sxs-lookup"><span data-stu-id="74098-219">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="74098-220">В дереве разверните узел "модель\Платежи\Кредитор".</span><span class="sxs-lookup"><span data-stu-id="74098-220">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="74098-221">В дереве разверните узел "модель\Платежи\Агент".</span><span class="sxs-lookup"><span data-stu-id="74098-221">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
20. <span data-ttu-id="74098-222">В дереве выберите "модель\Платежи\Кредитор\Агент\SWIFT".</span><span class="sxs-lookup"><span data-stu-id="74098-222">In the tree, select 'model\Payments\Creditor\Agent\SWIFT'.</span></span>
21. <span data-ttu-id="74098-223">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура = модель.Платежи\Поставщик\Банк\SWIFT\Строка".</span><span class="sxs-lookup"><span data-stu-id="74098-223">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\SWIFT\String'.</span></span>
22. <span data-ttu-id="74098-224">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="74098-224">Click Bind.</span></span>
23. <span data-ttu-id="74098-225">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="74098-225">Click Save.</span></span>

## <a name="validate-the-localized-format"></a><span data-ttu-id="74098-226">Проверка локализованного формата</span><span class="sxs-lookup"><span data-stu-id="74098-226">Validate the localized format</span></span>
1. <span data-ttu-id="74098-227">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="74098-227">Click Validate.</span></span>
2. <span data-ttu-id="74098-228">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="74098-228">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a><span data-ttu-id="74098-229">Изменение статуса текущей версии конфигурации базового формата</span><span class="sxs-lookup"><span data-stu-id="74098-229">Change the status of the current version of the base format configuration</span></span>
<span data-ttu-id="74098-230">Измените статус обновленной конфигурации базового формата с "Черновик" на "Завершено", чтобы сделать ее доступной для создания платежных документов и обновлений производных конфигураций форматов.</span><span class="sxs-lookup"><span data-stu-id="74098-230">Change the status of the updated base format configuration from Draft to Completed to make it available for generation of payment documents and updates of format configurations derived from it.</span></span>  

1. <span data-ttu-id="74098-231">Щелкните "Изменить статус".</span><span class="sxs-lookup"><span data-stu-id="74098-231">Click Change status.</span></span>

    <span data-ttu-id="74098-232">Обратите внимание, что текущая версия выбранной конфигурации имеет статус "Черновик".</span><span class="sxs-lookup"><span data-stu-id="74098-232">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="74098-233">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="74098-233">Click Complete.</span></span>
3. <span data-ttu-id="74098-234">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="74098-234">In the Description field, type a value.</span></span>
4. <span data-ttu-id="74098-235">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="74098-235">Click OK.</span></span>
5. <span data-ttu-id="74098-236">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="74098-236">In the list, find and select the desired record.</span></span>

## <a name="change-the-base-version-for-the-custom-format-configuration"></a><span data-ttu-id="74098-237">Изменение базовой версии конфигурации пользовательского формата</span><span class="sxs-lookup"><span data-stu-id="74098-237">Change the base version for the custom format configuration</span></span>

<span data-ttu-id="74098-238">Proseware, Inc. получает уведомление, что новая версия 1.2 конфигурации BACS (Соединенное Королевство, вымышленный) доступна для создания электронных платежных документов в соответствии с последними объявленными требованиями для конкретной страны.</span><span class="sxs-lookup"><span data-stu-id="74098-238">Proseware, Inc. is informed that a new version 1.2 of BACS (UK fictitious) configuration is available to generate electronic payment documents in accordance to recently announced country-specific requirements.</span></span> <span data-ttu-id="74098-239">Proseware, Inc. желает начать использовать ее как стандарт для этой страны.</span><span class="sxs-lookup"><span data-stu-id="74098-239">Proseware, Inc. wants to start using it as a standard for the country.</span></span>  

<span data-ttu-id="74098-240">Для Proseware, Inc. необходимо изменить версию базовой конфигурации для пользовательской конфигурации BACS (Соединенное Королевство, вымышленный, пользовательский).</span><span class="sxs-lookup"><span data-stu-id="74098-240">To do this, Proseware, Inc. needs to change the base configuration version for the custom configuration BACS (UK fictitious custom).</span></span> <span data-ttu-id="74098-241">Вместо версии 1.1 BACS (Соединенное Королевство, вымышленный) используйте новую версию 1.2.</span><span class="sxs-lookup"><span data-stu-id="74098-241">Instead of version 1.1 of BACS (UK fictitious) use new version 1.2.</span></span>  

1. <span data-ttu-id="74098-242">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="74098-242">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="74098-243">Выберите поставщика Proseware, Inc., чтобы пометить его в качестве активного.</span><span class="sxs-lookup"><span data-stu-id="74098-243">Select the Proseware, Inc. provider to mark it as active.</span></span>
3. <span data-ttu-id="74098-244">Щелкните "Установить как активное".</span><span class="sxs-lookup"><span data-stu-id="74098-244">Click Set active.</span></span>
4. <span data-ttu-id="74098-245">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="74098-245">Click Reporting configurations.</span></span>
5. <span data-ttu-id="74098-246">В дереве разверните узел "Платежи (упрощенная модель)".</span><span class="sxs-lookup"><span data-stu-id="74098-246">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="74098-247">В дереве разверните узел "Платежи (упрощенная модель)\BACS (Соединенное Королевство, вымышленный)".</span><span class="sxs-lookup"><span data-stu-id="74098-247">In the tree, expand 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
7. <span data-ttu-id="74098-248">В дереве выберите "Платежи (упрощенная модель)\BACS (Соединенное Королевство, вымышленный)\BACS (Соединенное Королевство, вымышленный, пользовательский)".</span><span class="sxs-lookup"><span data-stu-id="74098-248">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom)'.</span></span>

    <span data-ttu-id="74098-249">Выберите конфигурацию BACS (Соединенное Королевство, вымышленный, пользовательский), которой владеет Proseware, Inc.</span><span class="sxs-lookup"><span data-stu-id="74098-249">Select the BACS (UK fictitious custom) configuration, which is owned by Proseware, Inc.</span></span>  

    <span data-ttu-id="74098-250">Используйте черновую версию выбранной конфигурации, чтобы применить необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="74098-250">Use the draft version of the selected configuration to introduce required changes.</span></span>  

8. <span data-ttu-id="74098-251">Щелкните "Повторно разместить".</span><span class="sxs-lookup"><span data-stu-id="74098-251">Click Rebase.</span></span>

    <span data-ttu-id="74098-252">Выберите новую версию 1.2 базовой конфигурации для использования в качестве новой базы для обновления конфигурации.</span><span class="sxs-lookup"><span data-stu-id="74098-252">Select the new version 1.2 of the base configuration to be applied as a new base for updating the configuration.</span></span>  

9. <span data-ttu-id="74098-253">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="74098-253">Click OK.</span></span>

    <span data-ttu-id="74098-254">Обратите внимание, что были обнаружены конфликты между объединением пользовательской версии и новой базовой версии, представляющей некоторые изменения формата, которые невозможно объединить автоматически.</span><span class="sxs-lookup"><span data-stu-id="74098-254">Note that some conflicts have been discovered between merging the custom version and a new base version representing some format changes that can't be merged automatically.</span></span>  

## <a name="resolve-rebase-conflicts"></a><span data-ttu-id="74098-255">Разрешение конфликтов повторного размещения</span><span class="sxs-lookup"><span data-stu-id="74098-255">Resolve rebase conflicts</span></span>
1. <span data-ttu-id="74098-256">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="74098-256">Click Designer.</span></span>
    
    <span data-ttu-id="74098-257">Обратите внимание, что изменения лимита длины текста имени поставщика не могут быть разрешены автоматически.</span><span class="sxs-lookup"><span data-stu-id="74098-257">Note that changes to the vendor's name text length limit couldn't be resolved automatically.</span></span> <span data-ttu-id="74098-258">Поэтому это отображается в списке конфликтов.</span><span class="sxs-lookup"><span data-stu-id="74098-258">Therefore, this is presented in a conflicts list.</span></span> <span data-ttu-id="74098-259">Для каждого конфликта типа "Обновление" доступны следующие варианты: - Применить предыдущее базовое значение (кнопка вверху сетки), чтобы использовать предыдущее значение базовой версии (в нашем случае это 0).</span><span class="sxs-lookup"><span data-stu-id="74098-259">For each conflict of type Update, the following options are available:  - Apply a prior base value (button on top of the grid) to bring in the previous base version value (0 in our case).</span></span>  <span data-ttu-id="74098-260">- Применить базовое значение (кнопка вверху сетки), чтобы использовать новое значение базовой версии (в нашем случае это 100).</span><span class="sxs-lookup"><span data-stu-id="74098-260">- Apply a base value (button on top of the grid) to bring in the new base version value (100 in our case).</span></span>  <span data-ttu-id="74098-261">- Сохранить собственное (пользовательское) значение (в данном случае — 60).</span><span class="sxs-lookup"><span data-stu-id="74098-261">- Keep your own (custom) value (60 in our case).</span></span>  <span data-ttu-id="74098-262">Щелкните "Применить базовое значение", чтобы применить лимит определенной страны равный 100 символам для длины текста имени поставщика.</span><span class="sxs-lookup"><span data-stu-id="74098-262">Click Apply base value to apply a country-specific limit of 100 characters for vendor's name text length.</span></span>  

    <span data-ttu-id="74098-263">Обратите внимание, что Proseware, Inc. и Litware, Inc. имеют пользовательскую и локальную версии данного формата, использующие коды IBAN и SWIFT со связанными компонентами, которые автоматически объединяются в формат управления.</span><span class="sxs-lookup"><span data-stu-id="74098-263">Note that Proseware, Inc. and Litware, Inc. have custom and local versions of this format using IBAN and SWIFT codes with related components that are automatically merged in the managing format.</span></span>  

2. <span data-ttu-id="74098-264">Щелкните "Применить базовое значение".</span><span class="sxs-lookup"><span data-stu-id="74098-264">Click Apply base value.</span></span>

    <span data-ttu-id="74098-265">Щелкните "Применить базовое значение", чтобы применить лимит определенной страны равный 100 символам для имен поставщиков.</span><span class="sxs-lookup"><span data-stu-id="74098-265">Click Apply base value to apply the country-specific limit of 100 characters for vendor names.</span></span>  

3. <span data-ttu-id="74098-266">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="74098-266">Click Save.</span></span>

    <span data-ttu-id="74098-267">В результате сохранения формата будут разрешены конфликты из списка конфликтов.</span><span class="sxs-lookup"><span data-stu-id="74098-267">Saving the format will remove resolved conflicts from the conflicts list.</span></span>  

4. <span data-ttu-id="74098-268">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="74098-268">Close the page.</span></span>

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a><span data-ttu-id="74098-269">Изменение статуса новой версии конфигурации пользовательского формата</span><span class="sxs-lookup"><span data-stu-id="74098-269">Change the status of the new version of the custom format configuration</span></span>
1. <span data-ttu-id="74098-270">Щелкните "Изменить статус".</span><span class="sxs-lookup"><span data-stu-id="74098-270">Click Change status.</span></span>

    <span data-ttu-id="74098-271">Измените статус обновленной конфигурации пользовательского формата с "Черновик" на "Завершено".</span><span class="sxs-lookup"><span data-stu-id="74098-271">Change the status of the updated, custom format configuration from Draft to Completed.</span></span> <span data-ttu-id="74098-272">После этого конфигурация формата станет доступна для создания платежных документов.</span><span class="sxs-lookup"><span data-stu-id="74098-272">This will make the format configuration available for generating payment documents.</span></span> <span data-ttu-id="74098-273">Обратите внимание, что текущая версия выбранной конфигурации имеет статус "Черновик".</span><span class="sxs-lookup"><span data-stu-id="74098-273">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="74098-274">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="74098-274">Click Complete.</span></span>
3. <span data-ttu-id="74098-275">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="74098-275">In the Description field, type a value.</span></span>
4. <span data-ttu-id="74098-276">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="74098-276">Click OK.</span></span>

    <span data-ttu-id="74098-277">Обратите внимание, что созданная конфигурация сохраняется как полная версия 1.2.2: версия 2 базового формата BACS (Соединенное Королевство, вымышленный, пользовательский), которая основана на версии 2 базового формата BACS (Соединенное Королевство, вымышленный), который основан на версии 1 модели данных платежей (упрощенной модели).</span><span class="sxs-lookup"><span data-stu-id="74098-277">Note that the created configuration is saved as completed version 1.2.2: version 2 of base BACS (UK fictitious custom) format, which is based on version 2 of base BACS (UK fictitious) format, which is based on version 1 of Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-for-payment-files-generation"></a><span data-ttu-id="74098-278">Проверка настроенного формата для создания файлов платежей</span><span class="sxs-lookup"><span data-stu-id="74098-278">Test the customized format for payment files generation</span></span>
<span data-ttu-id="74098-279">Выполните шаги, описанные в процедуре "Использование созданного формата для создания электронных документов для платежей", в параллельном сеансе Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="74098-279">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in parallel Finance and Operations session.</span></span> <span data-ttu-id="74098-280">Выберите созданный формат BACS (Соединенное Королевство, вымышленный, пользовательский) в параметрах метода электронного платежа.</span><span class="sxs-lookup"><span data-stu-id="74098-280">Select the created 'BACS (UK fictitious custom)' format in electronic payment method parameters.</span></span> <span data-ttu-id="74098-281">Убедитесь, что созданный файл платежа содержит недавно введенный компанией Proseware, Inc. узел XML, представляющий код счета IBAN в соответствии с региональными требованиями.</span><span class="sxs-lookup"><span data-stu-id="74098-281">Make sure that the created payment file contains recently introduced by Proseware, Inc. XML node presenting IBAN account code in accordance to regional requirements.</span></span> <span data-ttu-id="74098-282">Файл также должен содержать недавно введенный компанией Litware, Inc. узел XML, представляющий банковский код SWIFT в соответствии со страновыми требованиями.</span><span class="sxs-lookup"><span data-stu-id="74098-282">The file also should contain the recently introduced by Litware, Inc. XML node presenting SWIFT bank code in accordance to country requirements.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]