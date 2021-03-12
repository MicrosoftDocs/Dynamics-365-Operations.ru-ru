---
title: Установка, настройка и обновление клиентского портала
description: В этой теме приведены сведения о лицензировании и инструкции по установке для клиентского портала.
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 2153bbca2be7c72e48b9dc51b1f7fdbe2ab89903
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977746"
---
# <a name="install-set-up-and-update-the-customer-portal"></a><span data-ttu-id="d3fcd-103">Установка, настройка и обновление клиентского портала</span><span class="sxs-lookup"><span data-stu-id="d3fcd-103">Install, set up, and update the Customer portal</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a><span data-ttu-id="d3fcd-104">Требования к лицензированию</span><span class="sxs-lookup"><span data-stu-id="d3fcd-104">Licensing requirements</span></span>

<span data-ttu-id="d3fcd-105">Для реализации клиентского портала необходимы следующие лицензии:</span><span class="sxs-lookup"><span data-stu-id="d3fcd-105">To implement the Customer portal, you must have the following licenses:</span></span>

- <span data-ttu-id="d3fcd-106">**Порталы Power Apps** — данная лицензия необходима для размещения клиентского портала.</span><span class="sxs-lookup"><span data-stu-id="d3fcd-106">**Power Apps portals** – This license is required to host the Customer portal.</span></span> <span data-ttu-id="d3fcd-107">Порталы лицензируются в зависимости от использования.</span><span class="sxs-lookup"><span data-stu-id="d3fcd-107">Portals are licensed based on usage.</span></span> <span data-ttu-id="d3fcd-108">Дополнительные сведения см. в разделе [Требования к лицензированию порталов Power Apps](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span><span class="sxs-lookup"><span data-stu-id="d3fcd-108">For more information, see the [Power Apps portals licensing requirements](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span></span>
- <span data-ttu-id="d3fcd-109">**Двойная запись** — у вас должны быть необходимые лицензии, чтобы включить двойную запись для таблиц Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d3fcd-109">**Dual-write** – You must have the necessary licenses to enable dual-write for Supply Chain Management tables.</span></span> <span data-ttu-id="d3fcd-110">Дополнительную информацию см. в [системных требованиях для двойной записи](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span><span class="sxs-lookup"><span data-stu-id="d3fcd-110">For more information, see the [system requirements for dual-write](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span></span>

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a><span data-ttu-id="d3fcd-111">Зависимости двойной записи и порталов Power Apps</span><span class="sxs-lookup"><span data-stu-id="d3fcd-111">Dependencies on dual-write and Power Apps portals</span></span>

<span data-ttu-id="d3fcd-112">Клиентский портал зависит от порталов Power Apps и двойной записи, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="d3fcd-112">The Customer portal depends on Power Apps portals and dual-write, as shown in the following illustration.</span></span>

<span data-ttu-id="d3fcd-113">![Зависимости клиентского портала](media/customer-portal-elements.png "Зависимости клиентского портала")</span><span class="sxs-lookup"><span data-stu-id="d3fcd-113">![Customer portal dependencies](media/customer-portal-elements.png "Customer portal dependencies")</span></span>

<span data-ttu-id="d3fcd-114">В отличие от других функций Supply Chain Management шаблон клиентского портала размещается на порталах Power Apps.</span><span class="sxs-lookup"><span data-stu-id="d3fcd-114">Unlike other features from Supply Chain Management, the Customer portal template resides in Power Apps portals.</span></span> <span data-ttu-id="d3fcd-115">Таким образом, клиентский портал ограничивается функциями и возможностями порталов Power Apps и таблиц в двойной записи.</span><span class="sxs-lookup"><span data-stu-id="d3fcd-115">Therefore, the Customer portal is limited by the functionality and capabilities that are provided by Power Apps portals and the tables in dual-write.</span></span>

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a><span data-ttu-id="d3fcd-116">Необходимая настройка для включения клиентского портала</span><span class="sxs-lookup"><span data-stu-id="d3fcd-116">Required setup to enable the Customer portal</span></span>

<span data-ttu-id="d3fcd-117">Убедившись в наличии необходимых лицензий, можно настроить двойную запись, как описано в [инструкциях по начальной синхронизации двойной записи](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span><span class="sxs-lookup"><span data-stu-id="d3fcd-117">After you've made sure that you have the required licenses, you can set up dual-write as described in the [dual-write initial synchronization instructions](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span></span>

<span data-ttu-id="d3fcd-118">Убедитесь, что следующие сопоставления таблиц активированы в двойной записи:</span><span class="sxs-lookup"><span data-stu-id="d3fcd-118">Be sure to enable the following table mappings in dual-write:</span></span>

- <span data-ttu-id="d3fcd-119">Заголовок заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="d3fcd-119">Sales Order Header</span></span>
- <span data-ttu-id="d3fcd-120">Сведения по заказам на продажу</span><span class="sxs-lookup"><span data-stu-id="d3fcd-120">Sales Order Details</span></span>
- <span data-ttu-id="d3fcd-121">Счета</span><span class="sxs-lookup"><span data-stu-id="d3fcd-121">Accounts</span></span>
- <span data-ttu-id="d3fcd-122">Контактные лица</span><span class="sxs-lookup"><span data-stu-id="d3fcd-122">Contacts</span></span>
- <span data-ttu-id="d3fcd-123">Товары</span><span class="sxs-lookup"><span data-stu-id="d3fcd-123">Products</span></span>

<span data-ttu-id="d3fcd-124">После завершения настройки можно подготовить шаблон клиентского портала.</span><span class="sxs-lookup"><span data-stu-id="d3fcd-124">After this setup is completed, you can provision the Customer portal template.</span></span>

## <a name="provision-the-customer-portal"></a><span data-ttu-id="d3fcd-125">Подготовка клиентского портала</span><span class="sxs-lookup"><span data-stu-id="d3fcd-125">Provision the Customer portal</span></span>

<span data-ttu-id="d3fcd-126">Перед началом убедитесь, что [требуемая настройка](#required-setup) уже выполнена.</span><span class="sxs-lookup"><span data-stu-id="d3fcd-126">Before you begin, make sure that you've already completed the [required setup](#required-setup).</span></span> <span data-ttu-id="d3fcd-127">Затем выполните следующие действия, чтобы подготовить клиентский портал.</span><span class="sxs-lookup"><span data-stu-id="d3fcd-127">Then follow these steps to provision the Customer portal.</span></span>

1. <span data-ttu-id="d3fcd-128">Перейдите к [make.powerapps.com](https://make.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="d3fcd-128">Go to [make.powerapps.com](https://make.powerapps.com/).</span></span>
2. <span data-ttu-id="d3fcd-129">Убедитесь, что используете среду, в которой включена двойная запись.</span><span class="sxs-lookup"><span data-stu-id="d3fcd-129">Make sure that you're using the environment where you enabled dual-write.</span></span>
3. <span data-ttu-id="d3fcd-130">На вкладке **Создать** перейдите к разделу **Начать из шаблона** и выберите шаблон с именем **Клиентский портал**.</span><span class="sxs-lookup"><span data-stu-id="d3fcd-130">On the **Create** tab, scroll down to the **Start from template** section, and select the template that is named **Customer Portal**.</span></span>
4. <span data-ttu-id="d3fcd-131">Следуйте инструкциям на экране.</span><span class="sxs-lookup"><span data-stu-id="d3fcd-131">Follow the on-screen instructions.</span></span>

<span data-ttu-id="d3fcd-132">После завершения подготовки к порталу клиента можно получить доступ в разделе **Ваши приложения** на **домашней странице**.</span><span class="sxs-lookup"><span data-stu-id="d3fcd-132">After provisioning is completed, you can access the Customer portal in the **Your apps** section of the **Home** page.</span></span>

> [!NOTE]
> <span data-ttu-id="d3fcd-133">Если решение с двойной записью не установлено в рабочей среде, будет выведено сообщение об ошибке и клиентский портал не будет подготовлен.</span><span class="sxs-lookup"><span data-stu-id="d3fcd-133">If the dual-write solution isn't installed in the environment that you're working in, you will receive an error message, and the Customer portal won't be provisioned.</span></span>

## <a name="update-the-customer-portal"></a><span data-ttu-id="d3fcd-134">Обновление клиентского портала</span><span class="sxs-lookup"><span data-stu-id="d3fcd-134">Update the Customer portal</span></span>

<span data-ttu-id="d3fcd-135">Дополнительные возможности могут быть добавлены на клиентский портал позже.</span><span class="sxs-lookup"><span data-stu-id="d3fcd-135">More functionality might be added to the Customer portal later.</span></span> <span data-ttu-id="d3fcd-136">Любые изменения, вносимые корпорацией Майкрософт в соответствующие компоненты решения, будут автоматически отображаться в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="d3fcd-136">Any changes that Microsoft makes to the underlying solution components will automatically appear in your environment.</span></span> <span data-ttu-id="d3fcd-137">Однако для сайта, настроенного в вашей среде, изменения, внесенные в данные конфигурации, не будут автоматически отражены.</span><span class="sxs-lookup"><span data-stu-id="d3fcd-137">However, the website that is provisioned in your environment won't automatically reflect changes that are made to the configuration data.</span></span> <span data-ttu-id="d3fcd-138">Эти изменения потребуется применить вручную, получив код из нового шаблона и объединив его с подготовленным сайтом.</span><span class="sxs-lookup"><span data-stu-id="d3fcd-138">You will have to manually apply those changes by getting the code from the new template and merging it with the provisioned website.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d3fcd-139">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d3fcd-139">Additional resources</span></span>

<span data-ttu-id="d3fcd-140">Чтобы узнать, как настроить клиентский портал, следует начать с изучения следующей документации по используемым технологиям:</span><span class="sxs-lookup"><span data-stu-id="d3fcd-140">To learn how you can set up and customize the Customer portal, you should start by reviewing the following documentation for the underlying technologies:</span></span>

- [<span data-ttu-id="d3fcd-141">Документация по порталам Power Apps</span><span class="sxs-lookup"><span data-stu-id="d3fcd-141">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="d3fcd-142">Документация по двойной записи</span><span class="sxs-lookup"><span data-stu-id="d3fcd-142">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

<span data-ttu-id="d3fcd-143">Для эффективного управления порталами необходимо понимать порталы Power Apps и жизненный цикл Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="d3fcd-143">To effectively manage your portals, you must understand the Power Apps portals and Microsoft Dataverse lifecycle.</span></span> <span data-ttu-id="d3fcd-144">Дополнительные сведения см. на следующих ресурсах:</span><span class="sxs-lookup"><span data-stu-id="d3fcd-144">For more information, see the following resources:</span></span>

- [<span data-ttu-id="d3fcd-145">О жизненном цикле портала</span><span class="sxs-lookup"><span data-stu-id="d3fcd-145">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="d3fcd-146">Обновление портала</span><span class="sxs-lookup"><span data-stu-id="d3fcd-146">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="d3fcd-147">Миграция конфигурации портала</span><span class="sxs-lookup"><span data-stu-id="d3fcd-147">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="d3fcd-148">Управление жизненным циклом решения: Dynamics 365 для приложений Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="d3fcd-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)
