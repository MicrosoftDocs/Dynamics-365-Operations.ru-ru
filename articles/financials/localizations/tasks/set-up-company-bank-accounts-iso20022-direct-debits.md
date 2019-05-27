---
title: Настройка банковских счетов компании для безакцептного списания ISO20022
description: В этой задаче описывается настройка сведений о банковском счете компании, которые необходимы для создания файлов платежей клиентов.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 290d0eeb383dc3808935809e21b1bf6c99a8550a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552402"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="f88ca-103">Настройка банковских счетов компании для безакцептного списания ISO20022</span><span class="sxs-lookup"><span data-stu-id="f88ca-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f88ca-104">В этой задаче описывается настройка сведений о банковском счете компании, которые необходимы для создания файлов платежей клиентов.</span><span class="sxs-lookup"><span data-stu-id="f88ca-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="f88ca-105">Эта процедура использует формат прямого дебетования ISO 20022 в качестве примера.</span><span class="sxs-lookup"><span data-stu-id="f88ca-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="f88ca-106">Другие форматы могут требовать дополнительных сведений о настройке, таких как код компании или код сортировки.</span><span class="sxs-lookup"><span data-stu-id="f88ca-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="f88ca-107">Эта задача была создана с использованием компании с демонстрационными данными DEMF.</span><span class="sxs-lookup"><span data-stu-id="f88ca-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="f88ca-108">Это вторая процедура из пяти, которые демонстрируют процесс платежа клиентов с помощью конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="f88ca-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="f88ca-109">Настройка кода IBAN и SWIFT-кода</span><span class="sxs-lookup"><span data-stu-id="f88ca-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="f88ca-110">Перейдите в раздел "Управление банком и кассовыми операциями" > "Банковские счета".</span><span class="sxs-lookup"><span data-stu-id="f88ca-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="f88ca-111">Используйте экспресс-фильтр для фильтрации поля "Банковский счет" по значению 'DEMF OPER".</span><span class="sxs-lookup"><span data-stu-id="f88ca-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="f88ca-112">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f88ca-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f88ca-113">Например, щелкните "DEMF OPER", чтобы открыть сведения о банковском счете.</span><span class="sxs-lookup"><span data-stu-id="f88ca-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="f88ca-114">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="f88ca-114">Click Edit.</span></span>
5. <span data-ttu-id="f88ca-115">Разверните или сверните раздел "Дополнительная идентификация".</span><span class="sxs-lookup"><span data-stu-id="f88ca-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="f88ca-116">В поле "IBAN" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f88ca-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="f88ca-117">Например, введите "DE89370400440532013000".</span><span class="sxs-lookup"><span data-stu-id="f88ca-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="f88ca-118">В поле "SWIFT-код" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f88ca-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="f88ca-119">Например, введите "DEUTDEFF".</span><span class="sxs-lookup"><span data-stu-id="f88ca-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="f88ca-120">Обратите внимание, что SWIFT\BIC не является обязательным для многих форматов платежей, однако рекомендуется, чтобы этот код был зарегистрирован для банковского счета.</span><span class="sxs-lookup"><span data-stu-id="f88ca-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="f88ca-121">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="f88ca-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="f88ca-122">Настройка банковского счета для юридического лица</span><span class="sxs-lookup"><span data-stu-id="f88ca-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="f88ca-123">Перейдите в раздел "Управление организацией" > "Организации" > "Юридические лица".</span><span class="sxs-lookup"><span data-stu-id="f88ca-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="f88ca-124">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="f88ca-124">Click Edit.</span></span>
3. <span data-ttu-id="f88ca-125">Разверните или сверните раздел "Сведения о банковском счете".</span><span class="sxs-lookup"><span data-stu-id="f88ca-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="f88ca-126">В поле "Банковский счет" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f88ca-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f88ca-127">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f88ca-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f88ca-128">Например, выберите банковский счет "DEMF OPER".</span><span class="sxs-lookup"><span data-stu-id="f88ca-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="f88ca-129">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="f88ca-129">Click Save.</span></span>

