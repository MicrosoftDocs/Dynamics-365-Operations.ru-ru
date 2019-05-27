---
title: Домашняя страница управления организацией
description: Эта тема указывает на ресурсы, которые помогут использовать Microsoft Dynamics 365 for Finance and Operations в организации.
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a693529b55b66eb940f8215a336d5c4ae0acedd
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545864"
---
# <a name="organization-administration-home-page"></a><span data-ttu-id="fc789-103">Домашняя страница управления организацией</span><span class="sxs-lookup"><span data-stu-id="fc789-103">Organization administration home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc789-104">В этой теме перечислены материалы, которые пригодятся опытным пользователям и администраторам при настройке Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fc789-104">This topic points to content that will help power users and administrators configure Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="fc789-105">Эти материалы помогут им настроить систему для бесперебойной и эффективной работы на благо организации и бизнеса.</span><span class="sxs-lookup"><span data-stu-id="fc789-105">This content will help them configure the system to work smoothly and effectively for your organization and business.</span></span>

<span data-ttu-id="fc789-106">Многие из материалов, перечисленных здесь, относятся к функциям в модуле **Управление организацией**.</span><span class="sxs-lookup"><span data-stu-id="fc789-106">Much of the content listed here applies to features in the **Organizational administration** module.</span></span> <span data-ttu-id="fc789-107">Однако существуют некоторые задачи, такие как создание и использование шаблона записи, которые могут быть выполнены в любом модуле для повышения эффективности работы вашей организации.</span><span class="sxs-lookup"><span data-stu-id="fc789-107">However, there are a couple of tasks, such as creating and using a record template, that can be performed in any module to help your organization run more efficiently.</span></span>

## <a name="number-sequences"></a><span data-ttu-id="fc789-108">Номерные серии</span><span class="sxs-lookup"><span data-stu-id="fc789-108">Number sequences</span></span>

<span data-ttu-id="fc789-109">Номерные серии используются для создания четких уникальных кодов для записей справочника и записей проводок, для которых требуются коды.</span><span class="sxs-lookup"><span data-stu-id="fc789-109">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="fc789-110">Запись основных данных или запись проводки, для которой требуется идентификатор, называется *образцом*.</span><span class="sxs-lookup"><span data-stu-id="fc789-110">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span> <span data-ttu-id="fc789-111">Перед созданием новых записей для ссылки необходимо настроить номерную серию и связать ее со ссылкой.</span><span class="sxs-lookup"><span data-stu-id="fc789-111">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span>

- [<span data-ttu-id="fc789-112">Обзор номерной серии</span><span class="sxs-lookup"><span data-stu-id="fc789-112">Number sequence overview</span></span>](number-sequence-overview.md)
- <span data-ttu-id="fc789-113">[Настройка номерных серий с использованием мастера](tasks/set-up-number-sequences-wizard.md) (Руководство по задаче)</span><span class="sxs-lookup"><span data-stu-id="fc789-113">[Set up number sequences by using a wizard](tasks/set-up-number-sequences-wizard.md) (Task guide)</span></span>
- <span data-ttu-id="fc789-114">[Настройка номерных серий на индивидуальной основе](tasks/set-up-number-sequences-individual-basis.md) (Руководство по задаче)</span><span class="sxs-lookup"><span data-stu-id="fc789-114">[Set up number sequences on an individual basis](tasks/set-up-number-sequences-individual-basis.md) (Task guide)</span></span>

## <a name="organizations"></a><span data-ttu-id="fc789-115">Организации</span><span class="sxs-lookup"><span data-stu-id="fc789-115">Organizations</span></span>

<span data-ttu-id="fc789-116">Организация — это группа людей, работающих вместе, для выполнения бизнес-процесса или достижения цели.</span><span class="sxs-lookup"><span data-stu-id="fc789-116">An organization is a group of people who are working together to carry out a business process or achieve a goal.</span></span> <span data-ttu-id="fc789-117">Организационные иерархии представляют собой связи между организациями, которые занимаются коммерческой деятельностью.</span><span class="sxs-lookup"><span data-stu-id="fc789-117">Organizational hierarchies represent the relationships between the organizations that make up your business.</span></span>

<span data-ttu-id="fc789-118">Перед настройкой организаций и организационных иерархий в Finance and Operations убедитесь, что вы спланировали моделирование своей компании.</span><span class="sxs-lookup"><span data-stu-id="fc789-118">Before you set up organizations and organization hierarchies in Finance and Operations, make sure that you plan how your business will be modeled.</span></span> <span data-ttu-id="fc789-119">Организационная модель имеет значительное влияет на реализацию Dynamics 365 for Finance and Operations и бизнес-процессы.</span><span class="sxs-lookup"><span data-stu-id="fc789-119">The organization model has a significant effect on the implementation of Finance and Operations and on business processes.</span></span>

- [<span data-ttu-id="fc789-120">Организации и организационные иерархии</span><span class="sxs-lookup"><span data-stu-id="fc789-120">Organizations and organizational hierarchies</span></span>](organizations-organizational-hierarchies.md)
- [<span data-ttu-id="fc789-121">Планирование организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="fc789-121">Plan your organizational hierarchy</span></span>](plan-organizational-hierarchy.md)
- <span data-ttu-id="fc789-122">[Создание организационной иерархии](tasks/create-organization-hierarchy.md) (Руководство по задачам)</span><span class="sxs-lookup"><span data-stu-id="fc789-122">[Create an organization hierarchy](tasks/create-organization-hierarchy.md) (Task guide)</span></span>
- <span data-ttu-id="fc789-123">[Создание юридического лица](tasks/create-legal-entity.md) (Руководство по задачам)</span><span class="sxs-lookup"><span data-stu-id="fc789-123">[Create a legal entity](tasks/create-legal-entity.md) (Task guide)</span></span>
- <span data-ttu-id="fc789-124">[Создание операционной единицы](tasks/create-operating-unit.md) (Руководство по задачам)</span><span class="sxs-lookup"><span data-stu-id="fc789-124">[Create an operating unit](tasks/create-operating-unit.md) (Task guide)</span></span>

## <a name="address-books"></a><span data-ttu-id="fc789-125">Адресные книги</span><span class="sxs-lookup"><span data-stu-id="fc789-125">Address books</span></span>

<span data-ttu-id="fc789-126">Глобальная адресная книга — это централизованный репозиторий справочных данных, которые должны храниться для всех внутренних и внешних лиц и организаций, с которыми взаимодействует компания.</span><span class="sxs-lookup"><span data-stu-id="fc789-126">The global address book is a centralized repository for master data that must be stored for all internal and external persons and organizations that the company interacts with.</span></span> <span data-ttu-id="fc789-127">Данные, связанные с записями субъекта, включают в себя наименование, адрес и контактную информацию субъекта.</span><span class="sxs-lookup"><span data-stu-id="fc789-127">The data that is associated with party records includes the party's name, address, and contact information.</span></span>

<span data-ttu-id="fc789-128">После создания глобальной адресной книги вы можете создать дополнительные адресные книги согласно своим потребностям, например отдельную адресную книгу для каждой компании в вашей организации или для каждой сферы деятельности.</span><span class="sxs-lookup"><span data-stu-id="fc789-128">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span>

- [<span data-ttu-id="fc789-129">Глобальная адресная книга</span><span class="sxs-lookup"><span data-stu-id="fc789-129">Global address book</span></span>](overview-global-address-book.md)
- [<span data-ttu-id="fc789-130">Планирование настройки глобальной адресной книги и дополнительных адресных книг</span><span class="sxs-lookup"><span data-stu-id="fc789-130">Plan how to configure the global address book and additional address books</span></span>](plan-configuration-global-address-book-additional-address-books.md)
- [<span data-ttu-id="fc789-131">Настройка глобальной адресной книги</span><span class="sxs-lookup"><span data-stu-id="fc789-131">Configure the global address book</span></span>](tasks/configure-global-address-book.md)
- [<span data-ttu-id="fc789-132">Вопросы и ответы по адресным книгам</span><span class="sxs-lookup"><span data-stu-id="fc789-132">Address books FAQ</span></span>](qa-address-books.md)

## <a name="workflow"></a><span data-ttu-id="fc789-133">Документооборот</span><span class="sxs-lookup"><span data-stu-id="fc789-133">Workflow</span></span>

<span data-ttu-id="fc789-134">Workflow-процесс — это система, устанавливается вместе с Finance and Operations, которую можно использовать для создания отдельных workflow-процессов, или бизнес-процессов.</span><span class="sxs-lookup"><span data-stu-id="fc789-134">Workflow is a system that is installed with Finance and Operations that you can use to create individual workflows, or business processes.</span></span> <span data-ttu-id="fc789-135">При создании workflow-процесса вы указываете, как документ движется по системе, показывая, кто должен выполнить задачу, принять решение или утвердить документ.</span><span class="sxs-lookup"><span data-stu-id="fc789-135">When you create a workflow, you specify how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span>

- [<span data-ttu-id="fc789-136">Документооборот: обзор</span><span class="sxs-lookup"><span data-stu-id="fc789-136">Workflow overview</span></span>](overview-workflow-system.md)
- [<span data-ttu-id="fc789-137">Элементы workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="fc789-137">Workflow elements</span></span>](workflow-elements.md)
- [<span data-ttu-id="fc789-138">Действия workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="fc789-138">Workflow actions</span></span>](workflow-actions.md)
- [<span data-ttu-id="fc789-139">Создание workflow-процесса</span><span class="sxs-lookup"><span data-stu-id="fc789-139">Create a workflow</span></span>](create-workflow.md)

## <a name="electronic-signatures"></a><span data-ttu-id="fc789-140">Электронные подписи</span><span class="sxs-lookup"><span data-stu-id="fc789-140">Electronic signatures</span></span>

<span data-ttu-id="fc789-141">Электронная подпись подтверждает личность человека, который намеревается запустить или утвердить процесс обработки данных.</span><span class="sxs-lookup"><span data-stu-id="fc789-141">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="fc789-142">В некоторых отраслях промышленности электронная подпись имеет одинаковую юридическую силу с рукописной подписью.</span><span class="sxs-lookup"><span data-stu-id="fc789-142">In some industries, an electronic signature is as legally binding as a handwritten signature.</span></span> <span data-ttu-id="fc789-143">Электронные подписи являются обязательным требованием в некоторых строго регламентируемых отраслях, таких как фармацевтика, продукты и напитки, аэрокосмическая и оборонная.</span><span class="sxs-lookup"><span data-stu-id="fc789-143">Electronic signatures are a regulations compliance requirement for several regulated industries, such as pharmaceuticals, food and beverage, and aerospace and defense.</span></span>

<span data-ttu-id="fc789-144">В Finance and Operations вы можете использовать электронные подписи для критических бизнес-процессов.</span><span class="sxs-lookup"><span data-stu-id="fc789-144">In Finance and Operations, you can use electronic signatures for critical business processes.</span></span> <span data-ttu-id="fc789-145">Для некоторых процессов предусмотрены встроенные возможности использования электронных подписей.</span><span class="sxs-lookup"><span data-stu-id="fc789-145">Some processes have built-in electronic signature capabilities.</span></span> <span data-ttu-id="fc789-146">Можно также создать пользовательские требования к электронным подписям для любой таблицы и поля базы данных.</span><span class="sxs-lookup"><span data-stu-id="fc789-146">You can also create custom signature requirements for any database table and field.</span></span>

- [<span data-ttu-id="fc789-147">Обзор электронной подписи</span><span class="sxs-lookup"><span data-stu-id="fc789-147">Electronic signature overview</span></span>](electronic-signature-overview.md)
- <span data-ttu-id="fc789-148">[Настройка электронных подписей](tasks/set-up-electronic-signatures.md) (Руководство по задаче)</span><span class="sxs-lookup"><span data-stu-id="fc789-148">[Set up electronic signatures](tasks/set-up-electronic-signatures.md) (Task guide)</span></span>

## <a name="case-management"></a><span data-ttu-id="fc789-149">Управление обращениями</span><span class="sxs-lookup"><span data-stu-id="fc789-149">Case management</span></span>

<span data-ttu-id="fc789-150">Планирование, отслеживание и анализ обращений позволяет выработать эффективные решения, которые можно использовать для аналогичных проблем.</span><span class="sxs-lookup"><span data-stu-id="fc789-150">By planning, tracking, and analyzing cases, you can develop efficient resolutions that can be used for similar issues.</span></span> <span data-ttu-id="fc789-151">Например, при создании обращений представители отдела обслуживания клиентов или менеджеры по персоналу могут находить в статьях базы знаний сведения о том, как более эффективно работать с обращением или как его разрешить.</span><span class="sxs-lookup"><span data-stu-id="fc789-151">For example, when customer service representatives or Human Resources generalists create cases, they can find information in knowledge articles to help them work with or resolve a case more efficiently.</span></span>

- [<span data-ttu-id="fc789-152">Обзор управления обращениями</span><span class="sxs-lookup"><span data-stu-id="fc789-152">Case management overview</span></span>](cases.md)
- [<span data-ttu-id="fc789-153">Настройка безопасности обращений, процессов и категорий</span><span class="sxs-lookup"><span data-stu-id="fc789-153">Configure case security, processes, and categories</span></span>](plan-case-management.md)

## <a name="record-templates"></a><span data-ttu-id="fc789-154">Шаблоны записей</span><span class="sxs-lookup"><span data-stu-id="fc789-154">Record templates</span></span>

<span data-ttu-id="fc789-155">Шаблоны записей позволяют быстрее создавать записи в системе .</span><span class="sxs-lookup"><span data-stu-id="fc789-155">Record templates can help you to create records more quickly.</span></span> <span data-ttu-id="fc789-156">Вы можете создать шаблон записи, чтобы значения полей, которые используются часто, не требовалось вводить явно для каждой новой записи.</span><span class="sxs-lookup"><span data-stu-id="fc789-156">You can create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span>

- [<span data-ttu-id="fc789-157">Шаблоны записей</span><span class="sxs-lookup"><span data-stu-id="fc789-157">Record templates</span></span>](record-templates.md)
- <span data-ttu-id="fc789-158">[Создание шаблона записи для более удобного ввода данных](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (проводник по задаче)</span><span class="sxs-lookup"><span data-stu-id="fc789-158">[Create a record template to facilitate data entry](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (Task guide)</span></span>
- <span data-ttu-id="fc789-159">[Использование шаблона записи для создания новой записи](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (проводник по задаче)</span><span class="sxs-lookup"><span data-stu-id="fc789-159">[Use a record template to create a new record](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (Task guide)</span></span>

## <a name="general-organization-administration"></a><span data-ttu-id="fc789-160">Общие вопросы администрирования организации</span><span class="sxs-lookup"><span data-stu-id="fc789-160">General organization administration</span></span>

- <span data-ttu-id="fc789-161">[Изменение баннера или эмблемы](../get-started/tasks/change-banner-or-logo.md) (Руководство по задачам)</span><span class="sxs-lookup"><span data-stu-id="fc789-161">[Change the banner or logo](../get-started/tasks/change-banner-or-logo.md) (Task guide)</span></span>
- [<span data-ttu-id="fc789-162">Настройка управления документами</span><span class="sxs-lookup"><span data-stu-id="fc789-162">Configure document management</span></span>](configure-document-management.md)
- [<span data-ttu-id="fc789-163">Настройка и отправка электронной почты</span><span class="sxs-lookup"><span data-stu-id="fc789-163">Configure and send email</span></span>](configure-email.md)
- [<span data-ttu-id="fc789-164">Данные времени/даты и часовые пояса</span><span class="sxs-lookup"><span data-stu-id="fc789-164">Date/time data and time zones</span></span>](date-time-zones.md)
