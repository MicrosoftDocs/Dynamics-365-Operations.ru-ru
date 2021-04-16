---
title: Служба расчета налогов (предварительная версия)
description: В этой теме описывается общая область и функции службы расчета налогов.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818232"
---
# <a name="tax-calculation-service-preview"></a><span data-ttu-id="2e1ce-103">Служба расчета налогов (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="2e1ce-103">Tax calculation service (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="2e1ce-104">Служба расчета налогов представляет собой гипермасштабируемую многоклиентскую службу, которая позволяет модулю Global Tax Engine автоматизировать и упростить процесс определения и расчета налогов.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-104">The tax calculation service is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="2e1ce-105">Модуль налогов полностью настраиваемый.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="2e1ce-106">Элементы, которые могут быть настроены, включают в себя (но не ограничиваются этим) модель налогооблагаемых данных, налоговый код, матрицу налоговой применимости и формулу расчета налога.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="2e1ce-107">Модуль обработки налогов выполняется на платформе Microsoft Azure Core Services и предлагает современные технологии и экспоненциальную масштабируемость.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="2e1ce-108">Служба расчета налогов интегрируется с Dynamics 365 Finance и Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-108">The tax calculation service integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="2e1ce-109">В конечном итоге она также интегрируется с Dynamics 365 Project Operations, Dynamics 365 Commerce и другими собственными приложениями и приложениями сторонних разработчиков.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="2e1ce-110">Служба расчета налогов — это налоговый модуль на основе Microsoft, который предлагает экспоненциальную масштабируемость.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-110">The tax calculation service is a Microsoft-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="2e1ce-111">Он может помочь выполнить следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="2e1ce-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="2e1ce-112">Настройка службы расчета налогов с помощью службы Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="2e1ce-112">Configure the tax calculation service through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="2e1ce-113">RCS — это расширенная версия конструктора электронной отчетности (ER), которая доступна в качестве автономной службы.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="2e1ce-114">Настройка налоговой матрицы, чтобы автоматически определять налоговые коды и ставки.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="2e1ce-115">Настройка налоговой матрицы, чтобы автоматически определять номер налоговой регистрации.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="2e1ce-116">Настройка конструктора расчета налогов для определения формул и условий.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="2e1ce-117">Совместное использование решения определения и расчета налогов для нескольких юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="2e1ce-118">Чтобы использовать службу расчета налога, установите надстройку службы расчета налогов из проекта в Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="2e1ce-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="2e1ce-119">Затем выполните настройку в RCS и включите службу расчета налогов в Finance и Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="2e1ce-120">Дополнительные сведения см. в разделе [Начало работы с налоговой службой](https://go.microsoft.com/fwlink/?linkid=2138482).</span><span class="sxs-lookup"><span data-stu-id="2e1ce-120">For more information, see [Get started with tax service](https://go.microsoft.com/fwlink/?linkid=2138482).</span></span>

## <a name="availability"></a><span data-ttu-id="2e1ce-121">Доступность</span><span class="sxs-lookup"><span data-stu-id="2e1ce-121">Availability</span></span>

<span data-ttu-id="2e1ce-122">Служба расчета налогов доступна только в средах песочницы и для избранных клиентов через программу общедоступной предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-122">The tax calculation service is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="2e1ce-123">В конечном итоге она станет общедоступной для всех клиентов и производственных сред.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="2e1ce-124">Новые функции будут по-прежнему предоставляться в службе расчета налогов.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-124">New features will continue to be delivered in the tax calculation service.</span></span> <span data-ttu-id="2e1ce-125">Поэтому обязательно регулярно проверяйте самую актуальную документацию, чтобы узнать о покрытии и области поддерживаемых функций.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-125">Therefore, be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="2e1ce-126">Служба расчета налогов развернута в следующих географических регионах Azure.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-126">The tax calculation service is deployed in the following Azure geographies.</span></span> <span data-ttu-id="2e1ce-127">Она также будет развернута в большем числе географических регионов Azure на основе потребностей клиентов:</span><span class="sxs-lookup"><span data-stu-id="2e1ce-127">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="2e1ce-128">США</span><span class="sxs-lookup"><span data-stu-id="2e1ce-128">United States</span></span>
- <span data-ttu-id="2e1ce-129">Европа</span><span class="sxs-lookup"><span data-stu-id="2e1ce-129">Europe</span></span>
- <span data-ttu-id="2e1ce-130">Франция</span><span class="sxs-lookup"><span data-stu-id="2e1ce-130">France</span></span>
- <span data-ttu-id="2e1ce-131">Великобритания</span><span class="sxs-lookup"><span data-stu-id="2e1ce-131">United Kingdom</span></span>

> [!NOTE]
> <span data-ttu-id="2e1ce-132">Служба расчета налогов не поддерживает локальные развертывания Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-132">The tax calculation service doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="2e1ce-133">Она также не поддерживает предыдущие версии, такие как Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-133">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="2e1ce-134">Основные функции</span><span class="sxs-lookup"><span data-stu-id="2e1ce-134">Feature highlights</span></span>

- <span data-ttu-id="2e1ce-135">Настраиваемая налоговая матрица, чтобы автоматически определять и рассчитывать налог</span><span class="sxs-lookup"><span data-stu-id="2e1ce-135">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="2e1ce-136">Поддержка нескольких номеров регистрации налога на добавленную стоимость (НДС)</span><span class="sxs-lookup"><span data-stu-id="2e1ce-136">Support for multiple value-added tax (VAT) registration numbers</span></span>
- <span data-ttu-id="2e1ce-137">Поддержка заказов на перемещение для определения и расчета налога</span><span class="sxs-lookup"><span data-stu-id="2e1ce-137">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="2e1ce-138">Поддержка заказов на перемещение для определения нескольких номеров регистрации НДС</span><span class="sxs-lookup"><span data-stu-id="2e1ce-138">Transfer order support for determination of multiple VAT registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="2e1ce-139">Поддерживаемые проводки</span><span class="sxs-lookup"><span data-stu-id="2e1ce-139">Supported transactions</span></span>

<span data-ttu-id="2e1ce-140">Службу расчета налога можно включить по юридическим лицам и проводкам.</span><span class="sxs-lookup"><span data-stu-id="2e1ce-140">The tax calculation service can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="2e1ce-141">Следующие проводки поддерживаются:</span><span class="sxs-lookup"><span data-stu-id="2e1ce-141">The following transactions are supported:</span></span>

- <span data-ttu-id="2e1ce-142">Процесс продаж</span><span class="sxs-lookup"><span data-stu-id="2e1ce-142">Sales process</span></span>

    - <span data-ttu-id="2e1ce-143">Предложение по продажам</span><span class="sxs-lookup"><span data-stu-id="2e1ce-143">Sales quotation</span></span>
    - <span data-ttu-id="2e1ce-144">Заказ на продажу</span><span class="sxs-lookup"><span data-stu-id="2e1ce-144">Sales order</span></span>
    - <span data-ttu-id="2e1ce-145">Подтверждение</span><span class="sxs-lookup"><span data-stu-id="2e1ce-145">Confirmation</span></span>
    - <span data-ttu-id="2e1ce-146">Сборочный лист</span><span class="sxs-lookup"><span data-stu-id="2e1ce-146">Picking list</span></span>
    - <span data-ttu-id="2e1ce-147">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="2e1ce-147">Packing slip</span></span>
    - <span data-ttu-id="2e1ce-148">Накладная заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="2e1ce-148">Sales invoice</span></span>
    - <span data-ttu-id="2e1ce-149">Кредит-нота</span><span class="sxs-lookup"><span data-stu-id="2e1ce-149">Credit note</span></span>
    - <span data-ttu-id="2e1ce-150">Заказ на возврат</span><span class="sxs-lookup"><span data-stu-id="2e1ce-150">Return order</span></span>
    - <span data-ttu-id="2e1ce-151">Накладные расходы по заголовку</span><span class="sxs-lookup"><span data-stu-id="2e1ce-151">Header miscellaneous charge</span></span>
    - <span data-ttu-id="2e1ce-152">Накладные расходы по строке</span><span class="sxs-lookup"><span data-stu-id="2e1ce-152">Line miscellaneous charge</span></span>

- <span data-ttu-id="2e1ce-153">Процесс покупки</span><span class="sxs-lookup"><span data-stu-id="2e1ce-153">Purchase process</span></span>

    - <span data-ttu-id="2e1ce-154">Заказ на покупку</span><span class="sxs-lookup"><span data-stu-id="2e1ce-154">Purchase order</span></span>
    - <span data-ttu-id="2e1ce-155">Подтверждение</span><span class="sxs-lookup"><span data-stu-id="2e1ce-155">Confirmation</span></span>
    - <span data-ttu-id="2e1ce-156">Список прихода</span><span class="sxs-lookup"><span data-stu-id="2e1ce-156">Receipts list</span></span>
    - <span data-ttu-id="2e1ce-157">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="2e1ce-157">Product receipt</span></span>
    - <span data-ttu-id="2e1ce-158">Накладная по покупке </span><span class="sxs-lookup"><span data-stu-id="2e1ce-158">Purchase invoice</span></span>
    - <span data-ttu-id="2e1ce-159">Накладные расходы по заголовку</span><span class="sxs-lookup"><span data-stu-id="2e1ce-159">Header miscellaneous charge</span></span>
    - <span data-ttu-id="2e1ce-160">Накладные расходы по строке</span><span class="sxs-lookup"><span data-stu-id="2e1ce-160">Line miscellaneous charge</span></span>
    - <span data-ttu-id="2e1ce-161">Кредит-нота</span><span class="sxs-lookup"><span data-stu-id="2e1ce-161">Credit note</span></span>
    - <span data-ttu-id="2e1ce-162">Заказ на возврат</span><span class="sxs-lookup"><span data-stu-id="2e1ce-162">Return order</span></span>
    - <span data-ttu-id="2e1ce-163">Заявка на закупку</span><span class="sxs-lookup"><span data-stu-id="2e1ce-163">Purchase requisition</span></span>
    - <span data-ttu-id="2e1ce-164">Накладные расходы строки заявки на покупку</span><span class="sxs-lookup"><span data-stu-id="2e1ce-164">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="2e1ce-165">Запрос предложения</span><span class="sxs-lookup"><span data-stu-id="2e1ce-165">Request for quotation</span></span>
    - <span data-ttu-id="2e1ce-166">Накладные расходы заголовка запроса предложения</span><span class="sxs-lookup"><span data-stu-id="2e1ce-166">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="2e1ce-167">Накладные расходы строки запроса предложения</span><span class="sxs-lookup"><span data-stu-id="2e1ce-167">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="2e1ce-168">Процесс запасов</span><span class="sxs-lookup"><span data-stu-id="2e1ce-168">Inventory process</span></span>

    - <span data-ttu-id="2e1ce-169">Заказ на перемещение — отгрузка</span><span class="sxs-lookup"><span data-stu-id="2e1ce-169">Transfer order – ship</span></span>
    - <span data-ttu-id="2e1ce-170">Заказ на перемещение — получение</span><span class="sxs-lookup"><span data-stu-id="2e1ce-170">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="2e1ce-171">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2e1ce-171">Related resources</span></span>

[<span data-ttu-id="2e1ce-172">Начало работы с налоговой службой</span><span class="sxs-lookup"><span data-stu-id="2e1ce-172">Get started with tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138482)

[<span data-ttu-id="2e1ce-173">Множественный регистрационный номер НДС</span><span class="sxs-lookup"><span data-stu-id="2e1ce-173">Multiple VAT registration number</span></span>](https://go.microsoft.com/fwlink/?linkid=2153387)

[<span data-ttu-id="2e1ce-174">Поддержка функций налогов для заказа на перемещение</span><span class="sxs-lookup"><span data-stu-id="2e1ce-174">Tax feature support for transfer order</span></span>](https://go.microsoft.com/fwlink/?linkid=2153388)

[<span data-ttu-id="2e1ce-175">Как собрать расширение в налоговой службе</span><span class="sxs-lookup"><span data-stu-id="2e1ce-175">How to build extension in tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138483)
