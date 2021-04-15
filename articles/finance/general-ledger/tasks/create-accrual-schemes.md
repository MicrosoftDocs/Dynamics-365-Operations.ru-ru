---
title: Создание схем начисления
description: В этом разделе описывается, как создать схему начисления.
author: aprilolson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41ea75b5c54f43efd4d5b9ef194e6394fc50bccc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815148"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="ed78b-103">Создание схем начисления</span><span class="sxs-lookup"><span data-stu-id="ed78b-103">Create accrual schemes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ed78b-104">В этом разделе описывается, как создать схему начисления.</span><span class="sxs-lookup"><span data-stu-id="ed78b-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="ed78b-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="ed78b-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="ed78b-106">Выберите **Область переходов > Модули > Главная книга > Настройки журнала > Схемы начисления**.</span><span class="sxs-lookup"><span data-stu-id="ed78b-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="ed78b-107">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ed78b-107">Select **New**.</span></span>
3. <span data-ttu-id="ed78b-108">В поле **Код начисления** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ed78b-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="ed78b-109">В поле **Описание схемы начислений** введите значение.</span><span class="sxs-lookup"><span data-stu-id="ed78b-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="ed78b-110">В поле **Дебет** укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="ed78b-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="ed78b-111">Определенный счет ГК заменит счет ГК дебета в строке ваучера журнала и также будет использоваться для реверсирования расхода будущего периода на основе проводок начисления ГК.</span><span class="sxs-lookup"><span data-stu-id="ed78b-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="ed78b-112">В поле **Кредит** укажите требуемые значения.</span><span class="sxs-lookup"><span data-stu-id="ed78b-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="ed78b-113">Определенный счет ГК заменит счет ГК кредита в строке ваучера журнала и также будет использоваться для реверсирования расхода будущего периода на основе проводок начисления ГК.</span><span class="sxs-lookup"><span data-stu-id="ed78b-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="ed78b-114">В поле **Ваучер** выберите способ определения ваучера, когда выполняется разноска проводок.</span><span class="sxs-lookup"><span data-stu-id="ed78b-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="ed78b-115">В поле **Описание** введите значение для описания проводок, которые будут разнесены.</span><span class="sxs-lookup"><span data-stu-id="ed78b-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="ed78b-116">В поле **Частота периода** выберите, как часто должны происходить проводки.</span><span class="sxs-lookup"><span data-stu-id="ed78b-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="ed78b-117">В поле **Количество случаев по периоду** введите число.</span><span class="sxs-lookup"><span data-stu-id="ed78b-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="ed78b-118">В поле **Разнести проводки** выберите, когда проводки должны быть разнесены, например, **Ежемесячно**.</span><span class="sxs-lookup"><span data-stu-id="ed78b-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]