---
title: Типы диагностики для несоответствий
description: В этом разделе описывается, как использовать и создавать типы диагностики, которые могут использоваться с несоответствиями.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7a5c593f1d9e8f7a77f693f6e652e9355a985fb
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022284"
---
# <a name="diagnostic-types-for-nonconformances"></a><span data-ttu-id="f85a8-103">Типы диагностики для несоответствий</span><span class="sxs-lookup"><span data-stu-id="f85a8-103">Diagnostic types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f85a8-104">В этом разделе описывается, как использовать и создавать типы диагностики, которые могут использоваться с несоответствиями.</span><span class="sxs-lookup"><span data-stu-id="f85a8-104">This topic describes how to use and create diagnostic types that can be used with nonconformances.</span></span>

<span data-ttu-id="f85a8-105">Используйте страницу **Типы диагностики**, чтобы определить классификацию диагностических действий.</span><span class="sxs-lookup"><span data-stu-id="f85a8-105">You use the **Diagnostic types** page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="f85a8-106">Затем при создании исправления для несоответствия выберите диагностику.</span><span class="sxs-lookup"><span data-stu-id="f85a8-106">Then, when you create a correction for a nonconformance, you select a diagnostic.</span></span> <span data-ttu-id="f85a8-107">Коррекция определяет, какой тип диагностического действия должен быть принят для утвержденного несоответствия, и кто должно выполнить это действие.</span><span class="sxs-lookup"><span data-stu-id="f85a8-107">A correction specifies what type of diagnostic action should be taken for an approved nonconformance, and who should take that action.</span></span> <span data-ttu-id="f85a8-108">Она также определяет запрошенную дату завершения и запланированную дату завершения.</span><span class="sxs-lookup"><span data-stu-id="f85a8-108">It also specifies the requested completion date and the planned completion date.</span></span>

## <a name="examples-of-diagnostic-types"></a><span data-ttu-id="f85a8-109">Примеры типов диагностики</span><span class="sxs-lookup"><span data-stu-id="f85a8-109">Examples of diagnostic types</span></span>

<span data-ttu-id="f85a8-110">Вы работаете для производственной компании, и несколько номенклатур имеют не прошли проверку качества.</span><span class="sxs-lookup"><span data-stu-id="f85a8-110">You work for a manufacturing company, and several items have failed quality tests.</span></span> <span data-ttu-id="f85a8-111">Эти номенклатуры перемещаются в карантинную область и помечаются как несоответствующие продукты.</span><span class="sxs-lookup"><span data-stu-id="f85a8-111">Those items are moved into a quarantine area and marked as nonconforming products.</span></span> <span data-ttu-id="f85a8-112">Запись несоответствия создается в Microsoft Dynamics 365 Supply Chain Management для отслеживания сведений через разрешение проблемы.</span><span class="sxs-lookup"><span data-stu-id="f85a8-112">A nonconformance record is created in Microsoft Dynamics 365 Supply Chain Management to track the details through issue resolution.</span></span>

<span data-ttu-id="f85a8-113">В этом случае проблемы качества происходят из-за того, что подшипники на машине, на которой упакованы номенклатуры, неисправны и перегреваются.</span><span class="sxs-lookup"><span data-stu-id="f85a8-113">In this case, the quality issues are occurring because bearings in the machine that packages the items have gone bad and are overheating.</span></span> <span data-ttu-id="f85a8-114">Исправление этой проблемы заключается в замене деталей в машине.</span><span class="sxs-lookup"><span data-stu-id="f85a8-114">The correction for this problem is to replace the parts in the machine.</span></span>

<span data-ttu-id="f85a8-115">При настройке типов диагностики можно создать несколько записей, каждая из которых представляет собой различные типы проблем, которые могут быть в машине.</span><span class="sxs-lookup"><span data-stu-id="f85a8-115">When you configure the diagnostic types, you can create multiple records, each of which represents a different type of problem that the machine might have.</span></span> <span data-ttu-id="f85a8-116">В качестве альтернативы можно создать один универсальный тип диагностики, который представляет ремонт машины.</span><span class="sxs-lookup"><span data-stu-id="f85a8-116">Alternatively, you can create one generic diagnostic type that represents machine repair.</span></span>

## <a name="create-a-diagnostic-type"></a><span data-ttu-id="f85a8-117">Создание типа диагностики</span><span class="sxs-lookup"><span data-stu-id="f85a8-117">Create a diagnostic type</span></span>

1. <span data-ttu-id="f85a8-118">Перейдите в раздел **Управление запасами \> Настройка \> Управление качеством \> Типы диагностики**.</span><span class="sxs-lookup"><span data-stu-id="f85a8-118">Go to **Inventory management \> Setup \> Quality management \> Diagnostic types**.</span></span>
1. <span data-ttu-id="f85a8-119">На панели операций выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="f85a8-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="f85a8-120">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="f85a8-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="f85a8-121">**Диагностика** — введите уникальный идентификатора или имя типа диагностики.</span><span class="sxs-lookup"><span data-stu-id="f85a8-121">**Diagnostic** – Enter a unique ID or name for the diagnostic type.</span></span>
    - <span data-ttu-id="f85a8-122">**Описание** — введите подробное описание типа диагностики.</span><span class="sxs-lookup"><span data-stu-id="f85a8-122">**Description** – Enter a detailed description of the diagnostic type.</span></span>

1. <span data-ttu-id="f85a8-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f85a8-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f85a8-124">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f85a8-124">Additional resources</span></span>

- [<span data-ttu-id="f85a8-125">Обзор управления качеством</span><span class="sxs-lookup"><span data-stu-id="f85a8-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="f85a8-126">Включение управления качеством и несоответствием</span><span class="sxs-lookup"><span data-stu-id="f85a8-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="f85a8-127">Работники, ответственные за утверждение несоответствий</span><span class="sxs-lookup"><span data-stu-id="f85a8-127">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="f85a8-128">Карантинные зоны для несоответствий</span><span class="sxs-lookup"><span data-stu-id="f85a8-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="f85a8-129">Типы проблем для несоответствий</span><span class="sxs-lookup"><span data-stu-id="f85a8-129">Problem types for nonconformances</span></span>](quality-problem-types.md)
- [<span data-ttu-id="f85a8-130">Расходы по контролю качества для несоответствий</span><span class="sxs-lookup"><span data-stu-id="f85a8-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="f85a8-131">Операции для несоответствий</span><span class="sxs-lookup"><span data-stu-id="f85a8-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="f85a8-132">Управление качеством для складских процессов</span><span class="sxs-lookup"><span data-stu-id="f85a8-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
