---
title: Создание схем начисления
description: В этом разделе описывается, как создать схему начисления.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e8f8cf8546187ae1c65d4966887e1c5842dff431
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175604"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="6da5a-103">Создание схем начисления</span><span class="sxs-lookup"><span data-stu-id="6da5a-103">Create accrual schemes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6da5a-104">В этом разделе описывается, как создать схему начисления.</span><span class="sxs-lookup"><span data-stu-id="6da5a-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="6da5a-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="6da5a-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="6da5a-106">Выберите **Область переходов > Модули > Главная книга > Настройки журнала > Схемы начисления**.</span><span class="sxs-lookup"><span data-stu-id="6da5a-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="6da5a-107">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="6da5a-107">Select **New**.</span></span>
3. <span data-ttu-id="6da5a-108">В поле **Код начисления** введите значение.</span><span class="sxs-lookup"><span data-stu-id="6da5a-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="6da5a-109">В поле **Описание схемы начислений** введите значение.</span><span class="sxs-lookup"><span data-stu-id="6da5a-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="6da5a-110">В поле **Дебет** укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6da5a-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="6da5a-111">Определенный счет ГК заменит счет ГК дебета в строке ваучера журнала и также будет использоваться для реверсирования расхода будущего периода на основе проводок начисления ГК.</span><span class="sxs-lookup"><span data-stu-id="6da5a-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="6da5a-112">В поле **Кредит** укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="6da5a-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="6da5a-113">Определенный счет ГК заменит счет ГК кредита в строке ваучера журнала и также будет использоваться для реверсирования расхода будущего периода на основе проводок начисления ГК.</span><span class="sxs-lookup"><span data-stu-id="6da5a-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="6da5a-114">В поле **Ваучер** выберите способ определения ваучера, когда выполняется разноска проводок.</span><span class="sxs-lookup"><span data-stu-id="6da5a-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="6da5a-115">В поле **Описание** введите значение для описания проводок, которые будут разнесены.</span><span class="sxs-lookup"><span data-stu-id="6da5a-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="6da5a-116">В поле **Частота периода** выберите, как часто должны происходить проводки.</span><span class="sxs-lookup"><span data-stu-id="6da5a-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="6da5a-117">В поле **Количество случаев по периоду** введите число.</span><span class="sxs-lookup"><span data-stu-id="6da5a-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="6da5a-118">В поле **Разнести проводки** выберите, когда проводки должны быть разнесены, например, **Ежемесячно**.</span><span class="sxs-lookup"><span data-stu-id="6da5a-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>

