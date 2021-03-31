---
title: Настройка налоговых кодов
description: В этом разделе описывается, как настроить налоговые коды в Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 594e8f0595ecace748a70860c1ccacaf90b7d279
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222199"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="1b264-103">Настройка налоговых кодов</span><span class="sxs-lookup"><span data-stu-id="1b264-103">Set up sales tax codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1b264-104">В этом разделе описывается, как настроить налоговые коды.</span><span class="sxs-lookup"><span data-stu-id="1b264-104">This topic explains how to set up sales tax codes.</span></span> <span data-ttu-id="1b264-105">Налоговые коды создаются для каждого косвенного налога или пошлины, которые юридическое лицо должно рассчитывать, собирать и платить налоговым органам.</span><span class="sxs-lookup"><span data-stu-id="1b264-105">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="1b264-106">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="1b264-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="1b264-107">Перейдите к **Область перехода > Налог > Косвенные налоги > Налог > Налоговые коды**.</span><span class="sxs-lookup"><span data-stu-id="1b264-107">Go to **Navigation pane > Tax > Indirect taxes > Sales tax > Sales tax codes**.</span></span>
2. <span data-ttu-id="1b264-108">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1b264-108">Select **New**.</span></span>
3. <span data-ttu-id="1b264-109">В поле **Налоговый код** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1b264-109">In the **Sales tax code** field, type a value.</span></span>
4. <span data-ttu-id="1b264-110">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1b264-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="1b264-111">Выберите **Период сопоставления**, открыв раскрывающийся список, чтобы указать, в какие налоговые органы и через какие интервалы времени следует отправлять налоговые отчеты и выплачивать налоги.</span><span class="sxs-lookup"><span data-stu-id="1b264-111">Select a **Settlement period** by opening the pull-down list to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="1b264-112">Выберите **Группу разноски ГК**, чтобы указать счета ГК для разноски налога в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="1b264-112">Select a **Ledger posting group** to specify the main accounts to post sales tax to the general ledger.</span></span>
7. <span data-ttu-id="1b264-113">Разверните экспресс-вкладку **Расчет**.</span><span class="sxs-lookup"><span data-stu-id="1b264-113">Expand the **Calculation** FastTab.</span></span> <span data-ttu-id="1b264-114">Это включает в себя несколько полей, с помощью которых можно управлять способом расчета сумм налогов.</span><span class="sxs-lookup"><span data-stu-id="1b264-114">This includes multiple fields that control how sales tax amounts will be calculated.</span></span> <span data-ttu-id="1b264-115">Заполните эти поля по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="1b264-115">Fill these fields out as needed.</span></span>  
8. <span data-ttu-id="1b264-116">На **Панели операций** в верхней части интерфейса выберите **Налоговый код**.</span><span class="sxs-lookup"><span data-stu-id="1b264-116">On the **Action Pane** at the top of the interface, select **Sales tax code**.</span></span>
9. <span data-ttu-id="1b264-117">Выберите **Значения**.</span><span class="sxs-lookup"><span data-stu-id="1b264-117">Select **Values**.</span></span>
10. <span data-ttu-id="1b264-118">Введите значение для этого налогового кода в столбце **значение**.</span><span class="sxs-lookup"><span data-stu-id="1b264-118">Enter the value for this tax code in the **value** column.</span></span>
    - <span data-ttu-id="1b264-119">На экспресс-вкладке **Расчет** в поле «Источник», если выбран параметр «Сумма на единицу», значение будет умножаться на количество в проводке для расчета суммы налога.</span><span class="sxs-lookup"><span data-stu-id="1b264-119">On the **Calculation** FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="1b264-120">Если налоговый код не основан на единице, значение выражается в процентах, которые применяются к источнику для данного налогового кода для расчета суммы налога.</span><span class="sxs-lookup"><span data-stu-id="1b264-120">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
11. <span data-ttu-id="1b264-121">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1b264-121">Select **Save**.</span></span>
12. <span data-ttu-id="1b264-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1b264-122">Close the page.</span></span>
13. <span data-ttu-id="1b264-123">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1b264-123">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]