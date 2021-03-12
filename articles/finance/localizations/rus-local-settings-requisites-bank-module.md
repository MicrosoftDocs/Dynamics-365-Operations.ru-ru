---
title: Настройка банковских счетов (Россия)
description: В этой теме содержится информация о локальных параметрах и необходимых условиях для банковских модулей для России.
author: anasyash
manager: AnnBe
ms.date: 12/06/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankGroup, BankAccountTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: anasyash
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 4cdf319f11325675f62707be857f752c280fe1d2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4962540"
---
# <a name="set-up-bank-accounts-russia"></a><span data-ttu-id="47642-103">Настройка банковских счетов (Россия)</span><span class="sxs-lookup"><span data-stu-id="47642-103">Set up bank accounts (Russia)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47642-104">Прежде чем работать с рабочей областью **Управление банками**, необходимо выполнить следующие процедуры, чтобы обеспечить соблюдение предварительных условий, необходимых для использования банковских счетов в юридических лицах в России.</span><span class="sxs-lookup"><span data-stu-id="47642-104">Before working in the **Bank management** workspace, you should complete the following procedures to ensure that you have the prerequisites needed for using bank accounts in Russian legal entities.</span></span>

## <a name="create-a-bank-manually-or-update-information-for-a-bank"></a><span data-ttu-id="47642-105">Создание банка вручную или обновления сведений для банка</span><span class="sxs-lookup"><span data-stu-id="47642-105">Create a bank manually or update information for a bank</span></span>

1. <span data-ttu-id="47642-106">Перейдите в раздел **Управление банком и кассовыми операциями > Настройка > Банковские группы**.</span><span class="sxs-lookup"><span data-stu-id="47642-106">Go to **Cash and bank management > Setup > Bank groups**.</span></span>
2. <span data-ttu-id="47642-107">Выберите банк или создайте новый.</span><span class="sxs-lookup"><span data-stu-id="47642-107">Select a bank or create a new one.</span></span> 
2. <span data-ttu-id="47642-108">Введите характерную для России информацию для банка.</span><span class="sxs-lookup"><span data-stu-id="47642-108">Enter Russia-specific information for the bank.</span></span>  
   - <span data-ttu-id="47642-109">**БИК** — банковский идентификационный код.</span><span class="sxs-lookup"><span data-stu-id="47642-109">**BIC** – Bank identification code.</span></span> 
   - <span data-ttu-id="47642-110">**Корр. счет банка** — счет в банке-корреспонденте.</span><span class="sxs-lookup"><span data-stu-id="47642-110">**Corr. Bank account** – Corresponding bank account.</span></span>
   - <span data-ttu-id="47642-111">**Тип банка** — выберите **Основной**, **Зарубежный** или **Филиал**.</span><span class="sxs-lookup"><span data-stu-id="47642-111">**Bank type** – Select either **Main**, **Foreign**, or **Branch**.</span></span> <span data-ttu-id="47642-112">Если вы выбрали **Зарубежный**, выберите **Счет поставщика** на экспресс-вкладке **Общие**.</span><span class="sxs-lookup"><span data-stu-id="47642-112">If you select, **Foreign**, select a **Vendor account** on the **General** FastTab.</span></span> <span data-ttu-id="47642-113">Если вы выбрали **Филиал**, выберите значение в поле **Основной банк**.</span><span class="sxs-lookup"><span data-stu-id="47642-113">If you select **Branch**, select a value in the **Main bank** field.</span></span>
3. <span data-ttu-id="47642-114">(Необязательно) Выберите шаблон в формате DOCX для использования в поле **Валютное платежное поручение** на экспресс-вкладке **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="47642-114">(Optional) Select the .docx template to use in the **Payment order in currency** field on the **Setup** FastTab.</span></span> <span data-ttu-id="47642-115">Если этот шаблон определен, он будет использоваться по умолчанию для платежного поручения в валюте для всех зарубежных банковских счетов, связанных с этим банком.</span><span class="sxs-lookup"><span data-stu-id="47642-115">If defined, this will be the default template for the payment order in currency for all foreign bank accounts related to this bank.</span></span>

> [!NOTE]
> <span data-ttu-id="47642-116">Прежде чем определять шаблон документа, создайте шаблоны в виде файлов и вложите их в запись.</span><span class="sxs-lookup"><span data-stu-id="47642-116">Before defining a document template, create the templates as files and attach them to the record.</span></span> <span data-ttu-id="47642-117">Определить наличие вложенных документов можно по числовому индикатору на значке **Вложения документов**.</span><span class="sxs-lookup"><span data-stu-id="47642-117">You can determine if a document is attached by using the number indicator on the **Document attachment** icon.</span></span>


## <a name="create-banks-by-importing-a-list-of-banks"></a><span data-ttu-id="47642-118">Создание банков путем импорта списка банков</span><span class="sxs-lookup"><span data-stu-id="47642-118">Create banks by importing a list of banks</span></span>

### <a name="prerequisites"></a><span data-ttu-id="47642-119">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="47642-119">Prerequisites</span></span>

1.  <span data-ttu-id="47642-120">Импортируйте файл конфигурации электронной отчетности "Каталог БИК банков (RU)" из Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="47642-120">Import the ‘Bank BIC catalog (RU)’ Electronic reporting (ER) configuration file from Microsoft Dynamics Lifecycle Services (LCS).</span></span>
<span data-ttu-id="47642-121">Дополнительные сведения см. в разделе [Загрузка конфигураций электронной отчетности из Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="47642-121">For more information, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

2. <span data-ttu-id="47642-122">Перейдите в раздел **Управление банком и кассовыми операциями > Настройка > Параметры управления банком и кассовыми операциями**.</span><span class="sxs-lookup"><span data-stu-id="47642-122">Go to **Cash and bank management > Setup > Cash and bank management parameters**.</span></span> <span data-ttu-id="47642-123">На экспресс-вкладке **Общие** в группе полей **Импорт списка банков** в поле **Импорт конфигурации формата** выберите конфигурацию электронной отчетности "Каталог БИК банков (RU)".</span><span class="sxs-lookup"><span data-stu-id="47642-123">On the **General** FastTab, in the **Import list of banks** fields group, in the **Import format configuration** field, select the ER configuration ‘Bank BIC catalog (RU)’.</span></span>


### <a name="import-a-list-of-banks"></a><span data-ttu-id="47642-124">Импорт списка банков</span><span class="sxs-lookup"><span data-stu-id="47642-124">Import a list of banks</span></span>

<span data-ttu-id="47642-125">Выберите **Управление банком и кассовыми операциями > Настройка > Банковские группы** и щелкните **Загрузить список банков**.</span><span class="sxs-lookup"><span data-stu-id="47642-125">Go to **Cash and bank management > Setup > Bank groups** and click **Load bank list**.</span></span> <span data-ttu-id="47642-126">Открывается диалоговое окно **Импорт данных**.</span><span class="sxs-lookup"><span data-stu-id="47642-126">The **Import of data** dialog box will open.</span></span>

<span data-ttu-id="47642-127">Список банков может быть обновлен для отмеченных регионов или только для выбранных банков.</span><span class="sxs-lookup"><span data-stu-id="47642-127">The bank list may be updated for marked states or for the chosen banks only.</span></span>

<span data-ttu-id="47642-128">В верхней области диалогового окна **Импорт данных** отметьте регионы для импорта или обновлении всех банков из помеченных регионов.</span><span class="sxs-lookup"><span data-stu-id="47642-128">In the upper pane of **Import of data** dialog box, mark states for importing/updating all banks from the marked state.</span></span>
<span data-ttu-id="47642-129">В нижней области диалогового окна **Импорт данных** используйте следующие кнопки, чтобы выбрать банки, которые будут включены в обновление:</span><span class="sxs-lookup"><span data-stu-id="47642-129">In the lower pane of **Import of data** dialog box, use the following buttons to choose the banks that will be included in the update:</span></span>
  - <span data-ttu-id="47642-130">**Выбрать существующий** — выбор и обновление банков, которые существуют в системе.</span><span class="sxs-lookup"><span data-stu-id="47642-130">**Select existing** - Select and update the banks which exist in the system.</span></span>
  - <span data-ttu-id="47642-131">**Выбрать все** — выбор и обновление всех банков, которые выбраны.</span><span class="sxs-lookup"><span data-stu-id="47642-131">**Select all** - Select and update all banks that are selected.</span></span>
  - <span data-ttu-id="47642-132">**Очистить все** — очистить все банки.</span><span class="sxs-lookup"><span data-stu-id="47642-132">**Deselect all** - Clear all banks.</span></span> 

## <a name="create-a-bank-account"></a><span data-ttu-id="47642-133">Создание банковского счета</span><span class="sxs-lookup"><span data-stu-id="47642-133">Create a bank account</span></span>

1. <span data-ttu-id="47642-134">Создайте новый банковский счет, выбрав **Управление банком и кассовыми операциями > Банковские счета > Банковские счета**.</span><span class="sxs-lookup"><span data-stu-id="47642-134">Create a new bank account at **Cash and bank management > Bank accounts > Bank accounts**.</span></span>
2. <span data-ttu-id="47642-135">Заполните все обязательные поля.</span><span class="sxs-lookup"><span data-stu-id="47642-135">Complete all required fields.</span></span> <span data-ttu-id="47642-136">В следующем списке приведены некоторые поля, которые могут быть обязательными.</span><span class="sxs-lookup"><span data-stu-id="47642-136">The following list includes some fields that might be required.</span></span> 
    - <span data-ttu-id="47642-137">**Банковский счет** (код)</span><span class="sxs-lookup"><span data-stu-id="47642-137">**Bank account** (code)</span></span>
    - <span data-ttu-id="47642-138">**Номер банковского счета**</span><span class="sxs-lookup"><span data-stu-id="47642-138">**Bank account number**</span></span>
    - <span data-ttu-id="47642-139">**Счет ГК** — это счет главной книги, используемый для разноски.</span><span class="sxs-lookup"><span data-stu-id="47642-139">**Main account** - This is the general ledger account that is used for posting.</span></span>
    - <span data-ttu-id="47642-140">**Валюта**</span><span class="sxs-lookup"><span data-stu-id="47642-140">**Currency**</span></span>
    - <span data-ttu-id="47642-141">**SWIFT-код**</span><span class="sxs-lookup"><span data-stu-id="47642-141">**SWIFT code**</span></span> 

  <span data-ttu-id="47642-142">Дополнительные сведения см. в разделе [Рабочая область управления банками](../cash-bank-management/bank-management-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="47642-142">For more information ,see [Bank management workspace](../cash-bank-management/bank-management-workspace.md).</span></span>

3. <span data-ttu-id="47642-143">Введите информацию, характерную для России:</span><span class="sxs-lookup"><span data-stu-id="47642-143">Enter Russia-specific information:</span></span> 
    - <span data-ttu-id="47642-144">Выберите **Банк** в поле **Банковские группы**.</span><span class="sxs-lookup"><span data-stu-id="47642-144">Select **Bank** in the **Bank groups** field.</span></span> <span data-ttu-id="47642-145">Убедитесь, что поля **БИК** и **Корр. счет банка** заполнены правильно.</span><span class="sxs-lookup"><span data-stu-id="47642-145">Confirm that the **BIC** and **Corr. Bank account** fields are correct.</span></span> <span data-ttu-id="47642-146">Также проверьте содержимое полей **Адрес** и **Контактная информация** на соответствующих экспресс-вкладках и откорректируйте его соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="47642-146">Also, confirm **Address** and **Contact information** on respective FastTabs and update accordingly.</span></span>
    - <span data-ttu-id="47642-147">Задайте номерную серию для создания платежных поручений в поле **Нумерация П/П**.</span><span class="sxs-lookup"><span data-stu-id="47642-147">Define the number series for payment order generation in the **P/O numeration** field.</span></span>
    - <span data-ttu-id="47642-148">Для банковских счетов в иностранной валюте можно также определить шаблоны DOCX для создания платежных поручений в бумажном формате в следующих полях: **Валютное платежное поручение**, **Шаблон поручения (продажа валюты)** и **Шаблон поручения (покупка валюты)**.</span><span class="sxs-lookup"><span data-stu-id="47642-148">For bank accounts in foreign currency, you can also define .docx templates for generation of payment orders in paper format in the following fields: **Payment order in currency**, **Order template (currency sale)**, and **Order template (currency purchase)**.</span></span> 

> [!NOTE]
> <span data-ttu-id="47642-149">Прежде чем определять шаблон документа, создайте шаблоны в виде файлов и вложите их в запись.</span><span class="sxs-lookup"><span data-stu-id="47642-149">Before defining a document template, create the templates as files and attach them to the record.</span></span> <span data-ttu-id="47642-150">Определить наличие вложенных документов можно по числовому индикатору на значке **Вложения документов**.</span><span class="sxs-lookup"><span data-stu-id="47642-150">You can determine if a document is attached by using the number indicator on the **Document attachment** icon.</span></span>

![Банковский счет](media/rus-bank-account.jpg)
