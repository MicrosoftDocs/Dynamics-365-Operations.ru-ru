--- 
title: "Аудит накладных и ключевых данных в модуле расчетов с поставщиками"
description: "При получении накладной от поставщика за товары или услуги по заказу на покупку для бизнес-процессов может потребоваться, чтобы товары или услуги были получены, прежде чем накладная может утверждена для платежа."
author: saraschi2
manager: AnnBe
ms.date: 02/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 5cd9448c95b7ec0c4a82aca3d21d961259dfb109
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a><span data-ttu-id="f32ed-103">Аудит накладных и ключевых данных в модуле расчетов с поставщиками</span><span class="sxs-lookup"><span data-stu-id="f32ed-103">Audit invoices and key data in accounts payable</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f32ed-104">При получении накладной от поставщика за товары или услуги по заказу на покупку для бизнес-процессов может потребоваться, чтобы товары или услуги были получены, прежде чем накладная может утверждена для платежа.</span><span class="sxs-lookup"><span data-stu-id="f32ed-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="f32ed-105">Перед началом работы убедитесь, что выбран конфигурационный ключ "Сопоставление накладных".</span><span class="sxs-lookup"><span data-stu-id="f32ed-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="f32ed-106">На странице "Параметры расчетов с поставщиками" убедитесь, что установлен флажок "Включить проверку сопоставления накладных", в поле "Разнести накладную с несоответствиями" задано значение "Требуется утверждение" и в поле "Политика проверки соответствия строк" задано значение "Трехстороннее сопоставление".</span><span class="sxs-lookup"><span data-stu-id="f32ed-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="f32ed-107">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="f32ed-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="f32ed-108">Эти шаги выполняются ролями менеджера по расчету с поставщиками или главного бухгалтера.</span><span class="sxs-lookup"><span data-stu-id="f32ed-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="f32ed-109">Создание заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="f32ed-109">Create a purchase order</span></span>
1. <span data-ttu-id="f32ed-110">Перейдите в раздел "Все заказы на покупку".</span><span class="sxs-lookup"><span data-stu-id="f32ed-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="f32ed-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f32ed-111">Click New.</span></span>
3. <span data-ttu-id="f32ed-112">В поле "Счет поставщика" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f32ed-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f32ed-113">В поле "Счет поставщика" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f32ed-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="f32ed-114">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f32ed-114">Click OK.</span></span>
6. <span data-ttu-id="f32ed-115">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="f32ed-115">Click Add line.</span></span>
7. <span data-ttu-id="f32ed-116">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f32ed-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="f32ed-117">В области действий щелкните "Покупка".</span><span class="sxs-lookup"><span data-stu-id="f32ed-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="f32ed-118">Нажмите кнопку "Подтвердить".</span><span class="sxs-lookup"><span data-stu-id="f32ed-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="f32ed-119">Разноска поступления продуктов</span><span class="sxs-lookup"><span data-stu-id="f32ed-119">Post a product receipt</span></span>
1. <span data-ttu-id="f32ed-120">В области действий щелкните "Получение".</span><span class="sxs-lookup"><span data-stu-id="f32ed-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="f32ed-121">Щелкните "Поступление продуктов".</span><span class="sxs-lookup"><span data-stu-id="f32ed-121">Click Product receipt.</span></span>
3. <span data-ttu-id="f32ed-122">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="f32ed-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f32ed-123">В поле "Поступление продуктов" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f32ed-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="f32ed-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f32ed-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="f32ed-125">Регистрация и сопоставление накладной поставщика с поступлением продуктов</span><span class="sxs-lookup"><span data-stu-id="f32ed-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="f32ed-126">В области действий щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="f32ed-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="f32ed-127">Щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="f32ed-127">Click Invoice.</span></span>
3. <span data-ttu-id="f32ed-128">В поле "Число" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f32ed-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="f32ed-129">Щелкните "По умолчанию из: заказанное количество", чтобы открыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f32ed-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="f32ed-130">В поле "Количество по умолчанию для строк" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="f32ed-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="f32ed-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f32ed-131">Click OK.</span></span>
7. <span data-ttu-id="f32ed-132">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="f32ed-132">Click Yes.</span></span>
8. <span data-ttu-id="f32ed-133">Щелкните "Сопоставить поступления продуктов".</span><span class="sxs-lookup"><span data-stu-id="f32ed-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="f32ed-134">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="f32ed-134">Click OK.</span></span>
10. <span data-ttu-id="f32ed-135">В области действий щелкните "Просмотр".</span><span class="sxs-lookup"><span data-stu-id="f32ed-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="f32ed-136">Щелкните "Сведения о сопоставлении".</span><span class="sxs-lookup"><span data-stu-id="f32ed-136">Click Matching details.</span></span>

