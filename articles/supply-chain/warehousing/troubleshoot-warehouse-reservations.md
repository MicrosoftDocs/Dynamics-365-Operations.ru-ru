---
title: Устранение неполадок резервирования в модуле "Управление складом"
description: В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с резервированием на складе в Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828114"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="25634-103">Устранение неполадок резервирования в модуле "Управление складом"</span><span class="sxs-lookup"><span data-stu-id="25634-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25634-104">В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с резервированием на складе в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="25634-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="25634-105">Для тем, которые связаны с регистрациями партий и серийных номеров, см. раздел [Устранение неполадок в иерархиях резервирования партий и серийных номеров](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span><span class="sxs-lookup"><span data-stu-id="25634-105">For topics that are related to batch and serial number registrations, see [Troubleshoot warehouse batch and serial reservation hierarchies](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="25634-106">Я получаю следующее сообщение об ошибке: "Не удается удалить резервирования в связи с наличием зависимой от них работы."</span><span class="sxs-lookup"><span data-stu-id="25634-106">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="25634-107">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="25634-107">Issue description</span></span>

<span data-ttu-id="25634-108">Нельзя отменять резервирование запасов в строке продаж, так как с этой строкой связана открытая работа.</span><span class="sxs-lookup"><span data-stu-id="25634-108">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="25634-109">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="25634-109">Issue resolution</span></span>

<span data-ttu-id="25634-110">Выясните, существует ли открытая работа группы упаковки, чтобы переместить номенклатуру из станции упаковки в другое местоположение (например, *Дверь отсека*).</span><span class="sxs-lookup"><span data-stu-id="25634-110">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="25634-111">Просмотрите записи на страницах **Журнал создания работ** и **Сведения о работе**, чтобы определить, что физически резервирует запасы, а затем выполните или удалите работу, чтобы освободить резервирование.</span><span class="sxs-lookup"><span data-stu-id="25634-111">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="25634-112">Я получают следующее сообщение об ошибке: "Количество запасов -%1 не удалось обновить из-за недостаточности складских проводок для номенклатуры %2...."</span><span class="sxs-lookup"><span data-stu-id="25634-112">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="25634-113">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="25634-113">Issue description</span></span>

<span data-ttu-id="25634-114">Эта проблема может возникнуть, если система не может обновить количество запасов из-за того, что отсутствуют достаточные складские проводки с указанными аналитиками.</span><span class="sxs-lookup"><span data-stu-id="25634-114">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="25634-115">Ниже приведен весь текст полного сообщения об ошибке:</span><span class="sxs-lookup"><span data-stu-id="25634-115">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="25634-116">Количество запасов -%1 не удалось обновить из-за недостаточности складских проводок для номенклатуры %2 с аналитиками Размер=%3, Цвет=%4, Дополнения=%5, Сайт=%6, Склад=%7, Местонахождение=%8, Состояние запасов=Доступно, Грузоместо=%9, Новер партии=%10 для ссылочного кода %11 с номером лота %12.</span><span class="sxs-lookup"><span data-stu-id="25634-116">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="25634-117">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="25634-117">Issue resolution</span></span>

<span data-ttu-id="25634-118">Убедитесь, что никакие складские проводки не выполняют физическое резервирование количества.</span><span class="sxs-lookup"><span data-stu-id="25634-118">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="25634-119">Например, эти проводки могут открывать заказы контроля качества, записи блокировки запасов или заказы на выпуск.</span><span class="sxs-lookup"><span data-stu-id="25634-119">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="25634-120">Получено следующее сообщение об ошибке: "Физические запасы в наличии...невозможно зарезервировать, так как в запасе доступно только 0,00."</span><span class="sxs-lookup"><span data-stu-id="25634-120">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="25634-121">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="25634-121">Issue description</span></span>

<span data-ttu-id="25634-122">Эта проблема может возникнуть, если система не может обновить количество запасов из-за того, что отсутствуют достаточные складские проводки с указанными аналитиками.</span><span class="sxs-lookup"><span data-stu-id="25634-122">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="25634-123">Ниже приведен весь текст полного сообщения об ошибке:</span><span class="sxs-lookup"><span data-stu-id="25634-123">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="25634-124">Физические запасы в наличии Сайт=%1, Склад=%2, Состояние запасов=Доступно, Номер партии=%3, Владелец=%4: %5 невозможно зарезервировать, так как в запасах доступно только 0,00.</span><span class="sxs-lookup"><span data-stu-id="25634-124">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="25634-125">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="25634-125">Issue resolution</span></span>

<span data-ttu-id="25634-126">Вероятно, эта проблема вызвана открытой работой.</span><span class="sxs-lookup"><span data-stu-id="25634-126">This issue is probably caused by open work.</span></span> <span data-ttu-id="25634-127">Завершите работу или выполните получение без создания работы.</span><span class="sxs-lookup"><span data-stu-id="25634-127">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="25634-128">Убедитесь, что никакие складские проводки не выполняют физическое резервирование количества.</span><span class="sxs-lookup"><span data-stu-id="25634-128">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="25634-129">Например, эти проводки могут открывать заказы контроля качества, записи блокировки запасов или заказы на выпуск.</span><span class="sxs-lookup"><span data-stu-id="25634-129">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
