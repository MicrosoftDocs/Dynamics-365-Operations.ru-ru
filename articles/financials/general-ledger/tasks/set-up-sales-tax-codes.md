--- 
title: "Настройка кодов налогов"
description: "Налоговые коды создаются для каждого косвенного налога или пошлины, которые юридическое лицо должно рассчитывать, собирать и платить налоговым органам."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 968f4bb9f7d54cdb4de4f7842ed1777c9a9acd64
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="e7610-103">Настройка кодов налогов</span><span class="sxs-lookup"><span data-stu-id="e7610-103">Set up sales tax codes</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e7610-104">Налоговые коды создаются для каждого косвенного налога или пошлины, которые юридическое лицо должно рассчитывать, собирать и платить налоговым органам.</span><span class="sxs-lookup"><span data-stu-id="e7610-104">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="e7610-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="e7610-105">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="e7610-106">Перейдите в раздел "Налог" > "Косвенные налоги" > "Налог" > "Налоговые коды".</span><span class="sxs-lookup"><span data-stu-id="e7610-106">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="e7610-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="e7610-107">Click New.</span></span>
3. <span data-ttu-id="e7610-108">В поле "Налоговый код" введите значение.</span><span class="sxs-lookup"><span data-stu-id="e7610-108">In the Sales tax code field, type a value.</span></span>
4. <span data-ttu-id="e7610-109">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="e7610-109">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e7610-110">Выберите период сопоставления, чтобы указать, в какие налоговые органы и через какие интервалы времени следует отправлять налоговые отчеты и выплачивать налоги.</span><span class="sxs-lookup"><span data-stu-id="e7610-110">Select a Settlement period to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="e7610-111">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="e7610-111">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e7610-112">Выберите группу разноски ГК, чтобы указать счета ГК для разноски налога в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="e7610-112">Select a Ledger posting group to specify the main accounts to post sales tax to the general ledger.</span></span>
8. <span data-ttu-id="e7610-113">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="e7610-113">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="e7610-114">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="e7610-114">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="e7610-115">Разверните экспресс-вкладку "Расчет".</span><span class="sxs-lookup"><span data-stu-id="e7610-115">Expand the Calculation FastTab.</span></span>
    * <span data-ttu-id="e7610-116">На экспресс-вкладке "Расчет" имеется несколько полей, с помощью которых можно управлять способом расчета сумм налогов.</span><span class="sxs-lookup"><span data-stu-id="e7610-116">The Calculation FastTab has multiple fields that control how sales tax amounts will be calculated.</span></span>  
11. <span data-ttu-id="e7610-117">В области действий щелкните "Налоговый код".</span><span class="sxs-lookup"><span data-stu-id="e7610-117">On the Action Pane, click Sales tax code.</span></span>
12. <span data-ttu-id="e7610-118">Щелкните "Значение".</span><span class="sxs-lookup"><span data-stu-id="e7610-118">Click Values.</span></span>
13. <span data-ttu-id="e7610-119">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="e7610-119">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="e7610-120">Введите значение для данного налогового кода.</span><span class="sxs-lookup"><span data-stu-id="e7610-120">Enter the value for this tax code.</span></span>
    * <span data-ttu-id="e7610-121">На экспресс-вкладке "Расчет" в поле "Источник", если выбран параметр "Сумма на единицу", значение будет умножаться на количество в проводке для расчета суммы налога.</span><span class="sxs-lookup"><span data-stu-id="e7610-121">On the Calculation FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="e7610-122">Если налоговый код не основан на единице, значение выражается в процентах, которые применяются к источнику для данного налогового кода для расчета суммы налога.</span><span class="sxs-lookup"><span data-stu-id="e7610-122">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
15. <span data-ttu-id="e7610-123">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="e7610-123">Click Save.</span></span>
16. <span data-ttu-id="e7610-124">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e7610-124">Close the page.</span></span>
17. <span data-ttu-id="e7610-125">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="e7610-125">Click Save.</span></span>

