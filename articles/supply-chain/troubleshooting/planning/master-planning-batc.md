---
title: Вы не можете фильтровать номенклатуры сводного планирования по их связанным значениям групп покрытия
description: Вы не можете фильтровать номенклатуры сводного планирования по их связанным значениям групп покрытия.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049487"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a><span data-ttu-id="f233f-103">Вы не можете фильтровать номенклатуры сводного планирования по их связанным значениям групп покрытия</span><span class="sxs-lookup"><span data-stu-id="f233f-103">You can't filter master planning items by their related coverage group values</span></span>

<span data-ttu-id="f233f-104">Номер статьи базы знаний: 4612572</span><span class="sxs-lookup"><span data-stu-id="f233f-104">KB number: 4612572</span></span>

## <a name="symptoms"></a><span data-ttu-id="f233f-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="f233f-105">Symptoms</span></span>

<span data-ttu-id="f233f-106">Необходимо отфильтровать номенклатуры, которые будут включены в пакетное задание сводного планирования, на основе значений соответствующих записей из таблицы покрытия номенклатур.</span><span class="sxs-lookup"><span data-stu-id="f233f-106">You want to filter the items that will be included in a master planning batch job, based on the values of related records from the item coverage table.</span></span> <span data-ttu-id="f233f-107">(Например, требуется отфильтровать номенклатуры по их значению **Поставщик** и/или **Группа покрытия**.)</span><span class="sxs-lookup"><span data-stu-id="f233f-107">(For example, you want to filter items by their **Vendor** and/or **Coverage group** value).</span></span> <span data-ttu-id="f233f-108">Настройка фильтра для пакетного задания позволяет создать соединение из таблицы **Номенклатуры** в таблицу **Покрытие номенклатур**, а затем указать значения полей из таблицы покрытия номенклатур в запросе.</span><span class="sxs-lookup"><span data-stu-id="f233f-108">The filter setup for the batch job lets you create a join from the **Items** table to the **Item coverage** table, and then specify field values from the item coverage table in your query.</span></span> <span data-ttu-id="f233f-109">Однако после завершения этой настройки система все равно создает спланированные заказы для всего покрытия номенклатур, а не только для номенклатур, соответствующих указанным значениям полей в таблице покрытия номенклатур.</span><span class="sxs-lookup"><span data-stu-id="f233f-109">However, after you complete this setup, the system still creates planned orders for the whole item coverage, not just for the items that match the specified field values from the item coverage table.</span></span>

## <a name="resolution"></a><span data-ttu-id="f233f-110">Решение</span><span class="sxs-lookup"><span data-stu-id="f233f-110">Resolution</span></span>

<span data-ttu-id="f233f-111">Фильтр пакетного задания может выполнять фильтрацию только по номенклатурам.</span><span class="sxs-lookup"><span data-stu-id="f233f-111">The batch job filter can filter only on items.</span></span> <span data-ttu-id="f233f-112">Хотя можно добавить соединение в таблицу **Покрытие номенклатур**, настройки фильтра, сделанные для этой таблицы, не будут влиять на результаты запроса.</span><span class="sxs-lookup"><span data-stu-id="f233f-112">Although you can add a join to the **Item coverage** table, filter settings that you make against that table won't affect the query output.</span></span> <span data-ttu-id="f233f-113">Во время выполнения система выполняет планирование для всех групп покрытия и всех вариаций, которые имеют отфильтрованные номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="f233f-113">At runtime, the system runs planning for all the coverage groups and all the variations that the filtered items have.</span></span> <span data-ttu-id="f233f-114">После того как номенклатура уже включена в выполнение, любые группы покрытия, включенные в фильтр номенклатуры, не будут влиять на результаты планирования.</span><span class="sxs-lookup"><span data-stu-id="f233f-114">After an item is already included in the run, any coverage groups that are included in the item filter a won't affect the planning output.</span></span>
