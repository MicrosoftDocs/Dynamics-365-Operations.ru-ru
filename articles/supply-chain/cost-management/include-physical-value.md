---
title: Включать физическую стоимость
description: Флажок "Включать физическую стоимость" на экспресс-вкладке "Складская модель" страницы "Группы номенклатурных моделей" используется, чтобы указать, должны ли физически обновленные проводки учитываться при расчете скользящей средней себестоимости для номенклатуры.
author: AndersGirke
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6e70a40b15bf08d88958cbf3ee3e82ed63e7a48
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436017"
---
# <a name="include-physical-value"></a><span data-ttu-id="88fa6-103">Включать физическую стоимость</span><span class="sxs-lookup"><span data-stu-id="88fa6-103">Include physical value</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88fa6-104">Флажок "Включать физическую стоимость" на экспресс-вкладке "Складская модель" страницы "Группы номенклатурных моделей" используется, чтобы указать, должны ли физически обновленные проводки учитываться при расчете скользящей средней себестоимости для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="88fa6-104">You use the Include physical value check box on the Inventory model FastTab of the Item model groups page to specify whether physically updated transactions are considered when the running average cost price is calculated for an item.</span></span>

<span data-ttu-id="88fa6-105">Флажок **Включать физическую стоимость** имеет следующие значения.</span><span class="sxs-lookup"><span data-stu-id="88fa6-105">The **Include physical value** check box has the following values.</span></span>

| <span data-ttu-id="88fa6-106">Значение</span><span class="sxs-lookup"><span data-stu-id="88fa6-106">Value</span></span>    | <span data-ttu-id="88fa6-107">Результат</span><span class="sxs-lookup"><span data-stu-id="88fa6-107">Result</span></span>                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88fa6-108">Выбрано</span><span class="sxs-lookup"><span data-stu-id="88fa6-108">Selected</span></span> | <span data-ttu-id="88fa6-109">Для расчета скользящей средней себестоимости используются физически обновленные проводки, и финансово обновленные проводки.</span><span class="sxs-lookup"><span data-stu-id="88fa6-109">Both physically updated transactions and financially updated transactions are used to calculate the running average cost price.</span></span> |
| <span data-ttu-id="88fa6-110">Очищено</span><span class="sxs-lookup"><span data-stu-id="88fa6-110">Cleared</span></span>  | <span data-ttu-id="88fa6-111">Для расчета скользящей средней себестоимости используются только финансово обновленные проводки.</span><span class="sxs-lookup"><span data-stu-id="88fa6-111">Only financially updated transactions are used to calculate the running average cost price.</span></span>                                     |

<span data-ttu-id="88fa6-112">Флажок дает немного разные результаты в зависимости от используемой складской модели.</span><span class="sxs-lookup"><span data-stu-id="88fa6-112">The check box has slightly different effects, depending on the inventory model that you use.</span></span>

-   <span data-ttu-id="88fa6-113">При установке флажка **Включать физическую стоимость** при использовании складских моделей ФИФО (первым пришел, первым ушел), ЛИФО (последним пришел, первым ушел) или ЛИФО на дату, закрытие запасов приводит также к корректировке физически обновленных проводок.</span><span class="sxs-lookup"><span data-stu-id="88fa6-113">If you select the **Include physical value** check box when you use the FIFO (First in, first out), LIFO (Last in, first out), or LIFO date inventory model, inventory close also makes adjustments to physically updated transactions.</span></span>
-   <span data-ttu-id="88fa6-114">Если флажок **Включать физическую стоимость** при использовании данных моделей не установлен, закрытие запасов приводит к сопоставлению только с финансово обновленными проводками.</span><span class="sxs-lookup"><span data-stu-id="88fa6-114">If you don't select the **Include physical value** check box when you use these inventory models, inventory close makes settlements only to financially updated transactions.</span></span>
-   <span data-ttu-id="88fa6-115">При использовании складских моделей взвешенного среднего или взвешенного среднего по дате закрытие запасов приводит к сопоставлению только финансово обновленных проводок, вне зависимости от того, установлен ли флажок **Включать физическую стоимость**.</span><span class="sxs-lookup"><span data-stu-id="88fa6-115">When you use the weighted average or weighted average date inventory model, inventory close settles only financially updated transactions, regardless of whether you select the **Include physical value** check box.</span></span>

<span data-ttu-id="88fa6-116">**Пример 1.** Установлен флажок **Включать физическую стоимость** и получены следующие заказы на покупку:</span><span class="sxs-lookup"><span data-stu-id="88fa6-116">**Example 1** You've selected the **Include physical value** check box and receive the following purchase orders:</span></span>

-   <span data-ttu-id="88fa6-117">Заказ на покупку в количестве 2 шт. и себестоимостью USD 10,00, который был обновлен отборочной накладной.</span><span class="sxs-lookup"><span data-stu-id="88fa6-117">A purchase order for a quantity of 2 and a cost price of USD 10.00 that has been packing slip–updated.</span></span>
-   <span data-ttu-id="88fa6-118">Заказ на покупку в количестве 3 шт. и себестоимостью USD 12,00, который был обновлен накладной.</span><span class="sxs-lookup"><span data-stu-id="88fa6-118">A purchase order for a quantity of 3 and a cost price of USD 12.00 that has been invoice-updated.</span></span>

<span data-ttu-id="88fa6-119">В этом случае скользящее среднее значение себестоимости будет равно 11,20 USD = (2x10+3x12)/(2+3), поскольку для расчета себестоимости используются и физически обновленные проводки, и финансово обновленные проводки.</span><span class="sxs-lookup"><span data-stu-id="88fa6-119">In this case, the running average cost price will be USD 11.20 = (2x10+3x12)/(2+3), because both physically updated transactions and financially updated transactions are used to calculate the cost price.</span></span> 

<span data-ttu-id="88fa6-120">**Пример 2.** Флажок **Включать физическую стоимость** не установлен, и себестоимость в настройке номенклатуры составляет 10,00 USD.</span><span class="sxs-lookup"><span data-stu-id="88fa6-120">**Example 2** You haven't selected the **Include physical value** check box, and the cost price on the item setup is USD 10.00.</span></span> 

-   <span data-ttu-id="88fa6-121">Вы получили заказ на покупку в количестве 20 шт. с себестоимостью USD 12,00, который был обновлен отборочной накладной.</span><span class="sxs-lookup"><span data-stu-id="88fa6-121">You receive a purchase order for a quantity of 20 and a cost price of USD 12.00 that has been packing slip–updated.</span></span>

<span data-ttu-id="88fa6-122">При разноске заказа на продажу разнесенная сумма затрат составит 10,00 USD, поскольку скользящая средняя себестоимость не будет включать физически разнесенные проводки.</span><span class="sxs-lookup"><span data-stu-id="88fa6-122">When a sales order is posted, the posted cost amount is USD 10.00, because the running average cost price won't include physically posted transactions.</span></span> 

> [!NOTE]
> <span data-ttu-id="88fa6-123">Для сравнения: если установить флажок **Включать физическую стоимость** для данной номенклатуры, при разноске заказа на продажу разнесенная сумма затрат будет USD 12,00.</span><span class="sxs-lookup"><span data-stu-id="88fa6-123">For comparison, if you select the **Include physical value** check box for this item, when a sales order is posted, the posted cost amount will be USD 12.00.</span></span>
