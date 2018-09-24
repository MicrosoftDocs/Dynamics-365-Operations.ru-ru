---
title: "Управление проверкой счетов с International Bank Account Number (IBAN)"
description: "В этой теме рассматривается, как управлять проверкой счетов с International Bank Account Number (IBAN)."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: ru-ru
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="3590d-103">Управление проверкой счетов с International Bank Account Number (IBAN)</span><span class="sxs-lookup"><span data-stu-id="3590d-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3590d-104">Проверка счетов с International Bank Account Number (IBAN) повышает уровень проверок, выполняемых при добавлении IBAN к банковскому счету.</span><span class="sxs-lookup"><span data-stu-id="3590d-104">International Bank Account Number (IBAN) account validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="3590d-105">Структура IBAN хранится в Microsoft Dynamics 365 for Finance and Operation и автоматически загружается при первом использовании IBAN применительно к банковским счетам.</span><span class="sxs-lookup"><span data-stu-id="3590d-105">The structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operation, and is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="3590d-106">Номер банковского счета является частью структуры, определенной для номера IBAN.</span><span class="sxs-lookup"><span data-stu-id="3590d-106">The bank account number is part of the structure defined for an IBAN number.</span></span> <span data-ttu-id="3590d-107">Исходя из этой структуры, если положение и длина номера счета в IBAN не соответствуют положению, определенному в структуре для каждой страны или региона, будут выводиться предупредительные сообщения.</span><span class="sxs-lookup"><span data-stu-id="3590d-107">Based on that structure, if the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you will receive warning messages.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="3590d-108">Настройка структур IBAN</span><span class="sxs-lookup"><span data-stu-id="3590d-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="3590d-109">Перейдите в раздел **Управление банком и кассовыми операциями \> Настройка \> Структуры IBAN**.</span><span class="sxs-lookup"><span data-stu-id="3590d-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="3590d-110">Обратите внимание, что структуры IBAN для каждой страны или региона настроены автоматически.</span><span class="sxs-lookup"><span data-stu-id="3590d-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="3590d-111">Если требуется настроить структуры для определенной страны или региона, вы можете их отредактировать.</span><span class="sxs-lookup"><span data-stu-id="3590d-111">If you must customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="3590d-112">Определения структур будут входить в состав каждого нового выпуска.</span><span class="sxs-lookup"><span data-stu-id="3590d-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="3590d-113">Можно использовать меню **Сброс структур** для загрузки последних определений после каждого обновления.</span><span class="sxs-lookup"><span data-stu-id="3590d-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="3590d-114">Проверка структуры IBAN для банковского счета</span><span class="sxs-lookup"><span data-stu-id="3590d-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="3590d-115">Перейдите в раздел **Управление банком и кассовыми операциями \> Банковские счета \> Банковские счета**.</span><span class="sxs-lookup"><span data-stu-id="3590d-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="3590d-116">Создайте банковский счет.</span><span class="sxs-lookup"><span data-stu-id="3590d-116">Create a bank account.</span></span>
3. <span data-ttu-id="3590d-117">На экспресс-вкладке **Дополнительная информация** введите IBAN.</span><span class="sxs-lookup"><span data-stu-id="3590d-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="3590d-118">Если положение и длина номера счета в IBAN не соответствуют положению, определенному в структуре для каждой страны или региона, система выведет сообщение.</span><span class="sxs-lookup"><span data-stu-id="3590d-118">If the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you receive a message.</span></span> <span data-ttu-id="3590d-119">Если длина IBAN не соответствует длине в структуре IBAN, продолжить выполнение операции невозможно.</span><span class="sxs-lookup"><span data-stu-id="3590d-119">You can't continue if the length of the IBAN doesn't match the length in the IBAN structure.</span></span>

    <span data-ttu-id="3590d-120">Также проверяется, соответствует ли номер банковского счета той части IBAN, которая представляет номер банковского счета.</span><span class="sxs-lookup"><span data-stu-id="3590d-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="3590d-121">Если номер банковского счета не соответствует структуре, будет выведено сообщение.</span><span class="sxs-lookup"><span data-stu-id="3590d-121">If the bank account number doesn't match, you receive a warning message.</span></span> <span data-ttu-id="3590d-122">Это сообщение — не более чем предупреждение.</span><span class="sxs-lookup"><span data-stu-id="3590d-122">This message is only a warning.</span></span> <span data-ttu-id="3590d-123">Можно продолжить выполнение операции, даже если номер банковского счета не соответствует структуре IBAN.</span><span class="sxs-lookup"><span data-stu-id="3590d-123">You can continue even if the bank account number doesn't match.</span></span>

