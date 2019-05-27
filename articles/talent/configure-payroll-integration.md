---
title: Настройка интеграции зарплаты между Talent и Dayforce
description: В этом разделе объясняется, как настроить интеграцию между Microsoft Dynamics 365 for Talent и Ceridian Dayforce таким образом, чтобы вы могли обработать период оплаты.
author: andreabichsel
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9a88bf61dbb12520b555ceb7363b1c646d95386e
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518890"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="18cad-103">Настройка интеграции зарплаты между Talent и Dayforce</span><span class="sxs-lookup"><span data-stu-id="18cad-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="18cad-104">Интеграция между Microsoft Dynamics 365 for Talent и Ceridian Dayforce зависит от ряда действий настройки, описанных в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="18cad-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="18cad-105">Необходимо настроить интеграцию в Talent и Dayforce перед обработкой периода оплаты.</span><span class="sxs-lookup"><span data-stu-id="18cad-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="18cad-106">При использовании службы, например Dayforce, для выполнения оплаты, необходимо включить интеграцию в Talent.</span><span class="sxs-lookup"><span data-stu-id="18cad-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="18cad-107">Интеграция требует определенных данных из Talent.</span><span class="sxs-lookup"><span data-stu-id="18cad-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="18cad-108">Таким образом необходимо убедиться, что данные, отображаемые в Dayforce, настроены в Talent таким образом, чтобы поддерживать интеграцию.</span><span class="sxs-lookup"><span data-stu-id="18cad-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="18cad-109">Интеграция использует следующие широкие категории данных:</span><span class="sxs-lookup"><span data-stu-id="18cad-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="18cad-110">Данные управления персоналом</span><span class="sxs-lookup"><span data-stu-id="18cad-110">Human resources data</span></span>
- <span data-ttu-id="18cad-111">Данные о компенсациях</span><span class="sxs-lookup"><span data-stu-id="18cad-111">Compensation data</span></span>
- <span data-ttu-id="18cad-112">Данные о заработной плате, например циклы оплаты, периоды оплаты и коды начисления зарплаты</span><span class="sxs-lookup"><span data-stu-id="18cad-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="18cad-113">Данные о работнике</span><span class="sxs-lookup"><span data-stu-id="18cad-113">Worker data</span></span>

<span data-ttu-id="18cad-114">В этом разделе описываются шаги, которые необходимо выполнить, чтобы включить интеграцию.</span><span class="sxs-lookup"><span data-stu-id="18cad-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="18cad-115">Здесь также объясняются типы данных и сведения о конфигурации, которые необходимы для интеграции.</span><span class="sxs-lookup"><span data-stu-id="18cad-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="18cad-116">Включение интеграции</span><span class="sxs-lookup"><span data-stu-id="18cad-116">Enable the integration</span></span>

<span data-ttu-id="18cad-117">В Talent необходимо включить интеграцию и ввести информацию о конфигурации для подключения к Dayforce.</span><span class="sxs-lookup"><span data-stu-id="18cad-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="18cad-118">Если требуется, чтобы проводки ГК, которые производятся, импортировались в Microsoft Dynamics 365 for Finance and Operations, также необходимо установить учетную запись хранилища Microsoft Azure и ввести строку подключения хранилища Azure в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="18cad-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="18cad-119">Чтобы включить интеграцию в Talent, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="18cad-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="18cad-120">На странице **Администрирование системы** выберите **Конфигурация интеграции**.</span><span class="sxs-lookup"><span data-stu-id="18cad-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="18cad-121">Введите безопасную конечную точку FTP и путь к безопасной папке FTP.</span><span class="sxs-lookup"><span data-stu-id="18cad-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="18cad-122">Введите имя пользователя и пароль пользователя, который будет иметь доступ к безопасной конечной точке и пути к папке FTP.</span><span class="sxs-lookup"><span data-stu-id="18cad-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="18cad-123">Проверьте подключение, как требуется, а также установите для параметра **Включить интеграцию зарплаты** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="18cad-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="18cad-124">При включении интеграции создаются пакет экспорта данных и файлы, и задается значение частоты.</span><span class="sxs-lookup"><span data-stu-id="18cad-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="18cad-125">Можно изменить эту частоту, как требуется.</span><span class="sxs-lookup"><span data-stu-id="18cad-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="18cad-126">Дополнительные сведения об учетных записях хранилища Azure и строке подключения хранилища Azure см. в следующих разделах Azure:</span><span class="sxs-lookup"><span data-stu-id="18cad-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="18cad-127">Об учетных записях хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="18cad-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="18cad-128">Настройка строки подключения хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="18cad-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="18cad-129">Настройка данных</span><span class="sxs-lookup"><span data-stu-id="18cad-129">Configure your data</span></span> 

<span data-ttu-id="18cad-130">Для обработки зарплаты необходимо настроить данные управления персоналом в Talent.</span><span class="sxs-lookup"><span data-stu-id="18cad-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="18cad-131">Необходимо настроить организационные данные, такие как задания и должности, вместе со сведениями о льготах и компенсациях.</span><span class="sxs-lookup"><span data-stu-id="18cad-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="18cad-132">Эта информация содержит сведения о занятости, оплате и вычетах, которые необходимы для формирования заработной платы сотрудника.</span><span class="sxs-lookup"><span data-stu-id="18cad-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="18cad-133">Данные управления персоналом</span><span class="sxs-lookup"><span data-stu-id="18cad-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="18cad-134">Льготы</span><span class="sxs-lookup"><span data-stu-id="18cad-134">Benefits</span></span> 

<span data-ttu-id="18cad-135">Человеческие ресурсы обеспечивают инструменты для настройки и поддержки льгот, вычетов и планов компенсации работникам, которые организация предлагает или обрабатывает для своих работников.</span><span class="sxs-lookup"><span data-stu-id="18cad-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="18cad-136">При создании льгот имейте в виду следующие данные и конфигурации, которые используются в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="18cad-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="18cad-137">Планы льгот</span><span class="sxs-lookup"><span data-stu-id="18cad-137">Benefit plans</span></span>

- <span data-ttu-id="18cad-138">План (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-138">Plan (required)</span></span>
- <span data-ttu-id="18cad-139">Тип (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-139">Type (required)</span></span>
- <span data-ttu-id="18cad-140">Влияние на зарплату (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-140">Payroll impact (required)</span></span>
- <span data-ttu-id="18cad-141">Погасить задолженность</span><span class="sxs-lookup"><span data-stu-id="18cad-141">Recover arrears</span></span>
- <span data-ttu-id="18cad-142">Метод вычета</span><span class="sxs-lookup"><span data-stu-id="18cad-142">Deduction method</span></span>
- <span data-ttu-id="18cad-143">Приоритет вычета</span><span class="sxs-lookup"><span data-stu-id="18cad-143">Deduction priority</span></span>
- <span data-ttu-id="18cad-144">Период лимита</span><span class="sxs-lookup"><span data-stu-id="18cad-144">Limit period</span></span>
- <span data-ttu-id="18cad-145">Сумма лимита</span><span class="sxs-lookup"><span data-stu-id="18cad-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="18cad-146">Льготы</span><span class="sxs-lookup"><span data-stu-id="18cad-146">Benefits</span></span>

- <span data-ttu-id="18cad-147">План (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-147">Plan (required)</span></span>
- <span data-ttu-id="18cad-148">Тип (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-148">Type (required)</span></span>
- <span data-ttu-id="18cad-149">Параметр (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-149">Option (required)</span></span>
- <span data-ttu-id="18cad-150">Код льготы (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-150">Benefit ID (required)</span></span>
- <span data-ttu-id="18cad-151">Частота</span><span class="sxs-lookup"><span data-stu-id="18cad-151">Frequency</span></span>
- <span data-ttu-id="18cad-152">База</span><span class="sxs-lookup"><span data-stu-id="18cad-152">Basis</span></span>
- <span data-ttu-id="18cad-153">Сумма или ставка</span><span class="sxs-lookup"><span data-stu-id="18cad-153">Amount or rate</span></span>
- <span data-ttu-id="18cad-154">Код дохода</span><span class="sxs-lookup"><span data-stu-id="18cad-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="18cad-155">Поддерживаемые частоты</span><span class="sxs-lookup"><span data-stu-id="18cad-155">Supported frequencies</span></span> 

- <span data-ttu-id="18cad-156">Еженедельно</span><span class="sxs-lookup"><span data-stu-id="18cad-156">Weekly</span></span>
- <span data-ttu-id="18cad-157">Один раз в две недели</span><span class="sxs-lookup"><span data-stu-id="18cad-157">Bi-weekly</span></span>
- <span data-ttu-id="18cad-158">Два раза в месяц</span><span class="sxs-lookup"><span data-stu-id="18cad-158">Semi-monthly</span></span>
- <span data-ttu-id="18cad-159">Один раз в месяц</span><span class="sxs-lookup"><span data-stu-id="18cad-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="18cad-160">Поддерживаемые базы</span><span class="sxs-lookup"><span data-stu-id="18cad-160">Supported bases</span></span> 

- <span data-ttu-id="18cad-161">Фиксированная сумма</span><span class="sxs-lookup"><span data-stu-id="18cad-161">Fixed amount</span></span>
- <span data-ttu-id="18cad-162">Процент дохода</span><span class="sxs-lookup"><span data-stu-id="18cad-162">Percent of earnings</span></span>
- <span data-ttu-id="18cad-163">Продуктивные часы</span><span class="sxs-lookup"><span data-stu-id="18cad-163">Productive hours</span></span>

<span data-ttu-id="18cad-164">Dayforce создает следующие вычеты на основе влияния на зарплату, которое определено в плане льгот.</span><span class="sxs-lookup"><span data-stu-id="18cad-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="18cad-165">Выбор в Talent</span><span class="sxs-lookup"><span data-stu-id="18cad-165">Selection in Talent</span></span>        | <span data-ttu-id="18cad-166">Результат в Dayforce</span><span class="sxs-lookup"><span data-stu-id="18cad-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="18cad-167">None</span><span class="sxs-lookup"><span data-stu-id="18cad-167">None</span></span>                       | <span data-ttu-id="18cad-168">Вычет не создается.</span><span class="sxs-lookup"><span data-stu-id="18cad-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="18cad-169">Только удержание</span><span class="sxs-lookup"><span data-stu-id="18cad-169">Deduction only</span></span>             | <span data-ttu-id="18cad-170">Вычет сотрудника будет создан.</span><span class="sxs-lookup"><span data-stu-id="18cad-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="18cad-171">Только вклад</span><span class="sxs-lookup"><span data-stu-id="18cad-171">Contribution only</span></span>          | <span data-ttu-id="18cad-172">Вычет работодателя будет создан.</span><span class="sxs-lookup"><span data-stu-id="18cad-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="18cad-173">Удержание и вклад</span><span class="sxs-lookup"><span data-stu-id="18cad-173">Deduction and contribution</span></span> | <span data-ttu-id="18cad-174">Создаются вычеты сотрудников и работодателя.</span><span class="sxs-lookup"><span data-stu-id="18cad-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="18cad-175">Дополнительные сведения о том, как определять и управлять программами льгот, см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="18cad-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="18cad-176">Реализация программы льгот сотрудника</span><span class="sxs-lookup"><span data-stu-id="18cad-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="18cad-177">Создание новой льготы</span><span class="sxs-lookup"><span data-stu-id="18cad-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="18cad-178">Определение правил и политик проверки прав на льготы</span><span class="sxs-lookup"><span data-stu-id="18cad-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="18cad-179">Регистрация и удаление льгот для работников</span><span class="sxs-lookup"><span data-stu-id="18cad-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="18cad-180">Компенсация</span><span class="sxs-lookup"><span data-stu-id="18cad-180">Compensation</span></span> 

<span data-ttu-id="18cad-181">Управление компенсациями используется для управления предоставлением базовой оплаты и вознаграждений.</span><span class="sxs-lookup"><span data-stu-id="18cad-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="18cad-182">Тарифные ставки и единовременные надбавки контролируются с помощью планов фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="18cad-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="18cad-183">Поощрительные выплаты, такие как премии, вознаграждения за производительность, опционы на покупку акций и гранты, а также одноразовые компенсации, контролируются с помощью планов переменных компенсаций.</span><span class="sxs-lookup"><span data-stu-id="18cad-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="18cad-184">Dayforce использует сведения о компенсации для расчета почасовой или годовой ставки сотрудника.</span><span class="sxs-lookup"><span data-stu-id="18cad-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="18cad-185">Требуются планы фиксированной компенсации и преобразования ставки оплаты.</span><span class="sxs-lookup"><span data-stu-id="18cad-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="18cad-186">Сотрудники должны быть связаны с планом фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="18cad-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="18cad-187">Дополнительные сведения о планах компенсации см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="18cad-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="18cad-188">Создание планов фиксированной компенсации</span><span class="sxs-lookup"><span data-stu-id="18cad-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="18cad-189">Создание планов переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="18cad-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="18cad-190">Разработка структуры и планов зарплаты/компенсации</span><span class="sxs-lookup"><span data-stu-id="18cad-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="18cad-191">Обработка компенсаций</span><span class="sxs-lookup"><span data-stu-id="18cad-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="18cad-192">Определение процесса компенсации и расчет результатов</span><span class="sxs-lookup"><span data-stu-id="18cad-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="18cad-193">Включение сотрудника в план фиксированных компенсаций</span><span class="sxs-lookup"><span data-stu-id="18cad-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="18cad-194">Включение сотрудника в план переменных компенсаций</span><span class="sxs-lookup"><span data-stu-id="18cad-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="18cad-195">Должности</span><span class="sxs-lookup"><span data-stu-id="18cad-195">Jobs</span></span> 

<span data-ttu-id="18cad-196">Должностные обязанности — это набор задач и обязанностей, которые возлагаются на занимающее эту задание лицо.</span><span class="sxs-lookup"><span data-stu-id="18cad-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="18cad-197">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="18cad-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="18cad-198">Настройка компонентов должности</span><span class="sxs-lookup"><span data-stu-id="18cad-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="18cad-199">Определение новых заданий</span><span class="sxs-lookup"><span data-stu-id="18cad-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="18cad-200">Должности</span><span class="sxs-lookup"><span data-stu-id="18cad-200">Positions</span></span>

<span data-ttu-id="18cad-201">Позиция — это индивидуальный экземпляр должности.</span><span class="sxs-lookup"><span data-stu-id="18cad-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="18cad-202">Например, должность "Менеджер по продажам (восток)" — это одна из должностей, связанных с должностными обязанностями "Менеджер по продажам".</span><span class="sxs-lookup"><span data-stu-id="18cad-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="18cad-203">Должность существует в отделе.</span><span class="sxs-lookup"><span data-stu-id="18cad-203">A position exists in a department.</span></span> <span data-ttu-id="18cad-204">Только один работник может быть связан с каждой должностью.</span><span class="sxs-lookup"><span data-stu-id="18cad-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="18cad-205">Учитывайте следующие данные и конфигурацию при настройке должностей:</span><span class="sxs-lookup"><span data-stu-id="18cad-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="18cad-206">Должность (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-206">Position (required)</span></span>
- <span data-ttu-id="18cad-207">Описание (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-207">Description (required)</span></span>
- <span data-ttu-id="18cad-208">Должностные обязанности (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-208">Job (required)</span></span>
- <span data-ttu-id="18cad-209">Отдел (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-209">Department (required)</span></span>
- <span data-ttu-id="18cad-210">Тип должности (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-210">Position type (required)</span></span>
- <span data-ttu-id="18cad-211">Эквивалент полной занятости</span><span class="sxs-lookup"><span data-stu-id="18cad-211">Full-time equivalent</span></span>
- <span data-ttu-id="18cad-212">Обычные часы за год (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="18cad-213">Оплачивается юридическим лицом (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="18cad-214">Цикл оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-214">Pay cycle (required)</span></span>
- <span data-ttu-id="18cad-215">Финансовая аналитика по умолчанию — центр затрат (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="18cad-216">Назначение работника — работник, начало назначения, окончание назначения, код причины</span><span class="sxs-lookup"><span data-stu-id="18cad-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="18cad-217">Если несколько должностей в одном отделе связаны с одними и теми же должностными обязанностями, они объединяются в одну должность в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="18cad-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="18cad-218">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="18cad-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="18cad-219">Организация трудовых ресурсов с использованием подразделений, должностей и штатных единиц</span><span class="sxs-lookup"><span data-stu-id="18cad-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="18cad-220">Настройка должностей</span><span class="sxs-lookup"><span data-stu-id="18cad-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="18cad-221">Отделы</span><span class="sxs-lookup"><span data-stu-id="18cad-221">Departments</span></span>

<span data-ttu-id="18cad-222">Подразделение — это операционная единица, которая представляет собой категорию или функциональную область в организации.</span><span class="sxs-lookup"><span data-stu-id="18cad-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="18cad-223">Подразделение отвечает за конкретную область деятельности организации, например продажи, бухгалтерский учет или управление персоналом.</span><span class="sxs-lookup"><span data-stu-id="18cad-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="18cad-224">Подразделения можно использовать для формирования отчетности по функциональным областям.</span><span class="sxs-lookup"><span data-stu-id="18cad-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="18cad-225">Подразделения могут нести ответственность за прибыли и убытки.</span><span class="sxs-lookup"><span data-stu-id="18cad-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="18cad-226">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="18cad-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="18cad-227">Создание подразделения и связывание его с иерархией подразделений</span><span class="sxs-lookup"><span data-stu-id="18cad-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="18cad-228">Определение новых подразделений</span><span class="sxs-lookup"><span data-stu-id="18cad-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="18cad-229">Циклы оплаты и платежные периоды</span><span class="sxs-lookup"><span data-stu-id="18cad-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="18cad-230">Цикл оплаты определяет, как часто рассчитывается зарплата и определенные дни, когда работники получают зарплату.</span><span class="sxs-lookup"><span data-stu-id="18cad-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="18cad-231">Например, цикл оплаты может быть ежемесячным, и сотрудникам может выплачиваться зарплата в последний день месяца.</span><span class="sxs-lookup"><span data-stu-id="18cad-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="18cad-232">Кроме того, цикл оплаты может быть еженедельным, а сотрудники могут получать зарплату по вторникам после завершения периода оплаты.</span><span class="sxs-lookup"><span data-stu-id="18cad-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="18cad-233">Циклы оплаты назначаются должностям для управления выплатами работникам для этих должностей.</span><span class="sxs-lookup"><span data-stu-id="18cad-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="18cad-234">После создания циклов зарплаты можно создать платежные периоды для каждого цикла.</span><span class="sxs-lookup"><span data-stu-id="18cad-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="18cad-235">Каждый платежный период включает дату оплаты по умолчанию, которая основана на информации, предоставленной вами.</span><span class="sxs-lookup"><span data-stu-id="18cad-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="18cad-236">Однако можно изменить дату платежа по умолчанию в платежный период для учета исключений, например, когда дата оплаты приходится на праздник.</span><span class="sxs-lookup"><span data-stu-id="18cad-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="18cad-237">Dayforce использует следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="18cad-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="18cad-238">Цикл оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-238">Pay cycle (required)</span></span>
- <span data-ttu-id="18cad-239">Частота циклов оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="18cad-240">Дата начала периода (первый период оплаты обязателен)</span><span class="sxs-lookup"><span data-stu-id="18cad-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="18cad-241">Дата платежа по умолчанию (первый период оплаты обязателен)</span><span class="sxs-lookup"><span data-stu-id="18cad-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="18cad-242">Эта информация интегрирована с Dayforce как платежные группы, и разделяется по странам или регионам для каждого цикла оплаты.</span><span class="sxs-lookup"><span data-stu-id="18cad-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="18cad-243">Хотя бы один платежный период должен быть создан до интеграции.</span><span class="sxs-lookup"><span data-stu-id="18cad-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="18cad-244">Dayforce создает календари группы оплаты и даты оплаты на основе даты начала первого периода оплаты и даты оплаты по умолчанию, настроенных в Talent.</span><span class="sxs-lookup"><span data-stu-id="18cad-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="18cad-245">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="18cad-245">Earning codes</span></span>

<span data-ttu-id="18cad-246">Коды доходов уникально определяют каждый типа доходов, которые работники получают.</span><span class="sxs-lookup"><span data-stu-id="18cad-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="18cad-247">Эти коды имеют различные параметры, которые относятся к доходам, таких как правила учета, налоговые законы, требования к отчетности и возможности брутто в большую сторону.</span><span class="sxs-lookup"><span data-stu-id="18cad-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="18cad-248">Dayforce использует следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="18cad-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="18cad-249">Код дохода (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-249">Earning Code (required)</span></span>
- <span data-ttu-id="18cad-250">описание</span><span class="sxs-lookup"><span data-stu-id="18cad-250">Description</span></span>
- <span data-ttu-id="18cad-251">Единица измерения</span><span class="sxs-lookup"><span data-stu-id="18cad-251">Unit of measure</span></span>
- <span data-ttu-id="18cad-252">Продуктивный</span><span class="sxs-lookup"><span data-stu-id="18cad-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="18cad-253">Данные о работнике</span><span class="sxs-lookup"><span data-stu-id="18cad-253">Worker data</span></span>

<span data-ttu-id="18cad-254">Записи о различных типах сотрудников, которые имеются у вас, важны для вашей системы управления персоналом и системы расчета заработной платы.</span><span class="sxs-lookup"><span data-stu-id="18cad-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="18cad-255">Вводимые данные могут использоваться для отслеживания сведений о работниках и личной информации.</span><span class="sxs-lookup"><span data-stu-id="18cad-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="18cad-256">По работникам может храниться следующая информация.</span><span class="sxs-lookup"><span data-stu-id="18cad-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="18cad-257">**Основная** — базовые сведения о работнике, такие как контактные данные, демографические данные, идентифицирующие сведения, состав семье, сведения о службе в армии, данные об иностранных сотрудниках, персональные контакты и контакты на случай экстренных ситуаций.</span><span class="sxs-lookup"><span data-stu-id="18cad-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="18cad-258">**Занятость** — сведения о занятости работников, такие как участие в компании или организации, должность, дату начала и завершения работы, способность к работе, условия найма, пенсия, отпуска и сведения о переездах.</span><span class="sxs-lookup"><span data-stu-id="18cad-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="18cad-259">**Отпуск и отсутствие** — сведения об отпусках или пропуска работника, рабочие календари, проводки отсутствия и соответствующие настройки.</span><span class="sxs-lookup"><span data-stu-id="18cad-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="18cad-260">**Заработная плата и компенсации** — сведения о планах вознаграждениях и зарплате работника, такие как премии, комиссии, налоги, выход на пенсию и вычеты из зарплаты.</span><span class="sxs-lookup"><span data-stu-id="18cad-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="18cad-261">При вводе сведений о работнике имейте в виду следующие данные и конфигурации, которые используются в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="18cad-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="18cad-262">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="18cad-262">General information</span></span>

- <span data-ttu-id="18cad-263">Табельный номер (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-263">Personnel number (required)</span></span>
- <span data-ttu-id="18cad-264">Имя (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-264">First name (required)</span></span>
- <span data-ttu-id="18cad-265">Фамилия (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-265">Last name (required)</span></span>
- <span data-ttu-id="18cad-266">Отчество</span><span class="sxs-lookup"><span data-stu-id="18cad-266">Middle name</span></span>
- <span data-ttu-id="18cad-267">Дата начала стажа</span><span class="sxs-lookup"><span data-stu-id="18cad-267">Seniority date</span></span>
- <span data-ttu-id="18cad-268">Известно как</span><span class="sxs-lookup"><span data-stu-id="18cad-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="18cad-269">Личная информация</span><span class="sxs-lookup"><span data-stu-id="18cad-269">Personal information</span></span>

- <span data-ttu-id="18cad-270">Семейное положение (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-270">Marital status (required)</span></span>
- <span data-ttu-id="18cad-271">Дата рождения (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-271">Birth date (required)</span></span>
- <span data-ttu-id="18cad-272">Пол (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-272">Gender (required)</span></span>
- <span data-ttu-id="18cad-273">Лицо с инвалидностью</span><span class="sxs-lookup"><span data-stu-id="18cad-273">Person with disabilities</span></span>
- <span data-ttu-id="18cad-274">Национальность, регион страны (только в Мексике)</span><span class="sxs-lookup"><span data-stu-id="18cad-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="18cad-275">Адресная информация</span><span class="sxs-lookup"><span data-stu-id="18cad-275">Address information</span></span>

- <span data-ttu-id="18cad-276">Основной (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-276">Primary (required)</span></span>
- <span data-ttu-id="18cad-277">Страна/регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-277">Country/region (required)</span></span>
- <span data-ttu-id="18cad-278">Почтовый индекс (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-278">Postal code (required)</span></span>
- <span data-ttu-id="18cad-279">Номер дома (обязательно) (только для Мексики)</span><span class="sxs-lookup"><span data-stu-id="18cad-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="18cad-280">Дополнение здания (только в Мексике)</span><span class="sxs-lookup"><span data-stu-id="18cad-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="18cad-281">Город (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-281">City (required)</span></span>
- <span data-ttu-id="18cad-282">Регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-282">State (required)</span></span>
- <span data-ttu-id="18cad-283">Район (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="18cad-284">Контактная информация</span><span class="sxs-lookup"><span data-stu-id="18cad-284">Contact information</span></span> 

- <span data-ttu-id="18cad-285">Основной (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-285">Primary (required)</span></span>
- <span data-ttu-id="18cad-286">Контактный номер (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-286">Contact number (required)</span></span>
- <span data-ttu-id="18cad-287">Расширение</span><span class="sxs-lookup"><span data-stu-id="18cad-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="18cad-288">Информация по зарплате и коды дохода</span><span class="sxs-lookup"><span data-stu-id="18cad-288">Payroll information and earning codes</span></span>

<span data-ttu-id="18cad-289">Сотрудникам можно назначить конкретные доходы с заданной периодичностью оплаты и предпочтительный метод оплаты.</span><span class="sxs-lookup"><span data-stu-id="18cad-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="18cad-290">Следующие поля используются в Dayforce для обеспечения использования этих параметров и настроек.</span><span class="sxs-lookup"><span data-stu-id="18cad-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="18cad-291">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="18cad-291">Earning codes</span></span>

- <span data-ttu-id="18cad-292">Должность (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-292">Position (required)</span></span>
- <span data-ttu-id="18cad-293">Код дохода (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-293">Earning Code (required)</span></span>
- <span data-ttu-id="18cad-294">Частота (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-294">Frequency (required)</span></span>
- <span data-ttu-id="18cad-295">Сумма (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="18cad-296">Информация по зарплате</span><span class="sxs-lookup"><span data-stu-id="18cad-296">Payroll information</span></span>

- <span data-ttu-id="18cad-297">Способ оплаты</span><span class="sxs-lookup"><span data-stu-id="18cad-297">Payment Method</span></span>
- <span data-ttu-id="18cad-298">Экономический регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-298">Economic Region (required)</span></span>
- <span data-ttu-id="18cad-299">ИД льгот сотрудников</span><span class="sxs-lookup"><span data-stu-id="18cad-299">Employee Benefits ID</span></span>
- <span data-ttu-id="18cad-300">Идентификационный номер (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-300">National ID Number (required)</span></span>
- <span data-ttu-id="18cad-301">Номер документа о воинской службе</span><span class="sxs-lookup"><span data-stu-id="18cad-301">Military Service Number</span></span>
- <span data-ttu-id="18cad-302">Код смены (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-302">Shift ID (required)</span></span>
- <span data-ttu-id="18cad-303">Налоговой номер (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-303">Tax Number (required)</span></span>
- <span data-ttu-id="18cad-304">Код профсоюза (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-304">Union ID (required)</span></span>
- <span data-ttu-id="18cad-305">Идентификатор рабочего дня (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-305">Work Day ID (required)</span></span>
- <span data-ttu-id="18cad-306">Номер разрешения на работу</span><span class="sxs-lookup"><span data-stu-id="18cad-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="18cad-307">Для метода оплаты в Мексике поддерживает **Наличные деньги**, **Чек** (физический чек компании) и **Электронный платеж**.</span><span class="sxs-lookup"><span data-stu-id="18cad-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="18cad-308">Если способ оплаты не указан, **Чек** используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="18cad-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="18cad-309">Сведения о трудоустройстве</span><span class="sxs-lookup"><span data-stu-id="18cad-309">Employment details</span></span>

<span data-ttu-id="18cad-310">Подробная история занятости используется как ключевая информация для извлечения статуса найма, увольнения и повторного найма сотрудника в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="18cad-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="18cad-311">Dayforce поддерживает только одну активную запись о приеме на работу одновременно.</span><span class="sxs-lookup"><span data-stu-id="18cad-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="18cad-312">Дата начала трудоустройства (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-312">Employment start date (required)</span></span>
- <span data-ttu-id="18cad-313">Дата окончания занятости</span><span class="sxs-lookup"><span data-stu-id="18cad-313">Employment end date</span></span>
- <span data-ttu-id="18cad-314">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="18cad-314">Start date</span></span>
- <span data-ttu-id="18cad-315">Скорректированная дата приема на работу</span><span class="sxs-lookup"><span data-stu-id="18cad-315">Adjusted start date</span></span>
- <span data-ttu-id="18cad-316">Дата увольнения (обязательно после увольнения)</span><span class="sxs-lookup"><span data-stu-id="18cad-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="18cad-317">Причина увольнения (обязательно после увольнения)</span><span class="sxs-lookup"><span data-stu-id="18cad-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="18cad-318">Ключевые даты сотрудника получаются на основе следующих сведений.</span><span class="sxs-lookup"><span data-stu-id="18cad-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="18cad-319">Talent</span><span class="sxs-lookup"><span data-stu-id="18cad-319">Talent</span></span>                | <span data-ttu-id="18cad-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="18cad-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18cad-321">Самая последняя дата приема на работу</span><span class="sxs-lookup"><span data-stu-id="18cad-321">Most recent hire date</span></span> | <span data-ttu-id="18cad-322">Дата приема на работу для текущей записи истории занятости, которая еще не завершена</span><span class="sxs-lookup"><span data-stu-id="18cad-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="18cad-323">Дата увольнения</span><span class="sxs-lookup"><span data-stu-id="18cad-323">Termination date</span></span>      | <span data-ttu-id="18cad-324">Дата увольнения для текущей записи истории занятости, которая еще не завершена</span><span class="sxs-lookup"><span data-stu-id="18cad-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="18cad-325">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="18cad-325">Start date</span></span>            | <span data-ttu-id="18cad-326">Скорректированная дата приема на работу, дата приема на работу или дата приема на работу текущей неактивной записи история занятости</span><span class="sxs-lookup"><span data-stu-id="18cad-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="18cad-327">Дата первоначального приема на работу</span><span class="sxs-lookup"><span data-stu-id="18cad-327">Original hire date</span></span>    | <span data-ttu-id="18cad-328">Дата приема на работу самой ранней записи истории приема на работу</span><span class="sxs-lookup"><span data-stu-id="18cad-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="18cad-329">Компенсация</span><span class="sxs-lookup"><span data-stu-id="18cad-329">Compensation</span></span>

<span data-ttu-id="18cad-330">План фиксированной компенсации должен быть связан с каждой основной должностью работника на протяжении всего периода занятости.</span><span class="sxs-lookup"><span data-stu-id="18cad-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="18cad-331">Этот период начинается на даты, в которую сотрудник был нанят (или начальная дата приема на работу) и продолжается до увольнения.</span><span class="sxs-lookup"><span data-stu-id="18cad-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="18cad-332">Дата вступления в силу (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-332">Effective Date (required)</span></span>
- <span data-ttu-id="18cad-333">Срок действия</span><span class="sxs-lookup"><span data-stu-id="18cad-333">Expiration date</span></span>
- <span data-ttu-id="18cad-334">Ставка оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-334">Pay Rate (required)</span></span>
- <span data-ttu-id="18cad-335">Преобразования ставки оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="18cad-336">Годовой эквивалент (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="18cad-337">Почасовой эквивалент (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="18cad-338">Если сотрудник с почасовой оплатой имеет несколько должностей, фиксированная компенсация основной должности импортируется в Dayforce как базовая ставка/зарплата уровня сотрудника.</span><span class="sxs-lookup"><span data-stu-id="18cad-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="18cad-339">Дня неосновных должностей почасовая ставка сохраняется в соответствующей должности в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="18cad-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="18cad-340">Если штатный сотрудник имеет несколько должностей, суммарная почасовая ставка и годовая заработная плата для всех активных должностей определяется и используется в качестве базовой ставки/зарплаты уровня сотрудника.</span><span class="sxs-lookup"><span data-stu-id="18cad-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="18cad-341">Идентификационные номера</span><span class="sxs-lookup"><span data-stu-id="18cad-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="18cad-342">Код социального страхования</span><span class="sxs-lookup"><span data-stu-id="18cad-342">Social Security identifier</span></span> 

<span data-ttu-id="18cad-343">Каждый сотрудник должен иметь один первичный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="18cad-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="18cad-344">Этот идентификатор должен быть идентификатором типа **SSN**.</span><span class="sxs-lookup"><span data-stu-id="18cad-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="18cad-345">В Dayforce он автоматически извлекается как код социального страхования сотрудника, который необходим для приема на работу.</span><span class="sxs-lookup"><span data-stu-id="18cad-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="18cad-346">Основной (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-346">Primary (required)</span></span>
- <span data-ttu-id="18cad-347">Тип идентификации = "SSN"</span><span class="sxs-lookup"><span data-stu-id="18cad-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="18cad-348">Дата выпуска</span><span class="sxs-lookup"><span data-stu-id="18cad-348">Issued Date</span></span>
- <span data-ttu-id="18cad-349">Дата окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="18cad-349">Expiration Date</span></span>

<span data-ttu-id="18cad-350">Сотрудники могут объявить несколько идентификационных номеров для типа идентификатора **SSN**.</span><span class="sxs-lookup"><span data-stu-id="18cad-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="18cad-351">Тем не менее только запись, которая помечен как **Основная**, интегрируется в Dayforce, независимо от того, является ли номер активным или у него истек срок действия.</span><span class="sxs-lookup"><span data-stu-id="18cad-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="18cad-352">Банковские счета и выплаты</span><span class="sxs-lookup"><span data-stu-id="18cad-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="18cad-353">Необходимо ввести действительную информацию о банковском счете для любого сотрудника, который выбирает оплату через перевод на банковский счет.</span><span class="sxs-lookup"><span data-stu-id="18cad-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="18cad-354">Talent</span><span class="sxs-lookup"><span data-stu-id="18cad-354">Talent</span></span>                         | <span data-ttu-id="18cad-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="18cad-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18cad-356">Номер счета в банке (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="18cad-357">Код SWIFT (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-357">SWIFT code (required)</span></span>          | <span data-ttu-id="18cad-358">Поле **Код банка** используется при обработке зарплаты в Мексике.</span><span class="sxs-lookup"><span data-stu-id="18cad-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="18cad-359">Номер филиала (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="18cad-360">Тип банковского счета (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-360">Bank account type (required)</span></span>   | <span data-ttu-id="18cad-361">Поле **Тип счета** используется при обработке зарплаты в Мексике.</span><span class="sxs-lookup"><span data-stu-id="18cad-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="18cad-362">Поддерживаются значения **Выписка чека** и **Заработная плата**.</span><span class="sxs-lookup"><span data-stu-id="18cad-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="18cad-363">Работники, которые выбрали выплату переводом на банковский счет, должен предоставить ссылку на счет остатков, находящийся в юридическом лице с основным адресом в Мексике и связанный с действительным банковским счетом из мексиканского банка.</span><span class="sxs-lookup"><span data-stu-id="18cad-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="18cad-364">Все другие счета, не являющиеся счетами остатков, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="18cad-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="18cad-365">Адресная информация</span><span class="sxs-lookup"><span data-stu-id="18cad-365">Address information</span></span>

<span data-ttu-id="18cad-366">Каждый сотрудник должен иметь одно первичное местонахождение.</span><span class="sxs-lookup"><span data-stu-id="18cad-366">Every employee must have one primary location.</span></span> <span data-ttu-id="18cad-367">В Dayforce это расположение используется для определения основного места жительства сотрудника для целей налогообложения.</span><span class="sxs-lookup"><span data-stu-id="18cad-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="18cad-368">Основной (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-368">Primary (required)</span></span>
- <span data-ttu-id="18cad-369">Страна/регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-369">Country/region (required)</span></span>
- <span data-ttu-id="18cad-370">Почтовый индекс (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="18cad-371">Улица (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-371">Street (required)</span></span>
- <span data-ttu-id="18cad-372">Номер дома (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-372">Street Number (required)</span></span>
- <span data-ttu-id="18cad-373">Дополнение здания</span><span class="sxs-lookup"><span data-stu-id="18cad-373">Building Complement</span></span>
- <span data-ttu-id="18cad-374">Город (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-374">City (required)</span></span>
- <span data-ttu-id="18cad-375">Регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-375">State (required)</span></span>
- <span data-ttu-id="18cad-376">Район (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="18cad-377">Настройка данных для расчета заработной платы в США и Канаде</span><span class="sxs-lookup"><span data-stu-id="18cad-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="18cad-378">Если вы создаете оплату для сотрудников в США и Канаде, необходимо настроить следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="18cad-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="18cad-379">Обязательно указывать подразделения для должностей.</span><span class="sxs-lookup"><span data-stu-id="18cad-379">Departments are required on positions.</span></span>
- <span data-ttu-id="18cad-380">Центры затрат должен быть заданы как финансовые аналитики и должны быть первым элементом в строке финансовой аналитики по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="18cad-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="18cad-381">Можно настроить Talent, чтобы для должностей требовалось указывать подразделение.</span><span class="sxs-lookup"><span data-stu-id="18cad-381">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="18cad-382">Чтобы сделать это, выберите **Совместно используемые позиции управления персоналом > Позиции > Требовать подразделения для позиций**.</span><span class="sxs-lookup"><span data-stu-id="18cad-382">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="18cad-383">Рекомендуется включить этот параметр для интеграции.</span><span class="sxs-lookup"><span data-stu-id="18cad-383">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="18cad-384">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="18cad-384">Job types</span></span>

<span data-ttu-id="18cad-385">Типы должностей используются для группирования похожих должностных обязанностей в категории.</span><span class="sxs-lookup"><span data-stu-id="18cad-385">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="18cad-386">Типы должностей обязательны для обработки зарплаты в США и Канаде.</span><span class="sxs-lookup"><span data-stu-id="18cad-386">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="18cad-387">Примеры типов должностей включают полный рабочий день и неполный рабочий день, или зарплата и почасовая оплата.</span><span class="sxs-lookup"><span data-stu-id="18cad-387">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="18cad-388">Типы должностей сопоставляются с Dayforce как типы зарплаты, которые указывают тип оплаты сотрудника: почасовая или оклад.</span><span class="sxs-lookup"><span data-stu-id="18cad-388">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="18cad-389">Требуются следующие типы должностей и описаний.</span><span class="sxs-lookup"><span data-stu-id="18cad-389">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="18cad-390">Тип задания</span><span class="sxs-lookup"><span data-stu-id="18cad-390">Job type</span></span>   | <span data-ttu-id="18cad-391">описание</span><span class="sxs-lookup"><span data-stu-id="18cad-391">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="18cad-392">Почасовая</span><span class="sxs-lookup"><span data-stu-id="18cad-392">Hourly</span></span>     | <span data-ttu-id="18cad-393">Почасовая</span><span class="sxs-lookup"><span data-stu-id="18cad-393">Hourly</span></span>      |
| <span data-ttu-id="18cad-394">Оклад</span><span class="sxs-lookup"><span data-stu-id="18cad-394">Salaried</span></span>   | <span data-ttu-id="18cad-395">Оклад</span><span class="sxs-lookup"><span data-stu-id="18cad-395">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="18cad-396">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="18cad-396">Position types</span></span> 

<span data-ttu-id="18cad-397">С помощью типов должностей описывается, является ли должность занятостью на полный рабочий день, на неполный рабочий день или какой-либо другой.</span><span class="sxs-lookup"><span data-stu-id="18cad-397">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="18cad-398">Типы должностей сопоставляются с Dayforce как классы зарплаты, которые указывают тип оплаты сотрудника: полная занятость или частичная занятость.</span><span class="sxs-lookup"><span data-stu-id="18cad-398">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="18cad-399">Требуются следующие типы должностей и описаний.</span><span class="sxs-lookup"><span data-stu-id="18cad-399">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="18cad-400">Тип должности</span><span class="sxs-lookup"><span data-stu-id="18cad-400">Position type</span></span>   | <span data-ttu-id="18cad-401">описание</span><span class="sxs-lookup"><span data-stu-id="18cad-401">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="18cad-402">Полная занятость</span><span class="sxs-lookup"><span data-stu-id="18cad-402">Full-time</span></span>       | <span data-ttu-id="18cad-403">Работник с полной занятостью</span><span class="sxs-lookup"><span data-stu-id="18cad-403">Full time employee</span></span> |
| <span data-ttu-id="18cad-404">Частичная занятость</span><span class="sxs-lookup"><span data-stu-id="18cad-404">Part-time</span></span>       | <span data-ttu-id="18cad-405">Работник с частичной занятостью</span><span class="sxs-lookup"><span data-stu-id="18cad-405">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="18cad-406">Коды оснований</span><span class="sxs-lookup"><span data-stu-id="18cad-406">Reason codes</span></span>

<span data-ttu-id="18cad-407">Коды оснований содержат сведения о статусе сотрудника.</span><span class="sxs-lookup"><span data-stu-id="18cad-407">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="18cad-408">Коды оснований сопоставляются с Dayforce как причины статуса, которые определяют причину изменения статус должности или найма сотрудника.</span><span class="sxs-lookup"><span data-stu-id="18cad-408">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="18cad-409">Требуются следующие коды причин и описания.</span><span class="sxs-lookup"><span data-stu-id="18cad-409">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="18cad-410">Код основания</span><span class="sxs-lookup"><span data-stu-id="18cad-410">Reason code</span></span>    | <span data-ttu-id="18cad-411">описание</span><span class="sxs-lookup"><span data-stu-id="18cad-411">Description</span></span>      | <span data-ttu-id="18cad-412">Применимые сценарии</span><span class="sxs-lookup"><span data-stu-id="18cad-412">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="18cad-413">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="18cad-413">RESIGNATION</span></span>    | <span data-ttu-id="18cad-414">Увольнение</span><span class="sxs-lookup"><span data-stu-id="18cad-414">Resignation</span></span>      | <span data-ttu-id="18cad-415">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="18cad-415">Terminate worker</span></span>     |
| <span data-ttu-id="18cad-416">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="18cad-416">TERMINATION</span></span>    | <span data-ttu-id="18cad-417">Завершение</span><span class="sxs-lookup"><span data-stu-id="18cad-417">Termination</span></span>      | <span data-ttu-id="18cad-418">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="18cad-418">Terminate worker</span></span>     |
| <span data-ttu-id="18cad-419">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="18cad-419">RETIREMENT</span></span>     | <span data-ttu-id="18cad-420">Выходное пособие</span><span class="sxs-lookup"><span data-stu-id="18cad-420">Retirement</span></span>       | <span data-ttu-id="18cad-421">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="18cad-421">Terminate worker</span></span>     |
| <span data-ttu-id="18cad-422">ПРОЧЕЕ</span><span class="sxs-lookup"><span data-stu-id="18cad-422">OTHER</span></span>          | <span data-ttu-id="18cad-423">Другие причины</span><span class="sxs-lookup"><span data-stu-id="18cad-423">Other Reasons</span></span>    | <span data-ttu-id="18cad-424">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="18cad-424">Terminate worker</span></span>     |
| <span data-ttu-id="18cad-425">DEATH</span><span class="sxs-lookup"><span data-stu-id="18cad-425">DEATH</span></span>          | <span data-ttu-id="18cad-426">Смерть</span><span class="sxs-lookup"><span data-stu-id="18cad-426">Death</span></span>            | <span data-ttu-id="18cad-427">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="18cad-427">Terminate worker</span></span>     |
| <span data-ttu-id="18cad-428">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="18cad-428">LEAVEOFABSENCE</span></span> | <span data-ttu-id="18cad-429">Отпуск</span><span class="sxs-lookup"><span data-stu-id="18cad-429">Leave of Absence</span></span> | <span data-ttu-id="18cad-430">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="18cad-430">Terminate worker</span></span>     |
| <span data-ttu-id="18cad-431">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="18cad-431">CONTRACTEND</span></span>    | <span data-ttu-id="18cad-432">Завершение контракта</span><span class="sxs-lookup"><span data-stu-id="18cad-432">End of Contract</span></span>  | <span data-ttu-id="18cad-433">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="18cad-433">Terminate worker</span></span>     |
| <span data-ttu-id="18cad-434">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="18cad-434">SALARYCHANGE</span></span>   | <span data-ttu-id="18cad-435">Изменение зарплаты</span><span class="sxs-lookup"><span data-stu-id="18cad-435">Change of Salary</span></span> | <span data-ttu-id="18cad-436">Компенсация</span><span class="sxs-lookup"><span data-stu-id="18cad-436">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="18cad-437">Семейное положение</span><span class="sxs-lookup"><span data-stu-id="18cad-437">Marital status</span></span>

<span data-ttu-id="18cad-438">Значения семейного положения сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="18cad-438">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="18cad-439">В следующей таблице показано, как значения семейного положения сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="18cad-439">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="18cad-440">Talent</span><span class="sxs-lookup"><span data-stu-id="18cad-440">Talent</span></span>                 | <span data-ttu-id="18cad-441">Dayforce</span><span class="sxs-lookup"><span data-stu-id="18cad-441">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="18cad-442">Женат/замужем</span><span class="sxs-lookup"><span data-stu-id="18cad-442">Married</span></span>                | <span data-ttu-id="18cad-443">Женат/замужем</span><span class="sxs-lookup"><span data-stu-id="18cad-443">Married</span></span>              |
| <span data-ttu-id="18cad-444">Один</span><span class="sxs-lookup"><span data-stu-id="18cad-444">Single</span></span>                 | <span data-ttu-id="18cad-445">Один</span><span class="sxs-lookup"><span data-stu-id="18cad-445">Single</span></span>               |
| <span data-ttu-id="18cad-446">Вдовец/вдова</span><span class="sxs-lookup"><span data-stu-id="18cad-446">Widowed</span></span>                | <span data-ttu-id="18cad-447">Вдовец/вдова</span><span class="sxs-lookup"><span data-stu-id="18cad-447">Widowed</span></span>              |
| <span data-ttu-id="18cad-448">Разведен/разведена</span><span class="sxs-lookup"><span data-stu-id="18cad-448">Divorced</span></span>               | <span data-ttu-id="18cad-449">Разведен/разведена</span><span class="sxs-lookup"><span data-stu-id="18cad-449">Divorced</span></span>             |
| <span data-ttu-id="18cad-450">Зарегистрированное партнерство</span><span class="sxs-lookup"><span data-stu-id="18cad-450">Registered Partnership</span></span> | <span data-ttu-id="18cad-451">Партнерство на внутреннем рынке</span><span class="sxs-lookup"><span data-stu-id="18cad-451">Domestic Partnership</span></span> |
| <span data-ttu-id="18cad-452">None</span><span class="sxs-lookup"><span data-stu-id="18cad-452">None</span></span>                   | <span data-ttu-id="18cad-453">None</span><span class="sxs-lookup"><span data-stu-id="18cad-453">None</span></span>                 |
| <span data-ttu-id="18cad-454">Партнерство</span><span class="sxs-lookup"><span data-stu-id="18cad-454">Cohabiting</span></span>             | <span data-ttu-id="18cad-455">Партнерство</span><span class="sxs-lookup"><span data-stu-id="18cad-455">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="18cad-456">Род</span><span class="sxs-lookup"><span data-stu-id="18cad-456">Gender</span></span>

<span data-ttu-id="18cad-457">Значения пола сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="18cad-457">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="18cad-458">В следующей таблице показано, как значения пола сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="18cad-458">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="18cad-459">Talent</span><span class="sxs-lookup"><span data-stu-id="18cad-459">Talent</span></span>       | <span data-ttu-id="18cad-460">Dayforce</span><span class="sxs-lookup"><span data-stu-id="18cad-460">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="18cad-461">Мужской</span><span class="sxs-lookup"><span data-stu-id="18cad-461">Male</span></span>         | <span data-ttu-id="18cad-462">Мужской</span><span class="sxs-lookup"><span data-stu-id="18cad-462">Male</span></span>            |
| <span data-ttu-id="18cad-463">Женский</span><span class="sxs-lookup"><span data-stu-id="18cad-463">Female</span></span>       | <span data-ttu-id="18cad-464">Женский</span><span class="sxs-lookup"><span data-stu-id="18cad-464">Female</span></span>          |
| <span data-ttu-id="18cad-465">Неопределенный</span><span class="sxs-lookup"><span data-stu-id="18cad-465">Non-specific</span></span> | <span data-ttu-id="18cad-466">*Не поддерживается*</span><span class="sxs-lookup"><span data-stu-id="18cad-466">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="18cad-467">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="18cad-467">Earning codes</span></span>

<span data-ttu-id="18cad-468">Коды доходов уникально определяют каждый типа доходов, которые работники получают.</span><span class="sxs-lookup"><span data-stu-id="18cad-468">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="18cad-469">Эти коды покрывают несколько параметров, которые относятся к доходам, таких как правила учета, налоговые законы, требования к отчетности и возможности брутто в большую сторону.</span><span class="sxs-lookup"><span data-stu-id="18cad-469">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="18cad-470">Если используется неподдерживаемая частота, частота **Каждая оплата** используется по умолчанию для расчета.</span><span class="sxs-lookup"><span data-stu-id="18cad-470">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="18cad-471">Поддерживаемые частоты</span><span class="sxs-lookup"><span data-stu-id="18cad-471">Supported frequencies</span></span>

- <span data-ttu-id="18cad-472">Все</span><span class="sxs-lookup"><span data-stu-id="18cad-472">All</span></span>
- <span data-ttu-id="18cad-473">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="18cad-473">EVERYPAY</span></span>
- <span data-ttu-id="18cad-474">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="18cad-474">EACHPAYPERIOD</span></span>
- <span data-ttu-id="18cad-475">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="18cad-475">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="18cad-476">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="18cad-476">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="18cad-477">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-477">1OFMTH</span></span>
- <span data-ttu-id="18cad-478">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-478">LASTOFMTH</span></span>
- <span data-ttu-id="18cad-479">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-479">2OFMTH</span></span>
- <span data-ttu-id="18cad-480">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-480">3OFMTH</span></span>
- <span data-ttu-id="18cad-481">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-481">4OFMTH</span></span>
- <span data-ttu-id="18cad-482">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-482">5OFMTH</span></span>
- <span data-ttu-id="18cad-483">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-483">1N2OFMTH</span></span>
- <span data-ttu-id="18cad-484">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-484">3N4OFMTH</span></span>
- <span data-ttu-id="18cad-485">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-485">1N3OFMTH</span></span>
- <span data-ttu-id="18cad-486">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-486">1N4OFMTH</span></span>
- <span data-ttu-id="18cad-487">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-487">2N3OFMTH</span></span>
- <span data-ttu-id="18cad-488">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-488">2N4OFMTH</span></span>
- <span data-ttu-id="18cad-489">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-489">1N2N3OFMTH</span></span>
- <span data-ttu-id="18cad-490">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-490">1N2N4OFMTH</span></span>
- <span data-ttu-id="18cad-491">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-491">1N3N4OFMTH</span></span>
- <span data-ttu-id="18cad-492">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-492">2N3N4OFMTH</span></span>
- <span data-ttu-id="18cad-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="18cad-494">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="18cad-494">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="18cad-495">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="18cad-495">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="18cad-496">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="18cad-496">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="18cad-497">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="18cad-497">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="18cad-498">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="18cad-498">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="18cad-499">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="18cad-499">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="18cad-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="18cad-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="18cad-501">Адреса</span><span class="sxs-lookup"><span data-stu-id="18cad-501">Addresses</span></span>

<span data-ttu-id="18cad-502">Идентификация кодов конкретной страны или региона, области и района (муниципалитета) требует определенных форматов, которые Dayforce и поставщики в стране или в регионе могут распознать.</span><span class="sxs-lookup"><span data-stu-id="18cad-502">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="18cad-503">Хотя формат городов гибкий, каждый город должен быть связан с областью.</span><span class="sxs-lookup"><span data-stu-id="18cad-503">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="18cad-504">Talent</span><span class="sxs-lookup"><span data-stu-id="18cad-504">Talent</span></span>          | <span data-ttu-id="18cad-505">Dayforce</span><span class="sxs-lookup"><span data-stu-id="18cad-505">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="18cad-506">Страна/регион</span><span class="sxs-lookup"><span data-stu-id="18cad-506">Country/Region</span></span>  | <span data-ttu-id="18cad-507">Код страны</span><span class="sxs-lookup"><span data-stu-id="18cad-507">Country Code</span></span>          |
| <span data-ttu-id="18cad-508">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="18cad-508">Zip/Postal Code</span></span> | <span data-ttu-id="18cad-509">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="18cad-509">Postal Code</span></span>           |
| <span data-ttu-id="18cad-510">Область, край</span><span class="sxs-lookup"><span data-stu-id="18cad-510">State</span></span>           | <span data-ttu-id="18cad-511">Код региона</span><span class="sxs-lookup"><span data-stu-id="18cad-511">State Code</span></span>            |
| <span data-ttu-id="18cad-512">Город</span><span class="sxs-lookup"><span data-stu-id="18cad-512">City</span></span>            | <span data-ttu-id="18cad-513">Город</span><span class="sxs-lookup"><span data-stu-id="18cad-513">City</span></span>                  |
| <span data-ttu-id="18cad-514">Округ</span><span class="sxs-lookup"><span data-stu-id="18cad-514">County</span></span>          | <span data-ttu-id="18cad-515">Район (муниципалитет)</span><span class="sxs-lookup"><span data-stu-id="18cad-515">County (Municipality)</span></span> |
| <span data-ttu-id="18cad-516">Улица</span><span class="sxs-lookup"><span data-stu-id="18cad-516">Street</span></span>          | <span data-ttu-id="18cad-517">Строка адреса 1</span><span class="sxs-lookup"><span data-stu-id="18cad-517">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="18cad-518">Налоговые регионы</span><span class="sxs-lookup"><span data-stu-id="18cad-518">Tax regions</span></span>

<span data-ttu-id="18cad-519">Налоговые регионы используются для определения налогов, которые следует применять при создании заработной платы.</span><span class="sxs-lookup"><span data-stu-id="18cad-519">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="18cad-520">Налоговые регионы сопоставляются с Dayforce как адреса местоположения.</span><span class="sxs-lookup"><span data-stu-id="18cad-520">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="18cad-521">Налоговый регион по умолчанию должен быть связан с активной должностью работника.</span><span class="sxs-lookup"><span data-stu-id="18cad-521">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="18cad-522">Налоговый регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-522">Tax region (required)</span></span>
- <span data-ttu-id="18cad-523">Страна/Регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-523">Country/Region (required)</span></span>
- <span data-ttu-id="18cad-524">Регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-524">State (required)</span></span>
- <span data-ttu-id="18cad-525">Округ</span><span class="sxs-lookup"><span data-stu-id="18cad-525">County</span></span> 
- <span data-ttu-id="18cad-526">Город (обязательно)</span><span class="sxs-lookup"><span data-stu-id="18cad-526">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="18cad-527">Настройка данных для расчета заработной платы в Мексике</span><span class="sxs-lookup"><span data-stu-id="18cad-527">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="18cad-528">Если вы создаете оплату для сотрудников в Мексике, необходимо настроить следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="18cad-528">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="18cad-529">Обязательно указывать подразделения для должностей.</span><span class="sxs-lookup"><span data-stu-id="18cad-529">Departments are required on positions.</span></span>
- <span data-ttu-id="18cad-530">Центры затрат должен быть заданы как финансовые аналитики и должны быть первым элементом в строке финансовой аналитики по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="18cad-530">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="18cad-531">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="18cad-531">Job types</span></span>

<span data-ttu-id="18cad-532">Типы должностей используются для группирования похожих должностных обязанностей в категории.</span><span class="sxs-lookup"><span data-stu-id="18cad-532">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="18cad-533">Типы должностей обязательны для обработки зарплаты в Мексике.</span><span class="sxs-lookup"><span data-stu-id="18cad-533">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="18cad-534">Примеры типов должностей включают полный рабочий день и неполный рабочий день, или зарплата и почасовая оплата.</span><span class="sxs-lookup"><span data-stu-id="18cad-534">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="18cad-535">Типы должностей сопоставляются с Dayforce как типы зарплаты, которые указывают тип оплаты сотрудника: почасовая или оклад.</span><span class="sxs-lookup"><span data-stu-id="18cad-535">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="18cad-536">Требуются следующие типы должностей и описаний.</span><span class="sxs-lookup"><span data-stu-id="18cad-536">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="18cad-537">Тип задания</span><span class="sxs-lookup"><span data-stu-id="18cad-537">Job type</span></span>   | <span data-ttu-id="18cad-538">описание</span><span class="sxs-lookup"><span data-stu-id="18cad-538">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="18cad-539">Почасовая</span><span class="sxs-lookup"><span data-stu-id="18cad-539">Hourly</span></span>     | <span data-ttu-id="18cad-540">MX Почасовая</span><span class="sxs-lookup"><span data-stu-id="18cad-540">MX Hourly</span></span>   |
| <span data-ttu-id="18cad-541">Оклад</span><span class="sxs-lookup"><span data-stu-id="18cad-541">Salaried</span></span>   | <span data-ttu-id="18cad-542">MX Оклад</span><span class="sxs-lookup"><span data-stu-id="18cad-542">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="18cad-543">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="18cad-543">Position types</span></span> 

<span data-ttu-id="18cad-544">С помощью типов должностей описывается, является ли должность занятостью на полный рабочий день, на неполный рабочий день или какой-либо другой.</span><span class="sxs-lookup"><span data-stu-id="18cad-544">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="18cad-545">Типы должностей сопоставляются с Dayforce как классы зарплаты, которые указывают тип оплаты сотрудника: полная занятость или частичная занятость.</span><span class="sxs-lookup"><span data-stu-id="18cad-545">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="18cad-546">Требуются следующие типы должностей и описаний.</span><span class="sxs-lookup"><span data-stu-id="18cad-546">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="18cad-547">Тип должности</span><span class="sxs-lookup"><span data-stu-id="18cad-547">Position type</span></span>   | <span data-ttu-id="18cad-548">описание</span><span class="sxs-lookup"><span data-stu-id="18cad-548">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="18cad-549">Полная занятость</span><span class="sxs-lookup"><span data-stu-id="18cad-549">Full-time</span></span>       | <span data-ttu-id="18cad-550">Работник с полной занятостью</span><span class="sxs-lookup"><span data-stu-id="18cad-550">Full time employee</span></span> |
| <span data-ttu-id="18cad-551">Частичная занятость</span><span class="sxs-lookup"><span data-stu-id="18cad-551">Part-time</span></span>       | <span data-ttu-id="18cad-552">Работник с частичной занятостью</span><span class="sxs-lookup"><span data-stu-id="18cad-552">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="18cad-553">Коды оснований</span><span class="sxs-lookup"><span data-stu-id="18cad-553">Reason codes</span></span>

<span data-ttu-id="18cad-554">Коды оснований содержат сведения о статусе сотрудника.</span><span class="sxs-lookup"><span data-stu-id="18cad-554">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="18cad-555">Коды оснований сопоставляются с Dayforce как причины статуса, которые определяют причину изменения статус должности или найма сотрудника.</span><span class="sxs-lookup"><span data-stu-id="18cad-555">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="18cad-556">Требуются следующие коды причин и описания.</span><span class="sxs-lookup"><span data-stu-id="18cad-556">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="18cad-557">Код основания</span><span class="sxs-lookup"><span data-stu-id="18cad-557">Reason code</span></span>            | <span data-ttu-id="18cad-558">описание</span><span class="sxs-lookup"><span data-stu-id="18cad-558">Description</span></span>                    | <span data-ttu-id="18cad-559">Применимые сценарии</span><span class="sxs-lookup"><span data-stu-id="18cad-559">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="18cad-560">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="18cad-560">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="18cad-561">Увольнение до первой заработной платы</span><span class="sxs-lookup"><span data-stu-id="18cad-561">Departure before first payroll</span></span> | <span data-ttu-id="18cad-562">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="18cad-562">Terminate worker</span></span>     |
| <span data-ttu-id="18cad-563">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="18cad-563">RESIGNATION</span></span>            | <span data-ttu-id="18cad-564">Увольнение</span><span class="sxs-lookup"><span data-stu-id="18cad-564">Resignation</span></span>                    | <span data-ttu-id="18cad-565">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="18cad-565">Terminate worker</span></span>     |
| <span data-ttu-id="18cad-566">PENSION</span><span class="sxs-lookup"><span data-stu-id="18cad-566">PENSION</span></span>                | <span data-ttu-id="18cad-567">Пенсия</span><span class="sxs-lookup"><span data-stu-id="18cad-567">Pension</span></span>                        | <span data-ttu-id="18cad-568">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="18cad-568">Terminate worker</span></span>     |
| <span data-ttu-id="18cad-569">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="18cad-569">TERMINATION</span></span>            | <span data-ttu-id="18cad-570">Завершение</span><span class="sxs-lookup"><span data-stu-id="18cad-570">Termination</span></span>                    | <span data-ttu-id="18cad-571">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="18cad-571">Terminate worker</span></span>     |
| <span data-ttu-id="18cad-572">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="18cad-572">RETIREMENT</span></span>             | <span data-ttu-id="18cad-573">Выходное пособие</span><span class="sxs-lookup"><span data-stu-id="18cad-573">Retirement</span></span>                     | <span data-ttu-id="18cad-574">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="18cad-574">Terminate worker</span></span>     |
| <span data-ttu-id="18cad-575">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="18cad-575">ABSENTEE</span></span>               | <span data-ttu-id="18cad-576">Прогульщик</span><span class="sxs-lookup"><span data-stu-id="18cad-576">Absentee</span></span>                       | <span data-ttu-id="18cad-577">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="18cad-577">Terminate worker</span></span>     |
| <span data-ttu-id="18cad-578">ПРОЧЕЕ</span><span class="sxs-lookup"><span data-stu-id="18cad-578">OTHER</span></span>                  | <span data-ttu-id="18cad-579">Другие причины</span><span class="sxs-lookup"><span data-stu-id="18cad-579">Other Reasons</span></span>                  | <span data-ttu-id="18cad-580">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="18cad-580">Terminate worker</span></span>     |
| <span data-ttu-id="18cad-581">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="18cad-581">CLOSURE</span></span>                | <span data-ttu-id="18cad-582">Закрытие компании</span><span class="sxs-lookup"><span data-stu-id="18cad-582">Business Closure</span></span>               | <span data-ttu-id="18cad-583">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="18cad-583">Terminate worker</span></span>     |
| <span data-ttu-id="18cad-584">DEATH</span><span class="sxs-lookup"><span data-stu-id="18cad-584">DEATH</span></span>                  | <span data-ttu-id="18cad-585">Смерть</span><span class="sxs-lookup"><span data-stu-id="18cad-585">Death</span></span>                          | <span data-ttu-id="18cad-586">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="18cad-586">Terminate worker</span></span>     |
| <span data-ttu-id="18cad-587">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="18cad-587">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="18cad-588">Отпуск</span><span class="sxs-lookup"><span data-stu-id="18cad-588">Leave of Absence</span></span>               | <span data-ttu-id="18cad-589">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="18cad-589">Terminate worker</span></span>     |
| <span data-ttu-id="18cad-590">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="18cad-590">CONTRACTEND</span></span>            | <span data-ttu-id="18cad-591">Завершение контракта</span><span class="sxs-lookup"><span data-stu-id="18cad-591">End of Contract</span></span>                | <span data-ttu-id="18cad-592">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="18cad-592">Terminate worker</span></span>     |
| <span data-ttu-id="18cad-593">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="18cad-593">SALARYCHANGE</span></span>           | <span data-ttu-id="18cad-594">Изменение зарплаты</span><span class="sxs-lookup"><span data-stu-id="18cad-594">Change of Salary</span></span>               | <span data-ttu-id="18cad-595">Компенсация</span><span class="sxs-lookup"><span data-stu-id="18cad-595">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="18cad-596">Условия найма</span><span class="sxs-lookup"><span data-stu-id="18cad-596">Terms of employment</span></span>

<span data-ttu-id="18cad-597">Условия найма используются для создания категорий условий трудоустройства.</span><span class="sxs-lookup"><span data-stu-id="18cad-597">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="18cad-598">Условия сопоставляются с Dayforce как значения индикатора трудоустройства.</span><span class="sxs-lookup"><span data-stu-id="18cad-598">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="18cad-599">Необходимы следующие условия найма и описания.</span><span class="sxs-lookup"><span data-stu-id="18cad-599">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="18cad-600">Условия найма</span><span class="sxs-lookup"><span data-stu-id="18cad-600">Terms of employment</span></span>   | <span data-ttu-id="18cad-601">описание</span><span class="sxs-lookup"><span data-stu-id="18cad-601">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="18cad-602">Периодически</span><span class="sxs-lookup"><span data-stu-id="18cad-602">Regular</span></span>               | <span data-ttu-id="18cad-603">Периодически</span><span class="sxs-lookup"><span data-stu-id="18cad-603">Regular</span></span>     |
| <span data-ttu-id="18cad-604">Напрямую</span><span class="sxs-lookup"><span data-stu-id="18cad-604">Direct</span></span>                | <span data-ttu-id="18cad-605">Напрямую</span><span class="sxs-lookup"><span data-stu-id="18cad-605">Direct</span></span>      |
| <span data-ttu-id="18cad-606">Практика</span><span class="sxs-lookup"><span data-stu-id="18cad-606">Internship</span></span>            | <span data-ttu-id="18cad-607">Практика</span><span class="sxs-lookup"><span data-stu-id="18cad-607">Internship</span></span>  |
| <span data-ttu-id="18cad-608">Постоянный</span><span class="sxs-lookup"><span data-stu-id="18cad-608">Permanent</span></span>             | <span data-ttu-id="18cad-609">Постоянный</span><span class="sxs-lookup"><span data-stu-id="18cad-609">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="18cad-610">Семейное положение</span><span class="sxs-lookup"><span data-stu-id="18cad-610">Marital status</span></span>

<span data-ttu-id="18cad-611">Значения семейного положения сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="18cad-611">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="18cad-612">В следующей таблице показано, как значения семейного положения сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="18cad-612">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="18cad-613">Talent</span><span class="sxs-lookup"><span data-stu-id="18cad-613">Talent</span></span>                 | <span data-ttu-id="18cad-614">Dayforce</span><span class="sxs-lookup"><span data-stu-id="18cad-614">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="18cad-615">Женат/замужем</span><span class="sxs-lookup"><span data-stu-id="18cad-615">Married</span></span>                | <span data-ttu-id="18cad-616">Женат/замужем</span><span class="sxs-lookup"><span data-stu-id="18cad-616">Married</span></span>                   |
| <span data-ttu-id="18cad-617">Один</span><span class="sxs-lookup"><span data-stu-id="18cad-617">Single</span></span>                 | <span data-ttu-id="18cad-618">Один</span><span class="sxs-lookup"><span data-stu-id="18cad-618">Single</span></span>                    |
| <span data-ttu-id="18cad-619">Вдовец/вдова</span><span class="sxs-lookup"><span data-stu-id="18cad-619">Widowed</span></span>                | <span data-ttu-id="18cad-620">Вдовец/вдова</span><span class="sxs-lookup"><span data-stu-id="18cad-620">Widowed</span></span>                   |
| <span data-ttu-id="18cad-621">Разведен/разведена</span><span class="sxs-lookup"><span data-stu-id="18cad-621">Divorced</span></span>               | <span data-ttu-id="18cad-622">Разведен/разведена</span><span class="sxs-lookup"><span data-stu-id="18cad-622">Divorced</span></span>                  |
| <span data-ttu-id="18cad-623">Зарегистрированное партнерство</span><span class="sxs-lookup"><span data-stu-id="18cad-623">Registered Partnership</span></span> | <span data-ttu-id="18cad-624">Партнерство на внутреннем рынке</span><span class="sxs-lookup"><span data-stu-id="18cad-624">Domestic Partnership</span></span>      |
| <span data-ttu-id="18cad-625">None</span><span class="sxs-lookup"><span data-stu-id="18cad-625">None</span></span>                   | <span data-ttu-id="18cad-626">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="18cad-626">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="18cad-627">Партнерство</span><span class="sxs-lookup"><span data-stu-id="18cad-627">Cohabiting</span></span>             | <span data-ttu-id="18cad-628">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="18cad-628">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="18cad-629">Род</span><span class="sxs-lookup"><span data-stu-id="18cad-629">Gender</span></span>

<span data-ttu-id="18cad-630">Значения пола сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="18cad-630">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="18cad-631">В следующей таблице показано, как значения пола сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="18cad-631">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="18cad-632">Talent</span><span class="sxs-lookup"><span data-stu-id="18cad-632">Talent</span></span>       | <span data-ttu-id="18cad-633">Dayforce</span><span class="sxs-lookup"><span data-stu-id="18cad-633">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="18cad-634">Мужской</span><span class="sxs-lookup"><span data-stu-id="18cad-634">Male</span></span>         | <span data-ttu-id="18cad-635">Мужской</span><span class="sxs-lookup"><span data-stu-id="18cad-635">Male</span></span>                      |
| <span data-ttu-id="18cad-636">Женский</span><span class="sxs-lookup"><span data-stu-id="18cad-636">Female</span></span>       | <span data-ttu-id="18cad-637">Женский</span><span class="sxs-lookup"><span data-stu-id="18cad-637">Female</span></span>                    |
| <span data-ttu-id="18cad-638">Неопределенный</span><span class="sxs-lookup"><span data-stu-id="18cad-638">Non-specific</span></span> | <span data-ttu-id="18cad-639">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="18cad-639">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="18cad-640">Способ платежа</span><span class="sxs-lookup"><span data-stu-id="18cad-640">Payment method</span></span>

<span data-ttu-id="18cad-641">Методы оплаты предоставляют сотруднику и компании способ описания способа оплаты сотрудников.</span><span class="sxs-lookup"><span data-stu-id="18cad-641">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="18cad-642">Способы оплаты сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="18cad-642">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="18cad-643">В следующей таблице показано, как способы оплаты сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="18cad-643">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="18cad-644">Talent</span><span class="sxs-lookup"><span data-stu-id="18cad-644">Talent</span></span>             | <span data-ttu-id="18cad-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="18cad-645">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="18cad-646">Наличный расчет</span><span class="sxs-lookup"><span data-stu-id="18cad-646">Cash</span></span>               | <span data-ttu-id="18cad-647">Наличный расчет</span><span class="sxs-lookup"><span data-stu-id="18cad-647">Cash</span></span>                      |
| <span data-ttu-id="18cad-648">Электронный платеж</span><span class="sxs-lookup"><span data-stu-id="18cad-648">Electronic Payment</span></span> | <span data-ttu-id="18cad-649">Перевод</span><span class="sxs-lookup"><span data-stu-id="18cad-649">Transfer</span></span>                  |
| <span data-ttu-id="18cad-650">Проверка</span><span class="sxs-lookup"><span data-stu-id="18cad-650">Check</span></span>              | <span data-ttu-id="18cad-651">Чек</span><span class="sxs-lookup"><span data-stu-id="18cad-651">Cheque</span></span>                    |
| <span data-ttu-id="18cad-652">Банковская тратта</span><span class="sxs-lookup"><span data-stu-id="18cad-652">Bank Draft</span></span>         | <span data-ttu-id="18cad-653">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="18cad-653">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="18cad-654">Прочие</span><span class="sxs-lookup"><span data-stu-id="18cad-654">Other</span></span>              | <span data-ttu-id="18cad-655">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="18cad-655">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="18cad-656">Тип банковского счета</span><span class="sxs-lookup"><span data-stu-id="18cad-656">Bank account type</span></span>

<span data-ttu-id="18cad-657">Типы банковских счетов используются для электронных платежей сотрудникам.</span><span class="sxs-lookup"><span data-stu-id="18cad-657">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="18cad-658">Типы банковских счетов сопоставляются с Dayforce как сведения о счетах безналичных расчетов.</span><span class="sxs-lookup"><span data-stu-id="18cad-658">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="18cad-659">Типы банковских счетов переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="18cad-659">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="18cad-660">Talent</span><span class="sxs-lookup"><span data-stu-id="18cad-660">Talent</span></span>            | <span data-ttu-id="18cad-661">Dayforce</span><span class="sxs-lookup"><span data-stu-id="18cad-661">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="18cad-662">Чековый счет</span><span class="sxs-lookup"><span data-stu-id="18cad-662">Checking Account</span></span>  | <span data-ttu-id="18cad-663">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="18cad-663">CheckingAccount</span></span>           |
| <span data-ttu-id="18cad-664">Счет зарплаты</span><span class="sxs-lookup"><span data-stu-id="18cad-664">Payroll Account</span></span>   | <span data-ttu-id="18cad-665">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="18cad-665">PayrollAccount</span></span>            |
| <span data-ttu-id="18cad-666">Сберегательный счет</span><span class="sxs-lookup"><span data-stu-id="18cad-666">Savings Account</span></span>   | <span data-ttu-id="18cad-667">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="18cad-667">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="18cad-668">Счет BankGirot</span><span class="sxs-lookup"><span data-stu-id="18cad-668">BankGirot account</span></span> | <span data-ttu-id="18cad-669">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="18cad-669">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="18cad-670">Счет PlusGirot</span><span class="sxs-lookup"><span data-stu-id="18cad-670">PlusGirot account</span></span> | <span data-ttu-id="18cad-671">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="18cad-671">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="18cad-672">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="18cad-672">Earning codes</span></span>

<span data-ttu-id="18cad-673">Коды доходов уникально определяют каждый типа доходов, которые работники получают.</span><span class="sxs-lookup"><span data-stu-id="18cad-673">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="18cad-674">Эти коды покрывают несколько параметров, которые относятся к доходам, таких как правила учета, налоговые законы, требования к отчетности и возможности брутто в большую сторону.</span><span class="sxs-lookup"><span data-stu-id="18cad-674">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="18cad-675">Если используется неподдерживаемая частота, частота **Каждая оплата** используется по умолчанию для расчета.</span><span class="sxs-lookup"><span data-stu-id="18cad-675">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="18cad-676">Поддерживаемые частоты</span><span class="sxs-lookup"><span data-stu-id="18cad-676">Supported frequencies</span></span>

- <span data-ttu-id="18cad-677">Все</span><span class="sxs-lookup"><span data-stu-id="18cad-677">All</span></span>
- <span data-ttu-id="18cad-678">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="18cad-678">EVERYPAY</span></span>
- <span data-ttu-id="18cad-679">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="18cad-679">EACHPAYPERIOD</span></span>
- <span data-ttu-id="18cad-680">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="18cad-680">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="18cad-681">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="18cad-681">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="18cad-682">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-682">1OFMTH</span></span>
- <span data-ttu-id="18cad-683">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-683">LASTOFMTH</span></span>
- <span data-ttu-id="18cad-684">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-684">2OFMTH</span></span>
- <span data-ttu-id="18cad-685">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-685">3OFMTH</span></span>
- <span data-ttu-id="18cad-686">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-686">4OFMTH</span></span>
- <span data-ttu-id="18cad-687">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-687">5OFMTH</span></span>
- <span data-ttu-id="18cad-688">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-688">1N2OFMTH</span></span>
- <span data-ttu-id="18cad-689">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-689">3N4OFMTH</span></span>
- <span data-ttu-id="18cad-690">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-690">1N3OFMTH</span></span>
- <span data-ttu-id="18cad-691">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-691">1N4OFMTH</span></span>
- <span data-ttu-id="18cad-692">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-692">2N3OFMTH</span></span>
- <span data-ttu-id="18cad-693">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-693">2N4OFMTH</span></span>
- <span data-ttu-id="18cad-694">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-694">1N2N3OFMTH</span></span>
- <span data-ttu-id="18cad-695">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-695">1N2N4OFMTH</span></span>
- <span data-ttu-id="18cad-696">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-696">1N3N4OFMTH</span></span>
- <span data-ttu-id="18cad-697">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-697">2N3N4OFMTH</span></span>
- <span data-ttu-id="18cad-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="18cad-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="18cad-699">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="18cad-699">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="18cad-700">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="18cad-700">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="18cad-701">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="18cad-701">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="18cad-702">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="18cad-702">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="18cad-703">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="18cad-703">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="18cad-704">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="18cad-704">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="18cad-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="18cad-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="18cad-706">Адреса</span><span class="sxs-lookup"><span data-stu-id="18cad-706">Addresses</span></span>

<span data-ttu-id="18cad-707">Идентификация кодов конкретной страны или региона, области и района (муниципалитета) требует определенных форматов, которые Dayforce и поставщики в стране или в регионе могут распознать.</span><span class="sxs-lookup"><span data-stu-id="18cad-707">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="18cad-708">Хотя формат городов гибкий, каждый город должен быть связан с областью.</span><span class="sxs-lookup"><span data-stu-id="18cad-708">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="18cad-709">Talent</span><span class="sxs-lookup"><span data-stu-id="18cad-709">Talent</span></span>              | <span data-ttu-id="18cad-710">Dayforce</span><span class="sxs-lookup"><span data-stu-id="18cad-710">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="18cad-711">Страна/регион</span><span class="sxs-lookup"><span data-stu-id="18cad-711">Country/Region</span></span>      | <span data-ttu-id="18cad-712">Код страны</span><span class="sxs-lookup"><span data-stu-id="18cad-712">Country Code</span></span>          |
| <span data-ttu-id="18cad-713">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="18cad-713">Zip/Postal Code</span></span>     | <span data-ttu-id="18cad-714">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="18cad-714">Postal Code</span></span>           |
| <span data-ttu-id="18cad-715">Область, край</span><span class="sxs-lookup"><span data-stu-id="18cad-715">State</span></span>               | <span data-ttu-id="18cad-716">Код региона</span><span class="sxs-lookup"><span data-stu-id="18cad-716">State Code</span></span>            |
| <span data-ttu-id="18cad-717">Город</span><span class="sxs-lookup"><span data-stu-id="18cad-717">City</span></span>                | <span data-ttu-id="18cad-718">Город</span><span class="sxs-lookup"><span data-stu-id="18cad-718">City</span></span>                  |
| <span data-ttu-id="18cad-719">Округ</span><span class="sxs-lookup"><span data-stu-id="18cad-719">County</span></span>              | <span data-ttu-id="18cad-720">Район (муниципалитет)</span><span class="sxs-lookup"><span data-stu-id="18cad-720">County (Municipality)</span></span> |
| <span data-ttu-id="18cad-721">Улица</span><span class="sxs-lookup"><span data-stu-id="18cad-721">Street</span></span>              | <span data-ttu-id="18cad-722">Строка адреса 1</span><span class="sxs-lookup"><span data-stu-id="18cad-722">Address Line 1</span></span>        |
| <span data-ttu-id="18cad-723">Номер дома</span><span class="sxs-lookup"><span data-stu-id="18cad-723">Street Number</span></span>       | <span data-ttu-id="18cad-724">Строка адреса 2</span><span class="sxs-lookup"><span data-stu-id="18cad-724">Address Line 2</span></span>        |
| <span data-ttu-id="18cad-725">Дополнение здания</span><span class="sxs-lookup"><span data-stu-id="18cad-725">Building Complement</span></span> | <span data-ttu-id="18cad-726">Строка адреса 5</span><span class="sxs-lookup"><span data-stu-id="18cad-726">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="18cad-727">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18cad-727">Passport number</span></span>

<span data-ttu-id="18cad-728">Сотрудники могут объявить данные паспорта.</span><span class="sxs-lookup"><span data-stu-id="18cad-728">Employees can declare passport information.</span></span> <span data-ttu-id="18cad-729">Эта информация имеет тип идентификации **Паспорт** и интегрируется в Dayforce как часть сведений о сотруднике, специфических для Мексики.</span><span class="sxs-lookup"><span data-stu-id="18cad-729">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="18cad-730">Тип идентификации = "Паспорт"</span><span class="sxs-lookup"><span data-stu-id="18cad-730">Identification Type = "Passport"</span></span>
- <span data-ttu-id="18cad-731">Дата выпуска</span><span class="sxs-lookup"><span data-stu-id="18cad-731">Issued Date</span></span>
- <span data-ttu-id="18cad-732">Дата окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="18cad-732">Expiration Date</span></span>

<span data-ttu-id="18cad-733">Сотрудники могут объявить несколько идентификационных номеров для типа идентификатора **Паспорт**.</span><span class="sxs-lookup"><span data-stu-id="18cad-733">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="18cad-734">Тем не менее только запись текущего активного паспорта интегрируется в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="18cad-734">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="18cad-735">Если срок действия всех записей паспорта истек, в Dayforce интегрируется тот, который был выдан последним.</span><span class="sxs-lookup"><span data-stu-id="18cad-735">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
