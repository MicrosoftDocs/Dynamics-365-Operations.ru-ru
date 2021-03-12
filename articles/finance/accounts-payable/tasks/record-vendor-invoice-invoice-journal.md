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
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 18d8b74bd8783c23e548a3185414d1461bc1d869
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971836"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="f7bca-103">Регистрация накладной поставщика в журнале накладных</span><span class="sxs-lookup"><span data-stu-id="f7bca-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7bca-104">В этом руководстве показано, как зарегистрировать накладные поставщика, которые не связаны с заказами на покупку.</span><span class="sxs-lookup"><span data-stu-id="f7bca-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="f7bca-105">Примеры этого типа накладной включают расходы на поставки или услуги.</span><span class="sxs-lookup"><span data-stu-id="f7bca-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="f7bca-106">В данной записи используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="f7bca-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="f7bca-107">Перейдите к **Область перехода > Модули > Расчеты с поставщиками > Рабочие области > Запись накладной поставщика**.</span><span class="sxs-lookup"><span data-stu-id="f7bca-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="f7bca-108">В **Панели операций** щелкните **Создать журнал накладных**.</span><span class="sxs-lookup"><span data-stu-id="f7bca-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="f7bca-109">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f7bca-109">Click **New**.</span></span>
4. <span data-ttu-id="f7bca-110">В поле **Имя** введите имя журнала или нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f7bca-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="f7bca-111">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="f7bca-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="f7bca-112">В **Панели операций** щелкните **Строки**.</span><span class="sxs-lookup"><span data-stu-id="f7bca-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="f7bca-113">В поле **Дата** введите дату разноски, в соответствии с которой будет обновлена главная книга.</span><span class="sxs-lookup"><span data-stu-id="f7bca-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="f7bca-114">В поле **Счет** выберите **Счет поставщика**.</span><span class="sxs-lookup"><span data-stu-id="f7bca-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="f7bca-115">В поле **Накладная** введите номер накладной.</span><span class="sxs-lookup"><span data-stu-id="f7bca-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="f7bca-116">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="f7bca-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="f7bca-117">В поле **Кредит** введите число.</span><span class="sxs-lookup"><span data-stu-id="f7bca-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="f7bca-118">В поле **Корр. счет** введите номер счета или нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="f7bca-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="f7bca-119">По умолчанию в качестве значения **Налоговая группа** будет использоваться значение из счета поставщика.</span><span class="sxs-lookup"><span data-stu-id="f7bca-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="f7bca-120">По умолчанию в качестве значения **Налоговая группа номенклатур** будет использоваться значение из счета ГК, указанного в поле **Корр. счет**.</span><span class="sxs-lookup"><span data-stu-id="f7bca-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="f7bca-121">**Срок выполнения** будет рассчитан на основании условий оплаты.</span><span class="sxs-lookup"><span data-stu-id="f7bca-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="f7bca-122">По умолчанию в качестве значения **Скидка по оплате** будет использоваться значение из счета поставщика.</span><span class="sxs-lookup"><span data-stu-id="f7bca-122">The **Cash discount** will default from the Vendor account.</span></span>
12. <span data-ttu-id="f7bca-123">Если включен рабочий процесс журнала накладных поставщиков, щелкните **Рабочий процесс > Отправить**.</span><span class="sxs-lookup"><span data-stu-id="f7bca-123">If you have enabled Vendor invoice journal workflow, click **Workflow > Submit**.</span></span>
    * <span data-ttu-id="f7bca-124">Когда отправка утверждена, дата будет перемещена вперед до первого дня следующего открытого периода, если дата разноски проводки попадает в период, который находится на удержании или закрыт для разноски в книгу учета.</span><span class="sxs-lookup"><span data-stu-id="f7bca-124">When your submission is approved, the date will be advanced to the first day of the next open period, if the transaction posting date falls within a period that is On hold or Closed for ledger posting.</span></span>
12. <span data-ttu-id="f7bca-125">Щелкните **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="f7bca-125">Click **Post**.</span></span>
13. <span data-ttu-id="f7bca-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f7bca-126">Close the page.</span></span>

