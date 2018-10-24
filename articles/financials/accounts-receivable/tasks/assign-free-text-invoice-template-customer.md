--- 
title: "Назначение шаблона накладной с произвольным текстом клиенту"
description: "В этой задаче показано, как назначить шаблон накладной с произвольным текстом клиенту."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 317b3bd4c1f395987ef3dbbd268c40be5c688320
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="assign-free-text-invoice-template-to-a-customer"></a><span data-ttu-id="3db20-103">Назначение шаблона накладной с произвольным текстом клиенту</span><span class="sxs-lookup"><span data-stu-id="3db20-103">Assign free text invoice template to a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3db20-104">В этой задаче показано, как назначить шаблон накладной с произвольным текстом клиенту.</span><span class="sxs-lookup"><span data-stu-id="3db20-104">This task demonstrates how to assign a free text invoice template to a customer.</span></span> <span data-ttu-id="3db20-105">В этой задаче используется демонстрационная компания USMF и задача предназначена для пользователя, ответственного за обработку накладных расчетов с клиентами и управление ими.</span><span class="sxs-lookup"><span data-stu-id="3db20-105">This task uses the USMF demo company and is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="3db20-106">Перейдите в раздел "Расчеты с клиентами" > "Клиенты" > "Все клиенты".</span><span class="sxs-lookup"><span data-stu-id="3db20-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="3db20-107">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="3db20-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3db20-108">В области действий щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="3db20-108">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="3db20-109">Щелкните "Периодические накладные".</span><span class="sxs-lookup"><span data-stu-id="3db20-109">Click Recurring invoices.</span></span>
    * <span data-ttu-id="3db20-110">Данная страница используется для назначения шаблонов накладной с произвольным текстом клиенту и указания способа отправки накладных клиенту.</span><span class="sxs-lookup"><span data-stu-id="3db20-110">Use this page to assign free text invoice templates to customers and specify how frequently invoices will be sent to the customer.</span></span>  
5. <span data-ttu-id="3db20-111">Нажмите кнопку "Создать", чтобы назначить новый шаблон клиенту.</span><span class="sxs-lookup"><span data-stu-id="3db20-111">Click New to assign a new template to the customer.</span></span>
6. <span data-ttu-id="3db20-112">Выберите шаблон накладной с произвольным текстом, который требуется назначить клиенту.</span><span class="sxs-lookup"><span data-stu-id="3db20-112">Select the free text invoice template you want to assign to the customer.</span></span>
7. <span data-ttu-id="3db20-113">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="3db20-113">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="3db20-114">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="3db20-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="3db20-115">Введите дату, в которую будет создана первая накладная.</span><span class="sxs-lookup"><span data-stu-id="3db20-115">Enter the date when the first invoice will be generated.</span></span>
    * <span data-ttu-id="3db20-116">Введите повторяющуюся дату окончания.</span><span class="sxs-lookup"><span data-stu-id="3db20-116">Enter a recurring end date.</span></span>  
    * <span data-ttu-id="3db20-117">Выберите один из следующих вариантов: "Дата завершения не указана" — накладные будут создаваться бесконечно, пока шаблон не будет удален из счета клиента.</span><span class="sxs-lookup"><span data-stu-id="3db20-117">Select one of the following: No end date – Invoices will be generated indefinitely until the template is removed from the customer account.</span></span>  <span data-ttu-id="3db20-118">"Дата окончания выставления счетов" — выберите этот параметр и введите последнюю дату, когда можно создать накладную.</span><span class="sxs-lookup"><span data-stu-id="3db20-118">Billing end date – Select this option and enter the last date that the invoice can be generated.</span></span>  
    * <span data-ttu-id="3db20-119">Максимальная общая сумма, после которой накладные больше не будут создаваться.</span><span class="sxs-lookup"><span data-stu-id="3db20-119">Maximum cumulative amount after which invoice generation will stop.</span></span>  
    * <span data-ttu-id="3db20-120">Максимальная общая сумма, которую можно достичь с использованием выбранного шаблона.</span><span class="sxs-lookup"><span data-stu-id="3db20-120">Enter the maximum cumulative amount that can be reached using the selected template.</span></span> <span data-ttu-id="3db20-121">Например, если ввести 1000,00 и создать ежемесячные накладные по 100,00 каждая, накладные больше не будут создаваться после создания десяти накладных.</span><span class="sxs-lookup"><span data-stu-id="3db20-121">For example, if you enter 1,000.00 and generate monthly invoices for 100.00 each, invoices will stop generating after the tenth invoice is generated.</span></span>  
    * <span data-ttu-id="3db20-122">Создайте периодические накладные с помощью значений по умолчанию из шаблона накладной с произвольным текстом или счета клиента.</span><span class="sxs-lookup"><span data-stu-id="3db20-122">Generate recurring invoices by using the default values from either free text invoice template or the customer account.</span></span>  
    * <span data-ttu-id="3db20-123">Выберите, использовать ли шаблон накладной с произвольным текстом или счет клиента для определения значений по умолчанию для языка, профиля разноски, налоговой группы, налоговой группы номенклатур, кода списка, страны/региона для поставки, валюты, условий оплаты, способа оплаты, спецификации платежа, графика оплаты, скидки по оплате, финансовых аналитик и квитанции о переводе денег с жиросчета, когда накладные создаются.</span><span class="sxs-lookup"><span data-stu-id="3db20-123">Select whether to use the free text invoice template or the customer account to determine the default values for the language, posting profile, sales tax group, item sales tax group, list code, country/region for delivery, currency, terms of payment, method of payment, payment specification, payment schedule, cash discount, financial dimensions, and giro money transfer slip when invoices are created.</span></span>  
10. <span data-ttu-id="3db20-124">Выберите шаблон повторения.</span><span class="sxs-lookup"><span data-stu-id="3db20-124">Select the recurrence pattern.</span></span>
    * <span data-ttu-id="3db20-125">"Ежедневно" — выберите этот параметр и введите число дней в поле "На".</span><span class="sxs-lookup"><span data-stu-id="3db20-125">Daily – Select this option and enter the number of days in the Per field.</span></span> <span data-ttu-id="3db20-126">Например, если ввести 15, накладная будет произведена каждые 15 дней для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="3db20-126">For example, if you enter 15, an invoice will be generated every 15 days for this customer.</span></span>  <span data-ttu-id="3db20-127">"Еженедельно" — выберите этот параметр и введите число недель в поле "На".</span><span class="sxs-lookup"><span data-stu-id="3db20-127">Weekly - Select this option and enter the number of weeks in the Per field.</span></span> <span data-ttu-id="3db20-128">Например, если ввести 2, накладная будет произведена каждые две недели для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="3db20-128">For example, if you enter 2, an invoice will be generated every two weeks for this customer.</span></span>  <span data-ttu-id="3db20-129">"Ежемесячно" — выберите этот параметр и введите число месяцев в поле "На".</span><span class="sxs-lookup"><span data-stu-id="3db20-129">Monthly - Select this option and enter the number of months in the Per field.</span></span> <span data-ttu-id="3db20-130">Например, если ввести 6, накладная будет произведена каждые шесть месяцев для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="3db20-130">For example, if you enter 6, an invoice will be generated every six months for this customer.</span></span>  <span data-ttu-id="3db20-131">"Ежегодно" — выберите этот параметр и введите число лет в поле "На".</span><span class="sxs-lookup"><span data-stu-id="3db20-131">Yearly – Select this option and enter the number of years in the Per field.</span></span> <span data-ttu-id="3db20-132">Например, если ввести 2, накладная будет произведена каждые две года для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="3db20-132">For example, if you enter 2, an invoice will be generated every two years for this customer.</span></span>  
11. <span data-ttu-id="3db20-133">В поле "На" введите число.</span><span class="sxs-lookup"><span data-stu-id="3db20-133">In the Per field, enter a number.</span></span>


