---
title: Ссылки на исходные накладные в кредит-нотах
description: В этой теме объясняется, как настроить и напечатать исходные номера накладных в соответствующих кредит-нотах.
author: ilkond
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 673288f04b33aa2a578f9e2e7913dbe7ac309644
ms.sourcegitcommit: 7cdec5469ff0da145ac4e01caf3287d0627ae2dc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2021
ms.locfileid: "5100010"
---
# <a name="references-to-original-invoices-in-credit-notes"></a><span data-ttu-id="eb2b4-103">Ссылки на исходные накладные в кредит-нотах</span><span class="sxs-lookup"><span data-stu-id="eb2b4-103">References to original invoices in credit notes</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="eb2b4-104">В некоторых странах и регионах имеется юридическое требование, чтобы распечатанные кредит-ноты включали ссылки на исходные накладные.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-104">In some countries and regions, there is a legal requirement that printed credit notes include references to the original invoices.</span></span> <span data-ttu-id="eb2b4-105">В этой теме объясняется, как настроить и напечатать исходные номера накладных в соответствующих кредит-нотах.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-105">This topic explains how to set up and print the original invoice numbers in related credit notes.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="eb2b4-106">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="eb2b4-106">Prerequisites</span></span>

- <span data-ttu-id="eb2b4-107">В рабочей области **Управление функциями** включите функцию **Макет кредитования при обработке накладной для отчетов о накладных по продажам и проектам**.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-107">In the **Feature management** workspace, turn on the **Credit invoicing layout for sales and project invoice reports** feature.</span></span> <span data-ttu-id="eb2b4-108">Дополнительные сведения см. в разделе [Обзор управления функциями](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="eb2b4-108">For more information, see [Feature management overview](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="eb2b4-109">Подходящие для печати форматы необходимых документов должны быть настроены в управлении печатью.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-109">The printable formats of the required documents must be configured in Print management.</span></span>

<span data-ttu-id="eb2b4-110">Функциональная возможность, описанная в данной теме, применяется к следующим документам:</span><span class="sxs-lookup"><span data-stu-id="eb2b4-110">The functionality that is described in this topic applies to the following documents:</span></span>

<span data-ttu-id="eb2b4-111">**Расчеты с клиентами**</span><span class="sxs-lookup"><span data-stu-id="eb2b4-111">**Accounts receivable**</span></span>

- <span data-ttu-id="eb2b4-112">Кредит-нота с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="eb2b4-112">Free text credit note</span></span>
- <span data-ttu-id="eb2b4-113">Кредит-нота клиента</span><span class="sxs-lookup"><span data-stu-id="eb2b4-113">Customer credit note</span></span>

<span data-ttu-id="eb2b4-114">**Управление и учет по проектам**</span><span class="sxs-lookup"><span data-stu-id="eb2b4-114">**Project management and accounting**</span></span>

- <span data-ttu-id="eb2b4-115">Кредит-нота по проекту</span><span class="sxs-lookup"><span data-stu-id="eb2b4-115">Project credit note</span></span>

## <a name="configure-accounts-receivable-parameters"></a><span data-ttu-id="eb2b4-116">Настройка параметров расчетов с клиентами</span><span class="sxs-lookup"><span data-stu-id="eb2b4-116">Configure Accounts receivable parameters</span></span>

<span data-ttu-id="eb2b4-117">Выполните следующие действия, чтобы настроить параметр, который определяет, будут ли ссылки на исходные накладные распечатаны в соответствующих кредит-нотах.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-117">Follow these steps to set the parameter that controls whether references to the original invoices are printed in related credit notes.</span></span>

1. <span data-ttu-id="eb2b4-118">Перейдите в раздел **Расчеты с клиентами** \> **Настройка** \> **Параметры модуля расчетов с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-118">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="eb2b4-119">На вкладке **Обновления** на экспресс-вкладке **Накладная** установите для параметра **Применить форму кредитования при обработке накладной в отчетах по накладной на заказ на продажу и проект** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-119">On the **Updates** tab, on the **Invoice** FastTab, set the **Apply the credit invoicing layout into sales and project invoice reports** option to **Yes**.</span></span>

![Настройка параметров расчетов с клиентами](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a><span data-ttu-id="eb2b4-121">Определение ссылок на исходные накладные</span><span class="sxs-lookup"><span data-stu-id="eb2b4-121">Define references to original invoices</span></span>

<span data-ttu-id="eb2b4-122">Используйте следующие процедуры для определения ссылок на исходные накладные на основе типа документа.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-122">Use the following procedures to define references to original invoices, based on the document type.</span></span>

### <a name="free-text-credit-note"></a><span data-ttu-id="eb2b4-123">Кредит-нота с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="eb2b4-123">Free text credit note</span></span>

1. <span data-ttu-id="eb2b4-124">Перейдите в раздел **Расчеты с клиентами** \> **Накладные** \> **Все накладные с произвольным текстом**.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-124">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="eb2b4-125">Создайте новую кредит-ноту или выберите существующую кредит-ноту.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-125">Create a new credit note, or select an existing credit note.</span></span>
3. <span data-ttu-id="eb2b4-126">Откройте накладную.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-126">Open the invoice.</span></span>
4. <span data-ttu-id="eb2b4-127">В области действий на вкладке **Накладная** в группе **Функции** выберите **Кредитование при обработке накладной**.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-127">On the Action Pane, on the **Invoice** tab, in the **Functions** group, select **Credit invoicing**.</span></span>
5. <span data-ttu-id="eb2b4-128">Введите ссылку на исходную накладную и выберите причину коррекции.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-128">Enter the reference to the original invoice, and select the reason for the correction.</span></span>

![Определение ссылки для накладной с произвольным текстом](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a><span data-ttu-id="eb2b4-130">Кредит-нота клиента</span><span class="sxs-lookup"><span data-stu-id="eb2b4-130">Customer credit note</span></span>

1. <span data-ttu-id="eb2b4-131">Перейдите в раздел **Расчеты с клиентами** \> **Заказы** \> **Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-131">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="eb2b4-132">Выберите и откройте заказ на продажу, по которому выставлена накладная, которая должна быть исправлена.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-132">Select and open the invoiced sales order that must be corrected.</span></span>
3. <span data-ttu-id="eb2b4-133">В области действий на вкладке **Продажа** в группе **Кредит-нота** выберите **Кредит-нота**.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-133">On the Action Pane, on the **Sell** tab, in the **Credit note** group, select **Credit note**.</span></span>
4. <span data-ttu-id="eb2b4-134">Введите причину для коррекции.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-134">Enter the reason for the correction.</span></span> <span data-ttu-id="eb2b4-135">Ссылка на исходную накладную устанавливается автоматически.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-135">The reference to the original invoice is automatically established.</span></span>

![Определение ссылки для заказа на продажу](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a><span data-ttu-id="eb2b4-137">Кредит-нота по проекту</span><span class="sxs-lookup"><span data-stu-id="eb2b4-137">Project credit note</span></span>

1. <span data-ttu-id="eb2b4-138">Перейдите в раздел **Управление и учет по проектам** \> **Накладные по проектам** \> **Накладные по проектам**.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-138">Go to **Project management and accounting** \> **Project invoices** \> **Project invoices**.</span></span>
2. <span data-ttu-id="eb2b4-139">Выберите и откройте накладную по проекту, которая должна быть исправлена.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-139">Select and open the project invoice that must be corrected.</span></span>
3. <span data-ttu-id="eb2b4-140">В области действий на вкладке **Накладная по проекту** в группе **Функции** выберите **Выбрать для кредит-ноты**.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-140">On the Action Pane, on the **Project invoice** tab, in the **Functions** group, select **Select for credit note**.</span></span>
4. <span data-ttu-id="eb2b4-141">Выберите **Кредитование при обработке накладной**.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-141">Select **Credit invoicing**.</span></span>
5. <span data-ttu-id="eb2b4-142">Введите причину для коррекции.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-142">Enter the reason for the correction.</span></span> <span data-ttu-id="eb2b4-143">Ссылка на исходную накладную устанавливается автоматически.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-143">The reference to the original invoice is automatically established.</span></span>

![Определение ссылки для накладной по проекту](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a><span data-ttu-id="eb2b4-145">Печать кредит-нот</span><span class="sxs-lookup"><span data-stu-id="eb2b4-145">Printing credit notes</span></span>

<span data-ttu-id="eb2b4-146">При печати кредит-нот с произвольным текстом, клиентских кредит-нот и кредит-нот по проекту они будут включать ссылку на исходную накладную и причину корректировки.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-146">When you print free text, customer, and project credit notes, they will include the reference to the original invoice and the correction reason.</span></span>

![Распечатанная кредит-нота](media/credit-note-FTI.jpg)

> [!NOTE]
> <span data-ttu-id="eb2b4-148">Убедитесь, что печатаемые форматы документов правильно настроены, в предположении, что будут распечатаны ссылки на исходные накладные.</span><span class="sxs-lookup"><span data-stu-id="eb2b4-148">Make sure that the printable formats of the documents are correctly configured, on the assumption that references to original invoices will be printed.</span></span>
