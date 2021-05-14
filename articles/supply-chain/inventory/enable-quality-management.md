---
title: Включение управления качеством и несоответствием
description: В этом разделе представлен обзор процесса настройки и конфигурирования контроля качества и функций управления несоответствиями в Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d5da648e31d07d054246f5d308a6c6cdeb506c
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956262"
---
# <a name="enable-quality-and-nonconformance-management"></a><span data-ttu-id="67eb0-103">Включение управления качеством и несоответствием</span><span class="sxs-lookup"><span data-stu-id="67eb0-103">Enable quality and nonconformance management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67eb0-104">В этом разделе представлен обзор процесса настройки и конфигурирования контроля качества и функций управления несоответствиями в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="67eb0-104">This topic provides an overview of the process for setting up and configuring quality and nonconformance management features in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a><span data-ttu-id="67eb0-105">Включение управления качеством и несоответствием</span><span class="sxs-lookup"><span data-stu-id="67eb0-105">Enable quality and nonconformance management</span></span>

<span data-ttu-id="67eb0-106">Выполните следующие действия, чтобы включить управление качеством в системе.</span><span class="sxs-lookup"><span data-stu-id="67eb0-106">Follow these steps to enable quality management on your system.</span></span>

1. <span data-ttu-id="67eb0-107">Перейдите в раздел **Управление запасами \> Настройка \> Параметры управления запасами и складами**.</span><span class="sxs-lookup"><span data-stu-id="67eb0-107">Go to **Inventory management \> Setup \> Inventory and warehouse management parameters**.</span></span>
1. <span data-ttu-id="67eb0-108">На вкладке **Управление качеством** установите для параметра **Использовать управление качеством** значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="67eb0-108">On the **Quality management** tab, set the **Use quality management** option to *Yes*.</span></span>
1. <span data-ttu-id="67eb0-109">В поле **Почасовая ставка** введите почасовую ставку в местной валюте.</span><span class="sxs-lookup"><span data-stu-id="67eb0-109">In the **Hourly rate** field, enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="67eb0-110">Почасовая ставка используется для расчета затрат на операции, связанные с несоответствием.</span><span class="sxs-lookup"><span data-stu-id="67eb0-110">The hourly rate is used to calculate costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="67eb0-111">Почасовая ставка и вычисленная стоимость являются справочной информацией для несоответствия.</span><span class="sxs-lookup"><span data-stu-id="67eb0-111">The hourly rate and calculated costs provide reference information for a nonconformance.</span></span> <span data-ttu-id="67eb0-112">Они не взаимодействуют с другими функциями.</span><span class="sxs-lookup"><span data-stu-id="67eb0-112">They don't interact with other functionality.</span></span>
1. <span data-ttu-id="67eb0-113">Выберите **Настройка отчетов**.</span><span class="sxs-lookup"><span data-stu-id="67eb0-113">Select **Report setup**.</span></span>
1. <span data-ttu-id="67eb0-114">Добавьте новые строки для различных типов отчетов и выберите тип документа, который будет использоваться для каждого отчета.</span><span class="sxs-lookup"><span data-stu-id="67eb0-114">Add new lines for the various report types, and select the type of document to use for each report.</span></span>
1. <span data-ttu-id="67eb0-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="67eb0-115">Close the page.</span></span>
1. <span data-ttu-id="67eb0-116">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="67eb0-116">Close the page.</span></span>

## <a name="quality-management-configuration-process"></a><span data-ttu-id="67eb0-117">Процесс настройки управления качеством</span><span class="sxs-lookup"><span data-stu-id="67eb0-117">Quality management configuration process</span></span>

<span data-ttu-id="67eb0-118">Прежде чем можно будет начать пользоваться функциями управления качеством и создавать заказы для контроля качества, необходимо настроить систему и необходимые компоненты.</span><span class="sxs-lookup"><span data-stu-id="67eb0-118">Before you can start to use the quality management features and generate quality orders, you must configure the system and prerequisites.</span></span> <span data-ttu-id="67eb0-119">Ниже приводится список шагов, необходимых для настройки управления качеством.</span><span class="sxs-lookup"><span data-stu-id="67eb0-119">Here is a list of the steps that are required to configure quality management.</span></span>

1. <span data-ttu-id="67eb0-120">[Включение управления качеством и несоответствием](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="67eb0-120">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="67eb0-121">Необязательно: [Настройка инструментов тестирования](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="67eb0-121">Optional: [Configure test instruments](quality-test-instruments.md).</span></span>
1. <span data-ttu-id="67eb0-122">[Настройка тестов](quality-tests.md).</span><span class="sxs-lookup"><span data-stu-id="67eb0-122">[Configure tests](quality-tests.md).</span></span>
1. <span data-ttu-id="67eb0-123">[Настройка переменных тестирования и результаты](quality-test-variables.md).</span><span class="sxs-lookup"><span data-stu-id="67eb0-123">[Configure test variables and outcomes](quality-test-variables.md).</span></span>
1. <span data-ttu-id="67eb0-124">[Настройка групп тестирования](quality-test-groups.md).</span><span class="sxs-lookup"><span data-stu-id="67eb0-124">[Configure test groups](quality-test-groups.md).</span></span>
1. <span data-ttu-id="67eb0-125">Необязательно: [Настройка групп контроля качества и связь с продуктами](quality-groups.md).</span><span class="sxs-lookup"><span data-stu-id="67eb0-125">Optional: [Configure quality groups, and link to products](quality-groups.md).</span></span>
1. <span data-ttu-id="67eb0-126">Необязательно: [Настройка связей контроля качества](quality-associations.md).</span><span class="sxs-lookup"><span data-stu-id="67eb0-126">Optional: [Configure quality associations](quality-associations.md).</span></span>

<span data-ttu-id="67eb0-127">После завершения настройки можно начать создавать и обрабатывать заказы для контроля качества.</span><span class="sxs-lookup"><span data-stu-id="67eb0-127">After the configuration is completed, you can start to create and process quality orders.</span></span> <span data-ttu-id="67eb0-128">Для получения дополнительной информации о том, как создавать и работать с заказами для контроля качества фрагменты, см. [Заказ на контроль качества](quality-orders.md).</span><span class="sxs-lookup"><span data-stu-id="67eb0-128">For more information about how to create and work with quality orders, see [Quality orders](quality-orders.md).</span></span>

## <a name="nonconformance-management-configuration-process"></a><span data-ttu-id="67eb0-129">Процесс настройки управления несоответствиями</span><span class="sxs-lookup"><span data-stu-id="67eb0-129">Nonconformance management configuration process</span></span>

<span data-ttu-id="67eb0-130">Прежде чем можно будет начать пользоваться функциями управления несоответствиями и создавать несоответствия, необходимо настроить систему и необходимые компоненты.</span><span class="sxs-lookup"><span data-stu-id="67eb0-130">Before you can start to use the nonconformance management features and generate nonconformances, you must configure the system and prerequisites.</span></span> <span data-ttu-id="67eb0-131">Ниже приводится список шагов, необходимых для настройки управления несоответствиями.</span><span class="sxs-lookup"><span data-stu-id="67eb0-131">Here is a list of the steps that are required to configure nonconformance management.</span></span>

1. <span data-ttu-id="67eb0-132">[Включение управления качеством и несоответствием](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="67eb0-132">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="67eb0-133">[Настройка работников, ответственных за утверждение несоответствий](quality-responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="67eb0-133">[Configure workers who are responsible for approving nonconformances](quality-responsible-workers.md).</span></span>
1. <span data-ttu-id="67eb0-134">[Настройка типов проблем](quality-problem-types.md).</span><span class="sxs-lookup"><span data-stu-id="67eb0-134">[Configure problem types](quality-problem-types.md).</span></span>
1. <span data-ttu-id="67eb0-135">[Настройка зон карантина](quality-quarantine-zones.md).</span><span class="sxs-lookup"><span data-stu-id="67eb0-135">[Configure quarantine zones](quality-quarantine-zones.md).</span></span>
1. <span data-ttu-id="67eb0-136">[Настройка типов диагностики](quality-diagnostic-types.md).</span><span class="sxs-lookup"><span data-stu-id="67eb0-136">[Configure diagnostic types](quality-diagnostic-types.md).</span></span>
1. <span data-ttu-id="67eb0-137">[Настройка операций](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="67eb0-137">[Configure operations](quality-operations.md).</span></span>
1. <span data-ttu-id="67eb0-138">Необязательно: [Настройка расходов по контролю качества](quality-charges.md).</span><span class="sxs-lookup"><span data-stu-id="67eb0-138">Optional: [Configure quality charges](quality-charges.md).</span></span>

<span data-ttu-id="67eb0-139">После завершения настройки можно начать создавать и обрабатывать несоответствия.</span><span class="sxs-lookup"><span data-stu-id="67eb0-139">After the configuration is completed, you can start to create and process nonconformances.</span></span> <span data-ttu-id="67eb0-140">Дополнительные сведения о способе создания и работы с несоответствиями см. в разделе [Создание и обработка несоответствий](tasks/create-process-non-conformance.md).</span><span class="sxs-lookup"><span data-stu-id="67eb0-140">For more information about how to create and work with nonconformances, see [Create and process nonconformances](tasks/create-process-non-conformance.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="67eb0-141">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="67eb0-141">Additional resources</span></span>

- [<span data-ttu-id="67eb0-142">Обзор управления качеством</span><span class="sxs-lookup"><span data-stu-id="67eb0-142">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="67eb0-143">Включение управления качеством и несоответствием</span><span class="sxs-lookup"><span data-stu-id="67eb0-143">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="67eb0-144">Управление качеством для складских процессов</span><span class="sxs-lookup"><span data-stu-id="67eb0-144">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
