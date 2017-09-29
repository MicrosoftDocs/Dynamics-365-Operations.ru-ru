---
title: "Аккредитивы и импорт коллекций"
description: "Эта статья содержит общие сведения об аккредитивах и импорте коллекций. Оба типа банковского документа часто используются для покупки и продажи товаров через международные границы."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankLCImport
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 18321
ms.assetid: 5c97ab81-632b-4043-a940-674bcb496c80
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 4332c7bb0344bd0caabd5d1a26fb8e4bb4fc862d
ms.contentlocale: ru-ru
ms.lasthandoff: 06/29/2017


---

# <a name="letters-of-credit-and-import-collections"></a><span data-ttu-id="a47e6-104">Аккредитивы и импорт коллекций</span><span class="sxs-lookup"><span data-stu-id="a47e6-104">Letters of credit and import collections</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a47e6-105">Эта статья содержит общие сведения об аккредитивах и импорте коллекций.</span><span class="sxs-lookup"><span data-stu-id="a47e6-105">This article provides general information about letters of credit and import collections.</span></span> <span data-ttu-id="a47e6-106">Оба типа банковского документа часто используются для покупки и продажи товаров через международные границы.</span><span class="sxs-lookup"><span data-stu-id="a47e6-106">Both types of bank document are often used for the purchase and sale of goods across international borders.</span></span>

<a name="letters-of-credit"></a><span data-ttu-id="a47e6-107">Аккредитивы</span><span class="sxs-lookup"><span data-stu-id="a47e6-107">Letters of credit</span></span>
-----------------

<span data-ttu-id="a47e6-108">Аккредитивы используются для международных транзакций, чтобы помочь гарантировать, что платежи будут выполнены.</span><span class="sxs-lookup"><span data-stu-id="a47e6-108">Letters of credit are used for international transactions and help guarantee that payments will be made.</span></span> <span data-ttu-id="a47e6-109">Аккредитив — это соглашение, выданное банком, в котором банк соглашается обеспечить платеж от имени покупателя, если будут выполнены условия соглашения между покупателем и продавцом.</span><span class="sxs-lookup"><span data-stu-id="a47e6-109">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to guarantee payment on behalf of a buyer, provided that the terms of the agreement between the buyer and seller are met.</span></span> <span data-ttu-id="a47e6-110">Аккредитивом также называется документарный аккредитив.</span><span class="sxs-lookup"><span data-stu-id="a47e6-110">A letter of credit is also referred to as a documentary credit (DC).</span></span>

<span data-ttu-id="a47e6-111">Для кредитного письма импорта юридическое лицо является покупателем или заявителем кредитного письма.</span><span class="sxs-lookup"><span data-stu-id="a47e6-111">For an import letter of credit, the legal entity is the buyer or the applicant for the letter of credit.</span></span> <span data-ttu-id="a47e6-112">Для кредитного письма экспорта юридическое лицо является продавцом или бенефициаром кредитного письма.</span><span class="sxs-lookup"><span data-stu-id="a47e6-112">For an export letter of credit, the legal entity is the seller or the beneficiary of the letter of credit.</span></span> <span data-ttu-id="a47e6-113">Следующие субъекты являются участниками кредитного письма:</span><span class="sxs-lookup"><span data-stu-id="a47e6-113">The following parties are involved in a letter of credit:</span></span>

-   <span data-ttu-id="a47e6-114">Заявитель (покупатель), который намеревается оплатить товары</span><span class="sxs-lookup"><span data-stu-id="a47e6-114">The applicant (buyer) who intends to pay for the goods</span></span>
-   <span data-ttu-id="a47e6-115">Бенефициар (продавец), который получает платеж</span><span class="sxs-lookup"><span data-stu-id="a47e6-115">The beneficiary (seller) who will receive the payment</span></span>
-   <span data-ttu-id="a47e6-116">Выставляющий банк, выдающий аккредитив</span><span class="sxs-lookup"><span data-stu-id="a47e6-116">The issuing bank that issues the letter of credit</span></span>
-   <span data-ttu-id="a47e6-117">Авизующий банк, который выполняет проводку от имени заявителя</span><span class="sxs-lookup"><span data-stu-id="a47e6-117">The advising bank that carries out the transaction on behalf of the applicant</span></span>

<span data-ttu-id="a47e6-118">Аккредитив включает описание товаров, все необходимые документы, дату отгрузки и дату окончания действия, после которой платеж не будет совершаться.</span><span class="sxs-lookup"><span data-stu-id="a47e6-118">The letter of credit includes a description of the goods, any required documents, the date of shipment, and the expiration date after which payment won't be made.</span></span> <span data-ttu-id="a47e6-119">Выставляющий банк собирает маржу для аккредитива.</span><span class="sxs-lookup"><span data-stu-id="a47e6-119">The issuing bank collects a margin for the letter of credit.</span></span> 

<span data-ttu-id="a47e6-120">Аккредитив может быть **отзывной** или **безотзывный**.</span><span class="sxs-lookup"><span data-stu-id="a47e6-120">A letter of credit can be **revocable** or **irrevocable**.</span></span> <span data-ttu-id="a47e6-121">Аккредитив может быть **передаваемым**, **непередаваемым** или **возобновляемым**.</span><span class="sxs-lookup"><span data-stu-id="a47e6-121">The nature of a letter of credit can be **transferable**, **non-transferable**, or **revolving**.</span></span> <span data-ttu-id="a47e6-122">Обычно аккредитив является безотзывным и подтвержденным соглашением о том, что платеж будет выполнен конкретному бенефициару после оформления полной и точной документации по отгрузке.</span><span class="sxs-lookup"><span data-stu-id="a47e6-122">Typically, a letter of credit is an irrevocable and confirmed agreement that payment will be made to a specific beneficiary upon submission of complete and accurate shipping documentation.</span></span>

## <a name="import-collections"></a><span data-ttu-id="a47e6-123">Импорт коллекций</span><span class="sxs-lookup"><span data-stu-id="a47e6-123">Import collections</span></span>
<span data-ttu-id="a47e6-124">Импортное инкассо — это соглашение между банком и экспортером (продавцом), в котором банк соглашается на поставку документации по отгрузке международному импортеру (покупателю).</span><span class="sxs-lookup"><span data-stu-id="a47e6-124">An import collection is an agreement between the bank and the exporter (seller), in which the bank agrees to deliver the shipping documentation to the international importer (buyer).</span></span> <span data-ttu-id="a47e6-125">Предполагается, что банк доставляет документацию по отгрузке после получения платежа за отправленные товары наличными или подписанного платежного поручения для платежа.</span><span class="sxs-lookup"><span data-stu-id="a47e6-125">The bank is expected to deliver the shipping documentation upon receipt of payment for the shipped goods in cash, or upon receipt of a signed draft toward the payment.</span></span> 

<span data-ttu-id="a47e6-126">Импортное инкассо помогает гарантировать, что продавец получит деньги, когда покупатель получит документы по отгрузке для получения поставки импортированных товаров.</span><span class="sxs-lookup"><span data-stu-id="a47e6-126">An import collection helps guarantee that the seller is paid when the buyer collects the shipping documents to take delivery of the imported goods.</span></span>




