---
title: Настройка датированных будущим числом чеков
description: В этом разделе описан порядок определения, разносить ли записи журнала для чеков, датированных будущим числом, и какие журналы разноски использовать для клиринговых записей и платежей поставщикам.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22e67aa051b5ea8267df7efac40e007d0f11a83d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447267"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="866b0-103">Настройка датированных будущим числом чеков</span><span class="sxs-lookup"><span data-stu-id="866b0-103">Set up postdated checks</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="866b0-104">В этом разделе описан порядок определения, разносить ли записи журнала для чеков, датированных будущим числом, и какие журналы разноски использовать для клиринговых записей и платежей поставщикам.</span><span class="sxs-lookup"><span data-stu-id="866b0-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="866b0-105">Можно также определить клиринговые счета для выписанные чеки, полученные чеки и подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="866b0-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="866b0-106">Чеки, датированные будущим числом, выпущенные для осуществления и получения платежей в будущем.</span><span class="sxs-lookup"><span data-stu-id="866b0-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="866b0-107">Можно указать, должен ли чек отражаться в бухгалтерских книгах до даты его исполнения.</span><span class="sxs-lookup"><span data-stu-id="866b0-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="866b0-108">Роль для выполнения этой процедуры — казначей.</span><span class="sxs-lookup"><span data-stu-id="866b0-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="866b0-109">В данной процедуре используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="866b0-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="866b0-110">Настройка датированных будущим числом чеков</span><span class="sxs-lookup"><span data-stu-id="866b0-110">Set up postdated checks</span></span>
1. <span data-ttu-id="866b0-111">Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Параметры управления банком и кассовыми операциями".</span><span class="sxs-lookup"><span data-stu-id="866b0-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="866b0-112">Перейдите на вкладку "Чеки, датированные будущим числом".</span><span class="sxs-lookup"><span data-stu-id="866b0-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="866b0-113">Установите или снимите флажок "Разрешить чеки, датированные будущим числом".</span><span class="sxs-lookup"><span data-stu-id="866b0-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="866b0-114">Установите или снимите флажок "Разноска записей журнала для чеков, датированных будущим числом".</span><span class="sxs-lookup"><span data-stu-id="866b0-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="866b0-115">В поле "Клиринговый счет для выписанных чеков" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="866b0-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="866b0-116">В поле "Клиринговый счет для полученных чеков" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="866b0-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="866b0-117">В "Общий журнал для записей клиринга" поле введите значение.</span><span class="sxs-lookup"><span data-stu-id="866b0-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="866b0-118">В поле "Перенести чеки, датированные будущим числом, в этот журнал платежей поставщику" введите значение.</span><span class="sxs-lookup"><span data-stu-id="866b0-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="866b0-119">В поле "Клиринговый счет подоходного налога" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="866b0-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="866b0-120">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="866b0-120">Click Save.</span></span>
11. <span data-ttu-id="866b0-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="866b0-121">Close the page.</span></span>
12. <span data-ttu-id="866b0-122">Перейдите в раздел "Расчеты с поставщиками" > "Настройка платежей" > "Способы оплаты".</span><span class="sxs-lookup"><span data-stu-id="866b0-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="866b0-123">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="866b0-123">Click New.</span></span>
14. <span data-ttu-id="866b0-124">В поле "Способ оплаты" введите значение.</span><span class="sxs-lookup"><span data-stu-id="866b0-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="866b0-125">Выберите параметр "Разноска клиринга чеков, датированных будущим числом", чтобы указать, что сумма чека разносится на клиринговый счет.</span><span class="sxs-lookup"><span data-stu-id="866b0-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="866b0-126">В поле "Тип счета" выберите "Банк".</span><span class="sxs-lookup"><span data-stu-id="866b0-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="866b0-127">Корреспондирующим счетом способа оплаты будет банк.</span><span class="sxs-lookup"><span data-stu-id="866b0-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="866b0-128">В поле "Счет оплаты" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="866b0-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="866b0-129">Выберите банковский счет, который используется для вычета суммы накладной.</span><span class="sxs-lookup"><span data-stu-id="866b0-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="866b0-130">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="866b0-130">Click Save.</span></span>
19. <span data-ttu-id="866b0-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="866b0-131">Close the page.</span></span>

