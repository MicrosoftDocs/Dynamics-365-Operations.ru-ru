---
title: Создание и ведение блокировки запасов
description: В этой теме показано, как использовать блокировку запасов во избежание резервирования физических запасов в наличии другими исходящими документами-источниками.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956166"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="06b65-103">Создание и ведение блокировки запасов</span><span class="sxs-lookup"><span data-stu-id="06b65-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="06b65-104">В этой теме показано, как использовать блокировку запасов во избежание резервирования физических запасов в наличии другими исходящими документами-источниками.</span><span class="sxs-lookup"><span data-stu-id="06b65-104">This topic describes how to use an inventory blocking to prevent physical on-hand inventory from being reserved by other outbound source documents.</span></span> <span data-ttu-id="06b65-105">Перед началом процедуры в этом разделе необходимо получить номенклатуру с физическими запасами в наличии.</span><span class="sxs-lookup"><span data-stu-id="06b65-105">Before you start the procedures in this topic, you must have an item that physical on-hand inventory is available for.</span></span>

## <a name="block-inventory"></a><span data-ttu-id="06b65-106">Блокирование запасов</span><span class="sxs-lookup"><span data-stu-id="06b65-106">Block inventory</span></span>

<span data-ttu-id="06b65-107">Чтобы создать запись блокировки запасов для блокирования запасов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="06b65-107">To create an inventory blocking record so that inventory is blocked, follow these steps.</span></span>

1. <span data-ttu-id="06b65-108">Перейдите в раздел **Управление запасами \> Периодические задачи \> Блокировка запасов**.</span><span class="sxs-lookup"><span data-stu-id="06b65-108">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="06b65-109">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="06b65-109">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="06b65-110">В заголовке новой записи блокировки установите поле **Код номенклатуры** для номенклатуры, которую необходимо заблокировать, и введите описание.</span><span class="sxs-lookup"><span data-stu-id="06b65-110">On the header of the new blocking record, set the **Item number** field to the item that you want to block, and enter a description.</span></span>
1. <span data-ttu-id="06b65-111">На экспресс-вкладке **Общие** в поле **Количество** введите количество блокируемых номенклатур.</span><span class="sxs-lookup"><span data-stu-id="06b65-111">On the **General** FastTab, in the **Quantity** field, enter the number of items to block.</span></span>
1. <span data-ttu-id="06b65-112">На экспресс-вкладке **Складские аналитики** укажите сайт и склад, где в данный момент находятся номенклатуры, которые необходимо заблокировать.</span><span class="sxs-lookup"><span data-stu-id="06b65-112">On the **Inventory dimensions** FastTab, specify the site and warehouse where the items that you want to block are currently located.</span></span>
1. <span data-ttu-id="06b65-113">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="06b65-113">On the Action Pane, select **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="06b65-114">Обновление условий блокировки запасов</span><span class="sxs-lookup"><span data-stu-id="06b65-114">Update the conditions of the inventory blocking</span></span>

<span data-ttu-id="06b65-115">Чтобы обновить запись блокировки запасов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="06b65-115">To update an inventory blocking record, follow these steps.</span></span>

1. <span data-ttu-id="06b65-116">Перейдите в раздел **Управление запасами \> Периодические задачи \> Блокировка запасов**.</span><span class="sxs-lookup"><span data-stu-id="06b65-116">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="06b65-117">В области списка выберите соответствующую запись блокировки.</span><span class="sxs-lookup"><span data-stu-id="06b65-117">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="06b65-118">Измените запись требуемым образом.</span><span class="sxs-lookup"><span data-stu-id="06b65-118">Edit the record as required.</span></span> <span data-ttu-id="06b65-119">Например, можно изменить значение поля **Ожидаемая дата**, чтобы указать, что заблокированные запасы должны стать доступными для резервирования.</span><span class="sxs-lookup"><span data-stu-id="06b65-119">For example, you might change the value of the **Expected date** field to indicate when the blocked inventory is expected to become available for reservation.</span></span> <span data-ttu-id="06b65-120">Если выбран параметр **Ожидаемые приходы**, дата появится в ожидаемой проводке.</span><span class="sxs-lookup"><span data-stu-id="06b65-120">If the **Expected receipts** option is selected, the date will appear on the expected transaction.</span></span> <span data-ttu-id="06b65-121">(Параметр **Ожидаемые приходы** по умолчанию выбирается при создании записи блокировки вручную.)</span><span class="sxs-lookup"><span data-stu-id="06b65-121">(The **Expected receipts** option is selected by default when you manually create a blocking record.)</span></span>
1. <span data-ttu-id="06b65-122">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="06b65-122">On the Action Pane, select **Save**.</span></span>

## <a name="unblock-inventory"></a><span data-ttu-id="06b65-123">Разблокировка запасов</span><span class="sxs-lookup"><span data-stu-id="06b65-123">Unblock inventory</span></span>

<span data-ttu-id="06b65-124">Чтобы удалить запись блокировки запасов для разблокирования запасов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="06b65-124">To remove an inventory blocking record so that inventory is unblocked, follow these steps.</span></span>

1. <span data-ttu-id="06b65-125">Перейдите в раздел **Управление запасами \> Периодические задачи \> Блокировка запасов**.</span><span class="sxs-lookup"><span data-stu-id="06b65-125">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="06b65-126">В области списка выберите соответствующую запись блокировки.</span><span class="sxs-lookup"><span data-stu-id="06b65-126">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="06b65-127">В области действий выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="06b65-127">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="06b65-128">Выводится запрос на подтверждение операции.</span><span class="sxs-lookup"><span data-stu-id="06b65-128">You're prompted to confirm the operation.</span></span> <span data-ttu-id="06b65-129">Выберите **Да** для продолжения.</span><span class="sxs-lookup"><span data-stu-id="06b65-129">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="06b65-130">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="06b65-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
