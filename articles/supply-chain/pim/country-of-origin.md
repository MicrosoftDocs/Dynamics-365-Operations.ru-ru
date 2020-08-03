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
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fd234c57bf9893e9b8bcfa5ada7439a642f7a288
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596270"
---
# <a name="country-of-origin"></a><span data-ttu-id="cd472-105">Страна происхождения</span><span class="sxs-lookup"><span data-stu-id="cd472-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd472-106">Многие организации выдают сертификаты своим поставщикам, чтобы гарантировать соответствие продуктов конкретным стандартам сертификации.</span><span class="sxs-lookup"><span data-stu-id="cd472-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="cd472-107">Эти сертификаты часто зависят от страны происхождения.</span><span class="sxs-lookup"><span data-stu-id="cd472-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="cd472-108">Функция страны происхождения позволяет связать продукт с его страной происхождения и отслеживать сертификаты продуктов.</span><span class="sxs-lookup"><span data-stu-id="cd472-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="cd472-109">Настройка исходных и конечных стран</span><span class="sxs-lookup"><span data-stu-id="cd472-109">Configure source and destination countries</span></span>

<span data-ttu-id="cd472-110">Перед выпуском сертификата для продукта необходимо связать продукт с соответствующей страной назначения и его страной происхождения.</span><span class="sxs-lookup"><span data-stu-id="cd472-110">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="cd472-111">Перейдите к пункту **Управление сведениями о продукте \> Настройка \> Соответствие продуктов \> Страна происхождения \> Правила страны происхождения**.</span><span class="sxs-lookup"><span data-stu-id="cd472-111">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="cd472-112">Выберите существующую настройку страны для редактирования или выберите **Создать** на панели операций, чтобы создать новую настройку страны.</span><span class="sxs-lookup"><span data-stu-id="cd472-112">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="cd472-113">Задайте следующие значения для выбранной или новой страны.</span><span class="sxs-lookup"><span data-stu-id="cd472-113">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="cd472-114">Поле</span><span class="sxs-lookup"><span data-stu-id="cd472-114">Field</span></span> | <span data-ttu-id="cd472-115">описание</span><span class="sxs-lookup"><span data-stu-id="cd472-115">Description</span></span> |
    |---|---|
    | <span data-ttu-id="cd472-116">Код номенклатуры</span><span class="sxs-lookup"><span data-stu-id="cd472-116">Item number</span></span> | <span data-ttu-id="cd472-117">Выберите код номенклатуры для продукта.</span><span class="sxs-lookup"><span data-stu-id="cd472-117">Select the item number of the product.</span></span> |
    | <span data-ttu-id="cd472-118">Страна/регион места назначения</span><span class="sxs-lookup"><span data-stu-id="cd472-118">Destination country</span></span> | <span data-ttu-id="cd472-119">Выберите страну, в которую вы отправляете продукт.</span><span class="sxs-lookup"><span data-stu-id="cd472-119">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="cd472-120">Страна происхождения</span><span class="sxs-lookup"><span data-stu-id="cd472-120">Origin country</span></span> | <span data-ttu-id="cd472-121">Выберите страну, из которой вы доставляете продукт.</span><span class="sxs-lookup"><span data-stu-id="cd472-121">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="cd472-122">Цель этой настройки — помочь в создании отчета по спецификации (BOM), в котором можно включить страну происхождения для каждой части, для которой указаны страны происхождения и назначения.</span><span class="sxs-lookup"><span data-stu-id="cd472-122">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="cd472-123">Этот отчет поможет получить целостную картину, откуда поступают части и куда они отправляются.</span><span class="sxs-lookup"><span data-stu-id="cd472-123">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="cd472-124">Отслеживание сертификатов поставщиков</span><span class="sxs-lookup"><span data-stu-id="cd472-124">Keep track of vendor certificates</span></span>

<span data-ttu-id="cd472-125">Можно использовать страницу **Сертификаты поставщиков страницы происхождения** для отслеживания сертификатов, выданных поставщикам.</span><span class="sxs-lookup"><span data-stu-id="cd472-125">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="cd472-126">Необходимо решить, какие документы сертификатов вы выдаете и как они будут предоставляться клиентам.</span><span class="sxs-lookup"><span data-stu-id="cd472-126">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="cd472-127">Эта функция помогает отслеживать ваши сертификаты.</span><span class="sxs-lookup"><span data-stu-id="cd472-127">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="cd472-128">Она также позволяет выбрать, будут ли соответствующие номера сертификатов отображаться в накладных, отборочных накладных и/или подтверждениях заказов.</span><span class="sxs-lookup"><span data-stu-id="cd472-128">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="cd472-129">Для настройки сведений о ваших сертификатах выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cd472-129">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="cd472-130">Перейдите к пункту **Управление сведениями о продукте \> Настройка \> Соответствие продуктов \> Страна происхождения \> Сертификаты поставщика страны происхождения**.</span><span class="sxs-lookup"><span data-stu-id="cd472-130">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="cd472-131">Выберите существующую настройку сертификата для редактирования или выберите **Создать** на панели операций, чтобы создать новую настройку сертификата.</span><span class="sxs-lookup"><span data-stu-id="cd472-131">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="cd472-132">Задайте следующие настройки для выбранного или нового сертификата.</span><span class="sxs-lookup"><span data-stu-id="cd472-132">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="cd472-133">Поле</span><span class="sxs-lookup"><span data-stu-id="cd472-133">Field</span></span> | <span data-ttu-id="cd472-134">описание</span><span class="sxs-lookup"><span data-stu-id="cd472-134">Description</span></span> |
    |---|---|
    | <span data-ttu-id="cd472-135">Счет поставщика</span><span class="sxs-lookup"><span data-stu-id="cd472-135">Vendor account</span></span> | <span data-ttu-id="cd472-136">Выберите поставщика, для которого выдан сертификат.</span><span class="sxs-lookup"><span data-stu-id="cd472-136">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="cd472-137">Код номенклатуры</span><span class="sxs-lookup"><span data-stu-id="cd472-137">Item number</span></span> | <span data-ttu-id="cd472-138">Выберите номенклатуру, для которой выдан сертификат.</span><span class="sxs-lookup"><span data-stu-id="cd472-138">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="cd472-139">Страна/регион</span><span class="sxs-lookup"><span data-stu-id="cd472-139">Country/region</span></span> | <span data-ttu-id="cd472-140">Страна или регион назначения, для которых необходимо использовать этот сертификат.</span><span class="sxs-lookup"><span data-stu-id="cd472-140">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="cd472-141">Номер сертификата</span><span class="sxs-lookup"><span data-stu-id="cd472-141">Certificate number</span></span> | <span data-ttu-id="cd472-142">Введите идентификационный номер выданного сертификата.</span><span class="sxs-lookup"><span data-stu-id="cd472-142">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="cd472-143">Действует</span><span class="sxs-lookup"><span data-stu-id="cd472-143">Effective</span></span> | <span data-ttu-id="cd472-144">Выберите первую дату, когда текущий сертификат действителен.</span><span class="sxs-lookup"><span data-stu-id="cd472-144">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="cd472-145">Истечение срока действия</span><span class="sxs-lookup"><span data-stu-id="cd472-145">Expiration</span></span> | <span data-ttu-id="cd472-146">Выберите последнюю дату, когда текущий сертификат действителен.</span><span class="sxs-lookup"><span data-stu-id="cd472-146">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="cd472-147">Печать на счете</span><span class="sxs-lookup"><span data-stu-id="cd472-147">Print on invoice</span></span> | <span data-ttu-id="cd472-148">Установите этот флажок для печати номера сертификата на счетах, адресованных в указанную страну в указанном диапазоне дат.</span><span class="sxs-lookup"><span data-stu-id="cd472-148">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="cd472-149">Печать на отборочной накладной</span><span class="sxs-lookup"><span data-stu-id="cd472-149">Print on packing slip</span></span> | <span data-ttu-id="cd472-150">Установите этот флажок для печати номера сертификата на отборочных накладных, адресованных в указанную страну в указанном диапазоне дат.</span><span class="sxs-lookup"><span data-stu-id="cd472-150">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="cd472-151">Печать на заказе на продажу</span><span class="sxs-lookup"><span data-stu-id="cd472-151">Print on sales order</span></span> | <span data-ttu-id="cd472-152">Установите этот флажок для печати номера сертификата на заказах на продажу, адресованных в указанную страну в указанном диапазоне дат.</span><span class="sxs-lookup"><span data-stu-id="cd472-152">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="cd472-153">Включение страны происхождения в отчеты по спецификации</span><span class="sxs-lookup"><span data-stu-id="cd472-153">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="cd472-154">При создании отчета по спецификации можно включить страну происхождения для каждой части, для которой были указаны исходная и конечная страны, на странице **Правила страны происхождения**.</span><span class="sxs-lookup"><span data-stu-id="cd472-154">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="cd472-155">Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="cd472-155">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="cd472-156">Выберите или создайте продукт, чтобы открыть его страницу **Сведения о выпущенном продукте**.</span><span class="sxs-lookup"><span data-stu-id="cd472-156">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="cd472-157">В области действий на вкладке **Инженер** в группе **Спецификации** выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="cd472-157">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="cd472-158">На открывшейся странице списка в области операций выберите **Спецификация \> Печать**.</span><span class="sxs-lookup"><span data-stu-id="cd472-158">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="cd472-159">В диалоговом окне **Строки спецификации** задайте в поле **Страна назначения** страну назначения, которую необходимо просмотреть в отчете.</span><span class="sxs-lookup"><span data-stu-id="cd472-159">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="cd472-160">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="cd472-160">Select **OK**.</span></span>

<span data-ttu-id="cd472-161">Создается и отображается отчет, содержащий информацию о стране происхождения для каждой части.</span><span class="sxs-lookup"><span data-stu-id="cd472-161">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="cd472-162">Ниже приведен пример отчета.</span><span class="sxs-lookup"><span data-stu-id="cd472-162">Here is an example of the report.</span></span>

<span data-ttu-id="cd472-163">![Отчет о стране происхождения](media/country-of-origin-report.png "Отчет о стране происхождения")</span><span class="sxs-lookup"><span data-stu-id="cd472-163">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
