---
title: Синхронизация мощностей ресурсов
description: В этой теме приводятся сведения о синхронизации емкости ресурсов между календарями и проектами.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760642"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="65850-103">Синхронизация мощностей ресурсов</span><span class="sxs-lookup"><span data-stu-id="65850-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65850-104">Процессы для синхронизации ресурсов помогают гарантировать, что информация из календаря и базового календаря будет передаваться в планирование ресурсов проекта.</span><span class="sxs-lookup"><span data-stu-id="65850-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="65850-105">Если календарь изменен, процессы выполняют необходимые обновления в планировании ресурсов проекта.</span><span class="sxs-lookup"><span data-stu-id="65850-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="65850-106">Процессы также помогают повысить производительность, потому что информация о ресурсах из календаря синхронизируется заранее.</span><span class="sxs-lookup"><span data-stu-id="65850-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="65850-107">Следовательно, информация о планировании ресурсов обновляется быстрее.</span><span class="sxs-lookup"><span data-stu-id="65850-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="65850-108">Рекомендуется планировать процессы пакетами, а не по одному.</span><span class="sxs-lookup"><span data-stu-id="65850-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="65850-109">В противном случае имеется риск, что кто-то забудет включающие даты, когда информация синхронизировалась в последний раз.</span><span class="sxs-lookup"><span data-stu-id="65850-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="65850-110">Если включающие даты не используются, несоответствия могут иметь место во время синхронизации даты.</span><span class="sxs-lookup"><span data-stu-id="65850-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Синхронизация календаря](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="65850-112">Синхронизация сведения мощности ресурсов</span><span class="sxs-lookup"><span data-stu-id="65850-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="65850-113">Процесс синхронизации предназначен для синхронизации всех данных календаря ресурса.</span><span class="sxs-lookup"><span data-stu-id="65850-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="65850-114">Эта информация включает данные базового календаря обо всех изменениях в таблице мощности календаря ресурсов проекта.</span><span class="sxs-lookup"><span data-stu-id="65850-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="65850-115">Если в проект добавлены новые ресурсы, синхронизация помогает гарантировать доступность обновленных данных календаря.</span><span class="sxs-lookup"><span data-stu-id="65850-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="65850-116">Эта синхронизация может быть выполнена в любое время.</span><span class="sxs-lookup"><span data-stu-id="65850-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="65850-117">Рекомендуется использовать партию.</span><span class="sxs-lookup"><span data-stu-id="65850-117">We recommend that you use a batch.</span></span> <span data-ttu-id="65850-118">Параметры доступны во время синхронизации резервирований мощности.</span><span class="sxs-lookup"><span data-stu-id="65850-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="65850-119">Выберите **Управление и учет по проектам** &gt; **Периодические операции** &gt; **Синхронизация мощностей** &gt; **Синхронизация сведения мощности ресурсов**.</span><span class="sxs-lookup"><span data-stu-id="65850-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="65850-120">Задайте параметры в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="65850-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="65850-121">Параметр</span><span class="sxs-lookup"><span data-stu-id="65850-121">Option</span></span>      | <span data-ttu-id="65850-122">описание</span><span class="sxs-lookup"><span data-stu-id="65850-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="65850-123">Код периода</span><span class="sxs-lookup"><span data-stu-id="65850-123">Period code</span></span> | <span data-ttu-id="65850-124">При необходимости выберите код интервала дат главной книги, чтобы задать начальную и конечную даты для процесса синхронизации для сведения мощности ресурсов.</span><span class="sxs-lookup"><span data-stu-id="65850-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="65850-125">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="65850-125">Start date</span></span>  | <span data-ttu-id="65850-126">Введите начальную дату для процесса синхронизации для сведения мощности ресурсов.</span><span class="sxs-lookup"><span data-stu-id="65850-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="65850-127">Конечная дата</span><span class="sxs-lookup"><span data-stu-id="65850-127">End date</span></span>    | <span data-ttu-id="65850-128">Введите конечную дату для процесса синхронизации для сведения мощности ресурсов.</span><span class="sxs-lookup"><span data-stu-id="65850-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="65850-129">[![Процесс синхронизации](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="65850-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
