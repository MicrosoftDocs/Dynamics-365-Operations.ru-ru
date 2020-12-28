---
title: Устранение неполадок заказов на покупку
description: В этом разделе описывается устранение проблем, которые могут встретиться при работе с заказами на покупку.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 234458f865e37a2d962aee8ab218b9521847081d
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4436461"
---
# <a name="troubleshoot-purchase-orders"></a><span data-ttu-id="191d7-103">Устранение неполадок заказов на покупку</span><span class="sxs-lookup"><span data-stu-id="191d7-103">Troubleshoot purchase orders</span></span>

<span data-ttu-id="191d7-104">В этом разделе описывается устранение проблем, которые могут встретиться при работе с заказами на покупку.</span><span class="sxs-lookup"><span data-stu-id="191d7-104">This topic describes how to fix issues that you might encounter while you work with purchase orders.</span></span>

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a><span data-ttu-id="191d7-105">Действие может быть выполнено только после полного распределения номера строки.</span><span class="sxs-lookup"><span data-stu-id="191d7-105">An action can be completed only after the line number is fully distributed.</span></span>

<span data-ttu-id="191d7-106">Эта проблема может возникнуть из-за несогласованности в распределениях заказов на покупку.</span><span class="sxs-lookup"><span data-stu-id="191d7-106">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="191d7-107">Чтобы разблокировать эту проблему и сбросить заказ на покупку в состояние *Черновик*, перейдите в раздел **Закупки и источники \> Периодические задачи \> Очистка \> Сброс распределения заказов на покупку**.</span><span class="sxs-lookup"><span data-stu-id="191d7-107">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="191d7-108">Дополнительные сведения см. в следующей записи блога: [Устранение ошибок распределения заказов на покупку в Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="191d7-108">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a><span data-ttu-id="191d7-109">При импорте заказов на покупку с помощью управления данными номера строк заказа на покупку не будут следовать шагу, определенному в параметрах системы.</span><span class="sxs-lookup"><span data-stu-id="191d7-109">When purchase orders are imported through data management, purchase order line numbers don't follow the increment that defined in system parameters.</span></span>

### <a name="issue-description"></a><span data-ttu-id="191d7-110">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="191d7-110">Issue description</span></span>

<span data-ttu-id="191d7-111">По умолчанию автоматически формируемые номера строк для строк заказа на покупку, импортируемых через информационный объект *Строки заказа на покупку V2*, не используют увеличение номера системной строки, указанное в параметрах системы.</span><span class="sxs-lookup"><span data-stu-id="191d7-111">By default, automatically generated line numbers for purchase order lines that are imported through the *Purchase order lines V2* data entity don't use the system line number increment that is specified in system parameters.</span></span> <span data-ttu-id="191d7-112">Если вручную создать заказ на покупку и добавить строки через пользовательский интерфейс, номера строк увеличиваются правильно.</span><span class="sxs-lookup"><span data-stu-id="191d7-112">If you manually create a purchase order and add lines through the user interface (UI), the line numbers are incremented correctly.</span></span> <span data-ttu-id="191d7-113">Однако если используется структура управления данными (DMF), они не увеличиваются должным образом.</span><span class="sxs-lookup"><span data-stu-id="191d7-113">However, if you use the Data management framework (DMF), they aren't incremented correctly.</span></span>

<span data-ttu-id="191d7-114">Эта проблема происходит из-за того, что если при импорте строк через DMF номера строк еще не назначены в импортированной сущности, система использует метод DMF для их назначения.</span><span class="sxs-lookup"><span data-stu-id="191d7-114">This issue occurs because, when you import lines via DMF, if line numbers aren't already assigned in the imported entity, the system uses DMF's method for assigning them.</span></span> <span data-ttu-id="191d7-115">Этот метод всегда увеличивает номера строк на единицу.</span><span class="sxs-lookup"><span data-stu-id="191d7-115">That method always increments line numbers by one.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="191d7-116">Временное решение проблемы</span><span class="sxs-lookup"><span data-stu-id="191d7-116">Issue workaround</span></span>

<span data-ttu-id="191d7-117">Убедитесь, что требуемые номера строк уже заданы в полях номера строки информационного объекта при импорте строк заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="191d7-117">Make sure that the desired line numbers are already given in the data entity line number fields when you import the purchase order lines.</span></span> <span data-ttu-id="191d7-118">В этом случае DMF не перезапишет номера строк.</span><span class="sxs-lookup"><span data-stu-id="191d7-118">In this case, DMF won't overwrite the line numbers.</span></span>

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a><span data-ttu-id="191d7-119">Налоговая группа по умолчанию и скидка по оплате по умолчанию не заполняются из счета в накладной.</span><span class="sxs-lookup"><span data-stu-id="191d7-119">A default tax group and a default cash discount aren't filled in from the invoice account.</span></span>

<span data-ttu-id="191d7-120">При использовании счета в накладной, отличающегося от счета клиента, налоговая группа по умолчанию и используемая по умолчанию скидка по оплате не заполняется из счета по накладной при создании заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="191d7-120">If you're using an invoice account that differs from the customer account, a default tax group and a default cash discount aren't filled in from the invoice account when a purchase order is created.</span></span>

<span data-ttu-id="191d7-121">Такое поведение предусмотрено разработчиками.</span><span class="sxs-lookup"><span data-stu-id="191d7-121">This behavior is by design.</span></span> <span data-ttu-id="191d7-122">Значения по умолчанию для налоговой группы, скидок по оплате и другой ценовой информации основываются на счете клиента, а не на счете в накладной.</span><span class="sxs-lookup"><span data-stu-id="191d7-122">The default values for the tax group, cash discounts, and other price information are based on the customer account, not the invoice account.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="191d7-123">Во время подтверждения заказа на покупку я получаю ошибку "Ссылка на объект не указывает" или при разноске накладной поставщика возникает исключение "Адресат вызова создал исключение".</span><span class="sxs-lookup"><span data-stu-id="191d7-123">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="191d7-124">Эта проблема может возникнуть из-за несогласованности в распределениях заказов на покупку.</span><span class="sxs-lookup"><span data-stu-id="191d7-124">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="191d7-125">Чтобы разблокировать эту проблему и сбросить заказ на покупку в состояние *Черновик*, перейдите в раздел **Закупки и источники \> Периодические задачи \> Очистка \> Сброс распределения заказов на покупку**.</span><span class="sxs-lookup"><span data-stu-id="191d7-125">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="191d7-126">Дополнительные сведения см. в следующей записи блога: [Устранение ошибок распределения заказов на покупку в Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="191d7-126">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="191d7-127">Одно или несколько распределений по бухгалтерским счетам выполнены с чрезмерным или недостаточным распределением.</span><span class="sxs-lookup"><span data-stu-id="191d7-127">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="191d7-128">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="191d7-128">Issue description</span></span>

<span data-ttu-id="191d7-129">Вы получаете следующее ошибку: "Одно или несколько распределений по бухгалтерским счетам выполнены с чрезмерным или недостаточным распределением."</span><span class="sxs-lookup"><span data-stu-id="191d7-129">You receive the following error: "One or more accounting distributions is either over-distributed or under-distributed."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="191d7-130">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="191d7-130">Issue resolution</span></span>

<span data-ttu-id="191d7-131">Эта проблема может возникнуть из-за несогласованности в распределениях заказов на покупку.</span><span class="sxs-lookup"><span data-stu-id="191d7-131">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="191d7-132">Чтобы разблокировать эту проблему и сбросить заказ на покупку в состояние *Черновик*, перейдите в раздел **Закупки и источники \> Периодические задачи \> Очистка \> Сброс распределения заказов на покупку**.</span><span class="sxs-lookup"><span data-stu-id="191d7-132">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="191d7-133">Дополнительные сведения см. в следующей записи блога: [Устранение ошибок распределения заказов на покупку в Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="191d7-133">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="can-i-show-only-purchase-orders-that-i-created"></a><span data-ttu-id="191d7-134">Можно ли отобразить только заказы на покупку, созданные мной?</span><span class="sxs-lookup"><span data-stu-id="191d7-134">Can I show only purchase orders that I created?</span></span>

<span data-ttu-id="191d7-135">В настоящее время эта функциональная возможность недоступна.</span><span class="sxs-lookup"><span data-stu-id="191d7-135">This functionality isn't currently available.</span></span>

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a><span data-ttu-id="191d7-136">Можно ли резервировать запасы и создавать проводки по зарегистрированным запасам в заказе на покупку?</span><span class="sxs-lookup"><span data-stu-id="191d7-136">Can I reserve inventory and create transactions against registered inventory on a purchase order?</span></span>

### <a name="issue-description"></a><span data-ttu-id="191d7-137">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="191d7-137">Issue description</span></span>

<span data-ttu-id="191d7-138">Даже если номенклатуры находятся в состоянии *Зарегистрировано* в заказе на покупку, по-прежнему можно зарезервировать запасы.</span><span class="sxs-lookup"><span data-stu-id="191d7-138">Even when items are in a *Registered* state on a purchase order, you can still reserve the inventory.</span></span> <span data-ttu-id="191d7-139">Другими словами, можно создать проводки по зарегистрированным запасам.</span><span class="sxs-lookup"><span data-stu-id="191d7-139">In other words, you can create transactions against the registered inventory.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="191d7-140">Воспроизведение проблемы</span><span class="sxs-lookup"><span data-stu-id="191d7-140">Reproduce the issue</span></span>

<span data-ttu-id="191d7-141">Следующая процедура показывает один из способов воспроизведения проблемы.</span><span class="sxs-lookup"><span data-stu-id="191d7-141">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="191d7-142">Создание заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="191d7-142">Create a purchase order.</span></span>
2. <span data-ttu-id="191d7-143">Зарегистрируйте строку заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="191d7-143">Register the purchase order line.</span></span>
3. <span data-ttu-id="191d7-144">Обратите внимание, что можно создавать резервирования или проводки по зарегистрированным запасам.</span><span class="sxs-lookup"><span data-stu-id="191d7-144">Notice that you can generate reservations or transactions against the registered inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="191d7-145">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="191d7-145">Issue resolution</span></span>

<span data-ttu-id="191d7-146">Такое поведение предусмотрено разработчиками.</span><span class="sxs-lookup"><span data-stu-id="191d7-146">This behavior is by design.</span></span> <span data-ttu-id="191d7-147">Ожидание заключается в том, что зарегистрированные номенклатуры физически поступили на склад или в запасы, и поэтому они доступны для резервирования.</span><span class="sxs-lookup"><span data-stu-id="191d7-147">The expectation is that the registered items have physically arrived in the warehouse or inventory, and that they are therefore available for reservation.</span></span>

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a><span data-ttu-id="191d7-148">Заказы на покупку не отображают языковые настройки юридического лица.</span><span class="sxs-lookup"><span data-stu-id="191d7-148">Purchase orders don't reflect the language settings of the legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="191d7-149">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="191d7-149">Issue description</span></span>

<span data-ttu-id="191d7-150">Название продукта в заказе на покупку отображается на системном языке, а не на языке, указанном для юридического лица, в котором был создан заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="191d7-150">The product name on a purchase order is shown in the system language instead of the language that is set for the legal entity where the purchase order was created.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="191d7-151">Воспроизведение проблемы</span><span class="sxs-lookup"><span data-stu-id="191d7-151">Reproduce the issue</span></span>

<span data-ttu-id="191d7-152">Следующая процедура показывает один из способов воспроизведения проблемы.</span><span class="sxs-lookup"><span data-stu-id="191d7-152">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="191d7-153">Установите для системного языка значение *EN-US* (Английский США).</span><span class="sxs-lookup"><span data-stu-id="191d7-153">Set the system language to *EN-US* (US English).</span></span>
1. <span data-ttu-id="191d7-154">Убедитесь, что имеется продукт, в котором поддерживаются языки *EN-US* и *DE* (немецкий) для переводов названия продукта.</span><span class="sxs-lookup"><span data-stu-id="191d7-154">Make sure that there is a product where the *EN-US* and *DE* (German) languages are maintained for translations of the product name.</span></span>
1. <span data-ttu-id="191d7-155">Измените язык юридического лица на *DE*.</span><span class="sxs-lookup"><span data-stu-id="191d7-155">Change the language of a legal entity to *DE*.</span></span>
1. <span data-ttu-id="191d7-156">В юридическом лице, в котором установлен язык *DE*, создайте заказ на покупку, включающий этот продукт.</span><span class="sxs-lookup"><span data-stu-id="191d7-156">In the legal entity where *DE* is set as the language, create a purchase order that includes the product.</span></span>
1. <span data-ttu-id="191d7-157">Обратите внимание, что название продукта все равно отображается на английском языке (США) (язык системы).</span><span class="sxs-lookup"><span data-stu-id="191d7-157">Notice that the product name is still shown in US English (the system language).</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="191d7-158">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="191d7-158">Issue resolution</span></span>

<span data-ttu-id="191d7-159">Такое поведение предусмотрено разработчиками.</span><span class="sxs-lookup"><span data-stu-id="191d7-159">This behavior is by design.</span></span> <span data-ttu-id="191d7-160">В заказах на покупку продукт всегда отображается на системном языке.</span><span class="sxs-lookup"><span data-stu-id="191d7-160">On purchase orders, the product is always shown in the system language.</span></span> <span data-ttu-id="191d7-161">Язык заказов на покупку используется при создании журнала подтверждения.</span><span class="sxs-lookup"><span data-stu-id="191d7-161">The purchase order language is used when a confirmation journal is created.</span></span>

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a><span data-ttu-id="191d7-162">Сущность списка утвержденных поставщиков по продуктам не допускает изменения даты вступления в силу.</span><span class="sxs-lookup"><span data-stu-id="191d7-162">The Approved vendor list by product entity doesn't allow the effective date to be changed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="191d7-163">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="191d7-163">Issue description</span></span>

<span data-ttu-id="191d7-164">У продукта имеется утвержденный поставщик, который, например, имеет дату вступления в силу 11 января 2018 года (*01/11/2018*) и дату окончания срока действия *Никогда*.</span><span class="sxs-lookup"><span data-stu-id="191d7-164">A product has an approved vendor that has, for example, an effective date of January 11, 2018 (*01/11/2018*), and an expiration date of *Never*.</span></span> <span data-ttu-id="191d7-165">При попытке изменить дату вступления в силу на 10 января 2018 года (*01/10/2018*) или 12 января 2018 года (*01/12/2018*) появляется следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="191d7-165">If you try to change the effective date to January 10, 2018 (*01/10/2018*), or January 12, 2018 (*01/12/2018*), you receive the following error:</span></span>

> <span data-ttu-id="191d7-166">Не удается создать запись в списке утвержденных поставщиков (PdsApproveVendorList).</span><span class="sxs-lookup"><span data-stu-id="191d7-166">Cannot create a record in Approved supplier list (PdsApproveVendorList).</span></span> <span data-ttu-id="191d7-167">Значение "Дата окончания срока действия" должно быть больше или равно значению "Дата вступления в силу".</span><span class="sxs-lookup"><span data-stu-id="191d7-167">The 'Expiration' value needs to be greater than or equal to the 'Effective' value.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="191d7-168">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="191d7-168">Issue resolution</span></span>

<span data-ttu-id="191d7-169">Можно расширить только период, для которого утвержден поставщик.</span><span class="sxs-lookup"><span data-stu-id="191d7-169">You can only extend the period that the vendor is approved for.</span></span> <span data-ttu-id="191d7-170">Применяются следующие правила:</span><span class="sxs-lookup"><span data-stu-id="191d7-170">The following rules apply:</span></span>

- <span data-ttu-id="191d7-171">Чтобы изменить дату вступления в силу, чтобы она была раньше, чем любые существующие записи (периоды) для поставщика номенклатуры, дата окончания нового периода должна предшествовать всем датам истечения срока действия в существующих записях.</span><span class="sxs-lookup"><span data-stu-id="191d7-171">To change the effective date so that it's earlier than any of the existing records (periods) for the item vendor, the expiration date of the new period must be before all the expiration dates in the existing records.</span></span>
- <span data-ttu-id="191d7-172">Чтобы изменить дату истечения срока действия, чтобы она была позднее любого из существующих периодов, дата вступления в силу должна быть позже последней даты окончания срока действия в любой существующей записи.</span><span class="sxs-lookup"><span data-stu-id="191d7-172">To change the expiration date so that it's later than any of the existing periods, the effective date must be after the latest expiration date in any existing record.</span></span>
- <span data-ttu-id="191d7-173">Чтобы уменьшить общий период, на который утверждается поставщик, необходимо удалить или изменить существующие записи.</span><span class="sxs-lookup"><span data-stu-id="191d7-173">To reduce the overall period that the vendor is approved for, you must delete or modify existing records.</span></span> <span data-ttu-id="191d7-174">В качестве альтернативы можно использовать ключ **усечение** при импорте.</span><span class="sxs-lookup"><span data-stu-id="191d7-174">Alternatively, you can use the **truncate** switch during import.</span></span> <span data-ttu-id="191d7-175">Этот ключ удаляет все существующие записи в таблице для утвержденных поставщиков по номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="191d7-175">This switch deletes all existing records in the table for approved vendors by item.</span></span>

<span data-ttu-id="191d7-176">Для примера сценария, описанного в описании проблемы, в котором запись имеет дату вступления в силу *01/11/2018* и дату истечения срока действия *Никогда*, можно импортировать новую запись с датой вступления в силу *01/10/2018* и датой истечения срока действия *Никогда*.</span><span class="sxs-lookup"><span data-stu-id="191d7-176">For the example scenario that is described in the issue description, where a record has an effective date of *01/11/2018* and an expiration date of *Never*, you can import a new record that has an effective date of *01/10/2018* and an expiration date of *Never*.</span></span> <span data-ttu-id="191d7-177">Однако нельзя уменьшить период, чтобы дата вступления в силу обновлялась до *01/12/2018* через управление данными.</span><span class="sxs-lookup"><span data-stu-id="191d7-177">However, you can't reduce the period so that the effective date is updated to *01/12/2018* via data management.</span></span> <span data-ttu-id="191d7-178">Это изменение необходимо выполнить с помощью пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="191d7-178">You must make this change through the UI.</span></span>

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-nameisnt-synced"></a><span data-ttu-id="191d7-179">После изменения адреса поставки в заголовке заказа на покупку имя доставки не синхронизируется.</span><span class="sxs-lookup"><span data-stu-id="191d7-179">After I change the delivery address on a purchase order header, the delivery name isn't synced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="191d7-180">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="191d7-180">Issue description</span></span>

<span data-ttu-id="191d7-181">Адрес в заголовке заказа на покупку обновляется до адреса, который не является адресом доставки.</span><span class="sxs-lookup"><span data-stu-id="191d7-181">The address on the header of a purchase order is updated to an address that isn't a delivery address.</span></span> <span data-ttu-id="191d7-182">Хотя адрес обновляется в заказе на покупку, имя доставки не обновляется на основе обновленного адреса.</span><span class="sxs-lookup"><span data-stu-id="191d7-182">Although the address is updated on the purchase order, the delivery name isn't updated based on the updated address.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="191d7-183">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="191d7-183">Issue resolution</span></span>

<span data-ttu-id="191d7-184">Такое поведение предусмотрено разработчиками.</span><span class="sxs-lookup"><span data-stu-id="191d7-184">This behavior is by design.</span></span> <span data-ttu-id="191d7-185">Выбранный адрес должен классифицироваться как адрес доставки.</span><span class="sxs-lookup"><span data-stu-id="191d7-185">The selected address must be classified as a delivery address.</span></span> <span data-ttu-id="191d7-186">В противном случае имя доставки не обновляется в соответствии с выбранным адресом.</span><span class="sxs-lookup"><span data-stu-id="191d7-186">Otherwise, the delivery name isn't updated based on the selected address.</span></span>

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a><span data-ttu-id="191d7-187">Можно ли найти пользователя, который отменил заказ на покупку?</span><span class="sxs-lookup"><span data-stu-id="191d7-187">Can I find the user who canceled a purchase order?</span></span>

<span data-ttu-id="191d7-188">Эта информация отслеживается только в том случае, если заказ на покупку подлежит управлению изменениями.</span><span class="sxs-lookup"><span data-stu-id="191d7-188">This information is tracked only if the purchase order is subject to change management.</span></span> <span data-ttu-id="191d7-189">При использовании управления изменениями можно видеть, кто отправил изменение (отмену) и кто его утвердил.</span><span class="sxs-lookup"><span data-stu-id="191d7-189">If you use change management, you can see who submitted the change (the cancellation), and who approved it.</span></span>
