---
title: Настройка интеграции с Dayforce
description: Интеграция между Microsoft Dynamics 365 Human Resources и Ceridian Dayforce зависит от ряда действий настройки, описанных в этой статье. Необходимо настроить интеграцию в Human Resources и Dayforce перед обработкой периода оплаты.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 044a2d2f632b2c98ce94b6d61c2582a861640b68
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113992"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="b9634-104">Настройка интеграции с Dayforce</span><span class="sxs-lookup"><span data-stu-id="b9634-104">Configure integration with Dayforce</span></span>

<span data-ttu-id="b9634-105">Интеграция между Microsoft Dynamics 365 Human Resources и Ceridian Dayforce зависит от ряда действий настройки, описанных в этой статье.</span><span class="sxs-lookup"><span data-stu-id="b9634-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="b9634-106">Необходимо настроить интеграцию в Human Resources и Dayforce перед обработкой периода оплаты.</span><span class="sxs-lookup"><span data-stu-id="b9634-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="b9634-107">При использовании службы, например Dayforce, для выполнения оплаты, необходимо включить интеграцию в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b9634-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="b9634-108">Интеграция требует определенных данных из Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b9634-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="b9634-109">Таким образом необходимо убедиться, что данные, отображаемые в Dayforce, настроены в Human Resources таким образом, чтобы поддерживать интеграцию.</span><span class="sxs-lookup"><span data-stu-id="b9634-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="b9634-110">Интеграция использует следующие широкие категории данных:</span><span class="sxs-lookup"><span data-stu-id="b9634-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="b9634-111">Данные управления персоналом</span><span class="sxs-lookup"><span data-stu-id="b9634-111">Human resources data</span></span>
- <span data-ttu-id="b9634-112">Данные о компенсациях</span><span class="sxs-lookup"><span data-stu-id="b9634-112">Compensation data</span></span>
- <span data-ttu-id="b9634-113">Данные о заработной плате, например циклы оплаты, периоды оплаты и коды начисления зарплаты</span><span class="sxs-lookup"><span data-stu-id="b9634-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="b9634-114">Данные о работнике</span><span class="sxs-lookup"><span data-stu-id="b9634-114">Worker data</span></span>

<span data-ttu-id="b9634-115">В этой статье описываются шаги, которые необходимо выполнить, чтобы включить интеграцию.</span><span class="sxs-lookup"><span data-stu-id="b9634-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="b9634-116">Здесь также объясняются типы данных и сведения о конфигурации, которые необходимы для интеграции.</span><span class="sxs-lookup"><span data-stu-id="b9634-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="b9634-117">Включение интеграции</span><span class="sxs-lookup"><span data-stu-id="b9634-117">Enable the integration</span></span>

<span data-ttu-id="b9634-118">В Human Resources необходимо включить интеграцию и ввести информацию о конфигурации для подключения к Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b9634-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="b9634-119">Если требуется, чтобы проводки ГК, которые производятся, импортировались в Microsoft Dynamics 365 Finance, также необходимо установить учетную запись хранилища Microsoft Azure и ввести строку подключения хранилища Azure в Finance.</span><span class="sxs-lookup"><span data-stu-id="b9634-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="b9634-120">Чтобы включить интеграцию в Human Resources, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b9634-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="b9634-121">На странице **Администрирование системы** выберите **Конфигурация интеграции**.</span><span class="sxs-lookup"><span data-stu-id="b9634-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="b9634-122">Введите безопасную конечную точку FTP и путь к безопасной папке FTP.</span><span class="sxs-lookup"><span data-stu-id="b9634-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="b9634-123">Введите имя пользователя и пароль пользователя, который будет иметь доступ к безопасной конечной точке и пути к папке FTP.</span><span class="sxs-lookup"><span data-stu-id="b9634-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="b9634-124">Проверьте подключение, как требуется, а также установите для параметра **Включить интеграцию зарплаты** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="b9634-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="b9634-125">При включении интеграции создаются пакет экспорта данных и файлы, и задается значение частоты.</span><span class="sxs-lookup"><span data-stu-id="b9634-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="b9634-126">Можно изменить эту частоту, как требуется.</span><span class="sxs-lookup"><span data-stu-id="b9634-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="b9634-127">Дополнительные сведения об учетных записях хранилища Azure и строке подключения хранилища Azure см. в следующих статьях Azure:</span><span class="sxs-lookup"><span data-stu-id="b9634-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="b9634-128">Об учетных записях хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="b9634-128">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="b9634-129">Настройка строки подключения хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="b9634-129">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="b9634-130">Технические сведения о включении интеграции зарплаты</span><span class="sxs-lookup"><span data-stu-id="b9634-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="b9634-131">Включение интеграции зарплаты имеет два основных эффекта:</span><span class="sxs-lookup"><span data-stu-id="b9634-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="b9634-132">Будет создан проект экспорта данных с именем "Экспорт интеграции зарплаты".</span><span class="sxs-lookup"><span data-stu-id="b9634-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="b9634-133">Этот проект содержит сущности и поля, необходимые для интеграции зарплаты.</span><span class="sxs-lookup"><span data-stu-id="b9634-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="b9634-134">Чтобы проверить этот проект, перейдите в раздел **Администрирование системы**, выберите плитку **Управление данными**, затем откройте проект данных из списка проектов.</span><span class="sxs-lookup"><span data-stu-id="b9634-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="b9634-135">Это пакетное задание выполняет проект экспорта данных, шифрует получившийся пакет данных и передает файл пакета данных на конечную точку SFTP, настроенную на экране **Конфигурация интеграции**.</span><span class="sxs-lookup"><span data-stu-id="b9634-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="b9634-136">Пакет данных, переданный в конечную точку SFTP, шифруется с помощью уникального для пакета ключа.</span><span class="sxs-lookup"><span data-stu-id="b9634-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="b9634-137">Ключ находится в хранилище ключей Azure Key Vault, доступном только для по Ceridian.</span><span class="sxs-lookup"><span data-stu-id="b9634-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="b9634-138">Невозможно расшифровать и проверить содержимое пакета данных.</span><span class="sxs-lookup"><span data-stu-id="b9634-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="b9634-139">Если необходимо изучить содержимое пакета данных, необходимо экспортировать проект данных "Экспорт интеграции зарплаты" вручную, загрузить его и затем открыть.</span><span class="sxs-lookup"><span data-stu-id="b9634-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="b9634-140">При экспорте вручную шифрование или передача пакетов не применяются.</span><span class="sxs-lookup"><span data-stu-id="b9634-140">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="b9634-141">Настройка данных</span><span class="sxs-lookup"><span data-stu-id="b9634-141">Configure your data</span></span> 

<span data-ttu-id="b9634-142">Для обработки зарплаты необходимо настроить данные управления персоналом в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b9634-142">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="b9634-143">Необходимо настроить организационные данные, такие как задания и должности, вместе со сведениями о льготах и компенсациях.</span><span class="sxs-lookup"><span data-stu-id="b9634-143">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="b9634-144">Эта информация содержит сведения о занятости, оплате и вычетах, которые необходимы для формирования заработной платы сотрудника.</span><span class="sxs-lookup"><span data-stu-id="b9634-144">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="b9634-145">Данные управления персоналом</span><span class="sxs-lookup"><span data-stu-id="b9634-145">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="b9634-146">Льготы</span><span class="sxs-lookup"><span data-stu-id="b9634-146">Benefits</span></span> 

<span data-ttu-id="b9634-147">Человеческие ресурсы обеспечивают инструменты для настройки и поддержки льгот, вычетов и планов компенсации работникам, которые организация предлагает или обрабатывает для своих работников.</span><span class="sxs-lookup"><span data-stu-id="b9634-147">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="b9634-148">При создании льгот имейте в виду следующие данные и конфигурации, которые используются в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b9634-148">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="b9634-149">Планы льгот</span><span class="sxs-lookup"><span data-stu-id="b9634-149">Benefit plans</span></span>

- <span data-ttu-id="b9634-150">План (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-150">Plan (required)</span></span>
- <span data-ttu-id="b9634-151">Тип (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-151">Type (required)</span></span>
- <span data-ttu-id="b9634-152">Влияние на зарплату (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-152">Payroll impact (required)</span></span>
- <span data-ttu-id="b9634-153">Погасить задолженность</span><span class="sxs-lookup"><span data-stu-id="b9634-153">Recover arrears</span></span>
- <span data-ttu-id="b9634-154">Метод вычета</span><span class="sxs-lookup"><span data-stu-id="b9634-154">Deduction method</span></span>
- <span data-ttu-id="b9634-155">Приоритет вычета</span><span class="sxs-lookup"><span data-stu-id="b9634-155">Deduction priority</span></span>
- <span data-ttu-id="b9634-156">Период лимита</span><span class="sxs-lookup"><span data-stu-id="b9634-156">Limit period</span></span>
- <span data-ttu-id="b9634-157">Сумма лимита</span><span class="sxs-lookup"><span data-stu-id="b9634-157">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="b9634-158">Льготы</span><span class="sxs-lookup"><span data-stu-id="b9634-158">Benefits</span></span>

- <span data-ttu-id="b9634-159">План (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-159">Plan (required)</span></span>
- <span data-ttu-id="b9634-160">Тип (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-160">Type (required)</span></span>
- <span data-ttu-id="b9634-161">Параметр (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-161">Option (required)</span></span>
- <span data-ttu-id="b9634-162">Код льготы (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-162">Benefit ID (required)</span></span>
- <span data-ttu-id="b9634-163">Частота</span><span class="sxs-lookup"><span data-stu-id="b9634-163">Frequency</span></span>
- <span data-ttu-id="b9634-164">База</span><span class="sxs-lookup"><span data-stu-id="b9634-164">Basis</span></span>
- <span data-ttu-id="b9634-165">Сумма или ставка</span><span class="sxs-lookup"><span data-stu-id="b9634-165">Amount or rate</span></span>
- <span data-ttu-id="b9634-166">Код дохода</span><span class="sxs-lookup"><span data-stu-id="b9634-166">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="b9634-167">Поддерживаемые частоты</span><span class="sxs-lookup"><span data-stu-id="b9634-167">Supported frequencies</span></span> 

- <span data-ttu-id="b9634-168">Еженедельно</span><span class="sxs-lookup"><span data-stu-id="b9634-168">Weekly</span></span>
- <span data-ttu-id="b9634-169">Один раз в две недели</span><span class="sxs-lookup"><span data-stu-id="b9634-169">Bi-weekly</span></span>
- <span data-ttu-id="b9634-170">Два раза в месяц</span><span class="sxs-lookup"><span data-stu-id="b9634-170">Semi-monthly</span></span>
- <span data-ttu-id="b9634-171">Один раз в месяц</span><span class="sxs-lookup"><span data-stu-id="b9634-171">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="b9634-172">Поддерживаемые базы</span><span class="sxs-lookup"><span data-stu-id="b9634-172">Supported bases</span></span> 

- <span data-ttu-id="b9634-173">Фиксированная сумма</span><span class="sxs-lookup"><span data-stu-id="b9634-173">Fixed amount</span></span>
- <span data-ttu-id="b9634-174">Процент дохода</span><span class="sxs-lookup"><span data-stu-id="b9634-174">Percent of earnings</span></span>
- <span data-ttu-id="b9634-175">Продуктивные часы</span><span class="sxs-lookup"><span data-stu-id="b9634-175">Productive hours</span></span>

<span data-ttu-id="b9634-176">Dayforce создает следующие вычеты на основе влияния на зарплату, которое определено в плане льгот.</span><span class="sxs-lookup"><span data-stu-id="b9634-176">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="b9634-177">Выбор в Human Resources</span><span class="sxs-lookup"><span data-stu-id="b9634-177">Selection in Human Resources</span></span>        | <span data-ttu-id="b9634-178">Результат в Dayforce</span><span class="sxs-lookup"><span data-stu-id="b9634-178">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="b9634-179">Нет</span><span class="sxs-lookup"><span data-stu-id="b9634-179">None</span></span>                       | <span data-ttu-id="b9634-180">Вычет не создается.</span><span class="sxs-lookup"><span data-stu-id="b9634-180">No deduction is created.</span></span>                      |
| <span data-ttu-id="b9634-181">Только удержание</span><span class="sxs-lookup"><span data-stu-id="b9634-181">Deduction only</span></span>             | <span data-ttu-id="b9634-182">Вычет сотрудника будет создан.</span><span class="sxs-lookup"><span data-stu-id="b9634-182">An employee deduction is created.</span></span>             |
| <span data-ttu-id="b9634-183">Только вклад</span><span class="sxs-lookup"><span data-stu-id="b9634-183">Contribution only</span></span>          | <span data-ttu-id="b9634-184">Вычет работодателя будет создан.</span><span class="sxs-lookup"><span data-stu-id="b9634-184">An employer deduction is created.</span></span>             |
| <span data-ttu-id="b9634-185">Удержание и вклад</span><span class="sxs-lookup"><span data-stu-id="b9634-185">Deduction and contribution</span></span> | <span data-ttu-id="b9634-186">Создаются вычеты сотрудников и работодателя.</span><span class="sxs-lookup"><span data-stu-id="b9634-186">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="b9634-187">Дополнительные сведения о том, как определять и управлять программами льгот, см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="b9634-187">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="b9634-188">Реализация программы льгот сотрудника</span><span class="sxs-lookup"><span data-stu-id="b9634-188">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="b9634-189">Создать новую льготу</span><span class="sxs-lookup"><span data-stu-id="b9634-189">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="b9634-190">Определение правил и политик проверки прав на льготы</span><span class="sxs-lookup"><span data-stu-id="b9634-190">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="b9634-191">Регистрация и удаление льгот для работников</span><span class="sxs-lookup"><span data-stu-id="b9634-191">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="b9634-192">Компенсация</span><span class="sxs-lookup"><span data-stu-id="b9634-192">Compensation</span></span> 

<span data-ttu-id="b9634-193">Управление компенсациями используется для управления предоставлением базовой оплаты и вознаграждений.</span><span class="sxs-lookup"><span data-stu-id="b9634-193">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="b9634-194">Тарифные ставки и единовременные надбавки контролируются с помощью планов фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="b9634-194">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="b9634-195">Поощрительные выплаты, такие как премии, вознаграждения за производительность, опционы на покупку акций и гранты, а также одноразовые компенсации, контролируются с помощью планов переменных компенсаций.</span><span class="sxs-lookup"><span data-stu-id="b9634-195">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="b9634-196">Dayforce использует сведения о компенсации для расчета почасовой или годовой ставки сотрудника.</span><span class="sxs-lookup"><span data-stu-id="b9634-196">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="b9634-197">Требуются планы фиксированной компенсации и преобразования ставки оплаты.</span><span class="sxs-lookup"><span data-stu-id="b9634-197">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="b9634-198">Сотрудники должны быть связаны с планом фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="b9634-198">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="b9634-199">Дополнительные сведения о планах компенсации см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="b9634-199">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="b9634-200">Создание планов фиксированной компенсации</span><span class="sxs-lookup"><span data-stu-id="b9634-200">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="b9634-201">Создание планов переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="b9634-201">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="b9634-202">Разработка структуры и планов зарплаты/компенсации</span><span class="sxs-lookup"><span data-stu-id="b9634-202">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="b9634-203">Обработка компенсаций</span><span class="sxs-lookup"><span data-stu-id="b9634-203">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="b9634-204">Определение процесса компенсации и расчет результатов</span><span class="sxs-lookup"><span data-stu-id="b9634-204">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="b9634-205">Включение сотрудника в план фиксированных компенсаций</span><span class="sxs-lookup"><span data-stu-id="b9634-205">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="b9634-206">Включение сотрудника в план переменных компенсаций</span><span class="sxs-lookup"><span data-stu-id="b9634-206">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="b9634-207">Должности</span><span class="sxs-lookup"><span data-stu-id="b9634-207">Jobs</span></span> 

<span data-ttu-id="b9634-208">Должностные обязанности — это набор задач и обязанностей, которые возлагаются на занимающее эту задание лицо.</span><span class="sxs-lookup"><span data-stu-id="b9634-208">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="b9634-209">Дополнительные сведения см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="b9634-209">For more information, see the following articles:</span></span>

- [<span data-ttu-id="b9634-210">Настройка компонентов должности</span><span class="sxs-lookup"><span data-stu-id="b9634-210">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="b9634-211">Определение новых должностей</span><span class="sxs-lookup"><span data-stu-id="b9634-211">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="b9634-212">Позиции</span><span class="sxs-lookup"><span data-stu-id="b9634-212">Positions</span></span>

<span data-ttu-id="b9634-213">Позиция — это индивидуальный экземпляр должности.</span><span class="sxs-lookup"><span data-stu-id="b9634-213">A position is an individual instance of a job.</span></span> <span data-ttu-id="b9634-214">Например, должность "Менеджер по продажам (восток)" — это одна из должностей, связанных с должностными обязанностями "Менеджер по продажам".</span><span class="sxs-lookup"><span data-stu-id="b9634-214">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="b9634-215">Должность существует в отделе.</span><span class="sxs-lookup"><span data-stu-id="b9634-215">A position exists in a department.</span></span> <span data-ttu-id="b9634-216">Только один работник может быть связан с каждой должностью.</span><span class="sxs-lookup"><span data-stu-id="b9634-216">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="b9634-217">Учитывайте следующие данные и конфигурацию при настройке должностей:</span><span class="sxs-lookup"><span data-stu-id="b9634-217">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="b9634-218">Должность (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-218">Position (required)</span></span>
- <span data-ttu-id="b9634-219">Описание (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-219">Description (required)</span></span>
- <span data-ttu-id="b9634-220">Должностные обязанности (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-220">Job (required)</span></span>
- <span data-ttu-id="b9634-221">Отдел (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-221">Department (required)</span></span>
- <span data-ttu-id="b9634-222">Тип должности (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-222">Position type (required)</span></span>
- <span data-ttu-id="b9634-223">Эквивалент полной занятости</span><span class="sxs-lookup"><span data-stu-id="b9634-223">Full-time equivalent</span></span>
- <span data-ttu-id="b9634-224">Обычные часы за год (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-224">Annual regular hours (required)</span></span>
- <span data-ttu-id="b9634-225">Оплачивается юридическим лицом (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-225">Paid by legal entity (required)</span></span>
- <span data-ttu-id="b9634-226">Цикл оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-226">Pay cycle (required)</span></span>
- <span data-ttu-id="b9634-227">Финансовая аналитика по умолчанию — центр затрат (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-227">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="b9634-228">Назначение работника — работник, начало назначения, окончание назначения, код причины</span><span class="sxs-lookup"><span data-stu-id="b9634-228">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="b9634-229">Если несколько должностей в одном отделе связаны с одними и теми же должностными обязанностями, они объединяются в одну должность в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b9634-229">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="b9634-230">Дополнительные сведения см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="b9634-230">For more information, see the following articles:</span></span>

- [<span data-ttu-id="b9634-231">Организация трудовых ресурсов с использованием подразделений, должностей и штатных единиц</span><span class="sxs-lookup"><span data-stu-id="b9634-231">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="b9634-232">Настройка должностей</span><span class="sxs-lookup"><span data-stu-id="b9634-232">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="b9634-233">Отделы</span><span class="sxs-lookup"><span data-stu-id="b9634-233">Departments</span></span>

<span data-ttu-id="b9634-234">Подразделение — это операционная единица, которая представляет собой категорию или функциональную область в организации.</span><span class="sxs-lookup"><span data-stu-id="b9634-234">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="b9634-235">Подразделение отвечает за конкретную область деятельности организации, например продажи, бухгалтерский учет или управление персоналом.</span><span class="sxs-lookup"><span data-stu-id="b9634-235">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="b9634-236">Подразделения можно использовать для формирования отчетности по функциональным областям.</span><span class="sxs-lookup"><span data-stu-id="b9634-236">You can use departments to report on functional areas.</span></span> <span data-ttu-id="b9634-237">Подразделения могут нести ответственность за прибыли и убытки.</span><span class="sxs-lookup"><span data-stu-id="b9634-237">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="b9634-238">Дополнительные сведения см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="b9634-238">For more information, see the following articles:</span></span>

- [<span data-ttu-id="b9634-239">Создание подразделения и связывание его с иерархией подразделений</span><span class="sxs-lookup"><span data-stu-id="b9634-239">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="b9634-240">Определение новых подразделений</span><span class="sxs-lookup"><span data-stu-id="b9634-240">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="b9634-241">Циклы оплаты и платежные периоды</span><span class="sxs-lookup"><span data-stu-id="b9634-241">Pay cycles and pay periods</span></span>

<span data-ttu-id="b9634-242">Цикл оплаты определяет, как часто рассчитывается зарплата и определенные дни, когда работники получают зарплату.</span><span class="sxs-lookup"><span data-stu-id="b9634-242">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="b9634-243">Например, цикл оплаты может быть ежемесячным, и сотрудникам может выплачиваться зарплата в последний день месяца.</span><span class="sxs-lookup"><span data-stu-id="b9634-243">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="b9634-244">Кроме того, цикл оплаты может быть еженедельным, а сотрудники могут получать зарплату по вторникам после завершения периода оплаты.</span><span class="sxs-lookup"><span data-stu-id="b9634-244">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="b9634-245">Циклы оплаты назначаются должностям для управления выплатами работникам для этих должностей.</span><span class="sxs-lookup"><span data-stu-id="b9634-245">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="b9634-246">После создания циклов зарплаты можно создать платежные периоды для каждого цикла.</span><span class="sxs-lookup"><span data-stu-id="b9634-246">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="b9634-247">Каждый платежный период включает дату оплаты по умолчанию, которая основана на информации, предоставленной вами.</span><span class="sxs-lookup"><span data-stu-id="b9634-247">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="b9634-248">Однако можно изменить дату платежа по умолчанию в платежный период для учета исключений, например, когда дата оплаты приходится на праздник.</span><span class="sxs-lookup"><span data-stu-id="b9634-248">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="b9634-249">Dayforce использует следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="b9634-249">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="b9634-250">Цикл оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-250">Pay cycle (required)</span></span>
- <span data-ttu-id="b9634-251">Частота циклов оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-251">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="b9634-252">Дата начала периода (первый период оплаты обязателен)</span><span class="sxs-lookup"><span data-stu-id="b9634-252">Period start date (first pay period required)</span></span>
- <span data-ttu-id="b9634-253">Дата платежа по умолчанию (первый период оплаты обязателен)</span><span class="sxs-lookup"><span data-stu-id="b9634-253">Default payment date (first pay period required)</span></span>

<span data-ttu-id="b9634-254">Эта информация интегрирована с Dayforce как платежные группы, и разделяется по странам или регионам для каждого цикла оплаты.</span><span class="sxs-lookup"><span data-stu-id="b9634-254">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="b9634-255">Хотя бы один платежный период должен быть создан до интеграции.</span><span class="sxs-lookup"><span data-stu-id="b9634-255">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="b9634-256">Dayforce создает календари группы оплаты и даты оплаты на основе даты начала первого периода оплаты и даты оплаты по умолчанию, настроенных в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b9634-256">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="b9634-257">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="b9634-257">Earning codes</span></span>

<span data-ttu-id="b9634-258">Коды доходов уникально определяют каждый типа доходов, которые работники получают.</span><span class="sxs-lookup"><span data-stu-id="b9634-258">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="b9634-259">Эти коды имеют различные параметры, которые относятся к доходам, таких как правила учета, налоговые законы, требования к отчетности и возможности брутто в большую сторону.</span><span class="sxs-lookup"><span data-stu-id="b9634-259">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="b9634-260">Dayforce использует следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="b9634-260">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="b9634-261">Код дохода (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-261">Earning Code (required)</span></span>
- <span data-ttu-id="b9634-262">описание</span><span class="sxs-lookup"><span data-stu-id="b9634-262">Description</span></span>
- <span data-ttu-id="b9634-263">Единица измерения</span><span class="sxs-lookup"><span data-stu-id="b9634-263">Unit of measure</span></span>
- <span data-ttu-id="b9634-264">Продуктивный</span><span class="sxs-lookup"><span data-stu-id="b9634-264">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="b9634-265">Данные о работнике</span><span class="sxs-lookup"><span data-stu-id="b9634-265">Worker data</span></span>

<span data-ttu-id="b9634-266">Записи о различных типах сотрудников, которые имеются у вас, важны для вашей системы управления персоналом и системы расчета заработной платы.</span><span class="sxs-lookup"><span data-stu-id="b9634-266">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="b9634-267">Вводимые данные могут использоваться для отслеживания сведений о работниках и личной информации.</span><span class="sxs-lookup"><span data-stu-id="b9634-267">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="b9634-268">По работникам может храниться следующая информация.</span><span class="sxs-lookup"><span data-stu-id="b9634-268">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="b9634-269">**Основная** — базовые сведения о работнике, такие как контактные данные, демографические данные, идентифицирующие сведения, состав семье, сведения о службе в армии, данные об иностранных сотрудниках, персональные контакты и контакты на случай экстренных ситуаций.</span><span class="sxs-lookup"><span data-stu-id="b9634-269">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="b9634-270">**Занятость** — сведения о занятости работников, такие как участие в компании или организации, должность, дату начала и завершения работы, способность к работе, условия найма, пенсия, отпуска и сведения о переездах.</span><span class="sxs-lookup"><span data-stu-id="b9634-270">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="b9634-271">**Отпуск и отсутствие** — сведения об отпусках или пропуска работника, рабочие календари, проводки отсутствия и соответствующие настройки.</span><span class="sxs-lookup"><span data-stu-id="b9634-271">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="b9634-272">**Заработная плата и компенсации** — сведения о планах вознаграждениях и зарплате работника, такие как премии, комиссии, налоги, выход на пенсию и вычеты из зарплаты.</span><span class="sxs-lookup"><span data-stu-id="b9634-272">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="b9634-273">При вводе сведений о работнике имейте в виду следующие данные и конфигурации, которые используются в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b9634-273">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="b9634-274">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="b9634-274">General information</span></span>

- <span data-ttu-id="b9634-275">Табельный номер (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-275">Personnel number (required)</span></span>
- <span data-ttu-id="b9634-276">Имя (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-276">First name (required)</span></span>
- <span data-ttu-id="b9634-277">Фамилия (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-277">Last name (required)</span></span>
- <span data-ttu-id="b9634-278">Отчество</span><span class="sxs-lookup"><span data-stu-id="b9634-278">Middle name</span></span>
- <span data-ttu-id="b9634-279">Дата начала стажа</span><span class="sxs-lookup"><span data-stu-id="b9634-279">Seniority date</span></span>
- <span data-ttu-id="b9634-280">Известно как</span><span class="sxs-lookup"><span data-stu-id="b9634-280">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="b9634-281">Личная информация</span><span class="sxs-lookup"><span data-stu-id="b9634-281">Personal information</span></span>

- <span data-ttu-id="b9634-282">Семейное положение (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-282">Marital status (required)</span></span>
- <span data-ttu-id="b9634-283">Дата рождения (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-283">Birth date (required)</span></span>
- <span data-ttu-id="b9634-284">Пол (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-284">Gender (required)</span></span>
- <span data-ttu-id="b9634-285">Лицо с инвалидностью</span><span class="sxs-lookup"><span data-stu-id="b9634-285">Person with disabilities</span></span>
- <span data-ttu-id="b9634-286">Национальность, регион страны (только в Мексике)</span><span class="sxs-lookup"><span data-stu-id="b9634-286">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="b9634-287">Адресная информация</span><span class="sxs-lookup"><span data-stu-id="b9634-287">Address information</span></span>

- <span data-ttu-id="b9634-288">Основной (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-288">Primary (required)</span></span>
- <span data-ttu-id="b9634-289">Страна/регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-289">Country/region (required)</span></span>
- <span data-ttu-id="b9634-290">Почтовый индекс (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-290">Postal code (required)</span></span>
- <span data-ttu-id="b9634-291">Номер дома (обязательно) (только для Мексики)</span><span class="sxs-lookup"><span data-stu-id="b9634-291">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="b9634-292">Дополнение здания (только в Мексике)</span><span class="sxs-lookup"><span data-stu-id="b9634-292">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="b9634-293">Город (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-293">City (required)</span></span>
- <span data-ttu-id="b9634-294">Регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-294">State (required)</span></span>
- <span data-ttu-id="b9634-295">Район (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-295">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="b9634-296">Контактная информация</span><span class="sxs-lookup"><span data-stu-id="b9634-296">Contact information</span></span> 

- <span data-ttu-id="b9634-297">Основной (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-297">Primary (required)</span></span>
- <span data-ttu-id="b9634-298">Контактный номер (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-298">Contact number (required)</span></span>
- <span data-ttu-id="b9634-299">Расширение</span><span class="sxs-lookup"><span data-stu-id="b9634-299">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="b9634-300">Информация по зарплате и коды дохода</span><span class="sxs-lookup"><span data-stu-id="b9634-300">Payroll information and earning codes</span></span>

<span data-ttu-id="b9634-301">Сотрудникам можно назначить конкретные доходы с заданной периодичностью оплаты и предпочтительный метод оплаты.</span><span class="sxs-lookup"><span data-stu-id="b9634-301">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="b9634-302">Следующие поля используются в Dayforce для обеспечения использования этих параметров и настроек.</span><span class="sxs-lookup"><span data-stu-id="b9634-302">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="b9634-303">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="b9634-303">Earning codes</span></span>

- <span data-ttu-id="b9634-304">Должность (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-304">Position (required)</span></span>
- <span data-ttu-id="b9634-305">Код дохода (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-305">Earning Code (required)</span></span>
- <span data-ttu-id="b9634-306">Частота (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-306">Frequency (required)</span></span>
- <span data-ttu-id="b9634-307">Сумма (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-307">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="b9634-308">Информация по зарплате</span><span class="sxs-lookup"><span data-stu-id="b9634-308">Payroll information</span></span>

- <span data-ttu-id="b9634-309">Способ оплаты</span><span class="sxs-lookup"><span data-stu-id="b9634-309">Payment Method</span></span>
- <span data-ttu-id="b9634-310">Экономический регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-310">Economic Region (required)</span></span>
- <span data-ttu-id="b9634-311">ИД льгот сотрудников</span><span class="sxs-lookup"><span data-stu-id="b9634-311">Employee Benefits ID</span></span>
- <span data-ttu-id="b9634-312">Идентификационный номер (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-312">National ID Number (required)</span></span>
- <span data-ttu-id="b9634-313">Номер документа о воинской службе</span><span class="sxs-lookup"><span data-stu-id="b9634-313">Military Service Number</span></span>
- <span data-ttu-id="b9634-314">Код смены (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-314">Shift ID (required)</span></span>
- <span data-ttu-id="b9634-315">Налоговой номер (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-315">Tax Number (required)</span></span>
- <span data-ttu-id="b9634-316">Код профсоюза (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-316">Union ID (required)</span></span>
- <span data-ttu-id="b9634-317">Идентификатор рабочего дня (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-317">Work Day ID (required)</span></span>
- <span data-ttu-id="b9634-318">Номер разрешения на работу</span><span class="sxs-lookup"><span data-stu-id="b9634-318">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="b9634-319">Для метода оплаты в Мексике поддерживает **Наличные деньги**, **Чек** (физический чек компании) и **Электронный платеж**.</span><span class="sxs-lookup"><span data-stu-id="b9634-319">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="b9634-320">Если способ оплаты не указан, **Чек** используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b9634-320">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="b9634-321">Сведения о трудоустройстве</span><span class="sxs-lookup"><span data-stu-id="b9634-321">Employment details</span></span>

<span data-ttu-id="b9634-322">Подробная история занятости используется как ключевая информация для извлечения статуса найма, увольнения и повторного найма сотрудника в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b9634-322">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="b9634-323">Dayforce поддерживает только одну активную запись о приеме на работу одновременно.</span><span class="sxs-lookup"><span data-stu-id="b9634-323">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="b9634-324">Дата начала трудоустройства (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-324">Employment start date (required)</span></span>
- <span data-ttu-id="b9634-325">Дата окончания занятости</span><span class="sxs-lookup"><span data-stu-id="b9634-325">Employment end date</span></span>
- <span data-ttu-id="b9634-326">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="b9634-326">Start date</span></span>
- <span data-ttu-id="b9634-327">Скорректированная дата приема на работу</span><span class="sxs-lookup"><span data-stu-id="b9634-327">Adjusted start date</span></span>
- <span data-ttu-id="b9634-328">Дата увольнения (обязательно после увольнения)</span><span class="sxs-lookup"><span data-stu-id="b9634-328">Termination date (required upon termination)</span></span>
- <span data-ttu-id="b9634-329">Причина увольнения (обязательно после увольнения)</span><span class="sxs-lookup"><span data-stu-id="b9634-329">Termination reason (required upon termination)</span></span>

<span data-ttu-id="b9634-330">Ключевые даты сотрудника получаются на основе следующих сведений.</span><span class="sxs-lookup"><span data-stu-id="b9634-330">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="b9634-331">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="b9634-331">Human Resources</span></span>                | <span data-ttu-id="b9634-332">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b9634-332">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9634-333">Самая последняя дата приема на работу</span><span class="sxs-lookup"><span data-stu-id="b9634-333">Most recent hire date</span></span> | <span data-ttu-id="b9634-334">Дата приема на работу для текущей записи истории занятости, которая еще не завершена</span><span class="sxs-lookup"><span data-stu-id="b9634-334">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="b9634-335">Дата увольнения</span><span class="sxs-lookup"><span data-stu-id="b9634-335">Termination date</span></span>      | <span data-ttu-id="b9634-336">Дата увольнения для текущей записи истории занятости, которая еще не завершена</span><span class="sxs-lookup"><span data-stu-id="b9634-336">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="b9634-337">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="b9634-337">Start date</span></span>            | <span data-ttu-id="b9634-338">Скорректированная дата приема на работу, дата приема на работу или дата приема на работу текущей неактивной записи история занятости</span><span class="sxs-lookup"><span data-stu-id="b9634-338">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="b9634-339">Дата первоначального приема на работу</span><span class="sxs-lookup"><span data-stu-id="b9634-339">Original hire date</span></span>    | <span data-ttu-id="b9634-340">Дата приема на работу самой ранней записи истории приема на работу</span><span class="sxs-lookup"><span data-stu-id="b9634-340">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="b9634-341">Компенсация</span><span class="sxs-lookup"><span data-stu-id="b9634-341">Compensation</span></span>

<span data-ttu-id="b9634-342">План фиксированной компенсации должен быть связан с каждой основной должностью работника на протяжении всего периода занятости.</span><span class="sxs-lookup"><span data-stu-id="b9634-342">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="b9634-343">Этот период начинается на даты, в которую сотрудник был нанят (или начальная дата приема на работу) и продолжается до увольнения.</span><span class="sxs-lookup"><span data-stu-id="b9634-343">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="b9634-344">Дата вступления в силу (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-344">Effective Date (required)</span></span>
- <span data-ttu-id="b9634-345">Срок действия</span><span class="sxs-lookup"><span data-stu-id="b9634-345">Expiration date</span></span>
- <span data-ttu-id="b9634-346">Ставка оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-346">Pay Rate (required)</span></span>
- <span data-ttu-id="b9634-347">Преобразования ставки оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-347">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="b9634-348">Годовой эквивалент (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-348">Annual equivalent (required)</span></span>
- <span data-ttu-id="b9634-349">Почасовой эквивалент (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-349">Hourly equivalent (required)</span></span>

<span data-ttu-id="b9634-350">Если сотрудник с почасовой оплатой имеет несколько должностей, фиксированная компенсация основной должности импортируется в Dayforce как базовая ставка/зарплата уровня сотрудника.</span><span class="sxs-lookup"><span data-stu-id="b9634-350">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="b9634-351">Дня неосновных должностей почасовая ставка сохраняется в соответствующей должности в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b9634-351">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="b9634-352">Если штатный сотрудник имеет несколько должностей, суммарная почасовая ставка и годовая заработная плата для всех активных должностей определяется и используется в качестве базовой ставки/зарплаты уровня сотрудника.</span><span class="sxs-lookup"><span data-stu-id="b9634-352">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="b9634-353">Идентификационные номера</span><span class="sxs-lookup"><span data-stu-id="b9634-353">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="b9634-354">Код социального страхования</span><span class="sxs-lookup"><span data-stu-id="b9634-354">Social Security identifier</span></span> 

<span data-ttu-id="b9634-355">Каждый сотрудник должен иметь один первичный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="b9634-355">Every employee must have one primary identifier.</span></span> <span data-ttu-id="b9634-356">Этот идентификатор должен быть идентификатором типа **SSN**.</span><span class="sxs-lookup"><span data-stu-id="b9634-356">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="b9634-357">В Dayforce он автоматически извлекается как код социального страхования сотрудника, который необходим для приема на работу.</span><span class="sxs-lookup"><span data-stu-id="b9634-357">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="b9634-358">Основной (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-358">Primary (required)</span></span>
- <span data-ttu-id="b9634-359">Тип идентификации = "SSN"</span><span class="sxs-lookup"><span data-stu-id="b9634-359">Identification Type = "SSN"</span></span>
- <span data-ttu-id="b9634-360">Дата выпуска</span><span class="sxs-lookup"><span data-stu-id="b9634-360">Issued Date</span></span>
- <span data-ttu-id="b9634-361">Дата окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="b9634-361">Expiration Date</span></span>

<span data-ttu-id="b9634-362">Сотрудники могут объявить несколько идентификационных номеров для типа идентификатора **SSN**.</span><span class="sxs-lookup"><span data-stu-id="b9634-362">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="b9634-363">Тем не менее только запись, которая помечен как **Основная**, интегрируется в Dayforce, независимо от того, является ли номер активным или у него истек срок действия.</span><span class="sxs-lookup"><span data-stu-id="b9634-363">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="b9634-364">Банковские счета и выплаты</span><span class="sxs-lookup"><span data-stu-id="b9634-364">Bank accounts and disbursements</span></span>

<span data-ttu-id="b9634-365">Необходимо ввести действительную информацию о банковском счете для любого сотрудника, который выбирает оплату через перевод на банковский счет.</span><span class="sxs-lookup"><span data-stu-id="b9634-365">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="b9634-366">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="b9634-366">Human Resources</span></span>                         | <span data-ttu-id="b9634-367">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b9634-367">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9634-368">Номер счета в банке (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-368">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="b9634-369">Код SWIFT (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-369">SWIFT code (required)</span></span>          | <span data-ttu-id="b9634-370">Поле **Код банка** используется при обработке зарплаты в Мексике.</span><span class="sxs-lookup"><span data-stu-id="b9634-370">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="b9634-371">Номер филиала (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-371">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="b9634-372">Тип банковского счета (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-372">Bank account type (required)</span></span>   | <span data-ttu-id="b9634-373">Поле **Тип счета** используется при обработке зарплаты в Мексике.</span><span class="sxs-lookup"><span data-stu-id="b9634-373">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="b9634-374">Поддерживаются значения **Выписка чека** и **Заработная плата**.</span><span class="sxs-lookup"><span data-stu-id="b9634-374">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="b9634-375">Работники, которые выбрали выплату переводом на банковский счет, должен предоставить ссылку на счет остатков, находящийся в юридическом лице с основным адресом в Мексике и связанный с действительным банковским счетом из мексиканского банка.</span><span class="sxs-lookup"><span data-stu-id="b9634-375">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="b9634-376">Все другие счета, не являющиеся счетами остатков, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="b9634-376">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="b9634-377">Адресная информация</span><span class="sxs-lookup"><span data-stu-id="b9634-377">Address information</span></span>

<span data-ttu-id="b9634-378">Каждый сотрудник должен иметь одно первичное местонахождение.</span><span class="sxs-lookup"><span data-stu-id="b9634-378">Every employee must have one primary location.</span></span> <span data-ttu-id="b9634-379">В Dayforce это расположение используется для определения основного места жительства сотрудника для целей налогообложения.</span><span class="sxs-lookup"><span data-stu-id="b9634-379">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="b9634-380">Основной (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-380">Primary (required)</span></span>
- <span data-ttu-id="b9634-381">Страна/регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-381">Country/region (required)</span></span>
- <span data-ttu-id="b9634-382">Почтовый индекс (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-382">Zip/postal code (required)</span></span>
- <span data-ttu-id="b9634-383">Улица (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-383">Street (required)</span></span>
- <span data-ttu-id="b9634-384">Номер дома (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-384">Street Number (required)</span></span>
- <span data-ttu-id="b9634-385">Дополнение здания</span><span class="sxs-lookup"><span data-stu-id="b9634-385">Building Complement</span></span>
- <span data-ttu-id="b9634-386">Город (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-386">City (required)</span></span>
- <span data-ttu-id="b9634-387">Регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-387">State (required)</span></span>
- <span data-ttu-id="b9634-388">Район (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-388">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="b9634-389">Настройка данных для расчета заработной платы в США и Канаде</span><span class="sxs-lookup"><span data-stu-id="b9634-389">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="b9634-390">Если вы создаете оплату для сотрудников в США и Канаде, необходимо настроить следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="b9634-390">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="b9634-391">Обязательно указывать подразделения для должностей.</span><span class="sxs-lookup"><span data-stu-id="b9634-391">Departments are required on positions.</span></span>
- <span data-ttu-id="b9634-392">Центры затрат должен быть заданы как финансовые аналитики и должны быть первым элементом в строке финансовой аналитики по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b9634-392">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="b9634-393">Можно настроить Human Resources, чтобы для должностей требовалось указывать подразделение.</span><span class="sxs-lookup"><span data-stu-id="b9634-393">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="b9634-394">Чтобы сделать это, выберите **Совместно используемые позиции управления персоналом > Позиции > Требовать подразделения для позиций**.</span><span class="sxs-lookup"><span data-stu-id="b9634-394">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="b9634-395">Рекомендуется включить этот параметр для интеграции.</span><span class="sxs-lookup"><span data-stu-id="b9634-395">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="b9634-396">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="b9634-396">Job types</span></span>

<span data-ttu-id="b9634-397">Типы должностей используются для группирования похожих должностных обязанностей в категории.</span><span class="sxs-lookup"><span data-stu-id="b9634-397">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="b9634-398">Типы должностей обязательны для обработки зарплаты в США и Канаде.</span><span class="sxs-lookup"><span data-stu-id="b9634-398">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="b9634-399">Примеры типов должностей включают полный рабочий день и неполный рабочий день, или зарплата и почасовая оплата.</span><span class="sxs-lookup"><span data-stu-id="b9634-399">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="b9634-400">Типы должностей сопоставляются с Dayforce как типы зарплаты, которые указывают тип оплаты сотрудника: почасовая или оклад.</span><span class="sxs-lookup"><span data-stu-id="b9634-400">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="b9634-401">Требуются следующие типы должностей и описаний.</span><span class="sxs-lookup"><span data-stu-id="b9634-401">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="b9634-402">Тип задания</span><span class="sxs-lookup"><span data-stu-id="b9634-402">Job type</span></span>   | <span data-ttu-id="b9634-403">описание</span><span class="sxs-lookup"><span data-stu-id="b9634-403">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="b9634-404">Почасовая</span><span class="sxs-lookup"><span data-stu-id="b9634-404">Hourly</span></span>     | <span data-ttu-id="b9634-405">Почасовая</span><span class="sxs-lookup"><span data-stu-id="b9634-405">Hourly</span></span>      |
| <span data-ttu-id="b9634-406">Оклад</span><span class="sxs-lookup"><span data-stu-id="b9634-406">Salaried</span></span>   | <span data-ttu-id="b9634-407">Оклад</span><span class="sxs-lookup"><span data-stu-id="b9634-407">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="b9634-408">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="b9634-408">Position types</span></span> 

<span data-ttu-id="b9634-409">С помощью типов должностей описывается, является ли должность занятостью на полный рабочий день, на неполный рабочий день или какой-либо другой.</span><span class="sxs-lookup"><span data-stu-id="b9634-409">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="b9634-410">Типы должностей сопоставляются с Dayforce как классы зарплаты, которые указывают тип оплаты сотрудника: полная занятость или частичная занятость.</span><span class="sxs-lookup"><span data-stu-id="b9634-410">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="b9634-411">Требуются следующие типы должностей и описаний.</span><span class="sxs-lookup"><span data-stu-id="b9634-411">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="b9634-412">Тип должности</span><span class="sxs-lookup"><span data-stu-id="b9634-412">Position type</span></span>   | <span data-ttu-id="b9634-413">описание</span><span class="sxs-lookup"><span data-stu-id="b9634-413">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="b9634-414">Полная занятость</span><span class="sxs-lookup"><span data-stu-id="b9634-414">Full-time</span></span>       | <span data-ttu-id="b9634-415">Работник с полной занятостью</span><span class="sxs-lookup"><span data-stu-id="b9634-415">Full time employee</span></span> |
| <span data-ttu-id="b9634-416">Частичная занятость</span><span class="sxs-lookup"><span data-stu-id="b9634-416">Part-time</span></span>       | <span data-ttu-id="b9634-417">Работник с частичной занятостью</span><span class="sxs-lookup"><span data-stu-id="b9634-417">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="b9634-418">Коды оснований</span><span class="sxs-lookup"><span data-stu-id="b9634-418">Reason codes</span></span>

<span data-ttu-id="b9634-419">Коды оснований содержат сведения о статусе сотрудника.</span><span class="sxs-lookup"><span data-stu-id="b9634-419">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="b9634-420">Коды оснований сопоставляются с Dayforce как причины статуса, которые определяют причину изменения статус должности или найма сотрудника.</span><span class="sxs-lookup"><span data-stu-id="b9634-420">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="b9634-421">Требуются следующие коды причин и описания.</span><span class="sxs-lookup"><span data-stu-id="b9634-421">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="b9634-422">Код основания</span><span class="sxs-lookup"><span data-stu-id="b9634-422">Reason code</span></span>    | <span data-ttu-id="b9634-423">описание</span><span class="sxs-lookup"><span data-stu-id="b9634-423">Description</span></span>      | <span data-ttu-id="b9634-424">Применимые сценарии</span><span class="sxs-lookup"><span data-stu-id="b9634-424">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="b9634-425">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="b9634-425">RESIGNATION</span></span>    | <span data-ttu-id="b9634-426">Увольнение</span><span class="sxs-lookup"><span data-stu-id="b9634-426">Resignation</span></span>      | <span data-ttu-id="b9634-427">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="b9634-427">Terminate worker</span></span>     |
| <span data-ttu-id="b9634-428">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="b9634-428">TERMINATION</span></span>    | <span data-ttu-id="b9634-429">Завершение</span><span class="sxs-lookup"><span data-stu-id="b9634-429">Termination</span></span>      | <span data-ttu-id="b9634-430">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="b9634-430">Terminate worker</span></span>     |
| <span data-ttu-id="b9634-431">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="b9634-431">RETIREMENT</span></span>     | <span data-ttu-id="b9634-432">Выходное пособие</span><span class="sxs-lookup"><span data-stu-id="b9634-432">Retirement</span></span>       | <span data-ttu-id="b9634-433">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="b9634-433">Terminate worker</span></span>     |
| <span data-ttu-id="b9634-434">ПРОЧЕЕ</span><span class="sxs-lookup"><span data-stu-id="b9634-434">OTHER</span></span>          | <span data-ttu-id="b9634-435">Другие причины</span><span class="sxs-lookup"><span data-stu-id="b9634-435">Other Reasons</span></span>    | <span data-ttu-id="b9634-436">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="b9634-436">Terminate worker</span></span>     |
| <span data-ttu-id="b9634-437">DEATH</span><span class="sxs-lookup"><span data-stu-id="b9634-437">DEATH</span></span>          | <span data-ttu-id="b9634-438">Смерть</span><span class="sxs-lookup"><span data-stu-id="b9634-438">Death</span></span>            | <span data-ttu-id="b9634-439">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="b9634-439">Terminate worker</span></span>     |
| <span data-ttu-id="b9634-440">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="b9634-440">LEAVEOFABSENCE</span></span> | <span data-ttu-id="b9634-441">Отпуск</span><span class="sxs-lookup"><span data-stu-id="b9634-441">Leave of Absence</span></span> | <span data-ttu-id="b9634-442">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="b9634-442">Terminate worker</span></span>     |
| <span data-ttu-id="b9634-443">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="b9634-443">CONTRACTEND</span></span>    | <span data-ttu-id="b9634-444">Завершение контракта</span><span class="sxs-lookup"><span data-stu-id="b9634-444">End of Contract</span></span>  | <span data-ttu-id="b9634-445">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="b9634-445">Terminate worker</span></span>     |
| <span data-ttu-id="b9634-446">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="b9634-446">SALARYCHANGE</span></span>   | <span data-ttu-id="b9634-447">Изменение зарплаты</span><span class="sxs-lookup"><span data-stu-id="b9634-447">Change of Salary</span></span> | <span data-ttu-id="b9634-448">Компенсация</span><span class="sxs-lookup"><span data-stu-id="b9634-448">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="b9634-449">Семейное положение</span><span class="sxs-lookup"><span data-stu-id="b9634-449">Marital status</span></span>

<span data-ttu-id="b9634-450">Значения семейного положения сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="b9634-450">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b9634-451">В следующей таблице показано, как значения семейного положения сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b9634-451">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="b9634-452">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="b9634-452">Human Resources</span></span>                 | <span data-ttu-id="b9634-453">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b9634-453">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="b9634-454">Женат/замужем</span><span class="sxs-lookup"><span data-stu-id="b9634-454">Married</span></span>                | <span data-ttu-id="b9634-455">Женат/замужем</span><span class="sxs-lookup"><span data-stu-id="b9634-455">Married</span></span>              |
| <span data-ttu-id="b9634-456">Один</span><span class="sxs-lookup"><span data-stu-id="b9634-456">Single</span></span>                 | <span data-ttu-id="b9634-457">Один</span><span class="sxs-lookup"><span data-stu-id="b9634-457">Single</span></span>               |
| <span data-ttu-id="b9634-458">Вдовец/вдова</span><span class="sxs-lookup"><span data-stu-id="b9634-458">Widowed</span></span>                | <span data-ttu-id="b9634-459">Вдовец/вдова</span><span class="sxs-lookup"><span data-stu-id="b9634-459">Widowed</span></span>              |
| <span data-ttu-id="b9634-460">Разведен/разведена</span><span class="sxs-lookup"><span data-stu-id="b9634-460">Divorced</span></span>               | <span data-ttu-id="b9634-461">Разведен/разведена</span><span class="sxs-lookup"><span data-stu-id="b9634-461">Divorced</span></span>             |
| <span data-ttu-id="b9634-462">Зарегистрированное партнерство</span><span class="sxs-lookup"><span data-stu-id="b9634-462">Registered Partnership</span></span> | <span data-ttu-id="b9634-463">Партнерство на внутреннем рынке</span><span class="sxs-lookup"><span data-stu-id="b9634-463">Domestic Partnership</span></span> |
| <span data-ttu-id="b9634-464">None</span><span class="sxs-lookup"><span data-stu-id="b9634-464">None</span></span>                   | <span data-ttu-id="b9634-465">None</span><span class="sxs-lookup"><span data-stu-id="b9634-465">None</span></span>                 |
| <span data-ttu-id="b9634-466">Партнерство</span><span class="sxs-lookup"><span data-stu-id="b9634-466">Cohabiting</span></span>             | <span data-ttu-id="b9634-467">Партнерство</span><span class="sxs-lookup"><span data-stu-id="b9634-467">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="b9634-468">Род</span><span class="sxs-lookup"><span data-stu-id="b9634-468">Gender</span></span>

<span data-ttu-id="b9634-469">Значения пола сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="b9634-469">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b9634-470">В следующей таблице показано, как значения пола сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b9634-470">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="b9634-471">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="b9634-471">Human Resources</span></span>       | <span data-ttu-id="b9634-472">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b9634-472">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="b9634-473">Пол сотрудника</span><span class="sxs-lookup"><span data-stu-id="b9634-473">Male</span></span>         | <span data-ttu-id="b9634-474">Пол сотрудника</span><span class="sxs-lookup"><span data-stu-id="b9634-474">Male</span></span>            |
| <span data-ttu-id="b9634-475">Женский</span><span class="sxs-lookup"><span data-stu-id="b9634-475">Female</span></span>       | <span data-ttu-id="b9634-476">Женский</span><span class="sxs-lookup"><span data-stu-id="b9634-476">Female</span></span>          |
| <span data-ttu-id="b9634-477">Неопределенный</span><span class="sxs-lookup"><span data-stu-id="b9634-477">Non-specific</span></span> | <span data-ttu-id="b9634-478">*Не поддерживается*</span><span class="sxs-lookup"><span data-stu-id="b9634-478">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="b9634-479">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="b9634-479">Earning codes</span></span>

<span data-ttu-id="b9634-480">Коды доходов уникально определяют каждый типа доходов, которые работники получают.</span><span class="sxs-lookup"><span data-stu-id="b9634-480">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="b9634-481">Эти коды покрывают несколько параметров, которые относятся к доходам, таких как правила учета, налоговые законы, требования к отчетности и возможности брутто в большую сторону.</span><span class="sxs-lookup"><span data-stu-id="b9634-481">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="b9634-482">Если используется неподдерживаемая частота, частота **Каждая оплата** используется по умолчанию для расчета.</span><span class="sxs-lookup"><span data-stu-id="b9634-482">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="b9634-483">Поддерживаемые частоты</span><span class="sxs-lookup"><span data-stu-id="b9634-483">Supported frequencies</span></span>

- <span data-ttu-id="b9634-484">Все</span><span class="sxs-lookup"><span data-stu-id="b9634-484">All</span></span>
- <span data-ttu-id="b9634-485">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="b9634-485">EVERYPAY</span></span>
- <span data-ttu-id="b9634-486">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="b9634-486">EACHPAYPERIOD</span></span>
- <span data-ttu-id="b9634-487">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="b9634-487">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="b9634-488">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="b9634-488">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="b9634-489">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-489">1OFMTH</span></span>
- <span data-ttu-id="b9634-490">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-490">LASTOFMTH</span></span>
- <span data-ttu-id="b9634-491">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-491">2OFMTH</span></span>
- <span data-ttu-id="b9634-492">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-492">3OFMTH</span></span>
- <span data-ttu-id="b9634-493">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-493">4OFMTH</span></span>
- <span data-ttu-id="b9634-494">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-494">5OFMTH</span></span>
- <span data-ttu-id="b9634-495">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-495">1N2OFMTH</span></span>
- <span data-ttu-id="b9634-496">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-496">3N4OFMTH</span></span>
- <span data-ttu-id="b9634-497">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-497">1N3OFMTH</span></span>
- <span data-ttu-id="b9634-498">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-498">1N4OFMTH</span></span>
- <span data-ttu-id="b9634-499">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-499">2N3OFMTH</span></span>
- <span data-ttu-id="b9634-500">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-500">2N4OFMTH</span></span>
- <span data-ttu-id="b9634-501">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-501">1N2N3OFMTH</span></span>
- <span data-ttu-id="b9634-502">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-502">1N2N4OFMTH</span></span>
- <span data-ttu-id="b9634-503">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-503">1N3N4OFMTH</span></span>
- <span data-ttu-id="b9634-504">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-504">2N3N4OFMTH</span></span>
- <span data-ttu-id="b9634-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="b9634-506">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="b9634-506">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="b9634-507">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="b9634-507">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="b9634-508">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="b9634-508">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="b9634-509">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="b9634-509">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="b9634-510">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="b9634-510">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="b9634-511">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b9634-511">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="b9634-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b9634-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="b9634-513">Адреса</span><span class="sxs-lookup"><span data-stu-id="b9634-513">Addresses</span></span>

<span data-ttu-id="b9634-514">Идентификация кодов конкретной страны или региона, области и района (муниципалитета) требует определенных форматов, которые Dayforce и поставщики в стране или в регионе могут распознать.</span><span class="sxs-lookup"><span data-stu-id="b9634-514">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="b9634-515">Хотя формат городов гибкий, каждый город должен быть связан с областью.</span><span class="sxs-lookup"><span data-stu-id="b9634-515">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="b9634-516">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="b9634-516">Human Resources</span></span>          | <span data-ttu-id="b9634-517">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b9634-517">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="b9634-518">Страна/регион</span><span class="sxs-lookup"><span data-stu-id="b9634-518">Country/Region</span></span>  | <span data-ttu-id="b9634-519">Код страны</span><span class="sxs-lookup"><span data-stu-id="b9634-519">Country Code</span></span>          |
| <span data-ttu-id="b9634-520">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="b9634-520">Zip/Postal Code</span></span> | <span data-ttu-id="b9634-521">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="b9634-521">Postal Code</span></span>           |
| <span data-ttu-id="b9634-522">Область, край</span><span class="sxs-lookup"><span data-stu-id="b9634-522">State</span></span>           | <span data-ttu-id="b9634-523">Код региона</span><span class="sxs-lookup"><span data-stu-id="b9634-523">State Code</span></span>            |
| <span data-ttu-id="b9634-524">Город</span><span class="sxs-lookup"><span data-stu-id="b9634-524">City</span></span>            | <span data-ttu-id="b9634-525">Город</span><span class="sxs-lookup"><span data-stu-id="b9634-525">City</span></span>                  |
| <span data-ttu-id="b9634-526">Округ</span><span class="sxs-lookup"><span data-stu-id="b9634-526">County</span></span>          | <span data-ttu-id="b9634-527">Район (муниципалитет)</span><span class="sxs-lookup"><span data-stu-id="b9634-527">County (Municipality)</span></span> |
| <span data-ttu-id="b9634-528">Улица</span><span class="sxs-lookup"><span data-stu-id="b9634-528">Street</span></span>          | <span data-ttu-id="b9634-529">Строка адреса 1</span><span class="sxs-lookup"><span data-stu-id="b9634-529">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="b9634-530">Налоговые регионы</span><span class="sxs-lookup"><span data-stu-id="b9634-530">Tax regions</span></span>

<span data-ttu-id="b9634-531">Налоговые регионы используются для определения налогов, которые следует применять при создании заработной платы.</span><span class="sxs-lookup"><span data-stu-id="b9634-531">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="b9634-532">Налоговые регионы сопоставляются с Dayforce как адреса местоположения.</span><span class="sxs-lookup"><span data-stu-id="b9634-532">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="b9634-533">Налоговый регион по умолчанию должен быть связан с активной должностью работника.</span><span class="sxs-lookup"><span data-stu-id="b9634-533">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="b9634-534">Налоговый регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-534">Tax region (required)</span></span>
- <span data-ttu-id="b9634-535">Страна/Регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-535">Country/Region (required)</span></span>
- <span data-ttu-id="b9634-536">Регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-536">State (required)</span></span>
- <span data-ttu-id="b9634-537">Округ</span><span class="sxs-lookup"><span data-stu-id="b9634-537">County</span></span> 
- <span data-ttu-id="b9634-538">Город (обязательно)</span><span class="sxs-lookup"><span data-stu-id="b9634-538">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="b9634-539">Настройка данных для расчета заработной платы в Мексике</span><span class="sxs-lookup"><span data-stu-id="b9634-539">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="b9634-540">Если вы создаете оплату для сотрудников в Мексике, необходимо настроить следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="b9634-540">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="b9634-541">Обязательно указывать подразделения для должностей.</span><span class="sxs-lookup"><span data-stu-id="b9634-541">Departments are required on positions.</span></span>
- <span data-ttu-id="b9634-542">Центры затрат должен быть заданы как финансовые аналитики и должны быть первым элементом в строке финансовой аналитики по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b9634-542">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="b9634-543">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="b9634-543">Job types</span></span>

<span data-ttu-id="b9634-544">Типы должностей используются для группирования похожих должностных обязанностей в категории.</span><span class="sxs-lookup"><span data-stu-id="b9634-544">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="b9634-545">Типы должностей обязательны для обработки зарплаты в Мексике.</span><span class="sxs-lookup"><span data-stu-id="b9634-545">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="b9634-546">Примеры типов должностей включают полный рабочий день и неполный рабочий день, или зарплата и почасовая оплата.</span><span class="sxs-lookup"><span data-stu-id="b9634-546">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="b9634-547">Типы должностей сопоставляются с Dayforce как типы зарплаты, которые указывают тип оплаты сотрудника: почасовая или оклад.</span><span class="sxs-lookup"><span data-stu-id="b9634-547">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="b9634-548">Требуются следующие типы должностей и описаний.</span><span class="sxs-lookup"><span data-stu-id="b9634-548">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="b9634-549">Тип задания</span><span class="sxs-lookup"><span data-stu-id="b9634-549">Job type</span></span>   | <span data-ttu-id="b9634-550">описание</span><span class="sxs-lookup"><span data-stu-id="b9634-550">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="b9634-551">Почасовая</span><span class="sxs-lookup"><span data-stu-id="b9634-551">Hourly</span></span>     | <span data-ttu-id="b9634-552">MX Почасовая</span><span class="sxs-lookup"><span data-stu-id="b9634-552">MX Hourly</span></span>   |
| <span data-ttu-id="b9634-553">Оклад</span><span class="sxs-lookup"><span data-stu-id="b9634-553">Salaried</span></span>   | <span data-ttu-id="b9634-554">MX Оклад</span><span class="sxs-lookup"><span data-stu-id="b9634-554">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="b9634-555">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="b9634-555">Position types</span></span> 

<span data-ttu-id="b9634-556">С помощью типов должностей описывается, является ли должность занятостью на полный рабочий день, на неполный рабочий день или какой-либо другой.</span><span class="sxs-lookup"><span data-stu-id="b9634-556">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="b9634-557">Типы должностей сопоставляются с Dayforce как классы зарплаты, которые указывают тип оплаты сотрудника: полная занятость или частичная занятость.</span><span class="sxs-lookup"><span data-stu-id="b9634-557">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="b9634-558">Требуются следующие типы должностей и описаний.</span><span class="sxs-lookup"><span data-stu-id="b9634-558">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="b9634-559">Тип должности</span><span class="sxs-lookup"><span data-stu-id="b9634-559">Position type</span></span>   | <span data-ttu-id="b9634-560">описание</span><span class="sxs-lookup"><span data-stu-id="b9634-560">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="b9634-561">Полная занятость</span><span class="sxs-lookup"><span data-stu-id="b9634-561">Full-time</span></span>       | <span data-ttu-id="b9634-562">Работник с полной занятостью</span><span class="sxs-lookup"><span data-stu-id="b9634-562">Full time employee</span></span> |
| <span data-ttu-id="b9634-563">Частичная занятость</span><span class="sxs-lookup"><span data-stu-id="b9634-563">Part-time</span></span>       | <span data-ttu-id="b9634-564">Работник с частичной занятостью</span><span class="sxs-lookup"><span data-stu-id="b9634-564">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="b9634-565">Коды оснований</span><span class="sxs-lookup"><span data-stu-id="b9634-565">Reason codes</span></span>

<span data-ttu-id="b9634-566">Коды оснований содержат сведения о статусе сотрудника.</span><span class="sxs-lookup"><span data-stu-id="b9634-566">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="b9634-567">Коды оснований сопоставляются с Dayforce как причины статуса, которые определяют причину изменения статус должности или найма сотрудника.</span><span class="sxs-lookup"><span data-stu-id="b9634-567">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="b9634-568">Требуются следующие коды причин и описания.</span><span class="sxs-lookup"><span data-stu-id="b9634-568">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="b9634-569">Код основания</span><span class="sxs-lookup"><span data-stu-id="b9634-569">Reason code</span></span>            | <span data-ttu-id="b9634-570">описание</span><span class="sxs-lookup"><span data-stu-id="b9634-570">Description</span></span>                    | <span data-ttu-id="b9634-571">Применимые сценарии</span><span class="sxs-lookup"><span data-stu-id="b9634-571">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="b9634-572">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="b9634-572">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="b9634-573">Увольнение до первой заработной платы</span><span class="sxs-lookup"><span data-stu-id="b9634-573">Departure before first payroll</span></span> | <span data-ttu-id="b9634-574">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="b9634-574">Terminate worker</span></span>     |
| <span data-ttu-id="b9634-575">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="b9634-575">RESIGNATION</span></span>            | <span data-ttu-id="b9634-576">Увольнение</span><span class="sxs-lookup"><span data-stu-id="b9634-576">Resignation</span></span>                    | <span data-ttu-id="b9634-577">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="b9634-577">Terminate worker</span></span>     |
| <span data-ttu-id="b9634-578">PENSION</span><span class="sxs-lookup"><span data-stu-id="b9634-578">PENSION</span></span>                | <span data-ttu-id="b9634-579">Пенсия</span><span class="sxs-lookup"><span data-stu-id="b9634-579">Pension</span></span>                        | <span data-ttu-id="b9634-580">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="b9634-580">Terminate worker</span></span>     |
| <span data-ttu-id="b9634-581">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="b9634-581">TERMINATION</span></span>            | <span data-ttu-id="b9634-582">Завершение</span><span class="sxs-lookup"><span data-stu-id="b9634-582">Termination</span></span>                    | <span data-ttu-id="b9634-583">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="b9634-583">Terminate worker</span></span>     |
| <span data-ttu-id="b9634-584">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="b9634-584">RETIREMENT</span></span>             | <span data-ttu-id="b9634-585">Выходное пособие</span><span class="sxs-lookup"><span data-stu-id="b9634-585">Retirement</span></span>                     | <span data-ttu-id="b9634-586">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="b9634-586">Terminate worker</span></span>     |
| <span data-ttu-id="b9634-587">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="b9634-587">ABSENTEE</span></span>               | <span data-ttu-id="b9634-588">Прогульщик</span><span class="sxs-lookup"><span data-stu-id="b9634-588">Absentee</span></span>                       | <span data-ttu-id="b9634-589">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="b9634-589">Terminate worker</span></span>     |
| <span data-ttu-id="b9634-590">ПРОЧЕЕ</span><span class="sxs-lookup"><span data-stu-id="b9634-590">OTHER</span></span>                  | <span data-ttu-id="b9634-591">Другие причины</span><span class="sxs-lookup"><span data-stu-id="b9634-591">Other Reasons</span></span>                  | <span data-ttu-id="b9634-592">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="b9634-592">Terminate worker</span></span>     |
| <span data-ttu-id="b9634-593">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="b9634-593">CLOSURE</span></span>                | <span data-ttu-id="b9634-594">Закрытие компании</span><span class="sxs-lookup"><span data-stu-id="b9634-594">Business Closure</span></span>               | <span data-ttu-id="b9634-595">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="b9634-595">Terminate worker</span></span>     |
| <span data-ttu-id="b9634-596">DEATH</span><span class="sxs-lookup"><span data-stu-id="b9634-596">DEATH</span></span>                  | <span data-ttu-id="b9634-597">Смерть</span><span class="sxs-lookup"><span data-stu-id="b9634-597">Death</span></span>                          | <span data-ttu-id="b9634-598">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="b9634-598">Terminate worker</span></span>     |
| <span data-ttu-id="b9634-599">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="b9634-599">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="b9634-600">Отпуск</span><span class="sxs-lookup"><span data-stu-id="b9634-600">Leave of Absence</span></span>               | <span data-ttu-id="b9634-601">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="b9634-601">Terminate worker</span></span>     |
| <span data-ttu-id="b9634-602">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="b9634-602">CONTRACTEND</span></span>            | <span data-ttu-id="b9634-603">Завершение контракта</span><span class="sxs-lookup"><span data-stu-id="b9634-603">End of Contract</span></span>                | <span data-ttu-id="b9634-604">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="b9634-604">Terminate worker</span></span>     |
| <span data-ttu-id="b9634-605">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="b9634-605">SALARYCHANGE</span></span>           | <span data-ttu-id="b9634-606">Изменение зарплаты</span><span class="sxs-lookup"><span data-stu-id="b9634-606">Change of Salary</span></span>               | <span data-ttu-id="b9634-607">Компенсация</span><span class="sxs-lookup"><span data-stu-id="b9634-607">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="b9634-608">Условия найма</span><span class="sxs-lookup"><span data-stu-id="b9634-608">Terms of employment</span></span>

<span data-ttu-id="b9634-609">Условия найма используются для создания категорий условий трудоустройства.</span><span class="sxs-lookup"><span data-stu-id="b9634-609">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="b9634-610">Условия сопоставляются с Dayforce как значения индикатора трудоустройства.</span><span class="sxs-lookup"><span data-stu-id="b9634-610">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="b9634-611">Необходимы следующие условия найма и описания.</span><span class="sxs-lookup"><span data-stu-id="b9634-611">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="b9634-612">Условия найма</span><span class="sxs-lookup"><span data-stu-id="b9634-612">Terms of employment</span></span>   | <span data-ttu-id="b9634-613">описание</span><span class="sxs-lookup"><span data-stu-id="b9634-613">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="b9634-614">Периодически</span><span class="sxs-lookup"><span data-stu-id="b9634-614">Regular</span></span>               | <span data-ttu-id="b9634-615">Периодически</span><span class="sxs-lookup"><span data-stu-id="b9634-615">Regular</span></span>     |
| <span data-ttu-id="b9634-616">Напрямую</span><span class="sxs-lookup"><span data-stu-id="b9634-616">Direct</span></span>                | <span data-ttu-id="b9634-617">Напрямую</span><span class="sxs-lookup"><span data-stu-id="b9634-617">Direct</span></span>      |
| <span data-ttu-id="b9634-618">Практика</span><span class="sxs-lookup"><span data-stu-id="b9634-618">Internship</span></span>            | <span data-ttu-id="b9634-619">Практика</span><span class="sxs-lookup"><span data-stu-id="b9634-619">Internship</span></span>  |
| <span data-ttu-id="b9634-620">Постоянный</span><span class="sxs-lookup"><span data-stu-id="b9634-620">Permanent</span></span>             | <span data-ttu-id="b9634-621">Постоянный</span><span class="sxs-lookup"><span data-stu-id="b9634-621">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="b9634-622">Семейное положение</span><span class="sxs-lookup"><span data-stu-id="b9634-622">Marital status</span></span>

<span data-ttu-id="b9634-623">Значения семейного положения сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="b9634-623">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b9634-624">В следующей таблице показано, как значения семейного положения сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b9634-624">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="b9634-625">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="b9634-625">Human Resources</span></span>                 | <span data-ttu-id="b9634-626">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b9634-626">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="b9634-627">Женат/замужем</span><span class="sxs-lookup"><span data-stu-id="b9634-627">Married</span></span>                | <span data-ttu-id="b9634-628">Женат/замужем</span><span class="sxs-lookup"><span data-stu-id="b9634-628">Married</span></span>                   |
| <span data-ttu-id="b9634-629">Один</span><span class="sxs-lookup"><span data-stu-id="b9634-629">Single</span></span>                 | <span data-ttu-id="b9634-630">Один</span><span class="sxs-lookup"><span data-stu-id="b9634-630">Single</span></span>                    |
| <span data-ttu-id="b9634-631">Вдовец/вдова</span><span class="sxs-lookup"><span data-stu-id="b9634-631">Widowed</span></span>                | <span data-ttu-id="b9634-632">Вдовец/вдова</span><span class="sxs-lookup"><span data-stu-id="b9634-632">Widowed</span></span>                   |
| <span data-ttu-id="b9634-633">Разведен/разведена</span><span class="sxs-lookup"><span data-stu-id="b9634-633">Divorced</span></span>               | <span data-ttu-id="b9634-634">Разведен/разведена</span><span class="sxs-lookup"><span data-stu-id="b9634-634">Divorced</span></span>                  |
| <span data-ttu-id="b9634-635">Зарегистрированное партнерство</span><span class="sxs-lookup"><span data-stu-id="b9634-635">Registered Partnership</span></span> | <span data-ttu-id="b9634-636">Партнерство на внутреннем рынке</span><span class="sxs-lookup"><span data-stu-id="b9634-636">Domestic Partnership</span></span>      |
| <span data-ttu-id="b9634-637">None</span><span class="sxs-lookup"><span data-stu-id="b9634-637">None</span></span>                   | <span data-ttu-id="b9634-638">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="b9634-638">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b9634-639">Партнерство</span><span class="sxs-lookup"><span data-stu-id="b9634-639">Cohabiting</span></span>             | <span data-ttu-id="b9634-640">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="b9634-640">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="b9634-641">Род</span><span class="sxs-lookup"><span data-stu-id="b9634-641">Gender</span></span>

<span data-ttu-id="b9634-642">Значения пола сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="b9634-642">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b9634-643">В следующей таблице показано, как значения пола сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b9634-643">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="b9634-644">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="b9634-644">Human Resources</span></span>       | <span data-ttu-id="b9634-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b9634-645">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="b9634-646">Пол сотрудника</span><span class="sxs-lookup"><span data-stu-id="b9634-646">Male</span></span>         | <span data-ttu-id="b9634-647">Пол сотрудника</span><span class="sxs-lookup"><span data-stu-id="b9634-647">Male</span></span>                      |
| <span data-ttu-id="b9634-648">Женский</span><span class="sxs-lookup"><span data-stu-id="b9634-648">Female</span></span>       | <span data-ttu-id="b9634-649">Женский</span><span class="sxs-lookup"><span data-stu-id="b9634-649">Female</span></span>                    |
| <span data-ttu-id="b9634-650">Неопределенный</span><span class="sxs-lookup"><span data-stu-id="b9634-650">Non-specific</span></span> | <span data-ttu-id="b9634-651">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="b9634-651">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="b9634-652">Способ платежа</span><span class="sxs-lookup"><span data-stu-id="b9634-652">Payment method</span></span>

<span data-ttu-id="b9634-653">Методы оплаты предоставляют сотруднику и компании способ описания способа оплаты сотрудников.</span><span class="sxs-lookup"><span data-stu-id="b9634-653">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="b9634-654">Способы оплаты сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="b9634-654">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b9634-655">В следующей таблице показано, как способы оплаты сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b9634-655">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="b9634-656">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="b9634-656">Human Resources</span></span>             | <span data-ttu-id="b9634-657">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b9634-657">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="b9634-658">Касса за </span><span class="sxs-lookup"><span data-stu-id="b9634-658">Cash</span></span>               | <span data-ttu-id="b9634-659">Касса за </span><span class="sxs-lookup"><span data-stu-id="b9634-659">Cash</span></span>                      |
| <span data-ttu-id="b9634-660">Электронный платеж</span><span class="sxs-lookup"><span data-stu-id="b9634-660">Electronic Payment</span></span> | <span data-ttu-id="b9634-661">Перенос</span><span class="sxs-lookup"><span data-stu-id="b9634-661">Transfer</span></span>                  |
| <span data-ttu-id="b9634-662">Проверка</span><span class="sxs-lookup"><span data-stu-id="b9634-662">Check</span></span>              | <span data-ttu-id="b9634-663">Чек</span><span class="sxs-lookup"><span data-stu-id="b9634-663">Cheque</span></span>                    |
| <span data-ttu-id="b9634-664">Банковская тратта</span><span class="sxs-lookup"><span data-stu-id="b9634-664">Bank Draft</span></span>         | <span data-ttu-id="b9634-665">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="b9634-665">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b9634-666">Прочие</span><span class="sxs-lookup"><span data-stu-id="b9634-666">Other</span></span>              | <span data-ttu-id="b9634-667">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="b9634-667">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="b9634-668">Тип банковского счета</span><span class="sxs-lookup"><span data-stu-id="b9634-668">Bank account type</span></span>

<span data-ttu-id="b9634-669">Типы банковских счетов используются для электронных платежей сотрудникам.</span><span class="sxs-lookup"><span data-stu-id="b9634-669">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="b9634-670">Типы банковских счетов сопоставляются с Dayforce как сведения о счетах безналичных расчетов.</span><span class="sxs-lookup"><span data-stu-id="b9634-670">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="b9634-671">Типы банковских счетов переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="b9634-671">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="b9634-672">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="b9634-672">Human Resources</span></span>            | <span data-ttu-id="b9634-673">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b9634-673">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="b9634-674">Чековый счет</span><span class="sxs-lookup"><span data-stu-id="b9634-674">Checking Account</span></span>  | <span data-ttu-id="b9634-675">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="b9634-675">CheckingAccount</span></span>           |
| <span data-ttu-id="b9634-676">Счет зарплаты</span><span class="sxs-lookup"><span data-stu-id="b9634-676">Payroll Account</span></span>   | <span data-ttu-id="b9634-677">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="b9634-677">PayrollAccount</span></span>            |
| <span data-ttu-id="b9634-678">Сберегательный счет</span><span class="sxs-lookup"><span data-stu-id="b9634-678">Savings Account</span></span>   | <span data-ttu-id="b9634-679">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="b9634-679">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b9634-680">Счет BankGirot</span><span class="sxs-lookup"><span data-stu-id="b9634-680">BankGirot account</span></span> | <span data-ttu-id="b9634-681">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="b9634-681">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b9634-682">Счет PlusGirot</span><span class="sxs-lookup"><span data-stu-id="b9634-682">PlusGirot account</span></span> | <span data-ttu-id="b9634-683">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="b9634-683">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="b9634-684">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="b9634-684">Earning codes</span></span>

<span data-ttu-id="b9634-685">Коды доходов уникально определяют каждый типа доходов, которые работники получают.</span><span class="sxs-lookup"><span data-stu-id="b9634-685">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="b9634-686">Эти коды покрывают несколько параметров, которые относятся к доходам, таких как правила учета, налоговые законы, требования к отчетности и возможности брутто в большую сторону.</span><span class="sxs-lookup"><span data-stu-id="b9634-686">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="b9634-687">Если используется неподдерживаемая частота, частота **Каждая оплата** используется по умолчанию для расчета.</span><span class="sxs-lookup"><span data-stu-id="b9634-687">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="b9634-688">Поддерживаемые частоты</span><span class="sxs-lookup"><span data-stu-id="b9634-688">Supported frequencies</span></span>

- <span data-ttu-id="b9634-689">Все</span><span class="sxs-lookup"><span data-stu-id="b9634-689">All</span></span>
- <span data-ttu-id="b9634-690">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="b9634-690">EVERYPAY</span></span>
- <span data-ttu-id="b9634-691">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="b9634-691">EACHPAYPERIOD</span></span>
- <span data-ttu-id="b9634-692">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="b9634-692">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="b9634-693">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="b9634-693">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="b9634-694">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-694">1OFMTH</span></span>
- <span data-ttu-id="b9634-695">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-695">LASTOFMTH</span></span>
- <span data-ttu-id="b9634-696">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-696">2OFMTH</span></span>
- <span data-ttu-id="b9634-697">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-697">3OFMTH</span></span>
- <span data-ttu-id="b9634-698">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-698">4OFMTH</span></span>
- <span data-ttu-id="b9634-699">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-699">5OFMTH</span></span>
- <span data-ttu-id="b9634-700">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-700">1N2OFMTH</span></span>
- <span data-ttu-id="b9634-701">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-701">3N4OFMTH</span></span>
- <span data-ttu-id="b9634-702">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-702">1N3OFMTH</span></span>
- <span data-ttu-id="b9634-703">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-703">1N4OFMTH</span></span>
- <span data-ttu-id="b9634-704">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-704">2N3OFMTH</span></span>
- <span data-ttu-id="b9634-705">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-705">2N4OFMTH</span></span>
- <span data-ttu-id="b9634-706">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-706">1N2N3OFMTH</span></span>
- <span data-ttu-id="b9634-707">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-707">1N2N4OFMTH</span></span>
- <span data-ttu-id="b9634-708">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-708">1N3N4OFMTH</span></span>
- <span data-ttu-id="b9634-709">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-709">2N3N4OFMTH</span></span>
- <span data-ttu-id="b9634-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b9634-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="b9634-711">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="b9634-711">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="b9634-712">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="b9634-712">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="b9634-713">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="b9634-713">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="b9634-714">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="b9634-714">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="b9634-715">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="b9634-715">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="b9634-716">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b9634-716">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="b9634-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b9634-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="b9634-718">Адреса</span><span class="sxs-lookup"><span data-stu-id="b9634-718">Addresses</span></span>

<span data-ttu-id="b9634-719">Идентификация кодов конкретной страны или региона, области и района (муниципалитета) требует определенных форматов, которые Dayforce и поставщики в стране или в регионе могут распознать.</span><span class="sxs-lookup"><span data-stu-id="b9634-719">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="b9634-720">Хотя формат городов гибкий, каждый город должен быть связан с областью.</span><span class="sxs-lookup"><span data-stu-id="b9634-720">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="b9634-721">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="b9634-721">Human Resources</span></span>              | <span data-ttu-id="b9634-722">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b9634-722">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="b9634-723">Страна/регион</span><span class="sxs-lookup"><span data-stu-id="b9634-723">Country/Region</span></span>      | <span data-ttu-id="b9634-724">Код страны</span><span class="sxs-lookup"><span data-stu-id="b9634-724">Country Code</span></span>          |
| <span data-ttu-id="b9634-725">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="b9634-725">Zip/Postal Code</span></span>     | <span data-ttu-id="b9634-726">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="b9634-726">Postal Code</span></span>           |
| <span data-ttu-id="b9634-727">Область, край</span><span class="sxs-lookup"><span data-stu-id="b9634-727">State</span></span>               | <span data-ttu-id="b9634-728">Код региона</span><span class="sxs-lookup"><span data-stu-id="b9634-728">State Code</span></span>            |
| <span data-ttu-id="b9634-729">Город</span><span class="sxs-lookup"><span data-stu-id="b9634-729">City</span></span>                | <span data-ttu-id="b9634-730">Город</span><span class="sxs-lookup"><span data-stu-id="b9634-730">City</span></span>                  |
| <span data-ttu-id="b9634-731">Округ</span><span class="sxs-lookup"><span data-stu-id="b9634-731">County</span></span>              | <span data-ttu-id="b9634-732">Район (муниципалитет)</span><span class="sxs-lookup"><span data-stu-id="b9634-732">County (Municipality)</span></span> |
| <span data-ttu-id="b9634-733">Улица</span><span class="sxs-lookup"><span data-stu-id="b9634-733">Street</span></span>              | <span data-ttu-id="b9634-734">Строка адреса 1</span><span class="sxs-lookup"><span data-stu-id="b9634-734">Address Line 1</span></span>        |
| <span data-ttu-id="b9634-735">Номер дома</span><span class="sxs-lookup"><span data-stu-id="b9634-735">Street Number</span></span>       | <span data-ttu-id="b9634-736">Строка адреса 2</span><span class="sxs-lookup"><span data-stu-id="b9634-736">Address Line 2</span></span>        |
| <span data-ttu-id="b9634-737">Дополнение здания</span><span class="sxs-lookup"><span data-stu-id="b9634-737">Building Complement</span></span> | <span data-ttu-id="b9634-738">Строка адреса 5</span><span class="sxs-lookup"><span data-stu-id="b9634-738">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="b9634-739">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="b9634-739">Passport number</span></span>

<span data-ttu-id="b9634-740">Сотрудники могут объявить данные паспорта.</span><span class="sxs-lookup"><span data-stu-id="b9634-740">Employees can declare passport information.</span></span> <span data-ttu-id="b9634-741">Эта информация имеет тип идентификации **Паспорт** и интегрируется в Dayforce как часть сведений о сотруднике, специфических для Мексики.</span><span class="sxs-lookup"><span data-stu-id="b9634-741">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="b9634-742">Тип идентификации = "Паспорт"</span><span class="sxs-lookup"><span data-stu-id="b9634-742">Identification Type = "Passport"</span></span>
- <span data-ttu-id="b9634-743">Дата выпуска</span><span class="sxs-lookup"><span data-stu-id="b9634-743">Issued Date</span></span>
- <span data-ttu-id="b9634-744">Дата окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="b9634-744">Expiration Date</span></span>

<span data-ttu-id="b9634-745">Сотрудники могут объявить несколько идентификационных номеров для типа идентификатора **Паспорт**.</span><span class="sxs-lookup"><span data-stu-id="b9634-745">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="b9634-746">Тем не менее только запись текущего активного паспорта интегрируется в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b9634-746">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="b9634-747">Если срок действия всех записей паспорта истек, в Dayforce интегрируется тот, который был выдан последним.</span><span class="sxs-lookup"><span data-stu-id="b9634-747">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

