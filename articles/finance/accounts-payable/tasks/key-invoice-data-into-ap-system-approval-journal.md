---
title: Ввод данных счета в модуль расчетов с поставщиками с использованием журнала утверждения
description: В этой теме показано, как использовать регистр накладных для создания накладных и последующего использования журнала утверждения для обновления счетов расходов.
author: abruer
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d01c04fcf707109cd7bc6f056846506914e96dec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838893"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="42477-103">Ввод данных счета в модуль расчетов с поставщиками с использованием журнала утверждения</span><span class="sxs-lookup"><span data-stu-id="42477-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="42477-104">В этой теме показано, как использовать регистр накладных для создания накладных и последующего использования журнала утверждения для обновления счетов расходов.</span><span class="sxs-lookup"><span data-stu-id="42477-104">This topic explains how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="42477-105">Создание и разноска накладной</span><span class="sxs-lookup"><span data-stu-id="42477-105">Create and post and invoice</span></span>
1. <span data-ttu-id="42477-106">В области переходов выберите **Модули > Расчеты с поставщиками > Накладные > Регистрация накладных**.</span><span class="sxs-lookup"><span data-stu-id="42477-106">In the navigation pan, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="42477-107">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="42477-107">Select **New**.</span></span>
3. <span data-ttu-id="42477-108">Выберите имя регистра накладных для использования.</span><span class="sxs-lookup"><span data-stu-id="42477-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="42477-109">Выберите **Строки**, чтобы открыть регистр и ввести строки расходов.</span><span class="sxs-lookup"><span data-stu-id="42477-109">Select **Lines** to open the register and enter expense lines.</span></span>
5. <span data-ttu-id="42477-110">Выберите поставщика.</span><span class="sxs-lookup"><span data-stu-id="42477-110">Select a vendor.</span></span> <span data-ttu-id="42477-111">Например, введите или выберите `US-104`.</span><span class="sxs-lookup"><span data-stu-id="42477-111">For example, enter or select `US-104`.</span></span>
6. <span data-ttu-id="42477-112">В поле **Накладная** введите значение.</span><span class="sxs-lookup"><span data-stu-id="42477-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="42477-113">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="42477-113">In the **Description** field, type a value.</span></span>
8. <span data-ttu-id="42477-114">В поле **Кредит** введите число.</span><span class="sxs-lookup"><span data-stu-id="42477-114">In the **Credit** field, enter a number.</span></span>
9. <span data-ttu-id="42477-115">В поле **Кем утверждено** выберите утверждающего в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="42477-115">In the **Approved by** field, select an approver from the drop-down menu.</span></span>
10. <span data-ttu-id="42477-116">Выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="42477-116">Select **Post**.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="42477-117">Утверждение накладной</span><span class="sxs-lookup"><span data-stu-id="42477-117">Approve an invoice</span></span>
1. <span data-ttu-id="42477-118">В области переходов выберите **Модули > Расчеты с поставщиками > Накладные > Утверждение накладной**.</span><span class="sxs-lookup"><span data-stu-id="42477-118">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice approval**.</span></span>
2. <span data-ttu-id="42477-119">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="42477-119">Select **New**.</span></span>
3. <span data-ttu-id="42477-120">Выберите имя журнала утверждений накладных для использования.</span><span class="sxs-lookup"><span data-stu-id="42477-120">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="42477-121">Выберите **Строки** для отображения страницы, на которой можно будет выбрать накладные, которые требуется утвердить.</span><span class="sxs-lookup"><span data-stu-id="42477-121">Select **Lines** to display a page where you will be able to select the invoices that you want to approve.</span></span>
5. <span data-ttu-id="42477-122">Выберите **Найти ваучеры** для отображения всех накладных, готовых к утверждению.</span><span class="sxs-lookup"><span data-stu-id="42477-122">Select **Find Vouchers** to display all of the invoices that are ready for approval.</span></span>
6. <span data-ttu-id="42477-123">Отметьте созданную накладную, затем щелкните **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="42477-123">Mark the invoice that you created, then click **Select**.</span></span> <span data-ttu-id="42477-124">Выбранные выше ваучеры перемещаются в этот список после их выбора.</span><span class="sxs-lookup"><span data-stu-id="42477-124">The vouchers that you selected above are moved to this list after you select them.</span></span>  
7. <span data-ttu-id="42477-125">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="42477-125">Select **OK**.</span></span>
8. <span data-ttu-id="42477-126">Выберите поле **Номер счета** для добавления счета расходов в накладную.</span><span class="sxs-lookup"><span data-stu-id="42477-126">Select the **account number** field to add an expense account to the invoice.</span></span>
9. <span data-ttu-id="42477-127">Введите номер счета и выйдите из поля.</span><span class="sxs-lookup"><span data-stu-id="42477-127">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="42477-128">Например, введите `600120`.</span><span class="sxs-lookup"><span data-stu-id="42477-128">For example, enter `600120`.</span></span>
10. <span data-ttu-id="42477-129">Выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="42477-129">Select **Post**.</span></span>
11. <span data-ttu-id="42477-130">Выберите **Ваучер** для просмотра разнесенных записей.</span><span class="sxs-lookup"><span data-stu-id="42477-130">Select **Voucher** to view the entries that were posted.</span></span> <span data-ttu-id="42477-131">Счет утверждения ожидающих накладных реверсируется и заменяется на счет фактических расходов.</span><span class="sxs-lookup"><span data-stu-id="42477-131">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]