---
title: Расчет налогов (предварительная версия)
description: В этом разделе объясняется общий объем и функции Расчета налогов.
author: wangchen
ms.date: 04/12/2021
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
ms.openlocfilehash: 3df952e0632807e55f176e63dc2047be5e622ec2
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892357"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="07f74-103">Расчет налогов (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="07f74-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="07f74-104">Расчет налогов представляет собой гипермасштабируемую многоклиентскую службу, которая позволяет модулю Global Tax Engine автоматизировать и упростить процесс определения и расчета налогов.</span><span class="sxs-lookup"><span data-stu-id="07f74-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="07f74-105">Модуль налогов полностью настраиваемый.</span><span class="sxs-lookup"><span data-stu-id="07f74-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="07f74-106">Элементы, которые могут быть настроены, включают в себя (но не ограничиваются этим) модель налогооблагаемых данных, налоговый код, матрицу налоговой применимости и формулу расчета налога.</span><span class="sxs-lookup"><span data-stu-id="07f74-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="07f74-107">Модуль обработки налогов выполняется на платформе Microsoft Azure Core Services и предлагает современные технологии и экспоненциальную масштабируемость.</span><span class="sxs-lookup"><span data-stu-id="07f74-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="07f74-108">Расчет налогов интегрируется с Dynamics 365 Finance и Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="07f74-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="07f74-109">В конечном итоге она также интегрируется с Dynamics 365 Project Operations, Dynamics 365 Commerce и другими собственными приложениями и приложениями сторонних разработчиков.</span><span class="sxs-lookup"><span data-stu-id="07f74-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="07f74-110">Расчет налогов — это налоговый модуль на основе микрослужбы, который предлагает экспоненциальную масштабируемость.</span><span class="sxs-lookup"><span data-stu-id="07f74-110">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="07f74-111">Он может помочь выполнить следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="07f74-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="07f74-112">Настройка Расчета налогов с помощью службы Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="07f74-112">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="07f74-113">RCS — это расширенная версия конструктора электронной отчетности (ER), которая доступна в качестве автономной службы.</span><span class="sxs-lookup"><span data-stu-id="07f74-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="07f74-114">Настройка налоговой матрицы, чтобы автоматически определять налоговые коды и ставки.</span><span class="sxs-lookup"><span data-stu-id="07f74-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="07f74-115">Настройка налоговой матрицы, чтобы автоматически определять номер налоговой регистрации.</span><span class="sxs-lookup"><span data-stu-id="07f74-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="07f74-116">Настройка конструктора расчета налогов для определения формул и условий.</span><span class="sxs-lookup"><span data-stu-id="07f74-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="07f74-117">Совместное использование решения определения и расчета налогов для нескольких юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="07f74-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="07f74-118">Чтобы использовать службу расчета налога, установите надстройку службы расчета налогов из проекта в Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="07f74-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="07f74-119">Затем выполните настройку в RCS и включите службу расчета налогов в Finance и Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="07f74-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="07f74-120">Дополнительные сведения см. в разделе [Начало работы с налоговой службой](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="07f74-120">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="07f74-121">Доступность</span><span class="sxs-lookup"><span data-stu-id="07f74-121">Availability</span></span>

<span data-ttu-id="07f74-122">Расчет налогов доступен только в средах песочницы и для избранных клиентов через программу общедоступной предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="07f74-122">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="07f74-123">В конечном итоге она станет общедоступной для всех клиентов и производственных сред.</span><span class="sxs-lookup"><span data-stu-id="07f74-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="07f74-124">Новые функции будут по-прежнему предоставляться, поэтому обязательно регулярно проверяйте самую актуальную документацию, чтобы узнать о покрытии и области поддерживаемых функций.</span><span class="sxs-lookup"><span data-stu-id="07f74-124">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="07f74-125">Расчет налогов развернут в следующих географических регионах Azure.</span><span class="sxs-lookup"><span data-stu-id="07f74-125">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="07f74-126">Она также будет развернута в большем числе географических регионов Azure на основе потребностей клиентов:</span><span class="sxs-lookup"><span data-stu-id="07f74-126">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="07f74-127">США</span><span class="sxs-lookup"><span data-stu-id="07f74-127">United States</span></span>
- <span data-ttu-id="07f74-128">Европа</span><span class="sxs-lookup"><span data-stu-id="07f74-128">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="07f74-129">Расчет налогов не поддерживает локальные развертывания Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="07f74-129">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="07f74-130">Она также не поддерживает предыдущие версии, такие как Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="07f74-130">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="07f74-131">Основные функции</span><span class="sxs-lookup"><span data-stu-id="07f74-131">Feature highlights</span></span>

- <span data-ttu-id="07f74-132">Настраиваемая налоговая матрица, чтобы автоматически определять и рассчитывать налог</span><span class="sxs-lookup"><span data-stu-id="07f74-132">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="07f74-133">Поддержка нескольких налоговых регистрационных номеров</span><span class="sxs-lookup"><span data-stu-id="07f74-133">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="07f74-134">Поддержка заказов на перемещение для определения и расчета налога</span><span class="sxs-lookup"><span data-stu-id="07f74-134">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="07f74-135">Поддержка заказов на перемещение для определения нескольких налоговых регистрационных номеров</span><span class="sxs-lookup"><span data-stu-id="07f74-135">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="07f74-136">Поддерживаемые проводки</span><span class="sxs-lookup"><span data-stu-id="07f74-136">Supported transactions</span></span>

<span data-ttu-id="07f74-137">Расчет налога можно включить по юридическим лицам и проводкам.</span><span class="sxs-lookup"><span data-stu-id="07f74-137">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="07f74-138">Следующие проводки поддерживаются:</span><span class="sxs-lookup"><span data-stu-id="07f74-138">The following transactions are supported:</span></span>

- <span data-ttu-id="07f74-139">Процесс продаж</span><span class="sxs-lookup"><span data-stu-id="07f74-139">Sales process</span></span>

    - <span data-ttu-id="07f74-140">Предложение по продажам</span><span class="sxs-lookup"><span data-stu-id="07f74-140">Sales quotation</span></span>
    - <span data-ttu-id="07f74-141">Заказ на продажу</span><span class="sxs-lookup"><span data-stu-id="07f74-141">Sales order</span></span>
    - <span data-ttu-id="07f74-142">Подтверждение</span><span class="sxs-lookup"><span data-stu-id="07f74-142">Confirmation</span></span>
    - <span data-ttu-id="07f74-143">Сборочный лист</span><span class="sxs-lookup"><span data-stu-id="07f74-143">Picking list</span></span>
    - <span data-ttu-id="07f74-144">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="07f74-144">Packing slip</span></span>
    - <span data-ttu-id="07f74-145">Накладная заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="07f74-145">Sales invoice</span></span>
    - <span data-ttu-id="07f74-146">Кредит-нота</span><span class="sxs-lookup"><span data-stu-id="07f74-146">Credit note</span></span>
    - <span data-ttu-id="07f74-147">Заказ на возврат</span><span class="sxs-lookup"><span data-stu-id="07f74-147">Return order</span></span>
    - <span data-ttu-id="07f74-148">Накладные расходы по заголовку</span><span class="sxs-lookup"><span data-stu-id="07f74-148">Header miscellaneous charge</span></span>
    - <span data-ttu-id="07f74-149">Накладные расходы по строке</span><span class="sxs-lookup"><span data-stu-id="07f74-149">Line miscellaneous charge</span></span>

- <span data-ttu-id="07f74-150">Процесс покупки</span><span class="sxs-lookup"><span data-stu-id="07f74-150">Purchase process</span></span>

    - <span data-ttu-id="07f74-151">Заказ на покупку</span><span class="sxs-lookup"><span data-stu-id="07f74-151">Purchase order</span></span>
    - <span data-ttu-id="07f74-152">Подтверждение</span><span class="sxs-lookup"><span data-stu-id="07f74-152">Confirmation</span></span>
    - <span data-ttu-id="07f74-153">Список прихода</span><span class="sxs-lookup"><span data-stu-id="07f74-153">Receipts list</span></span>
    - <span data-ttu-id="07f74-154">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="07f74-154">Product receipt</span></span>
    - <span data-ttu-id="07f74-155">Накладная по покупке </span><span class="sxs-lookup"><span data-stu-id="07f74-155">Purchase invoice</span></span>
    - <span data-ttu-id="07f74-156">Накладные расходы по заголовку</span><span class="sxs-lookup"><span data-stu-id="07f74-156">Header miscellaneous charge</span></span>
    - <span data-ttu-id="07f74-157">Накладные расходы по строке</span><span class="sxs-lookup"><span data-stu-id="07f74-157">Line miscellaneous charge</span></span>
    - <span data-ttu-id="07f74-158">Кредит-нота</span><span class="sxs-lookup"><span data-stu-id="07f74-158">Credit note</span></span>
    - <span data-ttu-id="07f74-159">Заказ на возврат</span><span class="sxs-lookup"><span data-stu-id="07f74-159">Return order</span></span>
    - <span data-ttu-id="07f74-160">Заявка на закупку</span><span class="sxs-lookup"><span data-stu-id="07f74-160">Purchase requisition</span></span>
    - <span data-ttu-id="07f74-161">Накладные расходы строки заявки на покупку</span><span class="sxs-lookup"><span data-stu-id="07f74-161">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="07f74-162">Запрос предложения</span><span class="sxs-lookup"><span data-stu-id="07f74-162">Request for quotation</span></span>
    - <span data-ttu-id="07f74-163">Накладные расходы заголовка запроса предложения</span><span class="sxs-lookup"><span data-stu-id="07f74-163">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="07f74-164">Накладные расходы строки запроса предложения</span><span class="sxs-lookup"><span data-stu-id="07f74-164">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="07f74-165">Процесс запасов</span><span class="sxs-lookup"><span data-stu-id="07f74-165">Inventory process</span></span>

    - <span data-ttu-id="07f74-166">Заказ на перемещение — отгрузка</span><span class="sxs-lookup"><span data-stu-id="07f74-166">Transfer order – ship</span></span>
    - <span data-ttu-id="07f74-167">Заказ на перемещение — получение</span><span class="sxs-lookup"><span data-stu-id="07f74-167">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="07f74-168">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="07f74-168">Related resources</span></span>

[<span data-ttu-id="07f74-169">Начало работы с налоговой службой</span><span class="sxs-lookup"><span data-stu-id="07f74-169">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="07f74-170">Множественный регистрационный номер НДС</span><span class="sxs-lookup"><span data-stu-id="07f74-170">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="07f74-171">Поддержка функций налогов для заказа на перемещение</span><span class="sxs-lookup"><span data-stu-id="07f74-171">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="07f74-172">Как собрать расширение в налоговой службе</span><span class="sxs-lookup"><span data-stu-id="07f74-172">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)