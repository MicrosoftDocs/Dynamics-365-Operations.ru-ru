--- 
title: "Настройка налоговых групп и налоговых групп номенклатур"
description: "В этой записи задачи представлен процесс настройки налога и налоговых групп."
author: twheeloc
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 70805fd7def60f85a96c0957f8a35abd6b56588c
ms.contentlocale: ru-ru
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="417a4-103">Настройка налоговых групп и налоговых групп номенклатур</span><span class="sxs-lookup"><span data-stu-id="417a4-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="417a4-104">В этой записи задачи представлен процесс настройки налога и налоговых групп.</span><span class="sxs-lookup"><span data-stu-id="417a4-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="417a4-105">Налоговые группы — группы налоговых кодов, присоединенные к клиентам и поставщикам.</span><span class="sxs-lookup"><span data-stu-id="417a4-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="417a4-106">Они также присоединены к счетам ГК для проводок, которые не разнесены для конкретного поставщика или клиента.</span><span class="sxs-lookup"><span data-stu-id="417a4-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="417a4-107">Налоговые группы номенклатур — это группы налоговых кодов, присоединенные к ресурсам, таким как продукты.</span><span class="sxs-lookup"><span data-stu-id="417a4-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="417a4-108">Налоги, применяемые к конкретной проводке, определяются налоговыми кодами, включенными в налоговую группу и в налоговую группу номенклатур проводки.</span><span class="sxs-lookup"><span data-stu-id="417a4-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="417a4-109">Налог можно рассчитать, только если налоговая группа и налоговая группа номенклатур были выбраны для каждой проводки, для которой должен быть рассчитан или записан налог.</span><span class="sxs-lookup"><span data-stu-id="417a4-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="417a4-110">Перейдите в раздел "Налог" > "Косвенные налоги" > "Налог" > "Налоговые группы".</span><span class="sxs-lookup"><span data-stu-id="417a4-110">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="417a4-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="417a4-111">Click New.</span></span>
3. <span data-ttu-id="417a4-112">В поле "Налоговая группа" введите значение.</span><span class="sxs-lookup"><span data-stu-id="417a4-112">In the Sales tax group field, type a value.</span></span>
4. <span data-ttu-id="417a4-113">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="417a4-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="417a4-114">Переключите развертывание раздела "Настройка".</span><span class="sxs-lookup"><span data-stu-id="417a4-114">Toggle the expansion of the Setup section.</span></span>
6. <span data-ttu-id="417a4-115">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="417a4-115">Click Add.</span></span>
7. <span data-ttu-id="417a4-116">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="417a4-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="417a4-117">В поле "Налоговый код" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="417a4-117">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="417a4-118">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="417a4-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="417a4-119">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="417a4-119">Click Save.</span></span>
11. <span data-ttu-id="417a4-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="417a4-120">Close the page.</span></span>
12. <span data-ttu-id="417a4-121">Перейдите в раздел "Налог" > "Косвенные налоги" > "Налог" > "Налоговые группы номенклатур".</span><span class="sxs-lookup"><span data-stu-id="417a4-121">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
13. <span data-ttu-id="417a4-122">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="417a4-122">Click New.</span></span>
14. <span data-ttu-id="417a4-123">В поле "Налоговая группа номенклатур" введите значение.</span><span class="sxs-lookup"><span data-stu-id="417a4-123">In the Item sales tax group field, type a value.</span></span>
15. <span data-ttu-id="417a4-124">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="417a4-124">In the Description field, type a value.</span></span>
16. <span data-ttu-id="417a4-125">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="417a4-125">Click Add.</span></span>
17. <span data-ttu-id="417a4-126">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="417a4-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="417a4-127">В поле "Налоговый код" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="417a4-127">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="417a4-128">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="417a4-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="417a4-129">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="417a4-129">Click Save.</span></span>


