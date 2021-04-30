---
title: Настройка интеграции с Dayforce
description: Интеграция между Microsoft Dynamics 365 Human Resources и Ceridian Dayforce зависит от ряда действий настройки, описанных в этой статье. Необходимо настроить интеграцию в Human Resources и Dayforce перед обработкой периода оплаты.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 1647b7fbf84a78051e745e918954df32a2e7e1dd
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890012"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="2b1e1-104">Настройка интеграции с Dayforce</span><span class="sxs-lookup"><span data-stu-id="2b1e1-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2b1e1-105">Интеграция между Microsoft Dynamics 365 Human Resources и Ceridian Dayforce зависит от ряда действий настройки, описанных в этой статье.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="2b1e1-106">Необходимо настроить интеграцию в Human Resources и Dayforce перед обработкой периода оплаты.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="2b1e1-107">При использовании службы, например Dayforce, для выполнения оплаты, необходимо включить интеграцию в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="2b1e1-108">Интеграция требует определенных данных из Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="2b1e1-109">Таким образом необходимо убедиться, что данные, отображаемые в Dayforce, настроены в Human Resources таким образом, чтобы поддерживать интеграцию.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="2b1e1-110">Интеграция использует следующие широкие категории данных:</span><span class="sxs-lookup"><span data-stu-id="2b1e1-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="2b1e1-111">Данные управления персоналом</span><span class="sxs-lookup"><span data-stu-id="2b1e1-111">Human resources data</span></span>
- <span data-ttu-id="2b1e1-112">Данные о компенсациях</span><span class="sxs-lookup"><span data-stu-id="2b1e1-112">Compensation data</span></span>
- <span data-ttu-id="2b1e1-113">Данные о заработной плате, например циклы оплаты, периоды оплаты и коды начисления зарплаты</span><span class="sxs-lookup"><span data-stu-id="2b1e1-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="2b1e1-114">Данные о работнике</span><span class="sxs-lookup"><span data-stu-id="2b1e1-114">Worker data</span></span>

<span data-ttu-id="2b1e1-115">В этой статье описываются шаги, которые необходимо выполнить, чтобы включить интеграцию.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="2b1e1-116">Здесь также объясняются типы данных и сведения о конфигурации, которые необходимы для интеграции.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="2b1e1-117">Включение интеграции</span><span class="sxs-lookup"><span data-stu-id="2b1e1-117">Enable the integration</span></span>

<span data-ttu-id="2b1e1-118">В Human Resources необходимо включить интеграцию и ввести информацию о конфигурации для подключения к Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="2b1e1-119">Если требуется, чтобы проводки ГК, которые производятся, импортировались в Microsoft Dynamics 365 Finance, также необходимо установить учетную запись хранилища Microsoft Azure и ввести строку подключения хранилища Azure в Finance.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="2b1e1-120">Чтобы включить интеграцию в Human Resources, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="2b1e1-121">На странице **Администрирование системы** выберите **Конфигурация интеграции**.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="2b1e1-122">Введите безопасную конечную точку FTP и путь к безопасной папке FTP.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="2b1e1-123">Введите имя пользователя и пароль пользователя, который будет иметь доступ к безопасной конечной точке и пути к папке FTP.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="2b1e1-124">Проверьте подключение, как требуется, а также установите для параметра **Включить интеграцию зарплаты** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="2b1e1-125">При включении интеграции создаются пакет экспорта данных и файлы, и задается значение частоты.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="2b1e1-126">Можно изменить эту частоту, как требуется.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="2b1e1-127">Дополнительные сведения об учетных записях хранилища Azure и строке подключения хранилища Azure см. в следующих статьях Azure:</span><span class="sxs-lookup"><span data-stu-id="2b1e1-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="2b1e1-128">Об учетных записях хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="2b1e1-128">About Azure storage accounts</span></span>](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="2b1e1-129">Настройка строки подключения хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="2b1e1-129">Configure Azure Storage connection strings</span></span>](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="2b1e1-130">Технические сведения о включении интеграции зарплаты</span><span class="sxs-lookup"><span data-stu-id="2b1e1-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="2b1e1-131">Включение интеграции зарплаты имеет два основных эффекта:</span><span class="sxs-lookup"><span data-stu-id="2b1e1-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="2b1e1-132">Будет создан проект экспорта данных с именем "Экспорт интеграции зарплаты".</span><span class="sxs-lookup"><span data-stu-id="2b1e1-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="2b1e1-133">Этот проект содержит сущности и поля, необходимые для интеграции зарплаты.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="2b1e1-134">Чтобы проверить этот проект, перейдите в раздел **Администрирование системы**, выберите плитку **Управление данными**, затем откройте проект данных из списка проектов.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="2b1e1-135">Это пакетное задание выполняет проект экспорта данных, шифрует получившийся пакет данных и передает файл пакета данных на конечную точку SFTP, настроенную на экране **Конфигурация интеграции**.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="2b1e1-136">Пакет данных, переданный в конечную точку SFTP, шифруется с помощью уникального для пакета ключа.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="2b1e1-137">Ключ находится в хранилище ключей Azure Key Vault, доступном только для по Ceridian.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="2b1e1-138">Невозможно расшифровать и проверить содержимое пакета данных.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="2b1e1-139">Если необходимо изучить содержимое пакета данных, необходимо экспортировать проект данных "Экспорт интеграции зарплаты" вручную, загрузить его и затем открыть.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="2b1e1-140">При экспорте вручную шифрование или передача пакетов не применяются.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-140">Manual export will not apply encryption or transfer the package.</span></span>
> <span data-ttu-id="2b1e1-141">Для экземпляров, когда файлы интеграции отправляются из среды UAT или "песочницы" Dynamics 365 Human Resources в среду тестирования Ceridian Dayforce, можно использовать следующий URL-адрес хранилища ключей: https://payrollintegrationprod.vault.azure.net.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-141">For instances where the integration files are sent from a Dynamics 365 Human Resources UAT or Sandbox environment to a Ceridian Dayforce Test environment, you can use the following key vault URL: https://payrollintegrationprod.vault.azure.net.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="2b1e1-142">Настройка данных</span><span class="sxs-lookup"><span data-stu-id="2b1e1-142">Configure your data</span></span> 

<span data-ttu-id="2b1e1-143">Для обработки зарплаты необходимо настроить данные управления персоналом в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-143">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="2b1e1-144">Необходимо настроить организационные данные, такие как задания и должности, вместе со сведениями о льготах и компенсациях.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-144">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="2b1e1-145">Эта информация содержит сведения о занятости, оплате и вычетах, которые необходимы для формирования заработной платы сотрудника.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-145">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="2b1e1-146">Данные управления персоналом</span><span class="sxs-lookup"><span data-stu-id="2b1e1-146">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="2b1e1-147">Льготы</span><span class="sxs-lookup"><span data-stu-id="2b1e1-147">Benefits</span></span> 

<span data-ttu-id="2b1e1-148">Человеческие ресурсы обеспечивают инструменты для настройки и поддержки льгот, вычетов и планов компенсации работникам, которые организация предлагает или обрабатывает для своих работников.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-148">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="2b1e1-149">При создании льгот имейте в виду следующие данные и конфигурации, которые используются в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-149">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="2b1e1-150">Планы льгот</span><span class="sxs-lookup"><span data-stu-id="2b1e1-150">Benefit plans</span></span>

- <span data-ttu-id="2b1e1-151">План (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-151">Plan (required)</span></span>
- <span data-ttu-id="2b1e1-152">Тип (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-152">Type (required)</span></span>
- <span data-ttu-id="2b1e1-153">Влияние на зарплату (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-153">Payroll impact (required)</span></span>
- <span data-ttu-id="2b1e1-154">Погасить задолженность</span><span class="sxs-lookup"><span data-stu-id="2b1e1-154">Recover arrears</span></span>
- <span data-ttu-id="2b1e1-155">Метод вычета</span><span class="sxs-lookup"><span data-stu-id="2b1e1-155">Deduction method</span></span>
- <span data-ttu-id="2b1e1-156">Приоритет вычета</span><span class="sxs-lookup"><span data-stu-id="2b1e1-156">Deduction priority</span></span>
- <span data-ttu-id="2b1e1-157">Период лимита</span><span class="sxs-lookup"><span data-stu-id="2b1e1-157">Limit period</span></span>
- <span data-ttu-id="2b1e1-158">Сумма лимита</span><span class="sxs-lookup"><span data-stu-id="2b1e1-158">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="2b1e1-159">Льготы</span><span class="sxs-lookup"><span data-stu-id="2b1e1-159">Benefits</span></span>

- <span data-ttu-id="2b1e1-160">План (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-160">Plan (required)</span></span>
- <span data-ttu-id="2b1e1-161">Тип (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-161">Type (required)</span></span>
- <span data-ttu-id="2b1e1-162">Параметр (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-162">Option (required)</span></span>
- <span data-ttu-id="2b1e1-163">Код льготы (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-163">Benefit ID (required)</span></span>
- <span data-ttu-id="2b1e1-164">Частота</span><span class="sxs-lookup"><span data-stu-id="2b1e1-164">Frequency</span></span>
- <span data-ttu-id="2b1e1-165">База</span><span class="sxs-lookup"><span data-stu-id="2b1e1-165">Basis</span></span>
- <span data-ttu-id="2b1e1-166">Сумма или ставка</span><span class="sxs-lookup"><span data-stu-id="2b1e1-166">Amount or rate</span></span>
- <span data-ttu-id="2b1e1-167">Код дохода</span><span class="sxs-lookup"><span data-stu-id="2b1e1-167">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="2b1e1-168">Поддерживаемые частоты</span><span class="sxs-lookup"><span data-stu-id="2b1e1-168">Supported frequencies</span></span> 

- <span data-ttu-id="2b1e1-169">Еженедельно</span><span class="sxs-lookup"><span data-stu-id="2b1e1-169">Weekly</span></span>
- <span data-ttu-id="2b1e1-170">Один раз в две недели</span><span class="sxs-lookup"><span data-stu-id="2b1e1-170">Bi-weekly</span></span>
- <span data-ttu-id="2b1e1-171">Два раза в месяц</span><span class="sxs-lookup"><span data-stu-id="2b1e1-171">Semi-monthly</span></span>
- <span data-ttu-id="2b1e1-172">Один раз в месяц</span><span class="sxs-lookup"><span data-stu-id="2b1e1-172">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="2b1e1-173">Поддерживаемые базы</span><span class="sxs-lookup"><span data-stu-id="2b1e1-173">Supported bases</span></span> 

- <span data-ttu-id="2b1e1-174">Фиксированная сумма</span><span class="sxs-lookup"><span data-stu-id="2b1e1-174">Fixed amount</span></span>
- <span data-ttu-id="2b1e1-175">Процент дохода</span><span class="sxs-lookup"><span data-stu-id="2b1e1-175">Percent of earnings</span></span>
- <span data-ttu-id="2b1e1-176">Продуктивные часы</span><span class="sxs-lookup"><span data-stu-id="2b1e1-176">Productive hours</span></span>

<span data-ttu-id="2b1e1-177">Dayforce создает следующие вычеты на основе влияния на зарплату, которое определено в плане льгот.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-177">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="2b1e1-178">Выбор в Human Resources</span><span class="sxs-lookup"><span data-stu-id="2b1e1-178">Selection in Human Resources</span></span>        | <span data-ttu-id="2b1e1-179">Результат в Dayforce</span><span class="sxs-lookup"><span data-stu-id="2b1e1-179">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="2b1e1-180">Нет</span><span class="sxs-lookup"><span data-stu-id="2b1e1-180">None</span></span>                       | <span data-ttu-id="2b1e1-181">Вычет не создается.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-181">No deduction is created.</span></span>                      |
| <span data-ttu-id="2b1e1-182">Только удержание</span><span class="sxs-lookup"><span data-stu-id="2b1e1-182">Deduction only</span></span>             | <span data-ttu-id="2b1e1-183">Вычет сотрудника будет создан.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-183">An employee deduction is created.</span></span>             |
| <span data-ttu-id="2b1e1-184">Только вклад</span><span class="sxs-lookup"><span data-stu-id="2b1e1-184">Contribution only</span></span>          | <span data-ttu-id="2b1e1-185">Вычет работодателя будет создан.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-185">An employer deduction is created.</span></span>             |
| <span data-ttu-id="2b1e1-186">Удержание и вклад</span><span class="sxs-lookup"><span data-stu-id="2b1e1-186">Deduction and contribution</span></span> | <span data-ttu-id="2b1e1-187">Создаются вычеты сотрудников и работодателя.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-187">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="2b1e1-188">Дополнительные сведения о том, как определять и управлять программами льгот, см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="2b1e1-188">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="2b1e1-189">Реализация программы льгот сотрудника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-189">Deliver an employee benefits program</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="2b1e1-190">Создать новую льготу</span><span class="sxs-lookup"><span data-stu-id="2b1e1-190">Create a new benefit</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="2b1e1-191">Определение правил и политик проверки прав на льготы</span><span class="sxs-lookup"><span data-stu-id="2b1e1-191">Define benefit eligibility rules and policies</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="2b1e1-192">Регистрация и удаление льгот для работников</span><span class="sxs-lookup"><span data-stu-id="2b1e1-192">Enroll and remove benefits from workers</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="2b1e1-193">Компенсация</span><span class="sxs-lookup"><span data-stu-id="2b1e1-193">Compensation</span></span> 

<span data-ttu-id="2b1e1-194">Управление компенсациями используется для управления предоставлением базовой оплаты и вознаграждений.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-194">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="2b1e1-195">Тарифные ставки и единовременные надбавки контролируются с помощью планов фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-195">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="2b1e1-196">Поощрительные выплаты, такие как премии, вознаграждения за производительность, опционы на покупку акций и гранты, а также одноразовые компенсации, контролируются с помощью планов переменных компенсаций.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-196">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="2b1e1-197">Dayforce использует сведения о компенсации для расчета почасовой или годовой ставки сотрудника.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-197">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="2b1e1-198">Требуются планы фиксированной компенсации и преобразования ставки оплаты.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-198">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="2b1e1-199">Сотрудники должны быть связаны с планом фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-199">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="2b1e1-200">Дополнительные сведения о планах компенсации см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="2b1e1-200">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="2b1e1-201">Создание планов фиксированной компенсации</span><span class="sxs-lookup"><span data-stu-id="2b1e1-201">Create fixed compensation plans</span></span>](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="2b1e1-202">Создание планов переменной компенсации</span><span class="sxs-lookup"><span data-stu-id="2b1e1-202">Create variable compensation plans</span></span>](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="2b1e1-203">Разработка структуры и планов зарплаты/компенсации</span><span class="sxs-lookup"><span data-stu-id="2b1e1-203">Develop salary/compensation structure and plans</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="2b1e1-204">Обработка компенсаций</span><span class="sxs-lookup"><span data-stu-id="2b1e1-204">Process compensation</span></span>](/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="2b1e1-205">Определение процесса компенсации и расчет результатов</span><span class="sxs-lookup"><span data-stu-id="2b1e1-205">Define compensation process and calculate results</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="2b1e1-206">Включение сотрудника в план фиксированных компенсаций</span><span class="sxs-lookup"><span data-stu-id="2b1e1-206">Enroll an employee in a fixed compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="2b1e1-207">Включение сотрудника в план переменных компенсаций</span><span class="sxs-lookup"><span data-stu-id="2b1e1-207">Enroll an employee in a variable compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="2b1e1-208">Должности</span><span class="sxs-lookup"><span data-stu-id="2b1e1-208">Jobs</span></span> 

<span data-ttu-id="2b1e1-209">Должностные обязанности — это набор задач и обязанностей, которые возлагаются на занимающее эту задание лицо.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-209">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="2b1e1-210">Дополнительные сведения см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="2b1e1-210">For more information, see the following articles:</span></span>

- [<span data-ttu-id="2b1e1-211">Настройка компонентов должности</span><span class="sxs-lookup"><span data-stu-id="2b1e1-211">Setting up the components of a job</span></span>](/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="2b1e1-212">Определение новых должностей</span><span class="sxs-lookup"><span data-stu-id="2b1e1-212">Define new jobs</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="2b1e1-213">Позиции</span><span class="sxs-lookup"><span data-stu-id="2b1e1-213">Positions</span></span>

<span data-ttu-id="2b1e1-214">Позиция — это индивидуальный экземпляр должности.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-214">A position is an individual instance of a job.</span></span> <span data-ttu-id="2b1e1-215">Например, должность "Менеджер по продажам (восток)" — это одна из должностей, связанных с должностными обязанностями "Менеджер по продажам".</span><span class="sxs-lookup"><span data-stu-id="2b1e1-215">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="2b1e1-216">Должность существует в отделе.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-216">A position exists in a department.</span></span> <span data-ttu-id="2b1e1-217">Только один работник может быть связан с каждой должностью.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-217">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="2b1e1-218">Учитывайте следующие данные и конфигурацию при настройке должностей:</span><span class="sxs-lookup"><span data-stu-id="2b1e1-218">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="2b1e1-219">Должность (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-219">Position (required)</span></span>
- <span data-ttu-id="2b1e1-220">Описание (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-220">Description (required)</span></span>
- <span data-ttu-id="2b1e1-221">Должностные обязанности (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-221">Job (required)</span></span>
- <span data-ttu-id="2b1e1-222">Отдел (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-222">Department (required)</span></span>
- <span data-ttu-id="2b1e1-223">Тип должности (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-223">Position type (required)</span></span>
- <span data-ttu-id="2b1e1-224">Эквивалент полной занятости</span><span class="sxs-lookup"><span data-stu-id="2b1e1-224">Full-time equivalent</span></span>
- <span data-ttu-id="2b1e1-225">Обычные часы за год (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-225">Annual regular hours (required)</span></span>
- <span data-ttu-id="2b1e1-226">Оплачивается юридическим лицом (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-226">Paid by legal entity (required)</span></span>
- <span data-ttu-id="2b1e1-227">Цикл оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-227">Pay cycle (required)</span></span>
- <span data-ttu-id="2b1e1-228">Финансовая аналитика по умолчанию — центр затрат (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-228">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="2b1e1-229">Назначение работника — работник, начало назначения, окончание назначения, код причины</span><span class="sxs-lookup"><span data-stu-id="2b1e1-229">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="2b1e1-230">Если несколько должностей в одном отделе связаны с одними и теми же должностными обязанностями, они объединяются в одну должность в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-230">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="2b1e1-231">Дополнительные сведения см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="2b1e1-231">For more information, see the following articles:</span></span>

- [<span data-ttu-id="2b1e1-232">Организация трудовых ресурсов с использованием подразделений, должностей и штатных единиц</span><span class="sxs-lookup"><span data-stu-id="2b1e1-232">Organize your workforce using departments, jobs, and positions</span></span>](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="2b1e1-233">Настройка должностей</span><span class="sxs-lookup"><span data-stu-id="2b1e1-233">Set up positions</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="2b1e1-234">Отделы</span><span class="sxs-lookup"><span data-stu-id="2b1e1-234">Departments</span></span>

<span data-ttu-id="2b1e1-235">Подразделение — это операционная единица, которая представляет собой категорию или функциональную область в организации.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-235">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="2b1e1-236">Подразделение отвечает за конкретную область деятельности организации, например продажи, бухгалтерский учет или управление персоналом.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-236">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="2b1e1-237">Подразделения можно использовать для формирования отчетности по функциональным областям.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-237">You can use departments to report on functional areas.</span></span> <span data-ttu-id="2b1e1-238">Подразделения могут нести ответственность за прибыли и убытки.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-238">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="2b1e1-239">Дополнительные сведения см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="2b1e1-239">For more information, see the following articles:</span></span>

- [<span data-ttu-id="2b1e1-240">Создание подразделения и связывание его с иерархией подразделений</span><span class="sxs-lookup"><span data-stu-id="2b1e1-240">Create a department and associate it with the department hierarchy</span></span>](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="2b1e1-241">Определение новых подразделений</span><span class="sxs-lookup"><span data-stu-id="2b1e1-241">Define new departments</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="2b1e1-242">Циклы оплаты и платежные периоды</span><span class="sxs-lookup"><span data-stu-id="2b1e1-242">Pay cycles and pay periods</span></span>

<span data-ttu-id="2b1e1-243">Цикл оплаты определяет, как часто рассчитывается зарплата и определенные дни, когда работники получают зарплату.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-243">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="2b1e1-244">Например, цикл оплаты может быть ежемесячным, и сотрудникам может выплачиваться зарплата в последний день месяца.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-244">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="2b1e1-245">Кроме того, цикл оплаты может быть еженедельным, а сотрудники могут получать зарплату по вторникам после завершения периода оплаты.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-245">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="2b1e1-246">Циклы оплаты назначаются должностям для управления выплатами работникам для этих должностей.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-246">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="2b1e1-247">После создания циклов зарплаты можно создать платежные периоды для каждого цикла.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-247">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="2b1e1-248">Каждый платежный период включает дату оплаты по умолчанию, которая основана на информации, предоставленной вами.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-248">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="2b1e1-249">Однако можно изменить дату платежа по умолчанию в платежный период для учета исключений, например, когда дата оплаты приходится на праздник.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-249">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="2b1e1-250">Dayforce использует следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="2b1e1-250">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="2b1e1-251">Цикл оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-251">Pay cycle (required)</span></span>
- <span data-ttu-id="2b1e1-252">Частота циклов оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-252">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="2b1e1-253">Дата начала периода (первый период оплаты обязателен)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-253">Period start date (first pay period required)</span></span>
- <span data-ttu-id="2b1e1-254">Дата платежа по умолчанию (первый период оплаты обязателен)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-254">Default payment date (first pay period required)</span></span>

<span data-ttu-id="2b1e1-255">Эта информация интегрирована с Dayforce как платежные группы, и разделяется по странам или регионам для каждого цикла оплаты.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-255">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="2b1e1-256">Хотя бы один платежный период должен быть создан до интеграции.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-256">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="2b1e1-257">Dayforce создает календари группы оплаты и даты оплаты на основе даты начала первого периода оплаты и даты оплаты по умолчанию, настроенных в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-257">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="2b1e1-258">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="2b1e1-258">Earning codes</span></span>

<span data-ttu-id="2b1e1-259">Коды доходов уникально определяют каждый типа доходов, которые работники получают.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-259">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="2b1e1-260">Эти коды имеют различные параметры, которые относятся к доходам, таких как правила учета, налоговые законы, требования к отчетности и возможности брутто в большую сторону.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-260">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="2b1e1-261">Dayforce использует следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="2b1e1-261">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="2b1e1-262">Код дохода (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-262">Earning Code (required)</span></span>
- <span data-ttu-id="2b1e1-263">описание</span><span class="sxs-lookup"><span data-stu-id="2b1e1-263">Description</span></span>
- <span data-ttu-id="2b1e1-264">Единица измерения</span><span class="sxs-lookup"><span data-stu-id="2b1e1-264">Unit of measure</span></span>
- <span data-ttu-id="2b1e1-265">Продуктивный</span><span class="sxs-lookup"><span data-stu-id="2b1e1-265">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="2b1e1-266">Данные о работнике</span><span class="sxs-lookup"><span data-stu-id="2b1e1-266">Worker data</span></span>

<span data-ttu-id="2b1e1-267">Записи о различных типах сотрудников, которые имеются у вас, важны для вашей системы управления персоналом и системы расчета заработной платы.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-267">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="2b1e1-268">Вводимые данные могут использоваться для отслеживания сведений о работниках и личной информации.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-268">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="2b1e1-269">По работникам может храниться следующая информация.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-269">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="2b1e1-270">**Основная** — базовые сведения о работнике, такие как контактные данные, демографические данные, идентифицирующие сведения, состав семье, сведения о службе в армии, данные об иностранных сотрудниках, персональные контакты и контакты на случай экстренных ситуаций.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-270">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="2b1e1-271">**Занятость** — сведения о занятости работников, такие как участие в компании или организации, должность, дату начала и завершения работы, способность к работе, условия найма, пенсия, отпуска и сведения о переездах.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-271">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="2b1e1-272">**Отпуск и отсутствие** — сведения об отпусках или пропуска работника, рабочие календари, проводки отсутствия и соответствующие настройки.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-272">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="2b1e1-273">**Заработная плата и компенсации** — сведения о планах вознаграждениях и зарплате работника, такие как премии, комиссии, налоги, выход на пенсию и вычеты из зарплаты.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-273">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="2b1e1-274">При вводе сведений о работнике имейте в виду следующие данные и конфигурации, которые используются в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-274">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="2b1e1-275">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="2b1e1-275">General information</span></span>

- <span data-ttu-id="2b1e1-276">Табельный номер (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-276">Personnel number (required)</span></span>
- <span data-ttu-id="2b1e1-277">Имя (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-277">First name (required)</span></span>
- <span data-ttu-id="2b1e1-278">Фамилия (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-278">Last name (required)</span></span>
- <span data-ttu-id="2b1e1-279">Отчество</span><span class="sxs-lookup"><span data-stu-id="2b1e1-279">Middle name</span></span>
- <span data-ttu-id="2b1e1-280">Дата начала стажа</span><span class="sxs-lookup"><span data-stu-id="2b1e1-280">Seniority date</span></span>
- <span data-ttu-id="2b1e1-281">Известно как</span><span class="sxs-lookup"><span data-stu-id="2b1e1-281">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="2b1e1-282">Личная информация</span><span class="sxs-lookup"><span data-stu-id="2b1e1-282">Personal information</span></span>

- <span data-ttu-id="2b1e1-283">Семейное положение (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-283">Marital status (required)</span></span>
- <span data-ttu-id="2b1e1-284">Дата рождения (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-284">Birth date (required)</span></span>
- <span data-ttu-id="2b1e1-285">Пол (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-285">Gender (required)</span></span>
- <span data-ttu-id="2b1e1-286">Лицо с инвалидностью</span><span class="sxs-lookup"><span data-stu-id="2b1e1-286">Person with disabilities</span></span>
- <span data-ttu-id="2b1e1-287">Национальность, регион страны (только в Мексике)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-287">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="2b1e1-288">Адресная информация</span><span class="sxs-lookup"><span data-stu-id="2b1e1-288">Address information</span></span>

- <span data-ttu-id="2b1e1-289">Основной (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-289">Primary (required)</span></span>
- <span data-ttu-id="2b1e1-290">Страна/регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-290">Country/region (required)</span></span>
- <span data-ttu-id="2b1e1-291">Почтовый индекс (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-291">Postal code (required)</span></span>
- <span data-ttu-id="2b1e1-292">Номер дома (обязательно) (только для Мексики)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-292">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="2b1e1-293">Дополнение здания (только в Мексике)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-293">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="2b1e1-294">Город (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-294">City (required)</span></span>
- <span data-ttu-id="2b1e1-295">Регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-295">State (required)</span></span>
- <span data-ttu-id="2b1e1-296">Район (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-296">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="2b1e1-297">Контактная информация</span><span class="sxs-lookup"><span data-stu-id="2b1e1-297">Contact information</span></span> 

- <span data-ttu-id="2b1e1-298">Основной (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-298">Primary (required)</span></span>
- <span data-ttu-id="2b1e1-299">Контактный номер (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-299">Contact number (required)</span></span>
- <span data-ttu-id="2b1e1-300">Расширение</span><span class="sxs-lookup"><span data-stu-id="2b1e1-300">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="2b1e1-301">Информация по зарплате и коды дохода</span><span class="sxs-lookup"><span data-stu-id="2b1e1-301">Payroll information and earning codes</span></span>

<span data-ttu-id="2b1e1-302">Сотрудникам можно назначить конкретные доходы с заданной периодичностью оплаты и предпочтительный метод оплаты.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-302">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="2b1e1-303">Следующие поля используются в Dayforce для обеспечения использования этих параметров и настроек.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-303">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="2b1e1-304">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="2b1e1-304">Earning codes</span></span>

- <span data-ttu-id="2b1e1-305">Должность (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-305">Position (required)</span></span>
- <span data-ttu-id="2b1e1-306">Код дохода (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-306">Earning Code (required)</span></span>
- <span data-ttu-id="2b1e1-307">Частота (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-307">Frequency (required)</span></span>
- <span data-ttu-id="2b1e1-308">Сумма (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-308">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="2b1e1-309">Информация по зарплате</span><span class="sxs-lookup"><span data-stu-id="2b1e1-309">Payroll information</span></span>

- <span data-ttu-id="2b1e1-310">Способ оплаты</span><span class="sxs-lookup"><span data-stu-id="2b1e1-310">Payment Method</span></span>
- <span data-ttu-id="2b1e1-311">Экономический регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-311">Economic Region (required)</span></span>
- <span data-ttu-id="2b1e1-312">ИД льгот сотрудников</span><span class="sxs-lookup"><span data-stu-id="2b1e1-312">Employee Benefits ID</span></span>
- <span data-ttu-id="2b1e1-313">Идентификационный номер (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-313">National ID Number (required)</span></span>
- <span data-ttu-id="2b1e1-314">Номер документа о воинской службе</span><span class="sxs-lookup"><span data-stu-id="2b1e1-314">Military Service Number</span></span>
- <span data-ttu-id="2b1e1-315">Код смены (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-315">Shift ID (required)</span></span>
- <span data-ttu-id="2b1e1-316">Налоговой номер (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-316">Tax Number (required)</span></span>
- <span data-ttu-id="2b1e1-317">Код профсоюза (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-317">Union ID (required)</span></span>
- <span data-ttu-id="2b1e1-318">Идентификатор рабочего дня (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-318">Work Day ID (required)</span></span>
- <span data-ttu-id="2b1e1-319">Номер разрешения на работу</span><span class="sxs-lookup"><span data-stu-id="2b1e1-319">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="2b1e1-320">Для метода оплаты в Мексике поддерживает **Наличные деньги**, **Чек** (физический чек компании) и **Электронный платеж**.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-320">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="2b1e1-321">Если способ оплаты не указан, **Чек** используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-321">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="2b1e1-322">Сведения о трудоустройстве</span><span class="sxs-lookup"><span data-stu-id="2b1e1-322">Employment details</span></span>

<span data-ttu-id="2b1e1-323">Подробная история занятости используется как ключевая информация для извлечения статуса найма, увольнения и повторного найма сотрудника в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-323">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="2b1e1-324">Dayforce поддерживает только одну активную запись о приеме на работу одновременно.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-324">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="2b1e1-325">Дата начала трудоустройства (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-325">Employment start date (required)</span></span>
- <span data-ttu-id="2b1e1-326">Дата окончания занятости</span><span class="sxs-lookup"><span data-stu-id="2b1e1-326">Employment end date</span></span>
- <span data-ttu-id="2b1e1-327">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="2b1e1-327">Start date</span></span>
- <span data-ttu-id="2b1e1-328">Скорректированная дата приема на работу</span><span class="sxs-lookup"><span data-stu-id="2b1e1-328">Adjusted start date</span></span>
- <span data-ttu-id="2b1e1-329">Дата увольнения (обязательно после увольнения)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-329">Termination date (required upon termination)</span></span>
- <span data-ttu-id="2b1e1-330">Причина увольнения (обязательно после увольнения)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-330">Termination reason (required upon termination)</span></span>

<span data-ttu-id="2b1e1-331">Ключевые даты сотрудника получаются на основе следующих сведений.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-331">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="2b1e1-332">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="2b1e1-332">Human Resources</span></span>                | <span data-ttu-id="2b1e1-333">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2b1e1-333">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b1e1-334">Самая последняя дата приема на работу</span><span class="sxs-lookup"><span data-stu-id="2b1e1-334">Most recent hire date</span></span> | <span data-ttu-id="2b1e1-335">Дата приема на работу для текущей записи истории занятости, которая еще не завершена</span><span class="sxs-lookup"><span data-stu-id="2b1e1-335">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="2b1e1-336">Дата увольнения</span><span class="sxs-lookup"><span data-stu-id="2b1e1-336">Termination date</span></span>      | <span data-ttu-id="2b1e1-337">Дата увольнения для текущей записи истории занятости, которая еще не завершена</span><span class="sxs-lookup"><span data-stu-id="2b1e1-337">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="2b1e1-338">Начальная дата</span><span class="sxs-lookup"><span data-stu-id="2b1e1-338">Start date</span></span>            | <span data-ttu-id="2b1e1-339">Скорректированная дата приема на работу, дата приема на работу или дата приема на работу текущей неактивной записи история занятости</span><span class="sxs-lookup"><span data-stu-id="2b1e1-339">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="2b1e1-340">Дата первоначального приема на работу</span><span class="sxs-lookup"><span data-stu-id="2b1e1-340">Original hire date</span></span>    | <span data-ttu-id="2b1e1-341">Дата приема на работу самой ранней записи истории приема на работу</span><span class="sxs-lookup"><span data-stu-id="2b1e1-341">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="2b1e1-342">Компенсация</span><span class="sxs-lookup"><span data-stu-id="2b1e1-342">Compensation</span></span>

<span data-ttu-id="2b1e1-343">План фиксированной компенсации должен быть связан с каждой основной должностью работника на протяжении всего периода занятости.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-343">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="2b1e1-344">Этот период начинается на даты, в которую сотрудник был нанят (или начальная дата приема на работу) и продолжается до увольнения.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-344">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="2b1e1-345">Дата вступления в силу (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-345">Effective Date (required)</span></span>
- <span data-ttu-id="2b1e1-346">Срок действия</span><span class="sxs-lookup"><span data-stu-id="2b1e1-346">Expiration date</span></span>
- <span data-ttu-id="2b1e1-347">Ставка оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-347">Pay Rate (required)</span></span>
- <span data-ttu-id="2b1e1-348">Преобразования ставки оплаты (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-348">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="2b1e1-349">Годовой эквивалент (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-349">Annual equivalent (required)</span></span>
- <span data-ttu-id="2b1e1-350">Почасовой эквивалент (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-350">Hourly equivalent (required)</span></span>

<span data-ttu-id="2b1e1-351">Если сотрудник с почасовой оплатой имеет несколько должностей, фиксированная компенсация основной должности импортируется в Dayforce как базовая ставка/зарплата уровня сотрудника.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-351">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="2b1e1-352">Дня неосновных должностей почасовая ставка сохраняется в соответствующей должности в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-352">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="2b1e1-353">Если штатный сотрудник имеет несколько должностей, суммарная почасовая ставка и годовая заработная плата для всех активных должностей определяется и используется в качестве базовой ставки/зарплаты уровня сотрудника.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-353">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="2b1e1-354">Идентификационные номера</span><span class="sxs-lookup"><span data-stu-id="2b1e1-354">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="2b1e1-355">Код социального страхования</span><span class="sxs-lookup"><span data-stu-id="2b1e1-355">Social Security identifier</span></span> 

<span data-ttu-id="2b1e1-356">Каждый сотрудник должен иметь один первичный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-356">Every employee must have one primary identifier.</span></span> <span data-ttu-id="2b1e1-357">Этот идентификатор должен быть идентификатором типа **SSN**.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-357">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="2b1e1-358">В Dayforce он автоматически извлекается как код социального страхования сотрудника, который необходим для приема на работу.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-358">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="2b1e1-359">Основной (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-359">Primary (required)</span></span>
- <span data-ttu-id="2b1e1-360">Тип идентификации = "SSN"</span><span class="sxs-lookup"><span data-stu-id="2b1e1-360">Identification Type = "SSN"</span></span>
- <span data-ttu-id="2b1e1-361">Дата выпуска</span><span class="sxs-lookup"><span data-stu-id="2b1e1-361">Issued Date</span></span>
- <span data-ttu-id="2b1e1-362">Дата окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="2b1e1-362">Expiration Date</span></span>

<span data-ttu-id="2b1e1-363">Сотрудники могут объявить несколько идентификационных номеров для типа идентификатора **SSN**.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-363">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="2b1e1-364">Тем не менее только запись, которая помечен как **Основная**, интегрируется в Dayforce, независимо от того, является ли номер активным или у него истек срок действия.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-364">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="2b1e1-365">Банковские счета и выплаты</span><span class="sxs-lookup"><span data-stu-id="2b1e1-365">Bank accounts and disbursements</span></span>

<span data-ttu-id="2b1e1-366">Необходимо ввести действительную информацию о банковском счете для любого сотрудника, который выбирает оплату через перевод на банковский счет.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-366">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="2b1e1-367">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="2b1e1-367">Human Resources</span></span>                         | <span data-ttu-id="2b1e1-368">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2b1e1-368">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b1e1-369">Номер счета в банке (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-369">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="2b1e1-370">Код SWIFT (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-370">SWIFT code (required)</span></span>          | <span data-ttu-id="2b1e1-371">Поле **Код банка** используется при обработке зарплаты в Мексике.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-371">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="2b1e1-372">Номер филиала (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-372">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="2b1e1-373">Тип банковского счета (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-373">Bank account type (required)</span></span>   | <span data-ttu-id="2b1e1-374">Поле **Тип счета** используется при обработке зарплаты в Мексике.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-374">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="2b1e1-375">Поддерживаются значения **Выписка чека** и **Заработная плата**.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-375">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="2b1e1-376">Работники, которые выбрали выплату переводом на банковский счет, должен предоставить ссылку на счет остатков, находящийся в юридическом лице с основным адресом в Мексике и связанный с действительным банковским счетом из мексиканского банка.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-376">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="2b1e1-377">Все другие счета, не являющиеся счетами остатков, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-377">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="2b1e1-378">Адресная информация</span><span class="sxs-lookup"><span data-stu-id="2b1e1-378">Address information</span></span>

<span data-ttu-id="2b1e1-379">Каждый сотрудник должен иметь одно первичное местонахождение.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-379">Every employee must have one primary location.</span></span> <span data-ttu-id="2b1e1-380">В Dayforce это расположение используется для определения основного места жительства сотрудника для целей налогообложения.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-380">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="2b1e1-381">Основной (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-381">Primary (required)</span></span>
- <span data-ttu-id="2b1e1-382">Страна/регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-382">Country/region (required)</span></span>
- <span data-ttu-id="2b1e1-383">Почтовый индекс (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-383">Zip/postal code (required)</span></span>
- <span data-ttu-id="2b1e1-384">Улица (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-384">Street (required)</span></span>
- <span data-ttu-id="2b1e1-385">Номер дома (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-385">Street Number (required)</span></span>
- <span data-ttu-id="2b1e1-386">Дополнение здания</span><span class="sxs-lookup"><span data-stu-id="2b1e1-386">Building Complement</span></span>
- <span data-ttu-id="2b1e1-387">Город (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-387">City (required)</span></span>
- <span data-ttu-id="2b1e1-388">Регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-388">State (required)</span></span>
- <span data-ttu-id="2b1e1-389">Район (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-389">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="2b1e1-390">Настройка данных для расчета заработной платы в США и Канаде</span><span class="sxs-lookup"><span data-stu-id="2b1e1-390">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="2b1e1-391">Если вы создаете оплату для сотрудников в США и Канаде, необходимо настроить следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="2b1e1-391">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="2b1e1-392">Обязательно указывать подразделения для должностей.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-392">Departments are required on positions.</span></span>
- <span data-ttu-id="2b1e1-393">Центры затрат должен быть заданы как финансовые аналитики и должны быть первым элементом в строке финансовой аналитики по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-393">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="2b1e1-394">Можно настроить Human Resources, чтобы для должностей требовалось указывать подразделение.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-394">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="2b1e1-395">Чтобы сделать это, выберите **Совместно используемые позиции управления персоналом > Позиции > Требовать подразделения для позиций**.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-395">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="2b1e1-396">Рекомендуется включить этот параметр для интеграции.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-396">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="2b1e1-397">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="2b1e1-397">Job types</span></span>

<span data-ttu-id="2b1e1-398">Типы должностей используются для группирования похожих должностных обязанностей в категории.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-398">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="2b1e1-399">Типы должностей обязательны для обработки зарплаты в США и Канаде.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-399">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="2b1e1-400">Примеры типов должностей включают полный рабочий день и неполный рабочий день, или зарплата и почасовая оплата.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-400">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="2b1e1-401">Типы должностей сопоставляются с Dayforce как типы зарплаты, которые указывают тип оплаты сотрудника: почасовая или оклад.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-401">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="2b1e1-402">Требуются следующие типы должностей и описаний.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-402">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="2b1e1-403">Тип задания</span><span class="sxs-lookup"><span data-stu-id="2b1e1-403">Job type</span></span>   | <span data-ttu-id="2b1e1-404">описание</span><span class="sxs-lookup"><span data-stu-id="2b1e1-404">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="2b1e1-405">Почасовая</span><span class="sxs-lookup"><span data-stu-id="2b1e1-405">Hourly</span></span>     | <span data-ttu-id="2b1e1-406">Почасовая</span><span class="sxs-lookup"><span data-stu-id="2b1e1-406">Hourly</span></span>      |
| <span data-ttu-id="2b1e1-407">Оклад</span><span class="sxs-lookup"><span data-stu-id="2b1e1-407">Salaried</span></span>   | <span data-ttu-id="2b1e1-408">Оклад</span><span class="sxs-lookup"><span data-stu-id="2b1e1-408">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="2b1e1-409">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="2b1e1-409">Position types</span></span> 

<span data-ttu-id="2b1e1-410">С помощью типов должностей описывается, является ли должность занятостью на полный рабочий день, на неполный рабочий день или какой-либо другой.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-410">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="2b1e1-411">Типы должностей сопоставляются с Dayforce как классы зарплаты, которые указывают тип оплаты сотрудника: полная занятость или частичная занятость.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-411">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="2b1e1-412">Требуются следующие типы должностей и описаний.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-412">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="2b1e1-413">Тип должности</span><span class="sxs-lookup"><span data-stu-id="2b1e1-413">Position type</span></span>   | <span data-ttu-id="2b1e1-414">описание</span><span class="sxs-lookup"><span data-stu-id="2b1e1-414">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="2b1e1-415">Полная занятость</span><span class="sxs-lookup"><span data-stu-id="2b1e1-415">Full-time</span></span>       | <span data-ttu-id="2b1e1-416">Работник с полной занятостью</span><span class="sxs-lookup"><span data-stu-id="2b1e1-416">Full time employee</span></span> |
| <span data-ttu-id="2b1e1-417">Частичная занятость</span><span class="sxs-lookup"><span data-stu-id="2b1e1-417">Part-time</span></span>       | <span data-ttu-id="2b1e1-418">Работник с частичной занятостью</span><span class="sxs-lookup"><span data-stu-id="2b1e1-418">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="2b1e1-419">Коды оснований</span><span class="sxs-lookup"><span data-stu-id="2b1e1-419">Reason codes</span></span>

<span data-ttu-id="2b1e1-420">Коды оснований содержат сведения о статусе сотрудника.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-420">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="2b1e1-421">Коды оснований сопоставляются с Dayforce как причины статуса, которые определяют причину изменения статус должности или найма сотрудника.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-421">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="2b1e1-422">Требуются следующие коды причин и описания.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-422">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="2b1e1-423">Код основания</span><span class="sxs-lookup"><span data-stu-id="2b1e1-423">Reason code</span></span>    | <span data-ttu-id="2b1e1-424">описание</span><span class="sxs-lookup"><span data-stu-id="2b1e1-424">Description</span></span>      | <span data-ttu-id="2b1e1-425">Применимые сценарии</span><span class="sxs-lookup"><span data-stu-id="2b1e1-425">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="2b1e1-426">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="2b1e1-426">RESIGNATION</span></span>    | <span data-ttu-id="2b1e1-427">Увольнение</span><span class="sxs-lookup"><span data-stu-id="2b1e1-427">Resignation</span></span>      | <span data-ttu-id="2b1e1-428">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-428">Terminate worker</span></span>     |
| <span data-ttu-id="2b1e1-429">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="2b1e1-429">TERMINATION</span></span>    | <span data-ttu-id="2b1e1-430">Завершение</span><span class="sxs-lookup"><span data-stu-id="2b1e1-430">Termination</span></span>      | <span data-ttu-id="2b1e1-431">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-431">Terminate worker</span></span>     |
| <span data-ttu-id="2b1e1-432">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="2b1e1-432">RETIREMENT</span></span>     | <span data-ttu-id="2b1e1-433">Выходное пособие</span><span class="sxs-lookup"><span data-stu-id="2b1e1-433">Retirement</span></span>       | <span data-ttu-id="2b1e1-434">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-434">Terminate worker</span></span>     |
| <span data-ttu-id="2b1e1-435">ПРОЧЕЕ</span><span class="sxs-lookup"><span data-stu-id="2b1e1-435">OTHER</span></span>          | <span data-ttu-id="2b1e1-436">Другие причины</span><span class="sxs-lookup"><span data-stu-id="2b1e1-436">Other Reasons</span></span>    | <span data-ttu-id="2b1e1-437">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-437">Terminate worker</span></span>     |
| <span data-ttu-id="2b1e1-438">DEATH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-438">DEATH</span></span>          | <span data-ttu-id="2b1e1-439">Смерть</span><span class="sxs-lookup"><span data-stu-id="2b1e1-439">Death</span></span>            | <span data-ttu-id="2b1e1-440">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-440">Terminate worker</span></span>     |
| <span data-ttu-id="2b1e1-441">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="2b1e1-441">LEAVEOFABSENCE</span></span> | <span data-ttu-id="2b1e1-442">Отпуск</span><span class="sxs-lookup"><span data-stu-id="2b1e1-442">Leave of Absence</span></span> | <span data-ttu-id="2b1e1-443">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-443">Terminate worker</span></span>     |
| <span data-ttu-id="2b1e1-444">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="2b1e1-444">CONTRACTEND</span></span>    | <span data-ttu-id="2b1e1-445">Завершение контракта</span><span class="sxs-lookup"><span data-stu-id="2b1e1-445">End of Contract</span></span>  | <span data-ttu-id="2b1e1-446">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-446">Terminate worker</span></span>     |
| <span data-ttu-id="2b1e1-447">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="2b1e1-447">SALARYCHANGE</span></span>   | <span data-ttu-id="2b1e1-448">Изменение зарплаты</span><span class="sxs-lookup"><span data-stu-id="2b1e1-448">Change of Salary</span></span> | <span data-ttu-id="2b1e1-449">Компенсация</span><span class="sxs-lookup"><span data-stu-id="2b1e1-449">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="2b1e1-450">Семейное положение</span><span class="sxs-lookup"><span data-stu-id="2b1e1-450">Marital status</span></span>

<span data-ttu-id="2b1e1-451">Значения семейного положения сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-451">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="2b1e1-452">В следующей таблице показано, как значения семейного положения сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-452">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="2b1e1-453">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="2b1e1-453">Human Resources</span></span>                 | <span data-ttu-id="2b1e1-454">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2b1e1-454">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="2b1e1-455">Женат/замужем</span><span class="sxs-lookup"><span data-stu-id="2b1e1-455">Married</span></span>                | <span data-ttu-id="2b1e1-456">Женат/замужем</span><span class="sxs-lookup"><span data-stu-id="2b1e1-456">Married</span></span>              |
| <span data-ttu-id="2b1e1-457">Один</span><span class="sxs-lookup"><span data-stu-id="2b1e1-457">Single</span></span>                 | <span data-ttu-id="2b1e1-458">Один</span><span class="sxs-lookup"><span data-stu-id="2b1e1-458">Single</span></span>               |
| <span data-ttu-id="2b1e1-459">Вдовец/вдова</span><span class="sxs-lookup"><span data-stu-id="2b1e1-459">Widowed</span></span>                | <span data-ttu-id="2b1e1-460">Вдовец/вдова</span><span class="sxs-lookup"><span data-stu-id="2b1e1-460">Widowed</span></span>              |
| <span data-ttu-id="2b1e1-461">Разведен/разведена</span><span class="sxs-lookup"><span data-stu-id="2b1e1-461">Divorced</span></span>               | <span data-ttu-id="2b1e1-462">Разведен/разведена</span><span class="sxs-lookup"><span data-stu-id="2b1e1-462">Divorced</span></span>             |
| <span data-ttu-id="2b1e1-463">Зарегистрированное партнерство</span><span class="sxs-lookup"><span data-stu-id="2b1e1-463">Registered Partnership</span></span> | <span data-ttu-id="2b1e1-464">Партнерство на внутреннем рынке</span><span class="sxs-lookup"><span data-stu-id="2b1e1-464">Domestic Partnership</span></span> |
| <span data-ttu-id="2b1e1-465">None</span><span class="sxs-lookup"><span data-stu-id="2b1e1-465">None</span></span>                   | <span data-ttu-id="2b1e1-466">None</span><span class="sxs-lookup"><span data-stu-id="2b1e1-466">None</span></span>                 |
| <span data-ttu-id="2b1e1-467">Партнерство</span><span class="sxs-lookup"><span data-stu-id="2b1e1-467">Cohabiting</span></span>             | <span data-ttu-id="2b1e1-468">Партнерство</span><span class="sxs-lookup"><span data-stu-id="2b1e1-468">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="2b1e1-469">Род</span><span class="sxs-lookup"><span data-stu-id="2b1e1-469">Gender</span></span>

<span data-ttu-id="2b1e1-470">Значения пола сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-470">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="2b1e1-471">В следующей таблице показано, как значения пола сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-471">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="2b1e1-472">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="2b1e1-472">Human Resources</span></span>       | <span data-ttu-id="2b1e1-473">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2b1e1-473">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="2b1e1-474">Пол сотрудника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-474">Male</span></span>         | <span data-ttu-id="2b1e1-475">Пол сотрудника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-475">Male</span></span>            |
| <span data-ttu-id="2b1e1-476">Женский</span><span class="sxs-lookup"><span data-stu-id="2b1e1-476">Female</span></span>       | <span data-ttu-id="2b1e1-477">Женский</span><span class="sxs-lookup"><span data-stu-id="2b1e1-477">Female</span></span>          |
| <span data-ttu-id="2b1e1-478">Неопределенный</span><span class="sxs-lookup"><span data-stu-id="2b1e1-478">Non-specific</span></span> | <span data-ttu-id="2b1e1-479">*Не поддерживается*</span><span class="sxs-lookup"><span data-stu-id="2b1e1-479">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="2b1e1-480">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="2b1e1-480">Earning codes</span></span>

<span data-ttu-id="2b1e1-481">Коды доходов уникально определяют каждый типа доходов, которые работники получают.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-481">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="2b1e1-482">Эти коды покрывают несколько параметров, которые относятся к доходам, таких как правила учета, налоговые законы, требования к отчетности и возможности брутто в большую сторону.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-482">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="2b1e1-483">Если используется неподдерживаемая частота, частота **Каждая оплата** используется по умолчанию для расчета.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-483">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="2b1e1-484">Поддерживаемые частоты</span><span class="sxs-lookup"><span data-stu-id="2b1e1-484">Supported frequencies</span></span>

- <span data-ttu-id="2b1e1-485">Все</span><span class="sxs-lookup"><span data-stu-id="2b1e1-485">All</span></span>
- <span data-ttu-id="2b1e1-486">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="2b1e1-486">EVERYPAY</span></span>
- <span data-ttu-id="2b1e1-487">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="2b1e1-487">EACHPAYPERIOD</span></span>
- <span data-ttu-id="2b1e1-488">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="2b1e1-488">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="2b1e1-489">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="2b1e1-489">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="2b1e1-490">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-490">1OFMTH</span></span>
- <span data-ttu-id="2b1e1-491">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-491">LASTOFMTH</span></span>
- <span data-ttu-id="2b1e1-492">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-492">2OFMTH</span></span>
- <span data-ttu-id="2b1e1-493">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-493">3OFMTH</span></span>
- <span data-ttu-id="2b1e1-494">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-494">4OFMTH</span></span>
- <span data-ttu-id="2b1e1-495">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-495">5OFMTH</span></span>
- <span data-ttu-id="2b1e1-496">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-496">1N2OFMTH</span></span>
- <span data-ttu-id="2b1e1-497">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-497">3N4OFMTH</span></span>
- <span data-ttu-id="2b1e1-498">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-498">1N3OFMTH</span></span>
- <span data-ttu-id="2b1e1-499">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-499">1N4OFMTH</span></span>
- <span data-ttu-id="2b1e1-500">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-500">2N3OFMTH</span></span>
- <span data-ttu-id="2b1e1-501">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-501">2N4OFMTH</span></span>
- <span data-ttu-id="2b1e1-502">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-502">1N2N3OFMTH</span></span>
- <span data-ttu-id="2b1e1-503">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-503">1N2N4OFMTH</span></span>
- <span data-ttu-id="2b1e1-504">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-504">1N3N4OFMTH</span></span>
- <span data-ttu-id="2b1e1-505">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-505">2N3N4OFMTH</span></span>
- <span data-ttu-id="2b1e1-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="2b1e1-507">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="2b1e1-507">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="2b1e1-508">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="2b1e1-508">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="2b1e1-509">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="2b1e1-509">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="2b1e1-510">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="2b1e1-510">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="2b1e1-511">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="2b1e1-511">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="2b1e1-512">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="2b1e1-512">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="2b1e1-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="2b1e1-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="2b1e1-514">Адреса</span><span class="sxs-lookup"><span data-stu-id="2b1e1-514">Addresses</span></span>

<span data-ttu-id="2b1e1-515">Идентификация кодов конкретной страны или региона, области и района (муниципалитета) требует определенных форматов, которые Dayforce и поставщики в стране или в регионе могут распознать.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-515">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="2b1e1-516">Хотя формат городов гибкий, каждый город должен быть связан с областью.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-516">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="2b1e1-517">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="2b1e1-517">Human Resources</span></span>          | <span data-ttu-id="2b1e1-518">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2b1e1-518">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="2b1e1-519">Страна/регион</span><span class="sxs-lookup"><span data-stu-id="2b1e1-519">Country/Region</span></span>  | <span data-ttu-id="2b1e1-520">Код страны</span><span class="sxs-lookup"><span data-stu-id="2b1e1-520">Country Code</span></span>          |
| <span data-ttu-id="2b1e1-521">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="2b1e1-521">Zip/Postal Code</span></span> | <span data-ttu-id="2b1e1-522">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="2b1e1-522">Postal Code</span></span>           |
| <span data-ttu-id="2b1e1-523">Область, край</span><span class="sxs-lookup"><span data-stu-id="2b1e1-523">State</span></span>           | <span data-ttu-id="2b1e1-524">Код региона</span><span class="sxs-lookup"><span data-stu-id="2b1e1-524">State Code</span></span>            |
| <span data-ttu-id="2b1e1-525">Город</span><span class="sxs-lookup"><span data-stu-id="2b1e1-525">City</span></span>            | <span data-ttu-id="2b1e1-526">Город</span><span class="sxs-lookup"><span data-stu-id="2b1e1-526">City</span></span>                  |
| <span data-ttu-id="2b1e1-527">Округ</span><span class="sxs-lookup"><span data-stu-id="2b1e1-527">County</span></span>          | <span data-ttu-id="2b1e1-528">Район (муниципалитет)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-528">County (Municipality)</span></span> |
| <span data-ttu-id="2b1e1-529">Улица</span><span class="sxs-lookup"><span data-stu-id="2b1e1-529">Street</span></span>          | <span data-ttu-id="2b1e1-530">Строка адреса 1</span><span class="sxs-lookup"><span data-stu-id="2b1e1-530">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="2b1e1-531">Налоговые регионы</span><span class="sxs-lookup"><span data-stu-id="2b1e1-531">Tax regions</span></span>

<span data-ttu-id="2b1e1-532">Налоговые регионы используются для определения налогов, которые следует применять при создании заработной платы.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-532">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="2b1e1-533">Налоговые регионы сопоставляются с Dayforce как адреса местоположения.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-533">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="2b1e1-534">Налоговый регион по умолчанию должен быть связан с активной должностью работника.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-534">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="2b1e1-535">Налоговый регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-535">Tax region (required)</span></span>
- <span data-ttu-id="2b1e1-536">Страна/Регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-536">Country/Region (required)</span></span>
- <span data-ttu-id="2b1e1-537">Регион (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-537">State (required)</span></span>
- <span data-ttu-id="2b1e1-538">Округ</span><span class="sxs-lookup"><span data-stu-id="2b1e1-538">County</span></span> 
- <span data-ttu-id="2b1e1-539">Город (обязательно)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-539">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="2b1e1-540">Настройка данных для расчета заработной платы в Мексике</span><span class="sxs-lookup"><span data-stu-id="2b1e1-540">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="2b1e1-541">Если вы создаете оплату для сотрудников в Мексике, необходимо настроить следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="2b1e1-541">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="2b1e1-542">Обязательно указывать подразделения для должностей.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-542">Departments are required on positions.</span></span>
- <span data-ttu-id="2b1e1-543">Центры затрат должен быть заданы как финансовые аналитики и должны быть первым элементом в строке финансовой аналитики по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-543">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="2b1e1-544">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="2b1e1-544">Job types</span></span>

<span data-ttu-id="2b1e1-545">Типы должностей используются для группирования похожих должностных обязанностей в категории.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-545">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="2b1e1-546">Типы должностей обязательны для обработки зарплаты в Мексике.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-546">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="2b1e1-547">Примеры типов должностей включают полный рабочий день и неполный рабочий день, или зарплата и почасовая оплата.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-547">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="2b1e1-548">Типы должностей сопоставляются с Dayforce как типы зарплаты, которые указывают тип оплаты сотрудника: почасовая или оклад.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-548">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="2b1e1-549">Требуются следующие типы должностей и описаний.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-549">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="2b1e1-550">Тип задания</span><span class="sxs-lookup"><span data-stu-id="2b1e1-550">Job type</span></span>   | <span data-ttu-id="2b1e1-551">описание</span><span class="sxs-lookup"><span data-stu-id="2b1e1-551">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="2b1e1-552">Почасовая</span><span class="sxs-lookup"><span data-stu-id="2b1e1-552">Hourly</span></span>     | <span data-ttu-id="2b1e1-553">MX Почасовая</span><span class="sxs-lookup"><span data-stu-id="2b1e1-553">MX Hourly</span></span>   |
| <span data-ttu-id="2b1e1-554">Оклад</span><span class="sxs-lookup"><span data-stu-id="2b1e1-554">Salaried</span></span>   | <span data-ttu-id="2b1e1-555">MX Оклад</span><span class="sxs-lookup"><span data-stu-id="2b1e1-555">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="2b1e1-556">Типы должностей</span><span class="sxs-lookup"><span data-stu-id="2b1e1-556">Position types</span></span> 

<span data-ttu-id="2b1e1-557">С помощью типов должностей описывается, является ли должность занятостью на полный рабочий день, на неполный рабочий день или какой-либо другой.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-557">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="2b1e1-558">Типы должностей сопоставляются с Dayforce как классы зарплаты, которые указывают тип оплаты сотрудника: полная занятость или частичная занятость.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-558">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="2b1e1-559">Требуются следующие типы должностей и описаний.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-559">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="2b1e1-560">Тип должности</span><span class="sxs-lookup"><span data-stu-id="2b1e1-560">Position type</span></span>   | <span data-ttu-id="2b1e1-561">описание</span><span class="sxs-lookup"><span data-stu-id="2b1e1-561">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="2b1e1-562">Полная занятость</span><span class="sxs-lookup"><span data-stu-id="2b1e1-562">Full-time</span></span>       | <span data-ttu-id="2b1e1-563">Работник с полной занятостью</span><span class="sxs-lookup"><span data-stu-id="2b1e1-563">Full time employee</span></span> |
| <span data-ttu-id="2b1e1-564">Частичная занятость</span><span class="sxs-lookup"><span data-stu-id="2b1e1-564">Part-time</span></span>       | <span data-ttu-id="2b1e1-565">Работник с частичной занятостью</span><span class="sxs-lookup"><span data-stu-id="2b1e1-565">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="2b1e1-566">Коды оснований</span><span class="sxs-lookup"><span data-stu-id="2b1e1-566">Reason codes</span></span>

<span data-ttu-id="2b1e1-567">Коды оснований содержат сведения о статусе сотрудника.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-567">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="2b1e1-568">Коды оснований сопоставляются с Dayforce как причины статуса, которые определяют причину изменения статус должности или найма сотрудника.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-568">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="2b1e1-569">Требуются следующие коды причин и описания.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-569">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="2b1e1-570">Код основания</span><span class="sxs-lookup"><span data-stu-id="2b1e1-570">Reason code</span></span>            | <span data-ttu-id="2b1e1-571">описание</span><span class="sxs-lookup"><span data-stu-id="2b1e1-571">Description</span></span>                    | <span data-ttu-id="2b1e1-572">Применимые сценарии</span><span class="sxs-lookup"><span data-stu-id="2b1e1-572">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="2b1e1-573">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="2b1e1-573">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="2b1e1-574">Увольнение до первой заработной платы</span><span class="sxs-lookup"><span data-stu-id="2b1e1-574">Departure before first payroll</span></span> | <span data-ttu-id="2b1e1-575">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-575">Terminate worker</span></span>     |
| <span data-ttu-id="2b1e1-576">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="2b1e1-576">RESIGNATION</span></span>            | <span data-ttu-id="2b1e1-577">Увольнение</span><span class="sxs-lookup"><span data-stu-id="2b1e1-577">Resignation</span></span>                    | <span data-ttu-id="2b1e1-578">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-578">Terminate worker</span></span>     |
| <span data-ttu-id="2b1e1-579">PENSION</span><span class="sxs-lookup"><span data-stu-id="2b1e1-579">PENSION</span></span>                | <span data-ttu-id="2b1e1-580">Пенсия</span><span class="sxs-lookup"><span data-stu-id="2b1e1-580">Pension</span></span>                        | <span data-ttu-id="2b1e1-581">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-581">Terminate worker</span></span>     |
| <span data-ttu-id="2b1e1-582">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="2b1e1-582">TERMINATION</span></span>            | <span data-ttu-id="2b1e1-583">Завершение</span><span class="sxs-lookup"><span data-stu-id="2b1e1-583">Termination</span></span>                    | <span data-ttu-id="2b1e1-584">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-584">Terminate worker</span></span>     |
| <span data-ttu-id="2b1e1-585">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="2b1e1-585">RETIREMENT</span></span>             | <span data-ttu-id="2b1e1-586">Выходное пособие</span><span class="sxs-lookup"><span data-stu-id="2b1e1-586">Retirement</span></span>                     | <span data-ttu-id="2b1e1-587">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-587">Terminate worker</span></span>     |
| <span data-ttu-id="2b1e1-588">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="2b1e1-588">ABSENTEE</span></span>               | <span data-ttu-id="2b1e1-589">Прогульщик</span><span class="sxs-lookup"><span data-stu-id="2b1e1-589">Absentee</span></span>                       | <span data-ttu-id="2b1e1-590">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-590">Terminate worker</span></span>     |
| <span data-ttu-id="2b1e1-591">ПРОЧЕЕ</span><span class="sxs-lookup"><span data-stu-id="2b1e1-591">OTHER</span></span>                  | <span data-ttu-id="2b1e1-592">Другие причины</span><span class="sxs-lookup"><span data-stu-id="2b1e1-592">Other Reasons</span></span>                  | <span data-ttu-id="2b1e1-593">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-593">Terminate worker</span></span>     |
| <span data-ttu-id="2b1e1-594">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="2b1e1-594">CLOSURE</span></span>                | <span data-ttu-id="2b1e1-595">Закрытие компании</span><span class="sxs-lookup"><span data-stu-id="2b1e1-595">Business Closure</span></span>               | <span data-ttu-id="2b1e1-596">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-596">Terminate worker</span></span>     |
| <span data-ttu-id="2b1e1-597">DEATH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-597">DEATH</span></span>                  | <span data-ttu-id="2b1e1-598">Смерть</span><span class="sxs-lookup"><span data-stu-id="2b1e1-598">Death</span></span>                          | <span data-ttu-id="2b1e1-599">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-599">Terminate worker</span></span>     |
| <span data-ttu-id="2b1e1-600">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="2b1e1-600">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="2b1e1-601">Отпуск</span><span class="sxs-lookup"><span data-stu-id="2b1e1-601">Leave of Absence</span></span>               | <span data-ttu-id="2b1e1-602">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-602">Terminate worker</span></span>     |
| <span data-ttu-id="2b1e1-603">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="2b1e1-603">CONTRACTEND</span></span>            | <span data-ttu-id="2b1e1-604">Завершение контракта</span><span class="sxs-lookup"><span data-stu-id="2b1e1-604">End of Contract</span></span>                | <span data-ttu-id="2b1e1-605">Уволить работника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-605">Terminate worker</span></span>     |
| <span data-ttu-id="2b1e1-606">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="2b1e1-606">SALARYCHANGE</span></span>           | <span data-ttu-id="2b1e1-607">Изменение зарплаты</span><span class="sxs-lookup"><span data-stu-id="2b1e1-607">Change of Salary</span></span>               | <span data-ttu-id="2b1e1-608">Компенсация</span><span class="sxs-lookup"><span data-stu-id="2b1e1-608">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="2b1e1-609">Условия найма</span><span class="sxs-lookup"><span data-stu-id="2b1e1-609">Terms of employment</span></span>

<span data-ttu-id="2b1e1-610">Условия найма используются для создания категорий условий трудоустройства.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-610">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="2b1e1-611">Условия сопоставляются с Dayforce как значения индикатора трудоустройства.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-611">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="2b1e1-612">Необходимы следующие условия найма и описания.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-612">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="2b1e1-613">Условия найма</span><span class="sxs-lookup"><span data-stu-id="2b1e1-613">Terms of employment</span></span>   | <span data-ttu-id="2b1e1-614">описание</span><span class="sxs-lookup"><span data-stu-id="2b1e1-614">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="2b1e1-615">Периодически</span><span class="sxs-lookup"><span data-stu-id="2b1e1-615">Regular</span></span>               | <span data-ttu-id="2b1e1-616">Периодически</span><span class="sxs-lookup"><span data-stu-id="2b1e1-616">Regular</span></span>     |
| <span data-ttu-id="2b1e1-617">Напрямую</span><span class="sxs-lookup"><span data-stu-id="2b1e1-617">Direct</span></span>                | <span data-ttu-id="2b1e1-618">Напрямую</span><span class="sxs-lookup"><span data-stu-id="2b1e1-618">Direct</span></span>      |
| <span data-ttu-id="2b1e1-619">Практика</span><span class="sxs-lookup"><span data-stu-id="2b1e1-619">Internship</span></span>            | <span data-ttu-id="2b1e1-620">Практика</span><span class="sxs-lookup"><span data-stu-id="2b1e1-620">Internship</span></span>  |
| <span data-ttu-id="2b1e1-621">Постоянный</span><span class="sxs-lookup"><span data-stu-id="2b1e1-621">Permanent</span></span>             | <span data-ttu-id="2b1e1-622">Постоянный</span><span class="sxs-lookup"><span data-stu-id="2b1e1-622">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="2b1e1-623">Семейное положение</span><span class="sxs-lookup"><span data-stu-id="2b1e1-623">Marital status</span></span>

<span data-ttu-id="2b1e1-624">Значения семейного положения сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-624">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="2b1e1-625">В следующей таблице показано, как значения семейного положения сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-625">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="2b1e1-626">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="2b1e1-626">Human Resources</span></span>                 | <span data-ttu-id="2b1e1-627">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2b1e1-627">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="2b1e1-628">Женат/замужем</span><span class="sxs-lookup"><span data-stu-id="2b1e1-628">Married</span></span>                | <span data-ttu-id="2b1e1-629">Женат/замужем</span><span class="sxs-lookup"><span data-stu-id="2b1e1-629">Married</span></span>                   |
| <span data-ttu-id="2b1e1-630">Один</span><span class="sxs-lookup"><span data-stu-id="2b1e1-630">Single</span></span>                 | <span data-ttu-id="2b1e1-631">Один</span><span class="sxs-lookup"><span data-stu-id="2b1e1-631">Single</span></span>                    |
| <span data-ttu-id="2b1e1-632">Вдовец/вдова</span><span class="sxs-lookup"><span data-stu-id="2b1e1-632">Widowed</span></span>                | <span data-ttu-id="2b1e1-633">Вдовец/вдова</span><span class="sxs-lookup"><span data-stu-id="2b1e1-633">Widowed</span></span>                   |
| <span data-ttu-id="2b1e1-634">Разведен/разведена</span><span class="sxs-lookup"><span data-stu-id="2b1e1-634">Divorced</span></span>               | <span data-ttu-id="2b1e1-635">Разведен/разведена</span><span class="sxs-lookup"><span data-stu-id="2b1e1-635">Divorced</span></span>                  |
| <span data-ttu-id="2b1e1-636">Зарегистрированное партнерство</span><span class="sxs-lookup"><span data-stu-id="2b1e1-636">Registered Partnership</span></span> | <span data-ttu-id="2b1e1-637">Партнерство на внутреннем рынке</span><span class="sxs-lookup"><span data-stu-id="2b1e1-637">Domestic Partnership</span></span>      |
| <span data-ttu-id="2b1e1-638">None</span><span class="sxs-lookup"><span data-stu-id="2b1e1-638">None</span></span>                   | <span data-ttu-id="2b1e1-639">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="2b1e1-639">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="2b1e1-640">Партнерство</span><span class="sxs-lookup"><span data-stu-id="2b1e1-640">Cohabiting</span></span>             | <span data-ttu-id="2b1e1-641">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="2b1e1-641">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="2b1e1-642">Род</span><span class="sxs-lookup"><span data-stu-id="2b1e1-642">Gender</span></span>

<span data-ttu-id="2b1e1-643">Значения пола сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-643">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="2b1e1-644">В следующей таблице показано, как значения пола сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-644">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="2b1e1-645">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="2b1e1-645">Human Resources</span></span>       | <span data-ttu-id="2b1e1-646">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2b1e1-646">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="2b1e1-647">Пол сотрудника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-647">Male</span></span>         | <span data-ttu-id="2b1e1-648">Пол сотрудника</span><span class="sxs-lookup"><span data-stu-id="2b1e1-648">Male</span></span>                      |
| <span data-ttu-id="2b1e1-649">Женский</span><span class="sxs-lookup"><span data-stu-id="2b1e1-649">Female</span></span>       | <span data-ttu-id="2b1e1-650">Женский</span><span class="sxs-lookup"><span data-stu-id="2b1e1-650">Female</span></span>                    |
| <span data-ttu-id="2b1e1-651">Неопределенный</span><span class="sxs-lookup"><span data-stu-id="2b1e1-651">Non-specific</span></span> | <span data-ttu-id="2b1e1-652">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="2b1e1-652">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="2b1e1-653">Способ платежа</span><span class="sxs-lookup"><span data-stu-id="2b1e1-653">Payment method</span></span>

<span data-ttu-id="2b1e1-654">Методы оплаты предоставляют сотруднику и компании способ описания способа оплаты сотрудников.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-654">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="2b1e1-655">Способы оплаты сопоставляются с Dayforce и переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-655">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="2b1e1-656">В следующей таблице показано, как способы оплаты сопоставляются с Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-656">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="2b1e1-657">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="2b1e1-657">Human Resources</span></span>             | <span data-ttu-id="2b1e1-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2b1e1-658">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="2b1e1-659">Касса за </span><span class="sxs-lookup"><span data-stu-id="2b1e1-659">Cash</span></span>               | <span data-ttu-id="2b1e1-660">Касса за </span><span class="sxs-lookup"><span data-stu-id="2b1e1-660">Cash</span></span>                      |
| <span data-ttu-id="2b1e1-661">Электронный платеж</span><span class="sxs-lookup"><span data-stu-id="2b1e1-661">Electronic Payment</span></span> | <span data-ttu-id="2b1e1-662">Перенос</span><span class="sxs-lookup"><span data-stu-id="2b1e1-662">Transfer</span></span>                  |
| <span data-ttu-id="2b1e1-663">Проверка</span><span class="sxs-lookup"><span data-stu-id="2b1e1-663">Check</span></span>              | <span data-ttu-id="2b1e1-664">Чек</span><span class="sxs-lookup"><span data-stu-id="2b1e1-664">Cheque</span></span>                    |
| <span data-ttu-id="2b1e1-665">Банковская тратта</span><span class="sxs-lookup"><span data-stu-id="2b1e1-665">Bank Draft</span></span>         | <span data-ttu-id="2b1e1-666">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="2b1e1-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="2b1e1-667">Прочие</span><span class="sxs-lookup"><span data-stu-id="2b1e1-667">Other</span></span>              | <span data-ttu-id="2b1e1-668">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="2b1e1-668">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="2b1e1-669">Тип банковского счета</span><span class="sxs-lookup"><span data-stu-id="2b1e1-669">Bank account type</span></span>

<span data-ttu-id="2b1e1-670">Типы банковских счетов используются для электронных платежей сотрудникам.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-670">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="2b1e1-671">Типы банковских счетов сопоставляются с Dayforce как сведения о счетах безналичных расчетов.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-671">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="2b1e1-672">Типы банковских счетов переводятся, соответственно, в допустимые значения при интеграции.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-672">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="2b1e1-673">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="2b1e1-673">Human Resources</span></span>            | <span data-ttu-id="2b1e1-674">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2b1e1-674">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="2b1e1-675">Чековый счет</span><span class="sxs-lookup"><span data-stu-id="2b1e1-675">Checking Account</span></span>  | <span data-ttu-id="2b1e1-676">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="2b1e1-676">CheckingAccount</span></span>           |
| <span data-ttu-id="2b1e1-677">Счет зарплаты</span><span class="sxs-lookup"><span data-stu-id="2b1e1-677">Payroll Account</span></span>   | <span data-ttu-id="2b1e1-678">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="2b1e1-678">PayrollAccount</span></span>            |
| <span data-ttu-id="2b1e1-679">Сберегательный счет</span><span class="sxs-lookup"><span data-stu-id="2b1e1-679">Savings Account</span></span>   | <span data-ttu-id="2b1e1-680">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="2b1e1-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="2b1e1-681">Счет BankGirot</span><span class="sxs-lookup"><span data-stu-id="2b1e1-681">BankGirot account</span></span> | <span data-ttu-id="2b1e1-682">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="2b1e1-682">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="2b1e1-683">Счет PlusGirot</span><span class="sxs-lookup"><span data-stu-id="2b1e1-683">PlusGirot account</span></span> | <span data-ttu-id="2b1e1-684">*Не поддерживается для Мексики*</span><span class="sxs-lookup"><span data-stu-id="2b1e1-684">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="2b1e1-685">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="2b1e1-685">Earning codes</span></span>

<span data-ttu-id="2b1e1-686">Коды доходов уникально определяют каждый типа доходов, которые работники получают.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-686">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="2b1e1-687">Эти коды покрывают несколько параметров, которые относятся к доходам, таких как правила учета, налоговые законы, требования к отчетности и возможности брутто в большую сторону.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-687">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="2b1e1-688">Если используется неподдерживаемая частота, частота **Каждая оплата** используется по умолчанию для расчета.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-688">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="2b1e1-689">Поддерживаемые частоты</span><span class="sxs-lookup"><span data-stu-id="2b1e1-689">Supported frequencies</span></span>

- <span data-ttu-id="2b1e1-690">Все</span><span class="sxs-lookup"><span data-stu-id="2b1e1-690">All</span></span>
- <span data-ttu-id="2b1e1-691">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="2b1e1-691">EVERYPAY</span></span>
- <span data-ttu-id="2b1e1-692">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="2b1e1-692">EACHPAYPERIOD</span></span>
- <span data-ttu-id="2b1e1-693">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="2b1e1-693">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="2b1e1-694">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="2b1e1-694">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="2b1e1-695">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-695">1OFMTH</span></span>
- <span data-ttu-id="2b1e1-696">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-696">LASTOFMTH</span></span>
- <span data-ttu-id="2b1e1-697">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-697">2OFMTH</span></span>
- <span data-ttu-id="2b1e1-698">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-698">3OFMTH</span></span>
- <span data-ttu-id="2b1e1-699">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-699">4OFMTH</span></span>
- <span data-ttu-id="2b1e1-700">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-700">5OFMTH</span></span>
- <span data-ttu-id="2b1e1-701">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-701">1N2OFMTH</span></span>
- <span data-ttu-id="2b1e1-702">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-702">3N4OFMTH</span></span>
- <span data-ttu-id="2b1e1-703">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-703">1N3OFMTH</span></span>
- <span data-ttu-id="2b1e1-704">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-704">1N4OFMTH</span></span>
- <span data-ttu-id="2b1e1-705">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-705">2N3OFMTH</span></span>
- <span data-ttu-id="2b1e1-706">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-706">2N4OFMTH</span></span>
- <span data-ttu-id="2b1e1-707">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-707">1N2N3OFMTH</span></span>
- <span data-ttu-id="2b1e1-708">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-708">1N2N4OFMTH</span></span>
- <span data-ttu-id="2b1e1-709">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-709">1N3N4OFMTH</span></span>
- <span data-ttu-id="2b1e1-710">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-710">2N3N4OFMTH</span></span>
- <span data-ttu-id="2b1e1-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2b1e1-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="2b1e1-712">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="2b1e1-712">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="2b1e1-713">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="2b1e1-713">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="2b1e1-714">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="2b1e1-714">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="2b1e1-715">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="2b1e1-715">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="2b1e1-716">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="2b1e1-716">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="2b1e1-717">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="2b1e1-717">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="2b1e1-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="2b1e1-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="2b1e1-719">Адреса</span><span class="sxs-lookup"><span data-stu-id="2b1e1-719">Addresses</span></span>

<span data-ttu-id="2b1e1-720">Идентификация кодов конкретной страны или региона, области и района (муниципалитета) требует определенных форматов, которые Dayforce и поставщики в стране или в регионе могут распознать.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-720">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="2b1e1-721">Хотя формат городов гибкий, каждый город должен быть связан с областью.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-721">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="2b1e1-722">Управление персоналом</span><span class="sxs-lookup"><span data-stu-id="2b1e1-722">Human Resources</span></span>              | <span data-ttu-id="2b1e1-723">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2b1e1-723">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="2b1e1-724">Страна/регион</span><span class="sxs-lookup"><span data-stu-id="2b1e1-724">Country/Region</span></span>      | <span data-ttu-id="2b1e1-725">Код страны</span><span class="sxs-lookup"><span data-stu-id="2b1e1-725">Country Code</span></span>          |
| <span data-ttu-id="2b1e1-726">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="2b1e1-726">Zip/Postal Code</span></span>     | <span data-ttu-id="2b1e1-727">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="2b1e1-727">Postal Code</span></span>           |
| <span data-ttu-id="2b1e1-728">Область, край</span><span class="sxs-lookup"><span data-stu-id="2b1e1-728">State</span></span>               | <span data-ttu-id="2b1e1-729">Код региона</span><span class="sxs-lookup"><span data-stu-id="2b1e1-729">State Code</span></span>            |
| <span data-ttu-id="2b1e1-730">Город</span><span class="sxs-lookup"><span data-stu-id="2b1e1-730">City</span></span>                | <span data-ttu-id="2b1e1-731">Город</span><span class="sxs-lookup"><span data-stu-id="2b1e1-731">City</span></span>                  |
| <span data-ttu-id="2b1e1-732">Округ</span><span class="sxs-lookup"><span data-stu-id="2b1e1-732">County</span></span>              | <span data-ttu-id="2b1e1-733">Район (муниципалитет)</span><span class="sxs-lookup"><span data-stu-id="2b1e1-733">County (Municipality)</span></span> |
| <span data-ttu-id="2b1e1-734">Улица</span><span class="sxs-lookup"><span data-stu-id="2b1e1-734">Street</span></span>              | <span data-ttu-id="2b1e1-735">Строка адреса 1</span><span class="sxs-lookup"><span data-stu-id="2b1e1-735">Address Line 1</span></span>        |
| <span data-ttu-id="2b1e1-736">Номер дома</span><span class="sxs-lookup"><span data-stu-id="2b1e1-736">Street Number</span></span>       | <span data-ttu-id="2b1e1-737">Строка адреса 2</span><span class="sxs-lookup"><span data-stu-id="2b1e1-737">Address Line 2</span></span>        |
| <span data-ttu-id="2b1e1-738">Дополнение здания</span><span class="sxs-lookup"><span data-stu-id="2b1e1-738">Building Complement</span></span> | <span data-ttu-id="2b1e1-739">Строка адреса 5</span><span class="sxs-lookup"><span data-stu-id="2b1e1-739">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="2b1e1-740">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="2b1e1-740">Passport number</span></span>

<span data-ttu-id="2b1e1-741">Сотрудники могут объявить данные паспорта.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-741">Employees can declare passport information.</span></span> <span data-ttu-id="2b1e1-742">Эта информация имеет тип идентификации **Паспорт** и интегрируется в Dayforce как часть сведений о сотруднике, специфических для Мексики.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-742">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="2b1e1-743">Тип идентификации = "Паспорт"</span><span class="sxs-lookup"><span data-stu-id="2b1e1-743">Identification Type = "Passport"</span></span>
- <span data-ttu-id="2b1e1-744">Дата выпуска</span><span class="sxs-lookup"><span data-stu-id="2b1e1-744">Issued Date</span></span>
- <span data-ttu-id="2b1e1-745">Дата окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="2b1e1-745">Expiration Date</span></span>

<span data-ttu-id="2b1e1-746">Сотрудники могут объявить несколько идентификационных номеров для типа идентификатора **Паспорт**.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-746">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="2b1e1-747">Тем не менее только запись текущего активного паспорта интегрируется в Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-747">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="2b1e1-748">Если срок действия всех записей паспорта истек, в Dayforce интегрируется тот, который был выдан последним.</span><span class="sxs-lookup"><span data-stu-id="2b1e1-748">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]