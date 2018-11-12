---
title: "Настройка банковских счетов (Россия)"
description: "В этой теме содержится информация о локальных параметрах и необходимых условиях для банковских модулей для России."
author: anasyash
manager: AnnBe
ms.date: 10/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankGroup, BankAccountTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.author: anasyash
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: b589a6ce02cdc02436e256f9e81346fe8b766687
ms.openlocfilehash: bf4865c8553ce251d062049e3dbf8dce7c78c3a7
ms.contentlocale: ru-ru
ms.lasthandoff: 11/12/2018

---

# <a name="set-up-bank-accounts-russia"></a><span data-ttu-id="e1e8d-103">Настройка банковских счетов (Россия)</span><span class="sxs-lookup"><span data-stu-id="e1e8d-103">Set up bank accounts (Russia)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1e8d-104">Прежде чем работать с рабочей областью **Управление банками**, необходимо выполнить следующие процедуры, чтобы обеспечить соблюдение предварительных условий для настройки банковских счетов для России.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-104">Before working in the **Bank management** workspace, you should complete the following procedures to ensure that you have the prerequisites needed for setting up bank accounts for Russia.</span></span>

## <a name="enter-bank-group-information"></a><span data-ttu-id="e1e8d-105">Ввод информации о банковской группе</span><span class="sxs-lookup"><span data-stu-id="e1e8d-105">Enter bank group information</span></span>

1. <span data-ttu-id="e1e8d-106">Выберите **Управление банком и кассовыми операциями > Настройка > Банковские группы** и щелкните **Обновить банковский счет**.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-106">Go to **Cash and bank management > Setup > Bank groups** and click **Update bank accounts**.</span></span>
2. <span data-ttu-id="e1e8d-107">Выберите банковскую группу.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-107">Select a bank group.</span></span> 
2. <span data-ttu-id="e1e8d-108">Введите характерную для России информацию для банковской группы.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-108">Enter Russia-specific information for the bank group.</span></span>  
   - <span data-ttu-id="e1e8d-109">**БИК** — банковский идентификационный код</span><span class="sxs-lookup"><span data-stu-id="e1e8d-109">**BIC** – Bank identifification code</span></span> 
   - <span data-ttu-id="e1e8d-110">**Корр. счет банка** — счет в банке-корреспонденте</span><span class="sxs-lookup"><span data-stu-id="e1e8d-110">**Corr. Bank account** – Corresponding bank account</span></span>
   - <span data-ttu-id="e1e8d-111">**Тип банка** — выберите **Основной**, **Зарубежный** или **Филиал**.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-111">**Bank type** – Select either **Main**, **Foreign**, or **Branch**.</span></span> <span data-ttu-id="e1e8d-112">Если вы выбрали **Зарубежный**, выберите **Счет поставщика** на экспресс-вкладке **Общие**.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-112">If you select, **Foreign**, select a **Vendor account** on the **General** FastTab.</span></span> <span data-ttu-id="e1e8d-113">Если вы выбрали **Филиал**, выберите значение в поле **Основной банк**.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-113">If you select **Branch**, select a value in the **Main bank** field.</span></span>
3. <span data-ttu-id="e1e8d-114">(Необязательно) Выберите шаблон в формате DOCX для использования в поле **Валютное платежное поручение** на экспресс-вкладке **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-114">(Optional) Select the .docx template to use in the **Payment order in currency** field on the **Setup** FastTab.</span></span> <span data-ttu-id="e1e8d-115">Если этот шаблон определен, он будет использоваться по умолчанию для платежного поручения в валюте для всех зарубежных банковских счетов, связанных с этим банком.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-115">If defined, this will be the default template for the payment order in currency for all foreign bank accounts related to this bank.</span></span>

> [!NOTE]
> <span data-ttu-id="e1e8d-116">Прежде чем определять шаблон документа, создайте шаблоны в виде файлов и вложите их в запись.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-116">Before defining a document template, create the templates as files and attach them to the record.</span></span> <span data-ttu-id="e1e8d-117">Определить наличие вложенных документов можно по числовому индикатору на значке **Вложения документов**.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-117">You can determine if a document is attached by using the number indicator on the **Document attachment** icon.</span></span>

  ![Bank](media/rus-bank.jpg)
    

## <a name="create-a-bank-account"></a><span data-ttu-id="e1e8d-119">Создание банковского счета</span><span class="sxs-lookup"><span data-stu-id="e1e8d-119">Create a Bank account</span></span>

1. <span data-ttu-id="e1e8d-120">Создайте новый банковский счет, выбрав **Управление банком и кассовыми операциями > Банковские счета > Банковские счета**.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-120">Create a new bank account at **Cash and bank management > Bank accounts > Bank accounts**.</span></span>
2. <span data-ttu-id="e1e8d-121">Заполните все обязательные поля.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-121">Complete all required fields.</span></span> <span data-ttu-id="e1e8d-122">В следующем списке приведены некоторые поля, которые могут быть обязательными.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-122">The following list includes some fields that might be required.</span></span> 
    - <span data-ttu-id="e1e8d-123">**Банковский счет** (код)</span><span class="sxs-lookup"><span data-stu-id="e1e8d-123">**Bank account** (code)</span></span>
    - <span data-ttu-id="e1e8d-124">**Номер банковского счета**</span><span class="sxs-lookup"><span data-stu-id="e1e8d-124">**Bank account number**</span></span>
    - <span data-ttu-id="e1e8d-125">**Счет ГК** — это счет главной книги, используемый для разноски.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-125">**Main account** - This is the general ledger account that is used for posting.</span></span>
    - <span data-ttu-id="e1e8d-126">**Валюта**</span><span class="sxs-lookup"><span data-stu-id="e1e8d-126">**Currency**</span></span>
    - <span data-ttu-id="e1e8d-127">**SWIFT-код**</span><span class="sxs-lookup"><span data-stu-id="e1e8d-127">**SWIFT code**</span></span> 

  <span data-ttu-id="e1e8d-128">Дополнительные сведения см. в разделе [Рабочая область управления банками](../cash-bank-management/bank-management-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="e1e8d-128">For more information see [Bank management workspace](../cash-bank-management/bank-management-workspace.md).</span></span>

3. <span data-ttu-id="e1e8d-129">Введите информацию, характерную для России:</span><span class="sxs-lookup"><span data-stu-id="e1e8d-129">Enter Russia-specific information:</span></span> 
    - <span data-ttu-id="e1e8d-130">Выберите **Банк** в поле **Банковские группы**.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-130">Select **Bank** in the **Bank groups** field.</span></span> <span data-ttu-id="e1e8d-131">Убедитесь, что поля **БИК** и **Корр. счет банка** заполнены правильно.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-131">Confirm that the **BIC** and **Corr. Bank account** fields are correct.</span></span> <span data-ttu-id="e1e8d-132">Также проверьте содержимое полей **Адрес** и **Контактная информация** на соответствующих экспресс-вкладках и откорректируйте его соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-132">Also confirm **Address** and **Contact information** on respective FastTabs and update accordingly.</span></span>
    - <span data-ttu-id="e1e8d-133">Задайте номерную серию для создания платежных поручений в поле **Нумерация П/П**.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-133">Define the number series for payment order generation in the **P/O numeration** field.</span></span>
    - <span data-ttu-id="e1e8d-134">Для банковских счетов в иностранной валюте можно также определить шаблоны DOCX для создания платежных поручений в бумажном формате в следующих полях: **Валютное платежное поручение**, **Шаблон поручения (продажа валюты)** и **Шаблон поручения (покупка валюты)**.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-134">For bank accounts in foreign currency, you can also define .docx templates for generation of payment orders in paper format in the following fields: **Payment order in currency**, **Order template (currency sale)**, and **Order template (currency purchase)**.</span></span> 

> [!NOTE]
> <span data-ttu-id="e1e8d-135">Прежде чем определять шаблон документа, создайте шаблоны в виде файлов и вложите их в запись.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-135">Before defining a document template, create the templates as files and attach them to the record.</span></span> <span data-ttu-id="e1e8d-136">Определить наличие вложенных документов можно по числовому индикатору на значке **Вложения документов**.</span><span class="sxs-lookup"><span data-stu-id="e1e8d-136">You can determine if a document is attached by using the number indicator on the **Document attachment** icon.</span></span>

![Банковский счет](media/rus-bank-account.jpg)

