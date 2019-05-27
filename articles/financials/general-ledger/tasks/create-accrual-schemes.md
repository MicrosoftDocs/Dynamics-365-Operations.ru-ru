---
title: Создание схем начисления
description: В этом руководства рассказывается о создании схемы начисления.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ce96ccfb0dc3e4a723af967147dae93772c5b44f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553139"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="0e60d-103">Создание схем начисления</span><span class="sxs-lookup"><span data-stu-id="0e60d-103">Create accrual schemes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e60d-104">В этом руководства рассказывается о создании схемы начисления.</span><span class="sxs-lookup"><span data-stu-id="0e60d-104">This task guide steps through creating an accrual scheme.</span></span> <span data-ttu-id="0e60d-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="0e60d-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="0e60d-106">Перейдите в раздел "Главная книга" > "Настройка журнала" > "Схема начисления".</span><span class="sxs-lookup"><span data-stu-id="0e60d-106">Go to General ledger > Journal setup > Accrual schemes.</span></span>
2. <span data-ttu-id="0e60d-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="0e60d-107">Click New.</span></span>
3. <span data-ttu-id="0e60d-108">В поле "Код начисления" введите значение.</span><span class="sxs-lookup"><span data-stu-id="0e60d-108">In the Accrual identification field, type a value.</span></span>
4. <span data-ttu-id="0e60d-109">В поле "Описание схемы начислений" введите значение.</span><span class="sxs-lookup"><span data-stu-id="0e60d-109">In the Description of accrual scheme field, type a value.</span></span>
5. <span data-ttu-id="0e60d-110">В поле "Дебет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="0e60d-110">In the Debit field, specify the desired values.</span></span>
    * <span data-ttu-id="0e60d-111">Определенный счет ГК заменит счет ГК дебета в строке ваучера журнала и также будет использоваться для реверсирования расхода будущего периода на основе проводок начисления ГК.</span><span class="sxs-lookup"><span data-stu-id="0e60d-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="0e60d-112">В поле "Кредит" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="0e60d-112">In the Credit field, specify the desired values.</span></span>
    * <span data-ttu-id="0e60d-113">Определенный счет ГК заменит счет ГК кредита в строке ваучера журнала и также будет использоваться для реверсирования расхода будущего периода на основе проводок начисления ГК.</span><span class="sxs-lookup"><span data-stu-id="0e60d-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="0e60d-114">В поле "Ваучер" выберите способ определения ваучера, когда выполняется разноска проводок.</span><span class="sxs-lookup"><span data-stu-id="0e60d-114">In the Voucher field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="0e60d-115">В поле "Описание" введите значение для описания проводок, которые будут разнесены.</span><span class="sxs-lookup"><span data-stu-id="0e60d-115">In the Description field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="0e60d-116">В поле "Частота периода" выберите, как часто должны происходить проводки.</span><span class="sxs-lookup"><span data-stu-id="0e60d-116">In the Period frequency field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="0e60d-117">В поле "Количество случаев по периоду" введите число.</span><span class="sxs-lookup"><span data-stu-id="0e60d-117">In the Number of occurrences by period field, enter a number.</span></span>
11. <span data-ttu-id="0e60d-118">В поле "Разнести проводки" выберите, когда проводки должны быть разнесены, например, ежемесячно.</span><span class="sxs-lookup"><span data-stu-id="0e60d-118">In the Post transactions field, select when the transactions should be posted, such as Monthly.</span></span>

