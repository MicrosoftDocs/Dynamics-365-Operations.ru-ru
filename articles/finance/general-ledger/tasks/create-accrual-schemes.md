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
ms.openlocfilehash: a83870c4cec4de2e51e90ff1889d4beff6c23f95
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447279"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="e4411-103">Создание схем начисления</span><span class="sxs-lookup"><span data-stu-id="e4411-103">Create accrual schemes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e4411-104">В этом разделе описывается, как создать схему начисления.</span><span class="sxs-lookup"><span data-stu-id="e4411-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="e4411-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="e4411-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="e4411-106">Выберите **Область переходов > Модули > Главная книга > Настройки журнала > Схемы начисления**.</span><span class="sxs-lookup"><span data-stu-id="e4411-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="e4411-107">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="e4411-107">Select **New**.</span></span>
3. <span data-ttu-id="e4411-108">В поле **Код начисления** введите значение.</span><span class="sxs-lookup"><span data-stu-id="e4411-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="e4411-109">В поле **Описание схемы начислений** введите значение.</span><span class="sxs-lookup"><span data-stu-id="e4411-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="e4411-110">В поле **Дебет** укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="e4411-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="e4411-111">Определенный счет ГК заменит счет ГК дебета в строке ваучера журнала и также будет использоваться для реверсирования расхода будущего периода на основе проводок начисления ГК.</span><span class="sxs-lookup"><span data-stu-id="e4411-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="e4411-112">В поле **Кредит** укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="e4411-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="e4411-113">Определенный счет ГК заменит счет ГК кредита в строке ваучера журнала и также будет использоваться для реверсирования расхода будущего периода на основе проводок начисления ГК.</span><span class="sxs-lookup"><span data-stu-id="e4411-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="e4411-114">В поле **Ваучер** выберите способ определения ваучера, когда выполняется разноска проводок.</span><span class="sxs-lookup"><span data-stu-id="e4411-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="e4411-115">В поле **Описание** введите значение для описания проводок, которые будут разнесены.</span><span class="sxs-lookup"><span data-stu-id="e4411-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="e4411-116">В поле **Частота периода** выберите, как часто должны происходить проводки.</span><span class="sxs-lookup"><span data-stu-id="e4411-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="e4411-117">В поле **Количество случаев по периоду** введите число.</span><span class="sxs-lookup"><span data-stu-id="e4411-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="e4411-118">В поле **Разнести проводки** выберите, когда проводки должны быть разнесены, например, **Ежемесячно**.</span><span class="sxs-lookup"><span data-stu-id="e4411-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>

