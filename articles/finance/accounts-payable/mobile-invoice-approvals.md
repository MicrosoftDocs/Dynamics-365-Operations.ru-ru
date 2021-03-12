---
title: Утверждения накладных на мобильном устройстве
description: Этот раздел представляет практический подход к разработке мобильных сценариев, используя утверждения накладных поставщика для мобильных устройств как вариант использования.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1e18d26a4ccee195d09560c62b1fb1dd05750cfd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991365"
---
# <a name="mobile-invoice-approvals"></a><span data-ttu-id="af4b2-103">Утверждения накладных на мобильном устройстве</span><span class="sxs-lookup"><span data-stu-id="af4b2-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af4b2-104">Мобильные возможности позволяют бизнес-пользователю разрабатывать мобильное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="af4b2-104">Mobile capabilities let a business user design mobile experiences.</span></span> <span data-ttu-id="af4b2-105">Для более сложных сценариев платформа также позволяет разработчикам расширять возможности при необходимости.</span><span class="sxs-lookup"><span data-stu-id="af4b2-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="af4b2-106">Наиболее эффективный способ познакомиться с некоторыми новыми мобильными концепциями — пройти через процесс разработки нескольких сценариев.</span><span class="sxs-lookup"><span data-stu-id="af4b2-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="af4b2-107">Этот раздел представляет практический подход к разработке мобильных сценариев, используя утверждения накладных поставщика для мобильных устройств как вариант использования.</span><span class="sxs-lookup"><span data-stu-id="af4b2-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="af4b2-108">Этот раздел поможет разрабатывать другие варианты сценариев, а также может применяться к другим сценариям, которые не относятся к накладным поставщиков.</span><span class="sxs-lookup"><span data-stu-id="af4b2-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="af4b2-109">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="af4b2-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="af4b2-110">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="af4b2-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="af4b2-111">описание</span><span class="sxs-lookup"><span data-stu-id="af4b2-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af4b2-112">Предварительно ознакомьтесь с руководством по мобильным приложениям</span><span class="sxs-lookup"><span data-stu-id="af4b2-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="af4b2-113">Мобильная платформа</span><span class="sxs-lookup"><span data-stu-id="af4b2-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="af4b2-114">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="af4b2-114">Dynamics 365 Finance</span></span>                                                                              | <span data-ttu-id="af4b2-115">Среда с версией 1611 и обновлением платформы Platform update 3 (ноябрь 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="af4b2-115">An environment that has version 1611 and Platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="af4b2-116">Установите исправление KB 3204341.</span><span class="sxs-lookup"><span data-stu-id="af4b2-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="af4b2-117">Регистратор задач может ошибочно записывать две команды закрытия из раскрывающихся диалоговых окон, которые включены в обновление Platform update 3 (обновление за ноябрь 2016).</span><span class="sxs-lookup"><span data-stu-id="af4b2-117">Task recorder can erroneously record two Close commands for dropdown dialogs; this is included in Platform update 3 (November 2016 update).</span></span> |
| <span data-ttu-id="af4b2-118">Установите исправление KB 3207800.</span><span class="sxs-lookup"><span data-stu-id="af4b2-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="af4b2-119">Это исправление позволяет просматривать вложения на мобильном клиенте, который включен в обновление Platform update 3 (обновление за ноябрь 2016).</span><span class="sxs-lookup"><span data-stu-id="af4b2-119">This hotfix enables attachments to be viewed on the mobile client; this is included in Platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="af4b2-120">Установите исправление KB 3208224.</span><span class="sxs-lookup"><span data-stu-id="af4b2-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="af4b2-121">Код приложения для мобильного приложения утверждения накладных поставщика, которое входит в версию 7.0.1 (май 2016 г.).</span><span class="sxs-lookup"><span data-stu-id="af4b2-121">Application code for the mobile vendor invoice approval application; this is included in version 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="af4b2-122">Устройство Android, iOS или Windows, на которое установлено мобильное приложение.</span><span class="sxs-lookup"><span data-stu-id="af4b2-122">An Android or iOS or a Windows device that has the mobile app installed.</span></span> | <span data-ttu-id="af4b2-123">Найдите приложение в соответствующем магазине приложений.</span><span class="sxs-lookup"><span data-stu-id="af4b2-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="af4b2-124">Введение</span><span class="sxs-lookup"><span data-stu-id="af4b2-124">Introduction</span></span>
<span data-ttu-id="af4b2-125">Для мобильного утверждения накладных поставщика требуются три исправления, описанные в разделе "Необходимые условия".</span><span class="sxs-lookup"><span data-stu-id="af4b2-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="af4b2-126">Эти исправления не предоставляют рабочую область для утверждения накладных.</span><span class="sxs-lookup"><span data-stu-id="af4b2-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="af4b2-127">Чтобы узнать, что рабочая область находится в контексте мобильных устройств, ознакомьтесь с мобильным руководством, которое упомянуто в разделе "Необходимые условия".</span><span class="sxs-lookup"><span data-stu-id="af4b2-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="af4b2-128">Рабочая область утверждения накладных должна быть разработана.</span><span class="sxs-lookup"><span data-stu-id="af4b2-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="af4b2-129">Каждая организация организует и определяет свои бизнес-процессы для накладных поставщиков по-разному.</span><span class="sxs-lookup"><span data-stu-id="af4b2-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="af4b2-130">Прежде чем разрабатывать мобильные возможности для утверждения накладных поставщиков, следует рассмотреть следующие аспекты бизнес-процесса.</span><span class="sxs-lookup"><span data-stu-id="af4b2-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="af4b2-131">Смысл заключается в как можно более полном использовании этих данных для оптимизации работы пользователей на устройстве.</span><span class="sxs-lookup"><span data-stu-id="af4b2-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="af4b2-132">Какие поля из заголовка накладной пользователь захочет видеть на мобильных устройствах и в каком порядке?</span><span class="sxs-lookup"><span data-stu-id="af4b2-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="af4b2-133">Какие поля из строк накладной пользователь захочет видеть на мобильных устройствах и в каком порядке?</span><span class="sxs-lookup"><span data-stu-id="af4b2-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="af4b2-134">Сколько строк накладной содержит накладная?</span><span class="sxs-lookup"><span data-stu-id="af4b2-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="af4b2-135">Применяйте здесь правило 80-20 и оптимизируйте для 80 процентов.</span><span class="sxs-lookup"><span data-stu-id="af4b2-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="af4b2-136">Требуется ли пользователям видеть распределения по бухгалтерским счетам (кодирование накладных) на мобильном устройстве во время проверок?</span><span class="sxs-lookup"><span data-stu-id="af4b2-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="af4b2-137">Если ответ на этот вопрос "Да", рассмотрите следующие вопросы:</span><span class="sxs-lookup"><span data-stu-id="af4b2-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="af4b2-138">Сколько распределений по бухгалтерским счетам (сумма без учета скидок и наценок, налог с продаж, расходы, разбиения и т. д.) имеется в строке накладной?</span><span class="sxs-lookup"><span data-stu-id="af4b2-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="af4b2-139">Опять же, применяйте правило 80-20.</span><span class="sxs-lookup"><span data-stu-id="af4b2-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="af4b2-140">Содержат ли накладные распределения по бухгалтерским счетам также и в заголовке накладной?</span><span class="sxs-lookup"><span data-stu-id="af4b2-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="af4b2-141">Если да, должны ли эти распределения по бухгалтерским счетам были доступны на устройстве?</span><span class="sxs-lookup"><span data-stu-id="af4b2-141">If so, should these accounting distributions be available on the device?</span></span>

    > [!NOTE]
    > <span data-ttu-id="af4b2-142">В этом разделе не объясняется, как изменять распределения по бухгалтерским счетам, поскольку эта функция не поддерживается в настоящее время для мобильных сценариев.</span><span class="sxs-lookup"><span data-stu-id="af4b2-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="af4b2-143">Требуется ли пользователям просматривать вложения для накладной на устройстве?</span><span class="sxs-lookup"><span data-stu-id="af4b2-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="af4b2-144">Разработка мобильной работы для утверждения накладных будет отличаться в зависимости от ответов на эти вопросы.</span><span class="sxs-lookup"><span data-stu-id="af4b2-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="af4b2-145">Целью является оптимизация работы пользователей для бизнес-процесса на мобильным устройстве в организации.</span><span class="sxs-lookup"><span data-stu-id="af4b2-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="af4b2-146">В оставшейся части этого раздела рассмотрим два варианта сценария, которые основаны на разных ответах на предыдущие вопросы.</span><span class="sxs-lookup"><span data-stu-id="af4b2-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="af4b2-147">В качестве общих рекомендаций, при работе с мобильным конструктором обязательно публикуйте изменения во избежание потери обновлений.</span><span class="sxs-lookup"><span data-stu-id="af4b2-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="af4b2-148">Разработка простого сценария утверждения накладных для Contoso</span><span class="sxs-lookup"><span data-stu-id="af4b2-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af4b2-149">Атрибут сценария</span><span class="sxs-lookup"><span data-stu-id="af4b2-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="af4b2-150">Ответ</span><span class="sxs-lookup"><span data-stu-id="af4b2-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="af4b2-151">Какие поля из заголовка накладной пользователь захочет видеть на мобильных устройствах и в каком порядке?</span><span class="sxs-lookup"><span data-stu-id="af4b2-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="af4b2-152">Наименование Поставщика</span><span class="sxs-lookup"><span data-stu-id="af4b2-152">Vendor name</span></span></li>
<li><span data-ttu-id="af4b2-153">Общее количество по накладной</span><span class="sxs-lookup"><span data-stu-id="af4b2-153">Invoice total</span></span></li>
<li><span data-ttu-id="af4b2-154">Счет на</span><span class="sxs-lookup"><span data-stu-id="af4b2-154">Invoice account</span></span></li>
<li><span data-ttu-id="af4b2-155">Номер накладной</span><span class="sxs-lookup"><span data-stu-id="af4b2-155">Invoice number</span></span></li>
<li><span data-ttu-id="af4b2-156">Дата накладной</span><span class="sxs-lookup"><span data-stu-id="af4b2-156">Invoice date</span></span></li>
<li><span data-ttu-id="af4b2-157">Описание накладной</span><span class="sxs-lookup"><span data-stu-id="af4b2-157">Invoice description</span></span></li>
<li><span data-ttu-id="af4b2-158">Срок</span><span class="sxs-lookup"><span data-stu-id="af4b2-158">Due date</span></span></li>
<li><span data-ttu-id="af4b2-159">Валюта накладной</span><span class="sxs-lookup"><span data-stu-id="af4b2-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af4b2-160">Какие поля из строк накладной пользователь захочет видеть на мобильных устройствах и в каком порядке?</span><span class="sxs-lookup"><span data-stu-id="af4b2-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="af4b2-161">Категория закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="af4b2-161">Procurement category</span></span></li>
<li><span data-ttu-id="af4b2-162">Количество</span><span class="sxs-lookup"><span data-stu-id="af4b2-162">Quantity</span></span></li>
<li><span data-ttu-id="af4b2-163">Цена за ед. изм.</span><span class="sxs-lookup"><span data-stu-id="af4b2-163">Unit price</span></span></li>
<li><span data-ttu-id="af4b2-164">Чистая сумма строки</span><span class="sxs-lookup"><span data-stu-id="af4b2-164">Line net amount</span></span></li>
<li><span data-ttu-id="af4b2-165">Сумма по форме 1099</span><span class="sxs-lookup"><span data-stu-id="af4b2-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af4b2-166">Сколько строк накладной содержит накладная?</span><span class="sxs-lookup"><span data-stu-id="af4b2-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="af4b2-167">Применяйте здесь правило 80-20 и оптимизируйте для 80 процентов.</span><span class="sxs-lookup"><span data-stu-id="af4b2-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="af4b2-168">1</span><span class="sxs-lookup"><span data-stu-id="af4b2-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af4b2-169">Требуется ли пользователям видеть распределения по бухгалтерским счетам (кодирование накладных) на мобильном устройстве во время проверок?</span><span class="sxs-lookup"><span data-stu-id="af4b2-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="af4b2-170">Да</span><span class="sxs-lookup"><span data-stu-id="af4b2-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af4b2-171">Сколько распределений по бухгалтерским счетам (сумма без учета скидок и наценок, налог с продаж, расходы и т. д.) имеется в строке накладной?</span><span class="sxs-lookup"><span data-stu-id="af4b2-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="af4b2-172">Опять же, применяйте правило 80-20.</span><span class="sxs-lookup"><span data-stu-id="af4b2-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="af4b2-173">Сумма без учета скидок и наценок: 2 Налог: 0 Расходы: 0</span><span class="sxs-lookup"><span data-stu-id="af4b2-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af4b2-174">Содержат ли накладные распределения по бухгалтерским счетам также и в заголовке накладной?</span><span class="sxs-lookup"><span data-stu-id="af4b2-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="af4b2-175">Если да, должны ли эти распределения по бухгалтерским счетам были доступны на устройстве?</span><span class="sxs-lookup"><span data-stu-id="af4b2-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="af4b2-176">Не используется</span><span class="sxs-lookup"><span data-stu-id="af4b2-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af4b2-177">Требуется ли пользователям просматривать вложения для накладной на устройстве?</span><span class="sxs-lookup"><span data-stu-id="af4b2-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="af4b2-178">Да</span><span class="sxs-lookup"><span data-stu-id="af4b2-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="af4b2-179">Создание рабочей области</span><span class="sxs-lookup"><span data-stu-id="af4b2-179">Create the workspace</span></span>

1.  <span data-ttu-id="af4b2-180">В браузере выполните вход в приложение.</span><span class="sxs-lookup"><span data-stu-id="af4b2-180">In a browser, and sign in to the application.</span></span>
2.  <span data-ttu-id="af4b2-181">После входа добавьте **&mode=mobile** к URL-адресу, как показано в следующем примере, и обновите страницу: https://&lt;ваш_URL&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="af4b2-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="af4b2-182">Нажмите кнопку **Параметры** (шестеренка) в правом верхнем углу страницы, затем нажмите **Мобильное приложение**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="af4b2-183">Должен открыться конструктор мобильного приложения, точно так же, как отображается регистратора задач.</span><span class="sxs-lookup"><span data-stu-id="af4b2-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="af4b2-184">Нажмите **Добавить**, чтобы создать новую рабочую область.</span><span class="sxs-lookup"><span data-stu-id="af4b2-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="af4b2-185">Для этого примера назовите рабочую область **Мои утверждения**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="af4b2-186">Введите описание.</span><span class="sxs-lookup"><span data-stu-id="af4b2-186">Enter a description.</span></span>
6.  <span data-ttu-id="af4b2-187">Выберите цвет рабочей области.</span><span class="sxs-lookup"><span data-stu-id="af4b2-187">Select a workspace color.</span></span> <span data-ttu-id="af4b2-188">Цвет рабочей области будут использоваться для общего стилевого оформления в мобильном устройстве для этой рабочей области.</span><span class="sxs-lookup"><span data-stu-id="af4b2-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="af4b2-189">Выберите значок для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="af4b2-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="af4b2-190">Щелкните **Готово**</span><span class="sxs-lookup"><span data-stu-id="af4b2-190">Click **Done**</span></span>
9.  <span data-ttu-id="af4b2-191">Нажмите **Публикация рабочей области**, чтобы сохранить изменения</span><span class="sxs-lookup"><span data-stu-id="af4b2-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="af4b2-192">Накладные поставщика, назначенные мне</span><span class="sxs-lookup"><span data-stu-id="af4b2-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="af4b2-193">Первая страница мобильных устройств, которую следует разработать — это список накладных, назначенных пользователю для проверки.</span><span class="sxs-lookup"><span data-stu-id="af4b2-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="af4b2-194">Для разработки этой страницы для мобильных устройств используйте страницу **VendMobileInvoiceAssignedToMeListPage**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page.</span></span> <span data-ttu-id="af4b2-195">Прежде чем завершить эту процедуру, убедитесь, что по крайней мере одна накладная поставщика назначена вам для проверки, и что строка накладной содержит не менее двух распределений.</span><span class="sxs-lookup"><span data-stu-id="af4b2-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="af4b2-196">Эта настройка соответствует требованиям для этого сценария.</span><span class="sxs-lookup"><span data-stu-id="af4b2-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="af4b2-197">В URL-адресе измените имя пункта меню на **VendMobileInvoiceAssignedToMeListPage**, чтобы открыть мобильную версию страницы списка **Ожидающие накладные поставщика, назначенные мне** в модуле **Расчеты с поставщиками**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-197">In the URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="af4b2-198">В зависимости от количества накладных, назначенных вам в системе, на этой странице отображаются эти накладные.</span><span class="sxs-lookup"><span data-stu-id="af4b2-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="af4b2-199">Чтобы найти конкретную накладную, используйте расположенный слева фильтр.</span><span class="sxs-lookup"><span data-stu-id="af4b2-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="af4b2-200">Однако для этого примере конкретная накладная не требуется.</span><span class="sxs-lookup"><span data-stu-id="af4b2-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="af4b2-201">Нам просто нужна какая-то накладная, назначенная вам, которая позволяет разрабатывать страницу для мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="af4b2-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="af4b2-202">Новые доступные страницы были специально разработаны для разработки мобильных сценариев для накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="af4b2-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="af4b2-203">Таким образом, необходимо использовать эти страницы.</span><span class="sxs-lookup"><span data-stu-id="af4b2-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="af4b2-204">URL-адрес должен быть похож на следующий URL-адрес, и после его ввода должна открыться страница, которая показана на рисунке: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span><span class="sxs-lookup"><span data-stu-id="af4b2-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span></span> 

    <span data-ttu-id="af4b2-205">[![Страница ожидающих накладных поставщика, назначенных мне](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="af4b2-205">[![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
    
2.  <span data-ttu-id="af4b2-206">Нажмите кнопку **Параметры** (шестеренка) в правом верхнем углу страницы, затем нажмите **Мобильное приложение**</span><span class="sxs-lookup"><span data-stu-id="af4b2-206">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="af4b2-207">Выберите свою рабочую область и нажмите **Изменить**</span><span class="sxs-lookup"><span data-stu-id="af4b2-207">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="af4b2-208">Щелкните **Добавить страницу** для создания первой страницы для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="af4b2-208">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="af4b2-209">Введите имя, например **Мои накладные поставщика**, и описание, например **Накладные поставщика, назначенные мне для проверки**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-209">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="af4b2-210">Щелкните **Готово**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-210">Click **Done**.</span></span>
7.  <span data-ttu-id="af4b2-211">В мобильном конструкторе на вкладке **Поля** нажмите **Выбрать поля**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-211">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="af4b2-212">Столбцы на странице списка должны быть похожи на следующий рисунок.</span><span class="sxs-lookup"><span data-stu-id="af4b2-212">The columns on the list page must resemble the following illustration.</span></span> 

    <span data-ttu-id="af4b2-213">[![Столбцы на странице "Ожидающие накладные поставщика, назначенные мне"](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="af4b2-213">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
    
8.  <span data-ttu-id="af4b2-214">Добавьте необходимые столбцы со страницы списка, которые должны отображаться пользователям на странице мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="af4b2-214">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="af4b2-215">Порядок, в котором добавляются поля, соответствует порядку, в котором поля отображаются для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="af4b2-215">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="af4b2-216">Единственный способ изменить порядок полей — повторно выбрать все поля.</span><span class="sxs-lookup"><span data-stu-id="af4b2-216">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="af4b2-217">На основе требований для этого сценария, нужные следующие восемь полей.</span><span class="sxs-lookup"><span data-stu-id="af4b2-217">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="af4b2-218">Однако некоторые пользователи могут считать, что восемь полей — это слишком большой объем информации для мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="af4b2-218">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="af4b2-219">Поэтому в представлении списка на мобильном устройстве мы будет отображать только самые важные поля.</span><span class="sxs-lookup"><span data-stu-id="af4b2-219">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="af4b2-220">Остальные поля будут отображаться в табличном представлении, который мы разработаем позже.</span><span class="sxs-lookup"><span data-stu-id="af4b2-220">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="af4b2-221">Пока мы добавим следующие поля.</span><span class="sxs-lookup"><span data-stu-id="af4b2-221">For now, we will add the following fields.</span></span> <span data-ttu-id="af4b2-222">Щелкните знак "плюс" (**+**) в этих столбцах, чтобы добавить их на страницу мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="af4b2-222">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="af4b2-223">Наименование Поставщика</span><span class="sxs-lookup"><span data-stu-id="af4b2-223">Vendor name</span></span>
    - <span data-ttu-id="af4b2-224">Общее количество по накладной</span><span class="sxs-lookup"><span data-stu-id="af4b2-224">Invoice total</span></span>
    - <span data-ttu-id="af4b2-225">Счет на</span><span class="sxs-lookup"><span data-stu-id="af4b2-225">Invoice account</span></span>
    - <span data-ttu-id="af4b2-226">Номер накладной</span><span class="sxs-lookup"><span data-stu-id="af4b2-226">Invoice number</span></span>
    - <span data-ttu-id="af4b2-227">Дата накладной</span><span class="sxs-lookup"><span data-stu-id="af4b2-227">Invoice date</span></span>

    <span data-ttu-id="af4b2-228">После добавления этих поля страница мобильных устройств должно быть похожа на страницу на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="af4b2-228">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    
    <span data-ttu-id="af4b2-229">[![Страница после добавления полей](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="af4b2-229">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>

9.  <span data-ttu-id="af4b2-230">Теперь необходимо также добавить следующие столбцы, чтобы впоследствии можно было включить действия workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="af4b2-230">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="af4b2-231">Показать задачу завершения</span><span class="sxs-lookup"><span data-stu-id="af4b2-231">Show complete task</span></span>
    - <span data-ttu-id="af4b2-232">Показать задачу делегирования</span><span class="sxs-lookup"><span data-stu-id="af4b2-232">Show delegate task</span></span>
    - <span data-ttu-id="af4b2-233">Показать задачу отзыва</span><span class="sxs-lookup"><span data-stu-id="af4b2-233">Show recall task</span></span>
    - <span data-ttu-id="af4b2-234">Показать задачу отклонения</span><span class="sxs-lookup"><span data-stu-id="af4b2-234">Show reject task</span></span>
    - <span data-ttu-id="af4b2-235">Показать задачу запроса завершения</span><span class="sxs-lookup"><span data-stu-id="af4b2-235">Show request completion task</span></span>
    - <span data-ttu-id="af4b2-236">Показать задачу повторной отправки</span><span class="sxs-lookup"><span data-stu-id="af4b2-236">Show resubmit task</span></span>

10. <span data-ttu-id="af4b2-237">Щелкните **Готово**, чтобы выйти из режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="af4b2-237">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="af4b2-238">Щелкните **Назад**, а затем **Готово** для выхода из рабочей области</span><span class="sxs-lookup"><span data-stu-id="af4b2-238">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="af4b2-239">Нажмите **Публикация рабочей области**, чтобы сохранить свою работу.</span><span class="sxs-lookup"><span data-stu-id="af4b2-239">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="af4b2-240">Включите **Отображать итог по накладной в списке ожидающих накладных поставщика** в форме параметров расчетов с поставщиками в разделе **Накладная**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-240">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="af4b2-241">Обратите внимание, что только в том случае, если этот параметр включен, итоги по накладным будет рассчитываться для отображения на странице списка ожидающих накладных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="af4b2-241">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="af4b2-242">Это новая возможность в рамках необходимого исправления 3208224.</span><span class="sxs-lookup"><span data-stu-id="af4b2-242">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="af4b2-243">Сведения о накладных поставщика</span><span class="sxs-lookup"><span data-stu-id="af4b2-243">Vendor invoice details</span></span>

<span data-ttu-id="af4b2-244">Для создания страницы сведения о накладной для мобильных устройств используйте страницу **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-244">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="af4b2-245">Обратите внимание, что, в зависимости от количества накладных, которые имеются в системе, на этой странице отображается самая старая накладная (накладная, которая была создана первой).</span><span class="sxs-lookup"><span data-stu-id="af4b2-245">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="af4b2-246">Чтобы найти конкретную накладную, используйте расположенный слева фильтр.</span><span class="sxs-lookup"><span data-stu-id="af4b2-246">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="af4b2-247">Однако для этого примере конкретная накладная не требуется.</span><span class="sxs-lookup"><span data-stu-id="af4b2-247">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="af4b2-248">Нам просто требуются некоторые данные по накладной, чтобы можно было разрабатывать страницу для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="af4b2-248">We just require some invoice data so that we can design the mobile page.</span></span> 

<span data-ttu-id="af4b2-249">[![Страница workflow-процесса](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="af4b2-249">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="af4b2-250">В URL-адресе замените имя пункта меню на **VendMobileInvoiceHeaderDetails**, чтобы открыть форму</span><span class="sxs-lookup"><span data-stu-id="af4b2-250">In the URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>

2. <span data-ttu-id="af4b2-251">Откройте конструктор мобильных устройств с помощью кнопки **Параметры** (шестеренка).</span><span class="sxs-lookup"><span data-stu-id="af4b2-251">Open the mobile designer from the **Settings** (gear) button.</span></span>

3. <span data-ttu-id="af4b2-252">Щелкните кнопку **Изменить** для запуска режима редактирования в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="af4b2-252">Click the **Edit** button to start edit mode in the workspace.</span></span>

4. <span data-ttu-id="af4b2-253">Выберите ранее созданную страницу **Мои накладные поставщика**, затем щелкните **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-253">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>

5. <span data-ttu-id="af4b2-254">На вкладке **Поля** щелкните заголовок столбца **Сетка**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-254">On the **Fields** tab, click the **Grid** column heading.</span></span>

6. <span data-ttu-id="af4b2-255">Щелкните **Свойства &gt; Добавить страницу**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-255">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="af4b2-256">**Примечание.** При нажатии заголовка **Сетка** и добавлении страницы автоматически устанавливается связь со страницей сведений.</span><span class="sxs-lookup"><span data-stu-id="af4b2-256">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>

7. <span data-ttu-id="af4b2-257">Введите заголовок страницы, например **Сведения о накладной**, и описание, например **Просмотр заголовка накладной и сведений о строках**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-257">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>

8. <span data-ttu-id="af4b2-258">Нажмите **Выбор полей**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-258">Click **Select fields**.</span></span> <span data-ttu-id="af4b2-259">Обратите внимание, что порядок, в котором добавляются поля, соответствует порядку, в котором поля отображаются для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="af4b2-259">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="af4b2-260">Единственный способ изменить порядок полей — повторно выбрать все поля.</span><span class="sxs-lookup"><span data-stu-id="af4b2-260">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 

9. <span data-ttu-id="af4b2-261">Добавьте следующие поля из заголовка, на основе требований для этого сценария:</span><span class="sxs-lookup"><span data-stu-id="af4b2-261">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="af4b2-262">Наименование Поставщика</span><span class="sxs-lookup"><span data-stu-id="af4b2-262">Vendor name</span></span>
   - <span data-ttu-id="af4b2-263">Общее количество по накладной</span><span class="sxs-lookup"><span data-stu-id="af4b2-263">Invoice total</span></span>
   - <span data-ttu-id="af4b2-264">Счет на</span><span class="sxs-lookup"><span data-stu-id="af4b2-264">Invoice account</span></span>
   - <span data-ttu-id="af4b2-265">Номер накладной</span><span class="sxs-lookup"><span data-stu-id="af4b2-265">Invoice number</span></span>
   - <span data-ttu-id="af4b2-266">Дата накладной</span><span class="sxs-lookup"><span data-stu-id="af4b2-266">Invoice date</span></span>
   - <span data-ttu-id="af4b2-267">Описание накладной</span><span class="sxs-lookup"><span data-stu-id="af4b2-267">Invoice description</span></span>
   - <span data-ttu-id="af4b2-268">Срок</span><span class="sxs-lookup"><span data-stu-id="af4b2-268">Due date</span></span>
   - <span data-ttu-id="af4b2-269">Валюта накладной</span><span class="sxs-lookup"><span data-stu-id="af4b2-269">Invoice currency</span></span>

10. <span data-ttu-id="af4b2-270">Добавьте следующие поля из сетки строк на странице:</span><span class="sxs-lookup"><span data-stu-id="af4b2-270">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="af4b2-271">Категория закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="af4b2-271">Procurement category</span></span>
    - <span data-ttu-id="af4b2-272">Количество</span><span class="sxs-lookup"><span data-stu-id="af4b2-272">Quantity</span></span>
    - <span data-ttu-id="af4b2-273">Цена за ед. изм.</span><span class="sxs-lookup"><span data-stu-id="af4b2-273">Unit price</span></span>
    - <span data-ttu-id="af4b2-274">Чистая сумма строки</span><span class="sxs-lookup"><span data-stu-id="af4b2-274">Line net amount</span></span>
    - <span data-ttu-id="af4b2-275">Сумма по форме 1099</span><span class="sxs-lookup"><span data-stu-id="af4b2-275">1099 amount</span></span>

11. <span data-ttu-id="af4b2-276">После добавления всех полей из двух предыдущих шагов щелкните **Готово**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-276">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="af4b2-277">Страница должна выглядеть аналогично показанной на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="af4b2-277">The page must resemble the following illustration.</span></span>
    
    <span data-ttu-id="af4b2-278">[![Страница после добавления полей](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="af4b2-278">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>

12. <span data-ttu-id="af4b2-279">Щелкните **Готово**, чтобы выйти из режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="af4b2-279">Click **Done** to exit edit mode.</span></span>

13. <span data-ttu-id="af4b2-280">Щелкните **Назад**, а затем **Готово** для выхода из рабочей области</span><span class="sxs-lookup"><span data-stu-id="af4b2-280">Click **Back** and then **Done** to exit the workspace</span></span>

14. <span data-ttu-id="af4b2-281">Нажмите **Публикация рабочей области**, чтобы сохранить свою работу</span><span class="sxs-lookup"><span data-stu-id="af4b2-281">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="af4b2-282">Действия workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="af4b2-282">Workflow actions</span></span>

<span data-ttu-id="af4b2-283">Для добавления действий рабочего процесса используйте страницу **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-283">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="af4b2-284">Чтобы открыть эту страницу, замените имя пункта меню в URL-адреса, как было сделано ранее.</span><span class="sxs-lookup"><span data-stu-id="af4b2-284">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="af4b2-285">Затем откройте конструктор мобильных устройств с помощью кнопки **Параметры** (шестеренка).</span><span class="sxs-lookup"><span data-stu-id="af4b2-285">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="af4b2-286">Выполните следующие шаги для добавления действий workflow-процесса на странице сведений.</span><span class="sxs-lookup"><span data-stu-id="af4b2-286">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="af4b2-287">Необходимо наличие назначенных вам накладных в соответствующем состоянии, делающим доступными вам действия workflow-процесса, для которых вы собираетесь выполнить разработку.</span><span class="sxs-lookup"><span data-stu-id="af4b2-287">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="af4b2-288">Запись действий workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="af4b2-288">Record workflow actions</span></span>
1.  <span data-ttu-id="af4b2-289">Щелкните кнопку **Изменить** для запуска режима редактирования в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="af4b2-289">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="af4b2-290">Выберите ранее созданную страницу **Сведения о накладной**, затем щелкните **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-290">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="af4b2-291">На вкладке **Действия** нажмите **Добавить действие**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-291">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="af4b2-292">Введите заголовок действия, например **Утвердить**, и описание, например **Утвердить накладную**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-292">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="af4b2-293">Обратите внимание, что введенное здесь название действия становится именем действия, которое отображается для пользователя в мобильном приложении.</span><span class="sxs-lookup"><span data-stu-id="af4b2-293">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="af4b2-294">Щелкните **Готово**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-294">Click **Done**.</span></span>
6.  <span data-ttu-id="af4b2-295">Нажмите **Выбор полей**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-295">Click **Select fields**.</span></span>
7.  <span data-ttu-id="af4b2-296">Выполните workflow-процесс на странице **VendMobileInvoiceHeaderDetails** и выполните действие, которое вы хотите записать.</span><span class="sxs-lookup"><span data-stu-id="af4b2-296">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="af4b2-297">Обязательно введите комментарии workflow-процесса во время этого процесса, чтобы поле комментариев также было доступно пользователям мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="af4b2-297">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="af4b2-298">После выполнения действия workflow-процесса нажмите кнопку **Готово**, чтобы завершить задачу "Выбор полей".</span><span class="sxs-lookup"><span data-stu-id="af4b2-298">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="af4b2-299">Щелкните **Готово**, чтобы выйти из режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="af4b2-299">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="af4b2-300">Щелкните **Назад**, а затем **Готово** для выхода из рабочей области</span><span class="sxs-lookup"><span data-stu-id="af4b2-300">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="af4b2-301">Нажмите **Публикация рабочей области**, чтобы сохранить свою работу</span><span class="sxs-lookup"><span data-stu-id="af4b2-301">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="af4b2-302">Повторите предыдущие шаги для записи всех необходимых действий workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="af4b2-302">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="af4b2-303">Создание JS-файла</span><span class="sxs-lookup"><span data-stu-id="af4b2-303">Create a .js file</span></span>
1. <span data-ttu-id="af4b2-304">Откройте Блокнот или Microsoft Visual Studio и вставьте следующий код.</span><span class="sxs-lookup"><span data-stu-id="af4b2-304">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="af4b2-305">Сохраните файл как файл JS.</span><span class="sxs-lookup"><span data-stu-id="af4b2-305">Save the file as a .js file.</span></span> <span data-ttu-id="af4b2-306">Этот код выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="af4b2-306">This code does the following:</span></span>
    - <span data-ttu-id="af4b2-307">Он скрывает дополнительные столбцы, связанные с workflow-процессом, которые ранее были добавлены на страницу мобильного списка.</span><span class="sxs-lookup"><span data-stu-id="af4b2-307">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="af4b2-308">Мы добавили эти столбцы, чтобы приложение имело эти сведения в контексте и могло выполнить следующий шаг.</span><span class="sxs-lookup"><span data-stu-id="af4b2-308">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="af4b2-309">На основании активного шага бизнес-процесса, он применяет логику для отображения только этих действий.</span><span class="sxs-lookup"><span data-stu-id="af4b2-309">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="af4b2-310">Имена страниц и других элементов управления в коде должны быть такими же, как и в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="af4b2-310">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

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

2.  <span data-ttu-id="af4b2-311">Отправьте файл кода в рабочую область, выбрав вкладку **Логика**</span><span class="sxs-lookup"><span data-stu-id="af4b2-311">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="af4b2-312">Щелкните **Готово**, чтобы выйти из режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="af4b2-312">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="af4b2-313">Щелкните **Назад**, а затем **Готово** для выхода из рабочей области</span><span class="sxs-lookup"><span data-stu-id="af4b2-313">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="af4b2-314">Нажмите **Публикация рабочей области**, чтобы сохранить свою работу</span><span class="sxs-lookup"><span data-stu-id="af4b2-314">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="af4b2-315">Вложения накладной поставщиков</span><span class="sxs-lookup"><span data-stu-id="af4b2-315">Vendor invoice attachments</span></span>

1. <span data-ttu-id="af4b2-316">Нажмите кнопку **Параметры** (шестеренка) в правом верхнем углу страницы, затем нажмите **Мобильное приложение**</span><span class="sxs-lookup"><span data-stu-id="af4b2-316">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>

2. <span data-ttu-id="af4b2-317">Щелкните кнопку **Изменить** для запуска режима редактирования в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="af4b2-317">Click the **Edit** button to start edit mode in the workspace.</span></span>

3. <span data-ttu-id="af4b2-318">Выберите ранее созданную страницу <strong>Сведения о накладной\*\*, затем щелкните \*\*Изменить</strong>.</span><span class="sxs-lookup"><span data-stu-id="af4b2-318">Select the <strong>Invoice details \*\*page that you created earlier, and then click \*\*Edit</strong>.</span></span>

4. <span data-ttu-id="af4b2-319">Задайте для параметра **Управление документами** значение **Да**, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="af4b2-319">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="af4b2-320">**Примечание.** Если не требуется отображать вложения на мобильном устройстве, можно оставить для этого параметра значение **Нет**, что является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="af4b2-320">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   
   ![Управление документами](./media/docmanagement-216x300.png)

5. <span data-ttu-id="af4b2-322">Щелкните **Готово**, чтобы выйти из режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="af4b2-322">Click **Done** to exit edit mode.</span></span>

6. <span data-ttu-id="af4b2-323">Щелкните **Назад**, а затем **Готово** для выхода из рабочей области</span><span class="sxs-lookup"><span data-stu-id="af4b2-323">Click **Back** and then **Done** to exit the workspace</span></span>

7. <span data-ttu-id="af4b2-324">Нажмите **Публикация рабочей области**, чтобы сохранить свою работу</span><span class="sxs-lookup"><span data-stu-id="af4b2-324">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="af4b2-325">Распределения строки накладной поставщика</span><span class="sxs-lookup"><span data-stu-id="af4b2-325">Vendor invoice line distributions</span></span>

<span data-ttu-id="af4b2-326">Требования для данного сценария утверждают, что будет только одно распределение на уровне строки, а накладная всегда будет содержать только одну строку.</span><span class="sxs-lookup"><span data-stu-id="af4b2-326">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="af4b2-327">Поскольку этот сценарий является простым, работа пользователя на мобильном устройстве также должна быть достаточно простой, чтобы пользователю не нужно было переходить через несколько уровней для просмотра распределений.</span><span class="sxs-lookup"><span data-stu-id="af4b2-327">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="af4b2-328">Накладные поставщика включают параметр отображения всех распределений из заголовка накладной.</span><span class="sxs-lookup"><span data-stu-id="af4b2-328">Vendor invoices include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="af4b2-329">Именно это требуется для мобильного сценария.</span><span class="sxs-lookup"><span data-stu-id="af4b2-329">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="af4b2-330">Поэтому мы будет использовать страницу **VendMobileInvoiceAllDistributionTree** для разработки этой части мобильного сценария.</span><span class="sxs-lookup"><span data-stu-id="af4b2-330">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="af4b2-331">Знание требований помогает решить, какую конкретную страницу следует использовать и как именно оптимизировать мобильную работу для пользователя при разработке сценария.</span><span class="sxs-lookup"><span data-stu-id="af4b2-331">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="af4b2-332">Во втором сценарии будет использоваться другая страница для отображения распределений, так как требования для этого сценария отличаются.</span><span class="sxs-lookup"><span data-stu-id="af4b2-332">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="af4b2-333">В URL-адресе замените имя пункта меню, как делали раньше.</span><span class="sxs-lookup"><span data-stu-id="af4b2-333">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="af4b2-334">Страница, которая отображается, должен быть похожа на страницу на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="af4b2-334">The page that appears should resemble the following illustration.</span></span>

    <span data-ttu-id="af4b2-335">[![Страница "Все распределения"](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="af4b2-335">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>

2.  <span data-ttu-id="af4b2-336">Откройте конструктор мобильных устройств с помощью кнопки **Параметры** (шестеренка).</span><span class="sxs-lookup"><span data-stu-id="af4b2-336">Open the mobile designer from the **Settings** (gear) button.</span></span>

3.  <span data-ttu-id="af4b2-337">Щелкните кнопку **Изменить** для запуска режима редактирования в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="af4b2-337">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="af4b2-338">**Примечание.** Вы увидите, что две новые страницы были созданы автоматически.</span><span class="sxs-lookup"><span data-stu-id="af4b2-338">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="af4b2-339">Система создает эти страницы, поскольку вы включили управление документами в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="af4b2-339">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="af4b2-340">Можно игнорировать эти новые страницы.</span><span class="sxs-lookup"><span data-stu-id="af4b2-340">You can ignore these new pages.</span></span>

4.  <span data-ttu-id="af4b2-341">Щелкните **Добавить страницу**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-341">Click **Add page**.</span></span>

5.  <span data-ttu-id="af4b2-342">Введите заголовок страницы, например **Просмотр учета**, и описание, например **Просмотр учета для накладной**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-342">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>

6.  <span data-ttu-id="af4b2-343">Щелкните **Готово**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-343">Click **Done**.</span></span>

7.  <span data-ttu-id="af4b2-344">На вкладке **Поля** щелкните **Выбрать поля**, выберите следующие поля на странице распределений и нажмите кнопку **Готово**:</span><span class="sxs-lookup"><span data-stu-id="af4b2-344">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="af4b2-345">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="af4b2-345">Amount</span></span>
    2.  <span data-ttu-id="af4b2-346">Валютное</span><span class="sxs-lookup"><span data-stu-id="af4b2-346">Currency</span></span>
    3.  <span data-ttu-id="af4b2-347">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="af4b2-347">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="af4b2-348">Мы не выбрали столбец **Описание** в сетке распределений, поскольку требования для данного сценария утверждает, что сумма без учета скидок и наценок — это единственная сумма, для которой будут распределения.</span><span class="sxs-lookup"><span data-stu-id="af4b2-348">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="af4b2-349">Поэтому пользователю не требуется другое поле для определения типа суммы, к которой относится распределение.</span><span class="sxs-lookup"><span data-stu-id="af4b2-349">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="af4b2-350">Однако в следующем сценарии мы **будем** использовать эту информацию, поскольку в требованиях для данного сценария указано, что другие типы сумм имеют распределения (например, налог).</span><span class="sxs-lookup"><span data-stu-id="af4b2-350">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>

8.  <span data-ttu-id="af4b2-351">Щелкните **Готово**, чтобы выйти из режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="af4b2-351">Click **Done** to exit edit mode.</span></span>

9.  <span data-ttu-id="af4b2-352">Щелкните **Назад**, а затем **Готово** для выхода из рабочей области</span><span class="sxs-lookup"><span data-stu-id="af4b2-352">Click **Back** and then **Done** to exit the workspace</span></span>

10. <span data-ttu-id="af4b2-353">Нажмите **Публикация рабочей области**, чтобы сохранить свою работу</span><span class="sxs-lookup"><span data-stu-id="af4b2-353">Click **Publish workspace** to save your work</span></span>

#### <a name="adding-navigation-to-view-accounting-page"></a><span data-ttu-id="af4b2-354">Добавление переходов к странице "Просмотр учета"</span><span class="sxs-lookup"><span data-stu-id="af4b2-354">Adding navigation to "View accounting" page</span></span>

<span data-ttu-id="af4b2-355">Страница для мобильных устройств **Просмотр учета** в настоящее время не привязана ни к каким мобильным страницам, которые мы разработали до этого момента.</span><span class="sxs-lookup"><span data-stu-id="af4b2-355">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="af4b2-356">Так как пользователь должен иметь возможности перехода к странице **Просмотр учета** со страницы **Сведения о накладной** на мобильном устройстве, необходимо предоставить переход со страницы **Сведения о накладной** на страницу **Просмотр учета**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-356">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="af4b2-357">Мы обеспечиваем эту навигацию с помощью дополнительной логики через JavaScript.</span><span class="sxs-lookup"><span data-stu-id="af4b2-357">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="af4b2-358">Откройте JS-файл, созданный ранее, и добавьте строки, выделенные в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="af4b2-358">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="af4b2-359">Этот код выполняет следующие две операции:</span><span class="sxs-lookup"><span data-stu-id="af4b2-359">This code does two things:</span></span>
    1.  <span data-ttu-id="af4b2-360">Он помогает гарантировать, что пользователь не может перейти на страницу **Просмотр учета** непосредственно из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="af4b2-360">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="af4b2-361">Он создает элемент управления переходом со страницы **Сведения о накладной** на страницу **Просмотр учета**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-361">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="af4b2-362">Имена страниц и других элементов управления в коде должны быть такими же, как и в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="af4b2-362">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

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
    
2.  <span data-ttu-id="af4b2-363">Отправьте файл кода в рабочую область, выбрав вкладку **Логика**, чтобы перезаписать предыдущий код</span><span class="sxs-lookup"><span data-stu-id="af4b2-363">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="af4b2-364">Щелкните **Готово**, чтобы выйти из режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="af4b2-364">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="af4b2-365">Щелкните **Назад**, а затем **Готово** для выхода из рабочей области</span><span class="sxs-lookup"><span data-stu-id="af4b2-365">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="af4b2-366">Нажмите **Публикация рабочей области**, чтобы сохранить свою работу</span><span class="sxs-lookup"><span data-stu-id="af4b2-366">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="af4b2-367">Проверка</span><span class="sxs-lookup"><span data-stu-id="af4b2-367">Validation</span></span>

<span data-ttu-id="af4b2-368">Со своего мобильного устройства откройте приложение и подключитесь к своему экземпляру.</span><span class="sxs-lookup"><span data-stu-id="af4b2-368">From your mobile device, open the app, and connect to your instance.</span></span> <span data-ttu-id="af4b2-369">Убедитесь, что вы выполнили вход в компанию, в которой вам назначены накладные поставщика для проверки.</span><span class="sxs-lookup"><span data-stu-id="af4b2-369">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="af4b2-370">Вам должны быть доступны следующие действия:</span><span class="sxs-lookup"><span data-stu-id="af4b2-370">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="af4b2-371">Просмотрите рабочую область **Мои утверждения**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-371">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="af4b2-372">Перейдите в рабочую область **Мои утверждения** и просмотрите страницу **Мои накладные поставщика**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-372">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="af4b2-373">Перейдите на страницу **Мои накладные поставщика** и просмотрите список накладных, которые назначены вам.</span><span class="sxs-lookup"><span data-stu-id="af4b2-373">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="af4b2-374">Перейдите в одну из накладных и просмотрите сведения из заголовка накладной и сведения строки.</span><span class="sxs-lookup"><span data-stu-id="af4b2-374">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="af4b2-375">На странице сведений просмотрите ссылку на вложения и используйте эту ссылку для перехода к списку вложений и просмотра вложений.</span><span class="sxs-lookup"><span data-stu-id="af4b2-375">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="af4b2-376">На странице сведений просмотрите ссылку на страницу **Просмотр учета** и используйте эту ссылку для перехода на страницу распределений и просмотра распределений.</span><span class="sxs-lookup"><span data-stu-id="af4b2-376">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="af4b2-377">На странице сведений щелкните меню **Действия** внизу страницы и выполните действия workflow-процесса, которые относятся к этому шагу workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="af4b2-377">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="af4b2-378">Разработка сложного сценария утверждения накладных для Fabrikam</span><span class="sxs-lookup"><span data-stu-id="af4b2-378">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af4b2-379">Атрибут сценария</span><span class="sxs-lookup"><span data-stu-id="af4b2-379">Scenario attribute</span></span></th>
<th><span data-ttu-id="af4b2-380">Ответ</span><span class="sxs-lookup"><span data-stu-id="af4b2-380">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="af4b2-381">Какие поля из заголовка накладной пользователь захочет видеть на мобильных устройствах и в каком порядке?</span><span class="sxs-lookup"><span data-stu-id="af4b2-381">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="af4b2-382">Наименование Поставщика</span><span class="sxs-lookup"><span data-stu-id="af4b2-382">Vendor name</span></span></li>
<li><span data-ttu-id="af4b2-383">Сумма накладной</span><span class="sxs-lookup"><span data-stu-id="af4b2-383">Invoice amount</span></span></li>
<li><span data-ttu-id="af4b2-384">Счет на</span><span class="sxs-lookup"><span data-stu-id="af4b2-384">Invoice account</span></span></li>
<li><span data-ttu-id="af4b2-385">Номер накладной</span><span class="sxs-lookup"><span data-stu-id="af4b2-385">Invoice number</span></span></li>
<li><span data-ttu-id="af4b2-386">Дата накладной</span><span class="sxs-lookup"><span data-stu-id="af4b2-386">Invoice date</span></span></li>
<li><span data-ttu-id="af4b2-387">Описание накладной</span><span class="sxs-lookup"><span data-stu-id="af4b2-387">Invoice description</span></span></li>
<li><span data-ttu-id="af4b2-388">Срок</span><span class="sxs-lookup"><span data-stu-id="af4b2-388">Due date</span></span></li>
<li><span data-ttu-id="af4b2-389">Валюта накладной</span><span class="sxs-lookup"><span data-stu-id="af4b2-389">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af4b2-390">Какие поля из строк накладной пользователь захочет видеть на мобильных устройствах и в каком порядке?</span><span class="sxs-lookup"><span data-stu-id="af4b2-390">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="af4b2-391">Категория закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="af4b2-391">Procurement category</span></span></li>
<li><span data-ttu-id="af4b2-392">Количество</span><span class="sxs-lookup"><span data-stu-id="af4b2-392">Quantity</span></span></li>
<li><span data-ttu-id="af4b2-393">Цена за ед. изм.</span><span class="sxs-lookup"><span data-stu-id="af4b2-393">Unit price</span></span></li>
<li><span data-ttu-id="af4b2-394">Чистая сумма строки</span><span class="sxs-lookup"><span data-stu-id="af4b2-394">Line net amount</span></span></li>
<li><span data-ttu-id="af4b2-395">Сумма по форме 1099</span><span class="sxs-lookup"><span data-stu-id="af4b2-395">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af4b2-396">Сколько строк накладной содержит накладная?</span><span class="sxs-lookup"><span data-stu-id="af4b2-396">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="af4b2-397">Применяйте здесь правило 80-20 и оптимизируйте для 80 процентов.</span><span class="sxs-lookup"><span data-stu-id="af4b2-397">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="af4b2-398">5</span><span class="sxs-lookup"><span data-stu-id="af4b2-398">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af4b2-399">Требуется ли пользователям видеть распределения по бухгалтерским счетам (кодирование накладных) на мобильном устройстве во время проверок?</span><span class="sxs-lookup"><span data-stu-id="af4b2-399">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="af4b2-400">Да</span><span class="sxs-lookup"><span data-stu-id="af4b2-400">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af4b2-401">Сколько распределений по бухгалтерским счетам (сумма без учета скидок и наценок, налог с продаж, расходы и т. д.) имеется в строке накладной?</span><span class="sxs-lookup"><span data-stu-id="af4b2-401">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="af4b2-402">Опять же, применяйте правило 80-20.</span><span class="sxs-lookup"><span data-stu-id="af4b2-402">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="af4b2-403">Сумма без учета скидок и наценок: 2 Налог: 2 Расходы: 2</span><span class="sxs-lookup"><span data-stu-id="af4b2-403">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af4b2-404">Содержат ли накладные распределения по бухгалтерским счетам также и в заголовке накладной?</span><span class="sxs-lookup"><span data-stu-id="af4b2-404">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="af4b2-405">Если да, должны ли эти распределения по бухгалтерским счетам были доступны на устройстве?</span><span class="sxs-lookup"><span data-stu-id="af4b2-405">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="af4b2-406">Не используется</span><span class="sxs-lookup"><span data-stu-id="af4b2-406">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af4b2-407">Требуется ли пользователям просматривать вложения для накладной на устройстве?</span><span class="sxs-lookup"><span data-stu-id="af4b2-407">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="af4b2-408">Да</span><span class="sxs-lookup"><span data-stu-id="af4b2-408">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="af4b2-409">Далее</span><span class="sxs-lookup"><span data-stu-id="af4b2-409">Next steps</span></span>

<span data-ttu-id="af4b2-410">Можно сделать следующие изменения для сценария 1 в соответствии с требованиями для сценария 2.</span><span class="sxs-lookup"><span data-stu-id="af4b2-410">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="af4b2-411">Этот раздел служит для повышения эффективности работы с мобильными приложениями.</span><span class="sxs-lookup"><span data-stu-id="af4b2-411">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="af4b2-412">Так как в сценарии 2 ожидается больше строк в накладной, следующие изменения в структуре помогут оптимизировать работу пользователей на мобильном устройстве:</span><span class="sxs-lookup"><span data-stu-id="af4b2-412">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="af4b2-413">Вместо просмотра строк накладной на странице сведения (как в сценарии 1), пользователи могут выбрать просмотр строк на отдельной странице мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="af4b2-413">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="af4b2-414">Так как в этом сценарии ожидается более одной строки накладной, если использовать страницу **VendMobileInvoiceAllDistributionTree** при создании страницы распределений для мобильных устройств (как в сценарии 1), пользователю может быть сложно сопоставить строки с распределениями.</span><span class="sxs-lookup"><span data-stu-id="af4b2-414">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="af4b2-415">Поэтому для создания страницы распределений используйте страницу **VendMobileInvoiceLineDistributionTree**.</span><span class="sxs-lookup"><span data-stu-id="af4b2-415">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="af4b2-416">В идеальном случае в этом сценарии распределения должны отображаться в контексте строки накладной.</span><span class="sxs-lookup"><span data-stu-id="af4b2-416">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="af4b2-417">Поэтому убедитесь, что пользователь может перейти в строку для просмотра страницы распределений.</span><span class="sxs-lookup"><span data-stu-id="af4b2-417">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="af4b2-418">Используйте возможность ссылки на страницу для установления детализации, так же, как это было сделано для страниц заголовка и сведений в сценарии 1.</span><span class="sxs-lookup"><span data-stu-id="af4b2-418">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="af4b2-419">Так как в сценарии 2 ожидается более одного типа сумм в распределениях (налог с продаж, расходы и т. д.), будет полезно отобразить описание типа суммы.</span><span class="sxs-lookup"><span data-stu-id="af4b2-419">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="af4b2-420">(Мы опустили эти сведения в сценарии 1.)</span><span class="sxs-lookup"><span data-stu-id="af4b2-420">(We omitted this information in scenario 1.)</span></span>




