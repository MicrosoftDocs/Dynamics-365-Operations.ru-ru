---
title: Устранение неполадок в информации о продукте
description: В этом разделе описывается устранение проблем, которые могут встретиться при работе с информацией о продукте.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4c505ccfd1998acd40dbae715c7fa572e315af2e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007524"
---
# <a name="troubleshoot-product-information"></a><span data-ttu-id="e06a9-103">Устранение неполадок в информации о продукте</span><span class="sxs-lookup"><span data-stu-id="e06a9-103">Troubleshoot product information</span></span>

<span data-ttu-id="e06a9-104">В этом разделе описывается устранение проблем, которые могут встретиться при работе с информацией о продукте.</span><span class="sxs-lookup"><span data-stu-id="e06a9-104">This topic describes how to fix issues that you might encounter while you work with product information.</span></span>

## <a name="i-cant-delete-a-released-product"></a><span data-ttu-id="e06a9-105">Не удается удалить выпущенный продукт.</span><span class="sxs-lookup"><span data-stu-id="e06a9-105">I can't delete a released product.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e06a9-106">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="e06a9-106">Issue description</span></span>

<span data-ttu-id="e06a9-107">Удалить выпущенный продукт и все его варианты можно только в том случае, если выпущенный продукт не имеет каких-либо связанных проводок.</span><span class="sxs-lookup"><span data-stu-id="e06a9-107">You can delete a released product and all its variants only if the released product doesn't have any related transactions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e06a9-108">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="e06a9-108">Issue resolution</span></span>

<span data-ttu-id="e06a9-109">Выполните следующие действия, чтобы удалить выпущенный продукт или шаблон продукта.</span><span class="sxs-lookup"><span data-stu-id="e06a9-109">Follow these steps to delete a released product or product master.</span></span>

1. <span data-ttu-id="e06a9-110">Закройте все открытые проводки по номенклатурам.</span><span class="sxs-lookup"><span data-stu-id="e06a9-110">Close all open transactions for the items.</span></span>
1. <span data-ttu-id="e06a9-111">Сократите запасы до 0 (нуля).</span><span class="sxs-lookup"><span data-stu-id="e06a9-111">Reduce the inventory to 0 (zero).</span></span>
1. <span data-ttu-id="e06a9-112">Выполните закрытие запасов.</span><span class="sxs-lookup"><span data-stu-id="e06a9-112">Perform inventory closing.</span></span>
1. <span data-ttu-id="e06a9-113">Удалите все варианты продуктов для шаблона продукта, который необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="e06a9-113">Delete all product variants for the product master that you want to delete.</span></span>

## <a name="can-i-change-the-item-number-of-a-released-product"></a><span data-ttu-id="e06a9-114">Можно ли изменить код номенклатуры выпущенного продукта?</span><span class="sxs-lookup"><span data-stu-id="e06a9-114">Can I change the item number of a released product?</span></span>

<span data-ttu-id="e06a9-115">В большинстве случаев нельзя редактировать коды номенклатур для выпущенных продуктов, так как это изменение приведет к повреждению данных.</span><span class="sxs-lookup"><span data-stu-id="e06a9-115">In most cases, you can't edit item numbers for released products, because that change will cause data to become corrupted.</span></span> <span data-ttu-id="e06a9-116">Номер номенклатуры можно изменить только в том случае, если необходимо восстановить повреждения данных, которые были вызваны предыдущим переименованием первичного ключа этого выпущенного продукта, как упоминалось в списке [удаленных или устаревших функций для Finance and Operations 10.0.0 с обновлением платформы 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span><span class="sxs-lookup"><span data-stu-id="e06a9-116">You can edit the item number only if you must repair data corruption that was caused by a previous rename of the primary key of that released product, as mentioned in the list of [removed or deprecated features for Finance and Operations 10.0.0 with Platform update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span></span>

<span data-ttu-id="e06a9-117">Если вы хотите иметь возможность редактировать коды номенклатур для выпущенных продуктов, [проголосуйте за эту идею на портале идей](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span><span class="sxs-lookup"><span data-stu-id="e06a9-117">If you want to be able to edit item numbers for released products, [vote for this idea in Ideas portal](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span></span>

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a><span data-ttu-id="e06a9-118">Принцип очистки по умолчанию из продукта не вводится в строку спецификации.</span><span class="sxs-lookup"><span data-stu-id="e06a9-118">The default flushing principle from the product isn't being entered on the bill of materials line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e06a9-119">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="e06a9-119">Issue description</span></span>

<span data-ttu-id="e06a9-120">При добавлении номенклатуры в строку спецификации система не использует сведения о принципе очистки по умолчанию, которые настроены для данной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="e06a9-120">When you add an item to a bill of materials (BOM) line, the system doesn't use the default flushing principle information that is set up for the item.</span></span> <span data-ttu-id="e06a9-121">Иными словами, принцип очистки из номенклатуры не появляется на странице **Строка спецификации**.</span><span class="sxs-lookup"><span data-stu-id="e06a9-121">In other words, the flushing principle from the item doesn't appear on the **BOM line** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e06a9-122">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="e06a9-122">Issue resolution</span></span>

<span data-ttu-id="e06a9-123">Если в строке спецификации указан принцип очистки, он будет применяться к этой строке спецификации.</span><span class="sxs-lookup"><span data-stu-id="e06a9-123">If you specify a flushing principle on a BOM line, it will apply to that BOM line.</span></span> <span data-ttu-id="e06a9-124">Однако если принцип очистки пуст или не задан для строки спецификации, принцип очистки, установленный для номенклатуры, по-прежнему будет применяться к этой строке спецификации, даже если он не отображается в строке спецификации.</span><span class="sxs-lookup"><span data-stu-id="e06a9-124">However, if the flushing principle is blank, or if it isn't set on a BOM line, the flushing principle that is set on the item will still apply to that BOM line, even though it isn't shown on the BOM line.</span></span>

<span data-ttu-id="e06a9-125">Логика задания значений по умолчанию для других функций в Microsoft Dynamics 365 Supply Chain Management обычно не работает таким образом.</span><span class="sxs-lookup"><span data-stu-id="e06a9-125">The defaulting logic for other features in Microsoft Dynamics 365 Supply Chain Management doesn't usually work in this way.</span></span> <span data-ttu-id="e06a9-126">Однако текущее поведение изменить нельзя.</span><span class="sxs-lookup"><span data-stu-id="e06a9-126">However, the current behavior can't be changed.</span></span> <span data-ttu-id="e06a9-127">В противном случае некоторые существующие настройки, полагающиеся на него, могут быть нарушены.</span><span class="sxs-lookup"><span data-stu-id="e06a9-127">Otherwise, some existing customizations that rely on it might be broken.</span></span>

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a><span data-ttu-id="e06a9-128">Система позволяет сохранять повторяющиеся штрих-коды для разных номенклатур или для одной и той же номенклатуры с различной аналитикой.</span><span class="sxs-lookup"><span data-stu-id="e06a9-128">The system lets me save duplicate bar codes for different items or for the same item that has different dimensions.</span></span>

<span data-ttu-id="e06a9-129">В настоящее время система не применяет принудительно уникальные штрих-коды, и добавление этого ограничения было бы радикальным изменением.</span><span class="sxs-lookup"><span data-stu-id="e06a9-129">The system doesn't currently enforce unique bar codes, and the addition of this restriction would be a breaking change.</span></span> <span data-ttu-id="e06a9-130">Фактически, корпорация Майкрософт имеет свидетельства того, что некоторые существующие установки клиентов будут сломаны этим изменением.</span><span class="sxs-lookup"><span data-stu-id="e06a9-130">In fact, Microsoft has evidence that some existing customer installations would be broken by this change.</span></span> <span data-ttu-id="e06a9-131">Однако мы будем рассматривать более широкие изменения в проектировании, чтобы включить эту функцию в будущем.</span><span class="sxs-lookup"><span data-stu-id="e06a9-131">However, we will consider a broader design change to enable this feature in the future.</span></span>

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a><span data-ttu-id="e06a9-132">При редактировании шаблонов записей номенклатуры выводится следующее сообщение об ошибке: "Местоположение склада не может быть создано, так как номенклатура не является складской.</span><span class="sxs-lookup"><span data-stu-id="e06a9-132">I receive the following error message when I edit item record templates: "The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="e06a9-133">Для хранения номенклатур необходимо выбрать параметр учитываемого в запасах продукта для связанной группы номенклатурных моделей."</span><span class="sxs-lookup"><span data-stu-id="e06a9-133">To stock items, the Stocked product option on the associated item model group must be selected."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e06a9-134">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="e06a9-134">Issue description</span></span>

<span data-ttu-id="e06a9-135">Эта проблема возникает, если выполнить следующие шаги для попытки создания шаблона для номенклатуры, которая не хранится в запасах.</span><span class="sxs-lookup"><span data-stu-id="e06a9-135">This issue occurs if you follow these steps to try to create a template for an item that isn't stocked.</span></span>

1. <span data-ttu-id="e06a9-136">Откройте выпущенный продукт, который не хранится в запасах.</span><span class="sxs-lookup"><span data-stu-id="e06a9-136">Open a released product that isn't stocked.</span></span>
1. <span data-ttu-id="e06a9-137">На панели операций откройте вкладку **Параметры** и выберите **Сведения о записи**.</span><span class="sxs-lookup"><span data-stu-id="e06a9-137">On the Action Pane, on the **Options** tab, select **Record info**.</span></span>
1. <span data-ttu-id="e06a9-138">В диалоговом окне **Сведения о записи** выберите **Шаблон компании**.</span><span class="sxs-lookup"><span data-stu-id="e06a9-138">In the **Record information** dialog box, select **Company accounts template**.</span></span>

<span data-ttu-id="e06a9-139">В этом случае вы получите следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="e06a9-139">In this case, you receive the following error message:</span></span>

> <span data-ttu-id="e06a9-140">Местоположение склада не может быть создано, так как номенклатура не хранится в запасах.</span><span class="sxs-lookup"><span data-stu-id="e06a9-140">The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="e06a9-141">Для хранения номенклатур необходимо выбрать параметр учитываемого в запасах продукта для связанной группы номенклатурных моделей.</span><span class="sxs-lookup"><span data-stu-id="e06a9-141">To stock items, the Stocked product option on the associated item model group must be selected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e06a9-142">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="e06a9-142">Issue resolution</span></span>

<span data-ttu-id="e06a9-143">Процесс создания шаблонов продуктов требует дополнительной логики для конкретного продукта.</span><span class="sxs-lookup"><span data-stu-id="e06a9-143">The process of creating product templates requires extra product-specific logic.</span></span> <span data-ttu-id="e06a9-144">Таким образом, нельзя использовать для этой цели универсальную кнопку **Шаблон компании**.</span><span class="sxs-lookup"><span data-stu-id="e06a9-144">Therefore, you can't use the generic **Company accounts template** button for this purpose.</span></span> <span data-ttu-id="e06a9-145">Вместо этого выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e06a9-145">Instead, follow these steps.</span></span>

1. <span data-ttu-id="e06a9-146">Откройте выпущенный продукт.</span><span class="sxs-lookup"><span data-stu-id="e06a9-146">Open a released product.</span></span>
1. <span data-ttu-id="e06a9-147">В области действий на вкладке **Продукт** в группе **Создать** выберите **Шаблон \> Создать общий шаблон**.</span><span class="sxs-lookup"><span data-stu-id="e06a9-147">On the Action Pane, on the **Product** tab, in the **New** group, select **Template \> Create shared template**.</span></span>

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a><span data-ttu-id="e06a9-148">Текст справки по умолчанию, добавляемый в атрибуты продукта, не введен в выпущенный продукт.</span><span class="sxs-lookup"><span data-stu-id="e06a9-148">Default Help text that is added in product attributes isn't entered in a released product.</span></span>

<span data-ttu-id="e06a9-149">Описание и текст справки, добавляемые в атрибуты продукта, не отображаются или не вводятся по умолчанию в выпущенные продукты.</span><span class="sxs-lookup"><span data-stu-id="e06a9-149">A description and Help text that are added in the product attributes aren't visible or entered by default in the released products.</span></span> <span data-ttu-id="e06a9-150">Такое поведение предусмотрено разработчиками.</span><span class="sxs-lookup"><span data-stu-id="e06a9-150">This behavior is by design.</span></span>

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a><span data-ttu-id="e06a9-151">Введенное по умолчанию количество отличается, когда оно регистрируется из спецификации и регистрируется из версии спецификации.</span><span class="sxs-lookup"><span data-stu-id="e06a9-151">The default quantity that is entered differs when it's registered from a BOM and when it's registered from a BOM version.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e06a9-152">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="e06a9-152">Issue description</span></span>

<span data-ttu-id="e06a9-153">По умолчанию при добавлении номенклатуры в спецификацию количество устанавливается равным 1 вместо количества, определенного в поле **Мин. количество по заказу** на странице **Параметры заказа по умолчанию** для выбранного продукта.</span><span class="sxs-lookup"><span data-stu-id="e06a9-153">By default, when you add an item to a BOM, the quantity is set to 1 instead of the quantity that is defined in the **Min. order quantity** field on the **Default order settings** page for a selected product.</span></span> <span data-ttu-id="e06a9-154">Однако если при добавлении номенклатуры из версии спецификации выбрана номенклатура и вариант, количество, введенное по умолчанию, принимает во внимание минимальное количество, которое задается в настройках заказа по умолчанию для определенных аналитик.</span><span class="sxs-lookup"><span data-stu-id="e06a9-154">However, when you add an item from a BOM version, and the item and variant are selected, the quantity that is entered by default takes into account the minimum quantity that is set in the default order settings for the specific dimensions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e06a9-155">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="e06a9-155">Issue resolution</span></span>

<span data-ttu-id="e06a9-156">Это поведение является ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="e06a9-156">This behavior is expected.</span></span> <span data-ttu-id="e06a9-157">Однако тот факт, что логика отличается в спецификации и в версии спецификации, является известной проблемой.</span><span class="sxs-lookup"><span data-stu-id="e06a9-157">However, the fact that the logic differs in the BOM and the BOM version is a known issue.</span></span> <span data-ttu-id="e06a9-158">Тем не менее, такое поведение не изменится, так как изменение может повлиять на многие различные сценарии для клиентов.</span><span class="sxs-lookup"><span data-stu-id="e06a9-158">Nevertheless, this behavior won't be changed, because a change could affect many different customer scenarios.</span></span>

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a><span data-ttu-id="e06a9-159">В выпущенных сведениях о продукте невозможно изменить присоединенные изображения, отправленные из информационного объекта вложений документов продуктов.</span><span class="sxs-lookup"><span data-stu-id="e06a9-159">In the released product details, I can't change the attached images that were uploaded from the Product document attachments data entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e06a9-160">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="e06a9-160">Issue description</span></span>

<span data-ttu-id="e06a9-161">Эта проблема может возникнуть, если изображение прикрепляется к номенклатуре с помощью информационного объекта *Вложения документов продуктов*.</span><span class="sxs-lookup"><span data-stu-id="e06a9-161">This issue can occur when you attach an image to an item by using the *Product document attachments* data entity.</span></span> <span data-ttu-id="e06a9-162">В этом случае изображение номенклатуры отображается для данной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="e06a9-162">In this case, the item image is shown for the item.</span></span> <span data-ttu-id="e06a9-163">Однако если выбрано значение **Изменить изображение**, в списке загруженных изображений ничего не отображается.</span><span class="sxs-lookup"><span data-stu-id="e06a9-163">However, if you select **Change image**, nothing is shown in the list of uploaded images.</span></span> <span data-ttu-id="e06a9-164">Кроме того, для этой номенклатуры не отображаются вложения.</span><span class="sxs-lookup"><span data-stu-id="e06a9-164">Additionally, no attachments are shown for the item.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e06a9-165">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="e06a9-165">Issue resolution</span></span>

<span data-ttu-id="e06a9-166">Сущность *EcoResProductDocumentAttachmentEntity* (*Вложения документов продуктов*) импортирует вложения документов для *продуктов*, но не для *выпущенных продуктов*.</span><span class="sxs-lookup"><span data-stu-id="e06a9-166">The *EcoResProductDocumentAttachmentEntity* entity (*Product document attachments*) imports document attachments for *products* but not for *released products*.</span></span> <span data-ttu-id="e06a9-167">(Выпущенные продукты также называются *номенклатурами*.) Чтобы просмотреть вложения для номенклатуры на странице **Сведения о выпущенных продуктах**, следует использовать сущность *EcoResReleasedProductDocumentAttachmentEntity* (*Вложения документов выпущенных продуктов*) вместо этого.</span><span class="sxs-lookup"><span data-stu-id="e06a9-167">(Released products are also known as *items*.) To view the attachments for an item on the **Released product details** page, you must use the *EcoResReleasedProductDocumentAttachmentEntity* entity (*Released product document attachments*) instead.</span></span>

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a><span data-ttu-id="e06a9-168">Соединитель Microsoft Flow показывает следующее сообщение об ошибке: "Обновление не разрешено для поля ProductNumber."</span><span class="sxs-lookup"><span data-stu-id="e06a9-168">The Microsoft Flow connector shows the following error message: "Update not allowed for field 'ProductNumber'."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e06a9-169">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="e06a9-169">Issue description</span></span>

<span data-ttu-id="e06a9-170">Эта проблема возникает при попытке обновить поле **Номер продукта** с помощью сущности *Выпущенные продукты* версии V2 и Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="e06a9-170">This issue occurs if you try to update the **Product number** field by using the *Released products* entity V2 and Microsoft Flow.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e06a9-171">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="e06a9-171">Issue resolution</span></span>

<span data-ttu-id="e06a9-172">Это поведение является ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="e06a9-172">This behavior is expected.</span></span> <span data-ttu-id="e06a9-173">Возможность редактирования номера продукта для выпущенного продукта была удалена в Dynamics 365 Finance and Operations 10.0.0 с обновлением платформы 24, чтобы предотвратить повреждение данных.</span><span class="sxs-lookup"><span data-stu-id="e06a9-173">The ability to edit the product number for a released product was removed in Dynamics 365 Finance and Operations 10.0.0 with platform update 24 to help prevent data corruption.</span></span> <span data-ttu-id="e06a9-174">В исключительных случаях, когда необходимо восстановить повреждение данных, вызванное предыдущим переименованием первичного ключа выпущенного продукта, вы можете попросить службу поддержки Майкрософт, чтобы временно удалить это ограничение.</span><span class="sxs-lookup"><span data-stu-id="e06a9-174">In exceptional cases, where you must repair data corruption that was caused by a previous rename of the primary key of a released product, you can ask Microsoft Support to temporarily remove this restriction.</span></span>

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a><span data-ttu-id="e06a9-175">Не удается создать вариант выпущенного продукта в другом юридическом лице.</span><span class="sxs-lookup"><span data-stu-id="e06a9-175">I can't create a released product variant in another legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e06a9-176">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="e06a9-176">Issue description</span></span>

<span data-ttu-id="e06a9-177">При попытке выпуска шаблона продукта без вариантов и последующего создания вариантов в каждом юридическом лице (компании), когда они необходимы, вы не сможете выпустить варианты, используя предложения вариантов.</span><span class="sxs-lookup"><span data-stu-id="e06a9-177">If you try to release a product master without variants, and then create the variants in each legal entity (company) as they are required, you won't be able to release the variants by using variant suggestions.</span></span> <span data-ttu-id="e06a9-178">Вы также не сможете создавать варианты вручную.</span><span class="sxs-lookup"><span data-stu-id="e06a9-178">You also won't be able to manually create the variants.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e06a9-179">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="e06a9-179">Issue resolution</span></span>

<span data-ttu-id="e06a9-180">Такое поведение предусмотрено разработчиками.</span><span class="sxs-lookup"><span data-stu-id="e06a9-180">This behavior is by design.</span></span> <span data-ttu-id="e06a9-181">Отношения шаблона продукта и аналитик, которые может принимать шаблон, хранятся на общем уровне.</span><span class="sxs-lookup"><span data-stu-id="e06a9-181">The relations of a product master and the dimensions that the master can take are kept at a shared level.</span></span> <span data-ttu-id="e06a9-182">Таким образом, невозможно создать доступные аналитики для общего шаблона продукта в конкретном юридическом лице, где эти аналитики выпускаются, а затем реплицировать процесс в каждом юридическом лице, где эти аналитики требуются.</span><span class="sxs-lookup"><span data-stu-id="e06a9-182">Therefore, you can't create the available dimensions for a shared product master in the specific legal entity where those dimensions are released and then replicate the process in each legal entity where the dimensions are required.</span></span> <span data-ttu-id="e06a9-183">Вместо этого необходимо изменить процесс выпуска для адаптации к спроектированному процессу.</span><span class="sxs-lookup"><span data-stu-id="e06a9-183">Instead, you must change your release process to adapt to the designed process.</span></span>

<span data-ttu-id="e06a9-184">Ниже приводится процесс выпуска продуктов.</span><span class="sxs-lookup"><span data-stu-id="e06a9-184">Here is the process for releasing products.</span></span>

1. <span data-ttu-id="e06a9-185">Создайте общий шаблон продукта и аналитики, которые могут быть выпущены юридическим лицам.</span><span class="sxs-lookup"><span data-stu-id="e06a9-185">Create the shared product master and the dimensions that can be released to the legal entities.</span></span>
1. <span data-ttu-id="e06a9-186">Выпустите продукты для юридических лиц, используя предложения вариантов или вручную добавляя комбинации, которые должны быть выпущены.</span><span class="sxs-lookup"><span data-stu-id="e06a9-186">Release the products to the legal entities either by using variant suggestions or by manually adding the combinations that should be released.</span></span>

<span data-ttu-id="e06a9-187">Кроме того, можно непосредственно создать выпущенный продукт.</span><span class="sxs-lookup"><span data-stu-id="e06a9-187">Alternatively, you can directly create the released product.</span></span>

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a><span data-ttu-id="e06a9-188">При выпуске варианта в другой компании появляется следующее сообщение об ошибке: "Вариант продукта с указанными аналитиками уже был создан."</span><span class="sxs-lookup"><span data-stu-id="e06a9-188">When I release a variant in another company, I receive the following error message: "Product variant with specified dimensions has already been created."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e06a9-189">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="e06a9-189">Issue description</span></span>

<span data-ttu-id="e06a9-190">Если вариант продукта уже был выпущен в компании A, и вы пытаетесь выпустить его в компании B с помощью кнопки **Создать** на странице **Варианты выпущенного продукта**, появится следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="e06a9-190">If a product variant has already been released in a company A, and you try to release it in company B by using the **New** button on the **Released product variants** page, you will receive the following error message:</span></span>

> <span data-ttu-id="e06a9-191">Вариант продукта с выбранными аналитиками уже создан.</span><span class="sxs-lookup"><span data-stu-id="e06a9-191">Product variant with specified dimensions has already been created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e06a9-192">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="e06a9-192">Issue resolution</span></span>

<span data-ttu-id="e06a9-193">Кнопка **Создать** на странице **Варианты выпущенного продукта** создает вариант и выпускает его в контексте компании.</span><span class="sxs-lookup"><span data-stu-id="e06a9-193">The **New** button on the **Released product variants** page creates the variant and releases it in the company context.</span></span> <span data-ttu-id="e06a9-194">Если этот вариант уже был создан, нельзя использовать кнопку **Создать**, чтобы выпустить его в другой компании.</span><span class="sxs-lookup"><span data-stu-id="e06a9-194">If the variant has already been created, you can't use the **New** button to release it in another company.</span></span>

<span data-ttu-id="e06a9-195">Чтобы исправить ошибку, откройте страницу **Шаблон продукта** и выберите **Выпустить продукт**, чтобы выпустить существующий вариант в нужной компании.</span><span class="sxs-lookup"><span data-stu-id="e06a9-195">To fix the issue, open the **Product master** page, and select **Release product** to release the existing variant in the desired company.</span></span>
