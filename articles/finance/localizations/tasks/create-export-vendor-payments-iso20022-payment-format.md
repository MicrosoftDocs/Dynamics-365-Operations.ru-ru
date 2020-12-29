---
title: Создание и экспорт платежей поставщикам с помощью формата платежей ISO20022
description: В этой процедуре показано, как создать строки платежей в журнале платежей поставщику и как создать файл платежей поставщикам с использованием примера перемещения кредита ISO2022.
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff8a2858bfa96eb1d4b0afa1e48ebd1b578a4431
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447301"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="511c1-103">Создание и экспорт платежей поставщикам с помощью формата платежей ISO20022</span><span class="sxs-lookup"><span data-stu-id="511c1-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="511c1-104">В этом разделе объясняется, как создать строки платежей в журнале платежей поставщику и как создать файл платежей поставщикам с использованием примера перемещения кредита ISO2022.</span><span class="sxs-lookup"><span data-stu-id="511c1-104">This topic explains how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span>

<span data-ttu-id="511c1-105">Это пятая процедура из пяти, которые иллюстрируют процесс платежа поставщикам с помощью конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="511c1-105">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="511c1-106">Для выполнения этого примера используйте демонстрационные данные DEMF.</span><span class="sxs-lookup"><span data-stu-id="511c1-106">Use the DEMF demo data to complete this example.</span></span>

## <a name="example"></a><span data-ttu-id="511c1-107">Пример</span><span class="sxs-lookup"><span data-stu-id="511c1-107">Example</span></span>

1.    <span data-ttu-id="511c1-108">Перейдите в раздел **Расчеты с поставщиками > Платежи > Журнал платежей**.</span><span class="sxs-lookup"><span data-stu-id="511c1-108">Go to **Accounts payable > Payments > Payment journal**.</span></span>
2.    <span data-ttu-id="511c1-109">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="511c1-109">Click **New**.</span></span>
3.    <span data-ttu-id="511c1-110">В поле **Имя** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="511c1-110">In the **Name** field, enter or select a value.</span></span>
4.    <span data-ttu-id="511c1-111">Щелкните **Предложение по оплате -> Создать предложение по оплате**.</span><span class="sxs-lookup"><span data-stu-id="511c1-111">Click **Lines > Payment proposal > Create payment proposal**.</span></span>
5.    <span data-ttu-id="511c1-112">Разверните раздел **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="511c1-112">Expand the **Records to include** section.</span></span>
6.    <span data-ttu-id="511c1-113">Щелкните **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="511c1-113">Click **Filter**.</span></span>
7.    <span data-ttu-id="511c1-114">В списке выберите строку для **таблицы "Поставщики"** и **поля "Счет поставщика"**.</span><span class="sxs-lookup"><span data-stu-id="511c1-114">In the list, select the row for **Vendors table** and **Vendor account field**.</span></span>
8.    <span data-ttu-id="511c1-115">В поле **Критерии** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="511c1-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="511c1-116">Можно применить любые критерии для выбора проводок поставщиков для оплаты, для данного примера в качестве счета поставщика используется DE-001.</span><span class="sxs-lookup"><span data-stu-id="511c1-116">You can apply any criteria for selecting vendor transactions to pay, for this example, use DE-001 as a vendor account.</span></span>
12.    <span data-ttu-id="511c1-117">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="511c1-117">Click **OK**.</span></span>
13.    <span data-ttu-id="511c1-118">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="511c1-118">Click **OK**.</span></span>
14.    <span data-ttu-id="511c1-119">Щелкните **Создать платежи**.</span><span class="sxs-lookup"><span data-stu-id="511c1-119">Click **Create payments**.</span></span>
15. <span data-ttu-id="511c1-120">Создайте файл платежа ISO20022.</span><span class="sxs-lookup"><span data-stu-id="511c1-120">Generate an ISO20022 payment file.</span></span>
    1.    <span data-ttu-id="511c1-121">Щелкните **Создать платежи**.</span><span class="sxs-lookup"><span data-stu-id="511c1-121">Click **Generate payments**.</span></span>
    2.    <span data-ttu-id="511c1-122">В поле **Способ оплаты** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="511c1-122">In the **Method of payment** field, enter or select a value.</span></span>
    3.    <span data-ttu-id="511c1-123">В поле **Имя файла** введите значение.</span><span class="sxs-lookup"><span data-stu-id="511c1-123">In the **File name** field, type a value.</span></span> <span data-ttu-id="511c1-124">Так как в этом примере платеж производится в ЕВРО, созданный файл будет SEPA-совместимым.</span><span class="sxs-lookup"><span data-stu-id="511c1-124">For this example, because of the EUR payment, the generated file will be SEPA compliant.</span></span> <span data-ttu-id="511c1-125">Перенос кредита ISO20022, а также другие форматы платежей поставщикам могут также использоваться для создания платежей в других валютах.</span><span class="sxs-lookup"><span data-stu-id="511c1-125">ISO20022 credit transfer as well as other vendor payment formats can also be used for generating payments in other currencies.</span></span>
    4.    <span data-ttu-id="511c1-126">В поле **Банковский счет** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="511c1-126">In the **Bank account** field, enter or select a value.</span></span>

