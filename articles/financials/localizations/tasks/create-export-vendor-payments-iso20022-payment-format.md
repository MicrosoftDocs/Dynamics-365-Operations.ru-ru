--- 
title: "Создание и экспорт платежей поставщикам с помощью формата платежей ISO20022"
description: "В этой процедуре показано, как создать строки платежей в журнале платежей поставщику и как создать файл платежей поставщикам с использованием примера перемещения кредита ISO2022."
author: mrolecki
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: dac38165474712cfcd6cdd2712dab89230e07b1b
ms.contentlocale: ru-ru
ms.lasthandoff: 09/11/2018

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="e80da-103">Создание и экспорт платежей поставщикам с помощью формата платежей ISO20022</span><span class="sxs-lookup"><span data-stu-id="e80da-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e80da-104">В этой процедуре показано, как создать строки платежей в журнале платежей поставщику и как создать файл платежей поставщикам с использованием примера перемещения кредита ISO2022.</span><span class="sxs-lookup"><span data-stu-id="e80da-104">This procedure shows how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span> 

<span data-ttu-id="e80da-105">В качестве компании с демонстрационными данными для создания этой процедуры используется DEMF.</span><span class="sxs-lookup"><span data-stu-id="e80da-105">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="e80da-106">Это пятая процедура из пяти, которые иллюстрируют процесс платежа поставщикам с помощью конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="e80da-106">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="e80da-107">Эта процедура предназначена для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="e80da-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-payment-lines"></a><span data-ttu-id="e80da-108">Создание строк платежа</span><span class="sxs-lookup"><span data-stu-id="e80da-108">Create payment lines</span></span>
1. <span data-ttu-id="e80da-109">Перейдите в раздел "Расчеты с поставщиками" > "Платежи" > "Журнал платежей".</span><span class="sxs-lookup"><span data-stu-id="e80da-109">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="e80da-110">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="e80da-110">Click New.</span></span>
3. <span data-ttu-id="e80da-111">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="e80da-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="e80da-112">В поле "Имя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="e80da-112">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="e80da-113">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="e80da-113">Click Lines.</span></span>
6. <span data-ttu-id="e80da-114">Щелкните "Предложение по оплате".</span><span class="sxs-lookup"><span data-stu-id="e80da-114">Click Payment proposal.</span></span>
7. <span data-ttu-id="e80da-115">Щелкните "Создать предложение по оплате".</span><span class="sxs-lookup"><span data-stu-id="e80da-115">Click Create payment proposal.</span></span>
8. <span data-ttu-id="e80da-116">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="e80da-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="e80da-117">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="e80da-117">Click Filter.</span></span>
10. <span data-ttu-id="e80da-118">В списке выберите строку для таблицы "Поставщики" и поля "Счет поставщика".</span><span class="sxs-lookup"><span data-stu-id="e80da-118">In the list, select the row for Vendors table and Vendor account field.</span></span>
11. <span data-ttu-id="e80da-119">В поле "Критерии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="e80da-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="e80da-120">Можно применить любые критерии для выбора проводок поставщиков для оплаты, для данного примера в качестве счета поставщика используется DE-001.</span><span class="sxs-lookup"><span data-stu-id="e80da-120">You can apply any criteria for selecting vendor transactions to pay, for this example use DE-001 as a vendor account.</span></span>  
12. <span data-ttu-id="e80da-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e80da-121">Click OK.</span></span>
13. <span data-ttu-id="e80da-122">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e80da-122">Click OK.</span></span>
14. <span data-ttu-id="e80da-123">Щелкните "Создать платежи".</span><span class="sxs-lookup"><span data-stu-id="e80da-123">Click Create payments.</span></span>

## <a name="generate-an-iso20022-payment-file"></a><span data-ttu-id="e80da-124">Создание файла платежа ISO20022</span><span class="sxs-lookup"><span data-stu-id="e80da-124">Generate an ISO20022 payment file</span></span>


