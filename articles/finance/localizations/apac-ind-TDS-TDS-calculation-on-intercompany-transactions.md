---
title: Расчет ЕTD на внутрихолдинговых проводках
description: В этой теме описывается процесс, используемый для расчета налога, вычитаемого в источнике (TDS), по внутрихолдинговым проводкам в виде фаз.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 0e304747cc93bfe0a39beababc3182ca14664b11
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023541"
---
# <a name="tds-calculation-on-intercompany-transactions"></a><span data-ttu-id="f047e-103">Расчет ЕTD на внутрихолдинговых проводках</span><span class="sxs-lookup"><span data-stu-id="f047e-103">TDS calculation on intercompany transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f047e-104">В этой теме описывается процесс, используемый для расчета налога, вычитаемого в источнике (TDS), по внутрихолдинговым проводкам в виде фаз.</span><span class="sxs-lookup"><span data-stu-id="f047e-104">This topic describes the process that is used to calculate Tax Deducted at Source (TDS) on intercompany transactions in phases.</span></span>

<span data-ttu-id="f047e-105">При создании внутрихолдингового заказа на покупку или заказа на продажу группа TDS по умолчанию, которая определена для клиента или поставщика, используется для расчета суммы TDS.</span><span class="sxs-lookup"><span data-stu-id="f047e-105">When an intercompany purchase order or sales order is created, the default TDS group that is defined for the customer or vendor is used to calculate the TDS amount.</span></span> <span data-ttu-id="f047e-106">Сумма TDS разносится на возмещаемые счета или счета кредиторской задолженности после разноски накладной.</span><span class="sxs-lookup"><span data-stu-id="f047e-106">The TDS amount is posted to the recoverable or payable accounts after the invoice is posted.</span></span>

<span data-ttu-id="f047e-107">Внутрихолдинговый заказ на продажу или заказ на покупку создается автоматически для исходного заказа на покупку или заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="f047e-107">An intercompany sales order or purchase order is automatically created for the original purchase order or sales order.</span></span> <span data-ttu-id="f047e-108">Группа TDS по умолчанию отображается во внутрихолдинговом заказе, чтобы можно было рассчитать TDS.</span><span class="sxs-lookup"><span data-stu-id="f047e-108">The default TDS group is shown on the intercompany order, so that TDS can be calculated.</span></span> <span data-ttu-id="f047e-109">Группу TDS можно изменить.</span><span class="sxs-lookup"><span data-stu-id="f047e-109">You can change the TDS group.</span></span> <span data-ttu-id="f047e-110">Накладная может быть разнесена только в том случае, если чистая сумма накладной по внутрихолдинговому заказу, которая создается автоматически, совпадает с чистой суммой накладной в исходном заказе.</span><span class="sxs-lookup"><span data-stu-id="f047e-110">The invoice can be posted only if the net invoice amount on the intercompany order that is automatically created matches the net invoice amount on the original order.</span></span> <span data-ttu-id="f047e-111">(Чистая сумма представляет собой сумму накладной после вычета TDS.)</span><span class="sxs-lookup"><span data-stu-id="f047e-111">(The net amount is the invoice amount after TDS is deducted.)</span></span>

<span data-ttu-id="f047e-112">Например, накладная заказа на продажу создается для 50 000, и к ней привязывается TDS **10%**.</span><span class="sxs-lookup"><span data-stu-id="f047e-112">For example, a sales invoice is created for 50,000, and the **10%** TDS group is attached to it.</span></span> <span data-ttu-id="f047e-113">Разнесенная сумма по накладной составляет 45 000, а разнесенная сумма TDS для накладной заказа на продажу составляет 5000.</span><span class="sxs-lookup"><span data-stu-id="f047e-113">The posted invoice amount is 45,000, and the posted TDS amount for the sales invoice is 5,000.</span></span> <span data-ttu-id="f047e-114">Заказ на покупку автоматически создается для внутрихолдингового заказа на продажу, и к нему прикрепляется **10%** TDS.</span><span class="sxs-lookup"><span data-stu-id="f047e-114">A purchase order is automatically created for the intercompany sales order, and the  **10%** TDS group is attached to it.</span></span> <span data-ttu-id="f047e-115">Если изменить группу TDS на **15%**, невозможно будет разнести накладную, так как чистая сумма накладной для внутрихолдингового заказа на продажу, которая была автоматически создана, не совпадает с чистой суммой накладной исходного заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="f047e-115">If you change the TDS group to **15%**, you can't post the invoice, because the net invoice amount of the intercompany sales order that was automatically created doesn't match the net invoice amount of the original sales order.</span></span>

<span data-ttu-id="f047e-116">Журнал платежей, созданный для внутрихолдинговой накладной, разносится автоматически.</span><span class="sxs-lookup"><span data-stu-id="f047e-116">A payment journal that is created for an intercompany invoice is automatically posted.</span></span> <span data-ttu-id="f047e-117">Этот журнал платежей может быть разнесен только в том случае, если чистая сумма платежа в ней совпадает с суммой чистого платежа по исходному журналу платежей.</span><span class="sxs-lookup"><span data-stu-id="f047e-117">That payment journal can be posted only if the net payment amount on it matches the net payment amount on the original payment journal.</span></span>
