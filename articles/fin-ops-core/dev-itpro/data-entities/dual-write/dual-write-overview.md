---
title: Обзор двойной записи
description: В этой теме содержится обзор двойной записи, которая обеспечивает взаимодействие практически в режиме реального времени между приложениями для взаимодействия с клиентами и приложениями Finance and Operations.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6cc02b483a2975dd3be28032ea7e90b540945492
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561286"
---
# <a name="dual-write-overview"></a><span data-ttu-id="109e6-103">Обзор двойной записи</span><span class="sxs-lookup"><span data-stu-id="109e6-103">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="109e6-104">Что такое двойная запись?</span><span class="sxs-lookup"><span data-stu-id="109e6-104">What is dual-write?</span></span>

<span data-ttu-id="109e6-105">Двойная запись — это готовая инфраструктура, обеспечивающая взаимодействие практически в режиме реального времени между приложениями Customer Engagement и приложениями Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="109e6-105">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between customer engagement apps and Finance and Operations apps.</span></span> <span data-ttu-id="109e6-106">Когда данные о клиентах, продуктах, сотрудниках и операциях выходят за границы приложения, все подразделения организации получают полномочия.</span><span class="sxs-lookup"><span data-stu-id="109e6-106">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="109e6-107">Двойная запись обеспечивает тесно связанную двунаправленную интеграцию между приложениями Finance and Operations и Dataverse.</span><span class="sxs-lookup"><span data-stu-id="109e6-107">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="109e6-108">Любые изменения данных в приложениях Finance and Operations вызывают запись в Dataverse, а любые изменения данных в Dataverse вызывают записи в приложения Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="109e6-108">Any data change in Finance and Operations apps causes writes to Dataverse, and any data change in Dataverse causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="109e6-109">Этот автоматизированный поток данных обеспечивает интегрированное взаимодействие с пользователем через приложения.</span><span class="sxs-lookup"><span data-stu-id="109e6-109">This automated data flow provides an integrated user experience across the apps.</span></span>

![Связь данных между приложениями](media/dual-write-overview.jpg)

<span data-ttu-id="109e6-111">Двойная запись имеет два аспекта: *инфраструктуры* и *приложение*.</span><span class="sxs-lookup"><span data-stu-id="109e6-111">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="109e6-112">Инфраструктура</span><span class="sxs-lookup"><span data-stu-id="109e6-112">Infrastructure</span></span>

<span data-ttu-id="109e6-113">Инфраструктура с двойной записью является расширяемой и надежной и включает следующие основные функции:</span><span class="sxs-lookup"><span data-stu-id="109e6-113">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="109e6-114">Синхронные и двунаправленные потоки данных между приложениями</span><span class="sxs-lookup"><span data-stu-id="109e6-114">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="109e6-115">Синхронизация в сочетании с режимами воспроизведения, паузы и перехвата для поддержки системы во время интерактивных и автономных/асинхронных режимов.</span><span class="sxs-lookup"><span data-stu-id="109e6-115">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="109e6-116">Возможность синхронизации исходных данных между приложениями</span><span class="sxs-lookup"><span data-stu-id="109e6-116">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="109e6-117">Комбинированное представление действий и журналов ошибок для администраторов данных</span><span class="sxs-lookup"><span data-stu-id="109e6-117">Combined view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="109e6-118">Возможность настраивать настраиваемые оповещения и пороговые значения и подписываться на уведомления</span><span class="sxs-lookup"><span data-stu-id="109e6-118">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="109e6-119">Интуитивный пользовательский интерфейс для фильтрации и преобразования</span><span class="sxs-lookup"><span data-stu-id="109e6-119">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="109e6-120">Возможность задания и просмотра зависимостей и связей таблицы</span><span class="sxs-lookup"><span data-stu-id="109e6-120">Ability to set and view table dependencies and relationships</span></span>
+ <span data-ttu-id="109e6-121">Расширяемость для стандартных и настраиваемых таблиц и сопоставлений</span><span class="sxs-lookup"><span data-stu-id="109e6-121">Extensibility for both standard and custom tables and maps</span></span>
+ <span data-ttu-id="109e6-122">Надежное управление жизненным циклом приложения</span><span class="sxs-lookup"><span data-stu-id="109e6-122">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="109e6-123">Опыт установки из коробки для новых клиентов</span><span class="sxs-lookup"><span data-stu-id="109e6-123">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="109e6-124">Заявление</span><span class="sxs-lookup"><span data-stu-id="109e6-124">Application</span></span>

<span data-ttu-id="109e6-125">Двойная запись создает сопоставление между понятиями в приложениях Finance and Operations и понятиями в приложениях Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="109e6-125">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in customer engagement apps.</span></span> <span data-ttu-id="109e6-126">Интеграция поддерживает следующие сценарии:</span><span class="sxs-lookup"><span data-stu-id="109e6-126">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="109e6-127">Интегрированный справочник клиентов</span><span class="sxs-lookup"><span data-stu-id="109e6-127">Integrated customer master</span></span>
+ <span data-ttu-id="109e6-128">Доступ к карточкам постоянных клиентов и баллам поощрения</span><span class="sxs-lookup"><span data-stu-id="109e6-128">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="109e6-129">Унифицированный подход к шаблонам продуктов</span><span class="sxs-lookup"><span data-stu-id="109e6-129">Unified product mastering experience</span></span>
+ <span data-ttu-id="109e6-130">Осведомленность об организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="109e6-130">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="109e6-131">Интегрированный справочник поставщиков</span><span class="sxs-lookup"><span data-stu-id="109e6-131">Integrated vendor master</span></span>
+ <span data-ttu-id="109e6-132">Доступ к финансовым и налоговым ссылочным данным</span><span class="sxs-lookup"><span data-stu-id="109e6-132">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="109e6-133">Опыт работы с модулем ценообразования по запросу</span><span class="sxs-lookup"><span data-stu-id="109e6-133">On-demand price engine experience</span></span>
+ <span data-ttu-id="109e6-134">Интегрированный опыт потенциальных клиентов</span><span class="sxs-lookup"><span data-stu-id="109e6-134">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="109e6-135">Возможность обслуживания как внутренних активов, так и активов клиентов через местных агентов</span><span class="sxs-lookup"><span data-stu-id="109e6-135">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="109e6-136">Интегрированный опыт процесса от закупки до оплаты</span><span class="sxs-lookup"><span data-stu-id="109e6-136">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="109e6-137">Интегрированные мероприятия и замечания для данных и документов клиента</span><span class="sxs-lookup"><span data-stu-id="109e6-137">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="109e6-138">Возможность поиска сведений о запасах в наличии и их доступности</span><span class="sxs-lookup"><span data-stu-id="109e6-138">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="109e6-139">Опыт от проекта до оплаты</span><span class="sxs-lookup"><span data-stu-id="109e6-139">Project-to-cash experience</span></span>
+ <span data-ttu-id="109e6-140">Способность обрабатывать несколько адресов и ролей с помощью концепции субъекта</span><span class="sxs-lookup"><span data-stu-id="109e6-140">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="109e6-141">Управление одним источником для пользователей</span><span class="sxs-lookup"><span data-stu-id="109e6-141">Single source management for users</span></span>
+ <span data-ttu-id="109e6-142">Интегрированные каналы для розничной торговли и маркетинга</span><span class="sxs-lookup"><span data-stu-id="109e6-142">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="109e6-143">Видимость в рекламных акциях и скидках</span><span class="sxs-lookup"><span data-stu-id="109e6-143">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="109e6-144">Функции запросов на обслуживание</span><span class="sxs-lookup"><span data-stu-id="109e6-144">Request-for-service functions</span></span>
+ <span data-ttu-id="109e6-145">Упрощенные операции по обслуживанию</span><span class="sxs-lookup"><span data-stu-id="109e6-145">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="109e6-146">Основные причины для использования двойной записи</span><span class="sxs-lookup"><span data-stu-id="109e6-146">Top reasons to use dual-write</span></span>

<span data-ttu-id="109e6-147">Двойная запись обеспечивает интеграцию данных среди приложений Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="109e6-147">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="109e6-148">Эта надежная структура связывает среды и позволяет различным бизнес-приложениям работать вместе.</span><span class="sxs-lookup"><span data-stu-id="109e6-148">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="109e6-149">Ниже перечислены основные причины, по которым следует использовать двойную запись:</span><span class="sxs-lookup"><span data-stu-id="109e6-149">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="109e6-150">Двойной объем обеспечивает тесную, практически в режиме реального времени и двунаправленную интеграцию между приложениями Finance and Operations и приложениями на основе модели в Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="109e6-150">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="109e6-151">Эта интеграция делает Microsoft Dynamics 365 универсальным магазином для всех бизнес-решений.</span><span class="sxs-lookup"><span data-stu-id="109e6-151">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="109e6-152">Клиенты, которые используют Dynamics 365 Finance и Dynamics 365 Supply Chain Management, но те, которые используют решения сторонних производителей для управления взаимоотношениями с клиентами (CRM), переходят на Dynamics 365 из-за ее поддержки двойной записи.</span><span class="sxs-lookup"><span data-stu-id="109e6-152">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="109e6-153">Данные от клиентов, продуктов, операций, проектов и Интернета вещей (IoT) автоматически передаются в Dataverse посредством двойной записи.</span><span class="sxs-lookup"><span data-stu-id="109e6-153">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Dataverse through dual-write.</span></span> <span data-ttu-id="109e6-154">Это подключение полезно для предприятий, которые заинтересованы в расширении Power Platform.</span><span class="sxs-lookup"><span data-stu-id="109e6-154">This connection is useful for businesses that are interested in Power Platform expansions.</span></span>
+ <span data-ttu-id="109e6-155">Инфраструктура двойной записи следует принципу без кода/мало кода.</span><span class="sxs-lookup"><span data-stu-id="109e6-155">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="109e6-156">Для расширения стандартных сопоставлений таблицы к таблице и для включения пользовательских сопоставлений требуется минимум усилий в проектировании.</span><span class="sxs-lookup"><span data-stu-id="109e6-156">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="109e6-157">Двойная запись поддерживает как интерактивный режим, так и автономный режим.</span><span class="sxs-lookup"><span data-stu-id="109e6-157">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="109e6-158">Корпорацией Майкрософт является единственная компания, предлагающая поддержку интерактивных и автономных режимов.</span><span class="sxs-lookup"><span data-stu-id="109e6-158">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a><span data-ttu-id="109e6-159">Что означает двойная запись для разработчиков и архитекторов приложений Customer Engagement?</span><span class="sxs-lookup"><span data-stu-id="109e6-159">What does dual-write mean for developers and architects of customer engagement apps?</span></span>

<span data-ttu-id="109e6-160">Двойная запись автоматизирует потоки данных между приложениями Finance and Operations и приложениями Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="109e6-160">Dual-write automates the data flow between Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="109e6-161">Двойная запись состоит из двух решений AppSource, которые установлены на Dataverse.</span><span class="sxs-lookup"><span data-stu-id="109e6-161">Dual-write consists of two AppSource solutions that are installed on Dataverse.</span></span> <span data-ttu-id="109e6-162">Решения расширяют схему таблиц, подключаемые модули и рабочие процессы в Dataverse, чтобы они могли масштабироваться до размера ERP-системы.</span><span class="sxs-lookup"><span data-stu-id="109e6-162">The solutions expand the table schema, plugins, and workflows on Dataverse so that they can scale to ERP size.</span></span> <span data-ttu-id="109e6-163">Для успешной реализации разработчики и архитекторы приложений Customer Engagement должны понимать эти изменения и сотрудничать с их аналогами в приложениях Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="109e6-163">For a successful implementation, developers and architects of customer engagement apps must understand these changes and collaborate with their counterparts on Finance and Operations apps.</span></span>

<span data-ttu-id="109e6-164">Для создания равенства с приложениями Finance and Operations двойная запись вносит некоторые важные изменения схемы Dataverse.</span><span class="sxs-lookup"><span data-stu-id="109e6-164">To create parity with Finance and Operations applications, dual-write makes some crucial changes in the Dataverse schema.</span></span> <span data-ttu-id="109e6-165">Если вы понимаете план, то в будущем можно избежать необходимости переработки дизайна и во время разработки.</span><span class="sxs-lookup"><span data-stu-id="109e6-165">If you understand the plan, you can avoid some design and development rework in the future.</span></span>

+ <span data-ttu-id="109e6-166">Когда пакет с двойной записью AppSource установлен, Dataverse будет содержать новые концепции, такие как компания и субъект.</span><span class="sxs-lookup"><span data-stu-id="109e6-166">When the dual-write AppSource package is installed, Dataverse will have new concepts such as company and party.</span></span> <span data-ttu-id="109e6-167">Эти концепции помогают приложениям, построенным на основе Dataverse, в том числе Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service и Dynamics 365 Field Service, взаимодействовать с приложениями Finance and Operations без проблем.</span><span class="sxs-lookup"><span data-stu-id="109e6-167">These concepts help applications built on Dataverse, including Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service, to interact seamlessly with Finance and Operations apps.</span></span>

+ <span data-ttu-id="109e6-168">Действия и примечания унифицированы и расширены для поддержки C1s (пользователей системы) и C2S (клиентов системы).</span><span class="sxs-lookup"><span data-stu-id="109e6-168">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>

+ <span data-ttu-id="109e6-169">Чтобы избежать потери данных при передаче валютных данных между приложениями Finance and Operations и Dataverse, вы сможете увеличить число десятичных знаков в типе данных валюты приложений Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="109e6-169">To prevent data loss during currency transmission between Finance and Operations apps and the Dataverse, you'll be able to extend the number of decimal places in the currency data type of customers engagement apps.</span></span> <span data-ttu-id="109e6-170">Функция автоматически переводит существующие строки в новое расширенное состояние на уровне метаданных.</span><span class="sxs-lookup"><span data-stu-id="109e6-170">The feature autotranslates existing rows to the new extended state at the metadata layer.</span></span> <span data-ttu-id="109e6-171">В ходе этого процесса денежные значения переводятся в десятичные данные вместо денежных данных, и значение валюты поддерживают до 10 десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="109e6-171">During this process, the currency value is translated to decimal data rather than money data, and the currency value supports 10 decimal places.</span></span> <span data-ttu-id="109e6-172">Эта функция является добровольной, и организациям, в которых не требуется более 4 десятичных разрядов, не нужно соглашаться на эту функцию.</span><span class="sxs-lookup"><span data-stu-id="109e6-172">This feature is opt-in, and organizations that don't need more than 4 decimal places of precision do not need to opt in.</span></span> <span data-ttu-id="109e6-173">Дополнительные сведения см. в разделе [Миграция типов данных валюты для двойной записи](currrency-decimal-places.md).</span><span class="sxs-lookup"><span data-stu-id="109e6-173">For more information, see [Currency data-type migration for dual-write](currrency-decimal-places.md).</span></span>

+ <span data-ttu-id="109e6-174">[Даты вступления в силу](../../dev-tools/date-effectivity.md) будет добавлена в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="109e6-174">[Date effectivity](../../dev-tools/date-effectivity.md) will be added to Dataverse.</span></span> <span data-ttu-id="109e6-175">Она будет поддерживать прошлые, существующие и будущие данные в той же таблицы.</span><span class="sxs-lookup"><span data-stu-id="109e6-175">It will support past, present, and future data on the same table.</span></span>

+ <span data-ttu-id="109e6-176">[Пересчеты единиц измерения](../../../../supply-chain/pim/tasks/manage-unit-measure.md) продукта поддерживаются для продуктов, предложений с расценками, заказов и накладных.</span><span class="sxs-lookup"><span data-stu-id="109e6-176">Product [unit conversions](../../../../supply-chain/pim/tasks/manage-unit-measure.md) are supported for products, quotes, orders, and invoices.</span></span>

<span data-ttu-id="109e6-177">Дополнительные сведения о предстоящих изменениях см. в разделе [Новые возможности и изменения в двойной записи](whats-new-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="109e6-177">For more information about upcoming changes, see [What's new or changed in dual-write](whats-new-dual-write.md).</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]