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
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2c06f6f943c8a47fbe650a67017b95d799914a0e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971361"
---
# <a name="create-a-lease-group"></a><span data-ttu-id="1b3f2-104">Создание группы аренды</span><span class="sxs-lookup"><span data-stu-id="1b3f2-104">Create a lease group</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b3f2-105">В этом разделе описывается, как настроить группы аренды.</span><span class="sxs-lookup"><span data-stu-id="1b3f2-105">This topic explains how to set up lease groups.</span></span> <span data-ttu-id="1b3f2-106">Группы аренды необходимы для создания новых аренд.</span><span class="sxs-lookup"><span data-stu-id="1b3f2-106">Lease groups are required to create new leases.</span></span> <span data-ttu-id="1b3f2-107">Книги по аренде сопоставляются с каждой группой аренды.</span><span class="sxs-lookup"><span data-stu-id="1b3f2-107">Lease books are associated with each lease group.</span></span> <span data-ttu-id="1b3f2-108">Книги по аренде определяют книги по умолчанию, которые должны быть созданы для каждой аренды.</span><span class="sxs-lookup"><span data-stu-id="1b3f2-108">Lease books determine the default books that must be created for each lease.</span></span> <span data-ttu-id="1b3f2-109">Можно назначить отдельные счета для группы аренды на странице **Параметры разноски аренды**.</span><span class="sxs-lookup"><span data-stu-id="1b3f2-109">You can assign specific accounts to a lease group on the **Lease posting parameters** page.</span></span>

## <a name="create-a-lease-book-and-add-a-lease-group"></a><span data-ttu-id="1b3f2-110">Создание книги аренды и добавление группы арены</span><span class="sxs-lookup"><span data-stu-id="1b3f2-110">Create a lease book and add a lease group</span></span>

1. <span data-ttu-id="1b3f2-111">Перейдите в раздел **Аренда активов \> Настройка \> Группы аренды**.</span><span class="sxs-lookup"><span data-stu-id="1b3f2-111">Go to **Asset leasing \> Setup \> Lease groups**.</span></span>
2. <span data-ttu-id="1b3f2-112">На панели операций выберите **Создать** для добавления группы аренды.</span><span class="sxs-lookup"><span data-stu-id="1b3f2-112">On the Action Pane, select **New** to add a lease group.</span></span> <span data-ttu-id="1b3f2-113">В сетку добавляется строка.</span><span class="sxs-lookup"><span data-stu-id="1b3f2-113">A line is added to the grid.</span></span>
3. <span data-ttu-id="1b3f2-114">В новой строке в поле **Группа аренды** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1b3f2-114">On the new line, in the **Lease group** field, enter a value.</span></span>
4. <span data-ttu-id="1b3f2-115">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1b3f2-115">In the **Description** field, enter a value.</span></span>

<span data-ttu-id="1b3f2-116">Введенные сведения добавляются в поле **Группа аренды** на странице **Добавить аренду**.</span><span class="sxs-lookup"><span data-stu-id="1b3f2-116">The information that you just entered is added to the **Lease group** field on the **Add lease** page.</span></span>

## <a name="associate-a-book-with-a-lease-group"></a><span data-ttu-id="1b3f2-117">Связывание книги с группой аренды</span><span class="sxs-lookup"><span data-stu-id="1b3f2-117">Associate a book with a lease group</span></span>

<span data-ttu-id="1b3f2-118">После создания групп аренды можно назначить книги для каждой группы.</span><span class="sxs-lookup"><span data-stu-id="1b3f2-118">After you create lease groups, you can assign books to each group.</span></span> <span data-ttu-id="1b3f2-119">При создании аренды и назначении ее группе аренды система создает набор графиков для каждой книги, связанной с данной группой аренды.</span><span class="sxs-lookup"><span data-stu-id="1b3f2-119">When you create a lease and assign it to a lease group, the system creates a set of schedules for each book that is associated with that lease group.</span></span>

> [!NOTE]
> <span data-ttu-id="1b3f2-120">Прежде чем книги могут быть назначены группе аренды, необходимо настроить книги.</span><span class="sxs-lookup"><span data-stu-id="1b3f2-120">Books must be set up before they can be assigned to a lease group.</span></span>

1. <span data-ttu-id="1b3f2-121">Перейдите в раздел **Аренда активов \> Настройка \> Группа аренды**.</span><span class="sxs-lookup"><span data-stu-id="1b3f2-121">Go to **Asset leasing \> Setup \> Lease group**.</span></span>
2. <span data-ttu-id="1b3f2-122">Выберите группу аренды, а затем выберите **Книги**.</span><span class="sxs-lookup"><span data-stu-id="1b3f2-122">Select a lease group, and then select **Books**.</span></span>
3. <span data-ttu-id="1b3f2-123">Выберите **Создать**, а затем в поле **Тип книги** выберите книгу, которую необходимо назначить группе аренды.</span><span class="sxs-lookup"><span data-stu-id="1b3f2-123">Select **New**, and then, in the **Book type** field, select the book to assign to the lease group.</span></span> <span data-ttu-id="1b3f2-124">Имеется возможность назначить несколько книг группе аренды, если аренда должна быть учтена другими способами.</span><span class="sxs-lookup"><span data-stu-id="1b3f2-124">You can assign multiple books to a lease group if a lease must be accounted for in different ways.</span></span>
