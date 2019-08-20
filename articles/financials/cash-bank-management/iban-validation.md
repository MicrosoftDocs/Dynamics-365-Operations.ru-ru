---
title: Управление проверкой счетов с International Bank Account Number (IBAN)
description: В этой теме рассматривается, как управлять проверкой счетов с International Bank Account Number (IBAN).
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 70c497ec575ffcaa6f2fdc3fe77bae7b41dc02fb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842433"
---
# <a name="manage-international-bank-account-number-iban-validation"></a><span data-ttu-id="16643-103">Управление проверкой International Bank Account Number (IBAN)</span><span class="sxs-lookup"><span data-stu-id="16643-103">Manage International Bank Account Number (IBAN) validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16643-104">Проверка International Bank Account Number (IBAN) повышает уровень проверок, выполняемых при добавлении IBAN к банковскому счету.</span><span class="sxs-lookup"><span data-stu-id="16643-104">International Bank Account Number (IBAN) validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="16643-105">Сведения о структуре IBAN хранятся в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="16643-105">Information about the structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="16643-106">Эти сведения автоматически загружаются при первом использовании IBAN с банковскими счетам.</span><span class="sxs-lookup"><span data-stu-id="16643-106">That information is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="16643-107">Он содержит длину номера IBAN, начальные позиции номера банковского счета и кода банка, а также длину номера банковского счета и кода банка.</span><span class="sxs-lookup"><span data-stu-id="16643-107">It contains the length of the IBAN, the starting positions of the bank account number and the routing number, and the length of the bank account number and routing number.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="16643-108">Настройка структур IBAN</span><span class="sxs-lookup"><span data-stu-id="16643-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="16643-109">Перейдите в раздел **Управление банком и кассовыми операциями \> Настройка \> Структуры IBAN**.</span><span class="sxs-lookup"><span data-stu-id="16643-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="16643-110">Обратите внимание, что структуры IBAN для каждой страны или региона настроены автоматически.</span><span class="sxs-lookup"><span data-stu-id="16643-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="16643-111">Если требуется настроить структуры для определенной страны или региона, вы можете их отредактировать.</span><span class="sxs-lookup"><span data-stu-id="16643-111">If you want to customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="16643-112">Определения структур будут входить в состав каждого нового выпуска.</span><span class="sxs-lookup"><span data-stu-id="16643-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="16643-113">Можно использовать меню **Сброс структур** для загрузки последних определений после каждого обновления.</span><span class="sxs-lookup"><span data-stu-id="16643-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="16643-114">Проверка структуры IBAN для банковского счета</span><span class="sxs-lookup"><span data-stu-id="16643-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="16643-115">Перейдите в раздел **Управление банком и кассовыми операциями \> Банковские счета \> Банковские счета**.</span><span class="sxs-lookup"><span data-stu-id="16643-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="16643-116">Создайте банковский счет.</span><span class="sxs-lookup"><span data-stu-id="16643-116">Create a bank account.</span></span>
3. <span data-ttu-id="16643-117">На экспресс-вкладке **Дополнительная информация** введите IBAN.</span><span class="sxs-lookup"><span data-stu-id="16643-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="16643-118">Если длина IBAN не соответствует длине, которая определена для каждой страны или региона, появится предупреждающее сообщение.</span><span class="sxs-lookup"><span data-stu-id="16643-118">If the length of the IBAN doesn't match the length that is defined for each country or region, you will receive a warning message.</span></span> <span data-ttu-id="16643-119">Если длина IBAN не соответствует длине, указанной в структуре IBAN, продолжить выполнение операции невозможно.</span><span class="sxs-lookup"><span data-stu-id="16643-119">You can't continue if the length of the IBAN doesn't match the length specified in the IBAN structure.</span></span>

    <span data-ttu-id="16643-120">Также проверяется, соответствует ли номер банковского счета той части IBAN, которая представляет номер банковского счета.</span><span class="sxs-lookup"><span data-stu-id="16643-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="16643-121">Если номер банковского счета не соответствует структуре, будет выведено сообщение.</span><span class="sxs-lookup"><span data-stu-id="16643-121">If the bank account number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="16643-122">Это сообщение — не более чем предупреждение.</span><span class="sxs-lookup"><span data-stu-id="16643-122">This message is only a warning.</span></span> <span data-ttu-id="16643-123">Можно продолжить выполнение операции, даже если номер банковского счета не соответствует структуре IBAN.</span><span class="sxs-lookup"><span data-stu-id="16643-123">You can continue even if the bank account number doesn't match.</span></span>

    <span data-ttu-id="16643-124">Также проверяется, соответствует ли код банка той части IBAN, которая представляет код банка.</span><span class="sxs-lookup"><span data-stu-id="16643-124">The validation also verifies that the bank routing number matches the part of the IBAN that represents the bank routing number.</span></span> <span data-ttu-id="16643-125">Код банка включает номер банка и, часто, дополнительное отделение банка.</span><span class="sxs-lookup"><span data-stu-id="16643-125">The routing number includes a bank number and often an additional bank branch.</span></span> <span data-ttu-id="16643-126">Если код банка не соответствует, будет выведено сообщение.</span><span class="sxs-lookup"><span data-stu-id="16643-126">If the bank routing number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="16643-127">Это сообщение — не более чем предупреждение.</span><span class="sxs-lookup"><span data-stu-id="16643-127">This message is only a warning.</span></span> <span data-ttu-id="16643-128">Можно продолжить выполнение операции, даже если код банка не соответствует.</span><span class="sxs-lookup"><span data-stu-id="16643-128">You can continue even if the bank routing number doesn't match.</span></span>
