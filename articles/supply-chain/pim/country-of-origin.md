---
title: Страна происхождения
description: Многие организации выдают сертификаты своим поставщикам, чтобы гарантировать соответствие продуктов конкретным стандартам сертификации. Эти сертификаты часто зависят от страны происхождения. В этом разделе приводятся сведения о функции страны происхождения, которая позволяет связать продукт с его страной происхождения и отслеживать сертификаты продуктов.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: bb35770f32c21a685b21a41dc7c369ee01fe3891
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243305"
---
# <a name="country-of-origin"></a><span data-ttu-id="e393a-105">Страна происхождения</span><span class="sxs-lookup"><span data-stu-id="e393a-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e393a-106">Многие организации выдают сертификаты своим поставщикам, чтобы гарантировать соответствие продуктов конкретным стандартам сертификации.</span><span class="sxs-lookup"><span data-stu-id="e393a-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="e393a-107">Эти сертификаты часто зависят от страны происхождения.</span><span class="sxs-lookup"><span data-stu-id="e393a-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="e393a-108">Функция страны происхождения позволяет связать продукт с его страной происхождения и отслеживать сертификаты продуктов.</span><span class="sxs-lookup"><span data-stu-id="e393a-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="turn-on-the-country-of-origin-feature"></a><span data-ttu-id="e393a-109">Включение функции страны происхождения</span><span class="sxs-lookup"><span data-stu-id="e393a-109">Turn on the country of origin feature</span></span>

<span data-ttu-id="e393a-110">Прежде чем использовать эту функцию, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="e393a-110">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="e393a-111">Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения.</span><span class="sxs-lookup"><span data-stu-id="e393a-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="e393a-112">В рабочей области **Управление функциями** эта функция перечисляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="e393a-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e393a-113">**Модуль:** *Управление сведениями о продукте*</span><span class="sxs-lookup"><span data-stu-id="e393a-113">**Module:** *Product information management*</span></span>
- <span data-ttu-id="e393a-114">**Название функции:** *Функция управления страной происхождения*</span><span class="sxs-lookup"><span data-stu-id="e393a-114">**Feature name:** *Country of origin management feature*</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="e393a-115">Настройка исходных и конечных стран</span><span class="sxs-lookup"><span data-stu-id="e393a-115">Configure source and destination countries</span></span>

<span data-ttu-id="e393a-116">Перед выпуском сертификата для продукта необходимо связать продукт с соответствующей страной назначения и его страной происхождения.</span><span class="sxs-lookup"><span data-stu-id="e393a-116">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="e393a-117">Перейдите к пункту **Управление сведениями о продукте \> Настройка \> Соответствие продуктов \> Страна происхождения \> Правила страны происхождения**.</span><span class="sxs-lookup"><span data-stu-id="e393a-117">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="e393a-118">Выберите существующую настройку страны для редактирования или выберите **Создать** на панели операций, чтобы создать новую настройку страны.</span><span class="sxs-lookup"><span data-stu-id="e393a-118">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="e393a-119">Задайте следующие значения для выбранной или новой страны.</span><span class="sxs-lookup"><span data-stu-id="e393a-119">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="e393a-120">Поле</span><span class="sxs-lookup"><span data-stu-id="e393a-120">Field</span></span> | <span data-ttu-id="e393a-121">описание</span><span class="sxs-lookup"><span data-stu-id="e393a-121">Description</span></span> |
    |---|---|
    | <span data-ttu-id="e393a-122">Код номенклатуры</span><span class="sxs-lookup"><span data-stu-id="e393a-122">Item number</span></span> | <span data-ttu-id="e393a-123">Выберите код номенклатуры для продукта.</span><span class="sxs-lookup"><span data-stu-id="e393a-123">Select the item number of the product.</span></span> |
    | <span data-ttu-id="e393a-124">Страна/регион места назначения</span><span class="sxs-lookup"><span data-stu-id="e393a-124">Destination country</span></span> | <span data-ttu-id="e393a-125">Выберите страну, в которую вы отправляете продукт.</span><span class="sxs-lookup"><span data-stu-id="e393a-125">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="e393a-126">Страна происхождения</span><span class="sxs-lookup"><span data-stu-id="e393a-126">Origin country</span></span> | <span data-ttu-id="e393a-127">Выберите страну, из которой вы доставляете продукт.</span><span class="sxs-lookup"><span data-stu-id="e393a-127">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="e393a-128">Цель этой настройки — помочь в создании отчета по спецификации (BOM), в котором можно включить страну происхождения для каждой части, для которой указаны страны происхождения и назначения.</span><span class="sxs-lookup"><span data-stu-id="e393a-128">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="e393a-129">Этот отчет поможет получить целостную картину, откуда поступают части и куда они отправляются.</span><span class="sxs-lookup"><span data-stu-id="e393a-129">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="e393a-130">Отслеживание сертификатов поставщиков</span><span class="sxs-lookup"><span data-stu-id="e393a-130">Keep track of vendor certificates</span></span>

<span data-ttu-id="e393a-131">Можно использовать страницу **Сертификаты поставщиков страницы происхождения** для отслеживания сертификатов, выданных поставщикам.</span><span class="sxs-lookup"><span data-stu-id="e393a-131">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="e393a-132">Необходимо решить, какие документы сертификатов вы выдаете и как они будут предоставляться клиентам.</span><span class="sxs-lookup"><span data-stu-id="e393a-132">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="e393a-133">Эта функция помогает отслеживать ваши сертификаты.</span><span class="sxs-lookup"><span data-stu-id="e393a-133">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="e393a-134">Она также позволяет выбрать, будут ли соответствующие номера сертификатов отображаться в накладных, отборочных накладных и/или подтверждениях заказов.</span><span class="sxs-lookup"><span data-stu-id="e393a-134">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="e393a-135">Для настройки сведений о ваших сертификатах выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e393a-135">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="e393a-136">Перейдите к пункту **Управление сведениями о продукте \> Настройка \> Соответствие продуктов \> Страна происхождения \> Сертификаты поставщика страны происхождения**.</span><span class="sxs-lookup"><span data-stu-id="e393a-136">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="e393a-137">Выберите существующую настройку сертификата для редактирования или выберите **Создать** на панели операций, чтобы создать новую настройку сертификата.</span><span class="sxs-lookup"><span data-stu-id="e393a-137">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="e393a-138">Задайте следующие настройки для выбранного или нового сертификата.</span><span class="sxs-lookup"><span data-stu-id="e393a-138">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="e393a-139">Поле</span><span class="sxs-lookup"><span data-stu-id="e393a-139">Field</span></span> | <span data-ttu-id="e393a-140">описание</span><span class="sxs-lookup"><span data-stu-id="e393a-140">Description</span></span> |
    |---|---|
    | <span data-ttu-id="e393a-141">Счет поставщика</span><span class="sxs-lookup"><span data-stu-id="e393a-141">Vendor account</span></span> | <span data-ttu-id="e393a-142">Выберите поставщика, для которого выдан сертификат.</span><span class="sxs-lookup"><span data-stu-id="e393a-142">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="e393a-143">Код номенклатуры</span><span class="sxs-lookup"><span data-stu-id="e393a-143">Item number</span></span> | <span data-ttu-id="e393a-144">Выберите номенклатуру, для которой выдан сертификат.</span><span class="sxs-lookup"><span data-stu-id="e393a-144">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="e393a-145">Страна/регион</span><span class="sxs-lookup"><span data-stu-id="e393a-145">Country/region</span></span> | <span data-ttu-id="e393a-146">Страна или регион назначения, для которых необходимо использовать этот сертификат.</span><span class="sxs-lookup"><span data-stu-id="e393a-146">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="e393a-147">Номер сертификата</span><span class="sxs-lookup"><span data-stu-id="e393a-147">Certificate number</span></span> | <span data-ttu-id="e393a-148">Введите идентификационный номер выданного сертификата.</span><span class="sxs-lookup"><span data-stu-id="e393a-148">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="e393a-149">Действует</span><span class="sxs-lookup"><span data-stu-id="e393a-149">Effective</span></span> | <span data-ttu-id="e393a-150">Выберите первую дату, когда текущий сертификат действителен.</span><span class="sxs-lookup"><span data-stu-id="e393a-150">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="e393a-151">Истечение срока действия</span><span class="sxs-lookup"><span data-stu-id="e393a-151">Expiration</span></span> | <span data-ttu-id="e393a-152">Выберите последнюю дату, когда текущий сертификат действителен.</span><span class="sxs-lookup"><span data-stu-id="e393a-152">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="e393a-153">Печать на счете</span><span class="sxs-lookup"><span data-stu-id="e393a-153">Print on invoice</span></span> | <span data-ttu-id="e393a-154">Установите этот флажок для печати номера сертификата на счетах, адресованных в указанную страну в указанном диапазоне дат.</span><span class="sxs-lookup"><span data-stu-id="e393a-154">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="e393a-155">Печать на отборочной накладной</span><span class="sxs-lookup"><span data-stu-id="e393a-155">Print on packing slip</span></span> | <span data-ttu-id="e393a-156">Установите этот флажок для печати номера сертификата на отборочных накладных, адресованных в указанную страну в указанном диапазоне дат.</span><span class="sxs-lookup"><span data-stu-id="e393a-156">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="e393a-157">Печать на заказе на продажу</span><span class="sxs-lookup"><span data-stu-id="e393a-157">Print on sales order</span></span> | <span data-ttu-id="e393a-158">Установите этот флажок для печати номера сертификата на заказах на продажу, адресованных в указанную страну в указанном диапазоне дат.</span><span class="sxs-lookup"><span data-stu-id="e393a-158">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="e393a-159">Включение страны происхождения в отчеты по спецификации</span><span class="sxs-lookup"><span data-stu-id="e393a-159">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="e393a-160">При создании отчета по спецификации можно включить страну происхождения для каждой части, для которой были указаны исходная и конечная страны, на странице **Правила страны происхождения**.</span><span class="sxs-lookup"><span data-stu-id="e393a-160">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="e393a-161">Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="e393a-161">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="e393a-162">Выберите или создайте продукт, чтобы открыть его страницу **Сведения о выпущенном продукте**.</span><span class="sxs-lookup"><span data-stu-id="e393a-162">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="e393a-163">В области действий на вкладке **Инженер** в группе **Спецификации** выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="e393a-163">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="e393a-164">На открывшейся странице списка в области операций выберите **Спецификация \> Печать**.</span><span class="sxs-lookup"><span data-stu-id="e393a-164">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="e393a-165">В диалоговом окне **Строки спецификации** задайте в поле **Страна назначения** страну назначения, которую необходимо просмотреть в отчете.</span><span class="sxs-lookup"><span data-stu-id="e393a-165">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="e393a-166">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e393a-166">Select **OK**.</span></span>

<span data-ttu-id="e393a-167">Создается и отображается отчет, содержащий информацию о стране происхождения для каждой части.</span><span class="sxs-lookup"><span data-stu-id="e393a-167">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="e393a-168">Ниже приведен пример отчета.</span><span class="sxs-lookup"><span data-stu-id="e393a-168">Here is an example of the report.</span></span>

<span data-ttu-id="e393a-169">![Отчет о стране происхождения](media/country-of-origin-report.png "Отчет о стране происхождения")</span><span class="sxs-lookup"><span data-stu-id="e393a-169">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]