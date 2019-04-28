---
title: Утверждения накладных на мобильном устройстве
description: Этот раздел представляет практический подход к разработке мобильных сценариев в Dynamics 365 for Finance and Operations, используя утверждения накладных поставщика для мобильных устройств как вариант использования.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5a48ea7b0c1faf5726de21a246e3d8b4d98f166a
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/25/2019
ms.locfileid: "897186"
---
# <a name="mobile-invoice-approvals"></a><span data-ttu-id="b98fe-103">Утверждения накладных на мобильном устройстве</span><span class="sxs-lookup"><span data-stu-id="b98fe-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b98fe-104">Мобильные возможности в Microsoft Dynamics 365 for Finance and Operations позволяют бизнес-пользователю разрабатывать мобильное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="b98fe-104">Mobile capabilities in Microsoft Dynamics 365 for Finance and Operations let a business user design mobile experiences.</span></span> <span data-ttu-id="b98fe-105">Для более сложных сценариев платформа также позволяет разработчикам расширять возможности при необходимости.</span><span class="sxs-lookup"><span data-stu-id="b98fe-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="b98fe-106">Наиболее эффективный способ познакомиться с некоторыми новыми мобильными концепциями — пройти через процесс разработки нескольких сценариев.</span><span class="sxs-lookup"><span data-stu-id="b98fe-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="b98fe-107">Этот раздел представляет практический подход к разработке мобильных сценариев, используя утверждения накладных поставщика для мобильных устройств как вариант использования.</span><span class="sxs-lookup"><span data-stu-id="b98fe-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="b98fe-108">Этот раздел поможет разрабатывать другие варианты сценариев, а также может применяться к другим сценариям, которые не относятся к накладным поставщиков.</span><span class="sxs-lookup"><span data-stu-id="b98fe-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="b98fe-109">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="b98fe-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="b98fe-110">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="b98fe-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="b98fe-111">описание</span><span class="sxs-lookup"><span data-stu-id="b98fe-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b98fe-112">Предварительно ознакомьтесь с руководством по мобильным приложениям</span><span class="sxs-lookup"><span data-stu-id="b98fe-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="b98fe-113">Мобильная платформа</span><span class="sxs-lookup"><span data-stu-id="b98fe-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="b98fe-114">Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b98fe-114">Dynamics 365 for Finance and Operations</span></span>                                                                             | <span data-ttu-id="b98fe-115">Среда с установленными Microsoft Dynamics 365 for Operations версии 1611 и обновлением платформы 3 Microsoft Dynamics for Operations (ноябрь 2016 г.)</span><span class="sxs-lookup"><span data-stu-id="b98fe-115">An environment that has Microsoft Dynamics 365 for Operations version 1611 and Microsoft Dynamics for Operations platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="b98fe-116">Установите исправление KB 3204341.</span><span class="sxs-lookup"><span data-stu-id="b98fe-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="b98fe-117">Регистратор задач может ошибочно записывать две команды закрытия из раскрывающихся диалоговых окон, которые включены в обновление 3 платформы Dynamics 365 for Operation (обновление за ноябрь 2016)</span><span class="sxs-lookup"><span data-stu-id="b98fe-117">Task recorder can erroneously record two Close commands for dropdown dialogs this is included in Dynamics 365 for Operation platform update 3 (November 2016 update)</span></span> |
| <span data-ttu-id="b98fe-118">Установите исправление KB 3207800.</span><span class="sxs-lookup"><span data-stu-id="b98fe-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="b98fe-119">Это исправление позволяет просматривать вложения на мобильном клиенте, который включен в обновление 3 платформы Dynamics 365 for Operation (обновление за ноябрь 2016).</span><span class="sxs-lookup"><span data-stu-id="b98fe-119">This hotfix enables attachments to be viewed on the mobile client this is included in Dynamics 365 for Operation platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="b98fe-120">Установите исправление KB 3208224.</span><span class="sxs-lookup"><span data-stu-id="b98fe-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="b98fe-121">Код приложения для мобильного приложения утверждения накладных поставщика, которое входит в приложение Microsoft Dynamics AX 7.0.1 (май 2016 г.).</span><span class="sxs-lookup"><span data-stu-id="b98fe-121">Application code for the mobile vendor invoice approval application this is included in Microsoft Dynamics AX application 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="b98fe-122">Устройство Android, iOS или Windows, на которое установлено мобильное приложение для Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b98fe-122">An Android or iOS or a Windows device that has the mobile app installed for Finance and Operations</span></span> | <span data-ttu-id="b98fe-123">Найдите приложение в соответствующем магазине приложений.</span><span class="sxs-lookup"><span data-stu-id="b98fe-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="b98fe-124">Введение</span><span class="sxs-lookup"><span data-stu-id="b98fe-124">Introduction</span></span>
<span data-ttu-id="b98fe-125">Для мобильного утверждения накладных поставщика требуются три исправления, описанные в разделе "Необходимые условия".</span><span class="sxs-lookup"><span data-stu-id="b98fe-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="b98fe-126">Эти исправления не предоставляют рабочую область для утверждения накладных.</span><span class="sxs-lookup"><span data-stu-id="b98fe-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="b98fe-127">Чтобы узнать, что рабочая область находится в контексте мобильных устройств, ознакомьтесь с мобильным руководством, которое упомянуто в разделе "Необходимые условия".</span><span class="sxs-lookup"><span data-stu-id="b98fe-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="b98fe-128">Рабочая область утверждения накладных должна быть разработана.</span><span class="sxs-lookup"><span data-stu-id="b98fe-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="b98fe-129">Каждая организация организует и определяет свои бизнес-процессы для накладных поставщиков по-разному.</span><span class="sxs-lookup"><span data-stu-id="b98fe-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="b98fe-130">Прежде чем разрабатывать мобильные возможности для утверждения накладных поставщиков, следует рассмотреть следующие аспекты бизнес-процесса.</span><span class="sxs-lookup"><span data-stu-id="b98fe-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="b98fe-131">Смысл заключается в как можно более полном использовании этих данных для оптимизации работы пользователей на устройстве.</span><span class="sxs-lookup"><span data-stu-id="b98fe-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="b98fe-132">Какие поля из заголовка накладной пользователь захочет видеть на мобильных устройствах и в каком порядке?</span><span class="sxs-lookup"><span data-stu-id="b98fe-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="b98fe-133">Какие поля из строк накладной пользователь захочет видеть на мобильных устройствах и в каком порядке?</span><span class="sxs-lookup"><span data-stu-id="b98fe-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="b98fe-134">Сколько строк накладной содержит накладная?</span><span class="sxs-lookup"><span data-stu-id="b98fe-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="b98fe-135">Применяйте здесь правило 80-20 и оптимизируйте для 80 процентов.</span><span class="sxs-lookup"><span data-stu-id="b98fe-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="b98fe-136">Требуется ли пользователям видеть распределения по бухгалтерским счетам (кодирование накладных) на мобильном устройстве во время проверок?</span><span class="sxs-lookup"><span data-stu-id="b98fe-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="b98fe-137">Если ответ на этот вопрос "Да", рассмотрите следующие вопросы:</span><span class="sxs-lookup"><span data-stu-id="b98fe-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="b98fe-138">Сколько распределений по бухгалтерским счетам (сумма без учета скидок и наценок, налог с продаж, расходы, разбиения и т. д.) имеется в строке накладной?</span><span class="sxs-lookup"><span data-stu-id="b98fe-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="b98fe-139">Опять же, применяйте правило 80-20.</span><span class="sxs-lookup"><span data-stu-id="b98fe-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="b98fe-140">Содержат ли накладные распределения по бухгалтерским счетам также и в заголовке накладной?</span><span class="sxs-lookup"><span data-stu-id="b98fe-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="b98fe-141">Если да, должны ли эти распределения по бухгалтерским счетам были доступны на устройстве?</span><span class="sxs-lookup"><span data-stu-id="b98fe-141">If so, should these accounting distributions be available on the device?</span></span>

> [!NOTE]
> <span data-ttu-id="b98fe-142">В этом разделе не объясняется, как изменять распределения по бухгалтерским счетам, поскольку эта функция не поддерживается в настоящее время для мобильных сценариев.</span><span class="sxs-lookup"><span data-stu-id="b98fe-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="b98fe-143">Требуется ли пользователям просматривать вложения для накладной на устройстве?</span><span class="sxs-lookup"><span data-stu-id="b98fe-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="b98fe-144">Разработка мобильной работы для утверждения накладных будет отличаться в зависимости от ответов на эти вопросы.</span><span class="sxs-lookup"><span data-stu-id="b98fe-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="b98fe-145">Целью является оптимизация работы пользователей для бизнес-процесса на мобильным устройстве в организации.</span><span class="sxs-lookup"><span data-stu-id="b98fe-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="b98fe-146">В оставшейся части этого раздела рассмотрим два варианта сценария, которые основаны на разных ответах на предыдущие вопросы.</span><span class="sxs-lookup"><span data-stu-id="b98fe-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="b98fe-147">В качестве общих рекомендаций, при работе с мобильным конструктором обязательно публикуйте изменения во избежание потери обновлений.</span><span class="sxs-lookup"><span data-stu-id="b98fe-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="b98fe-148">Разработка простого сценария утверждения накладных для Contoso</span><span class="sxs-lookup"><span data-stu-id="b98fe-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b98fe-149">Атрибут сценария</span><span class="sxs-lookup"><span data-stu-id="b98fe-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="b98fe-150">Ответ</span><span class="sxs-lookup"><span data-stu-id="b98fe-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b98fe-151">Какие поля из заголовка накладной пользователь захочет видеть на мобильных устройствах и в каком порядке?</span><span class="sxs-lookup"><span data-stu-id="b98fe-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="b98fe-152">Наименование Поставщика</span><span class="sxs-lookup"><span data-stu-id="b98fe-152">Vendor name</span></span></li>
<li><span data-ttu-id="b98fe-153">Общее количество по накладной</span><span class="sxs-lookup"><span data-stu-id="b98fe-153">Invoice total</span></span></li>
<li><span data-ttu-id="b98fe-154">Счет на</span><span class="sxs-lookup"><span data-stu-id="b98fe-154">Invoice account</span></span></li>
<li><span data-ttu-id="b98fe-155">Номер накладной</span><span class="sxs-lookup"><span data-stu-id="b98fe-155">Invoice number</span></span></li>
<li><span data-ttu-id="b98fe-156">Дата накладной</span><span class="sxs-lookup"><span data-stu-id="b98fe-156">Invoice date</span></span></li>
<li><span data-ttu-id="b98fe-157">Описание накладной</span><span class="sxs-lookup"><span data-stu-id="b98fe-157">Invoice description</span></span></li>
<li><span data-ttu-id="b98fe-158">Срок</span><span class="sxs-lookup"><span data-stu-id="b98fe-158">Due date</span></span></li>
<li><span data-ttu-id="b98fe-159">Валюта накладной</span><span class="sxs-lookup"><span data-stu-id="b98fe-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b98fe-160">Какие поля из строк накладной пользователь захочет видеть на мобильных устройствах и в каком порядке?</span><span class="sxs-lookup"><span data-stu-id="b98fe-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="b98fe-161">Категория закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="b98fe-161">Procurement category</span></span></li>
<li><span data-ttu-id="b98fe-162">Количество</span><span class="sxs-lookup"><span data-stu-id="b98fe-162">Quantity</span></span></li>
<li><span data-ttu-id="b98fe-163">Цена за ед. изм.</span><span class="sxs-lookup"><span data-stu-id="b98fe-163">Unit price</span></span></li>
<li><span data-ttu-id="b98fe-164">Чистая сумма строки</span><span class="sxs-lookup"><span data-stu-id="b98fe-164">Line net amount</span></span></li>
<li><span data-ttu-id="b98fe-165">Сумма по форме 1099</span><span class="sxs-lookup"><span data-stu-id="b98fe-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b98fe-166">Сколько строк накладной содержит накладная?</span><span class="sxs-lookup"><span data-stu-id="b98fe-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="b98fe-167">Применяйте здесь правило 80-20 и оптимизируйте для 80 процентов.</span><span class="sxs-lookup"><span data-stu-id="b98fe-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="b98fe-168">1</span><span class="sxs-lookup"><span data-stu-id="b98fe-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b98fe-169">Требуется ли пользователям видеть распределения по бухгалтерским счетам (кодирование накладных) на мобильном устройстве во время проверок?</span><span class="sxs-lookup"><span data-stu-id="b98fe-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="b98fe-170">Да</span><span class="sxs-lookup"><span data-stu-id="b98fe-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b98fe-171">Сколько распределений по бухгалтерским счетам (сумма без учета скидок и наценок, налог с продаж, расходы и т. д.) имеется в строке накладной?</span><span class="sxs-lookup"><span data-stu-id="b98fe-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="b98fe-172">Опять же, применяйте правило 80-20.</span><span class="sxs-lookup"><span data-stu-id="b98fe-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="b98fe-173">Сумма без учета скидок и наценок: 2 Налог: 0 Расходы: 0</span><span class="sxs-lookup"><span data-stu-id="b98fe-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b98fe-174">Содержат ли накладные распределения по бухгалтерским счетам также и в заголовке накладной?</span><span class="sxs-lookup"><span data-stu-id="b98fe-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="b98fe-175">Если да, должны ли эти распределения по бухгалтерским счетам были доступны на устройстве?</span><span class="sxs-lookup"><span data-stu-id="b98fe-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="b98fe-176">Не используется</span><span class="sxs-lookup"><span data-stu-id="b98fe-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b98fe-177">Требуется ли пользователям просматривать вложения для накладной на устройстве?</span><span class="sxs-lookup"><span data-stu-id="b98fe-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="b98fe-178">Да</span><span class="sxs-lookup"><span data-stu-id="b98fe-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="b98fe-179">Создание рабочей области</span><span class="sxs-lookup"><span data-stu-id="b98fe-179">Create the workspace</span></span>

1.  <span data-ttu-id="b98fe-180">В браузере откройте Finance and Operations и войдите в систему.</span><span class="sxs-lookup"><span data-stu-id="b98fe-180">In a browser, open Finance and Operations, and sign in.</span></span>
2.  <span data-ttu-id="b98fe-181">После входа добавьте **&mode=mobile** к URL-адресу, как показано в следующем примере, и обновите страницу: https://&lt;ваш_URL&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="b98fe-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="b98fe-182">Нажмите кнопку **Параметры** (шестеренка) в правом верхнем углу страницы, затем нажмите **Мобильное приложение**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="b98fe-183">Должен открыться конструктор мобильного приложения, точно так же, как отображается регистратора задач.</span><span class="sxs-lookup"><span data-stu-id="b98fe-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="b98fe-184">Нажмите **Добавить**, чтобы создать новую рабочую область.</span><span class="sxs-lookup"><span data-stu-id="b98fe-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="b98fe-185">Для этого примера назовите рабочую область **Мои утверждения**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="b98fe-186">Введите описание.</span><span class="sxs-lookup"><span data-stu-id="b98fe-186">Enter a description.</span></span>
6.  <span data-ttu-id="b98fe-187">Выберите цвет рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b98fe-187">Select a workspace color.</span></span> <span data-ttu-id="b98fe-188">Цвет рабочей области будут использоваться для общего стилевого оформления в мобильном устройстве для этой рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b98fe-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="b98fe-189">Выберите значок для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b98fe-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="b98fe-190">Щелкните **Готово**</span><span class="sxs-lookup"><span data-stu-id="b98fe-190">Click **Done**</span></span>
9.  <span data-ttu-id="b98fe-191">Нажмите **Публикация рабочей области**, чтобы сохранить изменения</span><span class="sxs-lookup"><span data-stu-id="b98fe-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="b98fe-192">Накладные поставщика, назначенные мне</span><span class="sxs-lookup"><span data-stu-id="b98fe-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="b98fe-193">Первая страница мобильных устройств, которую следует разработать — это список накладных, назначенных пользователю для проверки.</span><span class="sxs-lookup"><span data-stu-id="b98fe-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="b98fe-194">Для разработки этой страницы для мобильных устройств используйте страницу **VendMobileInvoiceAssignedToMeListPage** в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b98fe-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page in Finance and Operations.</span></span> <span data-ttu-id="b98fe-195">Прежде чем завершить эту процедуру, убедитесь, что по крайней мере одна накладная поставщика назначена вам для проверки, и что строка накладной содержит не менее двух распределений.</span><span class="sxs-lookup"><span data-stu-id="b98fe-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="b98fe-196">Эта настройка соответствует требованиям для этого сценария.</span><span class="sxs-lookup"><span data-stu-id="b98fe-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="b98fe-197">В URL-адресе Finance and Operations измените имя пункта меню на **VendMobileInvoiceAssignedToMeListPage**, чтобы открыть мобильную версию страницы списка **Ожидающие накладные поставщика, назначенные мне** в модуле **Расчеты с поставщиками**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-197">In the Finance and Operations URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="b98fe-198">В зависимости от количества накладных, назначенных вам в системе, на этой странице отображаются эти накладные.</span><span class="sxs-lookup"><span data-stu-id="b98fe-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="b98fe-199">Чтобы найти конкретную накладную, используйте расположенный слева фильтр.</span><span class="sxs-lookup"><span data-stu-id="b98fe-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="b98fe-200">Однако для этого примере конкретная накладная не требуется.</span><span class="sxs-lookup"><span data-stu-id="b98fe-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="b98fe-201">Нам просто нужна какая-то накладная, назначенная вам, которая позволяет разрабатывать страницу для мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="b98fe-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="b98fe-202">Новые доступные страницы были специально разработаны для разработки мобильных сценариев для накладной поставщика.</span><span class="sxs-lookup"><span data-stu-id="b98fe-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="b98fe-203">Таким образом, необходимо использовать эти страницы.</span><span class="sxs-lookup"><span data-stu-id="b98fe-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="b98fe-204">URL-адрес должен быть похож на следующий URL-адрес, и после его ввода должна открыться страница, которая показана на рисунке: https://&lt;ваш_URL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Страница "Ожидающие накладные поставщика, назначенные мне"](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="b98fe-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
2.  <span data-ttu-id="b98fe-205">Нажмите кнопку **Параметры** (шестеренка) в правом верхнем углу страницы, затем нажмите **Мобильное приложение**</span><span class="sxs-lookup"><span data-stu-id="b98fe-205">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="b98fe-206">Выберите свою рабочую область и нажмите **Изменить**</span><span class="sxs-lookup"><span data-stu-id="b98fe-206">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="b98fe-207">Щелкните **Добавить страницу** для создания первой страницы для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="b98fe-207">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="b98fe-208">Введите имя, например **Мои накладные поставщика**, и описание, например **Накладные поставщика, назначенные мне для проверки**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-208">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="b98fe-209">Щелкните **Готово**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-209">Click **Done**.</span></span>
7.  <span data-ttu-id="b98fe-210">В мобильном конструкторе на вкладке **Поля** нажмите **Выбрать поля**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-210">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="b98fe-211">Столбцы на странице списка должны быть похожи на следующий рисунок.</span><span class="sxs-lookup"><span data-stu-id="b98fe-211">The columns on the list page must resemble the following illustration.</span></span> <span data-ttu-id="b98fe-212">[![Столбцы на странице "Ожидающие накладные поставщика, назначенные мне"](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="b98fe-212">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
8.  <span data-ttu-id="b98fe-213">Добавьте необходимые столбцы со страницы списка, которые должны отображаться пользователям на странице мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="b98fe-213">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="b98fe-214">Порядок, в котором добавляются поля, соответствует порядку, в котором поля отображаются для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="b98fe-214">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="b98fe-215">Единственный способ изменить порядок полей — повторно выбрать все поля.</span><span class="sxs-lookup"><span data-stu-id="b98fe-215">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="b98fe-216">На основе требований для этого сценария, нужные следующие восемь полей.</span><span class="sxs-lookup"><span data-stu-id="b98fe-216">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="b98fe-217">Однако некоторые пользователи могут считать, что восемь полей — это слишком большой объем информации для мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="b98fe-217">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="b98fe-218">Поэтому в представлении списка на мобильном устройстве мы будет отображать только самые важные поля.</span><span class="sxs-lookup"><span data-stu-id="b98fe-218">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="b98fe-219">Остальные поля будут отображаться в табличном представлении, который мы разработаем позже.</span><span class="sxs-lookup"><span data-stu-id="b98fe-219">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="b98fe-220">Пока мы добавим следующие поля.</span><span class="sxs-lookup"><span data-stu-id="b98fe-220">For now, we will add the following fields.</span></span> <span data-ttu-id="b98fe-221">Щелкните знак "плюс" (**+**) в этих столбцах, чтобы добавить их на страницу мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="b98fe-221">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="b98fe-222">Наименование Поставщика</span><span class="sxs-lookup"><span data-stu-id="b98fe-222">Vendor name</span></span>
    - <span data-ttu-id="b98fe-223">Общее количество по накладной</span><span class="sxs-lookup"><span data-stu-id="b98fe-223">Invoice total</span></span>
    - <span data-ttu-id="b98fe-224">Счет на</span><span class="sxs-lookup"><span data-stu-id="b98fe-224">Invoice account</span></span>
    - <span data-ttu-id="b98fe-225">Номер накладной</span><span class="sxs-lookup"><span data-stu-id="b98fe-225">Invoice number</span></span>
    - <span data-ttu-id="b98fe-226">Дата накладной</span><span class="sxs-lookup"><span data-stu-id="b98fe-226">Invoice date</span></span>

    <span data-ttu-id="b98fe-227">После добавления этих поля страница мобильных устройств должно быть похожа на страницу на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="b98fe-227">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    <span data-ttu-id="b98fe-228">[![Страница после добавления полей](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="b98fe-228">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>
9.  <span data-ttu-id="b98fe-229">Теперь необходимо также добавить следующие столбцы, чтобы впоследствии можно было включить действия workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="b98fe-229">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="b98fe-230">Показать задачу завершения</span><span class="sxs-lookup"><span data-stu-id="b98fe-230">Show complete task</span></span>
    - <span data-ttu-id="b98fe-231">Показать задачу делегирования</span><span class="sxs-lookup"><span data-stu-id="b98fe-231">Show delegate task</span></span>
    - <span data-ttu-id="b98fe-232">Показать задачу отзыва</span><span class="sxs-lookup"><span data-stu-id="b98fe-232">Show recall task</span></span>
    - <span data-ttu-id="b98fe-233">Показать задачу отклонения</span><span class="sxs-lookup"><span data-stu-id="b98fe-233">Show reject task</span></span>
    - <span data-ttu-id="b98fe-234">Показать задачу запроса завершения</span><span class="sxs-lookup"><span data-stu-id="b98fe-234">Show request completion task</span></span>
    - <span data-ttu-id="b98fe-235">Показать задачу повторной отправки</span><span class="sxs-lookup"><span data-stu-id="b98fe-235">Show resubmit task</span></span>

10. <span data-ttu-id="b98fe-236">Щелкните **Готово**, чтобы выйти из режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="b98fe-236">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="b98fe-237">Щелкните **Назад**, а затем **Готово** для выхода из рабочей области</span><span class="sxs-lookup"><span data-stu-id="b98fe-237">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="b98fe-238">Нажмите **Публикация рабочей области**, чтобы сохранить свою работу.</span><span class="sxs-lookup"><span data-stu-id="b98fe-238">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="b98fe-239">Включите **Отображать итог по накладной в списке ожидающих накладных поставщика** в форме параметров расчетов с поставщиками в разделе **Накладная**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-239">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="b98fe-240">Обратите внимание, что только в том случае, если этот параметр включен, итоги по накладным будет рассчитываться для отображения на странице списка ожидающих накладных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="b98fe-240">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="b98fe-241">Это новая возможность в рамках необходимого исправления 3208224.</span><span class="sxs-lookup"><span data-stu-id="b98fe-241">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="b98fe-242">Сведения о накладных поставщика</span><span class="sxs-lookup"><span data-stu-id="b98fe-242">Vendor invoice details</span></span>

<span data-ttu-id="b98fe-243">Для создания страницы сведения о накладной для мобильных устройств используйте страницу **VendMobileInvoiceHeaderDetails** в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b98fe-243">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page in Finance and Operations.</span></span> <span data-ttu-id="b98fe-244">Обратите внимание, что, в зависимости от количества накладных, которые имеются в системе, на этой странице отображается самая старая накладная (накладная, которая была создана первой).</span><span class="sxs-lookup"><span data-stu-id="b98fe-244">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="b98fe-245">Чтобы найти конкретную накладную, используйте расположенный слева фильтр.</span><span class="sxs-lookup"><span data-stu-id="b98fe-245">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="b98fe-246">Однако для этого примере конкретная накладная не требуется.</span><span class="sxs-lookup"><span data-stu-id="b98fe-246">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="b98fe-247">Нам просто требуются некоторые данные по накладной, чтобы можно было разрабатывать страницу для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="b98fe-247">We just require some invoice data so that we can design the mobile page.</span></span> <span data-ttu-id="b98fe-248">[![Страница workflow-процесса](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="b98fe-248">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="b98fe-249">В URL-адресе Finance and Operations замените имя пункта меню на **VendMobileInvoiceHeaderDetails**, чтобы открыть форму</span><span class="sxs-lookup"><span data-stu-id="b98fe-249">In the Finance and Operations URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>
2. <span data-ttu-id="b98fe-250">Откройте конструктор мобильных устройств с помощью кнопки **Параметры** (шестеренка).</span><span class="sxs-lookup"><span data-stu-id="b98fe-250">Open the mobile designer from the **Settings** (gear) button.</span></span>
3. <span data-ttu-id="b98fe-251">Щелкните кнопку **Изменить** для запуска режима редактирования в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b98fe-251">Click the **Edit** button to start edit mode in the workspace.</span></span>
4. <span data-ttu-id="b98fe-252">Выберите ранее созданную страницу **Мои накладные поставщика**, затем щелкните **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-252">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>
5. <span data-ttu-id="b98fe-253">На вкладке **Поля** щелкните заголовок столбца **Сетка**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-253">On the **Fields** tab, click the **Grid** column heading.</span></span>
6. <span data-ttu-id="b98fe-254">Щелкните **Свойства &gt; Добавить страницу**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-254">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="b98fe-255">**Примечание.** При нажатии заголовка **Сетка** и добавлении страницы автоматически устанавливается связь со страницей сведений.</span><span class="sxs-lookup"><span data-stu-id="b98fe-255">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>
7. <span data-ttu-id="b98fe-256">Введите заголовок страницы, например **Сведения о накладной**, и описание, например **Просмотр заголовка накладной и сведений о строках**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-256">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>
8. <span data-ttu-id="b98fe-257">Нажмите **Выбор полей**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-257">Click **Select fields**.</span></span> <span data-ttu-id="b98fe-258">Обратите внимание, что порядок, в котором добавляются поля, соответствует порядку, в котором поля отображаются для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="b98fe-258">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="b98fe-259">Единственный способ изменить порядок полей — повторно выбрать все поля.</span><span class="sxs-lookup"><span data-stu-id="b98fe-259">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 
9. <span data-ttu-id="b98fe-260">Добавьте следующие поля из заголовка, на основе требований для этого сценария:</span><span class="sxs-lookup"><span data-stu-id="b98fe-260">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="b98fe-261">Наименование Поставщика</span><span class="sxs-lookup"><span data-stu-id="b98fe-261">Vendor name</span></span>
   - <span data-ttu-id="b98fe-262">Общее количество по накладной</span><span class="sxs-lookup"><span data-stu-id="b98fe-262">Invoice total</span></span>
   - <span data-ttu-id="b98fe-263">Счет на</span><span class="sxs-lookup"><span data-stu-id="b98fe-263">Invoice account</span></span>
   - <span data-ttu-id="b98fe-264">Номер накладной</span><span class="sxs-lookup"><span data-stu-id="b98fe-264">Invoice number</span></span>
   - <span data-ttu-id="b98fe-265">Дата накладной</span><span class="sxs-lookup"><span data-stu-id="b98fe-265">Invoice date</span></span>
   - <span data-ttu-id="b98fe-266">Описание накладной</span><span class="sxs-lookup"><span data-stu-id="b98fe-266">Invoice description</span></span>
   - <span data-ttu-id="b98fe-267">Срок</span><span class="sxs-lookup"><span data-stu-id="b98fe-267">Due date</span></span>
   - <span data-ttu-id="b98fe-268">Валюта накладной</span><span class="sxs-lookup"><span data-stu-id="b98fe-268">Invoice currency</span></span>

10. <span data-ttu-id="b98fe-269">Добавьте следующие поля из сетки строк на странице:</span><span class="sxs-lookup"><span data-stu-id="b98fe-269">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="b98fe-270">Категория закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="b98fe-270">Procurement category</span></span>
    - <span data-ttu-id="b98fe-271">Количество</span><span class="sxs-lookup"><span data-stu-id="b98fe-271">Quantity</span></span>
    - <span data-ttu-id="b98fe-272">Цена за ед. изм.</span><span class="sxs-lookup"><span data-stu-id="b98fe-272">Unit price</span></span>
    - <span data-ttu-id="b98fe-273">Чистая сумма строки</span><span class="sxs-lookup"><span data-stu-id="b98fe-273">Line net amount</span></span>
    - <span data-ttu-id="b98fe-274">Сумма по форме 1099</span><span class="sxs-lookup"><span data-stu-id="b98fe-274">1099 amount</span></span>

11. <span data-ttu-id="b98fe-275">После добавления всех полей из двух предыдущих шагов щелкните **Готово**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-275">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="b98fe-276">Страница должна выглядеть аналогично показанной на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="b98fe-276">The page must resemble the following illustration.</span></span>
    <span data-ttu-id="b98fe-277">[![Страница после добавления полей](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="b98fe-277">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>
12. <span data-ttu-id="b98fe-278">Щелкните **Готово**, чтобы выйти из режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="b98fe-278">Click **Done** to exit edit mode.</span></span>
13. <span data-ttu-id="b98fe-279">Щелкните **Назад**, а затем **Готово** для выхода из рабочей области</span><span class="sxs-lookup"><span data-stu-id="b98fe-279">Click **Back** and then **Done** to exit the workspace</span></span>
14. <span data-ttu-id="b98fe-280">Нажмите **Публикация рабочей области**, чтобы сохранить свою работу</span><span class="sxs-lookup"><span data-stu-id="b98fe-280">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="b98fe-281">Действия workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="b98fe-281">Workflow actions</span></span>

<span data-ttu-id="b98fe-282">Чтобы добавить действия workflow-процесса, используйте страницу **VendMobileInvoiceHeaderDetails** в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b98fe-282">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page in Finance and Operations.</span></span> <span data-ttu-id="b98fe-283">Чтобы открыть эту страницу, замените имя пункта меню в URL-адреса, как было сделано ранее.</span><span class="sxs-lookup"><span data-stu-id="b98fe-283">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="b98fe-284">Затем откройте конструктор мобильных устройств с помощью кнопки **Параметры** (шестеренка).</span><span class="sxs-lookup"><span data-stu-id="b98fe-284">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="b98fe-285">Выполните следующие шаги для добавления действий workflow-процесса на странице сведений.</span><span class="sxs-lookup"><span data-stu-id="b98fe-285">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="b98fe-286">Необходимо наличие назначенных вам накладных в соответствующем состоянии, делающим доступными вам действия workflow-процесса, для которых вы собираетесь выполнить разработку.</span><span class="sxs-lookup"><span data-stu-id="b98fe-286">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="b98fe-287">Запись действий workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="b98fe-287">Record workflow actions</span></span>
1.  <span data-ttu-id="b98fe-288">Щелкните кнопку **Изменить** для запуска режима редактирования в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b98fe-288">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="b98fe-289">Выберите ранее созданную страницу **Сведения о накладной**, затем щелкните **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-289">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="b98fe-290">На вкладке **Действия** нажмите **Добавить действие**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-290">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="b98fe-291">Введите заголовок действия, например **Утвердить**, и описание, например **Утвердить накладную**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-291">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="b98fe-292">Обратите внимание, что введенное здесь название действия становится именем действия, которое отображается для пользователя в мобильном приложении.</span><span class="sxs-lookup"><span data-stu-id="b98fe-292">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="b98fe-293">Щелкните **Готово**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-293">Click **Done**.</span></span>
6.  <span data-ttu-id="b98fe-294">Нажмите **Выбор полей**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-294">Click **Select fields**.</span></span>
7.  <span data-ttu-id="b98fe-295">Выполните workflow-процесс на странице **VendMobileInvoiceHeaderDetails** и выполните действие, которое вы хотите записать.</span><span class="sxs-lookup"><span data-stu-id="b98fe-295">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="b98fe-296">Обязательно введите комментарии workflow-процесса во время этого процесса, чтобы поле комментариев также было доступно пользователям мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="b98fe-296">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="b98fe-297">После выполнения действия workflow-процесса нажмите кнопку **Готово**, чтобы завершить задачу "Выбор полей".</span><span class="sxs-lookup"><span data-stu-id="b98fe-297">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="b98fe-298">Щелкните **Готово**, чтобы выйти из режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="b98fe-298">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="b98fe-299">Щелкните **Назад**, а затем **Готово** для выхода из рабочей области</span><span class="sxs-lookup"><span data-stu-id="b98fe-299">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="b98fe-300">Нажмите **Публикация рабочей области**, чтобы сохранить свою работу</span><span class="sxs-lookup"><span data-stu-id="b98fe-300">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="b98fe-301">Повторите предыдущие шаги для записи всех необходимых действий workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="b98fe-301">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="b98fe-302">Создание JS-файла</span><span class="sxs-lookup"><span data-stu-id="b98fe-302">Create a .js file</span></span>
1. <span data-ttu-id="b98fe-303">Откройте Блокнот или Microsoft Visual Studio и вставьте следующий код.</span><span class="sxs-lookup"><span data-stu-id="b98fe-303">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="b98fe-304">Сохраните файл как файл JS.</span><span class="sxs-lookup"><span data-stu-id="b98fe-304">Save the file as a .js file.</span></span> <span data-ttu-id="b98fe-305">Этот код выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b98fe-305">This code does the following:</span></span>
    - <span data-ttu-id="b98fe-306">Он скрывает дополнительные столбцы, связанные с workflow-процессом, которые ранее были добавлены на страницу мобильного списка.</span><span class="sxs-lookup"><span data-stu-id="b98fe-306">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="b98fe-307">Мы добавили эти столбцы, чтобы приложение имело эти сведения в контексте и могло выполнить следующий шаг.</span><span class="sxs-lookup"><span data-stu-id="b98fe-307">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="b98fe-308">На основании активного шага бизнес-процесса, он применяет логику для отображения только этих действий.</span><span class="sxs-lookup"><span data-stu-id="b98fe-308">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

> [!NOTE]
> <span data-ttu-id="b98fe-309">Имена страниц и других элементов управления в коде должны быть такими же, как и в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b98fe-309">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

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

2.  <span data-ttu-id="b98fe-310">Отправьте файл кода в рабочую область, выбрав вкладку **Логика**</span><span class="sxs-lookup"><span data-stu-id="b98fe-310">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="b98fe-311">Щелкните **Готово**, чтобы выйти из режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="b98fe-311">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="b98fe-312">Щелкните **Назад**, а затем **Готово** для выхода из рабочей области</span><span class="sxs-lookup"><span data-stu-id="b98fe-312">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="b98fe-313">Нажмите **Публикация рабочей области**, чтобы сохранить свою работу</span><span class="sxs-lookup"><span data-stu-id="b98fe-313">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="b98fe-314">Вложения накладной поставщиков</span><span class="sxs-lookup"><span data-stu-id="b98fe-314">Vendor invoice attachments</span></span>

1. <span data-ttu-id="b98fe-315">Нажмите кнопку **Параметры** (шестеренка) в правом верхнем углу страницы, затем нажмите **Мобильное приложение**</span><span class="sxs-lookup"><span data-stu-id="b98fe-315">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
2. <span data-ttu-id="b98fe-316">Щелкните кнопку **Изменить** для запуска режима редактирования в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b98fe-316">Click the **Edit** button to start edit mode in the workspace.</span></span>
3. <span data-ttu-id="b98fe-317">Выберите ранее созданную страницу <strong>Сведения о накладной\*\*, затем щелкните \*\*Изменить</strong>.</span><span class="sxs-lookup"><span data-stu-id="b98fe-317">Select the <strong>Invoice details \*\*page that you created earlier, and then click \*\*Edit</strong>.</span></span>
4. <span data-ttu-id="b98fe-318">Задайте для параметра **Управление документами** значение **Да**, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="b98fe-318">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="b98fe-319">**Примечание.** Если не требуется отображать вложения на мобильном устройстве, можно оставить для этого параметра значение **Нет**, что является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b98fe-319">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   <span data-ttu-id="b98fe-320">![Управление документами](./media/docmanagement-216x300.png)</span><span class="sxs-lookup"><span data-stu-id="b98fe-320">![Document management](./media/docmanagement-216x300.png)</span></span>
5. <span data-ttu-id="b98fe-321">Щелкните **Готово**, чтобы выйти из режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="b98fe-321">Click **Done** to exit edit mode.</span></span>
6. <span data-ttu-id="b98fe-322">Щелкните **Назад**, а затем **Готово** для выхода из рабочей области</span><span class="sxs-lookup"><span data-stu-id="b98fe-322">Click **Back** and then **Done** to exit the workspace</span></span>
7. <span data-ttu-id="b98fe-323">Нажмите **Публикация рабочей области**, чтобы сохранить свою работу</span><span class="sxs-lookup"><span data-stu-id="b98fe-323">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="b98fe-324">Распределения строки накладной поставщика</span><span class="sxs-lookup"><span data-stu-id="b98fe-324">Vendor invoice line distributions</span></span>

<span data-ttu-id="b98fe-325">Требования для данного сценария утверждают, что будет только одно распределение на уровне строки, а накладная всегда будет содержать только одну строку.</span><span class="sxs-lookup"><span data-stu-id="b98fe-325">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="b98fe-326">Поскольку этот сценарий является простым, работа пользователя на мобильном устройстве также должна быть достаточно простой, чтобы пользователю не нужно было переходить через несколько уровней для просмотра распределений.</span><span class="sxs-lookup"><span data-stu-id="b98fe-326">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="b98fe-327">Накладные поставщика в Finance and Operations включают параметр отображения всех распределений из заголовка накладной.</span><span class="sxs-lookup"><span data-stu-id="b98fe-327">Vendor invoices in Finance and Operations include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="b98fe-328">Именно это требуется для мобильного сценария.</span><span class="sxs-lookup"><span data-stu-id="b98fe-328">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="b98fe-329">Поэтому мы будет использовать страницу **VendMobileInvoiceAllDistributionTree** для разработки этой части мобильного сценария.</span><span class="sxs-lookup"><span data-stu-id="b98fe-329">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="b98fe-330">Знание требований помогает решить, какую конкретную страницу следует использовать и как именно оптимизировать мобильную работу для пользователя при разработке сценария.</span><span class="sxs-lookup"><span data-stu-id="b98fe-330">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="b98fe-331">Во втором сценарии будет использоваться другая страница для отображения распределений, так как требования для этого сценария отличаются.</span><span class="sxs-lookup"><span data-stu-id="b98fe-331">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="b98fe-332">В URL-адресе замените имя пункта меню, как делали раньше.</span><span class="sxs-lookup"><span data-stu-id="b98fe-332">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="b98fe-333">Страница, которая отображается, должен быть похожа на страницу на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="b98fe-333">The page that appears should resemble the following illustration.</span></span>
<span data-ttu-id="b98fe-334">[![Страница "Все распределения"](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="b98fe-334">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>
2.  <span data-ttu-id="b98fe-335">Откройте конструктор мобильных устройств с помощью кнопки **Параметры** (шестеренка).</span><span class="sxs-lookup"><span data-stu-id="b98fe-335">Open the mobile designer from the **Settings** (gear) button.</span></span>
3.  <span data-ttu-id="b98fe-336">Щелкните кнопку **Изменить** для запуска режима редактирования в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b98fe-336">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="b98fe-337">**Примечание.** Вы увидите, что две новые страницы были созданы автоматически.</span><span class="sxs-lookup"><span data-stu-id="b98fe-337">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="b98fe-338">Система создает эти страницы, поскольку вы включили управление документами в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="b98fe-338">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="b98fe-339">Можно игнорировать эти новые страницы.</span><span class="sxs-lookup"><span data-stu-id="b98fe-339">You can ignore these new pages.</span></span>
4.  <span data-ttu-id="b98fe-340">Щелкните **Добавить страницу**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-340">Click **Add page**.</span></span>
5.  <span data-ttu-id="b98fe-341">Введите заголовок страницы, например **Просмотр учета**, и описание, например **Просмотр учета для накладной**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-341">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>
6.  <span data-ttu-id="b98fe-342">Щелкните **Готово**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-342">Click **Done**.</span></span>
7.  <span data-ttu-id="b98fe-343">На вкладке **Поля** щелкните **Выбрать поля**, выберите следующие поля на странице распределений и нажмите кнопку **Готово**:</span><span class="sxs-lookup"><span data-stu-id="b98fe-343">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="b98fe-344">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="b98fe-344">Amount</span></span>
    2.  <span data-ttu-id="b98fe-345">Валютное</span><span class="sxs-lookup"><span data-stu-id="b98fe-345">Currency</span></span>
    3.  <span data-ttu-id="b98fe-346">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="b98fe-346">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="b98fe-347">Мы не выбрали столбец **Описание** в сетке распределений, поскольку требования для данного сценария утверждает, что сумма без учета скидок и наценок — это единственная сумма, для которой будут распределения.</span><span class="sxs-lookup"><span data-stu-id="b98fe-347">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="b98fe-348">Поэтому пользователю не требуется другое поле для определения типа суммы, к которой относится распределение.</span><span class="sxs-lookup"><span data-stu-id="b98fe-348">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="b98fe-349">Однако в следующем сценарии мы **будем** использовать эту информацию, поскольку в требованиях для данного сценария указано, что другие типы сумм имеют распределения (например, налог).</span><span class="sxs-lookup"><span data-stu-id="b98fe-349">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>
8.  <span data-ttu-id="b98fe-350">Щелкните **Готово**, чтобы выйти из режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="b98fe-350">Click **Done** to exit edit mode.</span></span>
9.  <span data-ttu-id="b98fe-351">Щелкните **Назад**, а затем **Готово** для выхода из рабочей области</span><span class="sxs-lookup"><span data-stu-id="b98fe-351">Click **Back** and then **Done** to exit the workspace</span></span>
10. <span data-ttu-id="b98fe-352">Нажмите **Публикация рабочей области**, чтобы сохранить свою работу</span><span class="sxs-lookup"><span data-stu-id="b98fe-352">Click **Publish workspace** to save your work</span></span>

> [!NOTE] 
> <span data-ttu-id="b98fe-353">Страница для мобильных устройств **Просмотр учета** в настоящее время не привязана ни к каким мобильным страницам, которые мы разработали до этого момента.</span><span class="sxs-lookup"><span data-stu-id="b98fe-353">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="b98fe-354">Так как пользователь должен иметь возможности перехода к странице **Просмотр учета** со страницы **Сведения о накладной** на мобильном устройстве, необходимо предоставить переход со страницы **Сведения о накладной** на страницу **Просмотр учета**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-354">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="b98fe-355">Мы обеспечиваем эту навигацию с помощью дополнительной логики через JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b98fe-355">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="b98fe-356">Откройте JS-файл, созданный ранее, и добавьте строки, выделенные в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="b98fe-356">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="b98fe-357">Этот код выполняет следующие две операции:</span><span class="sxs-lookup"><span data-stu-id="b98fe-357">This code does two things:</span></span>
    1.  <span data-ttu-id="b98fe-358">Он помогает гарантировать, что пользователь не может перейти на страницу **Просмотр учета** непосредственно из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b98fe-358">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="b98fe-359">Он создает элемент управления переходом со страницы **Сведения о накладной** на страницу **Просмотр учета**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-359">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

> [!NOTE] 
> <span data-ttu-id="b98fe-360">Имена страниц и других элементов управления в коде должны быть такими же, как и в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b98fe-360">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

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

2.  <span data-ttu-id="b98fe-361">Отправьте файл кода в рабочую область, выбрав вкладку **Логика**, чтобы перезаписать предыдущий код</span><span class="sxs-lookup"><span data-stu-id="b98fe-361">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="b98fe-362">Щелкните **Готово**, чтобы выйти из режима редактирования.</span><span class="sxs-lookup"><span data-stu-id="b98fe-362">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="b98fe-363">Щелкните **Назад**, а затем **Готово** для выхода из рабочей области</span><span class="sxs-lookup"><span data-stu-id="b98fe-363">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="b98fe-364">Нажмите **Публикация рабочей области**, чтобы сохранить свою работу</span><span class="sxs-lookup"><span data-stu-id="b98fe-364">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="b98fe-365">Проверка</span><span class="sxs-lookup"><span data-stu-id="b98fe-365">Validation</span></span>

<span data-ttu-id="b98fe-366">Со своего мобильного устройства откройте приложение и подключитесь к своему экземпляру Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b98fe-366">From your mobile device, open the app, and connect to your Finance and Operations instance.</span></span> <span data-ttu-id="b98fe-367">Убедитесь, что вы выполнили вход в компанию, в которой вам назначены накладные поставщика для проверки.</span><span class="sxs-lookup"><span data-stu-id="b98fe-367">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="b98fe-368">Вам должны быть доступны следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b98fe-368">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="b98fe-369">Просмотрите рабочую область **Мои утверждения**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-369">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="b98fe-370">Перейдите в рабочую область **Мои утверждения** и просмотрите страницу **Мои накладные поставщика**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-370">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="b98fe-371">Перейдите на страницу **Мои накладные поставщика** и просмотрите список накладных, которые назначены вам.</span><span class="sxs-lookup"><span data-stu-id="b98fe-371">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="b98fe-372">Перейдите в одну из накладных и просмотрите сведения из заголовка накладной и сведения строки.</span><span class="sxs-lookup"><span data-stu-id="b98fe-372">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="b98fe-373">На странице сведений просмотрите ссылку на вложения и используйте эту ссылку для перехода к списку вложений и просмотра вложений.</span><span class="sxs-lookup"><span data-stu-id="b98fe-373">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="b98fe-374">На странице сведений просмотрите ссылку на страницу **Просмотр учета** и используйте эту ссылку для перехода на страницу распределений и просмотра распределений.</span><span class="sxs-lookup"><span data-stu-id="b98fe-374">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="b98fe-375">На странице сведений щелкните меню **Действия** внизу страницы и выполните действия workflow-процесса, которые относятся к этому шагу workflow-процесса.</span><span class="sxs-lookup"><span data-stu-id="b98fe-375">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="b98fe-376">Разработка сложного сценария утверждения накладных для Fabrikam</span><span class="sxs-lookup"><span data-stu-id="b98fe-376">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b98fe-377">Атрибут сценария</span><span class="sxs-lookup"><span data-stu-id="b98fe-377">Scenario attribute</span></span></th>
<th><span data-ttu-id="b98fe-378">Ответ</span><span class="sxs-lookup"><span data-stu-id="b98fe-378">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b98fe-379">Какие поля из заголовка накладной пользователь захочет видеть на мобильных устройствах и в каком порядке?</span><span class="sxs-lookup"><span data-stu-id="b98fe-379">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="b98fe-380">Наименование Поставщика</span><span class="sxs-lookup"><span data-stu-id="b98fe-380">Vendor name</span></span></li>
<li><span data-ttu-id="b98fe-381">Сумма накладной</span><span class="sxs-lookup"><span data-stu-id="b98fe-381">Invoice amount</span></span></li>
<li><span data-ttu-id="b98fe-382">Счет на</span><span class="sxs-lookup"><span data-stu-id="b98fe-382">Invoice account</span></span></li>
<li><span data-ttu-id="b98fe-383">Номер накладной</span><span class="sxs-lookup"><span data-stu-id="b98fe-383">Invoice number</span></span></li>
<li><span data-ttu-id="b98fe-384">Дата накладной</span><span class="sxs-lookup"><span data-stu-id="b98fe-384">Invoice date</span></span></li>
<li><span data-ttu-id="b98fe-385">Описание накладной</span><span class="sxs-lookup"><span data-stu-id="b98fe-385">Invoice description</span></span></li>
<li><span data-ttu-id="b98fe-386">Срок</span><span class="sxs-lookup"><span data-stu-id="b98fe-386">Due date</span></span></li>
<li><span data-ttu-id="b98fe-387">Валюта накладной</span><span class="sxs-lookup"><span data-stu-id="b98fe-387">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b98fe-388">Какие поля из строк накладной пользователь захочет видеть на мобильных устройствах и в каком порядке?</span><span class="sxs-lookup"><span data-stu-id="b98fe-388">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="b98fe-389">Категория закупаемой продукции</span><span class="sxs-lookup"><span data-stu-id="b98fe-389">Procurement category</span></span></li>
<li><span data-ttu-id="b98fe-390">Количество</span><span class="sxs-lookup"><span data-stu-id="b98fe-390">Quantity</span></span></li>
<li><span data-ttu-id="b98fe-391">Цена за ед. изм.</span><span class="sxs-lookup"><span data-stu-id="b98fe-391">Unit price</span></span></li>
<li><span data-ttu-id="b98fe-392">Чистая сумма строки</span><span class="sxs-lookup"><span data-stu-id="b98fe-392">Line net amount</span></span></li>
<li><span data-ttu-id="b98fe-393">Сумма по форме 1099</span><span class="sxs-lookup"><span data-stu-id="b98fe-393">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b98fe-394">Сколько строк накладной содержит накладная?</span><span class="sxs-lookup"><span data-stu-id="b98fe-394">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="b98fe-395">Применяйте здесь правило 80-20 и оптимизируйте для 80 процентов.</span><span class="sxs-lookup"><span data-stu-id="b98fe-395">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="b98fe-396">5</span><span class="sxs-lookup"><span data-stu-id="b98fe-396">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b98fe-397">Требуется ли пользователям видеть распределения по бухгалтерским счетам (кодирование накладных) на мобильном устройстве во время проверок?</span><span class="sxs-lookup"><span data-stu-id="b98fe-397">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="b98fe-398">Да</span><span class="sxs-lookup"><span data-stu-id="b98fe-398">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b98fe-399">Сколько распределений по бухгалтерским счетам (сумма без учета скидок и наценок, налог с продаж, расходы и т. д.) имеется в строке накладной?</span><span class="sxs-lookup"><span data-stu-id="b98fe-399">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="b98fe-400">Опять же, применяйте правило 80-20.</span><span class="sxs-lookup"><span data-stu-id="b98fe-400">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="b98fe-401">Сумма без учета скидок и наценок: 2 Налог: 2 Расходы: 2</span><span class="sxs-lookup"><span data-stu-id="b98fe-401">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b98fe-402">Содержат ли накладные распределения по бухгалтерским счетам также и в заголовке накладной?</span><span class="sxs-lookup"><span data-stu-id="b98fe-402">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="b98fe-403">Если да, должны ли эти распределения по бухгалтерским счетам были доступны на устройстве?</span><span class="sxs-lookup"><span data-stu-id="b98fe-403">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="b98fe-404">Не используется</span><span class="sxs-lookup"><span data-stu-id="b98fe-404">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b98fe-405">Требуется ли пользователям просматривать вложения для накладной на устройстве?</span><span class="sxs-lookup"><span data-stu-id="b98fe-405">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="b98fe-406">Да</span><span class="sxs-lookup"><span data-stu-id="b98fe-406">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="b98fe-407">Далее</span><span class="sxs-lookup"><span data-stu-id="b98fe-407">Next steps</span></span>

<span data-ttu-id="b98fe-408">Можно сделать следующие изменения для сценария 1 в соответствии с требованиями для сценария 2.</span><span class="sxs-lookup"><span data-stu-id="b98fe-408">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="b98fe-409">Этот раздел служит для повышения эффективности работы с мобильными приложениями.</span><span class="sxs-lookup"><span data-stu-id="b98fe-409">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="b98fe-410">Так как в сценарии 2 ожидается больше строк в накладной, следующие изменения в структуре помогут оптимизировать работу пользователей на мобильном устройстве:</span><span class="sxs-lookup"><span data-stu-id="b98fe-410">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="b98fe-411">Вместо просмотра строк накладной на странице сведения (как в сценарии 1), пользователи могут выбрать просмотр строк на отдельной странице мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="b98fe-411">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="b98fe-412">Так как в этом сценарии ожидается более одной строки накладной, если использовать страницу **VendMobileInvoiceAllDistributionTree** при создании страницы распределений для мобильных устройств (как в сценарии 1), пользователю может быть сложно сопоставить строки с распределениями.</span><span class="sxs-lookup"><span data-stu-id="b98fe-412">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="b98fe-413">Поэтому для создания страницы распределений используйте страницу **VendMobileInvoiceLineDistributionTree**.</span><span class="sxs-lookup"><span data-stu-id="b98fe-413">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="b98fe-414">В идеальном случае в этом сценарии распределения должны отображаться в контексте строки накладной.</span><span class="sxs-lookup"><span data-stu-id="b98fe-414">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="b98fe-415">Поэтому убедитесь, что пользователь может перейти в строку для просмотра страницы распределений.</span><span class="sxs-lookup"><span data-stu-id="b98fe-415">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="b98fe-416">Используйте возможность ссылки на страницу для установления детализации, так же, как это было сделано для страниц заголовка и сведений в сценарии 1.</span><span class="sxs-lookup"><span data-stu-id="b98fe-416">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="b98fe-417">Так как в сценарии 2 ожидается более одного типа сумм в распределениях (налог с продаж, расходы и т. д.), будет полезно отобразить описание типа суммы.</span><span class="sxs-lookup"><span data-stu-id="b98fe-417">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="b98fe-418">(Мы опустили эти сведения в сценарии 1.)</span><span class="sxs-lookup"><span data-stu-id="b98fe-418">(We omitted this information in scenario 1.)</span></span>




