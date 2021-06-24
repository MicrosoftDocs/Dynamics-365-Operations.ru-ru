---
title: Панель мониторинга управления использованием
description: В этой теме объясняется, как использовать панель мониторинга управления использованием для отслеживания использования службы электронных накладных и поддержания соответствия требованиям.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 411c2d33c81738dcacfb7c8feec991d0fd06fb78
ms.sourcegitcommit: 9069a8511dfe11d09a2b51d32547ba10fea48bed
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/02/2021
ms.locfileid: "6130514"
---
# <a name="usage-management-dashboard"></a><span data-ttu-id="aa148-103">Панель мониторинга управления использованием</span><span class="sxs-lookup"><span data-stu-id="aa148-103">Usage management dashboard</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa148-104">Панель мониторинга **Управление использованием** помогает отслеживать использование службы электронных накладных и, таким образом, помогает организации соответствовать требованиям ежемесячного использования.</span><span class="sxs-lookup"><span data-stu-id="aa148-104">The **Usage management** dashboard helps you monitor usage of the Electronic Invoicing service, and therefore helps your organization remain compliant in terms of its monthly usage.</span></span> <span data-ttu-id="aa148-105">Соответствие определяется путем расчета отправляемого объема и его сравнения с полученным объемом отправленных данных для выявления отклонений между приобретенным объемом и использованным объемом.</span><span class="sxs-lookup"><span data-stu-id="aa148-105">Compliance is determined by calculating the submission volume and comparing it with the acquired volume of submissions to identify any deviations between the acquired volume and the used volume.</span></span>

<span data-ttu-id="aa148-106">Панель мониторинга содержит следующие индикаторы:</span><span class="sxs-lookup"><span data-stu-id="aa148-106">The dashboard includes the following indicators:</span></span>

- <span data-ttu-id="aa148-107">Один индикатор затрат, который можно использовать для отслеживания потребления для целей соответствия лицензированию:</span><span class="sxs-lookup"><span data-stu-id="aa148-107">One cost indicator that you can use to monitor consumption for licensing compliance purposes:</span></span>

    - <span data-ttu-id="aa148-108">Использование в месяц (экспорт)</span><span class="sxs-lookup"><span data-stu-id="aa148-108">Usage per month (export)</span></span>

- <span data-ttu-id="aa148-109">Три рабочих индикатора, которые можно использовать для отслеживания использования службы электронных накладных для целей управления:</span><span class="sxs-lookup"><span data-stu-id="aa148-109">Three operational indicators that you can use to track usage of the Electronic Invoicing service for management purposes:</span></span>

    - <span data-ttu-id="aa148-110">Использование по функции</span><span class="sxs-lookup"><span data-stu-id="aa148-110">Usage by feature</span></span>
    - <span data-ttu-id="aa148-111">Использование по среде</span><span class="sxs-lookup"><span data-stu-id="aa148-111">Usage by environment</span></span>
    - <span data-ttu-id="aa148-112">Использование в месяц (импорт)</span><span class="sxs-lookup"><span data-stu-id="aa148-112">Usage per month (import)</span></span>

## <a name="measurement-scope"></a><span data-ttu-id="aa148-113">Область измерения</span><span class="sxs-lookup"><span data-stu-id="aa148-113">Measurement scope</span></span>

- <span data-ttu-id="aa148-114">Единица измерения:</span><span class="sxs-lookup"><span data-stu-id="aa148-114">Unit of measure:</span></span> 

    <span data-ttu-id="aa148-115">Панель мониторинга **Управление использованием** подсчитывает отправку бизнес-документов и импортированных электронных накладных.</span><span class="sxs-lookup"><span data-stu-id="aa148-115">The **Usage management** dashboard counts the submission of business documents and imported electronic invoices.</span></span>

- <span data-ttu-id="aa148-116">Организация:</span><span class="sxs-lookup"><span data-stu-id="aa148-116">Organization:</span></span> 

    <span data-ttu-id="aa148-117">Подсчет суммируется по коду клиента вашей организации, независимо от числа экземпляров Microsoft Dynamics 365 Finance или Dynamics 365 Supply Chain Management или числа юридических лиц, в которых активирована служба электронных накладных.</span><span class="sxs-lookup"><span data-stu-id="aa148-117">Counting is summarized by the tenant ID of your organization, regardless of the number of instances of Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management, or the number of legal entities where the Electronic Invoicing service is enabled.</span></span>


## <a name="indicator-usage-per-month-export"></a><span data-ttu-id="aa148-118">Индикатор: использование в месяц (экспорт)</span><span class="sxs-lookup"><span data-stu-id="aa148-118">Indicator: Usage per month (export)</span></span>

<span data-ttu-id="aa148-119">Этот индикатор предоставляет подробные сведения об электронных накладных, которые ваша организация выставила в течение определенного периода.</span><span class="sxs-lookup"><span data-stu-id="aa148-119">This indicator provides details about the electronic invoices that your organization issues during a defined period.</span></span>

### <a name="scope"></a><span data-ttu-id="aa148-120">Результат</span><span class="sxs-lookup"><span data-stu-id="aa148-120">Scope</span></span>
- <span data-ttu-id="aa148-121">Число деловых документов, отправленных из Finance и Supply Chain Management в службу электронного выставления накладных, независимо от количества строк, содержащихся в этих деловых документах.</span><span class="sxs-lookup"><span data-stu-id="aa148-121">The number of business documents that are submitted from Finance and Supply Chain Management to the Electronic Invoicing service, regardless of number of lines that those business documents contain.</span></span>
- <span data-ttu-id="aa148-122">Число отправленных бизнес-документов, успешно обработанных службой электронных накладных.</span><span class="sxs-lookup"><span data-stu-id="aa148-122">The number of submitted business documents that are successfully processed by the Electronic Invoicing service.</span></span> <span data-ttu-id="aa148-123">Документ считается успешно обработанным, когда завершен поток действий, определенных в настройке функций.</span><span class="sxs-lookup"><span data-stu-id="aa148-123">A document is considered successfully processed when the flow of actions that are defined in the feature setup is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="aa148-124">При отправке электронной накладной на внешнюю веб-службу подсчет не зависит от результатов обработки веб-службой (принята, отклонена или ошибка проверки схемы).</span><span class="sxs-lookup"><span data-stu-id="aa148-124">When an electronic invoice is submitted to an external web service, counting is independent of the results of web service processing (accepted, rejected, or schema validation error).</span></span> <span data-ttu-id="aa148-125">Если веб-служба получила и ответила на запрос из службы электронных накладных, отправка считается допустимой для подсчета.</span><span class="sxs-lookup"><span data-stu-id="aa148-125">If the web service received and responded to the request from the Electronic Invoicing service, the submission is considered a valid counting.</span></span>

- <span data-ttu-id="aa148-126">**Исключение:** деловые документы не подсчитываются, если они повторно передаются из Finance и Supply Chain Management в электронную службу выставления накладных, например в сценариях, в которых для изменения статуса электронной накладной требуется повторная отправка одного и того же делового документа.</span><span class="sxs-lookup"><span data-stu-id="aa148-126">**Exception:** Business documents aren't counted if they are resubmitted from Finance and Supply Chain Management to the Electronic Invoicing service, such as in the scenarios where a resubmission of the same business document is required to change the status of the electronic invoice.</span></span> <span data-ttu-id="aa148-127">Например, выдача электронной накладной для Бразилии (налоговый документ) учитывается как действительная, но запрос отмены для нее не учитывается.</span><span class="sxs-lookup"><span data-stu-id="aa148-127">For example, issuance of a Brazilian electronic invoice (fiscal document) is counted as valid, but the cancellation request for it isn't counted.</span></span>


### <a name="calculation"></a><span data-ttu-id="aa148-128">Расчет</span><span class="sxs-lookup"><span data-stu-id="aa148-128">Calculation</span></span>

<span data-ttu-id="aa148-129">Сальдо рассчитывается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="aa148-129">The calculation of the balance is calculated as follows:</span></span>

<span data-ttu-id="aa148-130">Сальдо = Бесплатно + Куплено - Использовано</span><span class="sxs-lookup"><span data-stu-id="aa148-130">Balance = Free + Purchased – Used</span></span>

<span data-ttu-id="aa148-131">Где:</span><span class="sxs-lookup"><span data-stu-id="aa148-131">Where:</span></span>

- <span data-ttu-id="aa148-132">Бесплатно:</span><span class="sxs-lookup"><span data-stu-id="aa148-132">Free:</span></span>
  
    <span data-ttu-id="aa148-133">Бесплатный объем деловых документов, которые клиент может отправлять в месяц.</span><span class="sxs-lookup"><span data-stu-id="aa148-133">A free volume of business documents the customer can submit per month.</span></span> <span data-ttu-id="aa148-134">Он включает в себя пакет из 100 деловых документов, которые могут быть отправлены в службу электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="aa148-134">It includes a package of 100 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="aa148-135">Бесплатный объем не является накопительным, и оставшееся сальдо не переносится на следующий период.</span><span class="sxs-lookup"><span data-stu-id="aa148-135">Free volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="aa148-136">Куплено:</span><span class="sxs-lookup"><span data-stu-id="aa148-136">Purchased:</span></span>
  
    <span data-ttu-id="aa148-137">Пакет из 1000 деловых документов, которые могут быть отправлены в службу электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="aa148-137">A package of 1,000 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="aa148-138">Этот пакет необходимо ежемесячно приобрести в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="aa148-138">This package must be acquired for your organization on a monthly basis.</span></span> <span data-ttu-id="aa148-139">Приобретенный объем не является накопительным, и оставшееся сальдо не переносится на следующий период.</span><span class="sxs-lookup"><span data-stu-id="aa148-139">Purchased volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="aa148-140">Использовано:</span><span class="sxs-lookup"><span data-stu-id="aa148-140">Used:</span></span> 

    <span data-ttu-id="aa148-141">Число отправок деловых документов в службу электронного выставления накладных в соответствии с определенными критериями.</span><span class="sxs-lookup"><span data-stu-id="aa148-141">The count of business document submissions to the Electronic Invoicing service according to defined criteria.</span></span>
   
> [!IMPORTANT]
> <span data-ttu-id="aa148-142">Если ваша организация планирует превысить месячный объем 100 бесплатных отправок, приобретите пиковый объем, чтобы обеспечить, что вы сохранили соответствие политике лицензирования Майкрософт для службы электронных накладных.</span><span class="sxs-lookup"><span data-stu-id="aa148-142">If your organization plans to exceed the monthly volume of 100 free submissions, purchase the peak volume to ensure that you remain compliant with the Microsoft licensing policy for the Electronic Invoicing service.</span></span>
>
> <span data-ttu-id="aa148-143">В настоящее время приобретенный объем должен вводиться вручную, в соответствии с датой приобретения, в качестве нескольких пакетов по 1000 отправок.</span><span class="sxs-lookup"><span data-stu-id="aa148-143">Currently, purchased volume must be manually entered, according to the date of acquisition, as multiple packages of 1,000 submissions.</span></span>

## <a name="indicator-usage-by-feature"></a><span data-ttu-id="aa148-144">Индикатор: использование по функциям</span><span class="sxs-lookup"><span data-stu-id="aa148-144">Indicator: Usage by feature</span></span>

<span data-ttu-id="aa148-145">Этот индикатор показывает использование функций электронного выставления накладных для выдачи электронных накладных за определенный период.</span><span class="sxs-lookup"><span data-stu-id="aa148-145">This indicator shows the usage of electronic invoicing features for issuance of electronic invoices during a defined period.</span></span>

- <span data-ttu-id="aa148-146">Расчет:</span><span class="sxs-lookup"><span data-stu-id="aa148-146">Calculation:</span></span>
  
    <span data-ttu-id="aa148-147">Использовано = сколько раз каждая функция электронного выставления накладных была использована при отправке деловых документов в службу электронных накладных.</span><span class="sxs-lookup"><span data-stu-id="aa148-147">Used = The count of how many times each electronic invoicing feature was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-by-environment"></a><span data-ttu-id="aa148-148">Индикатор: использование по средам</span><span class="sxs-lookup"><span data-stu-id="aa148-148">Indicator: Usage by environment</span></span>

<span data-ttu-id="aa148-149">Этот индикатор показывает использование сред электронного выставления накладных в течение определенного периода.</span><span class="sxs-lookup"><span data-stu-id="aa148-149">This indicator shows the usage of electronic invoicing service environments during a defined period.</span></span>

- <span data-ttu-id="aa148-150">Расчет:</span><span class="sxs-lookup"><span data-stu-id="aa148-150">Calculation:</span></span>
    
    <span data-ttu-id="aa148-151">Использовано = сколько раз каждая среда службы электронного выставления накладных была использована при отправке деловых документов в службу электронных накладных.</span><span class="sxs-lookup"><span data-stu-id="aa148-151">Used = The count of how many times each electronic invoicing service environment was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-per-month-import"></a><span data-ttu-id="aa148-152">Индикатор: использование в месяц (импорт)</span><span class="sxs-lookup"><span data-stu-id="aa148-152">Indicator: Usage per month (import)</span></span>

<span data-ttu-id="aa148-153">Этот индикатор показывает объем импорта электронных накладных с помощью службы электронного выставления накладных в Finance и Supply Chain Management в течение определенного периода времени.</span><span class="sxs-lookup"><span data-stu-id="aa148-153">This indicator shows the volume of importation of electronic invoices by Electronic Invoicing service into Finance and Supply Chain Management during a defined period.</span></span>

- <span data-ttu-id="aa148-154">Область:</span><span class="sxs-lookup"><span data-stu-id="aa148-154">Scope:</span></span>

    <span data-ttu-id="aa148-155">Электронные накладные, которые импортированы в Finance и Supply Chain Management, независимо от количества строк, содержащихся в электронных накладных.</span><span class="sxs-lookup"><span data-stu-id="aa148-155">Electronic invoices that are imported into Finance and Supply Chain Management, regardless of the number of lines that those electronic invoices contain.</span></span>

- <span data-ttu-id="aa148-156">Расчет:</span><span class="sxs-lookup"><span data-stu-id="aa148-156">Calculation:</span></span>

    <span data-ttu-id="aa148-157">Получено = число импортированных электронных накладных в Finance и Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="aa148-157">Received = The count of imported electronic invoices into Finance and Supply Chain Management.</span></span>

## <a name="functions"></a><span data-ttu-id="aa148-158">Функции</span><span class="sxs-lookup"><span data-stu-id="aa148-158">Functions</span></span>
### <a name="purchase"></a><span data-ttu-id="aa148-159">Покупка</span><span class="sxs-lookup"><span data-stu-id="aa148-159">Purchase</span></span>

<span data-ttu-id="aa148-160">На вкладке **Использование в месяц (экспорт)** выберите **Покупка**, чтобы вручную зарегистрировать сумму приобретенных отправок.</span><span class="sxs-lookup"><span data-stu-id="aa148-160">On the **Usage per month (export)** tab, select **Purchase** to manually register the amount of acquired submissions.</span></span>

<span data-ttu-id="aa148-161">Для заданной даты выберите **Создать** и введите число **Пакетов**, приобретенных на эту дату.</span><span class="sxs-lookup"><span data-stu-id="aa148-161">For a given date, select **New** and enter the number of **Packages** acquired for on that date.</span></span>

<span data-ttu-id="aa148-162">**Количество** рассчитывается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="aa148-162">The **Quantity** is calculated as:</span></span>

<span data-ttu-id="aa148-163">Количество = Пакеты \* 1000</span><span class="sxs-lookup"><span data-stu-id="aa148-163">Quantity = Packages \* 1.000</span></span>

<span data-ttu-id="aa148-164">Рассчитанное **Количество** отражается в поле **Приобретено** из индикатора **Использование в месяц (экспорт)**.</span><span class="sxs-lookup"><span data-stu-id="aa148-164">The calculated **Quantity** reflects in the **Purchased** from the indicator **Usage per month (export)**.</span></span>

### <a name="update"></a><span data-ttu-id="aa148-165">Обновить </span><span class="sxs-lookup"><span data-stu-id="aa148-165">Update</span></span>

<span data-ttu-id="aa148-166">В области действий выберите **Обновить**, чтобы обновить вычисление и обновить данные, отображаемые на странице и в диаграмме.</span><span class="sxs-lookup"><span data-stu-id="aa148-166">On the Action Pane, select **Update** to refresh the calculation and update the data shown on the page and in the chart.</span></span>

### <a name="reset-history-data"></a><span data-ttu-id="aa148-167">Сбросить исторические данные</span><span class="sxs-lookup"><span data-stu-id="aa148-167">Reset history data</span></span>

<span data-ttu-id="aa148-168">В области действий выберите **Сбросить исторические данные**, чтобы обновить базу данных, из которой будут рассчитываться индикаторы.</span><span class="sxs-lookup"><span data-stu-id="aa148-168">On the Action Pane, select **Reset history data** to refresh the database from where the indicators are calculated.</span></span>




> [!NOTE]
> <span data-ttu-id="aa148-169">На панели мониторинга **Управление использованием** не отображаются денежные суммы.</span><span class="sxs-lookup"><span data-stu-id="aa148-169">The **Usage management** dashboard doesn't show monetary amounts.</span></span> <span data-ttu-id="aa148-170">Вместо этого отображается только объем подсчитанных отправок и импортированных документов.</span><span class="sxs-lookup"><span data-stu-id="aa148-170">Instead, it shows only the volume of counted submissions and imported documents.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
