---
title: Настройка банковских счетов компании для кредитных переводов ISO20022
description: В этой процедуре показано, как настроить сведения о банковском счете компании, которые необходимы для создания файла платежа.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ad1ebbea9bca41f43f3f4098114116e32f8517b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205478"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="f0405-103">Настройка банковских счетов компании для кредитных переводов ISO20022</span><span class="sxs-lookup"><span data-stu-id="f0405-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f0405-104">В этой процедуре показано, как настроить сведения о банковском счете компании, которые необходимы для создания файла платежа.</span><span class="sxs-lookup"><span data-stu-id="f0405-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="f0405-105">Вы настраиваете информацию, необходимую для создания формата перемещения кредита ISO 20022, но в зависимости от выбранного формата также может требоваться другая информация, такая как код компании или код сортировки.</span><span class="sxs-lookup"><span data-stu-id="f0405-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="f0405-106">В качестве компании с демонстрационными данными для создания этой процедуры используется DEMF.</span><span class="sxs-lookup"><span data-stu-id="f0405-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="f0405-107">Это вторая процедура из пяти, которые иллюстрируют процесс платежа поставщикам с помощью конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="f0405-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="f0405-108">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="f0405-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="f0405-109">Настройка номера IBAN и SWIFT-кода</span><span class="sxs-lookup"><span data-stu-id="f0405-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="f0405-110">Перейдите в раздел "Управление банком и кассовыми операциями" > "Банковские счета".</span><span class="sxs-lookup"><span data-stu-id="f0405-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="f0405-111">Используйте экспресс-фильтр для фильтрации поля "Банковский счет" по значению 'DEMF OPER".</span><span class="sxs-lookup"><span data-stu-id="f0405-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="f0405-112">Щелкните "DEMF OPER", чтобы открыть сведения о банковском счете.</span><span class="sxs-lookup"><span data-stu-id="f0405-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="f0405-113">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="f0405-113">Click Edit.</span></span>
5. <span data-ttu-id="f0405-114">Разверните раздел "Дополнительная идентификация".</span><span class="sxs-lookup"><span data-stu-id="f0405-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="f0405-115">В поле "Номер IBAN" введите ''DE89370400440532013000".</span><span class="sxs-lookup"><span data-stu-id="f0405-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="f0405-116">В поле "SWIFT-код" введите "DEUTDEFF".</span><span class="sxs-lookup"><span data-stu-id="f0405-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="f0405-117">Обратите внимание, что SWIFT\BIC не требуется для многих форматов платежей, однако рекомендуется, чтобы этот код был зарегистрирован для банковского счета.</span><span class="sxs-lookup"><span data-stu-id="f0405-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="f0405-118">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="f0405-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="f0405-119">Настройка банковского счета для юридического лица</span><span class="sxs-lookup"><span data-stu-id="f0405-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="f0405-120">Перейдите в раздел "Управление организацией" > "Организации" > "Юридические лица".</span><span class="sxs-lookup"><span data-stu-id="f0405-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="f0405-121">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="f0405-121">Click Edit.</span></span>
3. <span data-ttu-id="f0405-122">Разверните раздел "Сведения о банковском счете".</span><span class="sxs-lookup"><span data-stu-id="f0405-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="f0405-123">В поле "Банковский счет" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f0405-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="f0405-124">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="f0405-124">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]