---
title: Расчет налогов (предварительная версия)
description: В этом разделе объясняется общий объем и функции Расчета налогов.
author: wangchen
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9daa6e001200d03a2639974fb6de618d77ddf09d
ms.sourcegitcommit: cb282e8d2306ab71adf80a84346a6863d2d019e8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184109"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="078de-103">Расчет налогов (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="078de-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="078de-104">Расчет налогов представляет собой гипермасштабируемую многоклиентскую службу, которая позволяет модулю Global Tax Engine автоматизировать и упростить процесс определения и расчета налогов.</span><span class="sxs-lookup"><span data-stu-id="078de-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="078de-105">Модуль налогов полностью настраиваемый.</span><span class="sxs-lookup"><span data-stu-id="078de-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="078de-106">Элементы, которые могут быть настроены, включают в себя (но не ограничиваются этим) модель налогооблагаемых данных, налоговый код, матрицу налоговой применимости и формулу расчета налога.</span><span class="sxs-lookup"><span data-stu-id="078de-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="078de-107">Модуль обработки налогов выполняется на платформе Microsoft Azure Core Services и предлагает современные технологии и экспоненциальную масштабируемость.</span><span class="sxs-lookup"><span data-stu-id="078de-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="078de-108">Расчет налогов интегрируется с Dynamics 365 Finance и Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="078de-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="078de-109">В конечном итоге она также интегрируется с Dynamics 365 Project Operations, Dynamics 365 Commerce и другими собственными приложениями и приложениями сторонних разработчиков.</span><span class="sxs-lookup"><span data-stu-id="078de-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="078de-110">При включении службы расчета налогов можно выполнить некоторые операции с соответствующими данными в центрах обработки данных, отличном от центра обработки данных, в котором хранятся данные службы.</span><span class="sxs-lookup"><span data-stu-id="078de-110">When you enable the Tax Calculation service, some operations on related data might be performed in a data center other than the data center that maintains your service data.</span></span> <span data-ttu-id="078de-111">Перед включением службы расчета налогов просмотрите [условия](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span><span class="sxs-lookup"><span data-stu-id="078de-111">Review the [Terms and Conditions](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) before you enable the Tax Calculation service.</span></span> <span data-ttu-id="078de-112">Мы заботимся о конфиденциальности ваших данных.</span><span class="sxs-lookup"><span data-stu-id="078de-112">Your privacy is important to us.</span></span> <span data-ttu-id="078de-113">Чтобы получить дополнительные сведения, ознакомьтесь с нашим [заявлением о конфиденциальности](https://go.microsoft.com/fwlink/?LinkId=521839).</span><span class="sxs-lookup"><span data-stu-id="078de-113">To learn more, read our [Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839).</span></span>

<span data-ttu-id="078de-114">Расчет налогов — это налоговый модуль на основе микрослужбы, который предлагает экспоненциальную масштабируемость.</span><span class="sxs-lookup"><span data-stu-id="078de-114">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="078de-115">Он может помочь выполнить следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="078de-115">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="078de-116">Настройка Расчета налогов с помощью службы Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="078de-116">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="078de-117">RCS — это расширенная версия конструктора электронной отчетности (ER), которая доступна в качестве автономной службы.</span><span class="sxs-lookup"><span data-stu-id="078de-117">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="078de-118">Настройка налоговой матрицы, чтобы автоматически определять налоговые коды и ставки.</span><span class="sxs-lookup"><span data-stu-id="078de-118">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="078de-119">Настройка налоговой матрицы, чтобы автоматически определять номер налоговой регистрации.</span><span class="sxs-lookup"><span data-stu-id="078de-119">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="078de-120">Настройка конструктора расчета налогов для определения формул и условий.</span><span class="sxs-lookup"><span data-stu-id="078de-120">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="078de-121">Совместное использование решения определения и расчета налогов для нескольких юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="078de-121">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="078de-122">Чтобы использовать службу расчета налога, установите надстройку службы расчета налогов из проекта в Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="078de-122">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="078de-123">Затем выполните настройку в RCS и включите службу расчета налогов в Finance и Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="078de-123">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="078de-124">Дополнительные сведения см. в разделе [Начало работы с налоговой службой](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="078de-124">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="078de-125">Доступность</span><span class="sxs-lookup"><span data-stu-id="078de-125">Availability</span></span>

<span data-ttu-id="078de-126">Расчет налогов доступен только в средах песочницы и для избранных клиентов через программу общедоступной предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="078de-126">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="078de-127">В конечном итоге она станет общедоступной для всех клиентов и производственных сред.</span><span class="sxs-lookup"><span data-stu-id="078de-127">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="078de-128">Новые функции будут по-прежнему предоставляться, поэтому обязательно регулярно проверяйте самую актуальную документацию, чтобы узнать о покрытии и области поддерживаемых функций.</span><span class="sxs-lookup"><span data-stu-id="078de-128">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="078de-129">Расчет налогов развернут в следующих географических регионах Azure.</span><span class="sxs-lookup"><span data-stu-id="078de-129">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="078de-130">Она также будет развернута в большем числе географических регионов Azure на основе потребностей клиентов:</span><span class="sxs-lookup"><span data-stu-id="078de-130">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="078de-131">США</span><span class="sxs-lookup"><span data-stu-id="078de-131">United States</span></span>
- <span data-ttu-id="078de-132">Европа</span><span class="sxs-lookup"><span data-stu-id="078de-132">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="078de-133">Расчет налогов не поддерживает локальные развертывания Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="078de-133">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="078de-134">Она также не поддерживает предыдущие версии, такие как Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="078de-134">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="078de-135">Основные функции</span><span class="sxs-lookup"><span data-stu-id="078de-135">Feature highlights</span></span>

- <span data-ttu-id="078de-136">Настраиваемая налоговая матрица, чтобы автоматически определять и рассчитывать налог</span><span class="sxs-lookup"><span data-stu-id="078de-136">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="078de-137">Поддержка нескольких налоговых регистрационных номеров</span><span class="sxs-lookup"><span data-stu-id="078de-137">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="078de-138">Поддержка заказов на перемещение для определения и расчета налога</span><span class="sxs-lookup"><span data-stu-id="078de-138">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="078de-139">Поддержка заказов на перемещение для определения нескольких налоговых регистрационных номеров</span><span class="sxs-lookup"><span data-stu-id="078de-139">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="078de-140">Поддерживаемые проводки</span><span class="sxs-lookup"><span data-stu-id="078de-140">Supported transactions</span></span>

<span data-ttu-id="078de-141">Расчет налога можно включить по юридическим лицам и проводкам.</span><span class="sxs-lookup"><span data-stu-id="078de-141">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="078de-142">Следующие проводки поддерживаются:</span><span class="sxs-lookup"><span data-stu-id="078de-142">The following transactions are supported:</span></span>

- <span data-ttu-id="078de-143">Процесс продаж</span><span class="sxs-lookup"><span data-stu-id="078de-143">Sales process</span></span>

    - <span data-ttu-id="078de-144">Предложение по продажам</span><span class="sxs-lookup"><span data-stu-id="078de-144">Sales quotation</span></span>
    - <span data-ttu-id="078de-145">Заказ на продажу</span><span class="sxs-lookup"><span data-stu-id="078de-145">Sales order</span></span>
    - <span data-ttu-id="078de-146">Подтверждение</span><span class="sxs-lookup"><span data-stu-id="078de-146">Confirmation</span></span>
    - <span data-ttu-id="078de-147">Сборочный лист</span><span class="sxs-lookup"><span data-stu-id="078de-147">Picking list</span></span>
    - <span data-ttu-id="078de-148">Отборочная накладная</span><span class="sxs-lookup"><span data-stu-id="078de-148">Packing slip</span></span>
    - <span data-ttu-id="078de-149">Накладная заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="078de-149">Sales invoice</span></span>
    - <span data-ttu-id="078de-150">Кредит-нота</span><span class="sxs-lookup"><span data-stu-id="078de-150">Credit note</span></span>
    - <span data-ttu-id="078de-151">Заказ на возврат</span><span class="sxs-lookup"><span data-stu-id="078de-151">Return order</span></span>
    - <span data-ttu-id="078de-152">Накладные расходы по заголовку</span><span class="sxs-lookup"><span data-stu-id="078de-152">Header miscellaneous charge</span></span>
    - <span data-ttu-id="078de-153">Накладные расходы по строке</span><span class="sxs-lookup"><span data-stu-id="078de-153">Line miscellaneous charge</span></span>

- <span data-ttu-id="078de-154">Процесс покупки</span><span class="sxs-lookup"><span data-stu-id="078de-154">Purchase process</span></span>

    - <span data-ttu-id="078de-155">Заказ на покупку</span><span class="sxs-lookup"><span data-stu-id="078de-155">Purchase order</span></span>
    - <span data-ttu-id="078de-156">Подтверждение</span><span class="sxs-lookup"><span data-stu-id="078de-156">Confirmation</span></span>
    - <span data-ttu-id="078de-157">Список прихода</span><span class="sxs-lookup"><span data-stu-id="078de-157">Receipts list</span></span>
    - <span data-ttu-id="078de-158">Поступление продуктов</span><span class="sxs-lookup"><span data-stu-id="078de-158">Product receipt</span></span>
    - <span data-ttu-id="078de-159">Накладная по покупке </span><span class="sxs-lookup"><span data-stu-id="078de-159">Purchase invoice</span></span>
    - <span data-ttu-id="078de-160">Накладные расходы по заголовку</span><span class="sxs-lookup"><span data-stu-id="078de-160">Header miscellaneous charge</span></span>
    - <span data-ttu-id="078de-161">Накладные расходы по строке</span><span class="sxs-lookup"><span data-stu-id="078de-161">Line miscellaneous charge</span></span>
    - <span data-ttu-id="078de-162">Кредит-нота</span><span class="sxs-lookup"><span data-stu-id="078de-162">Credit note</span></span>
    - <span data-ttu-id="078de-163">Заказ на возврат</span><span class="sxs-lookup"><span data-stu-id="078de-163">Return order</span></span>
    - <span data-ttu-id="078de-164">Заявка на закупку</span><span class="sxs-lookup"><span data-stu-id="078de-164">Purchase requisition</span></span>
    - <span data-ttu-id="078de-165">Накладные расходы строки заявки на покупку</span><span class="sxs-lookup"><span data-stu-id="078de-165">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="078de-166">Запрос предложения</span><span class="sxs-lookup"><span data-stu-id="078de-166">Request for quotation</span></span>
    - <span data-ttu-id="078de-167">Накладные расходы заголовка запроса предложения</span><span class="sxs-lookup"><span data-stu-id="078de-167">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="078de-168">Накладные расходы строки запроса предложения</span><span class="sxs-lookup"><span data-stu-id="078de-168">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="078de-169">Процесс запасов</span><span class="sxs-lookup"><span data-stu-id="078de-169">Inventory process</span></span>

    - <span data-ttu-id="078de-170">Заказ на перемещение — отгрузка</span><span class="sxs-lookup"><span data-stu-id="078de-170">Transfer order – ship</span></span>
    - <span data-ttu-id="078de-171">Заказ на перемещение — получение</span><span class="sxs-lookup"><span data-stu-id="078de-171">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="078de-172">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="078de-172">Related resources</span></span>

[<span data-ttu-id="078de-173">Начало работы с налоговой службой</span><span class="sxs-lookup"><span data-stu-id="078de-173">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="078de-174">Множественный регистрационный номер НДС</span><span class="sxs-lookup"><span data-stu-id="078de-174">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="078de-175">Поддержка функций налогов для заказа на перемещение</span><span class="sxs-lookup"><span data-stu-id="078de-175">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="078de-176">Как собрать расширение в налоговой службе</span><span class="sxs-lookup"><span data-stu-id="078de-176">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)
