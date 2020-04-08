---
title: Электронная отчетность — Сопоставление компонентов созданного формата с элементами модели данных (ноябрь 2016 г.)
description: В следующей процедуре показано, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может сопоставить элементы модели данных с компонентами созданной конфигурации электронной отчетности (ER), определяющей формат электронных документов для бизнес-домена платежей.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e77de79113e3f44da1d7f92f17a446df86f6852e
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143038"
---
# <a name="er-map-components-of-the-created-format-to-data-model-elements-november-2016"></a><span data-ttu-id="0b6cd-103">Электронная отчетность — Сопоставление компонентов созданного формата с элементами модели данных (ноябрь 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="0b6cd-103">ER Map components of the created format to data model elements (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b6cd-104">В следующей процедуре показано, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может сопоставить элементы модели данных с компонентами созданной конфигурации электронной отчетности (ER), определяющей формат электронных документов для бизнес-домена платежей.</span><span class="sxs-lookup"><span data-stu-id="0b6cd-104">The following procedure shows how a user in either the System administrator or Electronic reporting developer role can map data model elements to components of the created Electronic reporting (ER) configuration, which defines an electronic document format for the payments business domain.</span></span> <span data-ttu-id="0b6cd-105">Этот формат будет использоваться позднее для создания электронных документов для обработки платежей.</span><span class="sxs-lookup"><span data-stu-id="0b6cd-105">This format will be used later to generate electronic documents for processing payments.</span></span> <span data-ttu-id="0b6cd-106">В этом примере вам предстоит создать конфигурацию формата для демонстрационной компании Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="0b6cd-106">In this example, you will create a format configuration for the sample company, 'Litware, Inc.'.</span></span> <span data-ttu-id="0b6cd-107">Эти шаги можно выполнить в любой компании, поскольку конфигурации электронной отчетности используются всеми компаниями.</span><span class="sxs-lookup"><span data-stu-id="0b6cd-107">These steps can be performed in any company as ER configurations are shared for all companies.</span></span> <span data-ttu-id="0b6cd-108">Для выполнения этих шагов необходимо сначала выполнить шаги в руководстве по задаче "Создание конфигурации формата".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-108">To complete these steps, you must first complete the steps in the "Create a format configuration" task guide.</span></span>


## <a name="select-a-format-configuration"></a><span data-ttu-id="0b6cd-109">Выбор конфигурации формата</span><span class="sxs-lookup"><span data-stu-id="0b6cd-109">Select a format configuration</span></span>
1. <span data-ttu-id="0b6cd-110">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="0b6cd-111">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="0b6cd-112">В дереве разверните узел "Платежи (упрощенная модель)".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-112">In the tree, expand 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="0b6cd-113">В дереве выберите "Платежи (упрощенная модель)\BACS (Великобритания, вымышленный)".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-113">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
5. <span data-ttu-id="0b6cd-114">Выберите Конструктор.</span><span class="sxs-lookup"><span data-stu-id="0b6cd-114">Click Designer.</span></span>

## <a name="map-format-components-to-data-model-elements"></a><span data-ttu-id="0b6cd-115">Сопоставление компонентов формата с элементами модели данных</span><span class="sxs-lookup"><span data-stu-id="0b6cd-115">Map format components to data model elements</span></span>
1. <span data-ttu-id="0b6cd-116">Щелкните "Развернуть/свернуть".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-116">Click Expand/collapse.</span></span>
2. <span data-ttu-id="0b6cd-117">Перейдите на вкладку "Сопоставление".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-117">Click the Mapping tab.</span></span>
3. <span data-ttu-id="0b6cd-118">В дереве разверните узел "model".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-118">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="0b6cd-119">В дереве выберите "Xml\Сообщение\ProcessingDate\DateTime".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-119">In the tree, select 'Xml\Message\ProcessingDate\DateTime'.</span></span>
5. <span data-ttu-id="0b6cd-120">В дереве выберите "модель\ProcessingDateTime".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-120">In the tree, select 'model\ProcessingDateTime'.</span></span>
6. <span data-ttu-id="0b6cd-121">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-121">Click Bind.</span></span>
7. <span data-ttu-id="0b6cd-122">В дереве выберите "Xml\Сообщение\MessageId\Строка".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-122">In the tree, select 'Xml\Message\MessageId\String'.</span></span>
8. <span data-ttu-id="0b6cd-123">В дереве выберите "модель\MessageIdentification".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-123">In the tree, select 'model\MessageIdentification'.</span></span>
9. <span data-ttu-id="0b6cd-124">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-124">Click Bind.</span></span>
10. <span data-ttu-id="0b6cd-125">В дереве разверните узел "model\Payments".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-125">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="0b6cd-126">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Сумма\Строка".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-126">In the tree, select 'Xml\Message\Payments\Item\Amount\String'.</span></span>
12. <span data-ttu-id="0b6cd-127">В дереве выберите "модель\Платежи\InstructedAmount".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-127">In the tree, select 'model\Payments\InstructedAmount'.</span></span>
13. <span data-ttu-id="0b6cd-128">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-128">Click Bind.</span></span>
14. <span data-ttu-id="0b6cd-129">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\TransDate\DateTime".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-129">In the tree, select 'Xml\Message\Payments\Item\TransDate\DateTime'.</span></span>
15. <span data-ttu-id="0b6cd-130">В дереве выберите "модель\Платежи\TransactionDate".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-130">In the tree, select 'model\Payments\TransactionDate'.</span></span>
16. <span data-ttu-id="0b6cd-131">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-131">Click Bind.</span></span>
17. <span data-ttu-id="0b6cd-132">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Описание\Строка".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-132">In the tree, select 'Xml\Message\Payments\Item\Description\String'.</span></span>
18. <span data-ttu-id="0b6cd-133">В дереве выберите "Модель\Платежи\Описание".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-133">In the tree, select 'model\Payments\Description'.</span></span>
19. <span data-ttu-id="0b6cd-134">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-134">Click Bind.</span></span>
20. <span data-ttu-id="0b6cd-135">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Валюта\Строка".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-135">In the tree, select 'Xml\Message\Payments\Item\Currency\String'.</span></span>
21. <span data-ttu-id="0b6cd-136">В дереве выберите "модель\Платежи\Валюта".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-136">In the tree, select 'model\Payments\Currency'.</span></span>
22. <span data-ttu-id="0b6cd-137">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-137">Click Bind.</span></span>
23. <span data-ttu-id="0b6cd-138">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Код".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-138">In the tree, select 'Xml\Message\Payments\Item\Id'.</span></span>
24. <span data-ttu-id="0b6cd-139">В дереве выберите "модель\Платежи\End2EndID".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-139">In the tree, select 'model\Payments\End2EndID'.</span></span>
25. <span data-ttu-id="0b6cd-140">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-140">Click Bind.</span></span>
26. <span data-ttu-id="0b6cd-141">В дереве разверните узел "модель\Платежи\Кредитор".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-141">In the tree, expand 'model\Payments\Creditor'.</span></span>
27. <span data-ttu-id="0b6cd-142">В дереве разверните узел "модель\Платежи\Кредитор\Счет".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-142">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
28. <span data-ttu-id="0b6cd-143">В дереве разверните узел "модель\Платежи\Агент".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-143">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
29. <span data-ttu-id="0b6cd-144">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Поставщик\Имя\Строка".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-144">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
30. <span data-ttu-id="0b6cd-145">В дереве выберите "модель\Платежи\Кредитор\Имя".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-145">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
31. <span data-ttu-id="0b6cd-146">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-146">Click Bind.</span></span>
32. <span data-ttu-id="0b6cd-147">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Поставщик\Банк\RoutingNumber\Строка".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String'.</span></span>
33. <span data-ttu-id="0b6cd-148">В дереве выберите "модель\Платежи\Кредитор\Агент\RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-148">In the tree, select 'model\Payments\Creditor\Agent\RoutingNumber'.</span></span>
34. <span data-ttu-id="0b6cd-149">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-149">Click Bind.</span></span>
35. <span data-ttu-id="0b6cd-150">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Поставщик\Банк\AccountNumber\Строка".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-150">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String'.</span></span>
36. <span data-ttu-id="0b6cd-151">В дереве выберите "модель\Платежи\Кредитор\Счет\Номер".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-151">In the tree, select 'model\Payments\Creditor\Account\Number'.</span></span>
37. <span data-ttu-id="0b6cd-152">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-152">Click Bind.</span></span>
38. <span data-ttu-id="0b6cd-153">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Плательщик\Имя\Строка".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-153">In the tree, select 'Xml\Message\Payments\Item\Payer\Name\String'.</span></span>
39. <span data-ttu-id="0b6cd-154">В дереве разверните узел "модель\Платежи\Дебитор".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-154">In the tree, expand 'model\Payments\Debtor'.</span></span>
40. <span data-ttu-id="0b6cd-155">В дереве разверните узел "модель\Платежи\Дебитор\Счет".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-155">In the tree, expand 'model\Payments\Debtor\Account'.</span></span>
41. <span data-ttu-id="0b6cd-156">В дереве разверните узел "модель\Платежи\Дебитор\Агент".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-156">In the tree, expand 'model\Payments\Debtor\Agent'.</span></span>
42. <span data-ttu-id="0b6cd-157">В дереве выберите "модель\Платежи\Дебитор\Имя".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-157">In the tree, select 'model\Payments\Debtor\Name'.</span></span>
43. <span data-ttu-id="0b6cd-158">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-158">Click Bind.</span></span>
44. <span data-ttu-id="0b6cd-159">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Плательщик\Банк\RoutingNumber\Строка".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-159">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String'.</span></span>
45. <span data-ttu-id="0b6cd-160">В дереве выберите "модель\Платежи\Дебитор\Агент\RoutingNumber".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-160">In the tree, select 'model\Payments\Debtor\Agent\RoutingNumber'.</span></span>
46. <span data-ttu-id="0b6cd-161">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-161">Click Bind.</span></span>
47. <span data-ttu-id="0b6cd-162">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура\Плательщик\Банк\AccountNumber\Строка".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-162">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String'.</span></span>
48. <span data-ttu-id="0b6cd-163">В дереве выберите "модель\Платежи\Дебитор\Счет\Номер".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-163">In the tree, select 'model\Payments\Debtor\Account\Number'.</span></span>
49. <span data-ttu-id="0b6cd-164">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-164">Click Bind.</span></span>
50. <span data-ttu-id="0b6cd-165">В дереве выберите "Xml\Сообщение\Платежи\Номенклатура".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-165">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="0b6cd-166">В дереве выберите "модель\Платежи".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-166">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="0b6cd-167">Щелкните "Связать".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-167">Click Bind.</span></span>
53. <span data-ttu-id="0b6cd-168">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-168">Click Save.</span></span>

## <a name="validate-format-mapping"></a><span data-ttu-id="0b6cd-169">Проверка сопоставления формата</span><span class="sxs-lookup"><span data-stu-id="0b6cd-169">Validate format mapping</span></span>
1. <span data-ttu-id="0b6cd-170">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-170">Click Validate.</span></span>
    * <span data-ttu-id="0b6cd-171">Проверьте новое сопоставление, чтобы убедиться, что все привязки работают верно.</span><span class="sxs-lookup"><span data-stu-id="0b6cd-171">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="0b6cd-172">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="0b6cd-172">Close the page.</span></span>

## <a name="change-status-of-the-current-version-of-format-configuration"></a><span data-ttu-id="0b6cd-173">Изменение статуса текущей версии конфигурации формата</span><span class="sxs-lookup"><span data-stu-id="0b6cd-173">Change status of the current version of format configuration</span></span>
<span data-ttu-id="0b6cd-174">На следующих шагах вам предстоит изменить статус конфигурации формата с "Черновик" на "Завершено", чтобы сделать ее доступной для создания платежных документов.</span><span class="sxs-lookup"><span data-stu-id="0b6cd-174">In the next steps, you'll change the status of the format configuration from Draft to Completed to make it available for payment document generation.</span></span>  
1. <span data-ttu-id="0b6cd-175">Щелкните "Изменить статус".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-175">Click Change status.</span></span>
2. <span data-ttu-id="0b6cd-176">Щелкните "Завершить".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-176">Click Complete.</span></span>
3. <span data-ttu-id="0b6cd-177">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="0b6cd-177">In the Description field, type a value.</span></span>
    * <span data-ttu-id="0b6cd-178">Например, "версия 1".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-178">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="0b6cd-179">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-179">Click OK.</span></span>
5. <span data-ttu-id="0b6cd-180">Выберите завершенную версию текущей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0b6cd-180">Select completed version of the current configuration.</span></span>
    * <span data-ttu-id="0b6cd-181">Обратите внимание, что конфигурация сохраняется как завершенная версия 1.1. Это версия 1 формата, основанная на версии 1 модели данных.</span><span class="sxs-lookup"><span data-stu-id="0b6cd-181">Note that the configuration is saved as completed version 1.1: version 1 of the format based on the version 1 of the data model.</span></span>  

## <a name="define-effective-date-for-completed-version-of-format"></a><span data-ttu-id="0b6cd-182">Определение даты вступления в силу для завершенной версии формата</span><span class="sxs-lookup"><span data-stu-id="0b6cd-182">Define effective date for completed version of format</span></span>
<span data-ttu-id="0b6cd-183">Каждую версию формата можно установить в качестве доступной для использования начиная с указанной даты.</span><span class="sxs-lookup"><span data-stu-id="0b6cd-183">Each format version can be configured as available for usage starting from a certain date.</span></span> <span data-ttu-id="0b6cd-184">Если на определенную дату активно несколько версий формата, для использования выбирается последний формат (по номеру версии).</span><span class="sxs-lookup"><span data-stu-id="0b6cd-184">When more than one format version is active on a certain date, the latest format (based on version number) will be selected for usage.</span></span> <span data-ttu-id="0b6cd-185">Для выбора правильной версии используется значение даты сеанса.</span><span class="sxs-lookup"><span data-stu-id="0b6cd-185">The session date value is used for proper version selection.</span></span>  

## <a name="restrict-access-to-created-format-from-companies"></a><span data-ttu-id="0b6cd-186">Ограничение доступа к созданному формату из компаний</span><span class="sxs-lookup"><span data-stu-id="0b6cd-186">Restrict access to created format from companies</span></span>
1. <span data-ttu-id="0b6cd-187">Разверните раздел "Коды стран/регионов ISO".</span><span class="sxs-lookup"><span data-stu-id="0b6cd-187">Expand the ISO Country/region codes section.</span></span>
    * <span data-ttu-id="0b6cd-188">Доступ к каждому формату можно ограничить, указав конкретные страны/регионы, в которых может использоваться формат.</span><span class="sxs-lookup"><span data-stu-id="0b6cd-188">Each format access can be restricted by identifying particular countries/regions in which a format is applicable.</span></span> <span data-ttu-id="0b6cd-189">Если список стран/регионов для формата пуст, этот формат можно использовать в любой компании.</span><span class="sxs-lookup"><span data-stu-id="0b6cd-189">When the list of countries/regions for particular format is empty, this format can be used in any company.</span></span> <span data-ttu-id="0b6cd-190">Если в этот список стран/регионов вставлены какие-либо коды стран/регионов по ISO, этот формат можно использовать только в компаниях, у которых основной адрес находится в этой стране/регионе.</span><span class="sxs-lookup"><span data-stu-id="0b6cd-190">When some ISO country/region codes are inserted in the list of countries/regions, the format can only be use in companies if the primary address is in the country/region.</span></span>  

