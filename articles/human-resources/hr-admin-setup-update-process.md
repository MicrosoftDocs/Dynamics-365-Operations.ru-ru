---
title: Процесс обновления
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1817e072805bafbf0d5a9eb2698ef75abc75ad68
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/07/2020
ms.locfileid: "3031098"
---
# <a name="update-process"></a><span data-ttu-id="56fcc-102">Процесс обновления</span><span class="sxs-lookup"><span data-stu-id="56fcc-102">Update process</span></span>

<span data-ttu-id="56fcc-103">Microsoft Dynamics 365 Human Resources — это действительное программное обеспечение как услуга (SaaS), которое обеспечивает непрерывное обновление служб.</span><span class="sxs-lookup"><span data-stu-id="56fcc-103">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="56fcc-104">Эти обновления содержат как изменения приложений, так и платформ, которые часто обеспечивают важные улучшения службы, в том числе обновления нормативных документов.</span><span class="sxs-lookup"><span data-stu-id="56fcc-104">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="56fcc-105">Политика обновления</span><span class="sxs-lookup"><span data-stu-id="56fcc-105">Update policy</span></span>

<span data-ttu-id="56fcc-106">Обновления выпускаются регулярно для всех сред.</span><span class="sxs-lookup"><span data-stu-id="56fcc-106">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="56fcc-107">Human Resources поддерживается в соответствии с [политикой жизненного цикла поддержки Майкрософт](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), которая обеспечивает единообразную и предсказуемую поддержку продукта.</span><span class="sxs-lookup"><span data-stu-id="56fcc-107">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="56fcc-108">Ритмичность выпуска</span><span class="sxs-lookup"><span data-stu-id="56fcc-108">Release cadence</span></span>

<span data-ttu-id="56fcc-109">Обновления Human Resources автоматически применяются ко всем средам.</span><span class="sxs-lookup"><span data-stu-id="56fcc-109">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="56fcc-110">Human Resources предоставляет два типа выпусков:</span><span class="sxs-lookup"><span data-stu-id="56fcc-110">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="56fcc-111">**Обновления служб**: еженедельные обновления, которые включают исправления ошибок и новые возможности.</span><span class="sxs-lookup"><span data-stu-id="56fcc-111">**Service updates**: Weekly updates that include bug fixes and new features.</span></span> <span data-ttu-id="56fcc-112">Обновления службы также включают применимые обновления платформы при их выпуске.</span><span class="sxs-lookup"><span data-stu-id="56fcc-112">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="56fcc-113">Сведения о том, как выпускаются обновления платформы, см. в [Таблица 3: выпуски платформы](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span><span class="sxs-lookup"><span data-stu-id="56fcc-113">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="56fcc-114">Еженедельные обновления обычно выпускаются по средам.</span><span class="sxs-lookup"><span data-stu-id="56fcc-114">Weekly updates usually release on Wednesdays.</span></span> <span data-ttu-id="56fcc-115">Дополнительные сведения о еженедельных выпусках см. в разделе [Что нового и что изменилось в Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).</span><span class="sxs-lookup"><span data-stu-id="56fcc-115">For more information about weekly updates, see [What's new or changed in Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).</span></span>

    <span data-ttu-id="56fcc-116">Все поддерживаемые центры обработки данных обновляются еженедельно, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="56fcc-116">All supported data centers update weekly, unless otherwise noted.</span></span> <span data-ttu-id="56fcc-117">Еженедельное обновление обычно начинается в среду и завершается к воскресенью.</span><span class="sxs-lookup"><span data-stu-id="56fcc-117">Weekly updates typically begin on Wednesday and complete by Sunday.</span></span> <span data-ttu-id="56fcc-118">Регионы США, Австралия, Европа, Великобритания, Азия и Канада включены в еженедельные обновления.</span><span class="sxs-lookup"><span data-stu-id="56fcc-118">US, Australia, Europe, UK, Asia, and Canada regions are included in weekly updates.</span></span> 

- <span data-ttu-id="56fcc-119">**Обновления решения Common Data Service**: при необходимости эти обновления выполняются примерно каждые шесть недель.</span><span class="sxs-lookup"><span data-stu-id="56fcc-119">**Common Data Service solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="56fcc-120">Они включают в себя новые объекты и изменения существующих объектов в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="56fcc-120">They include new entities and changes to existing entities in Common Data Service.</span></span> <span data-ttu-id="56fcc-121">Эти обновления выпускаются в тех же регионы, что и еженедельные обновления, и для их репликации по всем центрам данных им требуется около шести недель.</span><span class="sxs-lookup"><span data-stu-id="56fcc-121">These updates release to the same regions as the weekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="56fcc-122">Обновления решения могут не соответствовать еженедельным обновлениям службы.</span><span class="sxs-lookup"><span data-stu-id="56fcc-122">Solution updates may or may not align with weekly service updates.</span></span>

<span data-ttu-id="56fcc-123">В следующей таблице показан примерный график:</span><span class="sxs-lookup"><span data-stu-id="56fcc-123">The following table shows a sample schedule:</span></span>

| <span data-ttu-id="56fcc-124">Неделя</span><span class="sxs-lookup"><span data-stu-id="56fcc-124">Week</span></span> | <span data-ttu-id="56fcc-125">Тип обновления</span><span class="sxs-lookup"><span data-stu-id="56fcc-125">Update type</span></span> |
| --- | --- |
| <span data-ttu-id="56fcc-126">1</span><span class="sxs-lookup"><span data-stu-id="56fcc-126">1</span></span> | <span data-ttu-id="56fcc-127">Обновление служб (все регионы)</span><span class="sxs-lookup"><span data-stu-id="56fcc-127">Service update (all regions)</span></span> |
| <span data-ttu-id="56fcc-128">2</span><span class="sxs-lookup"><span data-stu-id="56fcc-128">2</span></span> | <span data-ttu-id="56fcc-129">Обновление служб (все регионы) + обновление решения (регионы недели 1)</span><span class="sxs-lookup"><span data-stu-id="56fcc-129">Service update (all regions) + Solution update (Week 1 regions)</span></span> |
| <span data-ttu-id="56fcc-130">3</span><span class="sxs-lookup"><span data-stu-id="56fcc-130">3</span></span> | <span data-ttu-id="56fcc-131">Обновление служб (все регионы) + обновление решения (регионы недели 2)</span><span class="sxs-lookup"><span data-stu-id="56fcc-131">Service update (all regions) + Solution update (Week 2 regions)</span></span> |
| <span data-ttu-id="56fcc-132">4</span><span class="sxs-lookup"><span data-stu-id="56fcc-132">4</span></span> | <span data-ttu-id="56fcc-133">Обновление служб (все регионы) + обновление решения (регионы недели 3)</span><span class="sxs-lookup"><span data-stu-id="56fcc-133">Service update (all regions) + Solution update (Week 3 regions)</span></span> |
| <span data-ttu-id="56fcc-134">5</span><span class="sxs-lookup"><span data-stu-id="56fcc-134">5</span></span> | <span data-ttu-id="56fcc-135">Обновление служб (все регионы) + обновление решения (регионы недели 4)</span><span class="sxs-lookup"><span data-stu-id="56fcc-135">Service update (all regions) + Solution update (Week 4 regions)</span></span> |
| <span data-ttu-id="56fcc-136">6</span><span class="sxs-lookup"><span data-stu-id="56fcc-136">6</span></span> | <span data-ttu-id="56fcc-137">Обновление служб (все регионы) + обновление решения (регионы недели 5)</span><span class="sxs-lookup"><span data-stu-id="56fcc-137">Service update (all regions) + Solution update (Week 5 regions)</span></span> |
| <span data-ttu-id="56fcc-138">7</span><span class="sxs-lookup"><span data-stu-id="56fcc-138">7</span></span> | <span data-ttu-id="56fcc-139">Обновление служб (все регионы) + обновление решения (регионы недели 6)</span><span class="sxs-lookup"><span data-stu-id="56fcc-139">Service update (all regions) + Solution update (Week 6 regions)</span></span> |
| <span data-ttu-id="56fcc-140">8</span><span class="sxs-lookup"><span data-stu-id="56fcc-140">8</span></span> | <span data-ttu-id="56fcc-141">Обновление служб (все регионы)</span><span class="sxs-lookup"><span data-stu-id="56fcc-141">Service update (all regions)</span></span> |

> [!NOTE]
> <span data-ttu-id="56fcc-142">Обновления решения доступны во всех центрах обработки данных после их выпуска.</span><span class="sxs-lookup"><span data-stu-id="56fcc-142">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="56fcc-143">Если вы не ходите ждать автоматической репликации обновлений, можно вручную применить эти обновления к любой среде в любом центре обработки данных.</span><span class="sxs-lookup"><span data-stu-id="56fcc-143">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="56fcc-144">При необходимости Human Resources также предоставляет следующие типы исправлений:</span><span class="sxs-lookup"><span data-stu-id="56fcc-144">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="56fcc-145">**Редакция (исправление)**: исправления ошибок, которые могут возникать либо в выпуске, либо отдельно от выпуска еженедельного обновления служб</span><span class="sxs-lookup"><span data-stu-id="56fcc-145">**Revision (hotfix)**: bug fixes that can occur either with or apart from a weekly service update release</span></span>

- <span data-ttu-id="56fcc-146">**Экстренное исправление**: прогнозные и активные исправления, которые являются самостоятельными, могут включать только изменения конфигурации или кода для решения проблем в масштабе активного узла и могут происходить отдельно от еженедельного выпуска обновлений служб</span><span class="sxs-lookup"><span data-stu-id="56fcc-146">**Emergency fix**: proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a weekly service update release</span></span>

<span data-ttu-id="56fcc-147">Выпуски анализируются, тестируются и проверяются во внутренней среде.</span><span class="sxs-lookup"><span data-stu-id="56fcc-147">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="56fcc-148">После завершения построений они разворачиваются в производство.</span><span class="sxs-lookup"><span data-stu-id="56fcc-148">After builds are signed off, they're then deployed to production.</span></span>

## <a name="exceptions-in-2019"></a><span data-ttu-id="56fcc-149">Исключение в 2019</span><span class="sxs-lookup"><span data-stu-id="56fcc-149">Exceptions in 2019</span></span>

<span data-ttu-id="56fcc-150">Следующие даты являются исключениями для регулярного графика выпуска:</span><span class="sxs-lookup"><span data-stu-id="56fcc-150">The following dates are exceptions to the regular release schedule:</span></span>

| <span data-ttu-id="56fcc-151">Дата</span><span class="sxs-lookup"><span data-stu-id="56fcc-151">Date</span></span> | <span data-ttu-id="56fcc-152">Описание</span><span class="sxs-lookup"><span data-stu-id="56fcc-152">Description</span></span> |
| --- | --- |
| <span data-ttu-id="56fcc-153">Неделя 25 ноября</span><span class="sxs-lookup"><span data-stu-id="56fcc-153">Week of November 25</span></span> | <span data-ttu-id="56fcc-154">Без обновлений</span><span class="sxs-lookup"><span data-stu-id="56fcc-154">No updates</span></span> |
| <span data-ttu-id="56fcc-155">Неделя 16 декабря</span><span class="sxs-lookup"><span data-stu-id="56fcc-155">Week of December 16</span></span> | <span data-ttu-id="56fcc-156">Только незначительные обновления</span><span class="sxs-lookup"><span data-stu-id="56fcc-156">Minor updates only</span></span> |
| <span data-ttu-id="56fcc-157">Неделя 23 декабря</span><span class="sxs-lookup"><span data-stu-id="56fcc-157">Week of December 23</span></span> | <span data-ttu-id="56fcc-158">Без обновлений</span><span class="sxs-lookup"><span data-stu-id="56fcc-158">No updates</span></span> |
| <span data-ttu-id="56fcc-159">Неделя 30 декабря</span><span class="sxs-lookup"><span data-stu-id="56fcc-159">Week of December 30</span></span> | <span data-ttu-id="56fcc-160">Без обновлений</span><span class="sxs-lookup"><span data-stu-id="56fcc-160">No updates</span></span> |

## <a name="communications"></a><span data-ttu-id="56fcc-161">Связь</span><span class="sxs-lookup"><span data-stu-id="56fcc-161">Communications</span></span>

<span data-ttu-id="56fcc-162">Можно узнать, что есть в работе для модуля Human Resources и что мы сделали в следующих местах:</span><span class="sxs-lookup"><span data-stu-id="56fcc-162">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="56fcc-163">Дорожная карта Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="56fcc-163">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/talent/)

- [<span data-ttu-id="56fcc-164">Планы выпуска Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="56fcc-164">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="56fcc-165">Что нового и что изменилось в Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="56fcc-165">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="56fcc-166">[Поиск проблем в Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (только для связанных с платформой ошибок)</span><span class="sxs-lookup"><span data-stu-id="56fcc-166">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="56fcc-167">Блог Human Resources</span><span class="sxs-lookup"><span data-stu-id="56fcc-167">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="56fcc-168">Сообщество Human Resources Yammer</span><span class="sxs-lookup"><span data-stu-id="56fcc-168">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="56fcc-169">Предварительный просмотр функций в среде песочницы</span><span class="sxs-lookup"><span data-stu-id="56fcc-169">Preview features in a sandbox environment</span></span>

<span data-ttu-id="56fcc-170">Можно проверять функции предварительного просмотра в среде песочницы перед их включением в производственную среду.</span><span class="sxs-lookup"><span data-stu-id="56fcc-170">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="56fcc-171">Дополнительные сведения об включении функций см. в разделе [Обзор управления функциями](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="56fcc-171">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="56fcc-172">Все новые возможности остаются в виде предварительного просмотра по крайней мере на 30 дней, а обычно 30-60 дней.</span><span class="sxs-lookup"><span data-stu-id="56fcc-172">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="56fcc-173">Основные функции обычно доступны в октябре и апрель каждого года, следующего за периодом предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="56fcc-173">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="56fcc-174">После отображения новых возможностей в рабочей области Управление функциями их можно включить.</span><span class="sxs-lookup"><span data-stu-id="56fcc-174">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="56fcc-175">Некоторые функции могут быть включены по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="56fcc-175">Some features may be on by default.</span></span>

<span data-ttu-id="56fcc-176">Время от времени неотъемлемая функция будет включена по умолчанию и не может быть отключена (например, в рабочей области Управление функциями).</span><span class="sxs-lookup"><span data-stu-id="56fcc-176">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="56fcc-177">Когда функция обычно доступна, она может быть включена или выключена в производственных средах.</span><span class="sxs-lookup"><span data-stu-id="56fcc-177">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="56fcc-178">Рабочая область Управление функциями показывает, что функция предварительного просмотра станет обязательной.</span><span class="sxs-lookup"><span data-stu-id="56fcc-178">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="56fcc-179">Эта дата обычно приходится на 1 октября или 1 апреля, чтобы соответствовать полугодовым плановым выпускам.</span><span class="sxs-lookup"><span data-stu-id="56fcc-179">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="56fcc-180">Вы не можете отключить обязательные функции.</span><span class="sxs-lookup"><span data-stu-id="56fcc-180">You can't turn off mandatory features.</span></span> <span data-ttu-id="56fcc-181">До тех пор, пока она не станет обязательной, можно включать и выключать функцию во всех средах.</span><span class="sxs-lookup"><span data-stu-id="56fcc-181">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="56fcc-182">Настоятельно рекомендуется предварительный просмотр функций в песочнице или в испытательной среде.</span><span class="sxs-lookup"><span data-stu-id="56fcc-182">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="56fcc-183">Лучше всего создать копию текущей производственной среды или базы данных в среде песочницы, чтобы иметь возможность полного создания новых функций с данными.</span><span class="sxs-lookup"><span data-stu-id="56fcc-183">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="56fcc-184">Дополнительные сведения о подготовке среды песочницы см. в разделе [Подготовка проекта Human Resources](hr-admin-setup-provision.md).</span><span class="sxs-lookup"><span data-stu-id="56fcc-184">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="56fcc-185">Чтобы удалить тестовую среду, см. раздел [Удаление экземпляра](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span><span class="sxs-lookup"><span data-stu-id="56fcc-185">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="56fcc-186">Отчет об ошибках</span><span class="sxs-lookup"><span data-stu-id="56fcc-186">Report bugs</span></span>

<span data-ttu-id="56fcc-187">При проверке функций предварительного просмотра или попытке использовать новые возможности что-то может работать неправильно.</span><span class="sxs-lookup"><span data-stu-id="56fcc-187">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="56fcc-188">Сообщите об ошибках через [Поддержку Microsoft Dynamics 365](https://dynamics.microsoft.com/support/).</span><span class="sxs-lookup"><span data-stu-id="56fcc-188">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="56fcc-189">См. также</span><span class="sxs-lookup"><span data-stu-id="56fcc-189">See also</span></span>

- [<span data-ttu-id="56fcc-190">Планы выпусков Dynamics 365 и Power Platform</span><span class="sxs-lookup"><span data-stu-id="56fcc-190">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)
- [<span data-ttu-id="56fcc-191">Что нового и что изменилось в Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="56fcc-191">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)
- [<span data-ttu-id="56fcc-192">Политика жизненного цикла программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="56fcc-192">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

