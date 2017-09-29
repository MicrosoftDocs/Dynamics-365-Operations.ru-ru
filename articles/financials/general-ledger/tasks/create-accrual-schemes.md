--- 
title: "Создание схем начисления"
description: "В этом руководства рассказывается о создании схемы начисления."
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 324be23a1e26de0d05c7cf6a61567f7260d0c390
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="create-accrual-schemes"></a><span data-ttu-id="c58cb-103">Создание схем начисления</span><span class="sxs-lookup"><span data-stu-id="c58cb-103">Create accrual schemes</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c58cb-104">В этом руководства рассказывается о создании схемы начисления.</span><span class="sxs-lookup"><span data-stu-id="c58cb-104">This task guide steps through creating an accrual scheme.</span></span> <span data-ttu-id="c58cb-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="c58cb-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="c58cb-106">Перейдите в раздел "Главная книга" > "Настройка журнала" > "Схема начисления".</span><span class="sxs-lookup"><span data-stu-id="c58cb-106">Go to General ledger > Journal setup > Accrual schemes.</span></span>
2. <span data-ttu-id="c58cb-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="c58cb-107">Click New.</span></span>
3. <span data-ttu-id="c58cb-108">В поле "Код начисления" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c58cb-108">In the Accrual identification field, type a value.</span></span>
4. <span data-ttu-id="c58cb-109">В поле "Описание схемы начислений" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c58cb-109">In the Description of accrual scheme field, type a value.</span></span>
5. <span data-ttu-id="c58cb-110">В поле "Дебет" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="c58cb-110">In the Debit field, specify the desired values.</span></span>
    * <span data-ttu-id="c58cb-111">Определенный счет ГК заменит счет ГК дебета в строке ваучера журнала и также будет использоваться для реверсирования расхода будущего периода на основе проводок начисления ГК.</span><span class="sxs-lookup"><span data-stu-id="c58cb-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="c58cb-112">В поле "Кредит" укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="c58cb-112">In the Credit field, specify the desired values.</span></span>
    * <span data-ttu-id="c58cb-113">Определенный счет ГК заменит счет ГК кредита в строке ваучера журнала и также будет использоваться для реверсирования расхода будущего периода на основе проводок начисления ГК.</span><span class="sxs-lookup"><span data-stu-id="c58cb-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="c58cb-114">В поле "Ваучер" выберите способ определения ваучера, когда выполняется разноска проводок.</span><span class="sxs-lookup"><span data-stu-id="c58cb-114">In the Voucher field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="c58cb-115">В поле "Описание" введите значение для описания проводок, которые будут разнесены.</span><span class="sxs-lookup"><span data-stu-id="c58cb-115">In the Description field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="c58cb-116">В поле "Частота периода" выберите, как часто должны происходить проводки.</span><span class="sxs-lookup"><span data-stu-id="c58cb-116">In the Period frequency field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="c58cb-117">В поле "Количество случаев по периоду" введите число.</span><span class="sxs-lookup"><span data-stu-id="c58cb-117">In the Number of occurrences by period field, enter a number.</span></span>
11. <span data-ttu-id="c58cb-118">В поле "Разнести проводки" выберите, когда проводки должны быть разнесены, например, ежемесячно.</span><span class="sxs-lookup"><span data-stu-id="c58cb-118">In the Post transactions field, select when the transactions should be posted, such as Monthly.</span></span>


