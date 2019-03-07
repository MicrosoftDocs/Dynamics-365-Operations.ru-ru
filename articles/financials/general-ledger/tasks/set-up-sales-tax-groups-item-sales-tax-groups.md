---
title: Настройка налоговых групп и налоговых групп номенклатур
description: В этой записи задачи представлен процесс настройки налога и налоговых групп.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec5bbe37aa06f18172c417e903538cadc8a6f312
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "320060"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="bb8ab-103">Настройка налоговых групп и налоговых групп номенклатур</span><span class="sxs-lookup"><span data-stu-id="bb8ab-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bb8ab-104">В этой записи задачи представлен процесс настройки налога и налоговых групп.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="bb8ab-105">Налоговые группы — группы налоговых кодов, присоединенные к клиентам и поставщикам.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="bb8ab-106">Они также присоединены к счетам ГК для проводок, которые не разнесены для конкретного поставщика или клиента.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="bb8ab-107">Налоговые группы номенклатур — это группы налоговых кодов, присоединенные к ресурсам, таким как продукты.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="bb8ab-108">Налоги, применяемые к конкретной проводке, определяются налоговыми кодами, включенными в налоговую группу и в налоговую группу номенклатур проводки.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="bb8ab-109">Налог можно рассчитать, только если налоговая группа и налоговая группа номенклатур были выбраны для каждой проводки, для которой должен быть рассчитан или записан налог.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="bb8ab-110">Перейдите в раздел "Налог" > "Косвенные налоги" > "Налог" > "Налоговые группы".</span><span class="sxs-lookup"><span data-stu-id="bb8ab-110">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="bb8ab-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bb8ab-111">Click New.</span></span>
3. <span data-ttu-id="bb8ab-112">В поле "Налоговая группа" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-112">In the Sales tax group field, type a value.</span></span>
4. <span data-ttu-id="bb8ab-113">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bb8ab-114">Переключите развертывание раздела "Настройка".</span><span class="sxs-lookup"><span data-stu-id="bb8ab-114">Toggle the expansion of the Setup section.</span></span>
6. <span data-ttu-id="bb8ab-115">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-115">Click Add.</span></span>
7. <span data-ttu-id="bb8ab-116">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="bb8ab-117">В поле "Налоговый код" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-117">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="bb8ab-118">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="bb8ab-119">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="bb8ab-119">Click Save.</span></span>
11. <span data-ttu-id="bb8ab-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-120">Close the page.</span></span>
12. <span data-ttu-id="bb8ab-121">Перейдите в раздел "Налог" > "Косвенные налоги" > "Налог" > "Налоговые группы номенклатур".</span><span class="sxs-lookup"><span data-stu-id="bb8ab-121">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
13. <span data-ttu-id="bb8ab-122">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bb8ab-122">Click New.</span></span>
14. <span data-ttu-id="bb8ab-123">В поле "Налоговая группа номенклатур" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-123">In the Item sales tax group field, type a value.</span></span>
15. <span data-ttu-id="bb8ab-124">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-124">In the Description field, type a value.</span></span>
16. <span data-ttu-id="bb8ab-125">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-125">Click Add.</span></span>
17. <span data-ttu-id="bb8ab-126">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="bb8ab-127">В поле "Налоговый код" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-127">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="bb8ab-128">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="bb8ab-129">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="bb8ab-129">Click Save.</span></span>

