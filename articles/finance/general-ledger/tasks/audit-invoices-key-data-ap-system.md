---
title: Аудит накладных и ключевых данных в модуле расчетов с поставщиками
description: Эта тема показывает, как выполнять аудит накладных и ключевых данных в модуле расчетов с поставщиками.
author: saraschi2
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
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5bb89f0adce41b045b1f573c4c0e841f78b2248c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447085"
---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a><span data-ttu-id="035ff-103">Аудит накладных и ключевых данных в модуле расчетов с поставщиками</span><span class="sxs-lookup"><span data-stu-id="035ff-103">Audit invoices and key data in accounts payable</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="035ff-104">При получении накладной от поставщика за товары или услуги по заказу на покупку для бизнес-процессов может потребоваться, чтобы товары или услуги были получены, прежде чем накладная может утверждена для платежа.</span><span class="sxs-lookup"><span data-stu-id="035ff-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="035ff-105">Перед началом работы убедитесь, что выбран конфигурационный ключ "Сопоставление накладных".</span><span class="sxs-lookup"><span data-stu-id="035ff-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="035ff-106">На странице **Параметры расчетов с поставщиками** убедитесь, что установлен флажок "Включить проверку сопоставления накладных", в поле **Разнести накладную с несоответствиями** задано значение **Требуется утверждение** и в поле **Политика проверки соответствия строк** задано значение **Трехстороннее сопоставление**.</span><span class="sxs-lookup"><span data-stu-id="035ff-106">In the **Accounts payable parameters** page, ensure that the Enable invoice matching validation option is selected, the **Post invoice with discrepancies** field is set to **Require approval**, and the **Line matching policy** field is set to **Three-way matching**.</span></span>

<span data-ttu-id="035ff-107">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="035ff-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="035ff-108">Эти шаги выполняются ролями менеджера по расчету с поставщиками или главного бухгалтера.</span><span class="sxs-lookup"><span data-stu-id="035ff-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="035ff-109">Создание заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="035ff-109">Create a purchase order</span></span>
1. <span data-ttu-id="035ff-110">Перейдите в раздел **Все заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="035ff-110">Go to **All purchase orders**.</span></span>
2. <span data-ttu-id="035ff-111">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="035ff-111">Click **New**.</span></span>
3. <span data-ttu-id="035ff-112">В поле **Счет поставщика** введите значение.</span><span class="sxs-lookup"><span data-stu-id="035ff-112">In the **Vendor account** field, type a value.</span></span>
4. <span data-ttu-id="035ff-113">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="035ff-113">Click **OK**.</span></span>
5. <span data-ttu-id="035ff-114">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="035ff-114">Click **Add line**.</span></span>
6. <span data-ttu-id="035ff-115">В поле **Код номенклатуры** введите значение.</span><span class="sxs-lookup"><span data-stu-id="035ff-115">In the **Item number** field, type a value.</span></span>
7. <span data-ttu-id="035ff-116">В области действий щелкните **Покупка**.</span><span class="sxs-lookup"><span data-stu-id="035ff-116">On the Action Pane, click **Purchase**.</span></span>
8. <span data-ttu-id="035ff-117">Нажмите кнопку **Подтвердить**.</span><span class="sxs-lookup"><span data-stu-id="035ff-117">Click **Confirm**.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="035ff-118">Разноска поступления продуктов</span><span class="sxs-lookup"><span data-stu-id="035ff-118">Post a product receipt</span></span>
1. <span data-ttu-id="035ff-119">В области действий щелкните **Получить**.</span><span class="sxs-lookup"><span data-stu-id="035ff-119">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="035ff-120">Щелкните **Поступление продуктов**.</span><span class="sxs-lookup"><span data-stu-id="035ff-120">Click **Product receipt**.</span></span>
3. <span data-ttu-id="035ff-121">В поле **Поступление продуктов** введите значение.</span><span class="sxs-lookup"><span data-stu-id="035ff-121">In the **Product receipt** field, type a value.</span></span>
4. <span data-ttu-id="035ff-122">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="035ff-122">Click **OK**.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="035ff-123">Регистрация и сопоставление накладной поставщика с поступлением продуктов</span><span class="sxs-lookup"><span data-stu-id="035ff-123">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="035ff-124">В области действий щелкните **Накладная > Накладная**.</span><span class="sxs-lookup"><span data-stu-id="035ff-124">On the Action Pane, click **Invoice > Invoice**.</span></span>
2. <span data-ttu-id="035ff-125">В поле **Число** введите значение.</span><span class="sxs-lookup"><span data-stu-id="035ff-125">In the **Number** field, type a value.</span></span>
3. <span data-ttu-id="035ff-126">Щелкните **По умолчанию из: заказанное количество**, чтобы открыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="035ff-126">Click **Default from: Ordered quantity** to open the drop dialog.</span></span>
4. <span data-ttu-id="035ff-127">В поле **Количество по умолчанию для строк** выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="035ff-127">In the **Default quantity for lines** field, select an option.</span></span>
5. <span data-ttu-id="035ff-128">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="035ff-128">Click **OK**.</span></span>
6. <span data-ttu-id="035ff-129">Нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="035ff-129">Click **Yes**.</span></span>
7. <span data-ttu-id="035ff-130">Щелкните **Сопоставить поступления продуктов**.</span><span class="sxs-lookup"><span data-stu-id="035ff-130">Click **Match product receipts**.</span></span>
8. <span data-ttu-id="035ff-131">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="035ff-131">Click **OK**.</span></span>
9. <span data-ttu-id="035ff-132">В области действий щелкните **Просмотр**.</span><span class="sxs-lookup"><span data-stu-id="035ff-132">On the Action Pane, click **Review**.</span></span>
10. <span data-ttu-id="035ff-133">Щелкните **Сведения о сопоставлении**.</span><span class="sxs-lookup"><span data-stu-id="035ff-133">Click **Matching details**.</span></span>

