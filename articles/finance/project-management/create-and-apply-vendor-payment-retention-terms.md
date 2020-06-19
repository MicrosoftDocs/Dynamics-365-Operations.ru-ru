---
title: Создание и применение условий удержания оплаты поставщику
description: В этой теме излагаются сведения о настройке и ведении условий удержания оплаты поставщику.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410261"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="14a10-103">Создание и применение условий удержания оплаты поставщику</span><span class="sxs-lookup"><span data-stu-id="14a10-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="14a10-104">Настройка условий удержания оплаты поставщику для проекта полезна, когда организация хочет сохранить часть платежей, произведенных поставщику.</span><span class="sxs-lookup"><span data-stu-id="14a10-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="14a10-105">Например, если необходимо удерживать платеж поставщику до тех пор, пока продукты не будут поставлены в соответствие с вашими ожиданиями.</span><span class="sxs-lookup"><span data-stu-id="14a10-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="14a10-106">В процессе переговоров с поставщиком о контракте можно указать условия удержания оплаты поставщику.</span><span class="sxs-lookup"><span data-stu-id="14a10-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="14a10-107">Создание условий удержания оплаты поставщику</span><span class="sxs-lookup"><span data-stu-id="14a10-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="14a10-108">Можно указать процент от платежей поставщику, который нужно удержать, и процент от ранее удержанных сумм, который нужно освободить.</span><span class="sxs-lookup"><span data-stu-id="14a10-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="14a10-109">Суммы автоматически удерживаются в накладных поставщика, пока контракт не достигнет указанного состояния завершения.</span><span class="sxs-lookup"><span data-stu-id="14a10-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="14a10-110">Настроенные условия удержания можно применить к любому проекту, в котором участвует поставщик.</span><span class="sxs-lookup"><span data-stu-id="14a10-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="14a10-111">Для настройки и ведения условий удержания платежей поставщику выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="14a10-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="14a10-112">Перейдите **Управление и учет по проектам** > **Удержание** > **Условия удержания оплаты поставщика**.</span><span class="sxs-lookup"><span data-stu-id="14a10-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="14a10-113">Выберите **Создать**, чтобы добавить новое условие удержания для поставщика.</span><span class="sxs-lookup"><span data-stu-id="14a10-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="14a10-114">Значение **Код правила** для нового условия вводится автоматически.</span><span class="sxs-lookup"><span data-stu-id="14a10-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="14a10-115">В поле **Описание** введите краткое описание, а на экспресс-вкладке **Условия** выберите **Добавить строку** для ввода значений условий для следующего:</span><span class="sxs-lookup"><span data-stu-id="14a10-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="14a10-116">**Процент поставленных единиц**: укажите процент завершения для условия.</span><span class="sxs-lookup"><span data-stu-id="14a10-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="14a10-117">Суммы автоматически удерживаются по накладным поставщика, пока степень завершенности проекта не достигнет указанного процента.</span><span class="sxs-lookup"><span data-stu-id="14a10-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="14a10-118">Например, если указать 50,00, суммы будут удерживаться до выполнения проекта на 50 %.</span><span class="sxs-lookup"><span data-stu-id="14a10-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="14a10-119">**Удерживаемый процент**: введите процент от суммы накладной поставщика для удержания.</span><span class="sxs-lookup"><span data-stu-id="14a10-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="14a10-120">Например, если ввести 10,00, 10 процентов от суммы в накладной поставщика удерживается, пока проект не достигнет процента завершения, выбранного в поле **Процент поставленных единиц**.</span><span class="sxs-lookup"><span data-stu-id="14a10-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="14a10-121">**Выплачиваемый процент** выберите **Добавить строку**, чтобы ввести процент от любых ранее удержанных сумм для освобождения на выбранном уровне завершенности проекта.</span><span class="sxs-lookup"><span data-stu-id="14a10-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="14a10-122">При наличии нескольких этапов для различных уровней завершения проекта укажите отдельную строку условия удержания для каждого правила удержания.</span><span class="sxs-lookup"><span data-stu-id="14a10-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="14a10-123">Каждая строка может определять разный процент для удержания и разный процент для освобождения по каждому из указанных уровней завершения проекта.</span><span class="sxs-lookup"><span data-stu-id="14a10-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="14a10-124">После создания условий удержания для поставщика можно применить условия к проекту.</span><span class="sxs-lookup"><span data-stu-id="14a10-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="14a10-125">Применение условий удержания оплаты поставщику для проекта</span><span class="sxs-lookup"><span data-stu-id="14a10-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="14a10-126">Перейдите **Управление и учет по проектам** > **Проекты** > **Все проекты**, чтобы открыть проект на странице списка проектов.</span><span class="sxs-lookup"><span data-stu-id="14a10-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="14a10-127">На экспресс-вкладке **Договора с поставщиками** выберите **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="14a10-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="14a10-128">В поле **Код счета** выберите один из следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="14a10-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="14a10-129">**Таблица**: условия удержания оплаты применяются к одному поставщику.</span><span class="sxs-lookup"><span data-stu-id="14a10-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="14a10-130">**Группа**: условия удержания оплаты применяются ко всем поставщикам в группе поставщиков.</span><span class="sxs-lookup"><span data-stu-id="14a10-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="14a10-131">**Все**: условия удержания оплаты применяются ко всем поставщикам.</span><span class="sxs-lookup"><span data-stu-id="14a10-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="14a10-132">В поле **Поставщик/группа поставщиков** выберите поставщика или группу поставщиков, к которым применяются условия удержания оплаты.</span><span class="sxs-lookup"><span data-stu-id="14a10-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="14a10-133">Это поле недоступно, если на предыдущем шаге выбрано значение **Все**.</span><span class="sxs-lookup"><span data-stu-id="14a10-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="14a10-134">В поле **Условия удержания поставщика** выберите условия удержания, созданные в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="14a10-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="14a10-135">Если проект предусматривает и настроенные для поставщика условия режима "оплата после получения оплаты" (PWP), в поле **Процент порогового уровня PWP** укажите процент порогового уровня для проекта.</span><span class="sxs-lookup"><span data-stu-id="14a10-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="14a10-136">Условия удержания поставщика также отображаются в заказах на покупку, создаваемых для поставщика.</span><span class="sxs-lookup"><span data-stu-id="14a10-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
