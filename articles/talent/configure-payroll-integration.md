---
title: Настройка интеграции зарплаты между Talent и Dayforce
description: В этом разделе объясняется, как настроить интеграцию между Microsoft Dynamics 365 for Talent и Ceridian Dayforce таким образом, чтобы вы могли обработать период оплаты.
author: jcart1106
manager: AnnBe
ms.date: 07/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fcddf82cffb9f0ba94b83eb21809b810585ebc9e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "305921"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="72bba-103">Настройка интеграции зарплаты между Talent и Dayforce</span><span class="sxs-lookup"><span data-stu-id="72bba-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="72bba-104">Интеграция между Microsoft Dynamics 365 for Talent и Ceridian Dayforce зависит от ряда действий настройки, описанных в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="72bba-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="72bba-105">Необходимо настроить интеграцию в Talent и Dayforce перед обработкой периода оплаты.</span><span class="sxs-lookup"><span data-stu-id="72bba-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="72bba-106">При использовании службы, например Dayforce, для выполнения оплаты, необходимо включить интеграцию в Talent.</span><span class="sxs-lookup"><span data-stu-id="72bba-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="72bba-107">Интеграция требует определенных данных из Talent.</span><span class="sxs-lookup"><span data-stu-id="72bba-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="72bba-108">Таким образом необходимо убедиться, что данные, отображаемые в Dayforce, настроены в Talent таким образом, чтобы поддерживать интеграцию.</span><span class="sxs-lookup"><span data-stu-id="72bba-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="72bba-109">Интеграция использует следующие широкие категории данных:</span><span class="sxs-lookup"><span data-stu-id="72bba-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="72bba-110">Данные управления персоналом</span><span class="sxs-lookup"><span data-stu-id="72bba-110">Human resources data</span></span>
- <span data-ttu-id="72bba-111">Данные о компенсациях</span><span class="sxs-lookup"><span data-stu-id="72bba-111">Compensation data</span></span>
- <span data-ttu-id="72bba-112">Данные о заработной плате, например циклы оплаты, периоды оплаты и коды начисления зарплаты</span><span class="sxs-lookup"><span data-stu-id="72bba-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="72bba-113">Данные о работнике</span><span class="sxs-lookup"><span data-stu-id="72bba-113">Worker data</span></span>

<span data-ttu-id="72bba-114">В этом разделе описываются шаги, которые необходимо выполнить, чтобы включить интеграцию.</span><span class="sxs-lookup"><span data-stu-id="72bba-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="72bba-115">Здесь также объясняются типы данных и сведения о конфигурации, которые необходимы для интеграции.</span><span class="sxs-lookup"><span data-stu-id="72bba-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="72bba-116">Включение интеграции</span><span class="sxs-lookup"><span data-stu-id="72bba-116">Enable the integration</span></span>

<span data-ttu-id="72bba-117">В Talent необходимо включить интеграцию и ввести информацию о конфигурации для подключения к Dayforce.</span><span class="sxs-lookup"><span data-stu-id="72bba-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="72bba-118">Если требуется, чтобы проводки ГК, которые производятся, импортировались в Microsoft Dynamics 365 for Finance and Operations, также необходимо установить учетную запись хранилища Microsoft Azure и ввести строку подключения хранилища Azure в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="72bba-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="72bba-119">Чтобы включить интеграцию в Talent, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="72bba-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="72bba-120">На странице **Администрирование системы** выберите **Конфигурация интеграции**.</span><span class="sxs-lookup"><span data-stu-id="72bba-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="72bba-121">Введите безопасную конечную точку FTP и путь к безопасной папке FTP.</span><span class="sxs-lookup"><span data-stu-id="72bba-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="72bba-122">Введите имя пользователя и пароль пользователя, который будет иметь доступ к безопасной конечной точке и пути к папке FTP.</span><span class="sxs-lookup"><span data-stu-id="72bba-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="72bba-123">Проверьте подключение, как требуется, а также установите для параметра **Включить интеграцию зарплаты** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="72bba-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="72bba-124">При включении интеграции создаются пакет экспорта данных и файлы, и задается значение частоты.</span><span class="sxs-lookup"><span data-stu-id="72bba-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="72bba-125">Можно изменить эту частоту, как требуется.</span><span class="sxs-lookup"><span data-stu-id="72bba-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="72bba-126">Дополнительные сведения об учетных записях хранилища Azure и строке подключения хранилища Azure см. в следующих разделах Azure:</span><span class="sxs-lookup"><span data-stu-id="72bba-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="72bba-127">Об учетных записях хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="72bba-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="72bba-128">Настройка строки подключения хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="72bba-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="72bba-129">Настройка данных</span><span class="sxs-lookup"><span data-stu-id="72bba-129">Configure your data</span></span> 

<span data-ttu-id="72bba-130">Для обработки зарплаты необходимо настроить данные управления персоналом в Talent.</span><span class="sxs-lookup"><span data-stu-id="72bba-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="72bba-131">Необходимо настроить организационные данные, такие как задания и должности, вместе со сведениями о льготах и компенсациях.</span><span class="sxs-lookup"><span data-stu-id="72bba-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="72bba-132">Эта информация содержит сведения о занятости, оплате и вычетах, которые необходимы для формирования заработной платы сотрудника.</span><span class="sxs-lookup"><span data-stu-id="72bba-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="72bba-133">Данные управления персоналом</span><span class="sxs-lookup"><span data-stu-id="72bba-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="72bba-134">Льготы</span><span class="sxs-lookup"><span data-stu-id="72bba-134">Benefits</span></span> 

<span data-ttu-id="72bba-135">Человеческие ресурсы обеспечивают инструменты для настройки и поддержки льгот, вычетов и планов компенсации работникам, которые организация предлагает или обрабатывает для своих работников.</span><span class="sxs-lookup"><span data-stu-id="72bba-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="72bba-136">При создании льгот имейте в виду следующие данные и конфигурации, которые используются в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="72bba-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="72bba-137">Планы льгот</span><span class="sxs-lookup"><span data-stu-id="72bba-137">Benefit plans</span></span>

- <span data-ttu-id="72bba-138">План (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-138">Plan (required)</span></span>
- <span data-ttu-id="72bba-139">Тип (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-139">Type (required)</span></span>
- <span data-ttu-id="72bba-140">Влияние на зарплату (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-140">Payroll impact (required)</span></span>
- <span data-ttu-id="72bba-141">Погасить задолженность</span><span class="sxs-lookup"><span data-stu-id="72bba-141">Recover arrears</span></span>
- <span data-ttu-id="72bba-142">Метод вычета</span><span class="sxs-lookup"><span data-stu-id="72bba-142">Deduction method</span></span>
- <span data-ttu-id="72bba-143">Приоритет вычета</span><span class="sxs-lookup"><span data-stu-id="72bba-143">Deduction priority</span></span>
- <span data-ttu-id="72bba-144">Период лимита</span><span class="sxs-lookup"><span data-stu-id="72bba-144">Limit period</span></span>
- <span data-ttu-id="72bba-145">Сумма лимита</span><span class="sxs-lookup"><span data-stu-id="72bba-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="72bba-146">Льготы</span><span class="sxs-lookup"><span data-stu-id="72bba-146">Benefits</span></span>

- <span data-ttu-id="72bba-147">План (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-147">Plan (required)</span></span>
- <span data-ttu-id="72bba-148">Тип (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-148">Type (required)</span></span>
- <span data-ttu-id="72bba-149">Параметр (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-149">Option (required)</span></span>
- <span data-ttu-id="72bba-150">Код льготы (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-150">Benefit ID (required)</span></span>
- <span data-ttu-id="72bba-151">Частота</span><span class="sxs-lookup"><span data-stu-id="72bba-151">Frequency</span></span>
- <span data-ttu-id="72bba-152">База</span><span class="sxs-lookup"><span data-stu-id="72bba-152">Basis</span></span>
- <span data-ttu-id="72bba-153">Сумма или ставка</span><span class="sxs-lookup"><span data-stu-id="72bba-153">Amount or rate</span></span>
- <span data-ttu-id="72bba-154">Код дохода</span><span class="sxs-lookup"><span data-stu-id="72bba-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="72bba-155">Поддерживаемые частоты</span><span class="sxs-lookup"><span data-stu-id="72bba-155">Supported frequencies</span></span> 

- <span data-ttu-id="72bba-156">Еженедельно</span><span class="sxs-lookup"><span data-stu-id="72bba-156">Weekly</span></span>
- <span data-ttu-id="72bba-157">Один раз в две недели</span><span class="sxs-lookup"><span data-stu-id="72bba-157">Bi-weekly</span></span>
- <span data-ttu-id="72bba-158">Два раза в месяц</span><span class="sxs-lookup"><span data-stu-id="72bba-158">Semi-monthly</span></span>
- <span data-ttu-id="72bba-159">Один раз в месяц</span><span class="sxs-lookup"><span data-stu-id="72bba-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="72bba-160">Поддерживаемые базы</span><span class="sxs-lookup"><span data-stu-id="72bba-160">Supported bases</span></span> 

- <span data-ttu-id="72bba-161">Фиксированная сумма</span><span class="sxs-lookup"><span data-stu-id="72bba-161">Fixed amount</span></span>
- <span data-ttu-id="72bba-162">Процент дохода</span><span class="sxs-lookup"><span data-stu-id="72bba-162">Percent of earnings</span></span>
- <span data-ttu-id="72bba-163">Продуктивные часы</span><span class="sxs-lookup"><span data-stu-id="72bba-163">Productive hours</span></span>

<span data-ttu-id="72bba-164">Dayforce создает следующие вычеты на основе влияния на зарплату, которое определено в плане льгот.</span><span class="sxs-lookup"><span data-stu-id="72bba-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="72bba-165">Выбор в Talent</span><span class="sxs-lookup"><span data-stu-id="72bba-165">Selection in Talent</span></span>        | <span data-ttu-id="72bba-166">Результат в Dayforce</span><span class="sxs-lookup"><span data-stu-id="72bba-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="72bba-167">None</span><span class="sxs-lookup"><span data-stu-id="72bba-167">None</span></span>                       | <span data-ttu-id="72bba-168">Вычет не создается.</span><span class="sxs-lookup"><span data-stu-id="72bba-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="72bba-169">Только удержание</span><span class="sxs-lookup"><span data-stu-id="72bba-169">Deduction only</span></span>             | <span data-ttu-id="72bba-170">Вычет сотрудника будет создан.</span><span class="sxs-lookup"><span data-stu-id="72bba-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="72bba-171">Только вклад</span><span class="sxs-lookup"><span data-stu-id="72bba-171">Contribution only</span></span>          | <span data-ttu-id="72bba-172">Вычет работодателя будет создан.</span><span class="sxs-lookup"><span data-stu-id="72bba-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="72bba-173">Удержание и вклад</span><span class="sxs-lookup"><span data-stu-id="72bba-173">Deduction and contribution</span></span> | <span data-ttu-id="72bba-174">Создаются вычеты сотрудников и работодателя.</span><span class="sxs-lookup"><span data-stu-id="72bba-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="72bba-175">Дополнительные сведения о том, как определять и управлять программами льгот, см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="72bba-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="72bba-176">Реализация программы льгот сотрудника</span><span class="sxs-lookup"><span data-stu-id="72bba-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="72bba-177">Создание новой льготы</span><span class="sxs-lookup"><span data-stu-id="72bba-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="72bba-178">Определение правил и политик проверки прав на льготы</span><span class="sxs-lookup"><span data-stu-id="72bba-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="72bba-179">Регистрация и удаление льгот для работников</span><span class="sxs-lookup"><span data-stu-id="72bba-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="72bba-180">Компенсация</span><span class="sxs-lookup"><span data-stu-id="72bba-180">Compensation</span></span> 

<span data-ttu-id="72bba-181">Управление компенсациями используется для управления предоставлением базовой оплаты и вознаграждений.</span><span class="sxs-lookup"><span data-stu-id="72bba-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="72bba-182">Тарифные ставки и единовременные надбавки контролируются с помощью планов фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="72bba-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="72bba-183">Поощрительные выплаты, такие как премии, вознаграждения за производительность, опционы на покупку акций и гранты, а также одноразовые компенсации, контролируются с помощью планов переменных компенсаций.</span><span class="sxs-lookup"><span data-stu-id="72bba-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="72bba-184">Dayforce использует сведения о компенсации для расчета почасовой или годовой ставки сотрудника.</span><span class="sxs-lookup"><span data-stu-id="72bba-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="72bba-185">Требуются планы фиксированной компенсации и преобразования ставки оплаты.</span><span class="sxs-lookup"><span data-stu-id="72bba-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="72bba-186">Сотрудники должны быть связаны с планом фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="72bba-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="72bba-187">Дополнительные сведения о планах компенсации см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="72bba-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="72bba-188">Создание планов фиксированной компенсации</span><span class="sxs-lookup"><span data-stu-id="72bba-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="72bba-189">Создание планов переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="72bba-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="72bba-190">Разработка структуры и планов зарплаты/компенсации</span><span class="sxs-lookup"><span data-stu-id="72bba-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="72bba-191">Обработка компенсаций</span><span class="sxs-lookup"><span data-stu-id="72bba-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="72bba-192">Определение процесса компенсации и расчет результатов</span><span class="sxs-lookup"><span data-stu-id="72bba-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="72bba-193">Включение сотрудника в план фиксированных компенсаций</span><span class="sxs-lookup"><span data-stu-id="72bba-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="72bba-194">Включение сотрудника в план переменных компенсаций</span><span class="sxs-lookup"><span data-stu-id="72bba-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="72bba-195">Должности</span><span class="sxs-lookup"><span data-stu-id="72bba-195">Jobs</span></span> 

<span data-ttu-id="72bba-196">Должностные обязанности — это набор задач и обязанностей, которые возлагаются на занимающее эту задание лицо.</span><span class="sxs-lookup"><span data-stu-id="72bba-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="72bba-197">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="72bba-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="72bba-198">Настройка компонентов должности</span><span class="sxs-lookup"><span data-stu-id="72bba-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="72bba-199">Определение новых заданий</span><span class="sxs-lookup"><span data-stu-id="72bba-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="72bba-200">Должности</span><span class="sxs-lookup"><span data-stu-id="72bba-200">Positions</span></span>

<span data-ttu-id="72bba-201">Позиция — это индивидуальный экземпляр должности.</span><span class="sxs-lookup"><span data-stu-id="72bba-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="72bba-202">Например, должность "Менеджер по продажам (восток)" — это одна из должностей, связанных с должностными обязанностями "Менеджер по продажам".</span><span class="sxs-lookup"><span data-stu-id="72bba-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="72bba-203">Должность существует в отделе.</span><span class="sxs-lookup"><span data-stu-id="72bba-203">A position exists in a department.</span></span> <span data-ttu-id="72bba-204">Только один работник может быть связан с каждой должностью.</span><span class="sxs-lookup"><span data-stu-id="72bba-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="72bba-205">Учитывайте следующие данные и конфигурацию при настройке должностей:</span><span class="sxs-lookup"><span data-stu-id="72bba-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="72bba-206">Должность (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-206">Position (required)</span></span>
- <span data-ttu-id="72bba-207">Описание (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-207">Description (required)</span></span>
- <span data-ttu-id="72bba-208">Должностные обязанности (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-208">Job (required)</span></span>
- <span data-ttu-id="72bba-209">Отдел (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-209">Department (required)</span></span>
- <span data-ttu-id="72bba-210">Тип должности (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-210">Position type (required)</span></span>
- <span data-ttu-id="72bba-211">Эквивалент полной занятости</span><span class="sxs-lookup"><span data-stu-id="72bba-211">Full-time equivalent</span></span>
- <span data-ttu-id="72bba-212">Обычные часы за год (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="72bba-213">Оплачивается юридическим лицом (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="72bba-214">Цикл оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-214">Pay cycle (required)</span></span>
- <span data-ttu-id="72bba-215">Финансовая аналитика по умолчанию — центр затрат (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="72bba-216">Назначение работника — работник, начало назначения, окончание назначения, код причины</span><span class="sxs-lookup"><span data-stu-id="72bba-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="72bba-217">Если несколько должностей в одном отделе связаны с одними и теми же должностными обязанностями, они объединяются в одну должность в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="72bba-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="72bba-218">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="72bba-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="72bba-219">Организация трудовых ресурсов с использованием подразделений, должностей и штатных единиц</span><span class="sxs-lookup"><span data-stu-id="72bba-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="72bba-220">Настройка должностей</span><span class="sxs-lookup"><span data-stu-id="72bba-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="72bba-221">Отделы</span><span class="sxs-lookup"><span data-stu-id="72bba-221">Departments</span></span>

<span data-ttu-id="72bba-222">Подразделение — это операционная единица, которая представляет собой категорию или функциональную область в организации.</span><span class="sxs-lookup"><span data-stu-id="72bba-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="72bba-223">Подразделение отвечает за конкретную область деятельности организации, например продажи, бухгалтерский учет или управление персоналом.</span><span class="sxs-lookup"><span data-stu-id="72bba-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="72bba-224">Подразделения можно использовать для формирования отчетности по функциональным областям.</span><span class="sxs-lookup"><span data-stu-id="72bba-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="72bba-225">Подразделения могут нести ответственность за прибыли и убытки.</span><span class="sxs-lookup"><span data-stu-id="72bba-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="72bba-226">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="72bba-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="72bba-227">Создание подразделения и связывание его с иерархией подразделений</span><span class="sxs-lookup"><span data-stu-id="72bba-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="72bba-228">Определение новых подразделений</span><span class="sxs-lookup"><span data-stu-id="72bba-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="72bba-229">Циклы оплаты и платежные периоды</span><span class="sxs-lookup"><span data-stu-id="72bba-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="72bba-230">Цикл оплаты определяет, как часто рассчитывается зарплата и определенные дни, когда работники получают зарплату.</span><span class="sxs-lookup"><span data-stu-id="72bba-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="72bba-231">Например, цикл оплаты может быть ежемесячным, и сотрудникам может выплачиваться зарплата в последний день месяца.</span><span class="sxs-lookup"><span data-stu-id="72bba-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="72bba-232">Кроме того, цикл оплаты может быть еженедельным, а сотрудники могут получать зарплату по вторникам после завершения периода оплаты.</span><span class="sxs-lookup"><span data-stu-id="72bba-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="72bba-233">Циклы оплаты назначаются должностям для управления выплатами работникам для этих должностей.</span><span class="sxs-lookup"><span data-stu-id="72bba-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="72bba-234">После создания циклов зарплаты можно создать платежные периоды для каждого цикла.</span><span class="sxs-lookup"><span data-stu-id="72bba-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="72bba-235">Каждый платежный период включает дату оплаты по умолчанию, которая основана на информации, предоставленной вами.</span><span class="sxs-lookup"><span data-stu-id="72bba-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="72bba-236">Однако можно изменить дату платежа по умолчанию в платежный период для учета исключений, например, когда дата оплаты приходится на праздник.</span><span class="sxs-lookup"><span data-stu-id="72bba-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="72bba-237">Dayforce использует следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="72bba-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="72bba-238">Цикл оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-238">Pay cycle (required)</span></span>
- <span data-ttu-id="72bba-239">Частота циклов оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="72bba-240">Дата начала периода (первый период оплаты обязателен)</span><span class="sxs-lookup"><span data-stu-id="72bba-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="72bba-241">Дата платежа по умолчанию (первый период оплаты обязателен)</span><span class="sxs-lookup"><span data-stu-id="72bba-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="72bba-242">Эта информация интегрирована с Dayforce как платежные группы, и разделяется по странам или регионам для каждого цикла оплаты.</span><span class="sxs-lookup"><span data-stu-id="72bba-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="72bba-243">Хотя бы один платежный период должен быть создан до интеграции.</span><span class="sxs-lookup"><span data-stu-id="72bba-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="72bba-244">Dayforce создает календари группы оплаты и даты оплаты на основе даты начала первого периода оплаты и даты оплаты по умолчанию, настроенных в Talent.</span><span class="sxs-lookup"><span data-stu-id="72bba-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="72bba-245">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="72bba-245">Earning codes</span></span>

<span data-ttu-id="72bba-246">Коды доходов уникально определяют каждый типа доходов, которые работники получают.</span><span class="sxs-lookup"><span data-stu-id="72bba-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="72bba-247">Эти коды имеют различные параметры, которые относятся к доходам, таких как правила учета, налоговые законы, требования к отчетности и возможности брутто в большую сторону.</span><span class="sxs-lookup"><span data-stu-id="72bba-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="72bba-248">Dayforce использует следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="72bba-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="72bba-249">Код дохода (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-249">Earning Code (required)</span></span>
- <span data-ttu-id="72bba-250">описание</span><span class="sxs-lookup"><span data-stu-id="72bba-250">Description</span></span>
- <span data-ttu-id="72bba-251">Единица измерения</span><span class="sxs-lookup"><span data-stu-id="72bba-251">Unit of measure</span></span>
- <span data-ttu-id="72bba-252">Продуктивный</span><span class="sxs-lookup"><span data-stu-id="72bba-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="72bba-253">Данные о работнике</span><span class="sxs-lookup"><span data-stu-id="72bba-253">Worker data</span></span>

<span data-ttu-id="72bba-254">Записи о различных типах сотрудников, которые имеются у вас, важны для вашей системы управления персоналом и системы расчета заработной платы.</span><span class="sxs-lookup"><span data-stu-id="72bba-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="72bba-255">Вводимые данные могут использоваться для отслеживания сведений о работниках и личной информации.</span><span class="sxs-lookup"><span data-stu-id="72bba-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="72bba-256">По работникам может храниться следующая информация.</span><span class="sxs-lookup"><span data-stu-id="72bba-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="72bba-257">**Основная** — базовые сведения о работнике, такие как контактные данные, демографические данные, идентифицирующие сведения, состав семье, сведения о службе в армии, данные об иностранных сотрудниках, персональные контакты и контакты на случай экстренных ситуаций.</span><span class="sxs-lookup"><span data-stu-id="72bba-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="72bba-258">**Занятость** — сведения о занятости работников, такие как участие в компании или организации, должность, дату начала и завершения работы, способность к работе, условия найма, пенсия, отпуска и сведения о переездах.</span><span class="sxs-lookup"><span data-stu-id="72bba-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="72bba-259">**Отпуск и отсутствие** — сведения об отпусках или пропуска работника, рабочие календари, проводки отсутствия и соответствующие настройки.</span><span class="sxs-lookup"><span data-stu-id="72bba-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="72bba-260">**Заработная плата и компенсации** — сведения о планах вознаграждениях и зарплате работника, такие как премии, комиссии, налоги, выход на пенсию и вычеты из зарплаты.</span><span class="sxs-lookup"><span data-stu-id="72bba-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="72bba-261">При вводе сведений о работнике имейте в виду следующие данные и конфигурации, которые используются в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="72bba-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="72bba-262">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="72bba-262">General information</span></span>

- <span data-ttu-id="72bba-263">Табельный номер (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-263">Personnel number (required)</span></span>
- <span data-ttu-id="72bba-264">Имя (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-264">First name (required)</span></span>
- <span data-ttu-id="72bba-265">Фамилия (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-265">Last name (required)</span></span>
- <span data-ttu-id="72bba-266">Отчество</span><span class="sxs-lookup"><span data-stu-id="72bba-266">Middle name</span></span>
- <span data-ttu-id="72bba-267">Дата начала стажа</span><span class="sxs-lookup"><span data-stu-id="72bba-267">Seniority date</span></span>
- <span data-ttu-id="72bba-268">Известно как</span><span class="sxs-lookup"><span data-stu-id="72bba-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="72bba-269">Личная информация</span><span class="sxs-lookup"><span data-stu-id="72bba-269">Personal information</span></span>

- <span data-ttu-id="72bba-270">Семейное положение (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-270">Marital status (required)</span></span>
- <span data-ttu-id="72bba-271">Дата рождения (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-271">Birth date (required)</span></span>
- <span data-ttu-id="72bba-272">Пол (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-272">Gender (required)</span></span>
- <span data-ttu-id="72bba-273">Лицо с инвалидностью</span><span class="sxs-lookup"><span data-stu-id="72bba-273">Person with disabilities</span></span>
- <span data-ttu-id="72bba-274">Национальность, регион страны (только в Мексике)</span><span class="sxs-lookup"><span data-stu-id="72bba-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="72bba-275">Адресная информация</span><span class="sxs-lookup"><span data-stu-id="72bba-275">Address information</span></span>

- <span data-ttu-id="72bba-276">Основной (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-276">Primary (required)</span></span>
- <span data-ttu-id="72bba-277">Страна/регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-277">Country/region (required)</span></span>
- <span data-ttu-id="72bba-278">Почтовый индекс (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-278">Postal code (required)</span></span>
- <span data-ttu-id="72bba-279">Номер дома (обязательно) (только для Мексики)</span><span class="sxs-lookup"><span data-stu-id="72bba-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="72bba-280">Дополнение здания (только в Мексике)</span><span class="sxs-lookup"><span data-stu-id="72bba-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="72bba-281">Город (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-281">City (required)</span></span>
- <span data-ttu-id="72bba-282">Регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-282">State (required)</span></span>
- <span data-ttu-id="72bba-283">Район (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="72bba-284">Контактная информация</span><span class="sxs-lookup"><span data-stu-id="72bba-284">Contact information</span></span> 

- <span data-ttu-id="72bba-285">Основной (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-285">Primary (required)</span></span>
- <span data-ttu-id="72bba-286">Контактный номер (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-286">Contact number (required)</span></span>
- <span data-ttu-id="72bba-287">Расширение</span><span class="sxs-lookup"><span data-stu-id="72bba-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="72bba-288">Информация по зарплате и коды дохода</span><span class="sxs-lookup"><span data-stu-id="72bba-288">Payroll information and earning codes</span></span>

<span data-ttu-id="72bba-289">Сотрудникам можно назначить конкретные доходы с заданной периодичностью оплаты и предпочтительный метод оплаты.</span><span class="sxs-lookup"><span data-stu-id="72bba-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="72bba-290">Следующие поля используются в Dayforce для обеспечения использования этих параметров и настроек.</span><span class="sxs-lookup"><span data-stu-id="72bba-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="72bba-291">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="72bba-291">Earning codes</span></span>

- <span data-ttu-id="72bba-292">Должность (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-292">Position (required)</span></span>
- <span data-ttu-id="72bba-293">Код дохода (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-293">Earning Code (required)</span></span>
- <span data-ttu-id="72bba-294">Частота (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-294">Frequency (required)</span></span>
- <span data-ttu-id="72bba-295">Сумма (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="72bba-296">Информация по зарплате</span><span class="sxs-lookup"><span data-stu-id="72bba-296">Payroll information</span></span>

- <span data-ttu-id="72bba-297">Способ оплаты</span><span class="sxs-lookup"><span data-stu-id="72bba-297">Payment Method</span></span>
- <span data-ttu-id="72bba-298">Экономический регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-298">Economic Region (required)</span></span>
- <span data-ttu-id="72bba-299">ИД льгот сотрудников</span><span class="sxs-lookup"><span data-stu-id="72bba-299">Employee Benefits ID</span></span>
- <span data-ttu-id="72bba-300">Идентификационный номер (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-300">National ID Number (required)</span></span>
- <span data-ttu-id="72bba-301">Номер документа о воинской службе</span><span class="sxs-lookup"><span data-stu-id="72bba-301">Military Service Number</span></span>
- <span data-ttu-id="72bba-302">Код смены (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-302">Shift ID (required)</span></span>
- <span data-ttu-id="72bba-303">Налоговой номер (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-303">Tax Number (required)</span></span>
- <span data-ttu-id="72bba-304">Код профсоюза (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-304">Union ID (required)</span></span>
- <span data-ttu-id="72bba-305">Идентификатор рабочего дня (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-305">Work Day ID (required)</span></span>
- <span data-ttu-id="72bba-306">Номер разрешения на работу</span><span class="sxs-lookup"><span data-stu-id="72bba-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="72bba-307">Для метода оплаты в Мексике поддерживает **Наличные деньги**, **Чек** (физический чек компании) и **Электронный платеж**.</span><span class="sxs-lookup"><span data-stu-id="72bba-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="72bba-308">Если способ оплаты не указан, **Чек** используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="72bba-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="72bba-309">Сведения о трудоустройстве</span><span class="sxs-lookup"><span data-stu-id="72bba-309">Employment details</span></span>

<span data-ttu-id="72bba-310">Подробная история занятости используется как ключевая информация для извлечения статуса найма, увольнения и повторного найма сотрудника в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="72bba-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="72bba-311">Dayforce поддерживает только одну активную запись о приеме на работу одновременно.</span><span class="sxs-lookup"><span data-stu-id="72bba-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="72bba-312">Дата начала трудоустройства (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-312">Employment start date (required)</span></span>
- <span data-ttu-id="72bba-313">Дата окончания занятости</span><span class="sxs-lookup"><span data-stu-id="72bba-313">Employment end date</span></span>
- <span data-ttu-id="72bba-314">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="72bba-314">Start date</span></span>
- <span data-ttu-id="72bba-315">Скорректированная дата приема на работу</span><span class="sxs-lookup"><span data-stu-id="72bba-315">Adjusted start date</span></span>
- <span data-ttu-id="72bba-316">Дата увольнения (обязательно после увольнения)</span><span class="sxs-lookup"><span data-stu-id="72bba-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="72bba-317">Причина увольнения (обязательно после увольнения)</span><span class="sxs-lookup"><span data-stu-id="72bba-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="72bba-318">Ключевые даты сотрудника получаются на основе следующих сведений.</span><span class="sxs-lookup"><span data-stu-id="72bba-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="72bba-319">Talent</span><span class="sxs-lookup"><span data-stu-id="72bba-319">Talent</span></span>                | <span data-ttu-id="72bba-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="72bba-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72bba-321">Самая последняя дата приема на работу</span><span class="sxs-lookup"><span data-stu-id="72bba-321">Most recent hire date</span></span> | <span data-ttu-id="72bba-322">Дата приема на работу для текущей записи истории занятости, которая еще не завершена</span><span class="sxs-lookup"><span data-stu-id="72bba-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="72bba-323">Дата увольнения</span><span class="sxs-lookup"><span data-stu-id="72bba-323">Termination date</span></span>      | <span data-ttu-id="72bba-324">Дата увольнения для текущей записи истории занятости, которая еще не завершена</span><span class="sxs-lookup"><span data-stu-id="72bba-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="72bba-325">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="72bba-325">Start date</span></span>            | <span data-ttu-id="72bba-326">Скорректированная дата приема на работу, дата приема на работу или дата приема на работу текущей неактивной записи история занятости</span><span class="sxs-lookup"><span data-stu-id="72bba-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="72bba-327">Дата первоначального приема на работу</span><span class="sxs-lookup"><span data-stu-id="72bba-327">Original hire date</span></span>    | <span data-ttu-id="72bba-328">Дата приема на работу самой ранней записи истории приема на работу</span><span class="sxs-lookup"><span data-stu-id="72bba-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="72bba-329">Компенсация</span><span class="sxs-lookup"><span data-stu-id="72bba-329">Compensation</span></span>

<span data-ttu-id="72bba-330">План фиксированной компенсации должен быть связан с каждой основной должностью работника на протяжении всего периода занятости.</span><span class="sxs-lookup"><span data-stu-id="72bba-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="72bba-331">Этот период начинается на даты, в которую сотрудник был нанят (или начальная дата приема на работу) и продолжается до увольнения.</span><span class="sxs-lookup"><span data-stu-id="72bba-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="72bba-332">Дата вступления в силу (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-332">Effective Date (required)</span></span>
- <span data-ttu-id="72bba-333">Срок действия</span><span class="sxs-lookup"><span data-stu-id="72bba-333">Expiration date</span></span>
- <span data-ttu-id="72bba-334">Ставка оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-334">Pay Rate (required)</span></span>
- <span data-ttu-id="72bba-335">Преобразования ставки оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="72bba-336">Годовой эквивалент (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="72bba-337">Почасовой эквивалент (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="72bba-338">Если сотрудник с почасовой оплатой имеет несколько должностей, фиксированная компенсация основной должности импортируется в Dayforce как базовая ставка/зарплата уровня сотрудника.</span><span class="sxs-lookup"><span data-stu-id="72bba-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="72bba-339">Дня неосновных должностей почасовая ставка сохраняется в соответствующей должности в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="72bba-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="72bba-340">Если штатный сотрудник имеет несколько должностей, суммарная почасовая ставка и годовая заработная плата для всех активных должностей определяется и используется в качестве базовой ставки/зарплаты уровня сотрудника.</span><span class="sxs-lookup"><span data-stu-id="72bba-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="72bba-341">Идентификационные номера</span><span class="sxs-lookup"><span data-stu-id="72bba-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="72bba-342">Код социального страхования</span><span class="sxs-lookup"><span data-stu-id="72bba-342">Social Security identifier</span></span> 

<span data-ttu-id="72bba-343">Каждый сотрудник должен иметь один первичный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="72bba-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="72bba-344">Этот идентификатор должен быть идентификатором типа **SSN**.</span><span class="sxs-lookup"><span data-stu-id="72bba-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="72bba-345">В Dayforce он автоматически извлекается как код социального страхования сотрудника, который необходим для приема на работу.</span><span class="sxs-lookup"><span data-stu-id="72bba-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="72bba-346">Основной (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-346">Primary (required)</span></span>
- <span data-ttu-id="72bba-347">Тип идентификации = "SSN"</span><span class="sxs-lookup"><span data-stu-id="72bba-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="72bba-348">Дата выпуска</span><span class="sxs-lookup"><span data-stu-id="72bba-348">Issued Date</span></span>
- <span data-ttu-id="72bba-349">Дата окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="72bba-349">Expiration Date</span></span>

<span data-ttu-id="72bba-350">Сотрудники могут объявить несколько идентификационных номеров для типа идентификатора **SSN**.</span><span class="sxs-lookup"><span data-stu-id="72bba-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="72bba-351">Тем не менее только запись, которая помечен как **Основная**, интегрируется в Dayforce, независимо от того, является ли номер активным или у него истек срок действия.</span><span class="sxs-lookup"><span data-stu-id="72bba-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="72bba-352">Банковские счета и выплаты</span><span class="sxs-lookup"><span data-stu-id="72bba-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="72bba-353">Необходимо ввести действительную информацию о банковском счете для любого сотрудника, который выбирает оплату через перевод на банковский счет.</span><span class="sxs-lookup"><span data-stu-id="72bba-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="72bba-354">Talent</span><span class="sxs-lookup"><span data-stu-id="72bba-354">Talent</span></span>                         | <span data-ttu-id="72bba-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="72bba-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72bba-356">Номер счета в банке (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="72bba-357">Код SWIFT (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-357">SWIFT code (required)</span></span>          | <span data-ttu-id="72bba-358">Поле **Код банка** используется при обработке зарплаты в Мексике.</span><span class="sxs-lookup"><span data-stu-id="72bba-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="72bba-359">Номер филиала (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="72bba-360">Тип банковского счета (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-360">Bank account type (required)</span></span>   | <span data-ttu-id="72bba-361">Поле **Тип счета** используется при обработке зарплаты в Мексике.</span><span class="sxs-lookup"><span data-stu-id="72bba-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="72bba-362">Поддерживаются значения **Выписка чека** и **Заработная плата**.</span><span class="sxs-lookup"><span data-stu-id="72bba-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="72bba-363">Работники, которые выбрали выплату переводом на банковский счет, должен предоставить ссылку на счет остатков, находящийся в юридическом лице с основным адресом в Мексике и связанный с действительным банковским счетом из мексиканского банка.</span><span class="sxs-lookup"><span data-stu-id="72bba-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="72bba-364">Все другие счета, не являющиеся счетами остатков, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="72bba-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="72bba-365">Адресная информация</span><span class="sxs-lookup"><span data-stu-id="72bba-365">Address information</span></span>

<span data-ttu-id="72bba-366">Каждый сотрудник должен иметь одно первичное местонахождение.</span><span class="sxs-lookup"><span data-stu-id="72bba-366">Every employee must have one primary location.</span></span> <span data-ttu-id="72bba-367">В Dayforce это расположение используется для определения основного места жительства сотрудника для целей налогообложения.</span><span class="sxs-lookup"><span data-stu-id="72bba-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="72bba-368">Основной (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-368">Primary (required)</span></span>
- <span data-ttu-id="72bba-369">Страна/регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-369">Country/region (required)</span></span>
- <span data-ttu-id="72bba-370">Почтовый индекс (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="72bba-371">Улица (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-371">Street (required)</span></span>
- <span data-ttu-id="72bba-372">Номер дома (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-372">Street Number (required)</span></span>
- <span data-ttu-id="72bba-373">Дополнение здания</span><span class="sxs-lookup"><span data-stu-id="72bba-373">Building Complement</span></span>
- <span data-ttu-id="72bba-374">Город (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-374">City (required)</span></span>
- <span data-ttu-id="72bba-375">Регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-375">State (required)</span></span>
- <span data-ttu-id="72bba-376">Район (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="72bba-377">Настройка данных для расчета заработной платы в США и Канаде</span><span class="sxs-lookup"><span data-stu-id="72bba-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="72bba-378">Если вы создаете оплату для сотрудников в США и Канаде, необходимо настроить следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="72bba-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="72bba-379">Обязательно указывать подразделения для должностей.</span><span class="sxs-lookup"><span data-stu-id="72bba-379">Departments are required on positions.</span></span>
- <span data-ttu-id="72bba-380">Центры затрат должен быть заданы как финансовые аналитики и должны быть первым элементом в строке финансовой аналитики по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="72bba-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="72bba-381">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="72bba-381">Job types</span></span>

<span data-ttu-id="72bba-382">Типы должностей используются для группирования похожих должностных обязанностей в категории.</span><span class="sxs-lookup"><span data-stu-id="72bba-382">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="72bba-383">Типы должностей обязательны для обработки зарплаты в США и Канаде.</span><span class="sxs-lookup"><span data-stu-id="72bba-383">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="72bba-384">Примеры типов должностей включают полный рабочий день и неполный рабочий день, или зарплата и почасовая оплата.</span><span class="sxs-lookup"><span data-stu-id="72bba-384">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="72bba-385">Типы должностей сопоставляются с Dayforce как типы зарплаты, которые указывают тип оплаты сотрудника: почасовая или оклад.</span><span class="sxs-lookup"><span data-stu-id="72bba-385">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="72bba-386">Требуются следующие типы должностей и описаний.</span><span class="sxs-lookup"><span data-stu-id="72bba-386">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="72bba-387">Тип задания</span><span class="sxs-lookup"><span data-stu-id="72bba-387">Job type</span></span>   | <span data-ttu-id="72bba-388">описание</span><span class="sxs-lookup"><span data-stu-id="72bba-388">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="72bba-389">Почасовая</span><span class="sxs-lookup"><span data-stu-id="72bba-389">Hourly</span></span>     | <span data-ttu-id="72bba-390">Почасовая</span><span class="sxs-lookup"><span data-stu-id="72bba-390">Hourly</span></span>      |
| <span data-ttu-id="72bba-391">Оклад</span><span class="sxs-lookup"><span data-stu-id="72bba-391">Salaried</span></span>   | <span data-ttu-id="72bba-392">Оклад</span><span class="sxs-lookup"><span data-stu-id="72bba-392">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="72bba-393">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="72bba-393">Position types</span></span> 

<span data-ttu-id="72bba-394">С помощью типов должностей описывается, является ли должность занятостью на полный рабочий день, на неполный рабочий день или какой-либо другой.</span><span class="sxs-lookup"><span data-stu-id="72bba-394">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="72bba-395">Типы должностей сопоставляются с Dayforce как классы зарплаты, которые указывают тип оплаты сотрудника: полная занятость или частичная занятость.</span><span class="sxs-lookup"><span data-stu-id="72bba-395">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="72bba-396">Требуются следующие типы должностей и описаний.</span><span class="sxs-lookup"><span data-stu-id="72bba-396">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="72bba-397">Тип должности</span><span class="sxs-lookup"><span data-stu-id="72bba-397">Position type</span></span>   | <span data-ttu-id="72bba-398">описание</span><span class="sxs-lookup"><span data-stu-id="72bba-398">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="72bba-399">Полная занятость</span><span class="sxs-lookup"><span data-stu-id="72bba-399">Full-time</span></span>       | <span data-ttu-id="72bba-400">Работник с полной занятостью</span><span class="sxs-lookup"><span data-stu-id="72bba-400">Full time employee</span></span> |
| <span data-ttu-id="72bba-401">Частичная занятость</span><span class="sxs-lookup"><span data-stu-id="72bba-401">Part-time</span></span>       | <span data-ttu-id="72bba-402">Работник с частичной занятостью</span><span class="sxs-lookup"><span data-stu-id="72bba-402">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="72bba-403">Коды оснований</span><span class="sxs-lookup"><span data-stu-id="72bba-403">Reason codes</span></span>

<span data-ttu-id="72bba-404">Коды оснований содержат сведения о статусе сотрудника.</span><span class="sxs-lookup"><span data-stu-id="72bba-404">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="72bba-405">Коды оснований сопоставляются с Dayforce как причины статуса, которые определяют причину изменения статус должности или найма сотрудника.</span><span class="sxs-lookup"><span data-stu-id="72bba-405">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="72bba-406">Требуются следующие коды причин и описания.</span><span class="sxs-lookup"><span data-stu-id="72bba-406">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="72bba-407">Код основания</span><span class="sxs-lookup"><span data-stu-id="72bba-407">Reason code</span></span>    | <span data-ttu-id="72bba-408">описание</span><span class="sxs-lookup"><span data-stu-id="72bba-408">Description</span></span>      | <span data-ttu-id="72bba-409">Применимые сценарии</span><span class="sxs-lookup"><span data-stu-id="72bba-409">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="72bba-410">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="72bba-410">RESIGNATION</span></span>    | <span data-ttu-id="72bba-411">Увольнение</span><span class="sxs-lookup"><span data-stu-id="72bba-411">Resignation</span></span>      | <span data-ttu-id="72bba-412">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="72bba-412">Terminate worker</span></span>     |
| <span data-ttu-id="72bba-413">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="72bba-413">TERMINATION</span></span>    | <span data-ttu-id="72bba-414">Завершение</span><span class="sxs-lookup"><span data-stu-id="72bba-414">Termination</span></span>      | <span data-ttu-id="72bba-415">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="72bba-415">Terminate worker</span></span>     |
| <span data-ttu-id="72bba-416">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="72bba-416">RETIREMENT</span></span>     | <span data-ttu-id="72bba-417">Выходное пособие</span><span class="sxs-lookup"><span data-stu-id="72bba-417">Retirement</span></span>       | <span data-ttu-id="72bba-418">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="72bba-418">Terminate worker</span></span>     |
| <span data-ttu-id="72bba-419">ПРОЧЕЕ</span><span class="sxs-lookup"><span data-stu-id="72bba-419">OTHER</span></span>          | <span data-ttu-id="72bba-420">Другие причины</span><span class="sxs-lookup"><span data-stu-id="72bba-420">Other Reasons</span></span>    | <span data-ttu-id="72bba-421">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="72bba-421">Terminate worker</span></span>     |
| <span data-ttu-id="72bba-422">DEATH</span><span class="sxs-lookup"><span data-stu-id="72bba-422">DEATH</span></span>          | <span data-ttu-id="72bba-423">Смерть</span><span class="sxs-lookup"><span data-stu-id="72bba-423">Death</span></span>            | <span data-ttu-id="72bba-424">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="72bba-424">Terminate worker</span></span>     |
| <span data-ttu-id="72bba-425">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="72bba-425">LEAVEOFABSENCE</span></span> | <span data-ttu-id="72bba-426">Отпуск</span><span class="sxs-lookup"><span data-stu-id="72bba-426">Leave of Absence</span></span> | <span data-ttu-id="72bba-427">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="72bba-427">Terminate worker</span></span>     |
| <span data-ttu-id="72bba-428">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="72bba-428">CONTRACTEND</span></span>    | <span data-ttu-id="72bba-429">Завершение контракта</span><span class="sxs-lookup"><span data-stu-id="72bba-429">End of Contract</span></span>  | <span data-ttu-id="72bba-430">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="72bba-430">Terminate worker</span></span>     |
| <span data-ttu-id="72bba-431">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="72bba-431">SALARYCHANGE</span></span>   | <span data-ttu-id="72bba-432">Изменение зарплаты</span><span class="sxs-lookup"><span data-stu-id="72bba-432">Change of Salary</span></span> | <span data-ttu-id="72bba-433">Компенсация</span><span class="sxs-lookup"><span data-stu-id="72bba-433">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="72bba-434">Семейное положение</span><span class="sxs-lookup"><span data-stu-id="72bba-434">Marital status</span></span>

<span data-ttu-id="72bba-435">Значения семейного положения сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="72bba-435">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="72bba-436">В следующей таблице показано, как значения семейного положения сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="72bba-436">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="72bba-437">Talent</span><span class="sxs-lookup"><span data-stu-id="72bba-437">Talent</span></span>                 | <span data-ttu-id="72bba-438">Dayforce</span><span class="sxs-lookup"><span data-stu-id="72bba-438">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="72bba-439">Женат/замужем</span><span class="sxs-lookup"><span data-stu-id="72bba-439">Married</span></span>                | <span data-ttu-id="72bba-440">Женат/замужем</span><span class="sxs-lookup"><span data-stu-id="72bba-440">Married</span></span>              |
| <span data-ttu-id="72bba-441">Один</span><span class="sxs-lookup"><span data-stu-id="72bba-441">Single</span></span>                 | <span data-ttu-id="72bba-442">Один</span><span class="sxs-lookup"><span data-stu-id="72bba-442">Single</span></span>               |
| <span data-ttu-id="72bba-443">Вдовец/вдова</span><span class="sxs-lookup"><span data-stu-id="72bba-443">Widowed</span></span>                | <span data-ttu-id="72bba-444">Вдовец/вдова</span><span class="sxs-lookup"><span data-stu-id="72bba-444">Widowed</span></span>              |
| <span data-ttu-id="72bba-445">Разведен/разведена</span><span class="sxs-lookup"><span data-stu-id="72bba-445">Divorced</span></span>               | <span data-ttu-id="72bba-446">Разведен/разведена</span><span class="sxs-lookup"><span data-stu-id="72bba-446">Divorced</span></span>             |
| <span data-ttu-id="72bba-447">Зарегистрированное партнерство</span><span class="sxs-lookup"><span data-stu-id="72bba-447">Registered Partnership</span></span> | <span data-ttu-id="72bba-448">Партнерство на внутреннем рынке</span><span class="sxs-lookup"><span data-stu-id="72bba-448">Domestic Partnership</span></span> |
| <span data-ttu-id="72bba-449">None</span><span class="sxs-lookup"><span data-stu-id="72bba-449">None</span></span>                   | <span data-ttu-id="72bba-450">None</span><span class="sxs-lookup"><span data-stu-id="72bba-450">None</span></span>                 |
| <span data-ttu-id="72bba-451">Партнерство</span><span class="sxs-lookup"><span data-stu-id="72bba-451">Cohabiting</span></span>             | <span data-ttu-id="72bba-452">Партнерство</span><span class="sxs-lookup"><span data-stu-id="72bba-452">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="72bba-453">Род</span><span class="sxs-lookup"><span data-stu-id="72bba-453">Gender</span></span>

<span data-ttu-id="72bba-454">Значения пола сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="72bba-454">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="72bba-455">В следующей таблице показано, как значения пола сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="72bba-455">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="72bba-456">Talent</span><span class="sxs-lookup"><span data-stu-id="72bba-456">Talent</span></span>       | <span data-ttu-id="72bba-457">Dayforce</span><span class="sxs-lookup"><span data-stu-id="72bba-457">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="72bba-458">Мужской</span><span class="sxs-lookup"><span data-stu-id="72bba-458">Male</span></span>         | <span data-ttu-id="72bba-459">Мужской</span><span class="sxs-lookup"><span data-stu-id="72bba-459">Male</span></span>            |
| <span data-ttu-id="72bba-460">Женский</span><span class="sxs-lookup"><span data-stu-id="72bba-460">Female</span></span>       | <span data-ttu-id="72bba-461">Женский</span><span class="sxs-lookup"><span data-stu-id="72bba-461">Female</span></span>          |
| <span data-ttu-id="72bba-462">Неопределенный</span><span class="sxs-lookup"><span data-stu-id="72bba-462">Non-specific</span></span> | <span data-ttu-id="72bba-463">*Не поддерживается*</span><span class="sxs-lookup"><span data-stu-id="72bba-463">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="72bba-464">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="72bba-464">Earning codes</span></span>

<span data-ttu-id="72bba-465">Коды доходов уникально определяют каждый типа доходов, которые работники получают.</span><span class="sxs-lookup"><span data-stu-id="72bba-465">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="72bba-466">Эти коды покрывают несколько параметров, которые относятся к доходам, таких как правила учета, налоговые законы, требования к отчетности и возможности брутто в большую сторону.</span><span class="sxs-lookup"><span data-stu-id="72bba-466">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="72bba-467">Если используется неподдерживаемая частота, частота **Каждая оплата** используется по умолчанию для расчета.</span><span class="sxs-lookup"><span data-stu-id="72bba-467">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="72bba-468">Поддерживаемые частоты</span><span class="sxs-lookup"><span data-stu-id="72bba-468">Supported frequencies</span></span>

- <span data-ttu-id="72bba-469">Все</span><span class="sxs-lookup"><span data-stu-id="72bba-469">All</span></span>
- <span data-ttu-id="72bba-470">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="72bba-470">EVERYPAY</span></span>
- <span data-ttu-id="72bba-471">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="72bba-471">EACHPAYPERIOD</span></span>
- <span data-ttu-id="72bba-472">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="72bba-472">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="72bba-473">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="72bba-473">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="72bba-474">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-474">1OFMTH</span></span>
- <span data-ttu-id="72bba-475">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-475">LASTOFMTH</span></span>
- <span data-ttu-id="72bba-476">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-476">2OFMTH</span></span>
- <span data-ttu-id="72bba-477">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-477">3OFMTH</span></span>
- <span data-ttu-id="72bba-478">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-478">4OFMTH</span></span>
- <span data-ttu-id="72bba-479">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-479">5OFMTH</span></span>
- <span data-ttu-id="72bba-480">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-480">1N2OFMTH</span></span>
- <span data-ttu-id="72bba-481">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-481">3N4OFMTH</span></span>
- <span data-ttu-id="72bba-482">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-482">1N3OFMTH</span></span>
- <span data-ttu-id="72bba-483">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-483">1N4OFMTH</span></span>
- <span data-ttu-id="72bba-484">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-484">2N3OFMTH</span></span>
- <span data-ttu-id="72bba-485">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-485">2N4OFMTH</span></span>
- <span data-ttu-id="72bba-486">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-486">1N2N3OFMTH</span></span>
- <span data-ttu-id="72bba-487">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-487">1N2N4OFMTH</span></span>
- <span data-ttu-id="72bba-488">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-488">1N3N4OFMTH</span></span>
- <span data-ttu-id="72bba-489">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-489">2N3N4OFMTH</span></span>
- <span data-ttu-id="72bba-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="72bba-491">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="72bba-491">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="72bba-492">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="72bba-492">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="72bba-493">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="72bba-493">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="72bba-494">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="72bba-494">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="72bba-495">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="72bba-495">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="72bba-496">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="72bba-496">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="72bba-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="72bba-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="72bba-498">Адреса</span><span class="sxs-lookup"><span data-stu-id="72bba-498">Addresses</span></span>

<span data-ttu-id="72bba-499">Идентификация кодов конкретной страны или региона, области и района (муниципалитета) требует определенных форматов, которые Dayforce и поставщики в стране или в регионе могут распознать.</span><span class="sxs-lookup"><span data-stu-id="72bba-499">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="72bba-500">Хотя формат городов гибкий, каждый город должен быть связан с областью.</span><span class="sxs-lookup"><span data-stu-id="72bba-500">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="72bba-501">Talent</span><span class="sxs-lookup"><span data-stu-id="72bba-501">Talent</span></span>          | <span data-ttu-id="72bba-502">Dayforce</span><span class="sxs-lookup"><span data-stu-id="72bba-502">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="72bba-503">Страна/регион</span><span class="sxs-lookup"><span data-stu-id="72bba-503">Country/Region</span></span>  | <span data-ttu-id="72bba-504">Код страны</span><span class="sxs-lookup"><span data-stu-id="72bba-504">Country Code</span></span>          |
| <span data-ttu-id="72bba-505">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="72bba-505">Zip/Postal Code</span></span> | <span data-ttu-id="72bba-506">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="72bba-506">Postal Code</span></span>           |
| <span data-ttu-id="72bba-507">Область, край</span><span class="sxs-lookup"><span data-stu-id="72bba-507">State</span></span>           | <span data-ttu-id="72bba-508">Код региона</span><span class="sxs-lookup"><span data-stu-id="72bba-508">State Code</span></span>            |
| <span data-ttu-id="72bba-509">Город</span><span class="sxs-lookup"><span data-stu-id="72bba-509">City</span></span>            | <span data-ttu-id="72bba-510">Город</span><span class="sxs-lookup"><span data-stu-id="72bba-510">City</span></span>                  |
| <span data-ttu-id="72bba-511">Округ</span><span class="sxs-lookup"><span data-stu-id="72bba-511">County</span></span>          | <span data-ttu-id="72bba-512">Район (муниципалитет)</span><span class="sxs-lookup"><span data-stu-id="72bba-512">County (Municipality)</span></span> |
| <span data-ttu-id="72bba-513">Улица</span><span class="sxs-lookup"><span data-stu-id="72bba-513">Street</span></span>          | <span data-ttu-id="72bba-514">Строка адреса 1</span><span class="sxs-lookup"><span data-stu-id="72bba-514">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="72bba-515">Налоговые регионы</span><span class="sxs-lookup"><span data-stu-id="72bba-515">Tax regions</span></span>

<span data-ttu-id="72bba-516">Налоговые регионы используются для определения налогов, которые следует применять при создании заработной платы.</span><span class="sxs-lookup"><span data-stu-id="72bba-516">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="72bba-517">Налоговые регионы сопоставляются с Dayforce как адреса местоположения.</span><span class="sxs-lookup"><span data-stu-id="72bba-517">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="72bba-518">Налоговый регион по умолчанию должен быть связан с активной должностью работника.</span><span class="sxs-lookup"><span data-stu-id="72bba-518">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="72bba-519">Налоговый регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-519">Tax region (required)</span></span>
- <span data-ttu-id="72bba-520">Страна/Регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-520">Country/Region (required)</span></span>
- <span data-ttu-id="72bba-521">Регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-521">State (required)</span></span>
- <span data-ttu-id="72bba-522">Округ</span><span class="sxs-lookup"><span data-stu-id="72bba-522">County</span></span> 
- <span data-ttu-id="72bba-523">Город (обязательно)</span><span class="sxs-lookup"><span data-stu-id="72bba-523">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="72bba-524">Настройка данных для расчета заработной платы в Мексике</span><span class="sxs-lookup"><span data-stu-id="72bba-524">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="72bba-525">Если вы создаете оплату для сотрудников в Мексике, необходимо настроить следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="72bba-525">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="72bba-526">Обязательно указывать подразделения для должностей.</span><span class="sxs-lookup"><span data-stu-id="72bba-526">Departments are required on positions.</span></span>
- <span data-ttu-id="72bba-527">Центры затрат должен быть заданы как финансовые аналитики и должны быть первым элементом в строке финансовой аналитики по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="72bba-527">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="72bba-528">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="72bba-528">Job types</span></span>

<span data-ttu-id="72bba-529">Типы должностей используются для группирования похожих должностных обязанностей в категории.</span><span class="sxs-lookup"><span data-stu-id="72bba-529">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="72bba-530">Типы должностей обязательны для обработки зарплаты в Мексике.</span><span class="sxs-lookup"><span data-stu-id="72bba-530">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="72bba-531">Примеры типов должностей включают полный рабочий день и неполный рабочий день, или зарплата и почасовая оплата.</span><span class="sxs-lookup"><span data-stu-id="72bba-531">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="72bba-532">Типы должностей сопоставляются с Dayforce как типы зарплаты, которые указывают тип оплаты сотрудника: почасовая или оклад.</span><span class="sxs-lookup"><span data-stu-id="72bba-532">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="72bba-533">Требуются следующие типы должностей и описаний.</span><span class="sxs-lookup"><span data-stu-id="72bba-533">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="72bba-534">Тип задания</span><span class="sxs-lookup"><span data-stu-id="72bba-534">Job type</span></span>   | <span data-ttu-id="72bba-535">описание</span><span class="sxs-lookup"><span data-stu-id="72bba-535">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="72bba-536">Почасовая</span><span class="sxs-lookup"><span data-stu-id="72bba-536">Hourly</span></span>     | <span data-ttu-id="72bba-537">MX Почасовая</span><span class="sxs-lookup"><span data-stu-id="72bba-537">MX Hourly</span></span>   |
| <span data-ttu-id="72bba-538">Оклад</span><span class="sxs-lookup"><span data-stu-id="72bba-538">Salaried</span></span>   | <span data-ttu-id="72bba-539">MX Оклад</span><span class="sxs-lookup"><span data-stu-id="72bba-539">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="72bba-540">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="72bba-540">Position types</span></span> 

<span data-ttu-id="72bba-541">С помощью типов должностей описывается, является ли должность занятостью на полный рабочий день, на неполный рабочий день или какой-либо другой.</span><span class="sxs-lookup"><span data-stu-id="72bba-541">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="72bba-542">Типы должностей сопоставляются с Dayforce как классы зарплаты, которые указывают тип оплаты сотрудника: полная занятость или частичная занятость.</span><span class="sxs-lookup"><span data-stu-id="72bba-542">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="72bba-543">Требуются следующие типы должностей и описаний.</span><span class="sxs-lookup"><span data-stu-id="72bba-543">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="72bba-544">Тип должности</span><span class="sxs-lookup"><span data-stu-id="72bba-544">Position type</span></span>   | <span data-ttu-id="72bba-545">описание</span><span class="sxs-lookup"><span data-stu-id="72bba-545">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="72bba-546">Полная занятость</span><span class="sxs-lookup"><span data-stu-id="72bba-546">Full-time</span></span>       | <span data-ttu-id="72bba-547">Работник с полной занятостью</span><span class="sxs-lookup"><span data-stu-id="72bba-547">Full time employee</span></span> |
| <span data-ttu-id="72bba-548">Частичная занятость</span><span class="sxs-lookup"><span data-stu-id="72bba-548">Part-time</span></span>       | <span data-ttu-id="72bba-549">Работник с частичной занятостью</span><span class="sxs-lookup"><span data-stu-id="72bba-549">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="72bba-550">Коды оснований</span><span class="sxs-lookup"><span data-stu-id="72bba-550">Reason codes</span></span>

<span data-ttu-id="72bba-551">Коды оснований содержат сведения о статусе сотрудника.</span><span class="sxs-lookup"><span data-stu-id="72bba-551">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="72bba-552">Коды оснований сопоставляются с Dayforce как причины статуса, которые определяют причину изменения статус должности или найма сотрудника.</span><span class="sxs-lookup"><span data-stu-id="72bba-552">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="72bba-553">Требуются следующие коды причин и описания.</span><span class="sxs-lookup"><span data-stu-id="72bba-553">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="72bba-554">Код основания</span><span class="sxs-lookup"><span data-stu-id="72bba-554">Reason code</span></span>            | <span data-ttu-id="72bba-555">описание</span><span class="sxs-lookup"><span data-stu-id="72bba-555">Description</span></span>                    | <span data-ttu-id="72bba-556">Применимые сценарии</span><span class="sxs-lookup"><span data-stu-id="72bba-556">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="72bba-557">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="72bba-557">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="72bba-558">Увольнение до первой заработной платы</span><span class="sxs-lookup"><span data-stu-id="72bba-558">Departure before first payroll</span></span> | <span data-ttu-id="72bba-559">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="72bba-559">Terminate worker</span></span>     |
| <span data-ttu-id="72bba-560">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="72bba-560">RESIGNATION</span></span>            | <span data-ttu-id="72bba-561">Увольнение</span><span class="sxs-lookup"><span data-stu-id="72bba-561">Resignation</span></span>                    | <span data-ttu-id="72bba-562">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="72bba-562">Terminate worker</span></span>     |
| <span data-ttu-id="72bba-563">PENSION</span><span class="sxs-lookup"><span data-stu-id="72bba-563">PENSION</span></span>                | <span data-ttu-id="72bba-564">Пенсия</span><span class="sxs-lookup"><span data-stu-id="72bba-564">Pension</span></span>                        | <span data-ttu-id="72bba-565">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="72bba-565">Terminate worker</span></span>     |
| <span data-ttu-id="72bba-566">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="72bba-566">TERMINATION</span></span>            | <span data-ttu-id="72bba-567">Завершение</span><span class="sxs-lookup"><span data-stu-id="72bba-567">Termination</span></span>                    | <span data-ttu-id="72bba-568">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="72bba-568">Terminate worker</span></span>     |
| <span data-ttu-id="72bba-569">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="72bba-569">RETIREMENT</span></span>             | <span data-ttu-id="72bba-570">Выходное пособие</span><span class="sxs-lookup"><span data-stu-id="72bba-570">Retirement</span></span>                     | <span data-ttu-id="72bba-571">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="72bba-571">Terminate worker</span></span>     |
| <span data-ttu-id="72bba-572">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="72bba-572">ABSENTEE</span></span>               | <span data-ttu-id="72bba-573">Прогульщик</span><span class="sxs-lookup"><span data-stu-id="72bba-573">Absentee</span></span>                       | <span data-ttu-id="72bba-574">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="72bba-574">Terminate worker</span></span>     |
| <span data-ttu-id="72bba-575">ПРОЧЕЕ</span><span class="sxs-lookup"><span data-stu-id="72bba-575">OTHER</span></span>                  | <span data-ttu-id="72bba-576">Другие причины</span><span class="sxs-lookup"><span data-stu-id="72bba-576">Other Reasons</span></span>                  | <span data-ttu-id="72bba-577">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="72bba-577">Terminate worker</span></span>     |
| <span data-ttu-id="72bba-578">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="72bba-578">CLOSURE</span></span>                | <span data-ttu-id="72bba-579">Закрытие компании</span><span class="sxs-lookup"><span data-stu-id="72bba-579">Business Closure</span></span>               | <span data-ttu-id="72bba-580">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="72bba-580">Terminate worker</span></span>     |
| <span data-ttu-id="72bba-581">DEATH</span><span class="sxs-lookup"><span data-stu-id="72bba-581">DEATH</span></span>                  | <span data-ttu-id="72bba-582">Смерть</span><span class="sxs-lookup"><span data-stu-id="72bba-582">Death</span></span>                          | <span data-ttu-id="72bba-583">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="72bba-583">Terminate worker</span></span>     |
| <span data-ttu-id="72bba-584">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="72bba-584">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="72bba-585">Отпуск</span><span class="sxs-lookup"><span data-stu-id="72bba-585">Leave of Absence</span></span>               | <span data-ttu-id="72bba-586">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="72bba-586">Terminate worker</span></span>     |
| <span data-ttu-id="72bba-587">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="72bba-587">CONTRACTEND</span></span>            | <span data-ttu-id="72bba-588">Завершение контракта</span><span class="sxs-lookup"><span data-stu-id="72bba-588">End of Contract</span></span>                | <span data-ttu-id="72bba-589">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="72bba-589">Terminate worker</span></span>     |
| <span data-ttu-id="72bba-590">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="72bba-590">SALARYCHANGE</span></span>           | <span data-ttu-id="72bba-591">Изменение зарплаты</span><span class="sxs-lookup"><span data-stu-id="72bba-591">Change of Salary</span></span>               | <span data-ttu-id="72bba-592">Компенсация</span><span class="sxs-lookup"><span data-stu-id="72bba-592">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="72bba-593">Условия найма</span><span class="sxs-lookup"><span data-stu-id="72bba-593">Terms of employment</span></span>

<span data-ttu-id="72bba-594">Условия найма используются для создания категорий условий трудоустройства.</span><span class="sxs-lookup"><span data-stu-id="72bba-594">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="72bba-595">Условия сопоставляются с Dayforce как значения индикатора трудоустройства.</span><span class="sxs-lookup"><span data-stu-id="72bba-595">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="72bba-596">Необходимы следующие условия найма и описания.</span><span class="sxs-lookup"><span data-stu-id="72bba-596">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="72bba-597">Условия найма</span><span class="sxs-lookup"><span data-stu-id="72bba-597">Terms of employment</span></span>   | <span data-ttu-id="72bba-598">описание</span><span class="sxs-lookup"><span data-stu-id="72bba-598">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="72bba-599">Периодически</span><span class="sxs-lookup"><span data-stu-id="72bba-599">Regular</span></span>               | <span data-ttu-id="72bba-600">Периодически</span><span class="sxs-lookup"><span data-stu-id="72bba-600">Regular</span></span>     |
| <span data-ttu-id="72bba-601">Напрямую</span><span class="sxs-lookup"><span data-stu-id="72bba-601">Direct</span></span>                | <span data-ttu-id="72bba-602">Напрямую</span><span class="sxs-lookup"><span data-stu-id="72bba-602">Direct</span></span>      |
| <span data-ttu-id="72bba-603">Практика</span><span class="sxs-lookup"><span data-stu-id="72bba-603">Internship</span></span>            | <span data-ttu-id="72bba-604">Практика</span><span class="sxs-lookup"><span data-stu-id="72bba-604">Internship</span></span>  |
| <span data-ttu-id="72bba-605">Постоянный</span><span class="sxs-lookup"><span data-stu-id="72bba-605">Permanent</span></span>             | <span data-ttu-id="72bba-606">Постоянный</span><span class="sxs-lookup"><span data-stu-id="72bba-606">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="72bba-607">Семейное положение</span><span class="sxs-lookup"><span data-stu-id="72bba-607">Marital status</span></span>

<span data-ttu-id="72bba-608">Значения семейного положения сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="72bba-608">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="72bba-609">В следующей таблице показано, как значения семейного положения сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="72bba-609">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="72bba-610">Talent</span><span class="sxs-lookup"><span data-stu-id="72bba-610">Talent</span></span>                 | <span data-ttu-id="72bba-611">Dayforce</span><span class="sxs-lookup"><span data-stu-id="72bba-611">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="72bba-612">Женат/замужем</span><span class="sxs-lookup"><span data-stu-id="72bba-612">Married</span></span>                | <span data-ttu-id="72bba-613">Женат/замужем</span><span class="sxs-lookup"><span data-stu-id="72bba-613">Married</span></span>                   |
| <span data-ttu-id="72bba-614">Один</span><span class="sxs-lookup"><span data-stu-id="72bba-614">Single</span></span>                 | <span data-ttu-id="72bba-615">Один</span><span class="sxs-lookup"><span data-stu-id="72bba-615">Single</span></span>                    |
| <span data-ttu-id="72bba-616">Вдовец/вдова</span><span class="sxs-lookup"><span data-stu-id="72bba-616">Widowed</span></span>                | <span data-ttu-id="72bba-617">Вдовец/вдова</span><span class="sxs-lookup"><span data-stu-id="72bba-617">Widowed</span></span>                   |
| <span data-ttu-id="72bba-618">Разведен/разведена</span><span class="sxs-lookup"><span data-stu-id="72bba-618">Divorced</span></span>               | <span data-ttu-id="72bba-619">Разведен/разведена</span><span class="sxs-lookup"><span data-stu-id="72bba-619">Divorced</span></span>                  |
| <span data-ttu-id="72bba-620">Зарегистрированное партнерство</span><span class="sxs-lookup"><span data-stu-id="72bba-620">Registered Partnership</span></span> | <span data-ttu-id="72bba-621">Партнерство на внутреннем рынке</span><span class="sxs-lookup"><span data-stu-id="72bba-621">Domestic Partnership</span></span>      |
| <span data-ttu-id="72bba-622">None</span><span class="sxs-lookup"><span data-stu-id="72bba-622">None</span></span>                   | <span data-ttu-id="72bba-623">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="72bba-623">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="72bba-624">Партнерство</span><span class="sxs-lookup"><span data-stu-id="72bba-624">Cohabiting</span></span>             | <span data-ttu-id="72bba-625">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="72bba-625">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="72bba-626">Род</span><span class="sxs-lookup"><span data-stu-id="72bba-626">Gender</span></span>

<span data-ttu-id="72bba-627">Значения пола сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="72bba-627">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="72bba-628">В следующей таблице показано, как значения пола сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="72bba-628">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="72bba-629">Talent</span><span class="sxs-lookup"><span data-stu-id="72bba-629">Talent</span></span>       | <span data-ttu-id="72bba-630">Dayforce</span><span class="sxs-lookup"><span data-stu-id="72bba-630">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="72bba-631">Мужской</span><span class="sxs-lookup"><span data-stu-id="72bba-631">Male</span></span>         | <span data-ttu-id="72bba-632">Мужской</span><span class="sxs-lookup"><span data-stu-id="72bba-632">Male</span></span>                      |
| <span data-ttu-id="72bba-633">Женский</span><span class="sxs-lookup"><span data-stu-id="72bba-633">Female</span></span>       | <span data-ttu-id="72bba-634">Женский</span><span class="sxs-lookup"><span data-stu-id="72bba-634">Female</span></span>                    |
| <span data-ttu-id="72bba-635">Неопределенный</span><span class="sxs-lookup"><span data-stu-id="72bba-635">Non-specific</span></span> | <span data-ttu-id="72bba-636">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="72bba-636">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="72bba-637">Способ платежа</span><span class="sxs-lookup"><span data-stu-id="72bba-637">Payment method</span></span>

<span data-ttu-id="72bba-638">Методы оплаты предоставляют сотруднику и компании способ описания способа оплаты сотрудников.</span><span class="sxs-lookup"><span data-stu-id="72bba-638">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="72bba-639">Способы оплаты сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="72bba-639">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="72bba-640">В следующей таблице показано, как способы оплаты сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="72bba-640">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="72bba-641">Talent</span><span class="sxs-lookup"><span data-stu-id="72bba-641">Talent</span></span>             | <span data-ttu-id="72bba-642">Dayforce</span><span class="sxs-lookup"><span data-stu-id="72bba-642">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="72bba-643">Наличный расчет</span><span class="sxs-lookup"><span data-stu-id="72bba-643">Cash</span></span>               | <span data-ttu-id="72bba-644">Наличный расчет</span><span class="sxs-lookup"><span data-stu-id="72bba-644">Cash</span></span>                      |
| <span data-ttu-id="72bba-645">Электронный платеж</span><span class="sxs-lookup"><span data-stu-id="72bba-645">Electronic Payment</span></span> | <span data-ttu-id="72bba-646">Перевод</span><span class="sxs-lookup"><span data-stu-id="72bba-646">Transfer</span></span>                  |
| <span data-ttu-id="72bba-647">Проверка</span><span class="sxs-lookup"><span data-stu-id="72bba-647">Check</span></span>              | <span data-ttu-id="72bba-648">Чек</span><span class="sxs-lookup"><span data-stu-id="72bba-648">Cheque</span></span>                    |
| <span data-ttu-id="72bba-649">Банковская тратта</span><span class="sxs-lookup"><span data-stu-id="72bba-649">Bank Draft</span></span>         | <span data-ttu-id="72bba-650">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="72bba-650">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="72bba-651">Прочие</span><span class="sxs-lookup"><span data-stu-id="72bba-651">Other</span></span>              | <span data-ttu-id="72bba-652">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="72bba-652">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="72bba-653">Тип банковского счета</span><span class="sxs-lookup"><span data-stu-id="72bba-653">Bank account type</span></span>

<span data-ttu-id="72bba-654">Типы банковских счетов используются для электронных платежей сотрудникам.</span><span class="sxs-lookup"><span data-stu-id="72bba-654">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="72bba-655">Типы банковских счетов сопоставляются с Dayforce как сведения о счетах безналичных расчетов.</span><span class="sxs-lookup"><span data-stu-id="72bba-655">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="72bba-656">Типы банковских счетов переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="72bba-656">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="72bba-657">Talent</span><span class="sxs-lookup"><span data-stu-id="72bba-657">Talent</span></span>            | <span data-ttu-id="72bba-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="72bba-658">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="72bba-659">Чековый счет</span><span class="sxs-lookup"><span data-stu-id="72bba-659">Checking Account</span></span>  | <span data-ttu-id="72bba-660">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="72bba-660">CheckingAccount</span></span>           |
| <span data-ttu-id="72bba-661">Счет зарплаты</span><span class="sxs-lookup"><span data-stu-id="72bba-661">Payroll Account</span></span>   | <span data-ttu-id="72bba-662">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="72bba-662">PayrollAccount</span></span>            |
| <span data-ttu-id="72bba-663">Сберегательный счет</span><span class="sxs-lookup"><span data-stu-id="72bba-663">Savings Account</span></span>   | <span data-ttu-id="72bba-664">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="72bba-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="72bba-665">Счет BankGirot</span><span class="sxs-lookup"><span data-stu-id="72bba-665">BankGirot account</span></span> | <span data-ttu-id="72bba-666">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="72bba-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="72bba-667">Счет PlusGirot</span><span class="sxs-lookup"><span data-stu-id="72bba-667">PlusGirot account</span></span> | <span data-ttu-id="72bba-668">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="72bba-668">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="72bba-669">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="72bba-669">Earning codes</span></span>

<span data-ttu-id="72bba-670">Коды доходов уникально определяют каждый типа доходов, которые работники получают.</span><span class="sxs-lookup"><span data-stu-id="72bba-670">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="72bba-671">Эти коды покрывают несколько параметров, которые относятся к доходам, таких как правила учета, налоговые законы, требования к отчетности и возможности брутто в большую сторону.</span><span class="sxs-lookup"><span data-stu-id="72bba-671">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="72bba-672">Если используется неподдерживаемая частота, частота **Каждая оплата** используется по умолчанию для расчета.</span><span class="sxs-lookup"><span data-stu-id="72bba-672">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="72bba-673">Поддерживаемые частоты</span><span class="sxs-lookup"><span data-stu-id="72bba-673">Supported frequencies</span></span>

- <span data-ttu-id="72bba-674">Все</span><span class="sxs-lookup"><span data-stu-id="72bba-674">All</span></span>
- <span data-ttu-id="72bba-675">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="72bba-675">EVERYPAY</span></span>
- <span data-ttu-id="72bba-676">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="72bba-676">EACHPAYPERIOD</span></span>
- <span data-ttu-id="72bba-677">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="72bba-677">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="72bba-678">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="72bba-678">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="72bba-679">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-679">1OFMTH</span></span>
- <span data-ttu-id="72bba-680">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-680">LASTOFMTH</span></span>
- <span data-ttu-id="72bba-681">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-681">2OFMTH</span></span>
- <span data-ttu-id="72bba-682">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-682">3OFMTH</span></span>
- <span data-ttu-id="72bba-683">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-683">4OFMTH</span></span>
- <span data-ttu-id="72bba-684">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-684">5OFMTH</span></span>
- <span data-ttu-id="72bba-685">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-685">1N2OFMTH</span></span>
- <span data-ttu-id="72bba-686">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-686">3N4OFMTH</span></span>
- <span data-ttu-id="72bba-687">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-687">1N3OFMTH</span></span>
- <span data-ttu-id="72bba-688">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-688">1N4OFMTH</span></span>
- <span data-ttu-id="72bba-689">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-689">2N3OFMTH</span></span>
- <span data-ttu-id="72bba-690">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-690">2N4OFMTH</span></span>
- <span data-ttu-id="72bba-691">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-691">1N2N3OFMTH</span></span>
- <span data-ttu-id="72bba-692">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-692">1N2N4OFMTH</span></span>
- <span data-ttu-id="72bba-693">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-693">1N3N4OFMTH</span></span>
- <span data-ttu-id="72bba-694">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-694">2N3N4OFMTH</span></span>
- <span data-ttu-id="72bba-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="72bba-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="72bba-696">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="72bba-696">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="72bba-697">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="72bba-697">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="72bba-698">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="72bba-698">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="72bba-699">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="72bba-699">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="72bba-700">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="72bba-700">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="72bba-701">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="72bba-701">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="72bba-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="72bba-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="72bba-703">Адреса</span><span class="sxs-lookup"><span data-stu-id="72bba-703">Addresses</span></span>

<span data-ttu-id="72bba-704">Идентификация кодов конкретной страны или региона, области и района (муниципалитета) требует определенных форматов, которые Dayforce и поставщики в стране или в регионе могут распознать.</span><span class="sxs-lookup"><span data-stu-id="72bba-704">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="72bba-705">Хотя формат городов гибкий, каждый город должен быть связан с областью.</span><span class="sxs-lookup"><span data-stu-id="72bba-705">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="72bba-706">Talent</span><span class="sxs-lookup"><span data-stu-id="72bba-706">Talent</span></span>              | <span data-ttu-id="72bba-707">Dayforce</span><span class="sxs-lookup"><span data-stu-id="72bba-707">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="72bba-708">Страна/регион</span><span class="sxs-lookup"><span data-stu-id="72bba-708">Country/Region</span></span>      | <span data-ttu-id="72bba-709">Код страны</span><span class="sxs-lookup"><span data-stu-id="72bba-709">Country Code</span></span>          |
| <span data-ttu-id="72bba-710">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="72bba-710">Zip/Postal Code</span></span>     | <span data-ttu-id="72bba-711">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="72bba-711">Postal Code</span></span>           |
| <span data-ttu-id="72bba-712">Область, край</span><span class="sxs-lookup"><span data-stu-id="72bba-712">State</span></span>               | <span data-ttu-id="72bba-713">Код региона</span><span class="sxs-lookup"><span data-stu-id="72bba-713">State Code</span></span>            |
| <span data-ttu-id="72bba-714">Город</span><span class="sxs-lookup"><span data-stu-id="72bba-714">City</span></span>                | <span data-ttu-id="72bba-715">Город</span><span class="sxs-lookup"><span data-stu-id="72bba-715">City</span></span>                  |
| <span data-ttu-id="72bba-716">Округ</span><span class="sxs-lookup"><span data-stu-id="72bba-716">County</span></span>              | <span data-ttu-id="72bba-717">Район (муниципалитет)</span><span class="sxs-lookup"><span data-stu-id="72bba-717">County (Municipality)</span></span> |
| <span data-ttu-id="72bba-718">Улица</span><span class="sxs-lookup"><span data-stu-id="72bba-718">Street</span></span>              | <span data-ttu-id="72bba-719">Строка адреса 1</span><span class="sxs-lookup"><span data-stu-id="72bba-719">Address Line 1</span></span>        |
| <span data-ttu-id="72bba-720">Номер дома</span><span class="sxs-lookup"><span data-stu-id="72bba-720">Street Number</span></span>       | <span data-ttu-id="72bba-721">Строка адреса 2</span><span class="sxs-lookup"><span data-stu-id="72bba-721">Address Line 2</span></span>        |
| <span data-ttu-id="72bba-722">Дополнение здания</span><span class="sxs-lookup"><span data-stu-id="72bba-722">Building Complement</span></span> | <span data-ttu-id="72bba-723">Строка адреса 5</span><span class="sxs-lookup"><span data-stu-id="72bba-723">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="72bba-724">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="72bba-724">Passport number</span></span>

<span data-ttu-id="72bba-725">Сотрудники могут объявить данные паспорта.</span><span class="sxs-lookup"><span data-stu-id="72bba-725">Employees can declare passport information.</span></span> <span data-ttu-id="72bba-726">Эта информация имеет тип идентификации **Паспорт** и интегрируется в Dayforce как часть сведений о сотруднике, специфических для Мексики.</span><span class="sxs-lookup"><span data-stu-id="72bba-726">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="72bba-727">Тип идентификации = "Паспорт"</span><span class="sxs-lookup"><span data-stu-id="72bba-727">Identification Type = "Passport"</span></span>
- <span data-ttu-id="72bba-728">Дата выпуска</span><span class="sxs-lookup"><span data-stu-id="72bba-728">Issued Date</span></span>
- <span data-ttu-id="72bba-729">Дата окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="72bba-729">Expiration Date</span></span>

<span data-ttu-id="72bba-730">Сотрудники могут объявить несколько идентификационных номеров для типа идентификатора **Паспорт**.</span><span class="sxs-lookup"><span data-stu-id="72bba-730">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="72bba-731">Тем не менее только запись текущего активного паспорта интегрируется в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="72bba-731">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="72bba-732">Если срок действия всех записей паспорта истек, в Dayforce интегрируется тот, который был выдан последним.</span><span class="sxs-lookup"><span data-stu-id="72bba-732">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
