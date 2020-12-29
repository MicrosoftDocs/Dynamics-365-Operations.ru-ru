---
title: Регистрация накладной поставщика в журнале накладных
description: В этом руководстве показано, как зарегистрировать накладные поставщика, которые не связаны с заказами на покупку.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9f2cbe0c9d1609aa3713776f81bafa396fff301
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645289"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="e03cc-103">Регистрация накладной поставщика в журнале накладных</span><span class="sxs-lookup"><span data-stu-id="e03cc-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e03cc-104">В этом руководстве показано, как зарегистрировать накладные поставщика, которые не связаны с заказами на покупку.</span><span class="sxs-lookup"><span data-stu-id="e03cc-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="e03cc-105">Примеры этого типа накладной включают расходы на поставки или услуги.</span><span class="sxs-lookup"><span data-stu-id="e03cc-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="e03cc-106">В данной записи используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="e03cc-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="e03cc-107">Перейдите к **Область перехода > Модули > Расчеты с поставщиками > Рабочие области > Запись накладной поставщика**.</span><span class="sxs-lookup"><span data-stu-id="e03cc-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="e03cc-108">В **Панели операций** щелкните **Создать журнал накладных**.</span><span class="sxs-lookup"><span data-stu-id="e03cc-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="e03cc-109">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="e03cc-109">Click **New**.</span></span>
4. <span data-ttu-id="e03cc-110">В поле **Имя** введите имя журнала или нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e03cc-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="e03cc-111">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="e03cc-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="e03cc-112">В **Панели операций** щелкните **Строки**.</span><span class="sxs-lookup"><span data-stu-id="e03cc-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="e03cc-113">В поле **Дата** введите дату разноски, в соответствии с которой будет обновлена главная книга.</span><span class="sxs-lookup"><span data-stu-id="e03cc-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="e03cc-114">В поле **Счет** выберите **Счет поставщика**.</span><span class="sxs-lookup"><span data-stu-id="e03cc-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="e03cc-115">В поле **Накладная** введите номер накладной.</span><span class="sxs-lookup"><span data-stu-id="e03cc-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="e03cc-116">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="e03cc-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="e03cc-117">В поле **Кредит** введите число.</span><span class="sxs-lookup"><span data-stu-id="e03cc-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="e03cc-118">В поле **Корр. счет** введите номер счета или нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e03cc-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="e03cc-119">По умолчанию в качестве значения **Налоговая группа** будет использоваться значение из счета поставщика.</span><span class="sxs-lookup"><span data-stu-id="e03cc-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="e03cc-120">По умолчанию в качестве значения **Налоговая группа номенклатур** будет использоваться значение из счета ГК, указанного в поле **Корр. счет**.</span><span class="sxs-lookup"><span data-stu-id="e03cc-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="e03cc-121">**Срок выполнения** будет рассчитан на основании условий оплаты.</span><span class="sxs-lookup"><span data-stu-id="e03cc-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="e03cc-122">По умолчанию в качестве значения **Скидка по оплате** будет использоваться значение из счета поставщика.</span><span class="sxs-lookup"><span data-stu-id="e03cc-122">The **Cash discount** will default from the Vendor account.</span></span>
12. <span data-ttu-id="e03cc-123">Если включен рабочий процесс журнала накладных поставщиков, щелкните **Рабочий процесс > Отправить**.</span><span class="sxs-lookup"><span data-stu-id="e03cc-123">If you have enabled Vendor invoice journal workflow, click **Workflow > Submit**.</span></span>
    * <span data-ttu-id="e03cc-124">Когда отправка утверждена, дата будет перемещена вперед до первого дня следующего открытого периода, если дата разноски проводки попадает в период, который находится на удержании или закрыт для разноски в книгу учета.</span><span class="sxs-lookup"><span data-stu-id="e03cc-124">When your submission is approved, the date will be advanced to the first day of the next open period, if the transaction posting date falls within a period that is On hold or Closed for ledger posting.</span></span>
12. <span data-ttu-id="e03cc-125">Щелкните **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="e03cc-125">Click **Post**.</span></span>
13. <span data-ttu-id="e03cc-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e03cc-126">Close the page.</span></span>

