---
title: Настройка программ непрерывности для центров обработки вызовов
description: В этом статье описывается, как настроить программу непрерывности для центра обработки вызовов.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 369856f33c6da49b6c6b3f51f42c99a8f07fe777
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "320980"
---
# <a name="set-up-continuity-programs-for-call-centers"></a><span data-ttu-id="e8a7d-103">Настройка программ непрерывности для центров обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="e8a7d-103">Set up continuity programs for call centers</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e8a7d-104">В этом статье описывается, как настроить программу непрерывности для центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-104">This article describes how to set up a continuity program for a call center.</span></span>

<span data-ttu-id="e8a7d-105">Согласно программе непрерывности, которая также называется программой повторяющихся заказов, клиенты получают регулярные отгрузки продукта в соответствии с предопределенным графиком.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-105">In a continuity program, which is also known as a recurring order program, customers receive regular product shipments according to a predefined schedule.</span></span> <span data-ttu-id="e8a7d-106">Каждая отгрузка может содержать разные продукты, как в случае книжного клуба, предлагающего новую книгу каждый месяц, или один и тот же продукт.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-106">Each shipment can contain a different product, as in the case of a book-of-the-month club, or the same product can be sent repeatedly.</span></span> <span data-ttu-id="e8a7d-107">Для настройки программы непрерывности выполните следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-107">To set up a continuity program, you must complete the following tasks.</span></span>

1. <span data-ttu-id="e8a7d-108">Настройте параметры непрерывности на странице **Параметры центра обработки вызовов**.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-108">Set the continuity parameters on the **Call center parameters** page.</span></span>
2. <span data-ttu-id="e8a7d-109">Создайте программу непрерывности, в которой определяются сведения, такие как график оплаты, время отгрузки и возможность предварительного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-109">Create a continuity program that specifies details such as the payment schedule, the timing of the shipments, and whether billing is up front.</span></span> <span data-ttu-id="e8a7d-110">Также необходимо добавить список продуктов, включенных в программу непрерывности.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-110">You must also add a list of products that are included in the continuity program.</span></span> <span data-ttu-id="e8a7d-111">Каждый продукт получает идентификационный код события, назначаемый последовательно, начиная с 1.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-111">Each product receives an event ID number that is assigned sequentially, beginning with 1.</span></span> <span data-ttu-id="e8a7d-112">Коды событий определяют порядок отправки продуктов.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-112">The event IDs determine the order that products are sent in.</span></span>

    - <span data-ttu-id="e8a7d-113">Если клиенты получают разные продукты в каждой отгрузке, продукты отправляются в последовательном порядке в соответствии с их кодами событий, начиная с текущего события.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-113">If customers receive a different product in each shipment, the products are sent in sequential order, based on their event IDs and beginning with the current event.</span></span>
    - <span data-ttu-id="e8a7d-114">Если клиенты получают одинаковый продукт в каждой отгрузке, в списке содержится только один продукт, который имеет один код события.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-114">If customers receive the same product in each shipment, the list contains only one product that has one event ID.</span></span> <span data-ttu-id="e8a7d-115">Одно и то же событие происходит повторно.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-115">The same event occurs repeatedly.</span></span> <span data-ttu-id="e8a7d-116">Можно определить, сколько раз повторять каждое событие.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-116">You can specify how many times each event is repeated.</span></span>

3. <span data-ttu-id="e8a7d-117">Создайте родительский продукт, представляющий программу непрерывности, созданную в ходе задачи 2.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-117">Create a parent product that represents the continuity program that you created in task 2.</span></span> <span data-ttu-id="e8a7d-118">При добавлении этого продукта в заказ на продажу откроется страница **Непрерывность**.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-118">If you add this product to a sales order, the **Continuity** page opens.</span></span> <span data-ttu-id="e8a7d-119">Затем эту страницу можно использовать для создания фактического непрерывного заказа.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-119">You can then use that page to create the actual continuity order.</span></span> <span data-ttu-id="e8a7d-120">Родительский продукт не определяет отдельные продукты, которые клиент получает в каждой отгрузке.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-120">The parent product doesn't specify the individual products that the customer receives in each shipment.</span></span>

<span data-ttu-id="e8a7d-121">После настройки программы непрерывности, как описано в разделе выше, можно создать непрерывный заказ для клиента.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-121">After you've set up a continuity program as described above, you can create a continuity order for a customer.</span></span> <span data-ttu-id="e8a7d-122">Можно также выполнить следующие дополнительные задачи обслуживания.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-122">You might also have to perform the following additional maintenance tasks.</span></span>

- <span data-ttu-id="e8a7d-123">**Обновление периода текущего события непрерывности** — настройка пакетного задания для сообщения системе о периоде текущего события.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-123">**Update the current continuity event period** – Set up a batch job that tells the system what the current event period is.</span></span>
- <span data-ttu-id="e8a7d-124">**Создание дочерних непрерывных заказов** — создание дочерних заказов из родительского непрерывного заказа.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-124">**Create continuity child orders** – Create child orders from the parent continuity order.</span></span>
- <span data-ttu-id="e8a7d-125">**Обработка платежей непрерывности** — обработка выставления накладных и уведомлений для платежей, связанных с непрерывными заказами на продажу.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-125">**Process continuity payments** – Process billing and notifications for payments that are associated with continuity sales orders.</span></span>
- <span data-ttu-id="e8a7d-126">**Расширение строк непрерывности** (при необходимости) — увеличение количества повторов события непрерывности.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-126">**Extend continuity lines** (if required) – Extend the number of times that a continuity event can be repeated.</span></span> <span data-ttu-id="e8a7d-127">Количество повторов отгрузки можно увеличить, превысив лимит, установленный в поле **Порог повторения непрерывности** в параметрах центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-127">The repetition of shipments can then extend beyond the limit that was set in the **Continuity repeat threshold** field in the call center parameters.</span></span>
- <span data-ttu-id="e8a7d-128">**Выполнение обновления непрерывности** (при необходимости)— синхронизация изменений между программой непрерывности и непрерывными родительскими заказами на продажу.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-128">**Perform a continuity update** (if required) – Synchronize changes between the continuity program and the continuity parent sales orders.</span></span>
- <span data-ttu-id="e8a7d-129">**Закрытие строк и заказов родительского объекта непрерывности** — закрытие непрерывных заказов.</span><span class="sxs-lookup"><span data-stu-id="e8a7d-129">**Close continuity parent lines and orders** – Close continuity orders.</span></span>
