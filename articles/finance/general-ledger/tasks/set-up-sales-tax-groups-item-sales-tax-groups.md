---
title: Настройка налоговых групп и налоговых групп номенклатур
description: В этой записи задачи представлен процесс настройки налога и налоговых групп.
author: twheeloc
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e35f98de715af95b0bec2b2ca5d7e7570aa8fdba
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994498"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="b124a-103">Настройка налоговых групп и налоговых групп номенклатур</span><span class="sxs-lookup"><span data-stu-id="b124a-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b124a-104">В этой записи задачи представлен процесс настройки налога и налоговых групп.</span><span class="sxs-lookup"><span data-stu-id="b124a-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="b124a-105">Налоговые группы — группы налоговых кодов, присоединенные к клиентам и поставщикам.</span><span class="sxs-lookup"><span data-stu-id="b124a-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="b124a-106">Они также присоединены к счетам ГК для проводок, которые не разнесены для конкретного поставщика или клиента.</span><span class="sxs-lookup"><span data-stu-id="b124a-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="b124a-107">Налоговые группы номенклатур — это группы налоговых кодов, присоединенные к ресурсам, таким как продукты.</span><span class="sxs-lookup"><span data-stu-id="b124a-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="b124a-108">Налоги, применяемые к конкретной проводке, определяются налоговыми кодами, включенными в налоговую группу и в налоговую группу номенклатур проводки.</span><span class="sxs-lookup"><span data-stu-id="b124a-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="b124a-109">Налог можно рассчитать, только если налоговая группа и налоговая группа номенклатур были выбраны для каждой проводки, для которой должен быть рассчитан или записан налог.</span><span class="sxs-lookup"><span data-stu-id="b124a-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="b124a-110">Перейдите к **Область переходов > Модули > Налог > Косвенные налоги > Налог > Налоговые группы**.</span><span class="sxs-lookup"><span data-stu-id="b124a-110">Go to **Navigation pane > Modules > Tax > Indirect taxes > Sales tax > Sales tax groups**.</span></span>
2. <span data-ttu-id="b124a-111">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="b124a-111">Click **New**.</span></span>
3. <span data-ttu-id="b124a-112">В поле **Налоговая группа** введите значение.</span><span class="sxs-lookup"><span data-stu-id="b124a-112">In the **Sales tax group** field, type a value.</span></span>
4. <span data-ttu-id="b124a-113">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="b124a-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="b124a-114">Переключите развертывание раздела **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="b124a-114">Toggle the expansion of the **Setup** section.</span></span>
6. <span data-ttu-id="b124a-115">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="b124a-115">Click **Add**.</span></span>
7. <span data-ttu-id="b124a-116">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b124a-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="b124a-117">В поле **Налоговый код** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="b124a-117">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="b124a-118">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b124a-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="b124a-119">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b124a-119">Click **Save**.</span></span>
11. <span data-ttu-id="b124a-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b124a-120">Close the page.</span></span>
12. <span data-ttu-id="b124a-121">Перейдите в раздел **Налог > Косвенные налоги > Налог > Налоговые группы номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="b124a-121">Go to **Tax > Indirect taxes > Sales tax > Item sales tax groups**.</span></span>
13. <span data-ttu-id="b124a-122">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="b124a-122">Click **New**.</span></span>
14. <span data-ttu-id="b124a-123">В поле **Налоговая группа номенклатур** введите значение.</span><span class="sxs-lookup"><span data-stu-id="b124a-123">In the **Item sales tax group** field, type a value.</span></span>
15. <span data-ttu-id="b124a-124">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="b124a-124">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="b124a-125">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="b124a-125">Click **Add**.</span></span>
17. <span data-ttu-id="b124a-126">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b124a-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="b124a-127">В поле **Налоговый код** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="b124a-127">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="b124a-128">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b124a-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="b124a-129">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b124a-129">Click **Save**.</span></span>

