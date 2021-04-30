---
title: Ссылки на исходные накладные в кредит-нотах
description: В этой теме объясняется, как настроить и напечатать исходные номера накладных в соответствующих кредит-нотах.
author: ilkond
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8d7f32c5d3d29be8d1d2742c4017c1719cbd47a8
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897340"
---
# <a name="references-to-original-invoices-in-credit-notes"></a><span data-ttu-id="d4448-103">Ссылки на исходные накладные в кредит-нотах</span><span class="sxs-lookup"><span data-stu-id="d4448-103">References to original invoices in credit notes</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d4448-104">В некоторых странах и регионах имеется юридическое требование, чтобы распечатанные кредит-ноты включали ссылки на исходные накладные.</span><span class="sxs-lookup"><span data-stu-id="d4448-104">In some countries and regions, there is a legal requirement that printed credit notes include references to the original invoices.</span></span> <span data-ttu-id="d4448-105">В этой теме объясняется, как настроить и напечатать исходные номера накладных в соответствующих кредит-нотах.</span><span class="sxs-lookup"><span data-stu-id="d4448-105">This topic explains how to set up and print the original invoice numbers in related credit notes.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d4448-106">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="d4448-106">Prerequisites</span></span>

- <span data-ttu-id="d4448-107">В рабочей области **Управление функциями** включите функцию **Макет кредитования при обработке накладной для отчетов о накладных по продажам и проектам**.</span><span class="sxs-lookup"><span data-stu-id="d4448-107">In the **Feature management** workspace, turn on the **Credit invoicing layout for sales and project invoice reports** feature.</span></span> <span data-ttu-id="d4448-108">Дополнительные сведения см. в разделе [Обзор управления функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d4448-108">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="d4448-109">Подходящие для печати форматы необходимых документов должны быть настроены в управлении печатью.</span><span class="sxs-lookup"><span data-stu-id="d4448-109">The printable formats of the required documents must be configured in Print management.</span></span>

<span data-ttu-id="d4448-110">Функциональная возможность, описанная в данной теме, применяется к следующим документам:</span><span class="sxs-lookup"><span data-stu-id="d4448-110">The functionality that is described in this topic applies to the following documents:</span></span>

<span data-ttu-id="d4448-111">**Расчеты с клиентами**</span><span class="sxs-lookup"><span data-stu-id="d4448-111">**Accounts receivable**</span></span>

- <span data-ttu-id="d4448-112">Кредит-нота с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="d4448-112">Free text credit note</span></span>
- <span data-ttu-id="d4448-113">Кредит-нота клиента</span><span class="sxs-lookup"><span data-stu-id="d4448-113">Customer credit note</span></span>

<span data-ttu-id="d4448-114">**Управление и учет по проектам**</span><span class="sxs-lookup"><span data-stu-id="d4448-114">**Project management and accounting**</span></span>

- <span data-ttu-id="d4448-115">Кредит-нота по проекту</span><span class="sxs-lookup"><span data-stu-id="d4448-115">Project credit note</span></span>

## <a name="configure-accounts-receivable-parameters"></a><span data-ttu-id="d4448-116">Настройка параметров расчетов с клиентами</span><span class="sxs-lookup"><span data-stu-id="d4448-116">Configure Accounts receivable parameters</span></span>

<span data-ttu-id="d4448-117">Выполните следующие действия, чтобы настроить параметр, который определяет, будут ли ссылки на исходные накладные распечатаны в соответствующих кредит-нотах.</span><span class="sxs-lookup"><span data-stu-id="d4448-117">Follow these steps to set the parameter that controls whether references to the original invoices are printed in related credit notes.</span></span>

1. <span data-ttu-id="d4448-118">Перейдите в раздел **Расчеты с клиентами** \> **Настройка** \> **Параметры модуля расчетов с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="d4448-118">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="d4448-119">На вкладке **Обновления** на экспресс-вкладке **Накладная** установите для параметра **Применить форму кредитования при обработке накладной в отчетах по накладной на заказ на продажу и проект** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="d4448-119">On the **Updates** tab, on the **Invoice** FastTab, set the **Apply the credit invoicing layout into sales and project invoice reports** option to **Yes**.</span></span>

![Настройка параметров расчетов с клиентами](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a><span data-ttu-id="d4448-121">Определение ссылок на исходные накладные</span><span class="sxs-lookup"><span data-stu-id="d4448-121">Define references to original invoices</span></span>

<span data-ttu-id="d4448-122">Используйте следующие процедуры для определения ссылок на исходные накладные на основе типа документа.</span><span class="sxs-lookup"><span data-stu-id="d4448-122">Use the following procedures to define references to original invoices, based on the document type.</span></span>

### <a name="free-text-credit-note"></a><span data-ttu-id="d4448-123">Кредит-нота с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="d4448-123">Free text credit note</span></span>

1. <span data-ttu-id="d4448-124">Перейдите в раздел **Расчеты с клиентами** \> **Накладные** \> **Все накладные с произвольным текстом**.</span><span class="sxs-lookup"><span data-stu-id="d4448-124">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="d4448-125">Создайте новую кредит-ноту или выберите существующую кредит-ноту.</span><span class="sxs-lookup"><span data-stu-id="d4448-125">Create a new credit note, or select an existing credit note.</span></span>
3. <span data-ttu-id="d4448-126">Откройте накладную.</span><span class="sxs-lookup"><span data-stu-id="d4448-126">Open the invoice.</span></span>
4. <span data-ttu-id="d4448-127">В области действий на вкладке **Накладная** в группе **Функции** выберите **Кредитование при обработке накладной**.</span><span class="sxs-lookup"><span data-stu-id="d4448-127">On the Action Pane, on the **Invoice** tab, in the **Functions** group, select **Credit invoicing**.</span></span>
5. <span data-ttu-id="d4448-128">Введите ссылку на исходную накладную и выберите причину коррекции.</span><span class="sxs-lookup"><span data-stu-id="d4448-128">Enter the reference to the original invoice, and select the reason for the correction.</span></span>

![Определение ссылки для накладной с произвольным текстом](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a><span data-ttu-id="d4448-130">Кредит-нота клиента</span><span class="sxs-lookup"><span data-stu-id="d4448-130">Customer credit note</span></span>

1. <span data-ttu-id="d4448-131">Перейдите в раздел **Расчеты с клиентами** \> **Заказы** \> **Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="d4448-131">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="d4448-132">Выберите и откройте заказ на продажу, по которому выставлена накладная, которая должна быть исправлена.</span><span class="sxs-lookup"><span data-stu-id="d4448-132">Select and open the invoiced sales order that must be corrected.</span></span>
3. <span data-ttu-id="d4448-133">В области действий на вкладке **Продажа** в группе **Кредит-нота** выберите **Кредит-нота**.</span><span class="sxs-lookup"><span data-stu-id="d4448-133">On the Action Pane, on the **Sell** tab, in the **Credit note** group, select **Credit note**.</span></span>
4. <span data-ttu-id="d4448-134">Введите причину для коррекции.</span><span class="sxs-lookup"><span data-stu-id="d4448-134">Enter the reason for the correction.</span></span> <span data-ttu-id="d4448-135">Ссылка на исходную накладную устанавливается автоматически.</span><span class="sxs-lookup"><span data-stu-id="d4448-135">The reference to the original invoice is automatically established.</span></span>

![Определение ссылки для заказа на продажу](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a><span data-ttu-id="d4448-137">Кредит-нота по проекту</span><span class="sxs-lookup"><span data-stu-id="d4448-137">Project credit note</span></span>

1. <span data-ttu-id="d4448-138">Перейдите в раздел **Управление и учет по проектам** \> **Накладные по проектам** \> **Накладные по проектам**.</span><span class="sxs-lookup"><span data-stu-id="d4448-138">Go to **Project management and accounting** \> **Project invoices** \> **Project invoices**.</span></span>
2. <span data-ttu-id="d4448-139">Выберите и откройте накладную по проекту, которая должна быть исправлена.</span><span class="sxs-lookup"><span data-stu-id="d4448-139">Select and open the project invoice that must be corrected.</span></span>
3. <span data-ttu-id="d4448-140">В области действий на вкладке **Накладная по проекту** в группе **Функции** выберите **Выбрать для кредит-ноты**.</span><span class="sxs-lookup"><span data-stu-id="d4448-140">On the Action Pane, on the **Project invoice** tab, in the **Functions** group, select **Select for credit note**.</span></span>
4. <span data-ttu-id="d4448-141">Выберите **Кредитование при обработке накладной**.</span><span class="sxs-lookup"><span data-stu-id="d4448-141">Select **Credit invoicing**.</span></span>
5. <span data-ttu-id="d4448-142">Введите причину для коррекции.</span><span class="sxs-lookup"><span data-stu-id="d4448-142">Enter the reason for the correction.</span></span> <span data-ttu-id="d4448-143">Ссылка на исходную накладную устанавливается автоматически.</span><span class="sxs-lookup"><span data-stu-id="d4448-143">The reference to the original invoice is automatically established.</span></span>

![Определение ссылки для накладной по проекту](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a><span data-ttu-id="d4448-145">Печать кредит-нот</span><span class="sxs-lookup"><span data-stu-id="d4448-145">Printing credit notes</span></span>

<span data-ttu-id="d4448-146">При печати кредит-нот с произвольным текстом, клиентских кредит-нот и кредит-нот по проекту они будут включать ссылку на исходную накладную и причину корректировки.</span><span class="sxs-lookup"><span data-stu-id="d4448-146">When you print free text, customer, and project credit notes, they will include the reference to the original invoice and the correction reason.</span></span>

![Распечатанная кредит-нота](media/credit-note-FTI.jpg)

> [!NOTE]
> <span data-ttu-id="d4448-148">Убедитесь, что печатаемые форматы документов правильно настроены, в предположении, что будут распечатаны ссылки на исходные накладные.</span><span class="sxs-lookup"><span data-stu-id="d4448-148">Make sure that the printable formats of the documents are correctly configured, on the assumption that references to original invoices will be printed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]