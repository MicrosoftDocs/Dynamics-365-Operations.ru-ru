--- 
title: "Регистрация накладной поставщика в журнале накладных"
description: "В этом руководстве показано, как зарегистрировать накладные поставщика, которые не связаны с заказами на покупку."
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 42f93e6d8fcf62babc3e3244bc1fe76d1efd9d13
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="8b65b-103">Регистрация накладной поставщика в журнале накладных</span><span class="sxs-lookup"><span data-stu-id="8b65b-103">Record a vendor invoice in the invoice journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8b65b-104">В этом руководстве показано, как зарегистрировать накладные поставщика, которые не связаны с заказами на покупку.</span><span class="sxs-lookup"><span data-stu-id="8b65b-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="8b65b-105">Примеры этого типа накладной включают расходы на поставки или услуги.</span><span class="sxs-lookup"><span data-stu-id="8b65b-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="8b65b-106">В данной записи используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="8b65b-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="8b65b-107">Перейдите в раздел "Расчеты с поставщиками" > "Рабочие области" > "Запись накладной поставщика".</span><span class="sxs-lookup"><span data-stu-id="8b65b-107">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="8b65b-108">Щелкните "Новый журнал накладных".</span><span class="sxs-lookup"><span data-stu-id="8b65b-108">Click New invoice journal.</span></span>
3. <span data-ttu-id="8b65b-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8b65b-109">Click New.</span></span>
4. <span data-ttu-id="8b65b-110">В поле "Имя" введите имя журнала или нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8b65b-110">In the Name field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="8b65b-111">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8b65b-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="8b65b-112">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="8b65b-112">Click Lines.</span></span>
    * <span data-ttu-id="8b65b-113">В поле "Дата" введите дату разноски, в соответствии с которой будет обновлена главная книга.</span><span class="sxs-lookup"><span data-stu-id="8b65b-113">In the Date field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="8b65b-114">В поле "Счет" выберите счет поставщика.</span><span class="sxs-lookup"><span data-stu-id="8b65b-114">In the Account field, specify the Vendor account.</span></span>
8. <span data-ttu-id="8b65b-115">В поле Накладная введите номер накладной.</span><span class="sxs-lookup"><span data-stu-id="8b65b-115">In the Invoice field, enter the invoice number.</span></span>
9. <span data-ttu-id="8b65b-116">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="8b65b-116">In the Description field, type a value.</span></span>
10. <span data-ttu-id="8b65b-117">В поле "Кредит" введите число.</span><span class="sxs-lookup"><span data-stu-id="8b65b-117">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="8b65b-118">В поле "Корр. счет" введите номер счета или нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="8b65b-118">In the Offset account field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="8b65b-119">По умолчанию в качестве значения "Налоговая группа" будет использоваться значение из счета поставщика.</span><span class="sxs-lookup"><span data-stu-id="8b65b-119">The Sales tax group will default from the vendor account.</span></span>  
    * <span data-ttu-id="8b65b-120">По умолчанию в качестве значения "Налоговая группа номенклатур" будет использоваться значение из счета ГК, указанного в поле "Корр. счет".</span><span class="sxs-lookup"><span data-stu-id="8b65b-120">The Item sales tax group will default from the main account specified in the Offset account field.</span></span>  
    * <span data-ttu-id="8b65b-121">Срок выполнения будет рассчитан на основании условий оплаты.</span><span class="sxs-lookup"><span data-stu-id="8b65b-121">The Due date will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="8b65b-122">По умолчанию в качестве значения "Скидка по оплате" будет использоваться значение из счета поставщика.</span><span class="sxs-lookup"><span data-stu-id="8b65b-122">The Cash discount will default from the Vendor account.</span></span>  
12. <span data-ttu-id="8b65b-123">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="8b65b-123">Click Post.</span></span>
13. <span data-ttu-id="8b65b-124">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8b65b-124">Close the page.</span></span>


