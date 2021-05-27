---
title: Накладные расходы на операции несоответствия
description: В этой теме описывается, как создавать накладные расходы контроля качества, которые могут использоваться с операциями для несоответствия.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 382890232bff47a885840af1eb7e91d27bb46cae
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022308"
---
# <a name="charges-for-nonconformance-operations"></a><span data-ttu-id="ba6a1-103">Накладные расходы на операции несоответствия</span><span class="sxs-lookup"><span data-stu-id="ba6a1-103">Charges for nonconformance operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba6a1-104">В этой теме описывается, как создавать накладные расходы контроля качества, которые могут использоваться с операциями для несоответствия.</span><span class="sxs-lookup"><span data-stu-id="ba6a1-104">This topic describes how to create quality charges that can be used with operations for a nonconformance.</span></span>

<span data-ttu-id="ba6a1-105">Используйте страницу **Расходы по контролю качества**, чтобы определить типы расходов, которые могут быть добавлены для операций, связанных с несоответствиями.</span><span class="sxs-lookup"><span data-stu-id="ba6a1-105">You use the **Quality charges** page to define the types of charges that can be added to operations for a nonconformance.</span></span> <span data-ttu-id="ba6a1-106">Эти расходы позволяют отслеживать сведения о сборах и накладных расходах, которые вы захотите получить у клиента для несоответствующих продуктов, или о том, что поставщик должен компенсировать га несоответствующие полученные продукты.</span><span class="sxs-lookup"><span data-stu-id="ba6a1-106">Charges let you track details about fees or charges that you owe to a customer for nonconforming products, or that a vendor owes to you for nonconforming products that you received.</span></span> <span data-ttu-id="ba6a1-107">Можно также использовать накладные расходы для отслеживания затрат, которые необходимы для выполнения операции внешними поставщиками или услугами.</span><span class="sxs-lookup"><span data-stu-id="ba6a1-107">You might also use charges to track costs that are required for external vendors or services to perform an operation.</span></span>

## <a name="examples-of-quality-charges"></a><span data-ttu-id="ba6a1-108">Примеры расходов по контролю качества</span><span class="sxs-lookup"><span data-stu-id="ba6a1-108">Examples of quality charges</span></span>

<span data-ttu-id="ba6a1-109">Вы работаете в производственной компании.</span><span class="sxs-lookup"><span data-stu-id="ba6a1-109">You work for a manufacturing company.</span></span> <span data-ttu-id="ba6a1-110">Ваша компания имеет контракты с несколькими поставщиками.</span><span class="sxs-lookup"><span data-stu-id="ba6a1-110">Your company has contracts with several vendors.</span></span> <span data-ttu-id="ba6a1-111">Эти контракты описывают стандарты для отгрузки по времени, ущерба и качества продукта для номенклатур.</span><span class="sxs-lookup"><span data-stu-id="ba6a1-111">Those contracts outline standards for on-time shipment, damages, and product quality for items.</span></span> <span data-ttu-id="ba6a1-112">Аналогично, у нескольких клиентов имеются соглашения с компанией о возврате, убытках и качестве продукта.</span><span class="sxs-lookup"><span data-stu-id="ba6a1-112">Likewise, several of your customers have agreements with your company about returns, damages, and product quality.</span></span>

<span data-ttu-id="ba6a1-113">Структура сборов определяется для каждой ситуации и указывается в контракте.</span><span class="sxs-lookup"><span data-stu-id="ba6a1-113">A fee structure is defined for each circumstance and specified in the contract.</span></span> <span data-ttu-id="ba6a1-114">Можно настроить расходы по контролю качества для расчета различных типов накладных расходов, таких как *Повреждения*, *Поздняя отгрузка* и *Качество*.</span><span class="sxs-lookup"><span data-stu-id="ba6a1-114">You can configure quality charges to outline the various types of charges, such as *Damages*, *Late shipment*, and *Quality*.</span></span> <span data-ttu-id="ba6a1-115">Затем при создании несоответствия добавляется одна или несколько операций.</span><span class="sxs-lookup"><span data-stu-id="ba6a1-115">Then, when you create a nonconformance, you add one or more operations.</span></span> <span data-ttu-id="ba6a1-116">Для каждой операции выбираются **Накладные расходы** для определения сведений о сборах.</span><span class="sxs-lookup"><span data-stu-id="ba6a1-116">For each operation, you select **Charges** to define the details about the fees.</span></span>

## <a name="create-a-quality-charge"></a><span data-ttu-id="ba6a1-117">Создание расходов по контролю качества</span><span class="sxs-lookup"><span data-stu-id="ba6a1-117">Create a quality charge</span></span>

1. <span data-ttu-id="ba6a1-118">Перейдите в раздел **Управление запасами \> Настройка \> Управление качеством \> Расходы по контролю качества**.</span><span class="sxs-lookup"><span data-stu-id="ba6a1-118">Go to **Inventory management \> Setup \> Quality management \> Quality charges**.</span></span>
1. <span data-ttu-id="ba6a1-119">На панели операций выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="ba6a1-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="ba6a1-120">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="ba6a1-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="ba6a1-121">**Код накладных расходов** — введите уникальный код или имя для накладного расхода.</span><span class="sxs-lookup"><span data-stu-id="ba6a1-121">**Charges code** – Enter a unique ID or name for the quality charge.</span></span>
    - <span data-ttu-id="ba6a1-122">**Описание** — введите подробное описание расходов по контролю качества.</span><span class="sxs-lookup"><span data-stu-id="ba6a1-122">**Description** – Enter a detailed description of the quality charge.</span></span>

1. <span data-ttu-id="ba6a1-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ba6a1-123">Close the page.</span></span>

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a><span data-ttu-id="ba6a1-124">Добавление расходов по контролю качества в операцию для несоответствия</span><span class="sxs-lookup"><span data-stu-id="ba6a1-124">Add a quality charge to an operation for a nonconformance</span></span>

<span data-ttu-id="ba6a1-125">Дополнительные сведения о добавлении операций для несоответствия и применении к ним накладных расходов см. в разделе [Операции для несоответствий](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="ba6a1-125">For details about how to add operations to a nonconformance and apply charges to them, see [Operations for nonconformances](quality-operations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ba6a1-126">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ba6a1-126">Additional resources</span></span>

- [<span data-ttu-id="ba6a1-127">Обзор управления качеством</span><span class="sxs-lookup"><span data-stu-id="ba6a1-127">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="ba6a1-128">Включение управления качеством и несоответствием</span><span class="sxs-lookup"><span data-stu-id="ba6a1-128">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="ba6a1-129">Работники, ответственные за утверждение несоответствий</span><span class="sxs-lookup"><span data-stu-id="ba6a1-129">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="ba6a1-130">Карантинные зоны для несоответствий</span><span class="sxs-lookup"><span data-stu-id="ba6a1-130">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="ba6a1-131">Типы диагностики для несоответствий</span><span class="sxs-lookup"><span data-stu-id="ba6a1-131">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="ba6a1-132">Расходы по контролю качества для несоответствий</span><span class="sxs-lookup"><span data-stu-id="ba6a1-132">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="ba6a1-133">Операции для несоответствий</span><span class="sxs-lookup"><span data-stu-id="ba6a1-133">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="ba6a1-134">Управление качеством для складских процессов</span><span class="sxs-lookup"><span data-stu-id="ba6a1-134">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
