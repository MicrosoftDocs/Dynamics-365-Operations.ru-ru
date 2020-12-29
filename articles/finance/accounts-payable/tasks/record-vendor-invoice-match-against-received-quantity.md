---
title: Регистрация накладной поставщика и сопоставление с полученными количествами
description: При получении накладной от поставщика за товары или услуги по заказу на покупку для бизнес-процессов может потребоваться, чтобы товары или услуги были получены, прежде чем накладная может утверждена для платежа.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa79ab46e9fdc6f8a2b4524d372949314ac2d200
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447146"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a><span data-ttu-id="f47c0-103">Регистрация накладной поставщика и сопоставление с полученными количествами</span><span class="sxs-lookup"><span data-stu-id="f47c0-103">Record vendor invoice and match against received quantity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f47c0-104">При получении накладной от поставщика за товары или услуги по заказу на покупку для бизнес-процессов может потребоваться, чтобы товары или услуги были получены, прежде чем накладная может утверждена для платежа.</span><span class="sxs-lookup"><span data-stu-id="f47c0-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="f47c0-105">Перед началом работы убедитесь, что выбран конфигурационный ключ "Сопоставление накладных".</span><span class="sxs-lookup"><span data-stu-id="f47c0-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="f47c0-106">На странице "Параметры расчетов с поставщиками" убедитесь, что установлен флажок "Включить проверку сопоставления накладных", в поле "Разнести накладную с несоответствиями" задано значение "Требуется утверждение" и в поле "Политика проверки соответствия строк" задано значение "Трехстороннее сопоставление".</span><span class="sxs-lookup"><span data-stu-id="f47c0-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="f47c0-107">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="f47c0-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="f47c0-108">Эти шаги выполняются ролями менеджера по расчету с поставщиками или главного бухгалтера.</span><span class="sxs-lookup"><span data-stu-id="f47c0-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="f47c0-109">Создание заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="f47c0-109">Create a purchase order</span></span>
1. <span data-ttu-id="f47c0-110">Перейдите в раздел "Все заказы на покупку".</span><span class="sxs-lookup"><span data-stu-id="f47c0-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="f47c0-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f47c0-111">Click New.</span></span>
3. <span data-ttu-id="f47c0-112">В поле "Счет поставщика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f47c0-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f47c0-113">В поле "Счет поставщика" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f47c0-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="f47c0-114">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f47c0-114">Click OK.</span></span>
6. <span data-ttu-id="f47c0-115">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="f47c0-115">Click Add line.</span></span>
7. <span data-ttu-id="f47c0-116">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f47c0-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="f47c0-117">В области действий щелкните "Покупка".</span><span class="sxs-lookup"><span data-stu-id="f47c0-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="f47c0-118">Нажмите кнопку "Подтвердить".</span><span class="sxs-lookup"><span data-stu-id="f47c0-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="f47c0-119">Разноска поступления продуктов</span><span class="sxs-lookup"><span data-stu-id="f47c0-119">Post a product receipt</span></span>
1. <span data-ttu-id="f47c0-120">В области действий щелкните "Получение".</span><span class="sxs-lookup"><span data-stu-id="f47c0-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="f47c0-121">Щелкните "Поступление продуктов".</span><span class="sxs-lookup"><span data-stu-id="f47c0-121">Click Product receipt.</span></span>
3. <span data-ttu-id="f47c0-122">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="f47c0-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f47c0-123">В поле "Поступление продуктов" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f47c0-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="f47c0-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f47c0-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="f47c0-125">Регистрация и сопоставление накладной поставщика с поступлением продуктов</span><span class="sxs-lookup"><span data-stu-id="f47c0-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="f47c0-126">В области действий щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="f47c0-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="f47c0-127">Щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="f47c0-127">Click Invoice.</span></span>
3. <span data-ttu-id="f47c0-128">В поле "Число" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f47c0-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="f47c0-129">Щелкните "По умолчанию из: заказанное количество", чтобы открыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f47c0-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="f47c0-130">В поле "Количество по умолчанию для строк" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="f47c0-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="f47c0-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f47c0-131">Click OK.</span></span>
7. <span data-ttu-id="f47c0-132">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="f47c0-132">Click Yes.</span></span>
8. <span data-ttu-id="f47c0-133">Щелкните "Сопоставить поступления продуктов".</span><span class="sxs-lookup"><span data-stu-id="f47c0-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="f47c0-134">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f47c0-134">Click OK.</span></span>
10. <span data-ttu-id="f47c0-135">В области действий щелкните "Просмотр".</span><span class="sxs-lookup"><span data-stu-id="f47c0-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="f47c0-136">Щелкните "Сведения о сопоставлении".</span><span class="sxs-lookup"><span data-stu-id="f47c0-136">Click Matching details.</span></span>

