---
title: "Указание кросс-курса"
description: "В этой теме представлены сведения о Кросс-курсах в Microsoft Dynamics 365 for Finance and Operations."
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cf531c3a8f3bdb17314d1de436b98249169f82a3
ms.openlocfilehash: 112f77738b33aae94babe0cf8e9e61ff2ea3d004
ms.contentlocale: ru-ru
ms.lasthandoff: 05/22/2018

---

# <a name="specify-the-cross-rate"></a><span data-ttu-id="ef2cc-103">Указание кросс-курса</span><span class="sxs-lookup"><span data-stu-id="ef2cc-103">Specify the cross rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef2cc-104">В этом разделе описывается цель кросс-курса и процедура задания кросс-курса при сопоставлении платежа с накладной.</span><span class="sxs-lookup"><span data-stu-id="ef2cc-104">This topic explains the purpose of a cross rate, and how to specify the cross rate when you settle a payment with an invoice.</span></span> <span data-ttu-id="ef2cc-105">Используйте кросс-курс, когда соблюдаются все следующие условия.</span><span class="sxs-lookup"><span data-stu-id="ef2cc-105">Use a cross rate when all of the following criteria apply:</span></span> 
-   <span data-ttu-id="ef2cc-106">Платеж сопоставляется с накладной.</span><span class="sxs-lookup"><span data-stu-id="ef2cc-106">You are settling a payment with an invoice.</span></span> 
-   <span data-ttu-id="ef2cc-107">В строке платежа и строке накладной используются разные валюты.</span><span class="sxs-lookup"><span data-stu-id="ef2cc-107">The payment line and the invoice line use different currencies.</span></span> 
-   <span data-ttu-id="ef2cc-108">Ни одна из валют не является валютой учета.</span><span class="sxs-lookup"><span data-stu-id="ef2cc-108">Neither currency is the accounting currency.</span></span> 

<span data-ttu-id="ef2cc-109">Кросс-курс не используется для вычисления трансляции валюты транзакции платежа в валюту учета платежа.</span><span class="sxs-lookup"><span data-stu-id="ef2cc-109">The cross rate is not used to calculate the payment transaction currency translation to the payment accounting currency.</span></span> <span data-ttu-id="ef2cc-110">Вместо этого извлекаются валютные курсы из таблиц валютных курсов, чтобы вычислить значение суммы в валюте транзакции по оплате и значение суммы в валюте для учета платежа.</span><span class="sxs-lookup"><span data-stu-id="ef2cc-110">Instead, the exchange rates from the exchange rate tables are retrieved to calculate the value of the payment transaction currency amount and the payment accounting currency amount.</span></span> 

<span data-ttu-id="ef2cc-111">Например, валюта учета — американский доллар, валюта накладной — канадский доллар, а валюта платежа — евро.</span><span class="sxs-lookup"><span data-stu-id="ef2cc-111">For example, the accounting currency is USD, the invoice currency is CAD, and the payment currency is EUR.</span></span> <span data-ttu-id="ef2cc-112">Кросс-курс позволяет ввести валютный курс для конвертации непосредственно из канадского доллара в евро, минуя американский доллар.</span><span class="sxs-lookup"><span data-stu-id="ef2cc-112">The cross rate lets you enter an exchange rate to translate directly between CAD and EUR, and not have to translate through USD.</span></span> <span data-ttu-id="ef2cc-113">Выбирая накладную и основной платеж, можно ввести кросс-курс для строки накладной.</span><span class="sxs-lookup"><span data-stu-id="ef2cc-113">When you select an invoice and a primary payment, you can enter a cross rate for the invoice line.</span></span> <span data-ttu-id="ef2cc-114">Кросс-курс - это обменный курс между валютами для этих проводок на дату сопоставления.</span><span class="sxs-lookup"><span data-stu-id="ef2cc-114">The cross rate is the exchange rate between the currencies for those transactions, as of the settlement date.</span></span>

1.  <span data-ttu-id="ef2cc-115">Перейдите на одну из следующих страниц:</span><span class="sxs-lookup"><span data-stu-id="ef2cc-115">Go to one of the following pages:</span></span>
- <span data-ttu-id="ef2cc-116">**Расчеты с клиентами > Общее > Клиенты > Все клиенты**</span><span class="sxs-lookup"><span data-stu-id="ef2cc-116">**Accounts receivable > Common > Customers > All customers**</span></span> 
- <span data-ttu-id="ef2cc-117">**Расчеты с поставщиками > Общее > Поставщики > Все поставщики**</span><span class="sxs-lookup"><span data-stu-id="ef2cc-117">**Accounts payable > Common > Vendors > All vendors**</span></span> 
- <span data-ttu-id="ef2cc-118">**Закупки и источники > Общее > Поставщики > Все поставщики**</span><span class="sxs-lookup"><span data-stu-id="ef2cc-118">**Procurement and sourcing > Common > Vendors > All vendors**</span></span>
2.  <span data-ttu-id="ef2cc-119">Выберите клиента или поставщика, чьи открытые транзакции сопоставляются.</span><span class="sxs-lookup"><span data-stu-id="ef2cc-119">Select the customer or vendor whose open transactions you are settling.</span></span> 
3.  <span data-ttu-id="ef2cc-120">Для клиента на странице списка **Все клиенты** последовательно выберите пункты **Собрать > Сопоставлять открытые транзакции**.</span><span class="sxs-lookup"><span data-stu-id="ef2cc-120">For a customer, on the **All customers** list page, go to **Collect > Settle open transactions**.</span></span> <span data-ttu-id="ef2cc-121">Для поставщика на странице списка **Все поставщики** последовательно выберите пункты **Накладная > Сопоставлять открытые транзакции**.</span><span class="sxs-lookup"><span data-stu-id="ef2cc-121">For a vendor, on the **All vendors** list page, go to **Invoice > Settle open transactions**.</span></span> 
4.  <span data-ttu-id="ef2cc-122">Выберите транзакции, являющиеся основным платежом, и щелкните кнопку **Пометить оплату**.</span><span class="sxs-lookup"><span data-stu-id="ef2cc-122">Select the transaction that is the primary payment, and then click **Mark payment**.</span></span> <span data-ttu-id="ef2cc-123">Будет установлен флажок в столбце **Пометка**, а в столбце **Основной платеж** будет показан информационный значок.</span><span class="sxs-lookup"><span data-stu-id="ef2cc-123">The check box in the **Mark** column is selected, and an information icon is shown in the **Primary payment** column.</span></span> 
5.  <span data-ttu-id="ef2cc-124">В поле **Кросс-курс** введите обменный курс между валютами накладной и платежа на дату сопоставления.</span><span class="sxs-lookup"><span data-stu-id="ef2cc-124">In the **Cross rate** field, enter the exchange rate between the invoice currency and the payment currency, as of the settlement date.</span></span> 

