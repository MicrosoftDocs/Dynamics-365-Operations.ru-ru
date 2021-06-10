---
title: Процесс обновления
description: Microsoft Dynamics 365 Human Resources — это действительное программное обеспечение как услуга (SaaS), которое обеспечивает непрерывное обновление служб для изменений приложения и платформы.
author: andreabichsel
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2466c53885340991aeeb0a07af83517473b332b6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053643"
---
# <a name="update-process"></a><span data-ttu-id="66aad-103">Процесс обновления</span><span class="sxs-lookup"><span data-stu-id="66aad-103">Update process</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="66aad-104">Microsoft Dynamics 365 Human Resources — это действительное программное обеспечение как услуга (SaaS), которое обеспечивает непрерывное обновление служб.</span><span class="sxs-lookup"><span data-stu-id="66aad-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="66aad-105">Эти обновления содержат как изменения приложений, так и платформ, которые часто обеспечивают важные улучшения службы, в том числе обновления нормативных документов.</span><span class="sxs-lookup"><span data-stu-id="66aad-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="66aad-106">Политика обновления</span><span class="sxs-lookup"><span data-stu-id="66aad-106">Update policy</span></span>

<span data-ttu-id="66aad-107">Обновления выпускаются регулярно для всех сред.</span><span class="sxs-lookup"><span data-stu-id="66aad-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="66aad-108">Human Resources поддерживается в соответствии с [политикой жизненного цикла поддержки Майкрософт](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), которая обеспечивает единообразную и предсказуемую поддержку продукта.</span><span class="sxs-lookup"><span data-stu-id="66aad-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="66aad-109">Ритмичность выпуска</span><span class="sxs-lookup"><span data-stu-id="66aad-109">Release cadence</span></span> 

<span data-ttu-id="66aad-110">Обновления Human Resources автоматически применяются ко всем средам.</span><span class="sxs-lookup"><span data-stu-id="66aad-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="66aad-111">Human Resources предоставляет два типа выпусков:</span><span class="sxs-lookup"><span data-stu-id="66aad-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="66aad-112">**Обновления служб**: обновления выполняются через каждые две недели, которые включают исправления ошибок и новые возможности.</span><span class="sxs-lookup"><span data-stu-id="66aad-112">**Service updates**: Updates occur every two weeks that include bug fixes and new features.</span></span> <span data-ttu-id="66aad-113">Обновления службы также включают применимые обновления платформы при их выпуске.</span><span class="sxs-lookup"><span data-stu-id="66aad-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="66aad-114">Сведения о том, как выпускаются обновления платформы, см. в [Таблица 3: выпуски платформы](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md#table-3-platform-releases).</span><span class="sxs-lookup"><span data-stu-id="66aad-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md#table-3-platform-releases).</span></span> <span data-ttu-id="66aad-115">Осуществляемой раз в две недели обновления имеют поэтапное глобальное развертывание по регионам.</span><span class="sxs-lookup"><span data-stu-id="66aad-115">Biweekly updates have a staged global rollout across regions.</span></span> <span data-ttu-id="66aad-116">Дополнительные сведения об обновлениях раз в две недели см. в разделе [Что нового и что изменилось в Dynamics 365 Human Resources](hr-admin-whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="66aad-116">For more information about biweekly updates, see [What's new or changed in Dynamics 365 Human Resources](hr-admin-whats-new.md).</span></span>

    <span data-ttu-id="66aad-117">Все поддерживаемые центры обработки данных обновляются раз в две недели, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="66aad-117">All supported data centers update every two weeks, unless otherwise noted.</span></span> <span data-ttu-id="66aad-118">Регионы США, Австралия, Европа, Соединенное Королевство, Азия и Канада включены в обновления раз в две недели.</span><span class="sxs-lookup"><span data-stu-id="66aad-118">US, Australia, Europe, UK, Asia, and Canada regions are included in biweekly updates.</span></span> 

- <span data-ttu-id="66aad-119">**Обновления решения Dataverse**: при необходимости эти обновления выполняются примерно каждые шесть недель.</span><span class="sxs-lookup"><span data-stu-id="66aad-119">**Dataverse solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="66aad-120">Они включают в себя новые объекты и изменения существующих объектов в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="66aad-120">They include new entities and changes to existing entities in Dataverse.</span></span> <span data-ttu-id="66aad-121">Эти обновления выпускаются в тех же регионы, что и обновления раз в две недели, и для их репликации по всем центрам данных им требуется около шести недель.</span><span class="sxs-lookup"><span data-stu-id="66aad-121">These updates release to the same regions as the biweekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="66aad-122">Обновления решения могут не соответствовать обновлениям раз в две недели службы.</span><span class="sxs-lookup"><span data-stu-id="66aad-122">Solution updates may or may not align with biweekly service updates.</span></span>

> [!NOTE]
> <span data-ttu-id="66aad-123">Обновления решения доступны во всех центрах обработки данных после их выпуска.</span><span class="sxs-lookup"><span data-stu-id="66aad-123">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="66aad-124">Если вы не ходите ждать автоматической репликации обновлений, можно вручную применить эти обновления к любой среде в любом центре обработки данных.</span><span class="sxs-lookup"><span data-stu-id="66aad-124">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="66aad-125">При необходимости Human Resources также предоставляет следующие типы исправлений:</span><span class="sxs-lookup"><span data-stu-id="66aad-125">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="66aad-126">**Редакция (исправление)**: исправления ошибок, которые могут возникать либо в выпуске, либо отдельно от выпуска обновления служб раз в две недели</span><span class="sxs-lookup"><span data-stu-id="66aad-126">**Revision (hotfix)**: Bug fixes that can occur either with or apart from a biweekly service update release</span></span>

- <span data-ttu-id="66aad-127">**Экстренное исправление**: прогнозные и активные исправления, которые являются самостоятельными, могут включать только изменения конфигурации или кода для решения проблем в масштабе активного узла и могут происходить отдельно от выпуска обновлений служб раз в две недели</span><span class="sxs-lookup"><span data-stu-id="66aad-127">**Emergency fix**: Proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a biweekly service update release</span></span>

<span data-ttu-id="66aad-128">Выпуски анализируются, тестируются и проверяются во внутренней среде.</span><span class="sxs-lookup"><span data-stu-id="66aad-128">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="66aad-129">После завершения построений они разворачиваются в производство.</span><span class="sxs-lookup"><span data-stu-id="66aad-129">After builds are signed off, they're then deployed to production.</span></span>

## <a name="release-cadence-exceptions-in-2021"></a><span data-ttu-id="66aad-130">Исключения из ритмичности выпуска в 2021 г.</span><span class="sxs-lookup"><span data-stu-id="66aad-130">Release cadence exceptions in 2021</span></span>

<span data-ttu-id="66aad-131">Для учета праздников график выпуска для ноября и декабря 2021 выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="66aad-131">To account for holidays, the release schedule for November and December 2021 is as follows:</span></span>

- <span data-ttu-id="66aad-132">Ноябрьский выпуск: 1 ноября –14 ноября</span><span class="sxs-lookup"><span data-stu-id="66aad-132">November release: November 1 - November 14</span></span>
- <span data-ttu-id="66aad-133">Декабрьский выпуск: 29 ноября –12 декабря</span><span class="sxs-lookup"><span data-stu-id="66aad-133">December release: November 29 - December 12</span></span>
 
<span data-ttu-id="66aad-134">Ритмичность в две недели будет возобновлена в обычном порядке 10 января 2022 года.</span><span class="sxs-lookup"><span data-stu-id="66aad-134">The two-week release cadence will resume as usual on January 10, 2022.</span></span>

## <a name="communications"></a><span data-ttu-id="66aad-135">Связь</span><span class="sxs-lookup"><span data-stu-id="66aad-135">Communications</span></span>

<span data-ttu-id="66aad-136">Можно узнать, что есть в работе для модуля Human Resources и что мы сделали в следующих местах:</span><span class="sxs-lookup"><span data-stu-id="66aad-136">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="66aad-137">Дорожная карта Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="66aad-137">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/human-resources/)

- [<span data-ttu-id="66aad-138">Планы выпуска Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="66aad-138">Dynamics 365 Release Plans</span></span>](/dynamics365/release-plans/)

- [<span data-ttu-id="66aad-139">Что нового и что изменилось в Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="66aad-139">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="66aad-140">[Поиск проблем в Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (только для связанных с платформой ошибок)</span><span class="sxs-lookup"><span data-stu-id="66aad-140">[Issue search in Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="66aad-141">Блог Human Resources</span><span class="sxs-lookup"><span data-stu-id="66aad-141">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="66aad-142">Сообщество Human Resources Yammer</span><span class="sxs-lookup"><span data-stu-id="66aad-142">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="66aad-143">Предварительный просмотр функций в среде песочницы</span><span class="sxs-lookup"><span data-stu-id="66aad-143">Preview features in a sandbox environment</span></span>

<span data-ttu-id="66aad-144">Можно проверять функции предварительного просмотра в среде песочницы перед их включением в производственную среду.</span><span class="sxs-lookup"><span data-stu-id="66aad-144">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="66aad-145">Дополнительные сведения об включении функций см. в разделе [Обзор управления функциями](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="66aad-145">For more information about enabling features, see [Feature management overview](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="66aad-146">Все новые возможности остаются в виде предварительного просмотра по крайней мере на 30 дней, а обычно 30-60 дней.</span><span class="sxs-lookup"><span data-stu-id="66aad-146">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="66aad-147">Основные функции обычно доступны в октябре и апрель каждого года, следующего за периодом предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="66aad-147">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="66aad-148">После отображения новых возможностей в рабочей области Управление функциями их можно включить.</span><span class="sxs-lookup"><span data-stu-id="66aad-148">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="66aad-149">Некоторые функции могут быть включены по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="66aad-149">Some features may be on by default.</span></span>

<span data-ttu-id="66aad-150">Время от времени неотъемлемая функция будет включена по умолчанию и не может быть отключена (например, в рабочей области Управление функциями).</span><span class="sxs-lookup"><span data-stu-id="66aad-150">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="66aad-151">Когда функция обычно доступна, она может быть включена или выключена в производственных средах.</span><span class="sxs-lookup"><span data-stu-id="66aad-151">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="66aad-152">Рабочая область Управление функциями показывает, что функция предварительного просмотра станет обязательной.</span><span class="sxs-lookup"><span data-stu-id="66aad-152">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="66aad-153">Эта дата обычно приходится на 1 октября или 1 апреля, чтобы соответствовать полугодовым плановым выпускам.</span><span class="sxs-lookup"><span data-stu-id="66aad-153">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="66aad-154">Вы не можете отключить обязательные функции.</span><span class="sxs-lookup"><span data-stu-id="66aad-154">You can't turn off mandatory features.</span></span> <span data-ttu-id="66aad-155">До тех пор, пока она не станет обязательной, можно включать и выключать функцию во всех средах.</span><span class="sxs-lookup"><span data-stu-id="66aad-155">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="66aad-156">Настоятельно рекомендуется предварительный просмотр функций в песочнице или в испытательной среде.</span><span class="sxs-lookup"><span data-stu-id="66aad-156">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="66aad-157">Лучше всего создать копию текущей производственной среды или базы данных в среде песочницы, чтобы иметь возможность полного создания новых функций с данными.</span><span class="sxs-lookup"><span data-stu-id="66aad-157">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="66aad-158">Дополнительные сведения о подготовке среды песочницы см. в разделе [Подготовка проекта Human Resources](hr-admin-setup-provision.md).</span><span class="sxs-lookup"><span data-stu-id="66aad-158">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="66aad-159">Чтобы удалить тестовую среду, см. раздел [Удаление экземпляра](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span><span class="sxs-lookup"><span data-stu-id="66aad-159">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="66aad-160">Отчет об ошибках</span><span class="sxs-lookup"><span data-stu-id="66aad-160">Report bugs</span></span>

<span data-ttu-id="66aad-161">При проверке функций предварительного просмотра или попытке использовать новые возможности что-то может работать неправильно.</span><span class="sxs-lookup"><span data-stu-id="66aad-161">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="66aad-162">Сообщите об ошибках через [Поддержку Microsoft Dynamics 365](https://dynamics.microsoft.com/support/).</span><span class="sxs-lookup"><span data-stu-id="66aad-162">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="66aad-163">См. также</span><span class="sxs-lookup"><span data-stu-id="66aad-163">See also</span></span>

[<span data-ttu-id="66aad-164">Планы выпусков Dynamics 365 и Power Platform</span><span class="sxs-lookup"><span data-stu-id="66aad-164">Dynamics 365 and Power Platform Release Plans</span></span>](/dynamics365/release-plans)</br>
[<span data-ttu-id="66aad-165">Что нового и что изменилось в Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="66aad-165">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="66aad-166">Политика жизненного цикла программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="66aad-166">Software lifecycle policy</span></span>](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]