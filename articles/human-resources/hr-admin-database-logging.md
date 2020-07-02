---
title: Настройка и ведения журнала базы данных
description: Можно отслеживать изменения в таблицах и полях в Dynamics 365 Human Resources с помощью журнала базы данных.
author: Darinkramer
manager: AnnBe
ms.date: 06/10/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3dc4658a0a13af95978c66f5aab882902f754a2d
ms.sourcegitcommit: 88f38d584c5befb96e4d1daab4b28af5519ef125
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "3443595"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="7b023-103">Настройка и ведения журнала базы данных</span><span class="sxs-lookup"><span data-stu-id="7b023-103">Configure and manage database logging</span></span>

<span data-ttu-id="7b023-104">Можно отслеживать изменения в таблицах и полях в Dynamics 365 Human Resources с помощью журнала базы данных.</span><span class="sxs-lookup"><span data-stu-id="7b023-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="7b023-105">В этом разделе описывается следующее:</span><span class="sxs-lookup"><span data-stu-id="7b023-105">This topic describes how to:</span></span>

- <span data-ttu-id="7b023-106">Управление безопасностью и производительностью для ведения журнала базы данных</span><span class="sxs-lookup"><span data-stu-id="7b023-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="7b023-107">Настройка регистрации базы данных</span><span class="sxs-lookup"><span data-stu-id="7b023-107">Set up database logging</span></span>
- <span data-ttu-id="7b023-108">Очистка журналов базы данных</span><span class="sxs-lookup"><span data-stu-id="7b023-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="7b023-109">Обзор журналов базы данных</span><span class="sxs-lookup"><span data-stu-id="7b023-109">Overview of database logging</span></span>

<span data-ttu-id="7b023-110">Журналы базы данных отслеживают определенные изменения в таблицах и полях в Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7b023-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="7b023-111">Эти изменения включают вставку, обновление или удаление.</span><span class="sxs-lookup"><span data-stu-id="7b023-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="7b023-112">В журнале базы данных сохраняется запись об изменениях в таблицах или полях в таблице журнала базы данных.</span><span class="sxs-lookup"><span data-stu-id="7b023-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="7b023-113">Деловые применения журнала базы данных включают в себя:</span><span class="sxs-lookup"><span data-stu-id="7b023-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="7b023-114">Создание записи аудита изменений в определенных таблицах, содержащих конфиденциальную информацию.</span><span class="sxs-lookup"><span data-stu-id="7b023-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="7b023-115">Отслеживание одиночных проводок.</span><span class="sxs-lookup"><span data-stu-id="7b023-115">Tracking single transactions.</span></span> <span data-ttu-id="7b023-116">Ведение журнала базы данных не предназначено для отслеживания автоматических проводок, которые работают в пакетных заданиях.</span><span class="sxs-lookup"><span data-stu-id="7b023-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="7b023-117">Безопасность для ведения журнала базы данных</span><span class="sxs-lookup"><span data-stu-id="7b023-117">Security for database logging</span></span>

<span data-ttu-id="7b023-118">Журналы базы данных могут содержать конфиденциальные данные.</span><span class="sxs-lookup"><span data-stu-id="7b023-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="7b023-119">Ограничьте доступ, чтобы включить только те роли безопасности, для которых необходим доступ к данным журнала.</span><span class="sxs-lookup"><span data-stu-id="7b023-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="7b023-120">Ведение журнала базы данных и производительность</span><span class="sxs-lookup"><span data-stu-id="7b023-120">Database logging and performance</span></span>

<span data-ttu-id="7b023-121">В то же время как ведение журнала базы данных может быть полезно с точки зрения бизнеса, оно может потребовать больших затрат на использование ресурсов и управление ими.</span><span class="sxs-lookup"><span data-stu-id="7b023-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="7b023-122">Последствия ведения журнала базы данных для производительности включают в себя:</span><span class="sxs-lookup"><span data-stu-id="7b023-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="7b023-123">Таблица журнала базы данных может быстро расти и привести к увеличению размера базы данных.</span><span class="sxs-lookup"><span data-stu-id="7b023-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="7b023-124">Рост зависит от объема данных в журнале, которые вы решили сохранить.</span><span class="sxs-lookup"><span data-stu-id="7b023-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="7b023-125">По умолчанию в таблице журнала базы данных хранятся данные журнала только за 30 дней.</span><span class="sxs-lookup"><span data-stu-id="7b023-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="7b023-126">Ведение журнала базы данных может негативно повлиять на длительно выполняемые автоматизированные процессы, такие как длительные импорты данных.</span><span class="sxs-lookup"><span data-stu-id="7b023-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="7b023-127">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="7b023-127">Best practices</span></span>

<span data-ttu-id="7b023-128">Чтобы повысить производительность, ограничьте записи журнала, выбрав для включения в журнал отдельные поля, а не все таблицы.</span><span class="sxs-lookup"><span data-stu-id="7b023-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="7b023-129">Для обеспечения общей производительности ведение журнала базы данных ограничивается 20 таблицами.</span><span class="sxs-lookup"><span data-stu-id="7b023-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="7b023-130">Только обновления могут регистрироваться для отдельных полей.</span><span class="sxs-lookup"><span data-stu-id="7b023-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="7b023-131">Настройка регистрации базы данных</span><span class="sxs-lookup"><span data-stu-id="7b023-131">Set up database logging</span></span>

<span data-ttu-id="7b023-132">Для настройки ведения журнала базы данных можно использовать мастер **Журнал изменений базы данных**.</span><span class="sxs-lookup"><span data-stu-id="7b023-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="7b023-133">Мастер обеспечивает гибкий способ настройки ведения журнала для таблиц или полей.</span><span class="sxs-lookup"><span data-stu-id="7b023-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="7b023-134">Перейдите к пункту **Администрирование системы > Ссылки > База данных > Настройка журнала базы данных**.</span><span class="sxs-lookup"><span data-stu-id="7b023-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="7b023-135">Выберите **Создать**, чтобы запустить мастер **Ведение журнала изменений базы данных**.</span><span class="sxs-lookup"><span data-stu-id="7b023-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="7b023-136">Выполните работу с мастером.</span><span class="sxs-lookup"><span data-stu-id="7b023-136">Complete the wizard.</span></span>

## <a name="clean-up-database-logs"></a><span data-ttu-id="7b023-137">Очистка журналов базы данных</span><span class="sxs-lookup"><span data-stu-id="7b023-137">Clean up database logs</span></span>

<span data-ttu-id="7b023-138">Можно удалить весь журнал базы данных или его часть с помощью следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="7b023-138">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="7b023-139">Выберите все журналы для определенной таблицы.</span><span class="sxs-lookup"><span data-stu-id="7b023-139">Select all logs for a particular table.</span></span>
- <span data-ttu-id="7b023-140">Выберите отдельные типы журнала базы данных.</span><span class="sxs-lookup"><span data-stu-id="7b023-140">Select specific types of database log.</span></span>
- <span data-ttu-id="7b023-141">Выберите дату и время создания журнала.</span><span class="sxs-lookup"><span data-stu-id="7b023-141">Select a date and time that a log was created.</span></span>

<span data-ttu-id="7b023-142">Чтобы настроить очистку журнала базы данных, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="7b023-142">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="7b023-143">Перейдите к пункту **Администрирование системы > Ссылки > База данных > Журнал базы данных**.</span><span class="sxs-lookup"><span data-stu-id="7b023-143">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="7b023-144">Выберите **Очистить журнал**.</span><span class="sxs-lookup"><span data-stu-id="7b023-144">Select **Clean up log**.</span></span>

2. <span data-ttu-id="7b023-145">Выберите метод выбора журналов для удаления, введя один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="7b023-145">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="7b023-146">Код(ID) таблицы</span><span class="sxs-lookup"><span data-stu-id="7b023-146">Table ID</span></span>
   - <span data-ttu-id="7b023-147">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="7b023-147">Type of log</span></span>
   - <span data-ttu-id="7b023-148">Дата и время создания</span><span class="sxs-lookup"><span data-stu-id="7b023-148">Created date and time</span></span>

3. <span data-ttu-id="7b023-149">Используйте вкладку **Очистка журнала базы данных** для определения времени выполнения задачи очистки журнала.</span><span class="sxs-lookup"><span data-stu-id="7b023-149">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="7b023-150">По умолчанию журналы базы данных доступны в течение 30 дней.</span><span class="sxs-lookup"><span data-stu-id="7b023-150">By default, database logs are available for 30 days.</span></span>
