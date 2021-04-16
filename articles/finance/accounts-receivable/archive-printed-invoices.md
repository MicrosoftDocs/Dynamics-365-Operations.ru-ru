---
title: Архивировать напечатанные счета клиентов с хэш-номерами
description: В этом разделе описывается, как включить архивирование для хранения распечатанных накладных клиентов с хеш-числами.
author: ilyako
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5b0305381ee709ce52b18d171a1ea274e2126cce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827706"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a><span data-ttu-id="ae24b-103">Архивировать напечатанные счета клиентов с хэш-номерами</span><span class="sxs-lookup"><span data-stu-id="ae24b-103">Archive printed customer invoices with hash numbers</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="ae24b-104">В некоторых странах имеется законное требование о хранении рассчитанных хеш-чисел в системе вместе с распечаткой некоторых документов.</span><span class="sxs-lookup"><span data-stu-id="ae24b-104">In some countries, there is a legal requirement to store calculated hash numbers in the system together with printouts of some documents.</span></span> <span data-ttu-id="ae24b-105">Хэш-числа могут использоваться для отчетности в органы власти и во время аудита.</span><span class="sxs-lookup"><span data-stu-id="ae24b-105">Hash numbers can be used for reporting to authorities and during audits.</span></span>

<span data-ttu-id="ae24b-106">В этом разделе описывается, как настроить архивирование для хранения распечатанных накладных клиентов с хеш-числами.</span><span class="sxs-lookup"><span data-stu-id="ae24b-106">This topic explains how to configure archiving in order to store printed customer invoices with hash numbers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ae24b-107">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="ae24b-107">Prerequisites</span></span>

- <span data-ttu-id="ae24b-108">В рабочей области **управления функциями** включите функцию, **Архивировать распечатанные накладные клиента с хеш-числами**.</span><span class="sxs-lookup"><span data-stu-id="ae24b-108">In the **Feature management** workspace, turn on the feature, **Archive printed customer invoices with hash numbers**.</span></span> <span data-ttu-id="ae24b-109">Дополнительные сведения см. в разделе [Обзор управления функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ae24b-109">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="ae24b-110">Настройте подходящие для печати форматы необходимых документов в **управлении печатью**.</span><span class="sxs-lookup"><span data-stu-id="ae24b-110">Configure the printable formats of required documents in **Print management**.</span></span>

<span data-ttu-id="ae24b-111">Эти функции применимы к следующим документам.</span><span class="sxs-lookup"><span data-stu-id="ae24b-111">This functionality is applicable to the following documents.</span></span>

<span data-ttu-id="ae24b-112">**Расчеты с клиентами**</span><span class="sxs-lookup"><span data-stu-id="ae24b-112">**Accounts receivable**</span></span>
- <span data-ttu-id="ae24b-113">Накладная клиента</span><span class="sxs-lookup"><span data-stu-id="ae24b-113">Customer invoice</span></span>
- <span data-ttu-id="ae24b-114">Кредит-нота клиента</span><span class="sxs-lookup"><span data-stu-id="ae24b-114">Customer credit note</span></span>
- <span data-ttu-id="ae24b-115">Накладная с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="ae24b-115">Free text invoice</span></span>
- <span data-ttu-id="ae24b-116">Кредит-нота с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="ae24b-116">Free text credit note</span></span>

<span data-ttu-id="ae24b-117">**Управление и учет по проектам**</span><span class="sxs-lookup"><span data-stu-id="ae24b-117">**Project management and accounting**</span></span>
- <span data-ttu-id="ae24b-118">Накладная по проекту</span><span class="sxs-lookup"><span data-stu-id="ae24b-118">Project invoice</span></span>
- <span data-ttu-id="ae24b-119">Кредит-нота по проекту</span><span class="sxs-lookup"><span data-stu-id="ae24b-119">Project credit note</span></span>

## <a name="configure-customer-master-data"></a><span data-ttu-id="ae24b-120">Настройка справочника клиентов</span><span class="sxs-lookup"><span data-stu-id="ae24b-120">Configure customer master data</span></span>
<span data-ttu-id="ae24b-121">Выполните следующие шаги, чтобы настроить данные клиента и включить возможность автоматического сохранения распечатанных накладных в качестве вложений.</span><span class="sxs-lookup"><span data-stu-id="ae24b-121">Complete the following steps to configure customer data and turn on the ability to automatically save printed invoices as attachments.</span></span>

1. <span data-ttu-id="ae24b-122">Перейдите в раздел **Расчеты с клиентами** > **Все клиенты**.</span><span class="sxs-lookup"><span data-stu-id="ae24b-122">Go to **Accounts receivable** > **All customers**.</span></span> 
2. <span data-ttu-id="ae24b-123">Выберите клиента и на вкладке **Накладные и поставка** в разделе **E-INVOCE** в поле **вложение электронной накладной** выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="ae24b-123">Select a customer, and on the **Invoice and delivery** FastTab, in the **E-INVOCE** section, in the **eInvoice attachment** field, select **Yes**.</span></span>

## <a name="print-invoices"></a><span data-ttu-id="ae24b-124">Печать накладных</span><span class="sxs-lookup"><span data-stu-id="ae24b-124">Print invoices</span></span>
<span data-ttu-id="ae24b-125">Можно выполнить разноску и печать любого произвольного текста, клиента, накладной по проекту или кредит-ноты для клиента, настроенного в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="ae24b-125">You can post and print any free text, customer, and project invoice or credit note for the customer configured in the previous procedure.</span></span>

<span data-ttu-id="ae24b-126">Открывает страницу **вложения** для распечатанной накладной.</span><span class="sxs-lookup"><span data-stu-id="ae24b-126">Open the **Attachments** page for the printed invoice.</span></span> <span data-ttu-id="ae24b-127">На экспресс-вкладке **вложения** в группе полей **дополнительные сведения** в поле **хэш-число документа** найдите сохраненное хеш-число, рассчитанное для напечатанной накладной.</span><span class="sxs-lookup"><span data-stu-id="ae24b-127">On the **Attachment** FastTab, in the **Additional details** field group, in **Document hash number** field, find the stored hash number calculated for the printed invoice.</span></span>

![Хэш-число вложения](media/attach-hash-num.jpg)

