---
title: Настройка поставщиков и банковских счетов поставщиков для кредитовых переводов ISO20022
description: В этой процедуре показано, как настроить поставщика и сведения о банковском счете поставщика, необходимые для создания файла платежа переноса кредита ISO20022 или любого другого платежа поставщику.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab8c52b9b457505c2cf2bfca46cb938e73c0142e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175012"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="85dc8-103">Настройка поставщиков и банковских счетов поставщиков для кредитовых переводов ISO20022</span><span class="sxs-lookup"><span data-stu-id="85dc8-103">Set up vendors and vendor bank accounts for ISO20022 credit transfers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="85dc8-104">В этой процедуре показано, как настроить поставщика и сведения о банковском счете поставщика, необходимые для создания файла платежа переноса кредита ISO20022 или любого другого платежа поставщику.</span><span class="sxs-lookup"><span data-stu-id="85dc8-104">This procedure demonstrates how to set up the vendor and vendor specific bank account information required for ISO20022 Credit transfer or any other vendor payment file generation.</span></span> 

<span data-ttu-id="85dc8-105">В качестве компании с демонстрационными данными для создания этой процедуры используется DEMF.</span><span class="sxs-lookup"><span data-stu-id="85dc8-105">The demo data company used to create this procedure is DEMF.</span></span>
<span data-ttu-id="85dc8-106">Это четвертая процедура из пяти, которые иллюстрируют процесс платежа поставщикам с помощью конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="85dc8-106">This is the fourth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="85dc8-107">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="85dc8-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-bank-details"></a><span data-ttu-id="85dc8-108">Настройка сведений о банке</span><span class="sxs-lookup"><span data-stu-id="85dc8-108">Set up bank details</span></span>
1. <span data-ttu-id="85dc8-109">Перейдите в раздел "Расчеты с поставщиками" > "Поставщики" > "Все поставщики".</span><span class="sxs-lookup"><span data-stu-id="85dc8-109">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="85dc8-110">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="85dc8-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="85dc8-111">Например, отфильтруйте поле "Счет поставщика" по значению "DE-001".</span><span class="sxs-lookup"><span data-stu-id="85dc8-111">For example, filter on the Vendor account field with a value of 'DE-001'.</span></span>
3. <span data-ttu-id="85dc8-112">Щелкните "DE-001", чтобы открыть сведения о поставщике.</span><span class="sxs-lookup"><span data-stu-id="85dc8-112">Click DE-001 to open vendor details.</span></span>
4. <span data-ttu-id="85dc8-113">В области действий щелкните "Поставщик".</span><span class="sxs-lookup"><span data-stu-id="85dc8-113">On the Action Pane, click Vendor.</span></span>
5. <span data-ttu-id="85dc8-114">Щелкните "Банковские счета".</span><span class="sxs-lookup"><span data-stu-id="85dc8-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="85dc8-115">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="85dc8-115">Click Edit.</span></span>
    * <span data-ttu-id="85dc8-116">Если ни один банковский счет недоступен, необходимо создать банковский счет.</span><span class="sxs-lookup"><span data-stu-id="85dc8-116">If there is no bank account available, you need to create a new one.</span></span>  
7. <span data-ttu-id="85dc8-117">В поле "SWIFT-код" введите "COBADEFFXXX".</span><span class="sxs-lookup"><span data-stu-id="85dc8-117">In the SWIFT code field, type 'COBADEFFXXX'.</span></span>
8. <span data-ttu-id="85dc8-118">В поле "Номер IBAN" введите ''DE36200400000628808808".</span><span class="sxs-lookup"><span data-stu-id="85dc8-118">In the IBAN field, type 'DE36200400000628808808'.</span></span>
9. <span data-ttu-id="85dc8-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="85dc8-119">Close the page.</span></span>

## <a name="set-up-a-method-of-payment-for-the-vendor"></a><span data-ttu-id="85dc8-120">Настройка способа оплаты для поставщика</span><span class="sxs-lookup"><span data-stu-id="85dc8-120">Set up a method of payment for the vendor</span></span>
1. <span data-ttu-id="85dc8-121">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="85dc8-121">Click Edit.</span></span>
2. <span data-ttu-id="85dc8-122">Разверните или сверните раздел "Платеж".</span><span class="sxs-lookup"><span data-stu-id="85dc8-122">Expand or collapse the Payment section.</span></span>
3. <span data-ttu-id="85dc8-123">В поле "Способ оплаты" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="85dc8-123">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="85dc8-124">В списке перейдите по ссылке в строке SEPA CT.</span><span class="sxs-lookup"><span data-stu-id="85dc8-124">In the list, click the link in the SEPA CT row.</span></span>
5. <span data-ttu-id="85dc8-125">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="85dc8-125">Click Save.</span></span>

