--- 
title: "Настройка поставщиков и банковских счетов поставщиков для кредитовых переводов ISO20022"
description: "В этой процедуре показано, как настроить поставщика и сведения о банковском счете поставщика, необходимые для создания файла платежа переноса кредита ISO20022 или любого другого платежа поставщику."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c85c6d66effbd117a6f787295f66ca097b2fe4c6
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="d7a92-103">Настройка поставщиков и банковских счетов поставщиков для кредитовых переводов ISO20022</span><span class="sxs-lookup"><span data-stu-id="d7a92-103">Set up vendors and vendor bank accounts for ISO20022 credit transfers</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d7a92-104">В этой процедуре показано, как настроить поставщика и сведения о банковском счете поставщика, необходимые для создания файла платежа переноса кредита ISO20022 или любого другого платежа поставщику.</span><span class="sxs-lookup"><span data-stu-id="d7a92-104">This procedure demonstrates how to set up the vendor and vendor specific bank account information required for ISO20022 Credit transfer or any other vendor payment file generation.</span></span> 

<span data-ttu-id="d7a92-105">В качестве компании с демонстрационными данными для создания этой процедуры используется DEMF.</span><span class="sxs-lookup"><span data-stu-id="d7a92-105">The demo data company used to create this procedure is DEMF.</span></span>
<span data-ttu-id="d7a92-106">Это четвертая процедура из пяти, которые иллюстрируют процесс платежа поставщикам с помощью конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="d7a92-106">This is the fourth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="d7a92-107">Эта процедура предназначена для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="d7a92-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-bank-details"></a><span data-ttu-id="d7a92-108">Настройка сведений о банке</span><span class="sxs-lookup"><span data-stu-id="d7a92-108">Set up bank details</span></span>
1. <span data-ttu-id="d7a92-109">Перейдите в раздел "Расчеты с поставщиками" > "Поставщики" > "Все поставщики".</span><span class="sxs-lookup"><span data-stu-id="d7a92-109">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="d7a92-110">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="d7a92-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d7a92-111">Например, отфильтруйте поле "Счет поставщика" по значению "DE-001".</span><span class="sxs-lookup"><span data-stu-id="d7a92-111">For example, filter on the Vendor account field with a value of 'DE-001'.</span></span>
3. <span data-ttu-id="d7a92-112">Щелкните "DE-001", чтобы открыть сведения о поставщике.</span><span class="sxs-lookup"><span data-stu-id="d7a92-112">Click DE-001 to open vendor details.</span></span>
4. <span data-ttu-id="d7a92-113">В области действий щелкните "Поставщик".</span><span class="sxs-lookup"><span data-stu-id="d7a92-113">On the Action Pane, click Vendor.</span></span>
5. <span data-ttu-id="d7a92-114">Щелкните "Банковские счета".</span><span class="sxs-lookup"><span data-stu-id="d7a92-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="d7a92-115">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="d7a92-115">Click Edit.</span></span>
    * <span data-ttu-id="d7a92-116">Если ни один банковский счет недоступен, необходимо создать банковский счет.</span><span class="sxs-lookup"><span data-stu-id="d7a92-116">If there is no bank account available, you need to create a new one.</span></span>  
7. <span data-ttu-id="d7a92-117">В поле "SWIFT-код" введите "COBADEFFXXX".</span><span class="sxs-lookup"><span data-stu-id="d7a92-117">In the SWIFT code field, type 'COBADEFFXXX'.</span></span>
8. <span data-ttu-id="d7a92-118">В поле "Номер IBAN" введите ''DE36200400000628808808".</span><span class="sxs-lookup"><span data-stu-id="d7a92-118">In the IBAN field, type 'DE36200400000628808808'.</span></span>
9. <span data-ttu-id="d7a92-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d7a92-119">Close the page.</span></span>

## <a name="set-up-a-method-of-payment-for-the-vendor"></a><span data-ttu-id="d7a92-120">Настройка способа оплаты для поставщика</span><span class="sxs-lookup"><span data-stu-id="d7a92-120">Set up a method of payment for the vendor</span></span>
1. <span data-ttu-id="d7a92-121">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="d7a92-121">Click Edit.</span></span>
2. <span data-ttu-id="d7a92-122">Разверните или сверните раздел "Платеж".</span><span class="sxs-lookup"><span data-stu-id="d7a92-122">Expand or collapse the Payment section.</span></span>
3. <span data-ttu-id="d7a92-123">В поле "Способ оплаты" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="d7a92-123">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d7a92-124">В списке перейдите по ссылке в строке SEPA CT.</span><span class="sxs-lookup"><span data-stu-id="d7a92-124">In the list, click the link in the SEPA CT row.</span></span>
5. <span data-ttu-id="d7a92-125">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d7a92-125">Click Save.</span></span>


