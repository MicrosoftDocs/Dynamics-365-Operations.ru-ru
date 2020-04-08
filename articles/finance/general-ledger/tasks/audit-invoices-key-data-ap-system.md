---
title: Аудит накладных и ключевых данных в системе расчетов с поставщиками
description: При получении накладной от поставщика за товары или услуги по заказу на покупку для бизнес-процессов может потребоваться, чтобы товары или услуги были получены, прежде чем накладная может утверждена для платежа.
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
ms.openlocfilehash: 6e1af0dac107be6009eb3ca576c49ac5abbd9848
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139952"
---
# <a name="audit-invoices-and-key-data-in-ap-system"></a><span data-ttu-id="676ee-103">Аудит накладных и ключевых данных в системе расчетов с поставщиками</span><span class="sxs-lookup"><span data-stu-id="676ee-103">Audit invoices and key data in AP system</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="676ee-104">При получении накладной от поставщика за товары или услуги по заказу на покупку для бизнес-процессов может потребоваться, чтобы товары или услуги были получены, прежде чем накладная может утверждена для платежа.</span><span class="sxs-lookup"><span data-stu-id="676ee-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="676ee-105">Перед началом работы убедитесь, что выбран конфигурационный ключ "Сопоставление накладных".</span><span class="sxs-lookup"><span data-stu-id="676ee-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="676ee-106">На странице "Параметры расчетов с поставщиками" убедитесь, что установлен флажок "Включить проверку сопоставления накладных", в поле "Разнести накладную с несоответствиями" задано значение "Требуется утверждение" и в поле "Политика проверки соответствия строк" задано значение "Трехстороннее сопоставление".</span><span class="sxs-lookup"><span data-stu-id="676ee-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="676ee-107">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="676ee-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="676ee-108">Эти шаги выполняются ролями менеджера по расчету с поставщиками или главного бухгалтера.</span><span class="sxs-lookup"><span data-stu-id="676ee-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="676ee-109">Создание заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="676ee-109">Create a purchase order</span></span>
1. <span data-ttu-id="676ee-110">Перейдите в раздел **Все заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="676ee-110">Go to **All purchase orders**.</span></span>
2. <span data-ttu-id="676ee-111">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="676ee-111">Click **New**.</span></span>
3. <span data-ttu-id="676ee-112">В поле **Счет поставщика** введите значение.</span><span class="sxs-lookup"><span data-stu-id="676ee-112">In the **Vendor account** field, type a value.</span></span>
4. <span data-ttu-id="676ee-113">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="676ee-113">Click **OK**.</span></span>
5. <span data-ttu-id="676ee-114">Щелкните **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="676ee-114">Click **Add line**.</span></span>
6. <span data-ttu-id="676ee-115">В поле **Код номенклатуры** введите значение.</span><span class="sxs-lookup"><span data-stu-id="676ee-115">In the **Item number** field, type a value.</span></span>
7. <span data-ttu-id="676ee-116">В области действий щелкните **Покупка**.</span><span class="sxs-lookup"><span data-stu-id="676ee-116">On the Action Pane, click **Purchase**.</span></span>
8. <span data-ttu-id="676ee-117">Нажмите кнопку **Подтвердить**.</span><span class="sxs-lookup"><span data-stu-id="676ee-117">Click **Confirm**.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="676ee-118">Разноска поступления продуктов</span><span class="sxs-lookup"><span data-stu-id="676ee-118">Post a product receipt</span></span>
1. <span data-ttu-id="676ee-119">В области действий щелкните **Получить**.</span><span class="sxs-lookup"><span data-stu-id="676ee-119">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="676ee-120">Щелкните **Поступление продуктов**.</span><span class="sxs-lookup"><span data-stu-id="676ee-120">Click **Product receipt**.</span></span>
3. <span data-ttu-id="676ee-121">В поле **Поступление продуктов** введите значение.</span><span class="sxs-lookup"><span data-stu-id="676ee-121">In the **Product receipt** field, type a value.</span></span>
4. <span data-ttu-id="676ee-122">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="676ee-122">Click **OK**.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="676ee-123">Регистрация и сопоставление накладной поставщика с поступлением продуктов</span><span class="sxs-lookup"><span data-stu-id="676ee-123">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="676ee-124">В области действий щелкните **Накладная > Накладная**.</span><span class="sxs-lookup"><span data-stu-id="676ee-124">On the Action Pane, click **Invoice > Invoice**.</span></span>
2. <span data-ttu-id="676ee-125">В поле **Число** введите значение.</span><span class="sxs-lookup"><span data-stu-id="676ee-125">In the **Number** field, type a value.</span></span>
3. <span data-ttu-id="676ee-126">Щелкните **По умолчанию из: заказанное количество**, чтобы открыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="676ee-126">Click **Default from: Ordered quantity** to open the drop dialog.</span></span>
4. <span data-ttu-id="676ee-127">В поле **Количество по умолчанию для строк** выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="676ee-127">In the **Default quantity for lines** field, select an option.</span></span>
5. <span data-ttu-id="676ee-128">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="676ee-128">Click **OK**.</span></span>
6. <span data-ttu-id="676ee-129">Нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="676ee-129">Click **Yes**.</span></span>
7. <span data-ttu-id="676ee-130">Щелкните **Сопоставить поступления продуктов**.</span><span class="sxs-lookup"><span data-stu-id="676ee-130">Click **Match product receipts**.</span></span>
8. <span data-ttu-id="676ee-131">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="676ee-131">Click **OK**.</span></span>
9. <span data-ttu-id="676ee-132">В области действий щелкните **Просмотр**.</span><span class="sxs-lookup"><span data-stu-id="676ee-132">On the Action Pane, click **Review**.</span></span>
10. <span data-ttu-id="676ee-133">Щелкните **Сведения о сопоставлении**.</span><span class="sxs-lookup"><span data-stu-id="676ee-133">Click **Matching details**.</span></span>

