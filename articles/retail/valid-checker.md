---
title: Программа проверки согласованности проводок розничной торговли
description: В этом разделе описываются функции программы проверки согласованности проводок розничной торговли в Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 972c4d6b244eebc85cc801353ce8fb25ecbc0655
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517153"
---
# <a name="retail-transaction-consistency-checker"></a><span data-ttu-id="e7b40-103">Программа проверки согласованности проводок розничной торговли</span><span class="sxs-lookup"><span data-stu-id="e7b40-103">Retail transaction consistency checker</span></span>


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="e7b40-104">В этом разделе описываются функции программы проверки согласованности проводок розничной торговли, появившейся в Microsoft Dynamics 365 for Finance and Operations версии 8.1.3.</span><span class="sxs-lookup"><span data-stu-id="e7b40-104">This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</span></span> <span data-ttu-id="e7b40-105">Программа проверки согласованности обнаруживает и отделяет противоречивые проводки до их передачи в процесс разноски операций.</span><span class="sxs-lookup"><span data-stu-id="e7b40-105">The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</span></span>

<span data-ttu-id="e7b40-106">При разноске операции в Retail может произойти сбой из-за несогласованности данных в таблицах проводок розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="e7b40-106">When a statement is posted in Retail, posting can fail due to inconsistent data in the retail transaction tables.</span></span> <span data-ttu-id="e7b40-107">Ошибка данных может быть связана с непредвиденными проблемами в приложении POS или с неправильным импортом проводок из систем POS других разработчиков.</span><span class="sxs-lookup"><span data-stu-id="e7b40-107">The data issue may be caused by by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</span></span> <span data-ttu-id="e7b40-108">Ниже приведены возможные примеры несогласованности.</span><span class="sxs-lookup"><span data-stu-id="e7b40-108">Examples of how these inconsistencies may appear include:</span></span> 

  - <span data-ttu-id="e7b40-109">Общая сумма проводки в таблице заголовков не соответствует общей сумме проводок в строках.</span><span class="sxs-lookup"><span data-stu-id="e7b40-109">The transaction total on the header table does not match the transaction total on the lines.</span></span>
  - <span data-ttu-id="e7b40-110">Количество строк в таблице заголовков не соответствует количеству строк в таблице проводок.</span><span class="sxs-lookup"><span data-stu-id="e7b40-110">The line count on the header table does not match with the number of lines in the transaction table.</span></span>
  - <span data-ttu-id="e7b40-111">Сумма налога в таблице заголовков не соответствует сумме налога в строках.</span><span class="sxs-lookup"><span data-stu-id="e7b40-111">Taxes on the header table do not match the tax amount on the lines.</span></span> 
  
<span data-ttu-id="e7b40-112">Если в процесс разноски операций передаются несогласованные проводки, создаются противоречивые накладные по продажам и журналы платежей, что в результате приводит к сбою всего процесса разноски операций.</span><span class="sxs-lookup"><span data-stu-id="e7b40-112">When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</span></span> <span data-ttu-id="e7b40-113">Восстановление журналов операций из подобного состояния сопряжено со сложными исправлениями данных в нескольких таблицах проводок.</span><span class="sxs-lookup"><span data-stu-id="e7b40-113">Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</span></span> <span data-ttu-id="e7b40-114">Программа проверки согласованности проводок розничной торговли предотвращает подобные проблемы.</span><span class="sxs-lookup"><span data-stu-id="e7b40-114">The retail transaction consistency checker prevents such issues.</span></span>

<span data-ttu-id="e7b40-115">На следующей диаграмме представлен процесс разноски с использованием программы проверки согласованности проводок.</span><span class="sxs-lookup"><span data-stu-id="e7b40-115">The following chart illustrates the posting process with the transaction consistency checker.</span></span>

<span data-ttu-id="e7b40-116">![Процесс разноски журналов операций с использованием программы проверки согласованности проводок розничной торговли](./media/validchecker.png "Процесс разноски журналов операций с использованием программы проверки согласованности проводок розничной торговли")</span><span class="sxs-lookup"><span data-stu-id="e7b40-116">![Statement posting process with retail transaction consistency checker](./media/validchecker.png "Statement posting process with retail transaction consistency checker")</span></span>

<span data-ttu-id="e7b40-117">Процесс пакетной обработки **Проверить проводки магазина** проверяет согласованность таблиц проводок розничной торговли для следующих сценариев.</span><span class="sxs-lookup"><span data-stu-id="e7b40-117">The **Validate store transactions** batch process checks the consistency of the retail transaction tables for the following scenarios.</span></span>

- <span data-ttu-id="e7b40-118">Счет клиента — проверяется, что счет клиента в таблицах проводок розничной торговли присутствует в справочнике клиентов в головном офисе.</span><span class="sxs-lookup"><span data-stu-id="e7b40-118">Customer account - Validates that the customer account in the retail transaction tables exists in the HQ customer master.</span></span>
- <span data-ttu-id="e7b40-119">Количество строк — проверяется соответствие количества строк, указанного в таблице заголовков проводок, количеству строк в таблицах проводок продаж.</span><span class="sxs-lookup"><span data-stu-id="e7b40-119">Line count - Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</span></span>

## <a name="set-up-the-consistency-checker"></a><span data-ttu-id="e7b40-120">Настройка программы проверки согласованности</span><span class="sxs-lookup"><span data-stu-id="e7b40-120">Set up the consistency checker</span></span>
<span data-ttu-id="e7b40-121">Процесс пакетной обработки "Проверить проводки магазина" в разделе **Розничная торговля \> ИТ розничной торговли \> Разноска POS**, для периодического выполнения.</span><span class="sxs-lookup"><span data-stu-id="e7b40-121">Configure the "Validate store transactions" batch process, at **Retail \> Retail IT \> POS posting**, for periodic runs.</span></span> <span data-ttu-id="e7b40-122">Пакетное задание можно запланировать на основе организационной иерархии магазина, аналогично тому, как настраиваются процессы "Пакетный расчет журналов операций" и "Пакетная разноска журналов операций".</span><span class="sxs-lookup"><span data-stu-id="e7b40-122">The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</span></span> <span data-ttu-id="e7b40-123">Рекомендует настроить этот процесс пакетной обработки таким образом, чтобы он выполнялся несколько раз в день, и запланировать его выполнение на конец каждого выполнения P-задания.</span><span class="sxs-lookup"><span data-stu-id="e7b40-123">We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</span></span>

## <a name="results-of-validation-process"></a><span data-ttu-id="e7b40-124">Результаты выполнения процесса проверки</span><span class="sxs-lookup"><span data-stu-id="e7b40-124">Results of validation process</span></span>
<span data-ttu-id="e7b40-125">Результаты проверки, выполненной процессом пакетной обработки, отмечаются в соответствующей проводке розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="e7b40-125">The results of the validation check by the batch process are tagged on the appropriate retail transaction.</span></span> <span data-ttu-id="e7b40-126">В поле **Статус проверки** в записи проводки розничной торговли отображается значение **Успешно** или **Ошибка**, а дата последнего выполнения проверки отображается в поле **Время последней проверки**.</span><span class="sxs-lookup"><span data-stu-id="e7b40-126">The **Validation status** field on the retail transaction record is either set to **Successful** or **Error**, and the date of the last validation run appears on the **Last validation time** field.</span></span>

<span data-ttu-id="e7b40-127">Для просмотра более подробного описательного текста ошибки проверки выберите соответствующую запись проводки магазина розничной торговли и нажмите кнопку **Ошибки проверки**.</span><span class="sxs-lookup"><span data-stu-id="e7b40-127">To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the **Validation errors** button.</span></span>

<span data-ttu-id="e7b40-128">Проводки, которые не прошли проверку, и еще не проверенные проводки не передаются в журналы операций.</span><span class="sxs-lookup"><span data-stu-id="e7b40-128">Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</span></span> <span data-ttu-id="e7b40-129">Во время выполнения процесса "Создать строки журнала операций" пользователи будут получать уведомления о проводках, которые могли бы быть включены в журнал операций, но не были включены.</span><span class="sxs-lookup"><span data-stu-id="e7b40-129">During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</span></span>

<span data-ttu-id="e7b40-130">Если обнаружена ошибка проверки, ее можно исправить, только обратившись в службу поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="e7b40-130">If a validation error is found, the only way to fix the error is to contact Microsoft Support.</span></span> <span data-ttu-id="e7b40-131">В будущих выпусках для пользователей будет добавлен возможность исправлять записи, вызвавшие сбой, в интерфейсе пользователя.</span><span class="sxs-lookup"><span data-stu-id="e7b40-131">In a future release, capability will be added so that users can fix the records that failed through the user interface.</span></span> <span data-ttu-id="e7b40-132">Также будут предусмотрены возможности ведения журнала и аудита для отслеживания истории таких изменений.</span><span class="sxs-lookup"><span data-stu-id="e7b40-132">Logging and auditing capabilities will also be made available to trace the history of the modifications.</span></span>

> [!NOTE]
> <span data-ttu-id="e7b40-133">В будущих выпусках будут добавлены дополнительные правила проверки для поддержки других сценариев.</span><span class="sxs-lookup"><span data-stu-id="e7b40-133">Additional validation rules to support more scenarios will be added in a future release.</span></span>
