---
title: Создание группы аренды
description: В этом разделе описывается, как настроить группы аренды. Группы аренды необходимы для создания новых аренд.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f8512a59d0e9935090f97a0f0237bfefc8473955
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4447401"
---
# <a name="create-a-lease-group"></a><span data-ttu-id="a9904-104">Создание группы аренды</span><span class="sxs-lookup"><span data-stu-id="a9904-104">Create a lease group</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9904-105">В этом разделе описывается, как настроить группы аренды.</span><span class="sxs-lookup"><span data-stu-id="a9904-105">This topic explains how to set up lease groups.</span></span> <span data-ttu-id="a9904-106">Группы аренды необходимы для создания новых аренд.</span><span class="sxs-lookup"><span data-stu-id="a9904-106">Lease groups are required to create new leases.</span></span> <span data-ttu-id="a9904-107">Книги по аренде сопоставляются с каждой группой аренды.</span><span class="sxs-lookup"><span data-stu-id="a9904-107">Lease books are associated with each lease group.</span></span> <span data-ttu-id="a9904-108">Книги по аренде определяют книги по умолчанию, которые должны быть созданы для каждой аренды.</span><span class="sxs-lookup"><span data-stu-id="a9904-108">Lease books determine the default books that must be created for each lease.</span></span> <span data-ttu-id="a9904-109">Можно назначить отдельные счета для группы аренды на странице **Параметры разноски аренды**.</span><span class="sxs-lookup"><span data-stu-id="a9904-109">You can assign specific accounts to a lease group on the **Lease posting parameters** page.</span></span>

## <a name="create-a-lease-book-and-add-a-lease-group"></a><span data-ttu-id="a9904-110">Создание книги аренды и добавление группы арены</span><span class="sxs-lookup"><span data-stu-id="a9904-110">Create a lease book and add a lease group</span></span>

1. <span data-ttu-id="a9904-111">Перейдите в раздел **Аренда активов \> Настройка \> Группы аренды**.</span><span class="sxs-lookup"><span data-stu-id="a9904-111">Go to **Asset leasing \> Setup \> Lease groups**.</span></span>
2. <span data-ttu-id="a9904-112">На панели операций выберите **Создать** для добавления группы аренды.</span><span class="sxs-lookup"><span data-stu-id="a9904-112">On the Action Pane, select **New** to add a lease group.</span></span> <span data-ttu-id="a9904-113">В сетку добавляется строка.</span><span class="sxs-lookup"><span data-stu-id="a9904-113">A line is added to the grid.</span></span>
3. <span data-ttu-id="a9904-114">В новой строке в поле **Группа аренды** введите значение.</span><span class="sxs-lookup"><span data-stu-id="a9904-114">On the new line, in the **Lease group** field, enter a value.</span></span>
4. <span data-ttu-id="a9904-115">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="a9904-115">In the **Description** field, enter a value.</span></span>

<span data-ttu-id="a9904-116">Введенные сведения добавляются в поле **Группа аренды** на странице **Добавить аренду**.</span><span class="sxs-lookup"><span data-stu-id="a9904-116">The information that you just entered is added to the **Lease group** field on the **Add lease** page.</span></span>

## <a name="associate-a-book-with-a-lease-group"></a><span data-ttu-id="a9904-117">Связывание книги с группой аренды</span><span class="sxs-lookup"><span data-stu-id="a9904-117">Associate a book with a lease group</span></span>

<span data-ttu-id="a9904-118">После создания групп аренды можно назначить книги для каждой группы.</span><span class="sxs-lookup"><span data-stu-id="a9904-118">After you create lease groups, you can assign books to each group.</span></span> <span data-ttu-id="a9904-119">При создании аренды и назначении ее группе аренды система создает набор графиков для каждой книги, связанной с данной группой аренды.</span><span class="sxs-lookup"><span data-stu-id="a9904-119">When you create a lease and assign it to a lease group, the system creates a set of schedules for each book that is associated with that lease group.</span></span>

> [!NOTE]
> <span data-ttu-id="a9904-120">Прежде чем книги могут быть назначены группе аренды, необходимо настроить книги.</span><span class="sxs-lookup"><span data-stu-id="a9904-120">Books must be set up before they can be assigned to a lease group.</span></span>

1. <span data-ttu-id="a9904-121">Перейдите в раздел **Аренда активов \> Настройка \> Группа аренды**.</span><span class="sxs-lookup"><span data-stu-id="a9904-121">Go to **Asset leasing \> Setup \> Lease group**.</span></span>
2. <span data-ttu-id="a9904-122">Выберите группу аренды, а затем выберите **Книги**.</span><span class="sxs-lookup"><span data-stu-id="a9904-122">Select a lease group, and then select **Books**.</span></span>
3. <span data-ttu-id="a9904-123">Выберите **Создать**, а затем в поле **Тип книги** выберите книгу, которую необходимо назначить группе аренды.</span><span class="sxs-lookup"><span data-stu-id="a9904-123">Select **New**, and then, in the **Book type** field, select the book to assign to the lease group.</span></span> <span data-ttu-id="a9904-124">Имеется возможность назначить несколько книг группе аренды, если аренда должна быть учтена другими способами.</span><span class="sxs-lookup"><span data-stu-id="a9904-124">You can assign multiple books to a lease group if a lease must be accounted for in different ways.</span></span>
