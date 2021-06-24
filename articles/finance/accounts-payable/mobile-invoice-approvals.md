---
title: Утверждения накладных на мобильном устройстве
description: Этот раздел представляет практический подход к разработке мобильных сценариев, используя утверждения накладных поставщика для мобильных устройств как вариант использования.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 78ab17952801a1d77f321e212bb61e9b45d93216
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189210"
---
# <a name="mobile-invoice-approvals"></a><span data-ttu-id="40c4f-103">Утверждения накладных на мобильном устройстве</span><span class="sxs-lookup"><span data-stu-id="40c4f-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40c4f-104">Мобильные возможности позволяют бизнес-пользователю разрабатывать мобильное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="40c4f-104">Mobile capabilities let a business user design mobile experiences.</span></span> <span data-ttu-id="40c4f-105">Для более сложных сценариев платформа также позволяет разработчикам расширять возможности при необходимости.</span><span class="sxs-lookup"><span data-stu-id="40c4f-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="40c4f-106">Наиболее эффективный способ познакомиться с некоторыми новыми мобильными концепциями — пройти через процесс разработки нескольких сценариев.</span><span class="sxs-lookup"><span data-stu-id="40c4f-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="40c4f-107">Этот раздел представляет практический подход к разработке мобильных сценариев, используя утверждения накладных поставщика для мобильных устройств как вариант использования.</span><span class="sxs-lookup"><span data-stu-id="40c4f-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="40c4f-108">Этот раздел поможет разрабатывать другие варианты сценариев, а также может применяться к другим сценариям, которые не относятся к накладным поставщиков.</span><span class="sxs-lookup"><span data-stu-id="40c4f-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="40c4f-109">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="40c4f-109">Prerequisites</span></span>

| <span data-ttu-id="40c4f-110">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="40c4f-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="40c4f-111">описание</span><span class="sxs-lookup"><span data-stu-id="40c4f-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40c4f-112">Предварительно ознакомьтесь с руководством по мобильным приложениям</span><span class="sxs-lookup"><span data-stu-id="40c4f-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="40c4f-113">Мобильная платформа</span><span class="sxs-lookup"><span data-stu-id="40c4f-113">Mobile platform</span></span>](../../fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="40c4f-114">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="40c4f-114">Dynamics 365 Finance</span></span>                                                                              | <span data-ttu-id="40c4f-115">Среда с версией 1611 и обновлением платформы Platform update 3 (ноябрь 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="40c4f-115">An environment that has version 1611 and Platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="40c4f-116">Установите исправление KB 3204341.</span><span class="sxs-lookup"><span data-stu-id="40c4f-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="40c4f-117">Регистратор задач может ошибочно записывать две команды закрытия из раскрывающихся диалоговых окон, которые включены в обновление Platform update 3 (обновление за ноябрь 2016).</span><span class="sxs-lookup"><span data-stu-id="40c4f-117">Task recorder can erroneously record two Close commands for dropdown dialogs; this is included in Platform update 3 (November 2016 update).</span></span> |
| <span data-ttu-id="40c4f-118">Установите исправление KB 3207800.</span><span class="sxs-lookup"><span data-stu-id="40c4f-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="40c4f-119">Это исправление позволяет просматривать вложения на мобильном клиенте, который включен в обновление Platform update 3 (обновление за ноябрь 2016).</span><span class="sxs-lookup"><span data-stu-id="40c4f-119">This hotfix enables attachments to be viewed on the mobile client; this is included in Platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="40c4f-120">Установите исправление KB 3208224.</span><span class="sxs-lookup"><span data-stu-id="40c4f-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="40c4f-121">Код приложения для мобильного приложения утверждения накладных поставщика, которое входит в версию 7.0.1 (май 2016 г.).</span><span class="sxs-lookup"><span data-stu-id="40c4f-121">Application code for the mobile vendor invoice approval application; this is included in version 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="40c4f-122">Устройство Android, iOS или Windows, на которое установлено мобильное приложение.</span><span class="sxs-lookup"><span data-stu-id="40c4f-122">An Android or iOS or a Windows device that has the mobile app installed.</span></span> | <span data-ttu-id="40c4f-123">Найдите приложение в соответствующем магазине приложений.</span><span class="sxs-lookup"><span data-stu-id="40c4f-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="40c4f-124">Введение</span><span class="sxs-lookup"><span data-stu-id="40c4f-124">Introduction</span></span>
<span data-ttu-id="40c4f-125">Для мобильного утверждения накладных поставщика требуются три исправления, описанные в разделе "Необходимые условия".</span><span class="sxs-lookup"><span data-stu-id="40c4f-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="40c4f-126">Эти исправления не предоставляют рабочую область для утверждения накладных.</span><span class="sxs-lookup"><span data-stu-id="40c4f-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="40c4f-127">Чтобы узнать, что рабочая область находится в контексте мобильных устройств, ознакомьтесь с мобильным руководством, которое упомянуто в разделе "Необходимые условия".</span><span class="sxs-lookup"><span data-stu-id="40c4f-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="40c4f-128">Рабочая область утверждения накладных должна быть разработана.</span><span class="sxs-lookup"><span data-stu-id="40c4f-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="40c4f-129">Каждая организация организует и определяет свои бизнес-процессы для накладных поставщиков по-разному.</span><span class="sxs-lookup"><span data-stu-id="40c4f-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="40c4f-130">Прежде чем разрабатывать мобильные возможности для утверждения накладных поставщиков, следует рассмотреть следующие аспекты бизнес-процесса.</span><span class="sxs-lookup"><span data-stu-id="40c4f-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="40c4f-131">Смысл заключается в как можно более полном использовании этих данных для оптимизации работы пользователей на устройстве.</span><span class="sxs-lookup"><span data-stu-id="40c4f-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="40c4f-132">Какие поля из заголовка накладной пользователь захочет видеть на мобильных устройствах и в каком порядке?</span><span class="sxs-lookup"><span data-stu-id="40c4f-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="40c4f-133">Какие поля из строк накладной пользователь захочет видеть на мобильных устройствах и в каком порядке?</span><span class="sxs-lookup"><span data-stu-id="40c4f-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="40c4f-134">Сколько строк накладной содержит накладная?</span><span class="sxs-lookup"><span data-stu-id="40c4f-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="40c4f-135">Применяйте здесь правило 80-20 и оптимизируйте для 80 процентов.</span><span class="sxs-lookup"><span data-stu-id="40c4f-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="40c4f-136">Требуется ли пользователям видеть распределения по бухгалтерским счетам (кодирование накладных) на мобильном устройстве во время проверок?</span><span class="sxs-lookup"><span data-stu-id="40c4f-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="40c4f-137">Если ответ на этот вопрос "Да", рассмотрите следующие вопросы:</span><span class="sxs-lookup"><span data-stu-id="40c4f-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="40c4f-138">Сколько распределений по бухгалтерским счетам (сумма без учета скидок и наценок, налог с продаж, расходы, разбиения и т. д.) имеется в строке накладной?</span><span class="sxs-lookup"><span data-stu-id="40c4f-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="40c4f-139">Опять же, применяйте правило 80-20.</span><span class="sxs-lookup"><span data-stu-id="40c4f-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="40c4f-140">Содержат ли накладные распределения по бухгалтерским счетам также и в заголовке накладной?</span><span class="sxs-lookup"><span data-stu-id="40c4f-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="40c4f-141">Если да, должны ли эти распределения по бухгалтерским счетам были доступны на устройстве?</span><span class="sxs-lookup"><span data-stu-id="40c4f-141">If so, should these accounting distributions be available on the device?</span></span>

    > [!NOTE]
    > <span data-ttu-id="40c4f-142">В этом разделе не объясняется, как изменять распределения по бухгалтерским счетам, поскольку эта функция не поддерживается в настоящее время для мобильных сценариев.</span><span class="sxs-lookup"><span data-stu-id="40c4f-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="40c4f-143">Требуется ли пользователям просматривать вложения для накладной на устройстве?</span><span class="sxs-lookup"><span data-stu-id="40c4f-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="40c4f-144">Разработка мобильной работы для утверждения накладных будет отличаться в зависимости от ответов на эти вопросы.</span><span class="sxs-lookup"><span data-stu-id="40c4f-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="40c4f-145">Целью является оптимизация работы пользователей для бизнес-процесса на мобильным устройстве в организации.</span><span class="sxs-lookup"><span data-stu-id="40c4f-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="40c4f-146">В оставшейся части этого раздела рассмотрим два варианта сценария, которые основаны на разных ответах на предыдущие вопросы.</span><span class="sxs-lookup"><span data-stu-id="40c4f-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="40c4f-147">В качестве общих рекомендаций, при работе с мобильным конструктором обязательно публикуйте изменения во избежание потери обновлений.</span><span class="sxs-lookup"><span data-stu-id="40c4f-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="40c4f-148">Разработка простого сценария утверждения накладных для Contoso</span><span class="sxs-lookup"><span data-stu-id="40c4f-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="40c4f-149">Атрибут сценария</span><span class="sxs-lookup"><span data-stu-id="40c4f-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="40c4f-150">Ответ</span><span class="sxs-lookup"><span data-stu-id="40c4f-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="40c4f-151">Какие поля из заголовка накладной пользователь захочет видеть на мобильных устройствах и в каком порядке?</span><span class="sxs-lookup"><span data-stu-id="40c4f-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="40c4f-152">Наименование Поставщика</span><span class="sxs-lookup"><span data-stu-id="40c4f-152">Vendor name</span></span></li>
<li><span data-ttu-id="40c4f-153">Общее количество по накладной</span><span class="sxs-lookup"><span data-stu-id="40c4f-153">Invoice total</span></span></li>
<li><span data-ttu-id="40c4f-154">Счет на</span><span class="sxs-lookup"><span data-stu-id="40c4f-154">Invoice account</span></span></li>
<li><span data-ttu-id="40c4f-155">Номер накладной</span><span class="sxs-lookup"><span data-stu-id="40c4f-155">Invoice number</span></span></li>
<li><span data-ttu-id="40c4f-156">Дата накладной</span><span class="sxs-lookup"><span data-stu-id="40c4f-156">Invoice date</span></span></li>
<li><span data-ttu-id="40c4f-157">Описание накладной</span><span class="sxs-lookup"><span data-stu-id="40c4f-157">Invoice description</span></span></li>
<li><span data-ttu-id="40c4f-158">Срок</span><span class="sxs-lookup"><span data-stu-id="40c4f-158">Due date</span></span></li>
<li><span data-ttu-id="40c4f-159">Валюта накладной</span><span class="sxs-lookup"><span data-stu-id="40c4f-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40c4f-160">Какие поля из строк накладной пользователь захочет видеть на мобильных устройствах и в каком порядке?</span><span class="sxs-lookup"><span data-stu-id="40c4f-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="40c4f-161">Категория закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="40c4f-161">Procurement category</span></span></li>
<li><span data-ttu-id="40c4f-162">Количество</span><span class="sxs-lookup"><span data-stu-id="40c4f-162">Quantity</span></span></li>
<li><span data-ttu-id="40c4f-163">Цена за ед. изм.</span><span class="sxs-lookup"><span data-stu-id="40c4f-163">Unit price</span></span></li>
<li><span data-ttu-id="40c4f-164">Чистая сумма строки</span><span class="sxs-lookup"><span data-stu-id="40c4f-164">Line net amount</span></span></li>
<li><span data-ttu-id="40c4f-165">Сумма по форме 1099</span><span class="sxs-lookup"><span data-stu-id="40c4f-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40c4f-166">Сколько строк накладной содержит накладная?</span><span class="sxs-lookup"><span data-stu-id="40c4f-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="40c4f-167">Применяйте здесь правило 80-20 и оптимизируйте для 80 процентов.</span><span class="sxs-lookup"><span data-stu-id="40c4f-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="40c4f-168">1</span><span class="sxs-lookup"><span data-stu-id="40c4f-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40c4f-169">Требуется ли пользователям видеть распределения по бухгалтерским счетам (кодирование накладных) на мобильном устройстве во время проверок?</span><span class="sxs-lookup"><span data-stu-id="40c4f-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="40c4f-170">Да</span><span class="sxs-lookup"><span data-stu-id="40c4f-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40c4f-171">Сколько распределений по бухгалтерским счетам (сумма без учета скидок и наценок, налог с продаж, расходы и т. д.) имеется в строке накладной?</span><span class="sxs-lookup"><span data-stu-id="40c4f-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="40c4f-172">Опять же, применяйте правило 80-20.</span><span class="sxs-lookup"><span data-stu-id="40c4f-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="40c4f-173">Сумма без учета скидок и наценок: 2 Налог: 0 Расходы: 0</span><span class="sxs-lookup"><span data-stu-id="40c4f-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40c4f-174">Содержат ли накладные распределения по бухгалтерским счетам также и в заголовке накладной?</span><span class="sxs-lookup"><span data-stu-id="40c4f-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="40c4f-175">Если да, должны ли эти распределения по бухгалтерским счетам были доступны на устройстве?</span><span class="sxs-lookup"><span data-stu-id="40c4f-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="40c4f-176">Не используется</span><span class="sxs-lookup"><span data-stu-id="40c4f-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40c4f-177">Требуется ли пользователям просматривать вложения для накладной на устройстве?</span><span class="sxs-lookup"><span data-stu-id="40c4f-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="40c4f-178">Да</span><span class="sxs-lookup"><span data-stu-id="40c4f-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="40c4f-179">Создание рабочей области</span><span class="sxs-lookup"><span data-stu-id="40c4f-179">Create the workspace</span></span>

1.  <span data-ttu-id="40c4f-180">В браузере выполните вход в приложение.</span><span class="sxs-lookup"><span data-stu-id="40c4f-180">In a browser, and sign in to the application.</span></span>
2.  <span data-ttu-id="40c4f-181">После входа добавьте **&mode=mobile** к URL-адресу, как показано в следующем примере, и обновите страницу: https://&lt;ваш_URL&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="40c4f-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="40c4f-182">Нажмите кнопку **Параметры** (шестеренка) в правом верхнем углу страницы, затем нажмите **Мобильное приложение**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="40c4f-183">Должен открыться конструктор мобильного приложения, точно так же, как отображается регистратора задач.</span><span class="sxs-lookup"><span data-stu-id="40c4f-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="40c4f-184">Нажмите **Добавить**, чтобы создать новую рабочую область.</span><span class="sxs-lookup"><span data-stu-id="40c4f-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="40c4f-185">Для этого примера назовите рабочую область **Мои утверждения**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="40c4f-186">Введите описание.</span><span class="sxs-lookup"><span data-stu-id="40c4f-186">Enter a description.</span></span>
6.  <span data-ttu-id="40c4f-187">Выберите цвет рабочей области.</span><span class="sxs-lookup"><span data-stu-id="40c4f-187">Select a workspace color.</span></span> <span data-ttu-id="40c4f-188">Цвет рабочей области будут использоваться для общего стилевого оформления в мобильном устройстве для этой рабочей области.</span><span class="sxs-lookup"><span data-stu-id="40c4f-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="40c4f-189">Выберите значок для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="40c4f-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="40c4f-190">Щелкните **Готово**</span><span class="sxs-lookup"><span data-stu-id="40c4f-190">Click **Done**</span></span>
9.  <span data-ttu-id="40c4f-191">Нажмите **Публикация рабочей области**, чтобы сохранить изменения</span><span class="sxs-lookup"><span data-stu-id="40c4f-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="40c4f-192">Накладные поставщика, назначенные мне</span><span class="sxs-lookup"><span data-stu-id="40c4f-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="40c4f-193">Первая страница мобильных устройств, которую следует разработать — это список накладных, назначенных пользователю для проверки.</span><span class="sxs-lookup"><span data-stu-id="40c4f-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="40c4f-194">Для разработки этой страницы для мобильных устройств используйте страницу **VendMobileInvoiceAssignedToMeListPage**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page.</span></span> <span data-ttu-id="40c4f-195">Прежде чем завершить эту процедуру, убедитесь, что по крайней мере одна накладная поставщика назначена вам для проверки, и что строка накладной содержит не менее двух распределений.</span><span class="sxs-lookup"><span data-stu-id="40c4f-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="40c4f-196">Эта настройка соответствует требованиям для этого сценария.</span><span class="sxs-lookup"><span data-stu-id="40c4f-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="40c4f-197">В URL-адресе измените имя пункта меню на **VendMobileInvoiceAssignedToMeListPage**, чтобы открыть мобильную версию страницы списка **Ожидающие накладные поставщика, назначенные мне** в модуле **Расчеты с поставщиками**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-197">In the URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="40c4f-198">В зависимости от количества накладных, назначенных вам в системе, на этой странице отображаются эти накладные.</span><span class="sxs-lookup"><span data-stu-id="40c4f-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="40c4f-199">Чтобы найти конкретную накладную, используйте расположенный слева фильтр.</span><span class="sxs-lookup"><span data-stu-id="40c4f-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="40c4f-200">Однако для этого примере конкретная накладная не требуется.</span><span class="sxs-lookup"><span data-stu-id="40c4f-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="40c4f-201">Нам просто нужна какая-то накладная, назначенная вам, которая позволяет разрабатывать страницу для мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="40c4f-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="40c4f-202">Новые доступные страницы были специально разработаны для разработки мобильных сценариев для накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="40c4f-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="40c4f-203">Таким образом, необходимо использовать эти страницы.</span><span class="sxs-lookup"><span data-stu-id="40c4f-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="40c4f-204">URL-адрес должен быть похож на следующий URL-адрес, и после его ввода должна открыться страница, которая показана на рисунке: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span><span class="sxs-lookup"><span data-stu-id="40c4f-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span></span> 

    <span data-ttu-id="40c4f-205">[![Страница ожидающих накладных поставщика, назначенных мне](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="40c4f-205">[![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
    
2.  <span data-ttu-id="40c4f-206">Нажмите кнопку **Параметры** (шестеренка) в правом верхнем углу страницы, затем нажмите **Мобильное приложение**</span><span class="sxs-lookup"><span data-stu-id="40c4f-206">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="40c4f-207">Выберите свою рабочую область и нажмите **Изменить**</span><span class="sxs-lookup"><span data-stu-id="40c4f-207">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="40c4f-208">Щелкните **Добавить страницу** для создания первой страницы для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="40c4f-208">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="40c4f-209">Введите имя, например **Мои накладные поставщика**, и описание, например **Накладные поставщика, назначенные мне для проверки**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-209">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="40c4f-210">Щелкните **Готово**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-210">Click **Done**.</span></span>
7.  <span data-ttu-id="40c4f-211">В мобильном конструкторе на вкладке **Поля** нажмите **Выбрать поля**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-211">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="40c4f-212">Столбцы на странице списка должны быть похожи на следующий рисунок.</span><span class="sxs-lookup"><span data-stu-id="40c4f-212">The columns on the list page must resemble the following illustration.</span></span> 

    <span data-ttu-id="40c4f-213">[![Столбцы на странице "Ожидающие накладные поставщика, назначенные мне"](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="40c4f-213">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
    
8.  <span data-ttu-id="40c4f-214">Добавьте необходимые столбцы со страницы списка, которые должны отображаться пользователям на странице мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="40c4f-214">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="40c4f-215">Порядок, в котором добавляются поля, соответствует порядку, в котором поля отображаются для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="40c4f-215">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="40c4f-216">Единственный способ изменить порядок полей — повторно выбрать все поля.</span><span class="sxs-lookup"><span data-stu-id="40c4f-216">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="40c4f-217">На основе требований для этого сценария, нужные следующие восемь полей.</span><span class="sxs-lookup"><span data-stu-id="40c4f-217">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="40c4f-218">Однако некоторые пользователи могут считать, что восемь полей — это слишком большой объем информации для мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="40c4f-218">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="40c4f-219">Поэтому в представлении списка на мобильном устройстве мы будет отображать только самые важные поля.</span><span class="sxs-lookup"><span data-stu-id="40c4f-219">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="40c4f-220">Остальные поля будут отображаться в табличном представлении, который мы разработаем позже.</span><span class="sxs-lookup"><span data-stu-id="40c4f-220">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="40c4f-221">Пока мы добавим следующие поля.</span><span class="sxs-lookup"><span data-stu-id="40c4f-221">For now, we will add the following fields.</span></span> <span data-ttu-id="40c4f-222">Щелкните знак "плюс" (**+**) в этих столбцах, чтобы добавить их на страницу мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="40c4f-222">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="40c4f-223">Наименование Поставщика</span><span class="sxs-lookup"><span data-stu-id="40c4f-223">Vendor name</span></span>
    - <span data-ttu-id="40c4f-224">Общее количество по накладной</span><span class="sxs-lookup"><span data-stu-id="40c4f-224">Invoice total</span></span>
    - <span data-ttu-id="40c4f-225">Счет на</span><span class="sxs-lookup"><span data-stu-id="40c4f-225">Invoice account</span></span>
    - <span data-ttu-id="40c4f-226">Номер накладной</span><span class="sxs-lookup"><span data-stu-id="40c4f-226">Invoice number</span></span>
    - <span data-ttu-id="40c4f-227">Дата накладной</span><span class="sxs-lookup"><span data-stu-id="40c4f-227">Invoice date</span></span>

    <span data-ttu-id="40c4f-228">После добавления этих поля страница мобильных устройств должно быть похожа на страницу на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="40c4f-228">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    
    <span data-ttu-id="40c4f-229">[![Страница после добавления полей](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="40c4f-229">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>

9.  <span data-ttu-id="40c4f-230">Теперь необходимо также добавить следующие столбцы, чтобы впоследствии можно было включить действия workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="40c4f-230">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="40c4f-231">Показать задачу завершения</span><span class="sxs-lookup"><span data-stu-id="40c4f-231">Show complete task</span></span>
    - <span data-ttu-id="40c4f-232">Показать задачу делегирования</span><span class="sxs-lookup"><span data-stu-id="40c4f-232">Show delegate task</span></span>
    - <span data-ttu-id="40c4f-233">Показать задачу отзыва</span><span class="sxs-lookup"><span data-stu-id="40c4f-233">Show recall task</span></span>
    - <span data-ttu-id="40c4f-234">Показать задачу отклонения</span><span class="sxs-lookup"><span data-stu-id="40c4f-234">Show reject task</span></span>
    - <span data-ttu-id="40c4f-235">Показать задачу запроса завершения</span><span class="sxs-lookup"><span data-stu-id="40c4f-235">Show request completion task</span></span>
    - <span data-ttu-id="40c4f-236">Показать задачу повторной отправки</span><span class="sxs-lookup"><span data-stu-id="40c4f-236">Show resubmit task</span></span>

10. <span data-ttu-id="40c4f-237">Щелкните **Готово**, чтобы выйти из режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="40c4f-237">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="40c4f-238">Щелкните **Назад**, а затем **Готово** для выхода из рабочей области</span><span class="sxs-lookup"><span data-stu-id="40c4f-238">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="40c4f-239">Нажмите **Публикация рабочей области**, чтобы сохранить свою работу.</span><span class="sxs-lookup"><span data-stu-id="40c4f-239">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="40c4f-240">Включите **Отображать итог по накладной в списке ожидающих накладных поставщика** в форме параметров расчетов с поставщиками в разделе **Накладная**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-240">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="40c4f-241">Обратите внимание, что только в том случае, если этот параметр включен, итоги по накладным будет рассчитываться для отображения на странице списка ожидающих накладных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="40c4f-241">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="40c4f-242">Это новая возможность в рамках необходимого исправления 3208224.</span><span class="sxs-lookup"><span data-stu-id="40c4f-242">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="40c4f-243">Сведения о накладных поставщика</span><span class="sxs-lookup"><span data-stu-id="40c4f-243">Vendor invoice details</span></span>

<span data-ttu-id="40c4f-244">Для создания страницы сведения о накладной для мобильных устройств используйте страницу **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-244">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="40c4f-245">Обратите внимание, что, в зависимости от количества накладных, которые имеются в системе, на этой странице отображается самая старая накладная (накладная, которая была создана первой).</span><span class="sxs-lookup"><span data-stu-id="40c4f-245">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="40c4f-246">Чтобы найти конкретную накладную, используйте расположенный слева фильтр.</span><span class="sxs-lookup"><span data-stu-id="40c4f-246">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="40c4f-247">Однако для этого примере конкретная накладная не требуется.</span><span class="sxs-lookup"><span data-stu-id="40c4f-247">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="40c4f-248">Нам просто требуются некоторые данные по накладной, чтобы можно было разрабатывать страницу для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="40c4f-248">We just require some invoice data so that we can design the mobile page.</span></span> 

<span data-ttu-id="40c4f-249">[![Страница workflow-процесса](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="40c4f-249">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="40c4f-250">В URL-адресе замените имя пункта меню на **VendMobileInvoiceHeaderDetails**, чтобы открыть форму</span><span class="sxs-lookup"><span data-stu-id="40c4f-250">In the URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>

2. <span data-ttu-id="40c4f-251">Откройте конструктор мобильных устройств с помощью кнопки **Параметры** (шестеренка).</span><span class="sxs-lookup"><span data-stu-id="40c4f-251">Open the mobile designer from the **Settings** (gear) button.</span></span>

3. <span data-ttu-id="40c4f-252">Щелкните кнопку **Изменить** для запуска режима редактирования в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="40c4f-252">Click the **Edit** button to start edit mode in the workspace.</span></span>

4. <span data-ttu-id="40c4f-253">Выберите ранее созданную страницу **Мои накладные поставщика**, затем щелкните **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-253">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>

5. <span data-ttu-id="40c4f-254">На вкладке **Поля** щелкните заголовок столбца **Сетка**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-254">On the **Fields** tab, click the **Grid** column heading.</span></span>

6. <span data-ttu-id="40c4f-255">Щелкните **Свойства &gt; Добавить страницу**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-255">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="40c4f-256">**Примечание.** При нажатии заголовка **Сетка** и добавлении страницы автоматически устанавливается связь со страницей сведений.</span><span class="sxs-lookup"><span data-stu-id="40c4f-256">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>

7. <span data-ttu-id="40c4f-257">Введите заголовок страницы, например **Сведения о накладной**, и описание, например **Просмотр заголовка накладной и сведений о строках**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-257">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>

8. <span data-ttu-id="40c4f-258">Нажмите **Выбор полей**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-258">Click **Select fields**.</span></span> <span data-ttu-id="40c4f-259">Обратите внимание, что порядок, в котором добавляются поля, соответствует порядку, в котором поля отображаются для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="40c4f-259">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="40c4f-260">Единственный способ изменить порядок полей — повторно выбрать все поля.</span><span class="sxs-lookup"><span data-stu-id="40c4f-260">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 

9. <span data-ttu-id="40c4f-261">Добавьте следующие поля из заголовка, на основе требований для этого сценария:</span><span class="sxs-lookup"><span data-stu-id="40c4f-261">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="40c4f-262">Наименование Поставщика</span><span class="sxs-lookup"><span data-stu-id="40c4f-262">Vendor name</span></span>
   - <span data-ttu-id="40c4f-263">Общее количество по накладной</span><span class="sxs-lookup"><span data-stu-id="40c4f-263">Invoice total</span></span>
   - <span data-ttu-id="40c4f-264">Счет на</span><span class="sxs-lookup"><span data-stu-id="40c4f-264">Invoice account</span></span>
   - <span data-ttu-id="40c4f-265">Номер накладной</span><span class="sxs-lookup"><span data-stu-id="40c4f-265">Invoice number</span></span>
   - <span data-ttu-id="40c4f-266">Дата накладной</span><span class="sxs-lookup"><span data-stu-id="40c4f-266">Invoice date</span></span>
   - <span data-ttu-id="40c4f-267">Описание накладной</span><span class="sxs-lookup"><span data-stu-id="40c4f-267">Invoice description</span></span>
   - <span data-ttu-id="40c4f-268">Срок</span><span class="sxs-lookup"><span data-stu-id="40c4f-268">Due date</span></span>
   - <span data-ttu-id="40c4f-269">Валюта накладной</span><span class="sxs-lookup"><span data-stu-id="40c4f-269">Invoice currency</span></span>

10. <span data-ttu-id="40c4f-270">Добавьте следующие поля из сетки строк на странице:</span><span class="sxs-lookup"><span data-stu-id="40c4f-270">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="40c4f-271">Категория закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="40c4f-271">Procurement category</span></span>
    - <span data-ttu-id="40c4f-272">Количество</span><span class="sxs-lookup"><span data-stu-id="40c4f-272">Quantity</span></span>
    - <span data-ttu-id="40c4f-273">Цена за ед. изм.</span><span class="sxs-lookup"><span data-stu-id="40c4f-273">Unit price</span></span>
    - <span data-ttu-id="40c4f-274">Чистая сумма строки</span><span class="sxs-lookup"><span data-stu-id="40c4f-274">Line net amount</span></span>
    - <span data-ttu-id="40c4f-275">Сумма по форме 1099</span><span class="sxs-lookup"><span data-stu-id="40c4f-275">1099 amount</span></span>

11. <span data-ttu-id="40c4f-276">После добавления всех полей из двух предыдущих шагов щелкните **Готово**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-276">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="40c4f-277">Страница должна выглядеть аналогично показанной на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="40c4f-277">The page must resemble the following illustration.</span></span>
    
    <span data-ttu-id="40c4f-278">[![На рисунке показаны добавленные дополнительные поля](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="40c4f-278">[![Illustration showing additional fields added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>

12. <span data-ttu-id="40c4f-279">Щелкните **Готово**, чтобы выйти из режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="40c4f-279">Click **Done** to exit edit mode.</span></span>

13. <span data-ttu-id="40c4f-280">Щелкните **Назад**, а затем **Готово** для выхода из рабочей области</span><span class="sxs-lookup"><span data-stu-id="40c4f-280">Click **Back** and then **Done** to exit the workspace</span></span>

14. <span data-ttu-id="40c4f-281">Нажмите **Публикация рабочей области**, чтобы сохранить свою работу</span><span class="sxs-lookup"><span data-stu-id="40c4f-281">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="40c4f-282">Действия workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="40c4f-282">Workflow actions</span></span>

<span data-ttu-id="40c4f-283">Для добавления действий рабочего процесса используйте страницу **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-283">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="40c4f-284">Чтобы открыть эту страницу, замените имя пункта меню в URL-адреса, как было сделано ранее.</span><span class="sxs-lookup"><span data-stu-id="40c4f-284">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="40c4f-285">Затем откройте конструктор мобильных устройств с помощью кнопки **Параметры** (шестеренка).</span><span class="sxs-lookup"><span data-stu-id="40c4f-285">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="40c4f-286">Выполните следующие шаги для добавления действий workflow-процесса на странице сведений.</span><span class="sxs-lookup"><span data-stu-id="40c4f-286">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="40c4f-287">Необходимо наличие назначенных вам накладных в соответствующем состоянии, делающим доступными вам действия workflow-процесса, для которых вы собираетесь выполнить разработку.</span><span class="sxs-lookup"><span data-stu-id="40c4f-287">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="40c4f-288">Запись действий workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="40c4f-288">Record workflow actions</span></span>
1.  <span data-ttu-id="40c4f-289">Щелкните кнопку **Изменить** для запуска режима редактирования в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="40c4f-289">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="40c4f-290">Выберите ранее созданную страницу **Сведения о накладной**, затем щелкните **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-290">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="40c4f-291">На вкладке **Действия** нажмите **Добавить действие**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-291">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="40c4f-292">Введите заголовок действия, например **Утвердить**, и описание, например **Утвердить накладную**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-292">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="40c4f-293">Обратите внимание, что введенное здесь название действия становится именем действия, которое отображается для пользователя в мобильном приложении.</span><span class="sxs-lookup"><span data-stu-id="40c4f-293">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="40c4f-294">Щелкните **Готово**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-294">Click **Done**.</span></span>
6.  <span data-ttu-id="40c4f-295">Нажмите **Выбор полей**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-295">Click **Select fields**.</span></span>
7.  <span data-ttu-id="40c4f-296">Выполните workflow-процесс на странице **VendMobileInvoiceHeaderDetails** и выполните действие, которое вы хотите записать.</span><span class="sxs-lookup"><span data-stu-id="40c4f-296">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="40c4f-297">Обязательно введите комментарии workflow-процесса во время этого процесса, чтобы поле комментариев также было доступно пользователям мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="40c4f-297">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="40c4f-298">После выполнения действия workflow-процесса нажмите кнопку **Готово**, чтобы завершить задачу "Выбор полей".</span><span class="sxs-lookup"><span data-stu-id="40c4f-298">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="40c4f-299">Щелкните **Готово**, чтобы выйти из режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="40c4f-299">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="40c4f-300">Щелкните **Назад**, а затем **Готово** для выхода из рабочей области</span><span class="sxs-lookup"><span data-stu-id="40c4f-300">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="40c4f-301">Нажмите **Публикация рабочей области**, чтобы сохранить свою работу</span><span class="sxs-lookup"><span data-stu-id="40c4f-301">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="40c4f-302">Повторите предыдущие шаги для записи всех необходимых действий workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="40c4f-302">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="40c4f-303">Создание JS-файла</span><span class="sxs-lookup"><span data-stu-id="40c4f-303">Create a .js file</span></span>
1. <span data-ttu-id="40c4f-304">Откройте Блокнот или Microsoft Visual Studio и вставьте следующий код.</span><span class="sxs-lookup"><span data-stu-id="40c4f-304">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="40c4f-305">Сохраните файл как файл JS.</span><span class="sxs-lookup"><span data-stu-id="40c4f-305">Save the file as a .js file.</span></span> <span data-ttu-id="40c4f-306">Этот код выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="40c4f-306">This code does the following:</span></span>
    - <span data-ttu-id="40c4f-307">Он скрывает дополнительные столбцы, связанные с workflow-процессом, которые ранее были добавлены на страницу мобильного списка.</span><span class="sxs-lookup"><span data-stu-id="40c4f-307">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="40c4f-308">Мы добавили эти столбцы, чтобы приложение имело эти сведения в контексте и могло выполнить следующий шаг.</span><span class="sxs-lookup"><span data-stu-id="40c4f-308">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="40c4f-309">На основании активного шага бизнес-процесса, он применяет логику для отображения только этих действий.</span><span class="sxs-lookup"><span data-stu-id="40c4f-309">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="40c4f-310">Имена страниц и других элементов управления в коде должны быть такими же, как и в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="40c4f-310">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }
    ```

2.  <span data-ttu-id="40c4f-311">Отправьте файл кода в рабочую область, выбрав вкладку **Логика**</span><span class="sxs-lookup"><span data-stu-id="40c4f-311">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="40c4f-312">Щелкните **Готово**, чтобы выйти из режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="40c4f-312">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="40c4f-313">Щелкните **Назад**, а затем **Готово** для выхода из рабочей области</span><span class="sxs-lookup"><span data-stu-id="40c4f-313">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="40c4f-314">Нажмите **Публикация рабочей области**, чтобы сохранить свою работу</span><span class="sxs-lookup"><span data-stu-id="40c4f-314">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="40c4f-315">Вложения накладной поставщиков</span><span class="sxs-lookup"><span data-stu-id="40c4f-315">Vendor invoice attachments</span></span>

1. <span data-ttu-id="40c4f-316">Нажмите кнопку **Параметры** (шестеренка) в правом верхнем углу страницы, затем нажмите **Мобильное приложение**</span><span class="sxs-lookup"><span data-stu-id="40c4f-316">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>

2. <span data-ttu-id="40c4f-317">Щелкните кнопку **Изменить** для запуска режима редактирования в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="40c4f-317">Click the **Edit** button to start edit mode in the workspace.</span></span>

3. <span data-ttu-id="40c4f-318">Выберите ранее созданную страницу <strong>Сведения о накладной\*\*, затем щелкните \*\*Изменить</strong>.</span><span class="sxs-lookup"><span data-stu-id="40c4f-318">Select the <strong>Invoice details \*\*page that you created earlier, and then click \*\*Edit</strong>.</span></span>

4. <span data-ttu-id="40c4f-319">Задайте для параметра **Управление документами** значение **Да**, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="40c4f-319">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="40c4f-320">**Примечание.** Если не требуется отображать вложения на мобильном устройстве, можно оставить для этого параметра значение **Нет**, что является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="40c4f-320">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   
   ![Управление документами](./media/docmanagement-216x300.png)

5. <span data-ttu-id="40c4f-322">Щелкните **Готово**, чтобы выйти из режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="40c4f-322">Click **Done** to exit edit mode.</span></span>

6. <span data-ttu-id="40c4f-323">Щелкните **Назад**, а затем **Готово** для выхода из рабочей области</span><span class="sxs-lookup"><span data-stu-id="40c4f-323">Click **Back** and then **Done** to exit the workspace</span></span>

7. <span data-ttu-id="40c4f-324">Нажмите **Публикация рабочей области**, чтобы сохранить свою работу</span><span class="sxs-lookup"><span data-stu-id="40c4f-324">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="40c4f-325">Распределения строки накладной поставщика</span><span class="sxs-lookup"><span data-stu-id="40c4f-325">Vendor invoice line distributions</span></span>

<span data-ttu-id="40c4f-326">Требования для данного сценария утверждают, что будет только одно распределение на уровне строки, а накладная всегда будет содержать только одну строку.</span><span class="sxs-lookup"><span data-stu-id="40c4f-326">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="40c4f-327">Поскольку этот сценарий является простым, работа пользователя на мобильном устройстве также должна быть достаточно простой, чтобы пользователю не нужно было переходить через несколько уровней для просмотра распределений.</span><span class="sxs-lookup"><span data-stu-id="40c4f-327">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="40c4f-328">Накладные поставщика включают параметр отображения всех распределений из заголовка накладной.</span><span class="sxs-lookup"><span data-stu-id="40c4f-328">Vendor invoices include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="40c4f-329">Именно это требуется для мобильного сценария.</span><span class="sxs-lookup"><span data-stu-id="40c4f-329">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="40c4f-330">Поэтому мы будет использовать страницу **VendMobileInvoiceAllDistributionTree** для разработки этой части мобильного сценария.</span><span class="sxs-lookup"><span data-stu-id="40c4f-330">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="40c4f-331">Знание требований помогает решить, какую конкретную страницу следует использовать и как именно оптимизировать мобильную работу для пользователя при разработке сценария.</span><span class="sxs-lookup"><span data-stu-id="40c4f-331">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="40c4f-332">Во втором сценарии будет использоваться другая страница для отображения распределений, так как требования для этого сценария отличаются.</span><span class="sxs-lookup"><span data-stu-id="40c4f-332">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="40c4f-333">В URL-адресе замените имя пункта меню, как делали раньше.</span><span class="sxs-lookup"><span data-stu-id="40c4f-333">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="40c4f-334">Страница, которая отображается, должен быть похожа на страницу на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="40c4f-334">The page that appears should resemble the following illustration.</span></span>

    <span data-ttu-id="40c4f-335">[![Страница "Все распределения"](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="40c4f-335">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>

2.  <span data-ttu-id="40c4f-336">Откройте конструктор мобильных устройств с помощью кнопки **Параметры** (шестеренка).</span><span class="sxs-lookup"><span data-stu-id="40c4f-336">Open the mobile designer from the **Settings** (gear) button.</span></span>

3.  <span data-ttu-id="40c4f-337">Щелкните кнопку **Изменить** для запуска режима редактирования в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="40c4f-337">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="40c4f-338">**Примечание.** Вы увидите, что две новые страницы были созданы автоматически.</span><span class="sxs-lookup"><span data-stu-id="40c4f-338">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="40c4f-339">Система создает эти страницы, поскольку вы включили управление документами в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="40c4f-339">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="40c4f-340">Можно игнорировать эти новые страницы.</span><span class="sxs-lookup"><span data-stu-id="40c4f-340">You can ignore these new pages.</span></span>

4.  <span data-ttu-id="40c4f-341">Щелкните **Добавить страницу**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-341">Click **Add page**.</span></span>

5.  <span data-ttu-id="40c4f-342">Введите заголовок страницы, например **Просмотр учета**, и описание, например **Просмотр учета для накладной**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-342">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>

6.  <span data-ttu-id="40c4f-343">Щелкните **Готово**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-343">Click **Done**.</span></span>

7.  <span data-ttu-id="40c4f-344">На вкладке **Поля** щелкните **Выбрать поля**, выберите следующие поля на странице распределений и нажмите кнопку **Готово**:</span><span class="sxs-lookup"><span data-stu-id="40c4f-344">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="40c4f-345">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="40c4f-345">Amount</span></span>
    2.  <span data-ttu-id="40c4f-346">Валютное</span><span class="sxs-lookup"><span data-stu-id="40c4f-346">Currency</span></span>
    3.  <span data-ttu-id="40c4f-347">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="40c4f-347">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="40c4f-348">Мы не выбрали столбец **Описание** в сетке распределений, поскольку требования для данного сценария утверждает, что сумма без учета скидок и наценок — это единственная сумма, для которой будут распределения.</span><span class="sxs-lookup"><span data-stu-id="40c4f-348">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="40c4f-349">Поэтому пользователю не требуется другое поле для определения типа суммы, к которой относится распределение.</span><span class="sxs-lookup"><span data-stu-id="40c4f-349">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="40c4f-350">Однако в следующем сценарии мы **будем** использовать эту информацию, поскольку в требованиях для данного сценария указано, что другие типы сумм имеют распределения (например, налог).</span><span class="sxs-lookup"><span data-stu-id="40c4f-350">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>

8.  <span data-ttu-id="40c4f-351">Щелкните **Готово**, чтобы выйти из режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="40c4f-351">Click **Done** to exit edit mode.</span></span>

9.  <span data-ttu-id="40c4f-352">Щелкните **Назад**, а затем **Готово** для выхода из рабочей области</span><span class="sxs-lookup"><span data-stu-id="40c4f-352">Click **Back** and then **Done** to exit the workspace</span></span>

10. <span data-ttu-id="40c4f-353">Нажмите **Публикация рабочей области**, чтобы сохранить свою работу</span><span class="sxs-lookup"><span data-stu-id="40c4f-353">Click **Publish workspace** to save your work</span></span>

#### <a name="adding-navigation-to-view-accounting-page"></a><span data-ttu-id="40c4f-354">Добавление переходов к странице "Просмотр учета"</span><span class="sxs-lookup"><span data-stu-id="40c4f-354">Adding navigation to "View accounting" page</span></span>

<span data-ttu-id="40c4f-355">Страница для мобильных устройств **Просмотр учета** в настоящее время не привязана ни к каким мобильным страницам, которые мы разработали до этого момента.</span><span class="sxs-lookup"><span data-stu-id="40c4f-355">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="40c4f-356">Так как пользователь должен иметь возможности перехода к странице **Просмотр учета** со страницы **Сведения о накладной** на мобильном устройстве, необходимо предоставить переход со страницы **Сведения о накладной** на страницу **Просмотр учета**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-356">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="40c4f-357">Мы обеспечиваем эту навигацию с помощью дополнительной логики через JavaScript.</span><span class="sxs-lookup"><span data-stu-id="40c4f-357">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="40c4f-358">Откройте JS-файл, созданный ранее, и добавьте строки, выделенные в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="40c4f-358">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="40c4f-359">Этот код выполняет следующие две операции:</span><span class="sxs-lookup"><span data-stu-id="40c4f-359">This code does two things:</span></span>
    1.  <span data-ttu-id="40c4f-360">Он помогает гарантировать, что пользователь не может перейти на страницу **Просмотр учета** непосредственно из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="40c4f-360">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="40c4f-361">Он создает элемент управления переходом со страницы **Сведения о накладной** на страницу **Просмотр учета**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-361">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="40c4f-362">Имена страниц и других элементов управления в коде должны быть такими же, как и в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="40c4f-362">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }
    ```
    
2.  <span data-ttu-id="40c4f-363">Отправьте файл кода в рабочую область, выбрав вкладку **Логика**, чтобы перезаписать предыдущий код</span><span class="sxs-lookup"><span data-stu-id="40c4f-363">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="40c4f-364">Щелкните **Готово**, чтобы выйти из режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="40c4f-364">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="40c4f-365">Щелкните **Назад**, а затем **Готово** для выхода из рабочей области</span><span class="sxs-lookup"><span data-stu-id="40c4f-365">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="40c4f-366">Нажмите **Публикация рабочей области**, чтобы сохранить свою работу</span><span class="sxs-lookup"><span data-stu-id="40c4f-366">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="40c4f-367">Проверка</span><span class="sxs-lookup"><span data-stu-id="40c4f-367">Validation</span></span>

<span data-ttu-id="40c4f-368">Со своего мобильного устройства откройте приложение и подключитесь к своему экземпляру.</span><span class="sxs-lookup"><span data-stu-id="40c4f-368">From your mobile device, open the app, and connect to your instance.</span></span> <span data-ttu-id="40c4f-369">Убедитесь, что вы выполнили вход в компанию, в которой вам назначены накладные поставщика для проверки.</span><span class="sxs-lookup"><span data-stu-id="40c4f-369">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="40c4f-370">Вам должны быть доступны следующие действия:</span><span class="sxs-lookup"><span data-stu-id="40c4f-370">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="40c4f-371">Просмотрите рабочую область **Мои утверждения**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-371">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="40c4f-372">Перейдите в рабочую область **Мои утверждения** и просмотрите страницу **Мои накладные поставщика**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-372">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="40c4f-373">Перейдите на страницу **Мои накладные поставщика** и просмотрите список накладных, которые назначены вам.</span><span class="sxs-lookup"><span data-stu-id="40c4f-373">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="40c4f-374">Перейдите в одну из накладных и просмотрите сведения из заголовка накладной и сведения строки.</span><span class="sxs-lookup"><span data-stu-id="40c4f-374">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="40c4f-375">На странице сведений просмотрите ссылку на вложения и используйте эту ссылку для перехода к списку вложений и просмотра вложений.</span><span class="sxs-lookup"><span data-stu-id="40c4f-375">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="40c4f-376">На странице сведений просмотрите ссылку на страницу **Просмотр учета** и используйте эту ссылку для перехода на страницу распределений и просмотра распределений.</span><span class="sxs-lookup"><span data-stu-id="40c4f-376">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="40c4f-377">На странице сведений щелкните меню **Действия** внизу страницы и выполните действия workflow-процесса, которые относятся к этому шагу workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="40c4f-377">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="40c4f-378">Разработка сложного сценария утверждения накладных для Fabrikam</span><span class="sxs-lookup"><span data-stu-id="40c4f-378">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="40c4f-379">Атрибут сценария</span><span class="sxs-lookup"><span data-stu-id="40c4f-379">Scenario attribute</span></span></th>
<th><span data-ttu-id="40c4f-380">Ответ</span><span class="sxs-lookup"><span data-stu-id="40c4f-380">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="40c4f-381">Какие поля из заголовка накладной пользователь захочет видеть на мобильных устройствах и в каком порядке?</span><span class="sxs-lookup"><span data-stu-id="40c4f-381">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="40c4f-382">Наименование Поставщика</span><span class="sxs-lookup"><span data-stu-id="40c4f-382">Vendor name</span></span></li>
<li><span data-ttu-id="40c4f-383">Сумма накладной</span><span class="sxs-lookup"><span data-stu-id="40c4f-383">Invoice amount</span></span></li>
<li><span data-ttu-id="40c4f-384">Счет на</span><span class="sxs-lookup"><span data-stu-id="40c4f-384">Invoice account</span></span></li>
<li><span data-ttu-id="40c4f-385">Номер накладной</span><span class="sxs-lookup"><span data-stu-id="40c4f-385">Invoice number</span></span></li>
<li><span data-ttu-id="40c4f-386">Дата накладной</span><span class="sxs-lookup"><span data-stu-id="40c4f-386">Invoice date</span></span></li>
<li><span data-ttu-id="40c4f-387">Описание накладной</span><span class="sxs-lookup"><span data-stu-id="40c4f-387">Invoice description</span></span></li>
<li><span data-ttu-id="40c4f-388">Срок</span><span class="sxs-lookup"><span data-stu-id="40c4f-388">Due date</span></span></li>
<li><span data-ttu-id="40c4f-389">Валюта накладной</span><span class="sxs-lookup"><span data-stu-id="40c4f-389">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40c4f-390">Какие поля из строк накладной пользователь захочет видеть на мобильных устройствах и в каком порядке?</span><span class="sxs-lookup"><span data-stu-id="40c4f-390">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="40c4f-391">Категория закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="40c4f-391">Procurement category</span></span></li>
<li><span data-ttu-id="40c4f-392">Количество</span><span class="sxs-lookup"><span data-stu-id="40c4f-392">Quantity</span></span></li>
<li><span data-ttu-id="40c4f-393">Цена за ед. изм.</span><span class="sxs-lookup"><span data-stu-id="40c4f-393">Unit price</span></span></li>
<li><span data-ttu-id="40c4f-394">Чистая сумма строки</span><span class="sxs-lookup"><span data-stu-id="40c4f-394">Line net amount</span></span></li>
<li><span data-ttu-id="40c4f-395">Сумма по форме 1099</span><span class="sxs-lookup"><span data-stu-id="40c4f-395">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40c4f-396">Сколько строк накладной содержит накладная?</span><span class="sxs-lookup"><span data-stu-id="40c4f-396">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="40c4f-397">Применяйте здесь правило 80-20 и оптимизируйте для 80 процентов.</span><span class="sxs-lookup"><span data-stu-id="40c4f-397">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="40c4f-398">5</span><span class="sxs-lookup"><span data-stu-id="40c4f-398">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40c4f-399">Требуется ли пользователям видеть распределения по бухгалтерским счетам (кодирование накладных) на мобильном устройстве во время проверок?</span><span class="sxs-lookup"><span data-stu-id="40c4f-399">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="40c4f-400">Да</span><span class="sxs-lookup"><span data-stu-id="40c4f-400">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40c4f-401">Сколько распределений по бухгалтерским счетам (сумма без учета скидок и наценок, налог с продаж, расходы и т. д.) имеется в строке накладной?</span><span class="sxs-lookup"><span data-stu-id="40c4f-401">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="40c4f-402">Опять же, применяйте правило 80-20.</span><span class="sxs-lookup"><span data-stu-id="40c4f-402">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="40c4f-403">Сумма без учета скидок и наценок: 2 Налог: 2 Расходы: 2</span><span class="sxs-lookup"><span data-stu-id="40c4f-403">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40c4f-404">Содержат ли накладные распределения по бухгалтерским счетам также и в заголовке накладной?</span><span class="sxs-lookup"><span data-stu-id="40c4f-404">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="40c4f-405">Если да, должны ли эти распределения по бухгалтерским счетам были доступны на устройстве?</span><span class="sxs-lookup"><span data-stu-id="40c4f-405">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="40c4f-406">Не используется</span><span class="sxs-lookup"><span data-stu-id="40c4f-406">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40c4f-407">Требуется ли пользователям просматривать вложения для накладной на устройстве?</span><span class="sxs-lookup"><span data-stu-id="40c4f-407">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="40c4f-408">Да</span><span class="sxs-lookup"><span data-stu-id="40c4f-408">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="40c4f-409">Далее</span><span class="sxs-lookup"><span data-stu-id="40c4f-409">Next steps</span></span>

<span data-ttu-id="40c4f-410">Можно сделать следующие изменения для сценария 1 в соответствии с требованиями для сценария 2.</span><span class="sxs-lookup"><span data-stu-id="40c4f-410">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="40c4f-411">Этот раздел служит для повышения эффективности работы с мобильными приложениями.</span><span class="sxs-lookup"><span data-stu-id="40c4f-411">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="40c4f-412">Так как в сценарии 2 ожидается больше строк в накладной, следующие изменения в структуре помогут оптимизировать работу пользователей на мобильном устройстве:</span><span class="sxs-lookup"><span data-stu-id="40c4f-412">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="40c4f-413">Вместо просмотра строк накладной на странице сведения (как в сценарии 1), пользователи могут выбрать просмотр строк на отдельной странице мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="40c4f-413">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="40c4f-414">Так как в этом сценарии ожидается более одной строки накладной, если использовать страницу **VendMobileInvoiceAllDistributionTree** при создании страницы распределений для мобильных устройств (как в сценарии 1), пользователю может быть сложно сопоставить строки с распределениями.</span><span class="sxs-lookup"><span data-stu-id="40c4f-414">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="40c4f-415">Поэтому для создания страницы распределений используйте страницу **VendMobileInvoiceLineDistributionTree**.</span><span class="sxs-lookup"><span data-stu-id="40c4f-415">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="40c4f-416">В идеальном случае в этом сценарии распределения должны отображаться в контексте строки накладной.</span><span class="sxs-lookup"><span data-stu-id="40c4f-416">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="40c4f-417">Поэтому убедитесь, что пользователь может перейти в строку для просмотра страницы распределений.</span><span class="sxs-lookup"><span data-stu-id="40c4f-417">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="40c4f-418">Используйте возможность ссылки на страницу для установления детализации, так же, как это было сделано для страниц заголовка и сведений в сценарии 1.</span><span class="sxs-lookup"><span data-stu-id="40c4f-418">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="40c4f-419">Так как в сценарии 2 ожидается более одного типа сумм в распределениях (налог с продаж, расходы и т. д.), будет полезно отобразить описание типа суммы.</span><span class="sxs-lookup"><span data-stu-id="40c4f-419">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="40c4f-420">(Мы опустили эти сведения в сценарии 1.)</span><span class="sxs-lookup"><span data-stu-id="40c4f-420">(We omitted this information in scenario 1.)</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
