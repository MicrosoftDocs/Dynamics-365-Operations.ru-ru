---
title: Приход РБП
description: В этом разделе объясняется, как создавать и разносить проводки поступления для РБП, которые были созданы вручную. В нем также объясняется, как реверсировать проводки поступления.
author: anasyash
manager: AnnBe
ms.date: 06/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.author: anasyash
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 2c9b68253e559f6bcd85633e954966185b27fdaf
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552344"
---
# <a name="receipt-of-deferrals"></a><span data-ttu-id="16f6d-104">Поступление РБП</span><span class="sxs-lookup"><span data-stu-id="16f6d-104">Receipt of deferrals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16f6d-105">Для создания проводки поступления для РБП, созданных вручную, используется страница **Ваучер журнала**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-105">You use the **Journal voucher** page to create a receipt transaction for deferrals that were manually created.</span></span> <span data-ttu-id="16f6d-106">При разноске проводки поступления, статус РБП обновляется до **В работе**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-106">When you post the receipt transaction, the status of the deferrals is updated to **In process**.</span></span>

1. <span data-ttu-id="16f6d-107">Перейдите к **Главная книга** \> **Записи в журнале** \> **Журнал расходов будущих периодов**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-107">Go to **General ledger** \> **Journal entries** \> **Deferrals journal**.</span></span>
2. <span data-ttu-id="16f6d-108">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-108">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="16f6d-109">В поле **Имя** выберите имя журнала.</span><span class="sxs-lookup"><span data-stu-id="16f6d-109">In the **Name** field, select a journal name.</span></span>
4. <span data-ttu-id="16f6d-110">В области действий выберите **Строки**, чтобы открыть страницу **Ваучер журнала**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-110">On the Action Pane, select **Lines** to open the **Journal voucher** page.</span></span>
5. <span data-ttu-id="16f6d-111">На вкладке **Обзор** выберите **Создать**, чтобы создать новую строку.</span><span class="sxs-lookup"><span data-stu-id="16f6d-111">On the **Overview** tab, select **New** to create a line.</span></span>
6. <span data-ttu-id="16f6d-112">Выберите дату проводки в поле **Дата проводки**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-112">In the **Transaction date** field, select the transaction date.</span></span>
7. <span data-ttu-id="16f6d-113">В поле **Тип транзакции** выберите **Поступление**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-113">In the **Transaction type** field, select **Receipt**.</span></span>
8. <span data-ttu-id="16f6d-114">В поле **Идентификатор РБП** выберите РБП, чтобы создать проводку поступления для него.</span><span class="sxs-lookup"><span data-stu-id="16f6d-114">In the **Deferral ID** field, select the deferral to create a receipt transaction for.</span></span>
9. <span data-ttu-id="16f6d-115">В поле **Номер модели** выберите номер модели для РБП.</span><span class="sxs-lookup"><span data-stu-id="16f6d-115">In the **Model number** field, select the model number for the deferral.</span></span>
10. <span data-ttu-id="16f6d-116">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-116">Select **OK**.</span></span> <span data-ttu-id="16f6d-117">Строки ваучера создаются для выбранного РБП на странице **Ваучер журнала**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-117">Voucher lines are created for the selected deferral on the **Journal voucher** page.</span></span>

    <span data-ttu-id="16f6d-118">Для РБП создается проводка типа **Поступление**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-118">A transaction of the **Receipt** type is created for the deferral.</span></span> <span data-ttu-id="16f6d-119">Эта проводка имеет указанную дату поступления.</span><span class="sxs-lookup"><span data-stu-id="16f6d-119">This transaction has the specified receipt date.</span></span>

    ![Страница Ваучера журнала](media/rus-deferral-transactions-01.png)

11. <span data-ttu-id="16f6d-121">На панели операций выберите **Проверить** \> **Проверить** а затем **Разнести** \> **Разнести** для проверки и разноски журнала.</span><span class="sxs-lookup"><span data-stu-id="16f6d-121">On the Action Pane, select **Validate** \> **Validate** and then **Post** \> **Post** to validate and post the journal.</span></span>
12. <span data-ttu-id="16f6d-122">Перейдите к **Главная книга** \> **Расходы будущих периодов** \> **Расходы будущих периодов** для просмотра создаваемых РБП.</span><span class="sxs-lookup"><span data-stu-id="16f6d-122">Go to **General ledger** \> **Deferrals** \> **Deferrals** to view the deferrals that are generated.</span></span> <span data-ttu-id="16f6d-123">Для просмотра сведений о проводках на странице **Проводки по РБП**, на панели операций выберите **Модели РБП**, а затем выберите **Проводки**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-123">To view the transaction details on the **Deferrals transactions** page, on the Action Pane, select **Deferrals models**, and then select **Transactions**.</span></span>

## <a name="reverse-a-receipt-transaction"></a><span data-ttu-id="16f6d-124">Реверсирование проводки поступления</span><span class="sxs-lookup"><span data-stu-id="16f6d-124">Reverse a receipt transaction</span></span>

<span data-ttu-id="16f6d-125">Для реверсирования проводки поступления для РБП, созданной вручную, используется страница **Реверсирующая проводка**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-125">You use the **Reverse transaction** page to reverse a receipt transaction that was manually created for deferrals.</span></span> <span data-ttu-id="16f6d-126">Проводки поступления, созданные с помощью периодической задачи, можно реверсировать.</span><span class="sxs-lookup"><span data-stu-id="16f6d-126">Receipt transactions that are generated by using the periodic task can be reversed.</span></span> <span data-ttu-id="16f6d-127">Однако другие проводки ГК, созданные в рамках периодической задачи, необходимо вручную реверсировать в журнале главной книги.</span><span class="sxs-lookup"><span data-stu-id="16f6d-127">However, the other general ledger transactions that are created during the periodic task must be manually reversed in the general ledger journal.</span></span>

<span data-ttu-id="16f6d-128">РБП, созданные после выбытия основного средства, реверсируются, когда реверсируется проводка основных средств.</span><span class="sxs-lookup"><span data-stu-id="16f6d-128">Deferrals that are created after the fixed asset is disposed of are reversed when the fixed asset transaction is reversed.</span></span>

1. <span data-ttu-id="16f6d-129">Перейти к **главная книга** \> **Расходы будущих периодов** \> **Расходы будущих периодов**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-129">Go to **General ledger** \> **Deferrals** \> **Deferrals**.</span></span>
2. <span data-ttu-id="16f6d-130">Выберите идентификатор РБП, а затем, на панели операций на вкладке **Расходы будущих периодов** в группе **Книги** выберите **Модели РБП**, чтобы открыть страницу **Модели РБП**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-130">Select a deferral ID, and then, on the Action Pane, on the **Deferrals** tab, in the **Books** group, select **Deferrals models** to open the **Deferrals models** page.</span></span>
3. <span data-ttu-id="16f6d-131">Выберите модель РБП, а затем на панели операций выберите **Проводки**, чтобы открыть страницу **Проводки по РБП**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-131">Select a deferrals model, and then, on the Action Pane, select **Transactions** to open the **Deferrals transactions** page.</span></span>
4. <span data-ttu-id="16f6d-132">Выберите проводку поступления для реверсирования, а затем, на панели операций выберите **Реверсирующая проводка**, чтобы открыть диалоговое окно **Реверсирующая проводка**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-132">Select the receipt transaction to reverse, and then, on the Action Pane, select **Reverse transaction** to open the **Reverse transaction** dialog box.</span></span>
5. <span data-ttu-id="16f6d-133">В поле **Дата сторно** выберите дату реверсирования.</span><span class="sxs-lookup"><span data-stu-id="16f6d-133">In the **Date of storno** field, select the reversal date.</span></span> <span data-ttu-id="16f6d-134">Все проводки, созданные на эту дату, реверсируются.</span><span class="sxs-lookup"><span data-stu-id="16f6d-134">All transactions that are created on this date are reversed.</span></span>
6. <span data-ttu-id="16f6d-135">Установите флажок **По всем моделям**, чтобы реверсировать проводки, созданные с помощью налоговой модели учета и базовой модели учета.</span><span class="sxs-lookup"><span data-stu-id="16f6d-135">Select the **By all models** check box to reverse transactions that are created by using the tax value model and the base value model.</span></span>
7. <span data-ttu-id="16f6d-136">Выберите **ОК**, чтобы реверсировать проводку.</span><span class="sxs-lookup"><span data-stu-id="16f6d-136">Select **OK** to reverse the transaction.</span></span>
