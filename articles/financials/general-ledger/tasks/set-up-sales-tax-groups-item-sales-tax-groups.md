--- 
title: "Настройка налоговых групп и налоговых групп номенклатур"
description: "В этой записи задачи представлен процесс настройки налога и налоговых групп."
author: twheeloc
manager: AnnBe
ms.date: 11/10/2015
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4d7f1093edcfff65fd466fa8138b1bb5203648b3
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="c43a8-103">Настройка налоговых групп и налоговых групп номенклатур</span><span class="sxs-lookup"><span data-stu-id="c43a8-103">Set up sales tax groups and item sales tax groups</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c43a8-104">В этой записи задачи представлен процесс настройки налога и налоговых групп.</span><span class="sxs-lookup"><span data-stu-id="c43a8-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="c43a8-105">Налоговые группы — группы налоговых кодов, присоединенные к клиентам и поставщикам.</span><span class="sxs-lookup"><span data-stu-id="c43a8-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="c43a8-106">Они также присоединены к счетам ГК для проводок, которые не разнесены для конкретного поставщика или клиента.</span><span class="sxs-lookup"><span data-stu-id="c43a8-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="c43a8-107">Налоговые группы номенклатур — это группы налоговых кодов, присоединенные к ресурсам, таким как продукты.</span><span class="sxs-lookup"><span data-stu-id="c43a8-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="c43a8-108">Налоги, применяемые к конкретной проводке, определяются налоговыми кодами, включенными в налоговую группу и в налоговую группу номенклатур проводки.</span><span class="sxs-lookup"><span data-stu-id="c43a8-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="c43a8-109">Налог можно рассчитать, только если налоговая группа и налоговая группа номенклатур были выбраны для каждой проводки, для которой должен быть рассчитан или записан налог.</span><span class="sxs-lookup"><span data-stu-id="c43a8-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="c43a8-110">Перейдите в раздел "Налог" > "Косвенные налоги" > "Налог" > "Налоговые группы".</span><span class="sxs-lookup"><span data-stu-id="c43a8-110">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="c43a8-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="c43a8-111">Click New.</span></span>
3. <span data-ttu-id="c43a8-112">В поле "Налоговая группа" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c43a8-112">In the Sales tax group field, type a value.</span></span>
4. <span data-ttu-id="c43a8-113">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c43a8-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c43a8-114">Переключите развертывание раздела "Настройка".</span><span class="sxs-lookup"><span data-stu-id="c43a8-114">Toggle the expansion of the Setup section.</span></span>
6. <span data-ttu-id="c43a8-115">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="c43a8-115">Click Add.</span></span>
7. <span data-ttu-id="c43a8-116">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="c43a8-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="c43a8-117">В поле "Налоговый код" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c43a8-117">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="c43a8-118">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c43a8-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="c43a8-119">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="c43a8-119">Click Save.</span></span>
11. <span data-ttu-id="c43a8-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c43a8-120">Close the page.</span></span>
12. <span data-ttu-id="c43a8-121">Перейдите в раздел "Налог" > "Косвенные налоги" > "Налог" > "Налоговые группы номенклатур".</span><span class="sxs-lookup"><span data-stu-id="c43a8-121">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
13. <span data-ttu-id="c43a8-122">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="c43a8-122">Click New.</span></span>
14. <span data-ttu-id="c43a8-123">В поле "Налоговая группа номенклатур" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c43a8-123">In the Item sales tax group field, type a value.</span></span>
15. <span data-ttu-id="c43a8-124">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c43a8-124">In the Description field, type a value.</span></span>
16. <span data-ttu-id="c43a8-125">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="c43a8-125">Click Add.</span></span>
17. <span data-ttu-id="c43a8-126">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="c43a8-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="c43a8-127">В поле "Налоговый код" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="c43a8-127">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="c43a8-128">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c43a8-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="c43a8-129">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="c43a8-129">Click Save.</span></span>


