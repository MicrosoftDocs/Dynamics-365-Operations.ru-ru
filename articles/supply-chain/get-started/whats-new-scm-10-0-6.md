---
title: Что нового и что изменилось в Dynamics 365 Supply Chain Management 10.0.6 (ноябрь 2019 г.)
description: В этой теме описываются новые и измененные компоненты Dynamics 365 Supply Chain Management 10.0.6.
author: josaw1
manager: tfehr
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: f253355b3de4f148c11b1d9d3f43b6756e6bd38c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983683"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a><span data-ttu-id="04608-103">Что нового и что изменилось в Dynamics 365 Supply Chain Management 10.0.6 (ноябрь 2019 г.)</span><span class="sxs-lookup"><span data-stu-id="04608-103">What's new or changed in Dynamics 365 Supply Chain Management 10.0.6 (November 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04608-104">В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span><span class="sxs-lookup"><span data-stu-id="04608-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span></span> <span data-ttu-id="04608-105">Эта версия имеет номер сборки 10.0.234.</span><span class="sxs-lookup"><span data-stu-id="04608-105">This version has a build number of 10.0.234.</span></span> <span data-ttu-id="04608-106">Хотя общая дата доступности находится в ноябре, новые функции доступны для раннего выпуска в октябре.</span><span class="sxs-lookup"><span data-stu-id="04608-106">While the general availability date is in November, the new features are available for early release in October.</span></span> <span data-ttu-id="04608-107">Дополнительные сведения о версии 10.0.6 см. в разделе [Дополнительные ресурсы](whats-new-scm-10-0-6.md#additional-resources).</span><span class="sxs-lookup"><span data-stu-id="04608-107">For more information about version 10.0.6, see [Additional resources](whats-new-scm-10-0-6.md#additional-resources).</span></span>

## <a name="product-configuration-models-v2-data-entity"></a><span data-ttu-id="04608-108">Информационный объект моделей конфигурации продукта версии 2</span><span class="sxs-lookup"><span data-stu-id="04608-108">Product configuration models V2 data entity</span></span>

<span data-ttu-id="04608-109">Вторая версии для информационного объекта "модели конфигурации продукта" выпускается (называется "модели конфигурации продуктов версии 2").</span><span class="sxs-lookup"><span data-stu-id="04608-109">A second version for the "product configuration models" data entity is released (called "products configuration models V2").</span></span> <span data-ttu-id="04608-110">Шаблон по умолчанию "418 — модели конфигурации продукта" также должен быть, так как он использует новый информационный объект "модели конфигурации продукта версии 2" в шаблонах структуры импорта/экспорта.</span><span class="sxs-lookup"><span data-stu-id="04608-110">The default template "418-product configuration models" is also needs to be so that it uses the new "product configuration models V2" data entity in the import/export framework templates.</span></span> <span data-ttu-id="04608-111">Шаблон не будет автоматически обновляться, так что потребуется загрузить шаблон по умолчанию вручную.</span><span class="sxs-lookup"><span data-stu-id="04608-111">The template will not be auto-updated so that you will have to load the template from the default manually.</span></span> <span data-ttu-id="04608-112">Объект версии 2 экспортирует одну строку как отдельный файл во вложение, а не в виде встроенного файла, что устраняет ограничения размера у объекта версии 1.</span><span class="sxs-lookup"><span data-stu-id="04608-112">The V2 entity exports one row as separate file in an attachment instead of inline, solving the size limitations of the V1 entity.</span></span> 
 
<span data-ttu-id="04608-113">Что необходимо сделать, чтобы принять это изменение?</span><span class="sxs-lookup"><span data-stu-id="04608-113">What do you need to do to take this change?</span></span>
-    <span data-ttu-id="04608-114">Поскольку сущность версии 1 устарела, следует начать переход с версии 1 на версию 2.</span><span class="sxs-lookup"><span data-stu-id="04608-114">As the V1 entity has been deprecated, you should start migrating from V1 to V2.</span></span> <span data-ttu-id="04608-115">При использовании шаблона "418 — модели конфигурации продукта" можно нажать кнопку "загрузить шаблоны по умолчанию" и перезагрузить шаблон "418 — модели конфигурации продукта"</span><span class="sxs-lookup"><span data-stu-id="04608-115">If you are using the  "418-product configuration models" template, you can click on "load default templates" button and reload the template "418 – product configuration models"</span></span>
-    <span data-ttu-id="04608-116">Если необходимо обеспечить совместимость с существующими системами, можно сейчас продолжить работу с существующим шаблоном и (устаревшим) объектом версии 1 до переноса интеграций в новый шаблон.</span><span class="sxs-lookup"><span data-stu-id="04608-116">If you need to keep compatibility with existing systems, you can for now continue using the existing template and the (deprecated) V1 entity until you move your integrations to the new template.</span></span> 

## <a name="feature-management-enhancements"></a><span data-ttu-id="04608-117">Улучшения управления функциями</span><span class="sxs-lookup"><span data-stu-id="04608-117">Feature management enhancements</span></span>
<span data-ttu-id="04608-118">Теперь управление функциями позволяет включить все новые возможности по умолчанию, требовать подтверждения включения функции и включить все функции, которые еще не были включены.</span><span class="sxs-lookup"><span data-stu-id="04608-118">Feature management now allows you to enable all new features by default, require confirmation to enable a feature, and enable all features that have not already been enabled.</span></span> 


## <a name="purchase-agreement-responsible-party"></a><span data-ttu-id="04608-119">Ответственный субъект договора покупки</span><span class="sxs-lookup"><span data-stu-id="04608-119">Purchase agreement responsible party</span></span>
<span data-ttu-id="04608-120">Теперь имеется возможность определить основных и дополнительных ответственных лиц в форме классификации договоров покупки и полученных в результате договорах покупки.</span><span class="sxs-lookup"><span data-stu-id="04608-120">You now have the ability to define primary and secondary responsible parties on the Purchase agreement classification form and resulting Purchase agreements.</span></span>  <span data-ttu-id="04608-121">Это предоставляет пользователю доступ к тем, кто контролирует договора.</span><span class="sxs-lookup"><span data-stu-id="04608-121">This provides the user access to who oversees the agreements.</span></span>

## <a name="rfq-link-on-the-purchase-order-line"></a><span data-ttu-id="04608-122">Скидка запроса предложения в строке заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="04608-122">RFQ link on the Purchase order line</span></span>
<span data-ttu-id="04608-123">Можно добавить справочную ссылку из строк заказа на покупку назад в соответствующие строки запроса предложения, из которых они созданы, что позволяет пользователю легко получить доступ к соответствующему документу запроса предложения.</span><span class="sxs-lookup"><span data-stu-id="04608-123">You can add a reference link from the Purchase order lines back to the corresponding RFQ lines they originated from, allowing the user to easily be provided with the supporting request for quotation document.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="04608-124">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="04608-124">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="04608-125">Исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="04608-125">Bug fixes</span></span>
<span data-ttu-id="04608-126">Для получения сведений об исправлениях ошибок, включенных в каждое из обновлений, которые являются частью 10.0.6, войдите в службы Lifecycle Services (LCS) и просмотрите [статью базы знаний](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span><span class="sxs-lookup"><span data-stu-id="04608-126">For information about the bug fixes included in each of the updates that are part of 10.0.6, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span></span>

### <a name="platform-update-30"></a><span data-ttu-id="04608-127">Обновление платформы update 30</span><span class="sxs-lookup"><span data-stu-id="04608-127">Platform update 30</span></span>
<span data-ttu-id="04608-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 включает обновление платформы Platform update 30.</span><span class="sxs-lookup"><span data-stu-id="04608-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 includes Platform update 30.</span></span> <span data-ttu-id="04608-129">Дополнительные сведения об обновлении платформы Platform update 30 см. в разделе [Что нового и что изменилось в обновлении платформы Platform update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span><span class="sxs-lookup"><span data-stu-id="04608-129">To learn more about Platform update 30, see [What's new or changed in Platform update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span></span>

### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="04608-130">Dynamics 365: план выпуска волны 2 за 2019 год</span><span class="sxs-lookup"><span data-stu-id="04608-130">Dynamics 365: 2019 release wave 2 plan</span></span>
<span data-ttu-id="04608-131">Интересуетесь предстоящими и недавно выпущенными возможностями наших бизнес-приложений и платформ?</span><span class="sxs-lookup"><span data-stu-id="04608-131">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="04608-132">Ознакомьтесь с разделом [Dynamics 365: план выпуска волны 2 за 2019 год](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span><span class="sxs-lookup"><span data-stu-id="04608-132">Check out the [Dynamics 365: 2019 release wave 2 plan](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span></span> <span data-ttu-id="04608-133">Мы собрали в одном документе все сведения, чтобы вы могли использовать их для планирования.</span><span class="sxs-lookup"><span data-stu-id="04608-133">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-supply-chain-management-features"></a><span data-ttu-id="04608-134">Удаленные и устаревшие функции Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="04608-134">Removed and deprecated Supply Chain Management features</span></span>

<span data-ttu-id="04608-135">В теме [Удаленные или устаревшие функции в Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) описываются функции, которые запланированы к удалению или которые планируется удалить или объявить устаревшими для Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="04608-135">The [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic describes features that have been or are scheduled to be removed or deprecated for Supply Chain Management.</span></span>

- <span data-ttu-id="04608-136">*Удаленная* функция больше недоступна в продукте.</span><span class="sxs-lookup"><span data-stu-id="04608-136">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="04608-137">*Устаревшая* функция не находится в активной разработке и может быть удалена в следующем обновлении.</span><span class="sxs-lookup"><span data-stu-id="04608-137">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="04608-138">Перед удалением каких-либо функций из продукта уведомление об устаревании будет объявлено в теме [Удаленные или устаревшие функции в Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) за 12 месяцев до удаления.</span><span class="sxs-lookup"><span data-stu-id="04608-138">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="04608-139">Для критических изменений, которые влияют только на время компиляции, но являются двоично совместимыми с песочницей и производственными средами, время устаревания будет меньше 12 месяцев.</span><span class="sxs-lookup"><span data-stu-id="04608-139">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="04608-140">Обычно это функциональные обновления, которые должны быть выполнены для компилятора.</span><span class="sxs-lookup"><span data-stu-id="04608-140">Typically, these are functional updates that need to be made to the compiler.</span></span>
