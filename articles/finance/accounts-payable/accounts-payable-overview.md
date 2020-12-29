---
title: Обзор настройки модуля "Расчеты с поставщиками"
description: Эта статья описывает страницы, используемые для настройки основной и дополнительных функций для расчетов с поставщиками. Она также описывают шаги настройки, которые необходимо выполнить до начала настройки расчетов с поставщиками.
author: abruer
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eed11cbe73ede71cabf83655fc1d37b1a979a4c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447288"
---
# <a name="configure-accounts-payable-overview"></a><span data-ttu-id="ffc10-104">Обзор настройки модуля "Расчеты с поставщиками"</span><span class="sxs-lookup"><span data-stu-id="ffc10-104">Configure Accounts payable overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffc10-105">Эта статья описывает страницы, используемые для настройки основной и дополнительных функций для расчетов с поставщиками.</span><span class="sxs-lookup"><span data-stu-id="ffc10-105">This article describes the pages that you use to set up basic and optional functionality for Accounts payable.</span></span> <span data-ttu-id="ffc10-106">Она также описывают шаги настройки, которые необходимо выполнить до начала настройки расчетов с поставщиками.</span><span class="sxs-lookup"><span data-stu-id="ffc10-106">It also describes setup steps that you must complete before you start to set up Accounts payable.</span></span>

<a name="prerequisites-for-accounts-payable-setup"></a><span data-ttu-id="ffc10-107">Необходимые условия для настройки модуля "Расчеты с поставщиками"</span><span class="sxs-lookup"><span data-stu-id="ffc10-107">Prerequisites for Accounts payable setup</span></span>
----------------------------------------

<span data-ttu-id="ffc10-108">Перед настройкой модуля "Расчеты с поставщиками" необходимо настроить следующее:</span><span class="sxs-lookup"><span data-stu-id="ffc10-108">Before you can set up Accounts payable, you must complete the following setup:</span></span>

-   <span data-ttu-id="ffc10-109">В главной книге:</span><span class="sxs-lookup"><span data-stu-id="ffc10-109">In General ledger:</span></span>
    -   <span data-ttu-id="ffc10-110">Если планируется использовать журналы платежей, следует настроить журналы платежей.</span><span class="sxs-lookup"><span data-stu-id="ffc10-110">If you plan to use payment journals, set up payment journals.</span></span>
    -   <span data-ttu-id="ffc10-111">Если планируется использовать курсовые разницы, настройте коды валюты на странице "Валюты", типы валютного курса на странице "Типы валютного курса" и валютные курсы на странице "Валютные курсы".</span><span class="sxs-lookup"><span data-stu-id="ffc10-111">If you plan to run exchange rate adjustments, set up currency codes on the Currencies page, set up exchange rate types on the Exchange rate types page, and set up currency exchange rates on the Currency exchange rates page.</span></span>
-   <span data-ttu-id="ffc10-112">В разделе "Управление банком и кассовыми операциями" настройте банковские счета для использования со способами оплаты.</span><span class="sxs-lookup"><span data-stu-id="ffc10-112">In Cash and bank management, set up bank accounts to use with methods of payment.</span></span>

## <a name="setup-pages-for-accounts-payable"></a><span data-ttu-id="ffc10-113">Страницы настройки для модуля "Расчеты с поставщиками"</span><span class="sxs-lookup"><span data-stu-id="ffc10-113">Setup pages for Accounts payable</span></span>

<span data-ttu-id="ffc10-114">Следующие страницы позволяют настроить основные функции модуля "Расчеты с поставщиками" для каждого юридического лица.</span><span class="sxs-lookup"><span data-stu-id="ffc10-114">Use the following pages to set up the basic functionality of Accounts payable for each legal entity.</span></span> <span data-ttu-id="ffc10-115">Эти страницы перечислены в рекомендуемом порядке настройки.</span><span class="sxs-lookup"><span data-stu-id="ffc10-115">The pages are listed in the recommended order of setup.</span></span> <span data-ttu-id="ffc10-116">Чтобы упростить процесс настройки, имеется возможность создать шаблоны по первым созданным записям.</span><span class="sxs-lookup"><span data-stu-id="ffc10-116">To make the setup process easier, you can create templates from the first records that you create.</span></span> <span data-ttu-id="ffc10-117">В шаблоне значения обычно вводятся во множество полей, отражающих возможности, необходимые организации для определенного типа поставщика.</span><span class="sxs-lookup"><span data-stu-id="ffc10-117">In a template, values are typically entered in many fields to reflect the features that the organization wants to implement for a particular type of vendor.</span></span>
1.  <span data-ttu-id="ffc10-118">На странице "Условия оплаты" определите условия оплаты, назначенные для заказов на продажу, заказов на покупку, клиентов и поставщиков; эти условия определяют срок выполнения этой накладной.</span><span class="sxs-lookup"><span data-stu-id="ffc10-118">On the Terms of payment page, define the terms of payment that you assign to sales orders, purchase orders, customers, and vendors, and that determine invoice due dates.</span></span> <span data-ttu-id="ffc10-119">Дополнительные сведения см. в разделе [Определение сборов по платежам поставщикам](tasks/define-vendor-payment-fees.md).</span><span class="sxs-lookup"><span data-stu-id="ffc10-119">For more information, see [Define vendor payment fees](tasks/define-vendor-payment-fees.md).</span></span>
2.  <span data-ttu-id="ffc10-120">На странице "Способы оплаты - поставщики" создайте и ведите сведения о том, как организация осуществляет оплату поставщикам.</span><span class="sxs-lookup"><span data-stu-id="ffc10-120">On the Methods of payment - vendors page, create and maintain information about how the organization pays its vendors.</span></span>
3.  <span data-ttu-id="ffc10-121">На странице "Группы поставщиков" создайте и ведите группы поставщиков, которым присваиваются общие важные параметры для разноски, сопоставления и платежа, отчета и прогнозирования.</span><span class="sxs-lookup"><span data-stu-id="ffc10-121">On the Vendor groups page, create and maintain groups of vendors that share important parameters for posting, settlement and payment, reporting, and forecasting.</span></span>
4.  <span data-ttu-id="ffc10-122">На странице "Профили разноски по поставщикам" определите способ разноски проводок по поставщику в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="ffc10-122">On the Vendor posting profiles page, define how vendor transactions are posted to the general ledger.</span></span>
5.  <span data-ttu-id="ffc10-123">На странице "Параметры расчетов с поставщиками" настройте параметры по умолчанию, применяемые, если не указаны другие особые настройки, параметры для разного рода функций и различные номерные серии для модуля "Расчеты с поставщиками".</span><span class="sxs-lookup"><span data-stu-id="ffc10-123">On the Accounts payable parameters page, set up default settings that are applied if a more specific setting isn't specified, parameters for various kinds of functionality, and the various number sequences for Accounts payable.</span></span>
6.  <span data-ttu-id="ffc10-124">На странице "Настройка форм" определите формат различных документов, относящихся к поставщикам и применяемых в организации, чтобы отслеживать приходы от поставщиков и вводить причины движения платежей к поставщикам.</span><span class="sxs-lookup"><span data-stu-id="ffc10-124">On the Form setup page, define the format of various documents that are related to vendors, and that the organization uses to keep track of receipts from vendors and enter reasons for the flow of payments to vendors.</span></span>
7.  <span data-ttu-id="ffc10-125">На странице "Поставщики" создайте и ведите счета поставщиков, в том числе налоговых органов, перед которыми организация отчитывается по налогам.</span><span class="sxs-lookup"><span data-stu-id="ffc10-125">On the Vendors page, create and maintain vendor accounts, and also the tax authorities that your organization reports sales taxes to.</span></span>

## <a name="optional-setup-pages-for-accounts-payable"></a><span data-ttu-id="ffc10-126">Дополнительные страницы настройки модуля "Расчеты с поставщиками"</span><span class="sxs-lookup"><span data-stu-id="ffc10-126">Optional setup pages for Accounts payable</span></span>
<span data-ttu-id="ffc10-127">В дополнение к основным функциональным возможностям модуль "Расчеты с поставщиками" предлагает другие функции, которые можно настроить.</span><span class="sxs-lookup"><span data-stu-id="ffc10-127">In addition to the basic functionality, Accounts payable has other functionality that you can set up.</span></span>

<span data-ttu-id="ffc10-128">Дополнительные страницы настройки упорядочены по функциональности.</span><span class="sxs-lookup"><span data-stu-id="ffc10-128">The additional setup pages are organized by functionality.</span></span>

<span data-ttu-id="ffc10-129">**Политики**</span><span class="sxs-lookup"><span data-stu-id="ffc10-129">**Policies**</span></span>
-   <span data-ttu-id="ffc10-130">На странице "Политика накладных поставщиков" настройте политики накладных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="ffc10-130">On the Vendor invoice policy page, set up vendor invoice policies.</span></span>

<span data-ttu-id="ffc10-131">**Трехстороннее сопоставление накладных в модуле расчетов с поставщиками**</span><span class="sxs-lookup"><span data-stu-id="ffc10-131">**Invoice matching**</span></span>

-   <span data-ttu-id="ffc10-132">На странице "Допустимые отклонения по итогам накладных" настройте допуски для итогов по накладной.</span><span class="sxs-lookup"><span data-stu-id="ffc10-132">On the Invoice totals tolerances page, set up tolerances for invoice totals.</span></span>
-   <span data-ttu-id="ffc10-133">На странице "Политика проверки соответствия" настройте политики двухстороннего и трехстороннего сопоставления.</span><span class="sxs-lookup"><span data-stu-id="ffc10-133">On the Matching policy page, set up two-way and three-way matching policies.</span></span>
-   <span data-ttu-id="ffc10-134">На странице "Допустимые отклонения по цене" настройте допуски для цены за единицу.</span><span class="sxs-lookup"><span data-stu-id="ffc10-134">On the Price tolerances page, set up tolerances for unit prices.</span></span>
-   <span data-ttu-id="ffc10-135">На странице "Группы допустимых отклонений по цене номенклатуры" настройте группы допустимых отклонений по цене номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="ffc10-135">On the Item price tolerance groups page, set up tolerance groups for item prices.</span></span>
-   <span data-ttu-id="ffc10-136">На странице "Группы допустимых отклонений по цене поставщика" настройте группы допустимых отклонений по цене поставщика.</span><span class="sxs-lookup"><span data-stu-id="ffc10-136">On the Vendor price tolerance groups page, set up  tolerance groups for vendor prices.</span></span>
-   <span data-ttu-id="ffc10-137">На странице "Допустимые отклонения по накладным расходам" настройте допуски для накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="ffc10-137">On the Charges tolerances page, set up tolerances for charges.</span></span>

<span data-ttu-id="ffc10-138">**Документооборот**</span><span class="sxs-lookup"><span data-stu-id="ffc10-138">**Workflow**</span></span>

-   <span data-ttu-id="ffc10-139">На странице "Workflow-процессы для расчетов с поставщиками" настройте конфигурации workflow-процессов для утверждений журнала и заявок на покупку.</span><span class="sxs-lookup"><span data-stu-id="ffc10-139">On the Accounts payable workflows page, set up workflow configurations for journal approvals and purchase requisitions.</span></span>

<span data-ttu-id="ffc10-140">**Причины**</span><span class="sxs-lookup"><span data-stu-id="ffc10-140">**Reasons**</span></span>

-   <span data-ttu-id="ffc10-141">На странице "Основания для проводок по поставщикам" настройте коды причин.</span><span class="sxs-lookup"><span data-stu-id="ffc10-141">On the Vendor reasons page, set up reason codes.</span></span>

<span data-ttu-id="ffc10-142">**Расходы**</span><span class="sxs-lookup"><span data-stu-id="ffc10-142">**Charges**</span></span>

-   <span data-ttu-id="ffc10-143">На странице "Код накладных расходов" настройте коды накладных расходов, используемых в заказах на покупку.</span><span class="sxs-lookup"><span data-stu-id="ffc10-143">On the Charges code page, set up codes for the charges that are used in purchase orders.</span></span>
-   <span data-ttu-id="ffc10-144">На странице "Группа накладных расходов по поставщикам" создайте и ведите группы накладных расходов для поставщиков.</span><span class="sxs-lookup"><span data-stu-id="ffc10-144">On the Vendor charges group page, create and maintain charges groups for vendors.</span></span>
-   <span data-ttu-id="ffc10-145">На странице "Группы накладных расходов по номенклатурам" создайте и ведите группы накладных расходов по номенклатурам.</span><span class="sxs-lookup"><span data-stu-id="ffc10-145">On the Item charge groups page, create and maintain charges groups for items.</span></span>
-   <span data-ttu-id="ffc10-146">На странице "Автоматические затраты" определите накладные расходы, которые автоматически назначаются заказам.</span><span class="sxs-lookup"><span data-stu-id="ffc10-146">On the Auto charges page, define the charges that are automatically assigned to orders.</span></span>

<span data-ttu-id="ffc10-147">**Дополнительные номенклатуры**</span><span class="sxs-lookup"><span data-stu-id="ffc10-147">**Supplementary items**</span></span>

-   <span data-ttu-id="ffc10-148">На странице "Группы дополнительных номенклатур - Поставщик создайте и ведите группы дополнительных номенклатур для поставщиков.</span><span class="sxs-lookup"><span data-stu-id="ffc10-148">On the Supplementary item groups - Vendor page, create and maintain supplementary item groups for vendors.</span></span>
-   <span data-ttu-id="ffc10-149">На странице "Группы дополнительных номенклатур - Запасы создайте и ведите группы дополнительных номенклатур для номенклатур.</span><span class="sxs-lookup"><span data-stu-id="ffc10-149">On the Supplementary item groups - Inventory page, create and maintain supplementary item groups for items.</span></span>

<span data-ttu-id="ffc10-150">**Распределение**</span><span class="sxs-lookup"><span data-stu-id="ffc10-150">**Distribution**</span></span>

-   <span data-ttu-id="ffc10-151">На странице "Условия поставки" создайте и ведите условия для перемещения номенклатур от продавца к покупателю.</span><span class="sxs-lookup"><span data-stu-id="ffc10-151">On the Terms of delivery page, create and maintain the conditions for an item's transfer from seller to buyer.</span></span>
-   <span data-ttu-id="ffc10-152">На странице "Способы поставки" создайте и ведите способы транспортировки, применяемые при поставке заказа от продавца к покупателю.</span><span class="sxs-lookup"><span data-stu-id="ffc10-152">On the Modes of delivery page, create and maintain the methods of transport that are used when an order is delivered from the seller to the buyer.</span></span>
-   <span data-ttu-id="ffc10-153">На странице "Коды назначения" создайте и ведите коды и описания для пунктов назначения поставок.</span><span class="sxs-lookup"><span data-stu-id="ffc10-153">On the Destination codes page, create and maintain identifiers and descriptions for delivery destinations.</span></span>

<span data-ttu-id="ffc10-154">**Формы**</span><span class="sxs-lookup"><span data-stu-id="ffc10-154">**Forms**</span></span>

-   <span data-ttu-id="ffc10-155">На странице "Примечание к форме" создайте стандартный текст, который будет отображаться на различных страницах.</span><span class="sxs-lookup"><span data-stu-id="ffc10-155">On the Form notes page, create the standard text that appears on various pages.</span></span>
-   <span data-ttu-id="ffc10-156">На странице "Параметры сортировки формы" настройте порядок сортировки для заявок, списков поступлений, отборочных накладных и накладных.</span><span class="sxs-lookup"><span data-stu-id="ffc10-156">On the Form sorting parameters page, set up the sorting order for requisitions, receipt lists, packing slips, and invoices.</span></span>
-   <span data-ttu-id="ffc10-157">На странице "Настройка управления печатью" настройте сведения по управлению печатью для оригиналов и копий страниц.</span><span class="sxs-lookup"><span data-stu-id="ffc10-157">On the Print management setup page, set up print management information for originals and copies of pages.</span></span>

<span data-ttu-id="ffc10-158">**Оплаты**</span><span class="sxs-lookup"><span data-stu-id="ffc10-158">**Payments**</span></span>

-   <span data-ttu-id="ffc10-159">На странице "Скидки по оплате" создайте и ведите условия получения скидок по оплате.</span><span class="sxs-lookup"><span data-stu-id="ffc10-159">On the Cash discounts page, set up and manage the terms for obtaining cash discounts.</span></span> <span data-ttu-id="ffc10-160">Коды скидок по оплате связаны с поставщиками и применяются к заказам на покупку.</span><span class="sxs-lookup"><span data-stu-id="ffc10-160">The cash discount codes are linked to vendors and are applied to purchase orders.</span></span>
-   <span data-ttu-id="ffc10-161">На странице "Графики оплаты" настройте графики оплаты, используемые для управления платежами по взносам поставщикам.</span><span class="sxs-lookup"><span data-stu-id="ffc10-161">On the Payment schedules page, set up the payment schedules that are used to manage installment payments to vendors.</span></span>
-   <span data-ttu-id="ffc10-162">На странице "Дни платежа" определите дни платежа, которые применяются для расчета сроков, и укажите дни платежа для определенных дней недели или месяца.</span><span class="sxs-lookup"><span data-stu-id="ffc10-162">On the Payment days page, define the payment days that are used to calculate due dates, and specify payment days for a specific day of the week or month.</span></span>
-   <span data-ttu-id="ffc10-163">На странице "Сборы по платежам" создайте и ведите сборы по платежам, связанные с поставщиками.</span><span class="sxs-lookup"><span data-stu-id="ffc10-163">On the Payment fee page, create and maintain the payment fees that are associated with vendors.</span></span>
-   <span data-ttu-id="ffc10-164">На странице "Инструкция по оплате" создайте и ведите инструкции по оплате.</span><span class="sxs-lookup"><span data-stu-id="ffc10-164">On the Payment instruction page, create and maintain payment instructions.</span></span>

<span data-ttu-id="ffc10-165">**Статистика**</span><span class="sxs-lookup"><span data-stu-id="ffc10-165">**Statistics**</span></span>

-   <span data-ttu-id="ffc10-166">На странице "Определения периодов распределения по срокам" настройте интервалы, определенные пользователем, чтобы анализировать распределение задолженности счетов поставщика.</span><span class="sxs-lookup"><span data-stu-id="ffc10-166">On the Aging period definitions page, set up user-defined intervals that are used to analyze the maturity distribution of vendor accounts.</span></span>
-   <span data-ttu-id="ffc10-167">На странице "Отрасль" создайте коды отраслей, назначаемые поставщикам.</span><span class="sxs-lookup"><span data-stu-id="ffc10-167">On the Line of business page, create the line of business (LOB) codes that are assigned to vendors.</span></span>

<span data-ttu-id="ffc10-168">**Налог по форме 1099**</span><span class="sxs-lookup"><span data-stu-id="ffc10-168">**Tax 1099**</span></span>

-   <span data-ttu-id="ffc10-169">На странице **Поля формы 1099** проверьте и обновите минимальные суммы, о которых необходимо сообщать в Налоговое управление (IRS), на основании последних требований IRS.</span><span class="sxs-lookup"><span data-stu-id="ffc10-169">On the **1099 fields** page, verify and update the minimum amounts that must be reported to the Internal Revenue Service (IRS), based on the latest IRS requirements.</span></span>

## <a name="optional-setup-for-other-modules"></a><span data-ttu-id="ffc10-170">**Дополнительная настройка для других модулей**</span><span class="sxs-lookup"><span data-stu-id="ffc10-170">**Optional setup for other modules**</span></span>
<span data-ttu-id="ffc10-171">**Управление организацией**</span><span class="sxs-lookup"><span data-stu-id="ffc10-171">**Organization administration**</span></span>

-   <span data-ttu-id="ffc10-172">На странице "Номерные серии" настройте группы номерных серий для номеров накладной.</span><span class="sxs-lookup"><span data-stu-id="ffc10-172">On the Number sequences page, set up number sequence groups for invoice numbers.</span></span>
-   <span data-ttu-id="ffc10-173">На следующих страницах настройте данные об адресе:</span><span class="sxs-lookup"><span data-stu-id="ffc10-173">On the following pages, set up address information:</span></span>
    -   <span data-ttu-id="ffc10-174">Настройка адреса</span><span class="sxs-lookup"><span data-stu-id="ffc10-174">Address setup</span></span>
    -   <span data-ttu-id="ffc10-175">Коды NAF</span><span class="sxs-lookup"><span data-stu-id="ffc10-175">NAF codes</span></span>
    -   <span data-ttu-id="ffc10-176">Импорт почтовых индексов</span><span class="sxs-lookup"><span data-stu-id="ffc10-176">Import ZIP/postal codes</span></span>

<span data-ttu-id="ffc10-177">**Главная книга**</span><span class="sxs-lookup"><span data-stu-id="ffc10-177">**General ledger**</span></span>

-   <span data-ttu-id="ffc10-178">На странице "Финансовые аналитики" настройте финансовые аналитики.</span><span class="sxs-lookup"><span data-stu-id="ffc10-178">On the Financial dimensions page, set up financial dimensions.</span></span>
-   <span data-ttu-id="ffc10-179">На следующих страницах настройте сведения о налоге:</span><span class="sxs-lookup"><span data-stu-id="ffc10-179">On the following pages, set up tax information:</span></span>
    -   <span data-ttu-id="ffc10-180">Налоговые коды</span><span class="sxs-lookup"><span data-stu-id="ffc10-180">Sales tax codes</span></span>
    -   <span data-ttu-id="ffc10-181">Налоговые группы</span><span class="sxs-lookup"><span data-stu-id="ffc10-181">Sales tax groups</span></span>
    -   <span data-ttu-id="ffc10-182">Налоговые группы номенклатур</span><span class="sxs-lookup"><span data-stu-id="ffc10-182">Item sales tax groups</span></span>
    -   <span data-ttu-id="ffc10-183">Группа счетов</span><span class="sxs-lookup"><span data-stu-id="ffc10-183">Account group</span></span>
    -   <span data-ttu-id="ffc10-184">Коды налогового освобождения</span><span class="sxs-lookup"><span data-stu-id="ffc10-184">Sales tax exempt codes</span></span>
    -   <span data-ttu-id="ffc10-185">Налоговые инспекции</span><span class="sxs-lookup"><span data-stu-id="ffc10-185">Sales tax jurisdictions</span></span>
    -   <span data-ttu-id="ffc10-186">Налоговые органы</span><span class="sxs-lookup"><span data-stu-id="ffc10-186">Sales tax authorities</span></span>
    -   <span data-ttu-id="ffc10-187">Периоды сопоставления налогов</span><span class="sxs-lookup"><span data-stu-id="ffc10-187">Sales tax settlement periods</span></span>

<span data-ttu-id="ffc10-188">**Управление банком и кассовыми операциями**</span><span class="sxs-lookup"><span data-stu-id="ffc10-188">**Cash and bank management**</span></span>

-   <span data-ttu-id="ffc10-189">На странице "Коды назначений платежей" настройте код назначения центрального банка.</span><span class="sxs-lookup"><span data-stu-id="ffc10-189">On the Payment purpose codes page, set up the Central Bank purpose code.</span></span>





