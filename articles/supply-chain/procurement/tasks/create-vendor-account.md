---
title: Создание счета поставщика
description: В этой процедуре показано, как создать счет поставщика и добавить адрес и контактную информацию.
author: mkirknel
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba585a9bb1a296bbf7181530e151d737bfa22fc2
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149604"
---
# <a name="create-a-vendor-account"></a><span data-ttu-id="d98f2-103">Создание счета поставщика</span><span class="sxs-lookup"><span data-stu-id="d98f2-103">Create a vendor account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d98f2-104">В этой процедуре показано, как создать счет поставщика и добавить адрес и контактную информацию.</span><span class="sxs-lookup"><span data-stu-id="d98f2-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="d98f2-105">В процедуре не показано, как заполнять все поля, связанные с закупками и финансами.</span><span class="sxs-lookup"><span data-stu-id="d98f2-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="d98f2-106">Для получения дополнительных сведений об этих полях прочитайте описания полей.</span><span class="sxs-lookup"><span data-stu-id="d98f2-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="d98f2-107">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="d98f2-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="d98f2-108">Счета поставщиков обычно создаются специалистом по закупкам или сотрудниками отдела расчетов с клиентами.</span><span class="sxs-lookup"><span data-stu-id="d98f2-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="d98f2-109">Создание счета поставщика</span><span class="sxs-lookup"><span data-stu-id="d98f2-109">Create a vendor account</span></span>
1. <span data-ttu-id="d98f2-110">Выберите **Область переходов > Модули > Закупки и источники > Поставщики > Все поставщики**.</span><span class="sxs-lookup"><span data-stu-id="d98f2-110">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="d98f2-111">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d98f2-111">Click **New**.</span></span>
3. <span data-ttu-id="d98f2-112">В поле **Счет поставщика** введите значение.</span><span class="sxs-lookup"><span data-stu-id="d98f2-112">In the **Vendor account** field, type a value.</span></span>
    - <span data-ttu-id="d98f2-113">Значение может быть введено автоматически.</span><span class="sxs-lookup"><span data-stu-id="d98f2-113">The value may be populated automatically.</span></span> <span data-ttu-id="d98f2-114">В таком случае этот шаг можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="d98f2-114">If so, you can skip this step.</span></span>  
    - <span data-ttu-id="d98f2-115">Создавать счета поставщиков можно для физических лиц или для организаций.</span><span class="sxs-lookup"><span data-stu-id="d98f2-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="d98f2-116">От этого зависит набор доступных полей.</span><span class="sxs-lookup"><span data-stu-id="d98f2-116">This will affect which fields are available.</span></span> <span data-ttu-id="d98f2-117">В этом примере мы создадим счет поставщика для организации.</span><span class="sxs-lookup"><span data-stu-id="d98f2-117">In this example, we'll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="d98f2-118">В поле **Имя** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d98f2-118">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="d98f2-119">Если поставщик уже зарегистрирован в системе, можно с помощью раскрывающегося списка выбрать его в этом поле, и новый счет поставщика будет наследовать уже зарегистрированные адрес и контактную информацию.</span><span class="sxs-lookup"><span data-stu-id="d98f2-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that's already registered.</span></span>
5. <span data-ttu-id="d98f2-120">В поле **Группа** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d98f2-120">In the **Group** field, enter or select a value.</span></span> <span data-ttu-id="d98f2-121">Группа поставщиков используется для группирования поставщиков по какому-либо из следующих параметров: условия оплаты; период сопоставления; счета ГК для разноски запасов, включая налоговую группу; счета ГК по умолчанию; коды фильтров продуктов и конфигурация прогноза поставки.</span><span class="sxs-lookup"><span data-stu-id="d98f2-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment, settle period, inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>
6. <span data-ttu-id="d98f2-122">В поле **Число сотрудников** введите число.</span><span class="sxs-lookup"><span data-stu-id="d98f2-122">In the **Number of employees** field, enter a number.</span></span>
7. <span data-ttu-id="d98f2-123">В поле **Номер организации** введите значение.</span><span class="sxs-lookup"><span data-stu-id="d98f2-123">In the **Organization number** field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="d98f2-124">Добавление адреса</span><span class="sxs-lookup"><span data-stu-id="d98f2-124">Add an address</span></span>
1. <span data-ttu-id="d98f2-125">Разверните раздел **Адреса**.</span><span class="sxs-lookup"><span data-stu-id="d98f2-125">Expand the **Addresses** section.</span></span>
2. <span data-ttu-id="d98f2-126">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="d98f2-126">Click **Add**.</span></span>
3. <span data-ttu-id="d98f2-127">В поле **Цель** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d98f2-127">In the **Purpose** field, enter or select a value.</span></span> <span data-ttu-id="d98f2-128">Можно выбрать одну или несколько целей.</span><span class="sxs-lookup"><span data-stu-id="d98f2-128">You can select one or more purposes.</span></span> <span data-ttu-id="d98f2-129">Они используются для выбора правильного адреса для определенной цели.</span><span class="sxs-lookup"><span data-stu-id="d98f2-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="d98f2-130">Например, если цель — "Накладная", этот адрес будет использоваться при отправке накладных.</span><span class="sxs-lookup"><span data-stu-id="d98f2-130">For example, if the purpose is "Invoice" that address will be used when you send invoices.</span></span>
4. <span data-ttu-id="d98f2-131">В поле **Имя или описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="d98f2-131">In the **Name or description** field, type a value.</span></span>
5. <span data-ttu-id="d98f2-132">В поле **Страна/регион** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d98f2-132">In the **Country/region** field, enter or select a value.</span></span> <span data-ttu-id="d98f2-133">Введите информацию об адресе.</span><span class="sxs-lookup"><span data-stu-id="d98f2-133">Enter the address details.</span></span> <span data-ttu-id="d98f2-134">Выбранные страна/регион определяют поля, которые вам необходимо заполнить, в соответствии с форматом адреса в этой стране/регионе.</span><span class="sxs-lookup"><span data-stu-id="d98f2-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span> 
6. <span data-ttu-id="d98f2-135">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="d98f2-135">Click **OK**.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="d98f2-136">Добавление контактной информации</span><span class="sxs-lookup"><span data-stu-id="d98f2-136">Add contact information</span></span>
1. <span data-ttu-id="d98f2-137">Разверните раздел **Контактная информация**.</span><span class="sxs-lookup"><span data-stu-id="d98f2-137">Expand the **Contact information** section.</span></span>
2. <span data-ttu-id="d98f2-138">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="d98f2-138">Click **Add**.</span></span>
3. <span data-ttu-id="d98f2-139">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="d98f2-139">In the **Description** field, type a value.</span></span>
4. <span data-ttu-id="d98f2-140">В поле **Тип** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="d98f2-140">In the **Type** field, select an option.</span></span>
5. <span data-ttu-id="d98f2-141">В поле **Номер/адрес контактного лица** введите значение.</span><span class="sxs-lookup"><span data-stu-id="d98f2-141">In the **Contact number/address** field, type a value.</span></span> <span data-ttu-id="d98f2-142">Установите флажок "Основной", если это основной контакт.</span><span class="sxs-lookup"><span data-stu-id="d98f2-142">You can select the Primary check box if this is the primary contact.</span></span>  
6. <span data-ttu-id="d98f2-143">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d98f2-143">Click **Save**.</span></span>
7. <span data-ttu-id="d98f2-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d98f2-144">Close the page.</span></span>
8. <span data-ttu-id="d98f2-145">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d98f2-145">Close the page.</span></span>

