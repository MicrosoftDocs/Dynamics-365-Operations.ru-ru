---
title: Обзор двойной записи
description: В этом разделе представлен обзор двойной записи. Двойная запись — это инфраструктура, обеспечивающая взаимодействие практически в режиме реального времени между приложениями на основе модели Microsoft Dynamics 365 и приложениями Finance and Operations.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 12c6a39700a260c138fab67ed370f94b3aa04213
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076001"
---
# <a name="dual-write-overview"></a><span data-ttu-id="3b5e4-104">Обзор двойной записи</span><span class="sxs-lookup"><span data-stu-id="3b5e4-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

## <a name="what-is-dual-write"></a><span data-ttu-id="3b5e4-105">Что такое двойная запись?</span><span class="sxs-lookup"><span data-stu-id="3b5e4-105">What is dual-write?</span></span>

<span data-ttu-id="3b5e4-106">Двойная запись — это готовая инфраструктура, обеспечивающая взаимодействие практически в режиме реального времени между приложениями на основе модели в Microsoft Dynamics 365 и приложениями Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between model-driven apps in Microsoft Dynamics 365 and Finance and Operations apps.</span></span> <span data-ttu-id="3b5e4-107">Когда данные о клиентах, продуктах, сотрудниках и операциях выходят за границы приложения, все подразделения организации получают полномочия.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="3b5e4-108">Двойная запись обеспечивает тесно связанную двунаправленную интеграцию между приложениями Finance and Operations и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="3b5e4-109">Любые изменения данных в приложениях Finance and Operations вызывают запись в Common Data Service, а любые изменения данных в Common Data Service вызывают записи в приложения Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-109">Any data change in Finance and Operations apps causes writes to Common Data Service, and any data change in Common Data Service causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="3b5e4-110">Этот автоматизированный поток данных обеспечивает интегрированное взаимодействие с пользователем через приложения.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![Связь данных между приложениями](media/dual-write-overview.jpg)

<span data-ttu-id="3b5e4-112">Двойная запись имеет два аспекта: *инфраструктуры* и *приложение*.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="3b5e4-113">Инфраструктура</span><span class="sxs-lookup"><span data-stu-id="3b5e4-113">Infrastructure</span></span>

<span data-ttu-id="3b5e4-114">Инфраструктура с двойной записью является расширяемой и надежной и включает следующие основные функции:</span><span class="sxs-lookup"><span data-stu-id="3b5e4-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="3b5e4-115">Синхронные и двунаправленные потоки данных между приложениями</span><span class="sxs-lookup"><span data-stu-id="3b5e4-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="3b5e4-116">Синхронизация в сочетании с режимами воспроизведения, паузы и перехвата для поддержки системы во время интерактивных и автономных/асинхронных режимов.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="3b5e4-117">Возможность синхронизации исходных данных между приложениями</span><span class="sxs-lookup"><span data-stu-id="3b5e4-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="3b5e4-118">Консолидированное представление действий и журналов ошибок для администраторов данных</span><span class="sxs-lookup"><span data-stu-id="3b5e4-118">Consolidated view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="3b5e4-119">Возможность настраивать настраиваемые оповещения и пороговые значения и подписываться на уведомления</span><span class="sxs-lookup"><span data-stu-id="3b5e4-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="3b5e4-120">Интуитивный пользовательский интерфейс для фильтрации и преобразования</span><span class="sxs-lookup"><span data-stu-id="3b5e4-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="3b5e4-121">Возможность задания и просмотра зависимостей и связей объекта</span><span class="sxs-lookup"><span data-stu-id="3b5e4-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="3b5e4-122">Расширяемость для стандартных и настраиваемых объектов и сопоставлений</span><span class="sxs-lookup"><span data-stu-id="3b5e4-122">Extensibility for both standard and custom entities and maps</span></span>
+ <span data-ttu-id="3b5e4-123">Надежное управление жизненным циклом приложения</span><span class="sxs-lookup"><span data-stu-id="3b5e4-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="3b5e4-124">Опыт установки из коробки для новых клиентов</span><span class="sxs-lookup"><span data-stu-id="3b5e4-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="3b5e4-125">Заявление</span><span class="sxs-lookup"><span data-stu-id="3b5e4-125">Application</span></span>

<span data-ttu-id="3b5e4-126">Двойная запись создает сопоставление между понятиями в приложениях Finance and Operations и понятия в приложениях на основе модели в Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="3b5e4-127">Интеграция поддерживает следующие сценарии:</span><span class="sxs-lookup"><span data-stu-id="3b5e4-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="3b5e4-128">Интегрированный справочник клиентов</span><span class="sxs-lookup"><span data-stu-id="3b5e4-128">Integrated customer master</span></span>
+ <span data-ttu-id="3b5e4-129">Доступ к карточкам постоянных клиентов и баллам поощрения</span><span class="sxs-lookup"><span data-stu-id="3b5e4-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="3b5e4-130">Унифицированный подход к шаблонам продуктов</span><span class="sxs-lookup"><span data-stu-id="3b5e4-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="3b5e4-131">Осведомленность об организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="3b5e4-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="3b5e4-132">Интегрированный справочник поставщиков</span><span class="sxs-lookup"><span data-stu-id="3b5e4-132">Integrated vendor master</span></span>
+ <span data-ttu-id="3b5e4-133">Доступ к финансовым и налоговым ссылочным данным</span><span class="sxs-lookup"><span data-stu-id="3b5e4-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="3b5e4-134">Опыт работы с модулем ценообразования по запросу</span><span class="sxs-lookup"><span data-stu-id="3b5e4-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="3b5e4-135">Интегрированный опыт потенциальных клиентов</span><span class="sxs-lookup"><span data-stu-id="3b5e4-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="3b5e4-136">Возможность обслуживания как внутренних активов, так и активов клиентов через местных агентов</span><span class="sxs-lookup"><span data-stu-id="3b5e4-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="3b5e4-137">Интегрированный опыт процесса от закупки до оплаты</span><span class="sxs-lookup"><span data-stu-id="3b5e4-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="3b5e4-138">Интегрированные мероприятия и замечания для данных и документов клиента</span><span class="sxs-lookup"><span data-stu-id="3b5e4-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="3b5e4-139">Возможность поиска сведений о запасах в наличии и их доступности</span><span class="sxs-lookup"><span data-stu-id="3b5e4-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="3b5e4-140">Опыт от проекта до оплаты</span><span class="sxs-lookup"><span data-stu-id="3b5e4-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="3b5e4-141">Способность обрабатывать несколько адресов и ролей с помощью концепции субъекта</span><span class="sxs-lookup"><span data-stu-id="3b5e4-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="3b5e4-142">Управление одним источником для пользователей</span><span class="sxs-lookup"><span data-stu-id="3b5e4-142">Single source management for users</span></span>
+ <span data-ttu-id="3b5e4-143">Интегрированные каналы для розничной торговли и маркетинга</span><span class="sxs-lookup"><span data-stu-id="3b5e4-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="3b5e4-144">Видимость в рекламных акциях и скидках</span><span class="sxs-lookup"><span data-stu-id="3b5e4-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="3b5e4-145">Функции запросов на обслуживание</span><span class="sxs-lookup"><span data-stu-id="3b5e4-145">Request-for-service functions</span></span>
+ <span data-ttu-id="3b5e4-146">Упрощенные операции по обслуживанию</span><span class="sxs-lookup"><span data-stu-id="3b5e4-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="3b5e4-147">Основные причины для использования двойной записи</span><span class="sxs-lookup"><span data-stu-id="3b5e4-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="3b5e4-148">Двойная запись обеспечивает интеграцию данных среди приложений Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="3b5e4-149">Эта надежная структура связывает среды и позволяет различным бизнес-приложениям работать вместе.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="3b5e4-150">Ниже перечислены основные причины, по которым следует использовать двойную запись:</span><span class="sxs-lookup"><span data-stu-id="3b5e4-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="3b5e4-151">Двойной объем обеспечивает тесную, практически в режиме реального времени и двунаправленную интеграцию между приложениями Finance and Operations и приложениями на основе модели в Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="3b5e4-152">Эта интеграция делает Microsoft Dynamics 365 универсальным магазином для всех бизнес-решений.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="3b5e4-153">Клиенты, которые используют Dynamics 365 Finance и Dynamics 365 Supply Chain Management, но те, которые используют решения сторонних производителей для управления взаимоотношениями с клиентами (CRM), переходят на Dynamics 365 из-за ее поддержки двойной записи.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="3b5e4-154">Данные от клиентов, продуктов, операций, проектов и Интернета вещей (IoT) автоматически передаются в Common Data Service посредством двойной записи.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Common Data Service through dual-write.</span></span> <span data-ttu-id="3b5e4-155">Это подключение очень полезно для предприятий, которые заинтересованы в расширении Microsoft Power Platform.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-155">This connection is very useful for businesses that are interested in Microsoft Power Platform expansions.</span></span>
+ <span data-ttu-id="3b5e4-156">Инфраструктура двойной записи следует принципу без кода/мало кода.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="3b5e4-157">Для расширения стандартных сопоставлений таблицы к таблице и для включения пользовательских сопоставлений требуется минимум усилий в проектировании.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="3b5e4-158">Двойная запись поддерживает как интерактивный режим, так и автономный режим.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="3b5e4-159">Корпорацией Майкрософт является единственная компания, предлагающая поддержку интерактивных и автономных режимов.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a><span data-ttu-id="3b5e4-160">Что означает двойная запись для пользователей и архитекторов продуктов CRM?</span><span class="sxs-lookup"><span data-stu-id="3b5e4-160">What does dual-write mean for users and architects of CRM products?</span></span>

<span data-ttu-id="3b5e4-161">Двойная запись автоматизирует потоки данных между приложениями Finance and Operations и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-161">Dual-write automates the data flow between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="3b5e4-162">В будущих выпусках концепции приложений на основе модели в Dynamics 365 (например, клиент, контакт, предложение и заказ) будут масштабироваться до клиентов среднего и высшего среднего уровня.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-162">In future releases, concepts in model-driven apps in Dynamics 365 (for example, customer, contact, quotation, and order) will be scaled to mid-market and upper-mid-market customers.</span></span>

<span data-ttu-id="3b5e4-163">В первом выпуске большая часть автоматизации обрабатывается решениями двойной записи.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-163">In the first release, most of the automation is handled by dual-write solutions.</span></span> <span data-ttu-id="3b5e4-164">В будущих выпусках эти решения станут частью Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-164">In future releases, those solutions will become part of Common Data Service.</span></span> <span data-ttu-id="3b5e4-165">Понимание будущих изменений в Common Data Service позволяет сэкономить усилия в долгосрочной перспективе.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-165">By understanding the upcoming changes to Common Data Service, you can save yourself effort in the long term.</span></span> <span data-ttu-id="3b5e4-166">Ниже приведены некоторые важные изменения:</span><span class="sxs-lookup"><span data-stu-id="3b5e4-166">Here are some of the crucial changes:</span></span>

+ <span data-ttu-id="3b5e4-167">Common Data Service будет содержать новые понятия, такие как компания и ее субъект.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-167">Common Data Service will have new concepts, such as company and party.</span></span> <span data-ttu-id="3b5e4-168">Эти понятия повлияют на все приложения, построенные на основе Common Data Service, например, Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service и Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-168">These concepts will affect all apps that are built on Common Data Service, such as Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service.</span></span>
+ <span data-ttu-id="3b5e4-169">Действия и примечания унифицированы и расширены для поддержки C1s (пользователей системы) и C2S (клиентов системы).</span><span class="sxs-lookup"><span data-stu-id="3b5e4-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>
+ <span data-ttu-id="3b5e4-170">Ниже приведены некоторые предстоящие изменения в Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="3b5e4-170">Here are some of the upcoming changes in Common Data Service:</span></span>

    - <span data-ttu-id="3b5e4-171">Десятичный тип данных заменит тип денежных данных.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-171">The decimal data type will replace the money data type.</span></span>
    - <span data-ttu-id="3b5e4-172">Дата вступления в силу будет поддерживать прошлые, существующие и будущие данные на одном и том же месте.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-172">Date effectivity will support past, present, and future data in the same place.</span></span>
    - <span data-ttu-id="3b5e4-173">При этом будет поддерживаться обменный курс и валютный курс, а API-интерфейс **Валютный курс** будет пересмотрен.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-173">There will be more support for currency and exchange rates, and the **Exchange Rate** application programming interface (API) will be revised.</span></span>
    - <span data-ttu-id="3b5e4-174">Пересчет единиц измерения будет поддерживаться.</span><span class="sxs-lookup"><span data-stu-id="3b5e4-174">Unit conversions will be supported.</span></span>

<span data-ttu-id="3b5e4-175">Дополнительные сведения о предстоящих изменениях см. в разделе [Данные в Common Data Service — этап 1 и 2](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/extensibility/extensibility-roadmap).</span><span class="sxs-lookup"><span data-stu-id="3b5e4-175">For more information about upcoming changes, see [Data in Common Data Service – phase 1 & 2](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/extensibility/extensibility-roadmap).</span></span>
