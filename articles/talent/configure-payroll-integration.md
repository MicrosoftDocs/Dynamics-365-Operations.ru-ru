---
title: Настройка интеграции зарплаты между Talent и Dayforce
description: В этом разделе объясняется, как настроить интеграцию между Microsoft Dynamics 365 Talent и Ceridian Dayforce таким образом, чтобы вы могли обработать период оплаты.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
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
ms.openlocfilehash: 075b2bdfa08bb190f66b6d60074e1263feedcf70
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898548"
---
# <a name="configure-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="ece75-103">Настройка интеграции зарплаты между Talent и Dayforce</span><span class="sxs-lookup"><span data-stu-id="ece75-103">Configure payroll integration between Talent and Dayforce</span></span>

<span data-ttu-id="ece75-104">Интеграция между Microsoft Dynamics 365 Talent и Ceridian Dayforce зависит от ряда действий настройки, описанных в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="ece75-104">The integration between Microsoft Dynamics 365 Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="ece75-105">Необходимо настроить интеграцию в Talent и Dayforce перед обработкой периода оплаты.</span><span class="sxs-lookup"><span data-stu-id="ece75-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="ece75-106">При использовании службы, например Dayforce, для выполнения оплаты, необходимо включить интеграцию в Talent.</span><span class="sxs-lookup"><span data-stu-id="ece75-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="ece75-107">Интеграция требует определенных данных из Talent.</span><span class="sxs-lookup"><span data-stu-id="ece75-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="ece75-108">Таким образом необходимо убедиться, что данные, отображаемые в Dayforce, настроены в Talent таким образом, чтобы поддерживать интеграцию.</span><span class="sxs-lookup"><span data-stu-id="ece75-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="ece75-109">Интеграция использует следующие широкие категории данных:</span><span class="sxs-lookup"><span data-stu-id="ece75-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="ece75-110">Данные управления персоналом</span><span class="sxs-lookup"><span data-stu-id="ece75-110">Human resources data</span></span>
- <span data-ttu-id="ece75-111">Данные о компенсациях</span><span class="sxs-lookup"><span data-stu-id="ece75-111">Compensation data</span></span>
- <span data-ttu-id="ece75-112">Данные о заработной плате, например циклы оплаты, периоды оплаты и коды начисления зарплаты</span><span class="sxs-lookup"><span data-stu-id="ece75-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="ece75-113">Данные о работнике</span><span class="sxs-lookup"><span data-stu-id="ece75-113">Worker data</span></span>

<span data-ttu-id="ece75-114">В этом разделе описываются шаги, которые необходимо выполнить, чтобы включить интеграцию.</span><span class="sxs-lookup"><span data-stu-id="ece75-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="ece75-115">Здесь также объясняются типы данных и сведения о конфигурации, которые необходимы для интеграции.</span><span class="sxs-lookup"><span data-stu-id="ece75-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="ece75-116">Включение интеграции</span><span class="sxs-lookup"><span data-stu-id="ece75-116">Enable the integration</span></span>

<span data-ttu-id="ece75-117">В Talent необходимо включить интеграцию и ввести информацию о конфигурации для подключения к Dayforce.</span><span class="sxs-lookup"><span data-stu-id="ece75-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="ece75-118">Если требуется, чтобы проводки ГК, которые производятся, импортировались в Microsoft Dynamics 365 Finance, также необходимо установить учетную запись хранилища Microsoft Azure и ввести строку подключения хранилища Azure в Finance.</span><span class="sxs-lookup"><span data-stu-id="ece75-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="ece75-119">Чтобы включить интеграцию в Talent, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ece75-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="ece75-120">На странице **Администрирование системы** выберите **Конфигурация интеграции**.</span><span class="sxs-lookup"><span data-stu-id="ece75-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="ece75-121">Введите безопасную конечную точку FTP и путь к безопасной папке FTP.</span><span class="sxs-lookup"><span data-stu-id="ece75-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="ece75-122">Введите имя пользователя и пароль пользователя, который будет иметь доступ к безопасной конечной точке и пути к папке FTP.</span><span class="sxs-lookup"><span data-stu-id="ece75-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="ece75-123">Проверьте подключение, как требуется, а также установите для параметра **Включить интеграцию зарплаты** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="ece75-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="ece75-124">При включении интеграции создаются пакет экспорта данных и файлы, и задается значение частоты.</span><span class="sxs-lookup"><span data-stu-id="ece75-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="ece75-125">Можно изменить эту частоту, как требуется.</span><span class="sxs-lookup"><span data-stu-id="ece75-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="ece75-126">Дополнительные сведения об учетных записях хранилища Azure и строке подключения хранилища Azure см. в следующих разделах Azure:</span><span class="sxs-lookup"><span data-stu-id="ece75-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="ece75-127">Об учетных записях хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="ece75-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="ece75-128">Настройка строки подключения хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="ece75-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="ece75-129">Технические сведения о включении интеграции зарплаты</span><span class="sxs-lookup"><span data-stu-id="ece75-129">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="ece75-130">Включение интеграции зарплаты имеет два основных эффекта:</span><span class="sxs-lookup"><span data-stu-id="ece75-130">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="ece75-131">Будет создан проект экспорта данных с именем "Экспорт интеграции зарплаты".</span><span class="sxs-lookup"><span data-stu-id="ece75-131">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="ece75-132">Этот проект содержит сущности и поля, необходимые для интеграции зарплаты.</span><span class="sxs-lookup"><span data-stu-id="ece75-132">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="ece75-133">Чтобы проверить этот проект, перейдите в раздел **Администрирование системы**, выберите плитку **Управление данными**, затем откройте проект данных из списка проектов.</span><span class="sxs-lookup"><span data-stu-id="ece75-133">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="ece75-134">Это пакетное задание выполняет проект экспорта данных, шифрует получившийся пакет данных и передает файл пакета данных на конечную точку SFTP, настроенную на экране **Конфигурация интеграции**.</span><span class="sxs-lookup"><span data-stu-id="ece75-134">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="ece75-135">Пакет данных, переданный в конечную точку SFTP, шифруется с помощью уникального для пакета ключа.</span><span class="sxs-lookup"><span data-stu-id="ece75-135">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="ece75-136">Ключ находится в хранилище ключей Azure Key Vault, доступном только для по Ceridian.</span><span class="sxs-lookup"><span data-stu-id="ece75-136">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="ece75-137">Невозможно расшифровать и проверить содержимое пакета данных.</span><span class="sxs-lookup"><span data-stu-id="ece75-137">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="ece75-138">Если необходимо изучить содержимое пакета данных, необходимо экспортировать проект данных "Экспорт интеграции зарплаты" вручную, загрузить его и затем открыть.</span><span class="sxs-lookup"><span data-stu-id="ece75-138">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="ece75-139">При экспорте вручную шифрование или передача пакетов не применяются.</span><span class="sxs-lookup"><span data-stu-id="ece75-139">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="ece75-140">Настройка данных</span><span class="sxs-lookup"><span data-stu-id="ece75-140">Configure your data</span></span> 

<span data-ttu-id="ece75-141">Для обработки зарплаты необходимо настроить данные управления персоналом в Talent.</span><span class="sxs-lookup"><span data-stu-id="ece75-141">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="ece75-142">Необходимо настроить организационные данные, такие как задания и должности, вместе со сведениями о льготах и компенсациях.</span><span class="sxs-lookup"><span data-stu-id="ece75-142">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="ece75-143">Эта информация содержит сведения о занятости, оплате и вычетах, которые необходимы для формирования заработной платы сотрудника.</span><span class="sxs-lookup"><span data-stu-id="ece75-143">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="ece75-144">Данные управления персоналом</span><span class="sxs-lookup"><span data-stu-id="ece75-144">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="ece75-145">Льготы</span><span class="sxs-lookup"><span data-stu-id="ece75-145">Benefits</span></span> 

<span data-ttu-id="ece75-146">Человеческие ресурсы обеспечивают инструменты для настройки и поддержки льгот, вычетов и планов компенсации работникам, которые организация предлагает или обрабатывает для своих работников.</span><span class="sxs-lookup"><span data-stu-id="ece75-146">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="ece75-147">При создании льгот имейте в виду следующие данные и конфигурации, которые используются в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="ece75-147">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="ece75-148">Планы льгот</span><span class="sxs-lookup"><span data-stu-id="ece75-148">Benefit plans</span></span>

- <span data-ttu-id="ece75-149">План (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-149">Plan (required)</span></span>
- <span data-ttu-id="ece75-150">Тип (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-150">Type (required)</span></span>
- <span data-ttu-id="ece75-151">Влияние на зарплату (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-151">Payroll impact (required)</span></span>
- <span data-ttu-id="ece75-152">Погасить задолженность</span><span class="sxs-lookup"><span data-stu-id="ece75-152">Recover arrears</span></span>
- <span data-ttu-id="ece75-153">Метод вычета</span><span class="sxs-lookup"><span data-stu-id="ece75-153">Deduction method</span></span>
- <span data-ttu-id="ece75-154">Приоритет вычета</span><span class="sxs-lookup"><span data-stu-id="ece75-154">Deduction priority</span></span>
- <span data-ttu-id="ece75-155">Период лимита</span><span class="sxs-lookup"><span data-stu-id="ece75-155">Limit period</span></span>
- <span data-ttu-id="ece75-156">Сумма лимита</span><span class="sxs-lookup"><span data-stu-id="ece75-156">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="ece75-157">Льготы</span><span class="sxs-lookup"><span data-stu-id="ece75-157">Benefits</span></span>

- <span data-ttu-id="ece75-158">План (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-158">Plan (required)</span></span>
- <span data-ttu-id="ece75-159">Тип (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-159">Type (required)</span></span>
- <span data-ttu-id="ece75-160">Параметр (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-160">Option (required)</span></span>
- <span data-ttu-id="ece75-161">Код льготы (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-161">Benefit ID (required)</span></span>
- <span data-ttu-id="ece75-162">Частота</span><span class="sxs-lookup"><span data-stu-id="ece75-162">Frequency</span></span>
- <span data-ttu-id="ece75-163">База</span><span class="sxs-lookup"><span data-stu-id="ece75-163">Basis</span></span>
- <span data-ttu-id="ece75-164">Сумма или ставка</span><span class="sxs-lookup"><span data-stu-id="ece75-164">Amount or rate</span></span>
- <span data-ttu-id="ece75-165">Код дохода</span><span class="sxs-lookup"><span data-stu-id="ece75-165">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="ece75-166">Поддерживаемые частоты</span><span class="sxs-lookup"><span data-stu-id="ece75-166">Supported frequencies</span></span> 

- <span data-ttu-id="ece75-167">Еженедельно</span><span class="sxs-lookup"><span data-stu-id="ece75-167">Weekly</span></span>
- <span data-ttu-id="ece75-168">Один раз в две недели</span><span class="sxs-lookup"><span data-stu-id="ece75-168">Bi-weekly</span></span>
- <span data-ttu-id="ece75-169">Два раза в месяц</span><span class="sxs-lookup"><span data-stu-id="ece75-169">Semi-monthly</span></span>
- <span data-ttu-id="ece75-170">Один раз в месяц</span><span class="sxs-lookup"><span data-stu-id="ece75-170">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="ece75-171">Поддерживаемые базы</span><span class="sxs-lookup"><span data-stu-id="ece75-171">Supported bases</span></span> 

- <span data-ttu-id="ece75-172">Фиксированная сумма</span><span class="sxs-lookup"><span data-stu-id="ece75-172">Fixed amount</span></span>
- <span data-ttu-id="ece75-173">Процент дохода</span><span class="sxs-lookup"><span data-stu-id="ece75-173">Percent of earnings</span></span>
- <span data-ttu-id="ece75-174">Продуктивные часы</span><span class="sxs-lookup"><span data-stu-id="ece75-174">Productive hours</span></span>

<span data-ttu-id="ece75-175">Dayforce создает следующие вычеты на основе влияния на зарплату, которое определено в плане льгот.</span><span class="sxs-lookup"><span data-stu-id="ece75-175">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="ece75-176">Выбор в Talent</span><span class="sxs-lookup"><span data-stu-id="ece75-176">Selection in Talent</span></span>        | <span data-ttu-id="ece75-177">Результат в Dayforce</span><span class="sxs-lookup"><span data-stu-id="ece75-177">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="ece75-178">None</span><span class="sxs-lookup"><span data-stu-id="ece75-178">None</span></span>                       | <span data-ttu-id="ece75-179">Вычет не создается.</span><span class="sxs-lookup"><span data-stu-id="ece75-179">No deduction is created.</span></span>                      |
| <span data-ttu-id="ece75-180">Только удержание</span><span class="sxs-lookup"><span data-stu-id="ece75-180">Deduction only</span></span>             | <span data-ttu-id="ece75-181">Вычет сотрудника будет создан.</span><span class="sxs-lookup"><span data-stu-id="ece75-181">An employee deduction is created.</span></span>             |
| <span data-ttu-id="ece75-182">Только вклад</span><span class="sxs-lookup"><span data-stu-id="ece75-182">Contribution only</span></span>          | <span data-ttu-id="ece75-183">Вычет работодателя будет создан.</span><span class="sxs-lookup"><span data-stu-id="ece75-183">An employer deduction is created.</span></span>             |
| <span data-ttu-id="ece75-184">Удержание и вклад</span><span class="sxs-lookup"><span data-stu-id="ece75-184">Deduction and contribution</span></span> | <span data-ttu-id="ece75-185">Создаются вычеты сотрудников и работодателя.</span><span class="sxs-lookup"><span data-stu-id="ece75-185">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="ece75-186">Дополнительные сведения о том, как определять и управлять программами льгот, см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="ece75-186">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="ece75-187">Реализация программы льгот сотрудника</span><span class="sxs-lookup"><span data-stu-id="ece75-187">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="ece75-188">Создание новой льготы</span><span class="sxs-lookup"><span data-stu-id="ece75-188">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="ece75-189">Определение правил и политик проверки прав на льготы</span><span class="sxs-lookup"><span data-stu-id="ece75-189">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="ece75-190">Регистрация и удаление льгот для работников</span><span class="sxs-lookup"><span data-stu-id="ece75-190">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="ece75-191">Компенсация</span><span class="sxs-lookup"><span data-stu-id="ece75-191">Compensation</span></span> 

<span data-ttu-id="ece75-192">Управление компенсациями используется для управления предоставлением базовой оплаты и вознаграждений.</span><span class="sxs-lookup"><span data-stu-id="ece75-192">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="ece75-193">Тарифные ставки и единовременные надбавки контролируются с помощью планов фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="ece75-193">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="ece75-194">Поощрительные выплаты, такие как премии, вознаграждения за производительность, опционы на покупку акций и гранты, а также одноразовые компенсации, контролируются с помощью планов переменных компенсаций.</span><span class="sxs-lookup"><span data-stu-id="ece75-194">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="ece75-195">Dayforce использует сведения о компенсации для расчета почасовой или годовой ставки сотрудника.</span><span class="sxs-lookup"><span data-stu-id="ece75-195">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="ece75-196">Требуются планы фиксированной компенсации и преобразования ставки оплаты.</span><span class="sxs-lookup"><span data-stu-id="ece75-196">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="ece75-197">Сотрудники должны быть связаны с планом фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="ece75-197">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="ece75-198">Дополнительные сведения о планах компенсации см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="ece75-198">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="ece75-199">Создание планов фиксированной компенсации</span><span class="sxs-lookup"><span data-stu-id="ece75-199">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="ece75-200">Создание планов переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="ece75-200">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="ece75-201">Разработка структуры и планов зарплаты/компенсации</span><span class="sxs-lookup"><span data-stu-id="ece75-201">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="ece75-202">Обработка компенсаций</span><span class="sxs-lookup"><span data-stu-id="ece75-202">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="ece75-203">Определение процесса компенсации и расчет результатов</span><span class="sxs-lookup"><span data-stu-id="ece75-203">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="ece75-204">Включение сотрудника в план фиксированных компенсаций</span><span class="sxs-lookup"><span data-stu-id="ece75-204">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="ece75-205">Включение сотрудника в план переменных компенсаций</span><span class="sxs-lookup"><span data-stu-id="ece75-205">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="ece75-206">Должности</span><span class="sxs-lookup"><span data-stu-id="ece75-206">Jobs</span></span> 

<span data-ttu-id="ece75-207">Должностные обязанности — это набор задач и обязанностей, которые возлагаются на занимающее эту задание лицо.</span><span class="sxs-lookup"><span data-stu-id="ece75-207">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="ece75-208">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="ece75-208">For more information, see the following topics:</span></span>

- [<span data-ttu-id="ece75-209">Настройка компонентов должности</span><span class="sxs-lookup"><span data-stu-id="ece75-209">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="ece75-210">Определение новых заданий</span><span class="sxs-lookup"><span data-stu-id="ece75-210">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="ece75-211">Должности</span><span class="sxs-lookup"><span data-stu-id="ece75-211">Positions</span></span>

<span data-ttu-id="ece75-212">Позиция — это индивидуальный экземпляр должности.</span><span class="sxs-lookup"><span data-stu-id="ece75-212">A position is an individual instance of a job.</span></span> <span data-ttu-id="ece75-213">Например, должность "Менеджер по продажам (восток)" — это одна из должностей, связанных с должностными обязанностями "Менеджер по продажам".</span><span class="sxs-lookup"><span data-stu-id="ece75-213">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="ece75-214">Должность существует в отделе.</span><span class="sxs-lookup"><span data-stu-id="ece75-214">A position exists in a department.</span></span> <span data-ttu-id="ece75-215">Только один работник может быть связан с каждой должностью.</span><span class="sxs-lookup"><span data-stu-id="ece75-215">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="ece75-216">Учитывайте следующие данные и конфигурацию при настройке должностей:</span><span class="sxs-lookup"><span data-stu-id="ece75-216">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="ece75-217">Должность (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-217">Position (required)</span></span>
- <span data-ttu-id="ece75-218">Описание (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-218">Description (required)</span></span>
- <span data-ttu-id="ece75-219">Должностные обязанности (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-219">Job (required)</span></span>
- <span data-ttu-id="ece75-220">Отдел (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-220">Department (required)</span></span>
- <span data-ttu-id="ece75-221">Тип должности (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-221">Position type (required)</span></span>
- <span data-ttu-id="ece75-222">Эквивалент полной занятости</span><span class="sxs-lookup"><span data-stu-id="ece75-222">Full-time equivalent</span></span>
- <span data-ttu-id="ece75-223">Обычные часы за год (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-223">Annual regular hours (required)</span></span>
- <span data-ttu-id="ece75-224">Оплачивается юридическим лицом (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-224">Paid by legal entity (required)</span></span>
- <span data-ttu-id="ece75-225">Цикл оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-225">Pay cycle (required)</span></span>
- <span data-ttu-id="ece75-226">Финансовая аналитика по умолчанию — центр затрат (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-226">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="ece75-227">Назначение работника — работник, начало назначения, окончание назначения, код причины</span><span class="sxs-lookup"><span data-stu-id="ece75-227">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="ece75-228">Если несколько должностей в одном отделе связаны с одними и теми же должностными обязанностями, они объединяются в одну должность в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="ece75-228">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="ece75-229">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="ece75-229">For more information, see the following topics:</span></span>

- [<span data-ttu-id="ece75-230">Организация трудовых ресурсов с использованием подразделений, должностей и штатных единиц</span><span class="sxs-lookup"><span data-stu-id="ece75-230">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="ece75-231">Настройка должностей</span><span class="sxs-lookup"><span data-stu-id="ece75-231">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="ece75-232">Отделы</span><span class="sxs-lookup"><span data-stu-id="ece75-232">Departments</span></span>

<span data-ttu-id="ece75-233">Подразделение — это операционная единица, которая представляет собой категорию или функциональную область в организации.</span><span class="sxs-lookup"><span data-stu-id="ece75-233">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="ece75-234">Подразделение отвечает за конкретную область деятельности организации, например продажи, бухгалтерский учет или управление персоналом.</span><span class="sxs-lookup"><span data-stu-id="ece75-234">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="ece75-235">Подразделения можно использовать для формирования отчетности по функциональным областям.</span><span class="sxs-lookup"><span data-stu-id="ece75-235">You can use departments to report on functional areas.</span></span> <span data-ttu-id="ece75-236">Подразделения могут нести ответственность за прибыли и убытки.</span><span class="sxs-lookup"><span data-stu-id="ece75-236">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="ece75-237">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="ece75-237">For more information, see the following topics:</span></span>

- [<span data-ttu-id="ece75-238">Создание подразделения и связывание его с иерархией подразделений</span><span class="sxs-lookup"><span data-stu-id="ece75-238">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="ece75-239">Определение новых подразделений</span><span class="sxs-lookup"><span data-stu-id="ece75-239">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="ece75-240">Циклы оплаты и платежные периоды</span><span class="sxs-lookup"><span data-stu-id="ece75-240">Pay cycles and pay periods</span></span>

<span data-ttu-id="ece75-241">Цикл оплаты определяет, как часто рассчитывается зарплата и определенные дни, когда работники получают зарплату.</span><span class="sxs-lookup"><span data-stu-id="ece75-241">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="ece75-242">Например, цикл оплаты может быть ежемесячным, и сотрудникам может выплачиваться зарплата в последний день месяца.</span><span class="sxs-lookup"><span data-stu-id="ece75-242">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="ece75-243">Кроме того, цикл оплаты может быть еженедельным, а сотрудники могут получать зарплату по вторникам после завершения периода оплаты.</span><span class="sxs-lookup"><span data-stu-id="ece75-243">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="ece75-244">Циклы оплаты назначаются должностям для управления выплатами работникам для этих должностей.</span><span class="sxs-lookup"><span data-stu-id="ece75-244">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="ece75-245">После создания циклов зарплаты можно создать платежные периоды для каждого цикла.</span><span class="sxs-lookup"><span data-stu-id="ece75-245">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="ece75-246">Каждый платежный период включает дату оплаты по умолчанию, которая основана на информации, предоставленной вами.</span><span class="sxs-lookup"><span data-stu-id="ece75-246">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="ece75-247">Однако можно изменить дату платежа по умолчанию в платежный период для учета исключений, например, когда дата оплаты приходится на праздник.</span><span class="sxs-lookup"><span data-stu-id="ece75-247">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="ece75-248">Dayforce использует следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="ece75-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="ece75-249">Цикл оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-249">Pay cycle (required)</span></span>
- <span data-ttu-id="ece75-250">Частота циклов оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-250">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="ece75-251">Дата начала периода (первый период оплаты обязателен)</span><span class="sxs-lookup"><span data-stu-id="ece75-251">Period start date (first pay period required)</span></span>
- <span data-ttu-id="ece75-252">Дата платежа по умолчанию (первый период оплаты обязателен)</span><span class="sxs-lookup"><span data-stu-id="ece75-252">Default payment date (first pay period required)</span></span>

<span data-ttu-id="ece75-253">Эта информация интегрирована с Dayforce как платежные группы, и разделяется по странам или регионам для каждого цикла оплаты.</span><span class="sxs-lookup"><span data-stu-id="ece75-253">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="ece75-254">Хотя бы один платежный период должен быть создан до интеграции.</span><span class="sxs-lookup"><span data-stu-id="ece75-254">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="ece75-255">Dayforce создает календари группы оплаты и даты оплаты на основе даты начала первого периода оплаты и даты оплаты по умолчанию, настроенных в Talent.</span><span class="sxs-lookup"><span data-stu-id="ece75-255">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="ece75-256">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="ece75-256">Earning codes</span></span>

<span data-ttu-id="ece75-257">Коды доходов уникально определяют каждый типа доходов, которые работники получают.</span><span class="sxs-lookup"><span data-stu-id="ece75-257">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="ece75-258">Эти коды имеют различные параметры, которые относятся к доходам, таких как правила учета, налоговые законы, требования к отчетности и возможности брутто в большую сторону.</span><span class="sxs-lookup"><span data-stu-id="ece75-258">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="ece75-259">Dayforce использует следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="ece75-259">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="ece75-260">Код дохода (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-260">Earning Code (required)</span></span>
- <span data-ttu-id="ece75-261">описание</span><span class="sxs-lookup"><span data-stu-id="ece75-261">Description</span></span>
- <span data-ttu-id="ece75-262">Единица измерения</span><span class="sxs-lookup"><span data-stu-id="ece75-262">Unit of measure</span></span>
- <span data-ttu-id="ece75-263">Продуктивный</span><span class="sxs-lookup"><span data-stu-id="ece75-263">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="ece75-264">Данные о работнике</span><span class="sxs-lookup"><span data-stu-id="ece75-264">Worker data</span></span>

<span data-ttu-id="ece75-265">Записи о различных типах сотрудников, которые имеются у вас, важны для вашей системы управления персоналом и системы расчета заработной платы.</span><span class="sxs-lookup"><span data-stu-id="ece75-265">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="ece75-266">Вводимые данные могут использоваться для отслеживания сведений о работниках и личной информации.</span><span class="sxs-lookup"><span data-stu-id="ece75-266">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="ece75-267">По работникам может храниться следующая информация.</span><span class="sxs-lookup"><span data-stu-id="ece75-267">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="ece75-268">**Основная** — базовые сведения о работнике, такие как контактные данные, демографические данные, идентифицирующие сведения, состав семье, сведения о службе в армии, данные об иностранных сотрудниках, персональные контакты и контакты на случай экстренных ситуаций.</span><span class="sxs-lookup"><span data-stu-id="ece75-268">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="ece75-269">**Занятость** — сведения о занятости работников, такие как участие в компании или организации, должность, дату начала и завершения работы, способность к работе, условия найма, пенсия, отпуска и сведения о переездах.</span><span class="sxs-lookup"><span data-stu-id="ece75-269">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="ece75-270">**Отпуск и отсутствие** — сведения об отпусках или пропуска работника, рабочие календари, проводки отсутствия и соответствующие настройки.</span><span class="sxs-lookup"><span data-stu-id="ece75-270">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="ece75-271">**Заработная плата и компенсации** — сведения о планах вознаграждениях и зарплате работника, такие как премии, комиссии, налоги, выход на пенсию и вычеты из зарплаты.</span><span class="sxs-lookup"><span data-stu-id="ece75-271">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="ece75-272">При вводе сведений о работнике имейте в виду следующие данные и конфигурации, которые используются в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="ece75-272">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="ece75-273">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="ece75-273">General information</span></span>

- <span data-ttu-id="ece75-274">Табельный номер (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-274">Personnel number (required)</span></span>
- <span data-ttu-id="ece75-275">Имя (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-275">First name (required)</span></span>
- <span data-ttu-id="ece75-276">Фамилия (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-276">Last name (required)</span></span>
- <span data-ttu-id="ece75-277">Отчество</span><span class="sxs-lookup"><span data-stu-id="ece75-277">Middle name</span></span>
- <span data-ttu-id="ece75-278">Дата начала стажа</span><span class="sxs-lookup"><span data-stu-id="ece75-278">Seniority date</span></span>
- <span data-ttu-id="ece75-279">Известно как</span><span class="sxs-lookup"><span data-stu-id="ece75-279">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="ece75-280">Личная информация</span><span class="sxs-lookup"><span data-stu-id="ece75-280">Personal information</span></span>

- <span data-ttu-id="ece75-281">Семейное положение (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-281">Marital status (required)</span></span>
- <span data-ttu-id="ece75-282">Дата рождения (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-282">Birth date (required)</span></span>
- <span data-ttu-id="ece75-283">Пол (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-283">Gender (required)</span></span>
- <span data-ttu-id="ece75-284">Лицо с инвалидностью</span><span class="sxs-lookup"><span data-stu-id="ece75-284">Person with disabilities</span></span>
- <span data-ttu-id="ece75-285">Национальность, регион страны (только в Мексике)</span><span class="sxs-lookup"><span data-stu-id="ece75-285">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="ece75-286">Адресная информация</span><span class="sxs-lookup"><span data-stu-id="ece75-286">Address information</span></span>

- <span data-ttu-id="ece75-287">Основной (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-287">Primary (required)</span></span>
- <span data-ttu-id="ece75-288">Страна/регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-288">Country/region (required)</span></span>
- <span data-ttu-id="ece75-289">Почтовый индекс (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-289">Postal code (required)</span></span>
- <span data-ttu-id="ece75-290">Номер дома (обязательно) (только для Мексики)</span><span class="sxs-lookup"><span data-stu-id="ece75-290">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="ece75-291">Дополнение здания (только в Мексике)</span><span class="sxs-lookup"><span data-stu-id="ece75-291">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="ece75-292">Город (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-292">City (required)</span></span>
- <span data-ttu-id="ece75-293">Регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-293">State (required)</span></span>
- <span data-ttu-id="ece75-294">Район (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-294">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="ece75-295">Контактная информация</span><span class="sxs-lookup"><span data-stu-id="ece75-295">Contact information</span></span> 

- <span data-ttu-id="ece75-296">Основной (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-296">Primary (required)</span></span>
- <span data-ttu-id="ece75-297">Контактный номер (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-297">Contact number (required)</span></span>
- <span data-ttu-id="ece75-298">Расширение</span><span class="sxs-lookup"><span data-stu-id="ece75-298">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="ece75-299">Информация по зарплате и коды дохода</span><span class="sxs-lookup"><span data-stu-id="ece75-299">Payroll information and earning codes</span></span>

<span data-ttu-id="ece75-300">Сотрудникам можно назначить конкретные доходы с заданной периодичностью оплаты и предпочтительный метод оплаты.</span><span class="sxs-lookup"><span data-stu-id="ece75-300">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="ece75-301">Следующие поля используются в Dayforce для обеспечения использования этих параметров и настроек.</span><span class="sxs-lookup"><span data-stu-id="ece75-301">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="ece75-302">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="ece75-302">Earning codes</span></span>

- <span data-ttu-id="ece75-303">Должность (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-303">Position (required)</span></span>
- <span data-ttu-id="ece75-304">Код дохода (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-304">Earning Code (required)</span></span>
- <span data-ttu-id="ece75-305">Частота (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-305">Frequency (required)</span></span>
- <span data-ttu-id="ece75-306">Сумма (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-306">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="ece75-307">Информация по зарплате</span><span class="sxs-lookup"><span data-stu-id="ece75-307">Payroll information</span></span>

- <span data-ttu-id="ece75-308">Способ оплаты</span><span class="sxs-lookup"><span data-stu-id="ece75-308">Payment Method</span></span>
- <span data-ttu-id="ece75-309">Экономический регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-309">Economic Region (required)</span></span>
- <span data-ttu-id="ece75-310">ИД льгот сотрудников</span><span class="sxs-lookup"><span data-stu-id="ece75-310">Employee Benefits ID</span></span>
- <span data-ttu-id="ece75-311">Идентификационный номер (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-311">National ID Number (required)</span></span>
- <span data-ttu-id="ece75-312">Номер документа о воинской службе</span><span class="sxs-lookup"><span data-stu-id="ece75-312">Military Service Number</span></span>
- <span data-ttu-id="ece75-313">Код смены (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-313">Shift ID (required)</span></span>
- <span data-ttu-id="ece75-314">Налоговой номер (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-314">Tax Number (required)</span></span>
- <span data-ttu-id="ece75-315">Код профсоюза (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-315">Union ID (required)</span></span>
- <span data-ttu-id="ece75-316">Идентификатор рабочего дня (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-316">Work Day ID (required)</span></span>
- <span data-ttu-id="ece75-317">Номер разрешения на работу</span><span class="sxs-lookup"><span data-stu-id="ece75-317">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="ece75-318">Для метода оплаты в Мексике поддерживает **Наличные деньги**, **Чек** (физический чек компании) и **Электронный платеж**.</span><span class="sxs-lookup"><span data-stu-id="ece75-318">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="ece75-319">Если способ оплаты не указан, **Чек** используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ece75-319">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="ece75-320">Сведения о трудоустройстве</span><span class="sxs-lookup"><span data-stu-id="ece75-320">Employment details</span></span>

<span data-ttu-id="ece75-321">Подробная история занятости используется как ключевая информация для извлечения статуса найма, увольнения и повторного найма сотрудника в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="ece75-321">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="ece75-322">Dayforce поддерживает только одну активную запись о приеме на работу одновременно.</span><span class="sxs-lookup"><span data-stu-id="ece75-322">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="ece75-323">Дата начала трудоустройства (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-323">Employment start date (required)</span></span>
- <span data-ttu-id="ece75-324">Дата окончания занятости</span><span class="sxs-lookup"><span data-stu-id="ece75-324">Employment end date</span></span>
- <span data-ttu-id="ece75-325">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="ece75-325">Start date</span></span>
- <span data-ttu-id="ece75-326">Скорректированная дата приема на работу</span><span class="sxs-lookup"><span data-stu-id="ece75-326">Adjusted start date</span></span>
- <span data-ttu-id="ece75-327">Дата увольнения (обязательно после увольнения)</span><span class="sxs-lookup"><span data-stu-id="ece75-327">Termination date (required upon termination)</span></span>
- <span data-ttu-id="ece75-328">Причина увольнения (обязательно после увольнения)</span><span class="sxs-lookup"><span data-stu-id="ece75-328">Termination reason (required upon termination)</span></span>

<span data-ttu-id="ece75-329">Ключевые даты сотрудника получаются на основе следующих сведений.</span><span class="sxs-lookup"><span data-stu-id="ece75-329">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="ece75-330">Talent</span><span class="sxs-lookup"><span data-stu-id="ece75-330">Talent</span></span>                | <span data-ttu-id="ece75-331">Dayforce</span><span class="sxs-lookup"><span data-stu-id="ece75-331">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece75-332">Самая последняя дата приема на работу</span><span class="sxs-lookup"><span data-stu-id="ece75-332">Most recent hire date</span></span> | <span data-ttu-id="ece75-333">Дата приема на работу для текущей записи истории занятости, которая еще не завершена</span><span class="sxs-lookup"><span data-stu-id="ece75-333">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="ece75-334">Дата увольнения</span><span class="sxs-lookup"><span data-stu-id="ece75-334">Termination date</span></span>      | <span data-ttu-id="ece75-335">Дата увольнения для текущей записи истории занятости, которая еще не завершена</span><span class="sxs-lookup"><span data-stu-id="ece75-335">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="ece75-336">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="ece75-336">Start date</span></span>            | <span data-ttu-id="ece75-337">Скорректированная дата приема на работу, дата приема на работу или дата приема на работу текущей неактивной записи история занятости</span><span class="sxs-lookup"><span data-stu-id="ece75-337">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="ece75-338">Дата первоначального приема на работу</span><span class="sxs-lookup"><span data-stu-id="ece75-338">Original hire date</span></span>    | <span data-ttu-id="ece75-339">Дата приема на работу самой ранней записи истории приема на работу</span><span class="sxs-lookup"><span data-stu-id="ece75-339">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="ece75-340">Компенсация</span><span class="sxs-lookup"><span data-stu-id="ece75-340">Compensation</span></span>

<span data-ttu-id="ece75-341">План фиксированной компенсации должен быть связан с каждой основной должностью работника на протяжении всего периода занятости.</span><span class="sxs-lookup"><span data-stu-id="ece75-341">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="ece75-342">Этот период начинается на даты, в которую сотрудник был нанят (или начальная дата приема на работу) и продолжается до увольнения.</span><span class="sxs-lookup"><span data-stu-id="ece75-342">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="ece75-343">Дата вступления в силу (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-343">Effective Date (required)</span></span>
- <span data-ttu-id="ece75-344">Срок действия</span><span class="sxs-lookup"><span data-stu-id="ece75-344">Expiration date</span></span>
- <span data-ttu-id="ece75-345">Ставка оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-345">Pay Rate (required)</span></span>
- <span data-ttu-id="ece75-346">Преобразования ставки оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-346">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="ece75-347">Годовой эквивалент (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-347">Annual equivalent (required)</span></span>
- <span data-ttu-id="ece75-348">Почасовой эквивалент (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-348">Hourly equivalent (required)</span></span>

<span data-ttu-id="ece75-349">Если сотрудник с почасовой оплатой имеет несколько должностей, фиксированная компенсация основной должности импортируется в Dayforce как базовая ставка/зарплата уровня сотрудника.</span><span class="sxs-lookup"><span data-stu-id="ece75-349">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="ece75-350">Дня неосновных должностей почасовая ставка сохраняется в соответствующей должности в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="ece75-350">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="ece75-351">Если штатный сотрудник имеет несколько должностей, суммарная почасовая ставка и годовая заработная плата для всех активных должностей определяется и используется в качестве базовой ставки/зарплаты уровня сотрудника.</span><span class="sxs-lookup"><span data-stu-id="ece75-351">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="ece75-352">Идентификационные номера</span><span class="sxs-lookup"><span data-stu-id="ece75-352">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="ece75-353">Код социального страхования</span><span class="sxs-lookup"><span data-stu-id="ece75-353">Social Security identifier</span></span> 

<span data-ttu-id="ece75-354">Каждый сотрудник должен иметь один первичный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="ece75-354">Every employee must have one primary identifier.</span></span> <span data-ttu-id="ece75-355">Этот идентификатор должен быть идентификатором типа **SSN**.</span><span class="sxs-lookup"><span data-stu-id="ece75-355">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="ece75-356">В Dayforce он автоматически извлекается как код социального страхования сотрудника, который необходим для приема на работу.</span><span class="sxs-lookup"><span data-stu-id="ece75-356">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="ece75-357">Основной (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-357">Primary (required)</span></span>
- <span data-ttu-id="ece75-358">Тип идентификации = "SSN"</span><span class="sxs-lookup"><span data-stu-id="ece75-358">Identification Type = "SSN"</span></span>
- <span data-ttu-id="ece75-359">Дата выпуска</span><span class="sxs-lookup"><span data-stu-id="ece75-359">Issued Date</span></span>
- <span data-ttu-id="ece75-360">Дата окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="ece75-360">Expiration Date</span></span>

<span data-ttu-id="ece75-361">Сотрудники могут объявить несколько идентификационных номеров для типа идентификатора **SSN**.</span><span class="sxs-lookup"><span data-stu-id="ece75-361">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="ece75-362">Тем не менее только запись, которая помечен как **Основная**, интегрируется в Dayforce, независимо от того, является ли номер активным или у него истек срок действия.</span><span class="sxs-lookup"><span data-stu-id="ece75-362">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="ece75-363">Банковские счета и выплаты</span><span class="sxs-lookup"><span data-stu-id="ece75-363">Bank accounts and disbursements</span></span>

<span data-ttu-id="ece75-364">Необходимо ввести действительную информацию о банковском счете для любого сотрудника, который выбирает оплату через перевод на банковский счет.</span><span class="sxs-lookup"><span data-stu-id="ece75-364">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="ece75-365">Talent</span><span class="sxs-lookup"><span data-stu-id="ece75-365">Talent</span></span>                         | <span data-ttu-id="ece75-366">Dayforce</span><span class="sxs-lookup"><span data-stu-id="ece75-366">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece75-367">Номер счета в банке (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-367">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="ece75-368">Код SWIFT (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-368">SWIFT code (required)</span></span>          | <span data-ttu-id="ece75-369">Поле **Код банка** используется при обработке зарплаты в Мексике.</span><span class="sxs-lookup"><span data-stu-id="ece75-369">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="ece75-370">Номер филиала (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-370">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="ece75-371">Тип банковского счета (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-371">Bank account type (required)</span></span>   | <span data-ttu-id="ece75-372">Поле **Тип счета** используется при обработке зарплаты в Мексике.</span><span class="sxs-lookup"><span data-stu-id="ece75-372">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="ece75-373">Поддерживаются значения **Выписка чека** и **Заработная плата**.</span><span class="sxs-lookup"><span data-stu-id="ece75-373">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="ece75-374">Работники, которые выбрали выплату переводом на банковский счет, должен предоставить ссылку на счет остатков, находящийся в юридическом лице с основным адресом в Мексике и связанный с действительным банковским счетом из мексиканского банка.</span><span class="sxs-lookup"><span data-stu-id="ece75-374">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="ece75-375">Все другие счета, не являющиеся счетами остатков, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="ece75-375">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="ece75-376">Адресная информация</span><span class="sxs-lookup"><span data-stu-id="ece75-376">Address information</span></span>

<span data-ttu-id="ece75-377">Каждый сотрудник должен иметь одно первичное местонахождение.</span><span class="sxs-lookup"><span data-stu-id="ece75-377">Every employee must have one primary location.</span></span> <span data-ttu-id="ece75-378">В Dayforce это расположение используется для определения основного места жительства сотрудника для целей налогообложения.</span><span class="sxs-lookup"><span data-stu-id="ece75-378">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="ece75-379">Основной (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-379">Primary (required)</span></span>
- <span data-ttu-id="ece75-380">Страна/регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-380">Country/region (required)</span></span>
- <span data-ttu-id="ece75-381">Почтовый индекс (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-381">Zip/postal code (required)</span></span>
- <span data-ttu-id="ece75-382">Улица (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-382">Street (required)</span></span>
- <span data-ttu-id="ece75-383">Номер дома (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-383">Street Number (required)</span></span>
- <span data-ttu-id="ece75-384">Дополнение здания</span><span class="sxs-lookup"><span data-stu-id="ece75-384">Building Complement</span></span>
- <span data-ttu-id="ece75-385">Город (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-385">City (required)</span></span>
- <span data-ttu-id="ece75-386">Регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-386">State (required)</span></span>
- <span data-ttu-id="ece75-387">Район (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-387">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="ece75-388">Настройка данных для расчета заработной платы в США и Канаде</span><span class="sxs-lookup"><span data-stu-id="ece75-388">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="ece75-389">Если вы создаете оплату для сотрудников в США и Канаде, необходимо настроить следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="ece75-389">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="ece75-390">Обязательно указывать подразделения для должностей.</span><span class="sxs-lookup"><span data-stu-id="ece75-390">Departments are required on positions.</span></span>
- <span data-ttu-id="ece75-391">Центры затрат должен быть заданы как финансовые аналитики и должны быть первым элементом в строке финансовой аналитики по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ece75-391">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="ece75-392">Можно настроить Talent, чтобы для должностей требовалось указывать подразделение.</span><span class="sxs-lookup"><span data-stu-id="ece75-392">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="ece75-393">Чтобы сделать это, выберите **Совместно используемые позиции управления персоналом > Позиции > Требовать подразделения для позиций**.</span><span class="sxs-lookup"><span data-stu-id="ece75-393">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="ece75-394">Рекомендуется включить этот параметр для интеграции.</span><span class="sxs-lookup"><span data-stu-id="ece75-394">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="ece75-395">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="ece75-395">Job types</span></span>

<span data-ttu-id="ece75-396">Типы должностей используются для группирования похожих должностных обязанностей в категории.</span><span class="sxs-lookup"><span data-stu-id="ece75-396">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="ece75-397">Типы должностей обязательны для обработки зарплаты в США и Канаде.</span><span class="sxs-lookup"><span data-stu-id="ece75-397">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="ece75-398">Примеры типов должностей включают полный рабочий день и неполный рабочий день, или зарплата и почасовая оплата.</span><span class="sxs-lookup"><span data-stu-id="ece75-398">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="ece75-399">Типы должностей сопоставляются с Dayforce как типы зарплаты, которые указывают тип оплаты сотрудника: почасовая или оклад.</span><span class="sxs-lookup"><span data-stu-id="ece75-399">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="ece75-400">Требуются следующие типы должностей и описаний.</span><span class="sxs-lookup"><span data-stu-id="ece75-400">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="ece75-401">Тип задания</span><span class="sxs-lookup"><span data-stu-id="ece75-401">Job type</span></span>   | <span data-ttu-id="ece75-402">описание</span><span class="sxs-lookup"><span data-stu-id="ece75-402">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="ece75-403">Почасовая</span><span class="sxs-lookup"><span data-stu-id="ece75-403">Hourly</span></span>     | <span data-ttu-id="ece75-404">Почасовая</span><span class="sxs-lookup"><span data-stu-id="ece75-404">Hourly</span></span>      |
| <span data-ttu-id="ece75-405">Оклад</span><span class="sxs-lookup"><span data-stu-id="ece75-405">Salaried</span></span>   | <span data-ttu-id="ece75-406">Оклад</span><span class="sxs-lookup"><span data-stu-id="ece75-406">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="ece75-407">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="ece75-407">Position types</span></span> 

<span data-ttu-id="ece75-408">С помощью типов должностей описывается, является ли должность занятостью на полный рабочий день, на неполный рабочий день или какой-либо другой.</span><span class="sxs-lookup"><span data-stu-id="ece75-408">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="ece75-409">Типы должностей сопоставляются с Dayforce как классы зарплаты, которые указывают тип оплаты сотрудника: полная занятость или частичная занятость.</span><span class="sxs-lookup"><span data-stu-id="ece75-409">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="ece75-410">Требуются следующие типы должностей и описаний.</span><span class="sxs-lookup"><span data-stu-id="ece75-410">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="ece75-411">Тип должности</span><span class="sxs-lookup"><span data-stu-id="ece75-411">Position type</span></span>   | <span data-ttu-id="ece75-412">описание</span><span class="sxs-lookup"><span data-stu-id="ece75-412">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="ece75-413">Полная занятость</span><span class="sxs-lookup"><span data-stu-id="ece75-413">Full-time</span></span>       | <span data-ttu-id="ece75-414">Работник с полной занятостью</span><span class="sxs-lookup"><span data-stu-id="ece75-414">Full time employee</span></span> |
| <span data-ttu-id="ece75-415">Частичная занятость</span><span class="sxs-lookup"><span data-stu-id="ece75-415">Part-time</span></span>       | <span data-ttu-id="ece75-416">Работник с частичной занятостью</span><span class="sxs-lookup"><span data-stu-id="ece75-416">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="ece75-417">Коды оснований</span><span class="sxs-lookup"><span data-stu-id="ece75-417">Reason codes</span></span>

<span data-ttu-id="ece75-418">Коды оснований содержат сведения о статусе сотрудника.</span><span class="sxs-lookup"><span data-stu-id="ece75-418">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="ece75-419">Коды оснований сопоставляются с Dayforce как причины статуса, которые определяют причину изменения статус должности или найма сотрудника.</span><span class="sxs-lookup"><span data-stu-id="ece75-419">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="ece75-420">Требуются следующие коды причин и описания.</span><span class="sxs-lookup"><span data-stu-id="ece75-420">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="ece75-421">Код основания</span><span class="sxs-lookup"><span data-stu-id="ece75-421">Reason code</span></span>    | <span data-ttu-id="ece75-422">описание</span><span class="sxs-lookup"><span data-stu-id="ece75-422">Description</span></span>      | <span data-ttu-id="ece75-423">Применимые сценарии</span><span class="sxs-lookup"><span data-stu-id="ece75-423">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="ece75-424">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="ece75-424">RESIGNATION</span></span>    | <span data-ttu-id="ece75-425">Увольнение</span><span class="sxs-lookup"><span data-stu-id="ece75-425">Resignation</span></span>      | <span data-ttu-id="ece75-426">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="ece75-426">Terminate worker</span></span>     |
| <span data-ttu-id="ece75-427">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="ece75-427">TERMINATION</span></span>    | <span data-ttu-id="ece75-428">Завершение</span><span class="sxs-lookup"><span data-stu-id="ece75-428">Termination</span></span>      | <span data-ttu-id="ece75-429">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="ece75-429">Terminate worker</span></span>     |
| <span data-ttu-id="ece75-430">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="ece75-430">RETIREMENT</span></span>     | <span data-ttu-id="ece75-431">Выходное пособие</span><span class="sxs-lookup"><span data-stu-id="ece75-431">Retirement</span></span>       | <span data-ttu-id="ece75-432">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="ece75-432">Terminate worker</span></span>     |
| <span data-ttu-id="ece75-433">ПРОЧЕЕ</span><span class="sxs-lookup"><span data-stu-id="ece75-433">OTHER</span></span>          | <span data-ttu-id="ece75-434">Другие причины</span><span class="sxs-lookup"><span data-stu-id="ece75-434">Other Reasons</span></span>    | <span data-ttu-id="ece75-435">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="ece75-435">Terminate worker</span></span>     |
| <span data-ttu-id="ece75-436">DEATH</span><span class="sxs-lookup"><span data-stu-id="ece75-436">DEATH</span></span>          | <span data-ttu-id="ece75-437">Смерть</span><span class="sxs-lookup"><span data-stu-id="ece75-437">Death</span></span>            | <span data-ttu-id="ece75-438">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="ece75-438">Terminate worker</span></span>     |
| <span data-ttu-id="ece75-439">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="ece75-439">LEAVEOFABSENCE</span></span> | <span data-ttu-id="ece75-440">Отпуск</span><span class="sxs-lookup"><span data-stu-id="ece75-440">Leave of Absence</span></span> | <span data-ttu-id="ece75-441">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="ece75-441">Terminate worker</span></span>     |
| <span data-ttu-id="ece75-442">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="ece75-442">CONTRACTEND</span></span>    | <span data-ttu-id="ece75-443">Завершение контракта</span><span class="sxs-lookup"><span data-stu-id="ece75-443">End of Contract</span></span>  | <span data-ttu-id="ece75-444">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="ece75-444">Terminate worker</span></span>     |
| <span data-ttu-id="ece75-445">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="ece75-445">SALARYCHANGE</span></span>   | <span data-ttu-id="ece75-446">Изменение зарплаты</span><span class="sxs-lookup"><span data-stu-id="ece75-446">Change of Salary</span></span> | <span data-ttu-id="ece75-447">Компенсация</span><span class="sxs-lookup"><span data-stu-id="ece75-447">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="ece75-448">Семейное положение</span><span class="sxs-lookup"><span data-stu-id="ece75-448">Marital status</span></span>

<span data-ttu-id="ece75-449">Значения семейного положения сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="ece75-449">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="ece75-450">В следующей таблице показано, как значения семейного положения сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="ece75-450">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="ece75-451">Talent</span><span class="sxs-lookup"><span data-stu-id="ece75-451">Talent</span></span>                 | <span data-ttu-id="ece75-452">Dayforce</span><span class="sxs-lookup"><span data-stu-id="ece75-452">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="ece75-453">Женат/замужем</span><span class="sxs-lookup"><span data-stu-id="ece75-453">Married</span></span>                | <span data-ttu-id="ece75-454">Женат/замужем</span><span class="sxs-lookup"><span data-stu-id="ece75-454">Married</span></span>              |
| <span data-ttu-id="ece75-455">Один</span><span class="sxs-lookup"><span data-stu-id="ece75-455">Single</span></span>                 | <span data-ttu-id="ece75-456">Один</span><span class="sxs-lookup"><span data-stu-id="ece75-456">Single</span></span>               |
| <span data-ttu-id="ece75-457">Вдовец/вдова</span><span class="sxs-lookup"><span data-stu-id="ece75-457">Widowed</span></span>                | <span data-ttu-id="ece75-458">Вдовец/вдова</span><span class="sxs-lookup"><span data-stu-id="ece75-458">Widowed</span></span>              |
| <span data-ttu-id="ece75-459">Разведен/разведена</span><span class="sxs-lookup"><span data-stu-id="ece75-459">Divorced</span></span>               | <span data-ttu-id="ece75-460">Разведен/разведена</span><span class="sxs-lookup"><span data-stu-id="ece75-460">Divorced</span></span>             |
| <span data-ttu-id="ece75-461">Зарегистрированное партнерство</span><span class="sxs-lookup"><span data-stu-id="ece75-461">Registered Partnership</span></span> | <span data-ttu-id="ece75-462">Партнерство на внутреннем рынке</span><span class="sxs-lookup"><span data-stu-id="ece75-462">Domestic Partnership</span></span> |
| <span data-ttu-id="ece75-463">None</span><span class="sxs-lookup"><span data-stu-id="ece75-463">None</span></span>                   | <span data-ttu-id="ece75-464">None</span><span class="sxs-lookup"><span data-stu-id="ece75-464">None</span></span>                 |
| <span data-ttu-id="ece75-465">Партнерство</span><span class="sxs-lookup"><span data-stu-id="ece75-465">Cohabiting</span></span>             | <span data-ttu-id="ece75-466">Партнерство</span><span class="sxs-lookup"><span data-stu-id="ece75-466">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="ece75-467">Род</span><span class="sxs-lookup"><span data-stu-id="ece75-467">Gender</span></span>

<span data-ttu-id="ece75-468">Значения пола сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="ece75-468">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="ece75-469">В следующей таблице показано, как значения пола сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="ece75-469">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="ece75-470">Talent</span><span class="sxs-lookup"><span data-stu-id="ece75-470">Talent</span></span>       | <span data-ttu-id="ece75-471">Dayforce</span><span class="sxs-lookup"><span data-stu-id="ece75-471">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="ece75-472">Мужской</span><span class="sxs-lookup"><span data-stu-id="ece75-472">Male</span></span>         | <span data-ttu-id="ece75-473">Мужской</span><span class="sxs-lookup"><span data-stu-id="ece75-473">Male</span></span>            |
| <span data-ttu-id="ece75-474">Женский</span><span class="sxs-lookup"><span data-stu-id="ece75-474">Female</span></span>       | <span data-ttu-id="ece75-475">Женский</span><span class="sxs-lookup"><span data-stu-id="ece75-475">Female</span></span>          |
| <span data-ttu-id="ece75-476">Неопределенный</span><span class="sxs-lookup"><span data-stu-id="ece75-476">Non-specific</span></span> | <span data-ttu-id="ece75-477">*Не поддерживается*</span><span class="sxs-lookup"><span data-stu-id="ece75-477">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="ece75-478">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="ece75-478">Earning codes</span></span>

<span data-ttu-id="ece75-479">Коды доходов уникально определяют каждый типа доходов, которые работники получают.</span><span class="sxs-lookup"><span data-stu-id="ece75-479">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="ece75-480">Эти коды покрывают несколько параметров, которые относятся к доходам, таких как правила учета, налоговые законы, требования к отчетности и возможности брутто в большую сторону.</span><span class="sxs-lookup"><span data-stu-id="ece75-480">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="ece75-481">Если используется неподдерживаемая частота, частота **Каждая оплата** используется по умолчанию для расчета.</span><span class="sxs-lookup"><span data-stu-id="ece75-481">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="ece75-482">Поддерживаемые частоты</span><span class="sxs-lookup"><span data-stu-id="ece75-482">Supported frequencies</span></span>

- <span data-ttu-id="ece75-483">Все</span><span class="sxs-lookup"><span data-stu-id="ece75-483">All</span></span>
- <span data-ttu-id="ece75-484">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="ece75-484">EVERYPAY</span></span>
- <span data-ttu-id="ece75-485">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="ece75-485">EACHPAYPERIOD</span></span>
- <span data-ttu-id="ece75-486">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="ece75-486">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="ece75-487">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="ece75-487">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="ece75-488">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-488">1OFMTH</span></span>
- <span data-ttu-id="ece75-489">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-489">LASTOFMTH</span></span>
- <span data-ttu-id="ece75-490">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-490">2OFMTH</span></span>
- <span data-ttu-id="ece75-491">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-491">3OFMTH</span></span>
- <span data-ttu-id="ece75-492">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-492">4OFMTH</span></span>
- <span data-ttu-id="ece75-493">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-493">5OFMTH</span></span>
- <span data-ttu-id="ece75-494">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-494">1N2OFMTH</span></span>
- <span data-ttu-id="ece75-495">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-495">3N4OFMTH</span></span>
- <span data-ttu-id="ece75-496">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-496">1N3OFMTH</span></span>
- <span data-ttu-id="ece75-497">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-497">1N4OFMTH</span></span>
- <span data-ttu-id="ece75-498">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-498">2N3OFMTH</span></span>
- <span data-ttu-id="ece75-499">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-499">2N4OFMTH</span></span>
- <span data-ttu-id="ece75-500">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-500">1N2N3OFMTH</span></span>
- <span data-ttu-id="ece75-501">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-501">1N2N4OFMTH</span></span>
- <span data-ttu-id="ece75-502">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-502">1N3N4OFMTH</span></span>
- <span data-ttu-id="ece75-503">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-503">2N3N4OFMTH</span></span>
- <span data-ttu-id="ece75-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="ece75-505">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="ece75-505">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="ece75-506">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="ece75-506">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="ece75-507">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="ece75-507">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="ece75-508">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="ece75-508">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="ece75-509">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="ece75-509">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="ece75-510">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="ece75-510">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="ece75-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="ece75-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="ece75-512">Адреса</span><span class="sxs-lookup"><span data-stu-id="ece75-512">Addresses</span></span>

<span data-ttu-id="ece75-513">Идентификация кодов конкретной страны или региона, области и района (муниципалитета) требует определенных форматов, которые Dayforce и поставщики в стране или в регионе могут распознать.</span><span class="sxs-lookup"><span data-stu-id="ece75-513">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="ece75-514">Хотя формат городов гибкий, каждый город должен быть связан с областью.</span><span class="sxs-lookup"><span data-stu-id="ece75-514">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="ece75-515">Talent</span><span class="sxs-lookup"><span data-stu-id="ece75-515">Talent</span></span>          | <span data-ttu-id="ece75-516">Dayforce</span><span class="sxs-lookup"><span data-stu-id="ece75-516">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="ece75-517">Страна/регион</span><span class="sxs-lookup"><span data-stu-id="ece75-517">Country/Region</span></span>  | <span data-ttu-id="ece75-518">Код страны</span><span class="sxs-lookup"><span data-stu-id="ece75-518">Country Code</span></span>          |
| <span data-ttu-id="ece75-519">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="ece75-519">Zip/Postal Code</span></span> | <span data-ttu-id="ece75-520">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="ece75-520">Postal Code</span></span>           |
| <span data-ttu-id="ece75-521">Область, край</span><span class="sxs-lookup"><span data-stu-id="ece75-521">State</span></span>           | <span data-ttu-id="ece75-522">Код региона</span><span class="sxs-lookup"><span data-stu-id="ece75-522">State Code</span></span>            |
| <span data-ttu-id="ece75-523">Город</span><span class="sxs-lookup"><span data-stu-id="ece75-523">City</span></span>            | <span data-ttu-id="ece75-524">Город</span><span class="sxs-lookup"><span data-stu-id="ece75-524">City</span></span>                  |
| <span data-ttu-id="ece75-525">Округ</span><span class="sxs-lookup"><span data-stu-id="ece75-525">County</span></span>          | <span data-ttu-id="ece75-526">Район (муниципалитет)</span><span class="sxs-lookup"><span data-stu-id="ece75-526">County (Municipality)</span></span> |
| <span data-ttu-id="ece75-527">Улица</span><span class="sxs-lookup"><span data-stu-id="ece75-527">Street</span></span>          | <span data-ttu-id="ece75-528">Строка адреса 1</span><span class="sxs-lookup"><span data-stu-id="ece75-528">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="ece75-529">Налоговые регионы</span><span class="sxs-lookup"><span data-stu-id="ece75-529">Tax regions</span></span>

<span data-ttu-id="ece75-530">Налоговые регионы используются для определения налогов, которые следует применять при создании заработной платы.</span><span class="sxs-lookup"><span data-stu-id="ece75-530">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="ece75-531">Налоговые регионы сопоставляются с Dayforce как адреса местоположения.</span><span class="sxs-lookup"><span data-stu-id="ece75-531">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="ece75-532">Налоговый регион по умолчанию должен быть связан с активной должностью работника.</span><span class="sxs-lookup"><span data-stu-id="ece75-532">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="ece75-533">Налоговый регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-533">Tax region (required)</span></span>
- <span data-ttu-id="ece75-534">Страна/Регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-534">Country/Region (required)</span></span>
- <span data-ttu-id="ece75-535">Регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-535">State (required)</span></span>
- <span data-ttu-id="ece75-536">Округ</span><span class="sxs-lookup"><span data-stu-id="ece75-536">County</span></span> 
- <span data-ttu-id="ece75-537">Город (обязательно)</span><span class="sxs-lookup"><span data-stu-id="ece75-537">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="ece75-538">Настройка данных для расчета заработной платы в Мексике</span><span class="sxs-lookup"><span data-stu-id="ece75-538">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="ece75-539">Если вы создаете оплату для сотрудников в Мексике, необходимо настроить следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="ece75-539">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="ece75-540">Обязательно указывать подразделения для должностей.</span><span class="sxs-lookup"><span data-stu-id="ece75-540">Departments are required on positions.</span></span>
- <span data-ttu-id="ece75-541">Центры затрат должен быть заданы как финансовые аналитики и должны быть первым элементом в строке финансовой аналитики по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ece75-541">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="ece75-542">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="ece75-542">Job types</span></span>

<span data-ttu-id="ece75-543">Типы должностей используются для группирования похожих должностных обязанностей в категории.</span><span class="sxs-lookup"><span data-stu-id="ece75-543">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="ece75-544">Типы должностей обязательны для обработки зарплаты в Мексике.</span><span class="sxs-lookup"><span data-stu-id="ece75-544">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="ece75-545">Примеры типов должностей включают полный рабочий день и неполный рабочий день, или зарплата и почасовая оплата.</span><span class="sxs-lookup"><span data-stu-id="ece75-545">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="ece75-546">Типы должностей сопоставляются с Dayforce как типы зарплаты, которые указывают тип оплаты сотрудника: почасовая или оклад.</span><span class="sxs-lookup"><span data-stu-id="ece75-546">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="ece75-547">Требуются следующие типы должностей и описаний.</span><span class="sxs-lookup"><span data-stu-id="ece75-547">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="ece75-548">Тип задания</span><span class="sxs-lookup"><span data-stu-id="ece75-548">Job type</span></span>   | <span data-ttu-id="ece75-549">описание</span><span class="sxs-lookup"><span data-stu-id="ece75-549">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="ece75-550">Почасовая</span><span class="sxs-lookup"><span data-stu-id="ece75-550">Hourly</span></span>     | <span data-ttu-id="ece75-551">MX Почасовая</span><span class="sxs-lookup"><span data-stu-id="ece75-551">MX Hourly</span></span>   |
| <span data-ttu-id="ece75-552">Оклад</span><span class="sxs-lookup"><span data-stu-id="ece75-552">Salaried</span></span>   | <span data-ttu-id="ece75-553">MX Оклад</span><span class="sxs-lookup"><span data-stu-id="ece75-553">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="ece75-554">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="ece75-554">Position types</span></span> 

<span data-ttu-id="ece75-555">С помощью типов должностей описывается, является ли должность занятостью на полный рабочий день, на неполный рабочий день или какой-либо другой.</span><span class="sxs-lookup"><span data-stu-id="ece75-555">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="ece75-556">Типы должностей сопоставляются с Dayforce как классы зарплаты, которые указывают тип оплаты сотрудника: полная занятость или частичная занятость.</span><span class="sxs-lookup"><span data-stu-id="ece75-556">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="ece75-557">Требуются следующие типы должностей и описаний.</span><span class="sxs-lookup"><span data-stu-id="ece75-557">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="ece75-558">Тип должности</span><span class="sxs-lookup"><span data-stu-id="ece75-558">Position type</span></span>   | <span data-ttu-id="ece75-559">описание</span><span class="sxs-lookup"><span data-stu-id="ece75-559">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="ece75-560">Полная занятость</span><span class="sxs-lookup"><span data-stu-id="ece75-560">Full-time</span></span>       | <span data-ttu-id="ece75-561">Работник с полной занятостью</span><span class="sxs-lookup"><span data-stu-id="ece75-561">Full time employee</span></span> |
| <span data-ttu-id="ece75-562">Частичная занятость</span><span class="sxs-lookup"><span data-stu-id="ece75-562">Part-time</span></span>       | <span data-ttu-id="ece75-563">Работник с частичной занятостью</span><span class="sxs-lookup"><span data-stu-id="ece75-563">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="ece75-564">Коды оснований</span><span class="sxs-lookup"><span data-stu-id="ece75-564">Reason codes</span></span>

<span data-ttu-id="ece75-565">Коды оснований содержат сведения о статусе сотрудника.</span><span class="sxs-lookup"><span data-stu-id="ece75-565">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="ece75-566">Коды оснований сопоставляются с Dayforce как причины статуса, которые определяют причину изменения статус должности или найма сотрудника.</span><span class="sxs-lookup"><span data-stu-id="ece75-566">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="ece75-567">Требуются следующие коды причин и описания.</span><span class="sxs-lookup"><span data-stu-id="ece75-567">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="ece75-568">Код основания</span><span class="sxs-lookup"><span data-stu-id="ece75-568">Reason code</span></span>            | <span data-ttu-id="ece75-569">описание</span><span class="sxs-lookup"><span data-stu-id="ece75-569">Description</span></span>                    | <span data-ttu-id="ece75-570">Применимые сценарии</span><span class="sxs-lookup"><span data-stu-id="ece75-570">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="ece75-571">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="ece75-571">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="ece75-572">Увольнение до первой заработной платы</span><span class="sxs-lookup"><span data-stu-id="ece75-572">Departure before first payroll</span></span> | <span data-ttu-id="ece75-573">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="ece75-573">Terminate worker</span></span>     |
| <span data-ttu-id="ece75-574">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="ece75-574">RESIGNATION</span></span>            | <span data-ttu-id="ece75-575">Увольнение</span><span class="sxs-lookup"><span data-stu-id="ece75-575">Resignation</span></span>                    | <span data-ttu-id="ece75-576">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="ece75-576">Terminate worker</span></span>     |
| <span data-ttu-id="ece75-577">PENSION</span><span class="sxs-lookup"><span data-stu-id="ece75-577">PENSION</span></span>                | <span data-ttu-id="ece75-578">Пенсия</span><span class="sxs-lookup"><span data-stu-id="ece75-578">Pension</span></span>                        | <span data-ttu-id="ece75-579">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="ece75-579">Terminate worker</span></span>     |
| <span data-ttu-id="ece75-580">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="ece75-580">TERMINATION</span></span>            | <span data-ttu-id="ece75-581">Завершение</span><span class="sxs-lookup"><span data-stu-id="ece75-581">Termination</span></span>                    | <span data-ttu-id="ece75-582">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="ece75-582">Terminate worker</span></span>     |
| <span data-ttu-id="ece75-583">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="ece75-583">RETIREMENT</span></span>             | <span data-ttu-id="ece75-584">Выходное пособие</span><span class="sxs-lookup"><span data-stu-id="ece75-584">Retirement</span></span>                     | <span data-ttu-id="ece75-585">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="ece75-585">Terminate worker</span></span>     |
| <span data-ttu-id="ece75-586">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="ece75-586">ABSENTEE</span></span>               | <span data-ttu-id="ece75-587">Прогульщик</span><span class="sxs-lookup"><span data-stu-id="ece75-587">Absentee</span></span>                       | <span data-ttu-id="ece75-588">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="ece75-588">Terminate worker</span></span>     |
| <span data-ttu-id="ece75-589">ПРОЧЕЕ</span><span class="sxs-lookup"><span data-stu-id="ece75-589">OTHER</span></span>                  | <span data-ttu-id="ece75-590">Другие причины</span><span class="sxs-lookup"><span data-stu-id="ece75-590">Other Reasons</span></span>                  | <span data-ttu-id="ece75-591">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="ece75-591">Terminate worker</span></span>     |
| <span data-ttu-id="ece75-592">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="ece75-592">CLOSURE</span></span>                | <span data-ttu-id="ece75-593">Закрытие компании</span><span class="sxs-lookup"><span data-stu-id="ece75-593">Business Closure</span></span>               | <span data-ttu-id="ece75-594">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="ece75-594">Terminate worker</span></span>     |
| <span data-ttu-id="ece75-595">DEATH</span><span class="sxs-lookup"><span data-stu-id="ece75-595">DEATH</span></span>                  | <span data-ttu-id="ece75-596">Смерть</span><span class="sxs-lookup"><span data-stu-id="ece75-596">Death</span></span>                          | <span data-ttu-id="ece75-597">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="ece75-597">Terminate worker</span></span>     |
| <span data-ttu-id="ece75-598">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="ece75-598">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="ece75-599">Отпуск</span><span class="sxs-lookup"><span data-stu-id="ece75-599">Leave of Absence</span></span>               | <span data-ttu-id="ece75-600">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="ece75-600">Terminate worker</span></span>     |
| <span data-ttu-id="ece75-601">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="ece75-601">CONTRACTEND</span></span>            | <span data-ttu-id="ece75-602">Завершение контракта</span><span class="sxs-lookup"><span data-stu-id="ece75-602">End of Contract</span></span>                | <span data-ttu-id="ece75-603">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="ece75-603">Terminate worker</span></span>     |
| <span data-ttu-id="ece75-604">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="ece75-604">SALARYCHANGE</span></span>           | <span data-ttu-id="ece75-605">Изменение зарплаты</span><span class="sxs-lookup"><span data-stu-id="ece75-605">Change of Salary</span></span>               | <span data-ttu-id="ece75-606">Компенсация</span><span class="sxs-lookup"><span data-stu-id="ece75-606">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="ece75-607">Условия найма</span><span class="sxs-lookup"><span data-stu-id="ece75-607">Terms of employment</span></span>

<span data-ttu-id="ece75-608">Условия найма используются для создания категорий условий трудоустройства.</span><span class="sxs-lookup"><span data-stu-id="ece75-608">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="ece75-609">Условия сопоставляются с Dayforce как значения индикатора трудоустройства.</span><span class="sxs-lookup"><span data-stu-id="ece75-609">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="ece75-610">Необходимы следующие условия найма и описания.</span><span class="sxs-lookup"><span data-stu-id="ece75-610">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="ece75-611">Условия найма</span><span class="sxs-lookup"><span data-stu-id="ece75-611">Terms of employment</span></span>   | <span data-ttu-id="ece75-612">описание</span><span class="sxs-lookup"><span data-stu-id="ece75-612">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="ece75-613">Периодически</span><span class="sxs-lookup"><span data-stu-id="ece75-613">Regular</span></span>               | <span data-ttu-id="ece75-614">Периодически</span><span class="sxs-lookup"><span data-stu-id="ece75-614">Regular</span></span>     |
| <span data-ttu-id="ece75-615">Напрямую</span><span class="sxs-lookup"><span data-stu-id="ece75-615">Direct</span></span>                | <span data-ttu-id="ece75-616">Напрямую</span><span class="sxs-lookup"><span data-stu-id="ece75-616">Direct</span></span>      |
| <span data-ttu-id="ece75-617">Практика</span><span class="sxs-lookup"><span data-stu-id="ece75-617">Internship</span></span>            | <span data-ttu-id="ece75-618">Практика</span><span class="sxs-lookup"><span data-stu-id="ece75-618">Internship</span></span>  |
| <span data-ttu-id="ece75-619">Постоянный</span><span class="sxs-lookup"><span data-stu-id="ece75-619">Permanent</span></span>             | <span data-ttu-id="ece75-620">Постоянный</span><span class="sxs-lookup"><span data-stu-id="ece75-620">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="ece75-621">Семейное положение</span><span class="sxs-lookup"><span data-stu-id="ece75-621">Marital status</span></span>

<span data-ttu-id="ece75-622">Значения семейного положения сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="ece75-622">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="ece75-623">В следующей таблице показано, как значения семейного положения сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="ece75-623">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="ece75-624">Talent</span><span class="sxs-lookup"><span data-stu-id="ece75-624">Talent</span></span>                 | <span data-ttu-id="ece75-625">Dayforce</span><span class="sxs-lookup"><span data-stu-id="ece75-625">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="ece75-626">Женат/замужем</span><span class="sxs-lookup"><span data-stu-id="ece75-626">Married</span></span>                | <span data-ttu-id="ece75-627">Женат/замужем</span><span class="sxs-lookup"><span data-stu-id="ece75-627">Married</span></span>                   |
| <span data-ttu-id="ece75-628">Один</span><span class="sxs-lookup"><span data-stu-id="ece75-628">Single</span></span>                 | <span data-ttu-id="ece75-629">Один</span><span class="sxs-lookup"><span data-stu-id="ece75-629">Single</span></span>                    |
| <span data-ttu-id="ece75-630">Вдовец/вдова</span><span class="sxs-lookup"><span data-stu-id="ece75-630">Widowed</span></span>                | <span data-ttu-id="ece75-631">Вдовец/вдова</span><span class="sxs-lookup"><span data-stu-id="ece75-631">Widowed</span></span>                   |
| <span data-ttu-id="ece75-632">Разведен/разведена</span><span class="sxs-lookup"><span data-stu-id="ece75-632">Divorced</span></span>               | <span data-ttu-id="ece75-633">Разведен/разведена</span><span class="sxs-lookup"><span data-stu-id="ece75-633">Divorced</span></span>                  |
| <span data-ttu-id="ece75-634">Зарегистрированное партнерство</span><span class="sxs-lookup"><span data-stu-id="ece75-634">Registered Partnership</span></span> | <span data-ttu-id="ece75-635">Партнерство на внутреннем рынке</span><span class="sxs-lookup"><span data-stu-id="ece75-635">Domestic Partnership</span></span>      |
| <span data-ttu-id="ece75-636">None</span><span class="sxs-lookup"><span data-stu-id="ece75-636">None</span></span>                   | <span data-ttu-id="ece75-637">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="ece75-637">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="ece75-638">Партнерство</span><span class="sxs-lookup"><span data-stu-id="ece75-638">Cohabiting</span></span>             | <span data-ttu-id="ece75-639">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="ece75-639">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="ece75-640">Род</span><span class="sxs-lookup"><span data-stu-id="ece75-640">Gender</span></span>

<span data-ttu-id="ece75-641">Значения пола сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="ece75-641">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="ece75-642">В следующей таблице показано, как значения пола сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="ece75-642">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="ece75-643">Talent</span><span class="sxs-lookup"><span data-stu-id="ece75-643">Talent</span></span>       | <span data-ttu-id="ece75-644">Dayforce</span><span class="sxs-lookup"><span data-stu-id="ece75-644">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="ece75-645">Мужской</span><span class="sxs-lookup"><span data-stu-id="ece75-645">Male</span></span>         | <span data-ttu-id="ece75-646">Мужской</span><span class="sxs-lookup"><span data-stu-id="ece75-646">Male</span></span>                      |
| <span data-ttu-id="ece75-647">Женский</span><span class="sxs-lookup"><span data-stu-id="ece75-647">Female</span></span>       | <span data-ttu-id="ece75-648">Женский</span><span class="sxs-lookup"><span data-stu-id="ece75-648">Female</span></span>                    |
| <span data-ttu-id="ece75-649">Неопределенный</span><span class="sxs-lookup"><span data-stu-id="ece75-649">Non-specific</span></span> | <span data-ttu-id="ece75-650">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="ece75-650">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="ece75-651">Способ платежа</span><span class="sxs-lookup"><span data-stu-id="ece75-651">Payment method</span></span>

<span data-ttu-id="ece75-652">Методы оплаты предоставляют сотруднику и компании способ описания способа оплаты сотрудников.</span><span class="sxs-lookup"><span data-stu-id="ece75-652">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="ece75-653">Способы оплаты сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="ece75-653">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="ece75-654">В следующей таблице показано, как способы оплаты сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="ece75-654">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="ece75-655">Talent</span><span class="sxs-lookup"><span data-stu-id="ece75-655">Talent</span></span>             | <span data-ttu-id="ece75-656">Dayforce</span><span class="sxs-lookup"><span data-stu-id="ece75-656">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="ece75-657">Наличный расчет</span><span class="sxs-lookup"><span data-stu-id="ece75-657">Cash</span></span>               | <span data-ttu-id="ece75-658">Наличный расчет</span><span class="sxs-lookup"><span data-stu-id="ece75-658">Cash</span></span>                      |
| <span data-ttu-id="ece75-659">Электронный платеж</span><span class="sxs-lookup"><span data-stu-id="ece75-659">Electronic Payment</span></span> | <span data-ttu-id="ece75-660">Перевод</span><span class="sxs-lookup"><span data-stu-id="ece75-660">Transfer</span></span>                  |
| <span data-ttu-id="ece75-661">Проверка</span><span class="sxs-lookup"><span data-stu-id="ece75-661">Check</span></span>              | <span data-ttu-id="ece75-662">Чек</span><span class="sxs-lookup"><span data-stu-id="ece75-662">Cheque</span></span>                    |
| <span data-ttu-id="ece75-663">Банковская тратта</span><span class="sxs-lookup"><span data-stu-id="ece75-663">Bank Draft</span></span>         | <span data-ttu-id="ece75-664">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="ece75-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="ece75-665">Прочие</span><span class="sxs-lookup"><span data-stu-id="ece75-665">Other</span></span>              | <span data-ttu-id="ece75-666">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="ece75-666">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="ece75-667">Тип банковского счета</span><span class="sxs-lookup"><span data-stu-id="ece75-667">Bank account type</span></span>

<span data-ttu-id="ece75-668">Типы банковских счетов используются для электронных платежей сотрудникам.</span><span class="sxs-lookup"><span data-stu-id="ece75-668">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="ece75-669">Типы банковских счетов сопоставляются с Dayforce как сведения о счетах безналичных расчетов.</span><span class="sxs-lookup"><span data-stu-id="ece75-669">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="ece75-670">Типы банковских счетов переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="ece75-670">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="ece75-671">Talent</span><span class="sxs-lookup"><span data-stu-id="ece75-671">Talent</span></span>            | <span data-ttu-id="ece75-672">Dayforce</span><span class="sxs-lookup"><span data-stu-id="ece75-672">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="ece75-673">Чековый счет</span><span class="sxs-lookup"><span data-stu-id="ece75-673">Checking Account</span></span>  | <span data-ttu-id="ece75-674">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="ece75-674">CheckingAccount</span></span>           |
| <span data-ttu-id="ece75-675">Счет зарплаты</span><span class="sxs-lookup"><span data-stu-id="ece75-675">Payroll Account</span></span>   | <span data-ttu-id="ece75-676">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="ece75-676">PayrollAccount</span></span>            |
| <span data-ttu-id="ece75-677">Сберегательный счет</span><span class="sxs-lookup"><span data-stu-id="ece75-677">Savings Account</span></span>   | <span data-ttu-id="ece75-678">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="ece75-678">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="ece75-679">Счет BankGirot</span><span class="sxs-lookup"><span data-stu-id="ece75-679">BankGirot account</span></span> | <span data-ttu-id="ece75-680">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="ece75-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="ece75-681">Счет PlusGirot</span><span class="sxs-lookup"><span data-stu-id="ece75-681">PlusGirot account</span></span> | <span data-ttu-id="ece75-682">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="ece75-682">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="ece75-683">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="ece75-683">Earning codes</span></span>

<span data-ttu-id="ece75-684">Коды доходов уникально определяют каждый типа доходов, которые работники получают.</span><span class="sxs-lookup"><span data-stu-id="ece75-684">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="ece75-685">Эти коды покрывают несколько параметров, которые относятся к доходам, таких как правила учета, налоговые законы, требования к отчетности и возможности брутто в большую сторону.</span><span class="sxs-lookup"><span data-stu-id="ece75-685">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="ece75-686">Если используется неподдерживаемая частота, частота **Каждая оплата** используется по умолчанию для расчета.</span><span class="sxs-lookup"><span data-stu-id="ece75-686">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="ece75-687">Поддерживаемые частоты</span><span class="sxs-lookup"><span data-stu-id="ece75-687">Supported frequencies</span></span>

- <span data-ttu-id="ece75-688">Все</span><span class="sxs-lookup"><span data-stu-id="ece75-688">All</span></span>
- <span data-ttu-id="ece75-689">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="ece75-689">EVERYPAY</span></span>
- <span data-ttu-id="ece75-690">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="ece75-690">EACHPAYPERIOD</span></span>
- <span data-ttu-id="ece75-691">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="ece75-691">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="ece75-692">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="ece75-692">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="ece75-693">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-693">1OFMTH</span></span>
- <span data-ttu-id="ece75-694">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-694">LASTOFMTH</span></span>
- <span data-ttu-id="ece75-695">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-695">2OFMTH</span></span>
- <span data-ttu-id="ece75-696">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-696">3OFMTH</span></span>
- <span data-ttu-id="ece75-697">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-697">4OFMTH</span></span>
- <span data-ttu-id="ece75-698">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-698">5OFMTH</span></span>
- <span data-ttu-id="ece75-699">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-699">1N2OFMTH</span></span>
- <span data-ttu-id="ece75-700">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-700">3N4OFMTH</span></span>
- <span data-ttu-id="ece75-701">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-701">1N3OFMTH</span></span>
- <span data-ttu-id="ece75-702">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-702">1N4OFMTH</span></span>
- <span data-ttu-id="ece75-703">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-703">2N3OFMTH</span></span>
- <span data-ttu-id="ece75-704">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-704">2N4OFMTH</span></span>
- <span data-ttu-id="ece75-705">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-705">1N2N3OFMTH</span></span>
- <span data-ttu-id="ece75-706">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-706">1N2N4OFMTH</span></span>
- <span data-ttu-id="ece75-707">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-707">1N3N4OFMTH</span></span>
- <span data-ttu-id="ece75-708">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-708">2N3N4OFMTH</span></span>
- <span data-ttu-id="ece75-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="ece75-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="ece75-710">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="ece75-710">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="ece75-711">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="ece75-711">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="ece75-712">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="ece75-712">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="ece75-713">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="ece75-713">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="ece75-714">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="ece75-714">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="ece75-715">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="ece75-715">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="ece75-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="ece75-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="ece75-717">Адреса</span><span class="sxs-lookup"><span data-stu-id="ece75-717">Addresses</span></span>

<span data-ttu-id="ece75-718">Идентификация кодов конкретной страны или региона, области и района (муниципалитета) требует определенных форматов, которые Dayforce и поставщики в стране или в регионе могут распознать.</span><span class="sxs-lookup"><span data-stu-id="ece75-718">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="ece75-719">Хотя формат городов гибкий, каждый город должен быть связан с областью.</span><span class="sxs-lookup"><span data-stu-id="ece75-719">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="ece75-720">Talent</span><span class="sxs-lookup"><span data-stu-id="ece75-720">Talent</span></span>              | <span data-ttu-id="ece75-721">Dayforce</span><span class="sxs-lookup"><span data-stu-id="ece75-721">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="ece75-722">Страна/регион</span><span class="sxs-lookup"><span data-stu-id="ece75-722">Country/Region</span></span>      | <span data-ttu-id="ece75-723">Код страны</span><span class="sxs-lookup"><span data-stu-id="ece75-723">Country Code</span></span>          |
| <span data-ttu-id="ece75-724">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="ece75-724">Zip/Postal Code</span></span>     | <span data-ttu-id="ece75-725">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="ece75-725">Postal Code</span></span>           |
| <span data-ttu-id="ece75-726">Область, край</span><span class="sxs-lookup"><span data-stu-id="ece75-726">State</span></span>               | <span data-ttu-id="ece75-727">Код региона</span><span class="sxs-lookup"><span data-stu-id="ece75-727">State Code</span></span>            |
| <span data-ttu-id="ece75-728">Город</span><span class="sxs-lookup"><span data-stu-id="ece75-728">City</span></span>                | <span data-ttu-id="ece75-729">Город</span><span class="sxs-lookup"><span data-stu-id="ece75-729">City</span></span>                  |
| <span data-ttu-id="ece75-730">Округ</span><span class="sxs-lookup"><span data-stu-id="ece75-730">County</span></span>              | <span data-ttu-id="ece75-731">Район (муниципалитет)</span><span class="sxs-lookup"><span data-stu-id="ece75-731">County (Municipality)</span></span> |
| <span data-ttu-id="ece75-732">Улица</span><span class="sxs-lookup"><span data-stu-id="ece75-732">Street</span></span>              | <span data-ttu-id="ece75-733">Строка адреса 1</span><span class="sxs-lookup"><span data-stu-id="ece75-733">Address Line 1</span></span>        |
| <span data-ttu-id="ece75-734">Номер дома</span><span class="sxs-lookup"><span data-stu-id="ece75-734">Street Number</span></span>       | <span data-ttu-id="ece75-735">Строка адреса 2</span><span class="sxs-lookup"><span data-stu-id="ece75-735">Address Line 2</span></span>        |
| <span data-ttu-id="ece75-736">Дополнение здания</span><span class="sxs-lookup"><span data-stu-id="ece75-736">Building Complement</span></span> | <span data-ttu-id="ece75-737">Строка адреса 5</span><span class="sxs-lookup"><span data-stu-id="ece75-737">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="ece75-738">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="ece75-738">Passport number</span></span>

<span data-ttu-id="ece75-739">Сотрудники могут объявить данные паспорта.</span><span class="sxs-lookup"><span data-stu-id="ece75-739">Employees can declare passport information.</span></span> <span data-ttu-id="ece75-740">Эта информация имеет тип идентификации **Паспорт** и интегрируется в Dayforce как часть сведений о сотруднике, специфических для Мексики.</span><span class="sxs-lookup"><span data-stu-id="ece75-740">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="ece75-741">Тип идентификации = "Паспорт"</span><span class="sxs-lookup"><span data-stu-id="ece75-741">Identification Type = "Passport"</span></span>
- <span data-ttu-id="ece75-742">Дата выпуска</span><span class="sxs-lookup"><span data-stu-id="ece75-742">Issued Date</span></span>
- <span data-ttu-id="ece75-743">Дата окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="ece75-743">Expiration Date</span></span>

<span data-ttu-id="ece75-744">Сотрудники могут объявить несколько идентификационных номеров для типа идентификатора **Паспорт**.</span><span class="sxs-lookup"><span data-stu-id="ece75-744">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="ece75-745">Тем не менее только запись текущего активного паспорта интегрируется в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="ece75-745">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="ece75-746">Если срок действия всех записей паспорта истек, в Dayforce интегрируется тот, который был выдан последним.</span><span class="sxs-lookup"><span data-stu-id="ece75-746">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
