---
title: Настройка статуса рейса
description: В этой теме описывается, как установить значения статуса, которые пользователи могут назначить для рейса.
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: b7180cc9ab2d13f2260635d717adb7aab2177ab9
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500894"
---
# <a name="voyage-status-setup"></a><span data-ttu-id="79841-103">Настройка статуса рейса</span><span class="sxs-lookup"><span data-stu-id="79841-103">Voyage status setup</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="79841-104">На странице **Статусы рейса** необходимо определить набор значений статуса, которые пользователи могут назначить для рейса.</span><span class="sxs-lookup"><span data-stu-id="79841-104">On the **Voyage statuses** page, you establish the set of status values that users can assign to voyages.</span></span> <span data-ttu-id="79841-105">Пользователи могут назначить значения статуса рейса для всех уровней рейса: рейса, контейнера отгрузки, листа, заказа на покупку и номенклатуры (строки покупки и строки заказа на перемещение).</span><span class="sxs-lookup"><span data-stu-id="79841-105">Users can assign voyage status values to all levels of a voyage: voyage, shipping container, folio, purchase order, and item (purchase lines and transfer order lines).</span></span> <span data-ttu-id="79841-106">Они используются для двух целей:</span><span class="sxs-lookup"><span data-stu-id="79841-106">They are used for two purposes:</span></span>

- <span data-ttu-id="79841-107">Сообщает пользователю о статусе рейса, контейнера отгрузки, листа, заказа на покупку или номенклатуры (строки покупки и строки заказа на перемещение).</span><span class="sxs-lookup"><span data-stu-id="79841-107">Inform the user about the status of the voyage, shipping container, folio, purchase order, or item (purchase lines and transfer order lines).</span></span>
- <span data-ttu-id="79841-108">Ограничить использование области затрат, запрещая изменение или удаление.</span><span class="sxs-lookup"><span data-stu-id="79841-108">Limit the use of the cost area by preventing modification or deletion.</span></span>

<span data-ttu-id="79841-109">Чтобы настроить статусы рейсов, перейдите **Стоимость на складе \> Настройка \> Статусы рейса**.</span><span class="sxs-lookup"><span data-stu-id="79841-109">To set up your voyage statuses, go to **Landed cost \> Setup \> Voyage statuses**.</span></span> <span data-ttu-id="79841-110">Здесь можно использовать кнопки на панели операций для добавления, удаления и редактирования статусов.</span><span class="sxs-lookup"><span data-stu-id="79841-110">There, you can add, remove, and edit statuses by using the buttons on the Action Pane.</span></span>

<span data-ttu-id="79841-111">К каждой области затрат есть свой собственный набор и иерархия статусов рейса.</span><span class="sxs-lookup"><span data-stu-id="79841-111">Each cost area has its own set and hierarchy of voyage statuses.</span></span> <span data-ttu-id="79841-112">Таким образом, на странице **Статусы рейса** в поле **Область затрат** необходимо сначала выбрать область затрат, для которой необходимо просмотреть или создать статусы рейса.</span><span class="sxs-lookup"><span data-stu-id="79841-112">Therefore, on the **Voyage statuses** page, in the **Cost area** field, you must first select the cost area that you want to view or create voyage statuses for.</span></span> <span data-ttu-id="79841-113">Затем для каждого состояния рейса задайте необходимые поля, которые описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="79841-113">Then, for each voyage status, set the fields that are described in the following table, as required.</span></span> <span data-ttu-id="79841-114">Обратите внимание, что статус рейса также может быть автоматически изменен системными событиям, например, правилами, которые были установлены с помощью центра управления отслеживанием.</span><span class="sxs-lookup"><span data-stu-id="79841-114">Note that the status of a voyage can also be automatically changed by system events, such as rules that have been established by using the tracking control center.</span></span>

| <span data-ttu-id="79841-115">Поле</span><span class="sxs-lookup"><span data-stu-id="79841-115">Field</span></span> | <span data-ttu-id="79841-116">описание</span><span class="sxs-lookup"><span data-stu-id="79841-116">Description</span></span> |
|---|---|
| <span data-ttu-id="79841-117">Статус поездки</span><span class="sxs-lookup"><span data-stu-id="79841-117">Voyage status</span></span> | <span data-ttu-id="79841-118">Введите название статуса рейса.</span><span class="sxs-lookup"><span data-stu-id="79841-118">Enter the name of the voyage status.</span></span> |
| <span data-ttu-id="79841-119">описание</span><span class="sxs-lookup"><span data-stu-id="79841-119">Description</span></span> | <span data-ttu-id="79841-120">Введите описание статуса рейса.</span><span class="sxs-lookup"><span data-stu-id="79841-120">Enter a description of the voyage status.</span></span> |
| <span data-ttu-id="79841-121">Изменить</span><span class="sxs-lookup"><span data-stu-id="79841-121">Modify</span></span> | <span data-ttu-id="79841-122">Установите этот флажок, если пользователям разрешено изменять рейсы с данным статусом.</span><span class="sxs-lookup"><span data-stu-id="79841-122">Select this check box if users are allowed to modify voyages that have this status.</span></span> |
| <span data-ttu-id="79841-123">Удаление</span><span class="sxs-lookup"><span data-stu-id="79841-123">Delete</span></span> | <span data-ttu-id="79841-124">Установите этот флажок, если пользователям разрешено удалять рейсы с данным статусом.</span><span class="sxs-lookup"><span data-stu-id="79841-124">Select this check box if users are allowed to delete voyages that have this status.</span></span> |
| <span data-ttu-id="79841-125">Обязательно</span><span class="sxs-lookup"><span data-stu-id="79841-125">Mandatory</span></span> | <span data-ttu-id="79841-126">Установите этот флажок, чтобы сделать статус рейса обязательным, чтобы он не мог быть пропущен.</span><span class="sxs-lookup"><span data-stu-id="79841-126">Select this check box to make the voyage status mandatory, so that it can't be skipped.</span></span> |
| <span data-ttu-id="79841-127">Родительский</span><span class="sxs-lookup"><span data-stu-id="79841-127">Parent</span></span> | <span data-ttu-id="79841-128">Это поле используется для определения иерархии между значениями статуса.</span><span class="sxs-lookup"><span data-stu-id="79841-128">Use this field to establish a hierarchy among the status values.</span></span> <span data-ttu-id="79841-129">Статусы рейса могут быть изменены (вручную или автоматически) только в направлении вниз по иерархии, от родительского статуса до одного из дочерних статусов.</span><span class="sxs-lookup"><span data-stu-id="79841-129">Voyage statuses can be changed (either manually or automatically) only downward in the hierarchy, from a parent status to one of its child statuses.</span></span>

> [!NOTE]
> <span data-ttu-id="79841-130">Необходимо настроить только конкретные статусы рейса, используемые в организации.</span><span class="sxs-lookup"><span data-stu-id="79841-130">You have to set up only the specific voyage statuses that your organization uses.</span></span> <span data-ttu-id="79841-131">Обычно статусы рейсов включают *Подтверждено*, *Товары в пути*, *Получено*, *Готово к учету затрат* и *Учтено в затратах*.</span><span class="sxs-lookup"><span data-stu-id="79841-131">Typical voyage statuses include *Confirmed*, *Goods in transit*, *Received*, *Ready for costing*, and *Costed*.</span></span> <span data-ttu-id="79841-132">Однако могут присутствовать и другие статусы.</span><span class="sxs-lookup"><span data-stu-id="79841-132">However, other statuses might be present.</span></span>
