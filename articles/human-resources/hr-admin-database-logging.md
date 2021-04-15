---
title: Настройка и ведения журнала базы данных
description: Можно отслеживать изменения в таблицах и полях в Dynamics 365 Human Resources с помощью журнала базы данных.
author: andreabichsel
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d22ff9f3ce68c81f37840342c795d7d162eb027b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801343"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="1a1a4-103">Настройка и ведения журнала базы данных</span><span class="sxs-lookup"><span data-stu-id="1a1a4-103">Configure and manage database logging</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1a1a4-104">Можно отслеживать изменения в таблицах и полях в Dynamics 365 Human Resources с помощью журнала базы данных.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="1a1a4-105">В этом разделе описывается следующее:</span><span class="sxs-lookup"><span data-stu-id="1a1a4-105">This topic describes how to:</span></span>

- <span data-ttu-id="1a1a4-106">Управление безопасностью и производительностью для ведения журнала базы данных</span><span class="sxs-lookup"><span data-stu-id="1a1a4-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="1a1a4-107">Настройка регистрации базы данных</span><span class="sxs-lookup"><span data-stu-id="1a1a4-107">Set up database logging</span></span>
- <span data-ttu-id="1a1a4-108">Очистка журналов базы данных</span><span class="sxs-lookup"><span data-stu-id="1a1a4-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="1a1a4-109">Обзор журналов базы данных</span><span class="sxs-lookup"><span data-stu-id="1a1a4-109">Overview of database logging</span></span>

<span data-ttu-id="1a1a4-110">Журналы базы данных отслеживают определенные изменения в таблицах и полях в Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="1a1a4-111">Эти изменения включают вставку, обновление или удаление.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="1a1a4-112">В журнале базы данных сохраняется запись об изменениях в таблицах или полях в таблице журнала базы данных.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="1a1a4-113">Деловые применения журнала базы данных включают в себя:</span><span class="sxs-lookup"><span data-stu-id="1a1a4-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="1a1a4-114">Создание записи аудита изменений в определенных таблицах, содержащих конфиденциальную информацию.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="1a1a4-115">Отслеживание одиночных проводок.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-115">Tracking single transactions.</span></span> <span data-ttu-id="1a1a4-116">Ведение журнала базы данных не предназначено для отслеживания автоматических проводок, которые работают в пакетных заданиях.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="1a1a4-117">Безопасность для ведения журнала базы данных</span><span class="sxs-lookup"><span data-stu-id="1a1a4-117">Security for database logging</span></span>

<span data-ttu-id="1a1a4-118">Журналы базы данных могут содержать конфиденциальные данные.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="1a1a4-119">Ограничьте доступ, чтобы включить только те роли безопасности, для которых необходим доступ к данным журнала.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="1a1a4-120">Ведение журнала базы данных и производительность</span><span class="sxs-lookup"><span data-stu-id="1a1a4-120">Database logging and performance</span></span>

<span data-ttu-id="1a1a4-121">В то же время как ведение журнала базы данных может быть полезно с точки зрения бизнеса, оно может потребовать больших затрат на использование ресурсов и управление ими.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="1a1a4-122">Последствия ведения журнала базы данных для производительности включают в себя:</span><span class="sxs-lookup"><span data-stu-id="1a1a4-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="1a1a4-123">Таблица журнала базы данных может быстро расти и привести к увеличению размера базы данных.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="1a1a4-124">Рост зависит от объема данных в журнале, которые вы решили сохранить.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="1a1a4-125">По умолчанию в таблице журнала базы данных хранятся данные журнала только за 30 дней.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="1a1a4-126">Ведение журнала базы данных может негативно повлиять на длительно выполняемые автоматизированные процессы, такие как длительные импорты данных.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="1a1a4-127">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="1a1a4-127">Best practices</span></span>

<span data-ttu-id="1a1a4-128">Чтобы повысить производительность, ограничьте записи журнала, выбрав для включения в журнал отдельные поля, а не все таблицы.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="1a1a4-129">Для обеспечения общей производительности ведение журнала базы данных ограничивается 20 таблицами.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="1a1a4-130">Только обновления могут регистрироваться для отдельных полей.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="1a1a4-131">Настройка регистрации базы данных</span><span class="sxs-lookup"><span data-stu-id="1a1a4-131">Set up database logging</span></span>

<span data-ttu-id="1a1a4-132">Для настройки ведения журнала базы данных можно использовать мастер **Журнал изменений базы данных**.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="1a1a4-133">Мастер обеспечивает гибкий способ настройки ведения журнала для таблиц или полей.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="1a1a4-134">Перейдите к пункту **Администрирование системы > Ссылки > База данных > Настройка журнала базы данных**.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="1a1a4-135">Выберите **Создать**, чтобы запустить мастер **Ведение журнала изменений базы данных**.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="1a1a4-136">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-136">Select **Next**.</span></span> 
3. <span data-ttu-id="1a1a4-137">На странице **Таблицы и поля** мастера выберите таблицы и поля, для которых необходимо включить ведение журнала базы данных, и выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-137">On the **Tables and fields** page of the wizard, select the the tables and fields on which you want to enable database logging, and select **Next**.</span></span>

   > [!Note]
   > <span data-ttu-id="1a1a4-138">Ведение журнала базы данных доступно не во всех таблицах базы данных Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-138">Database logging is not available on all tables in the Human Resources database.</span></span> <span data-ttu-id="1a1a4-139">При выборе команды **Показать все таблицы** под списком разворачивается список таблиц и полей, в котором отображаются все таблицы базы данных, для которых доступно ведение журнала базы данных, но это будет подмножество полного списка таблиц базы данных.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-139">Selecting **Show all tables** below the list expands the list of tables and fields to show all database tables for which database logging is available, but this will be a subset of the full list of database tables.</span></span>

4. <span data-ttu-id="1a1a4-140">На странице **Типы изменения** мастера выберите операции с данными, для которых необходимо отслеживать изменения для каждой из таблиц и полей, и выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-140">On the **Types of change** page of the wizard, select the data operations for which you want to track changes for each of the tables and fields, and select **Next**.</span></span> <span data-ttu-id="1a1a4-141">В таблице далее представлено описание операций с данными, доступных для ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-141">See the table below for a description of the data operations that are available for logging.</span></span>
5. <span data-ttu-id="1a1a4-142">На странице **Готово** проверьте изменения, которые будут сделаны, и нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-142">On the **Finish** page, review the changes that will be made, and select **Finish**.</span></span>

| <span data-ttu-id="1a1a4-143">Операция</span><span class="sxs-lookup"><span data-stu-id="1a1a4-143">Operation</span></span> | <span data-ttu-id="1a1a4-144">описание</span><span class="sxs-lookup"><span data-stu-id="1a1a4-144">Description</span></span> |
| -- | -- |
| <span data-ttu-id="1a1a4-145">Отслеживать новые проводки</span><span class="sxs-lookup"><span data-stu-id="1a1a4-145">Track new transactions</span></span> | <span data-ttu-id="1a1a4-146">Создайте журнал для новых записей, созданных в таблице.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-146">Create a log for new records that are created in the table.</span></span> |
| <span data-ttu-id="1a1a4-147">Обновить </span><span class="sxs-lookup"><span data-stu-id="1a1a4-147">Update</span></span> | <span data-ttu-id="1a1a4-148">Создайте журнал для обновлений записей таблицы или обновлений в отдельных выбранных полей в таблице.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-148">Create a log for updates to table records, or updates to individually selected fields in the table.</span></span> <span data-ttu-id="1a1a4-149">Если выбрано ведение журнала обновлений для таблицы, то запись журнала создается каждый раз, когда выполняется обновление любого поля любой записи в таблице.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-149">If you select to log updates for the table, then a log record is created each time an update is made to any field of any record on the table.</span></span> <span data-ttu-id="1a1a4-150">Если выбрано ведение журнала обновлений для конкретных полей, запись журнала создается только при обновлении этих полей записей таблицы.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-150">If you select to log updates for specific fields, then a log record is created only when updates are made to those fields of table records.</span></span> |
| <span data-ttu-id="1a1a4-151">Удаление</span><span class="sxs-lookup"><span data-stu-id="1a1a4-151">Delete</span></span> | <span data-ttu-id="1a1a4-152">Создание журнала для записей, удаленных из таблицы.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-152">Create a log for records deleted from the table.</span></span> |
| <span data-ttu-id="1a1a4-153">Переименовать ключ</span><span class="sxs-lookup"><span data-stu-id="1a1a4-153">Rename key</span></span> | <span data-ttu-id="1a1a4-154">Создание записи журнала при переименовании табличного ключа.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-154">Create a log record when a table key is renamed.</span></span> |


## <a name="clean-up-database-logs"></a><span data-ttu-id="1a1a4-155">Очистка журналов базы данных</span><span class="sxs-lookup"><span data-stu-id="1a1a4-155">Clean up database logs</span></span>

<span data-ttu-id="1a1a4-156">Можно удалить весь журнал базы данных или его часть с помощью следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="1a1a4-156">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="1a1a4-157">Выберите все журналы для определенной таблицы.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-157">Select all logs for a particular table.</span></span>
- <span data-ttu-id="1a1a4-158">Выберите отдельные типы журнала базы данных.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-158">Select specific types of database log.</span></span>
- <span data-ttu-id="1a1a4-159">Выберите дату и время создания журнала.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-159">Select a date and time that a log was created.</span></span>

<span data-ttu-id="1a1a4-160">Чтобы настроить очистку журнала базы данных, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="1a1a4-160">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="1a1a4-161">Перейдите к пункту **Администрирование системы > Ссылки > База данных > Журнал базы данных**.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-161">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="1a1a4-162">Выберите **Очистить журнал**.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-162">Select **Clean up log**.</span></span>

2. <span data-ttu-id="1a1a4-163">Выберите метод выбора журналов для удаления, введя один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="1a1a4-163">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="1a1a4-164">Код(ID) таблицы</span><span class="sxs-lookup"><span data-stu-id="1a1a4-164">Table ID</span></span>
   - <span data-ttu-id="1a1a4-165">Тип журнала</span><span class="sxs-lookup"><span data-stu-id="1a1a4-165">Type of log</span></span>
   - <span data-ttu-id="1a1a4-166">Дата и время создания</span><span class="sxs-lookup"><span data-stu-id="1a1a4-166">Created date and time</span></span>

3. <span data-ttu-id="1a1a4-167">Используйте вкладку **Очистка журнала базы данных** для определения времени выполнения задачи очистки журнала.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-167">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="1a1a4-168">По умолчанию журналы базы данных доступны в течение 30 дней.</span><span class="sxs-lookup"><span data-stu-id="1a1a4-168">By default, database logs are available for 30 days.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
