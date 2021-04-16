---
title: Начало работы с электронным выставлением накладных для Мексики
description: В этой теме приводятся сведения, которые помогут приступить к работе с электронным выставлением накладных для Мексики.
author: gionoder
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 2f5dd1d6bc520c9f5349c77dfcabdf2d538881ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840060"
---
# <a name="get-started-with-electronic-invoicing-for-mexico"></a><span data-ttu-id="b203b-103">Начало работы с электронным выставлением накладных для Мексики</span><span class="sxs-lookup"><span data-stu-id="b203b-103">Get started with Electronic invoicing for Mexico</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="b203b-104">Модуль электронного выставления накладных для Мексики в настоящее время может не поддерживать все функции, доступные в документе Comprobante Fiscal Digital por Internet (CFDI) и в соответствующей интеграции, встроенной в Microsoft Dynamics 365 Finance или Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b203b-104">Electronic invoicing for Mexico might not currently support all the functions that are available in the Comprobante Fiscal Digital por Internet (CFDI) document, and in the related integration that is built into Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="b203b-105">В этой теме приводятся сведения, которые помогут приступить к работе с электронным выставлением накладных для Мексики.</span><span class="sxs-lookup"><span data-stu-id="b203b-105">This topic provides information that will help you get started with Electronic invoicing for Mexico.</span></span> <span data-ttu-id="b203b-106">Она поможет выполнить этапы настройки, зависящие от страны или региона, в службах Regulatory Configuration Services (RCS) и в Finance.</span><span class="sxs-lookup"><span data-stu-id="b203b-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="b203b-107">Она также поможет выполнить шаги, которые необходимо проследить в Finance, чтобы отправить накладные CFDI через службу, и в ней объясняется, как просмотреть результаты обработки и статус накладных CFDI.</span><span class="sxs-lookup"><span data-stu-id="b203b-107">It also guides you through the steps that you must follow in Finance to submit CFDI invoices through the service, and it explains how to review the processing results and the status of CFDI invoices.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b203b-108">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="b203b-108">Prerequisites</span></span>

<span data-ttu-id="b203b-109">Перед выполнением шагов, описанных в этой теме, необходимо выполнить шаги из раздела [Приступая к работе с модулем электронного выставления накладных](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="b203b-109">Before you complete the steps in this topic, you must complete the steps in [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="b203b-110">Настройка RCS</span><span class="sxs-lookup"><span data-stu-id="b203b-110">RCS setup</span></span>

<span data-ttu-id="b203b-111">Во время настройки RCS будут выполнены следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="b203b-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="b203b-112">Импорт компонента электронных накладных для обработки накладных CFDI.</span><span class="sxs-lookup"><span data-stu-id="b203b-112">Import the e-Invoicing feature for processing CFDI invoices.</span></span>
2. <span data-ttu-id="b203b-113">Просмотрите конфигурации формата, необходимые для создания, отправки и получения ответов о накладных CFDI, а также для отправки и получения ответов об отмене.</span><span class="sxs-lookup"><span data-stu-id="b203b-113">Review the format configurations that are required to generate, submit, and receive responses about CFDI invoices, and to submit and receive responses about cancellation.</span></span>
3. <span data-ttu-id="b203b-114">Настройте события, которые поддерживают сценарии отправки накладных CFDI.</span><span class="sxs-lookup"><span data-stu-id="b203b-114">Configure the events that support the CFDI invoice submission scenarios.</span></span>
4. <span data-ttu-id="b203b-115">Опубликуйте компонент электронных накладных для накладных CFDI.</span><span class="sxs-lookup"><span data-stu-id="b203b-115">Publish the e-Invoicing feature for CFDI invoices.</span></span>

> [!NOTE]
> <span data-ttu-id="b203b-116">"Функция электронных накладных" — это универсальное имя для ресурса, который настраивается и публикуется для использования сервера модуля электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="b203b-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing server.</span></span> <span data-ttu-id="b203b-117">В этом случае накладные CFDI (MX) представляют собой функцию электронных накладных, которая будет настроена.</span><span class="sxs-lookup"><span data-stu-id="b203b-117">In this case, CFDI invoices (MX) are the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="b203b-118">Импорт функции выставления накладных в электронной форме</span><span class="sxs-lookup"><span data-stu-id="b203b-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="b203b-119">Войдите в учетную запись RCS.</span><span class="sxs-lookup"><span data-stu-id="b203b-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="b203b-120">В рабочей области **Функции глобализации** в разделе **Функции** выберите плитку **Электронные накладные**.</span><span class="sxs-lookup"><span data-stu-id="b203b-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="b203b-121">На странице **Функции электронного выставления накладных** выберите **Импорт**, чтобы импортировать функцию **Накладные CFDI (MX)** из глобального репозитория.</span><span class="sxs-lookup"><span data-stu-id="b203b-121">On the **e-Invoicing Features** page, select **Import** to import the **CFDI invoices (MX)** feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b203b-122">Если эта функция не отображается в списке, выберите **Синхронизировать**, затем повторите шаг 3.</span><span class="sxs-lookup"><span data-stu-id="b203b-122">If you don't see the feature in the list, select **Synchronize**, and then repeat step 3.</span></span>

![Импорт функции накладных CFDI (MX)](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

<span data-ttu-id="b203b-124">При импорте компонента **Накладные CFDI (MX)** из глобального репозитория также импортируются все параметры функций, включая конфигурации и действия.</span><span class="sxs-lookup"><span data-stu-id="b203b-124">When you import the **CFDI invoices (MX)** feature from the Global repository, all the feature settings, including configurations and actions, are also imported.</span></span>

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a><span data-ttu-id="b203b-125">Создание новой версии функции накладных CFDI (MX)</span><span class="sxs-lookup"><span data-stu-id="b203b-125">Create a new version of the CFDI invoices (MX) feature</span></span>

<span data-ttu-id="b203b-126">Можно создать новую версию, если, например, необходимо обновить URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="b203b-126">You can create a new version if, for example, URLs must be updated.</span></span> <span data-ttu-id="b203b-127">Дополнительные сведения см. в разделе [Выставление электронных накладных CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span><span class="sxs-lookup"><span data-stu-id="b203b-127">For more information, see [E-invoicing CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span></span>

- <span data-ttu-id="b203b-128">На странице **Функции электронных накладных** на вкладке **Версии** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="b203b-128">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![Добавление новой версии функции электронных накладных](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="b203b-130">Обновление версии конфигурации</span><span class="sxs-lookup"><span data-stu-id="b203b-130">Update the configuration version</span></span>

1. <span data-ttu-id="b203b-131">На странице **Функции электронного выставления накладных** на вкладке **Конфигурации** выберите **Добавить** или **Удалить** для управления версиями конфигураций (конфигурации формата файлов электронной отчетности).</span><span class="sxs-lookup"><span data-stu-id="b203b-131">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![Управление конфигурациями функции электронных накладных](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    <span data-ttu-id="b203b-133">При создании новой версии все конфигурации наследуются из последней опубликованной версии.</span><span class="sxs-lookup"><span data-stu-id="b203b-133">When you create a new version, all configurations are inherited from the last published version.</span></span> <span data-ttu-id="b203b-134">Для обработки накладных CFDI требуются следующие конфигурации:</span><span class="sxs-lookup"><span data-stu-id="b203b-134">To process CFDI invoices, the following configurations are required:</span></span>

    - <span data-ttu-id="b203b-135">Накладная CFDI (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="b203b-135">CFDI invoice (BusinessDocumentService)</span></span>
    - <span data-ttu-id="b203b-136">Импорт ответного сообщения CFDI</span><span class="sxs-lookup"><span data-stu-id="b203b-136">CFDI response message import</span></span>
    - <span data-ttu-id="b203b-137">Импорт журнала ошибок CFDI</span><span class="sxs-lookup"><span data-stu-id="b203b-137">CFDI error log import</span></span>
    - <span data-ttu-id="b203b-138">Запрос отмены CFDI (MX) (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="b203b-138">CFDI cancelation request (MX) (BusinessDocumentService)</span></span>
    - <span data-ttu-id="b203b-139">Накладная CFDI (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="b203b-139">CFDI invoice (BusinessDocumentService)</span></span>

2. <span data-ttu-id="b203b-140">В списке выберите версию конфигурации, а затем выберите **Правка** или **Просмотр**, чтобы открыть страницу **Конструктор форматов**, на которой можно изменить или просмотреть конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="b203b-140">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![Открытие страницы конструктора формата](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. <span data-ttu-id="b203b-142">Страница **Конструктор форматов** используется для изменения и просмотра конфигураций форматов файлов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="b203b-142">Use the **Format designer** page to edit and view the ER format file configurations.</span></span> <span data-ttu-id="b203b-143">Дополнительные сведения см. в разделе [Создание конфигураций электронных документов](../../dev-itpro/analytics/electronic-reporting-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="b203b-143">For more information, see [Create electronic document configurations](../../dev-itpro/analytics/electronic-reporting-configuration.md).</span></span>

    ![Страница конструктора форматов](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="b203b-145">Управление настройками функции электронных накладных</span><span class="sxs-lookup"><span data-stu-id="b203b-145">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="b203b-146">На странице **Функции электронного выставления накладных** на вкладке **Настройки** выберите **Добавить**, **Удалить** или **Изменить** для управления настройками функций электронных накладных.</span><span class="sxs-lookup"><span data-stu-id="b203b-146">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![Управление настройками функций электронных накладных](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

<span data-ttu-id="b203b-148">Чтобы отправить накладные CFDI для авторизации (создать файл XML, отправить XML-файл и обработать ответ), необходимо настроить функцию **Накладная по продаже**.</span><span class="sxs-lookup"><span data-stu-id="b203b-148">To submit CFDI invoices for authorization (generate the XML file, submit the XML file, and process the response), the **Sales invoice** feature setup is required.</span></span>

<span data-ttu-id="b203b-149">Для отправки отмены накладной CFDI необходимы настройки функций **Запрос отмены** и **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="b203b-149">To submit CFDI invoice cancellation, the **Cancellation** and **Cancel** feature setups are required.</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="b203b-150">Настройка настройки функций накладных на продажу</span><span class="sxs-lookup"><span data-stu-id="b203b-150">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="b203b-151">На странице **Функции электронного выставления накладных** на вкладке **Настройки** в столбце **Настройка функции** выберите **Накладная на продажу**.</span><span class="sxs-lookup"><span data-stu-id="b203b-151">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="b203b-152">Выберите **Правка**, чтобы настроить действия, правила применимости и переменные.</span><span class="sxs-lookup"><span data-stu-id="b203b-152">Select **Edit** to configure the actions, applicability rules, and variables.</span></span>

    ![Редактирование настройки функции электронных накладных](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="b203b-154">На странице **Настройка версии функции** выберите вкладку **Действия** для управления списком действий.</span><span class="sxs-lookup"><span data-stu-id="b203b-154">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="b203b-155">Действия определяют список операций, которые должны выполняться в последовательном порядке для обеспечения полного выполнения события.</span><span class="sxs-lookup"><span data-stu-id="b203b-155">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Вкладка "Действия"](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | <span data-ttu-id="b203b-157">Код действия</span><span class="sxs-lookup"><span data-stu-id="b203b-157">Action ID</span></span> | <span data-ttu-id="b203b-158">Действие</span><span class="sxs-lookup"><span data-stu-id="b203b-158">Action</span></span>                   | <span data-ttu-id="b203b-159">Имя действия</span><span class="sxs-lookup"><span data-stu-id="b203b-159">Action name</span></span>                                  | <span data-ttu-id="b203b-160">Описание действия</span><span class="sxs-lookup"><span data-stu-id="b203b-160">Action description</span></span>                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | <span data-ttu-id="b203b-161">1</span><span class="sxs-lookup"><span data-stu-id="b203b-161">1</span></span>         | <span data-ttu-id="b203b-162">Преобразование документа</span><span class="sxs-lookup"><span data-stu-id="b203b-162">Transform document</span></span>       | <span data-ttu-id="b203b-163">Создание электронной накладной CFDI без цифровой подписи</span><span class="sxs-lookup"><span data-stu-id="b203b-163">Generate CFDI E-Invoice without digital sign</span></span> | <span data-ttu-id="b203b-164">Создайте электронную накладную CFDI.</span><span class="sxs-lookup"><span data-stu-id="b203b-164">Generate the CFDI e-invoice.</span></span>                                |
    | <span data-ttu-id="b203b-165">2</span><span class="sxs-lookup"><span data-stu-id="b203b-165">2</span></span>         | <span data-ttu-id="b203b-166">Подписать документ</span><span class="sxs-lookup"><span data-stu-id="b203b-166">Sign document</span></span>            | <span data-ttu-id="b203b-167">Цифровая подпись</span><span class="sxs-lookup"><span data-stu-id="b203b-167">Digital sign</span></span>                                 | <span data-ttu-id="b203b-168">Подпишите электронную накладную цифровой подписью для отправки.</span><span class="sxs-lookup"><span data-stu-id="b203b-168">Digitally sign the e-invoice for submission.</span></span>                |
    | <span data-ttu-id="b203b-169">3</span><span class="sxs-lookup"><span data-stu-id="b203b-169">3</span></span>         | <span data-ttu-id="b203b-170">Вызов мексиканской службы PAC</span><span class="sxs-lookup"><span data-stu-id="b203b-170">Call Mexican PAC service</span></span> | <span data-ttu-id="b203b-171">Отправка электронной накладной CFDI</span><span class="sxs-lookup"><span data-stu-id="b203b-171">Submit CFDI E-Invoice</span></span>                        | <span data-ttu-id="b203b-172">Клиент Windows Communication Foundation (WCF) отправляет электронную накладную CFDI.</span><span class="sxs-lookup"><span data-stu-id="b203b-172">The Windows Communication Foundation (WCF) client submits the CFDI e-invoice.</span></span> |
    | <span data-ttu-id="b203b-173">4</span><span class="sxs-lookup"><span data-stu-id="b203b-173">4</span></span>         | <span data-ttu-id="b203b-174">Обработка ответа</span><span class="sxs-lookup"><span data-stu-id="b203b-174">Process response</span></span>         | <span data-ttu-id="b203b-175">Анализ ответа веб-службы</span><span class="sxs-lookup"><span data-stu-id="b203b-175">Analyze web service response</span></span>                 | <span data-ttu-id="b203b-176">Анализ ответа веб-службы и возврат журнала ошибок.</span><span class="sxs-lookup"><span data-stu-id="b203b-176">Analyze the web service response, and return the error log.</span></span> |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a><span data-ttu-id="b203b-177">Настройка URL-адреса для веб-служб PAC в Мексике</span><span class="sxs-lookup"><span data-stu-id="b203b-177">Set up the URL for Mexican PAC web services</span></span> 

1. <span data-ttu-id="b203b-178">На странице **Настройка версии функции** на вкладке **Действия** на экспресс-вкладке **Действия** выберите **Вызов мексиканской службы PAC**.</span><span class="sxs-lookup"><span data-stu-id="b203b-178">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Mexican PAC service**.</span></span>
2. <span data-ttu-id="b203b-179">На экспресс-вкладке **Параметры** в поле **URL-адрес** введите URL-адрес веб-службы для отправки накладной CFDI.</span><span class="sxs-lookup"><span data-stu-id="b203b-179">On the **Parameters** FastTab, in the **URL address** field, enter the URL of the web service for CFDI invoice submission.</span></span>

> [!NOTE]
> <span data-ttu-id="b203b-180">Выполните те же шаги для обновления URL-адреса для действия **Вызов мексиканской службы PAC** для настроек функций **Отмена** и **Запрос отмены**.</span><span class="sxs-lookup"><span data-stu-id="b203b-180">Use the same steps to update the URL for **Call Mexican PAC service** action for the **Cancel** and **Cancelation request** feature setups.</span></span>

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a><span data-ttu-id="b203b-181">Назначение черновой версии для среды выставления электронных накладных</span><span class="sxs-lookup"><span data-stu-id="b203b-181">Assign the Draft version to an e-Invoicing environment</span></span>

1. <span data-ttu-id="b203b-182">На странице **Функции электронных накладных** на вкладке **Среды** выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="b203b-182">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="b203b-183">В поле **Среда** выберите среду.</span><span class="sxs-lookup"><span data-stu-id="b203b-183">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="b203b-184">В поле **Действует с** выберите дату, когда новая среда должна начать действовать.</span><span class="sxs-lookup"><span data-stu-id="b203b-184">In the **Effective from** field, select the date when the environment should become effective.</span></span>
3. <span data-ttu-id="b203b-185">Выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="b203b-185">Select **Enable**.</span></span>

![Включение среды выставления накладных в электронной форме](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a><span data-ttu-id="b203b-187">Изменение статуса версии на "Завершено"</span><span class="sxs-lookup"><span data-stu-id="b203b-187">Change the version status to Completed</span></span>

1. <span data-ttu-id="b203b-188">На странице **Функции электронных накладных** на вкладке **Версии** выберите версию функции электронных накладных, имеющую статус **Черновик**.</span><span class="sxs-lookup"><span data-stu-id="b203b-188">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="b203b-189">Выберите **Изменить статус \> Завершено**.</span><span class="sxs-lookup"><span data-stu-id="b203b-189">Select **Change status \> Complete**.</span></span>

## <a name="change-the-version-status-to-published"></a><span data-ttu-id="b203b-190">Изменение статуса версии на "Опубликовано"</span><span class="sxs-lookup"><span data-stu-id="b203b-190">Change the version status to Published</span></span>

- <span data-ttu-id="b203b-191">На странице **Функции электронных накладных** на вкладке **Версии** выберите **Изменить статус \> Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="b203b-191">On the **e-Invoicing Features** page, on the **Versions** tab, select **Change status \> Publish**.</span></span>

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="b203b-192">Публикация функции выставления накладных в электронной форме</span><span class="sxs-lookup"><span data-stu-id="b203b-192">Publish the e-Invoicing feature</span></span>

1. <span data-ttu-id="b203b-193">На странице **Функции электронного выставления накладных** выберите вкладку **Версии**, чтобы управлять состоянием функции **Накладные CFDI (MX)**.</span><span class="sxs-lookup"><span data-stu-id="b203b-193">On the **e-Invoicing Features** page, select the **Versions** tab to manage the status of the **CFDI invoices (MX)** feature.</span></span>
2. <span data-ttu-id="b203b-194">Чтобы изменить статус функции, выберите **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="b203b-194">Select **Change status** to change the status of the feature.</span></span>

![Изменение статуса функции электронных накладных](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing--integration-in-finance"></a><span data-ttu-id="b203b-196">Настройка интеграции модуля электронного выставления накладных в Finance</span><span class="sxs-lookup"><span data-stu-id="b203b-196">Set up Electronic invoicing  integration in Finance</span></span>

<span data-ttu-id="b203b-197">Для настройки модуля электронного выставления накладных в Finance выполняются следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="b203b-197">To set up Electronic invoicing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="b203b-198">Импортируйте модель данных электронной отчетности, сопоставление модели данных электронной отчетности и форматы, которые требуются для накладных CFDI.</span><span class="sxs-lookup"><span data-stu-id="b203b-198">Import the ER data model, the ER data model mapping, and the formats that are required for CFDI invoices.</span></span>
2. <span data-ttu-id="b203b-199">Настройте типы откликов для обновления накладных CFDI.</span><span class="sxs-lookup"><span data-stu-id="b203b-199">Configure response types for updating the CFDI invoices.</span></span> <span data-ttu-id="b203b-200">Эти типы откликов используются для ответа от сервера авторизованного поставщика сертификации (PAC).</span><span class="sxs-lookup"><span data-stu-id="b203b-200">These response types are used for the response from the authorized certification provider (PAC) server.</span></span>

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a><span data-ttu-id="b203b-201">Импортируйте модель данных электронной отчетности, сопоставление модели данных электронной отчетности и контекстные конфигурации для накладных CFDI.</span><span class="sxs-lookup"><span data-stu-id="b203b-201">Import the ER data model, ER data model mapping, and context configurations for CFDI invoices</span></span>

1. <span data-ttu-id="b203b-202">Войдите в Finance.</span><span class="sxs-lookup"><span data-stu-id="b203b-202">Sign in to Finance.</span></span>
2. <span data-ttu-id="b203b-203">В рабочей области **Электронная отчетность** в разделе **Поставщики конфигурации** выберите заголовок **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="b203b-203">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span> <span data-ttu-id="b203b-204">Убедитесь, что этот поставщик конфигурации имеет значение **Активный**.</span><span class="sxs-lookup"><span data-stu-id="b203b-204">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="b203b-205">Дополнительные сведения о том, как задать для поставщика состояние **Активный** см. в разделе [Создание поставщиков конфигураций и пометка их как активных](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="b203b-205">For information about how to set a provider to **Active**, see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="b203b-206">Выберите **Репозитории**.</span><span class="sxs-lookup"><span data-stu-id="b203b-206">Select **Repositories**.</span></span>
4. <span data-ttu-id="b203b-207">Выберите **Глобальный ресурс \> Открыть**.</span><span class="sxs-lookup"><span data-stu-id="b203b-207">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="b203b-208">Импортируйте **Модель накладных**, **Сопоставление модели накладных**, **Формат накладных CFDI (MX)**, **Формата запроса отмены накладной CFDI (MX)** и **Формат отмены накладной CFDI (MX)**.</span><span class="sxs-lookup"><span data-stu-id="b203b-208">Import **Invoice model**, **Invoice model mapping**, **CFDI invoice format (MX)**, **CFDI invoice cancelation request format (MX)**, and **CFDI invoice cancel format (MX)**.</span></span>

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a><span data-ttu-id="b203b-209">Включите функцию для обработки накладных CFDI</span><span class="sxs-lookup"><span data-stu-id="b203b-209">Turn on the feature for processing CFDI invoices</span></span>

1. <span data-ttu-id="b203b-210">Перейдите в раздел **Администрирование организации \> Настройка \> Параметры электронных документов**.</span><span class="sxs-lookup"><span data-stu-id="b203b-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="b203b-211">На вкладке **Функции** установите флажок **Включить** в строках для ссылок на функции **MX-00010** и **MX-00016**.</span><span class="sxs-lookup"><span data-stu-id="b203b-211">On the **Features** tab, select the **Enable** check box in the rows for feature references **MX-00010** and **MX-00016**.</span></span>

![Включение функций для обработки накладных CFDI](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a><span data-ttu-id="b203b-213">Импорт конфигураций электронной отчетности и настройка типов откликов для обновления накладных CFDI</span><span class="sxs-lookup"><span data-stu-id="b203b-213">Import ER configurations and set up the response types for updating CFDI invoices</span></span>

#### <a name="import-er-configurations"></a><span data-ttu-id="b203b-214">Импорт конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="b203b-214">Import ER configurations</span></span>

1. <span data-ttu-id="b203b-215">В рабочей области **Электронная отчетность** в разделе **Поставщики конфигурации** выберите заголовок **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="b203b-215">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span>
3. <span data-ttu-id="b203b-216">Выберите **Репозитории**.</span><span class="sxs-lookup"><span data-stu-id="b203b-216">Select **Repositories**.</span></span>
4. <span data-ttu-id="b203b-217">Выберите **Глобальный ресурс \> Открыть**.</span><span class="sxs-lookup"><span data-stu-id="b203b-217">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="b203b-218">Импортируйте **Модель ответного сообщения**, **Импорт журнала ошибок CFDI (MX)** и **Импорт ответного сообщения CFDI (MX)**.</span><span class="sxs-lookup"><span data-stu-id="b203b-218">Import **Response message model**, **CFDI error log import (MX)**, and **CFDI response message import (MX)**.</span></span>

#### <a name="set-up-the-response-types"></a><span data-ttu-id="b203b-219">Настройка типов ответов</span><span class="sxs-lookup"><span data-stu-id="b203b-219">Set up the response types</span></span>

1. <span data-ttu-id="b203b-220">Перейдите в раздел **Администрирование организации \> Настройка \> Параметры электронных документов**.</span><span class="sxs-lookup"><span data-stu-id="b203b-220">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="b203b-221">На вкладке **Электронный документ** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="b203b-221">On the **Electronic document** tab, select **Add**.</span></span>
3. <span data-ttu-id="b203b-222">Введите журнал накладных клиента, затем в поле **Имя таблицы** выберите накладную по проекту.</span><span class="sxs-lookup"><span data-stu-id="b203b-222">Enter the customer invoice journal, and then, in the **Table name** field, select the project invoice.</span></span>
4. <span data-ttu-id="b203b-223">Для каждой таблицы определите связанный контекст документа:</span><span class="sxs-lookup"><span data-stu-id="b203b-223">For each table, define a related document context:</span></span>

    - <span data-ttu-id="b203b-224">Для **журнала накладных клиента** введите **Контекст накладной клиента**.</span><span class="sxs-lookup"><span data-stu-id="b203b-224">For **Customer invoice journal**, enter **Customer invoice context**.</span></span>
    - <span data-ttu-id="b203b-225">Для **накладной по проекту** введите **Контекст накладной по проекту**.</span><span class="sxs-lookup"><span data-stu-id="b203b-225">For **Project invoice**, enter **Project invoice context**.</span></span>

4. <span data-ttu-id="b203b-226">Выберите **Типы откликов**, чтобы настроить типы откликов, которые могут быть возвращены из модуля электронного выставления накладных и включены в журнал накладных клиента или накладную по проекту.</span><span class="sxs-lookup"><span data-stu-id="b203b-226">Select **Response types** to configure the response types that can be returned from Electronic invoicing and included in a customer invoice journal or project invoice.</span></span>
5. <span data-ttu-id="b203b-227">Выберите **Создать**, затем в поле **Тип ответа** выберите **Ответ**.</span><span class="sxs-lookup"><span data-stu-id="b203b-227">Select **New**, and then, in the **Response type** field, select **Response**.</span></span>
6. <span data-ttu-id="b203b-228">В поле **Статус отправки** выберите **Ожидание**.</span><span class="sxs-lookup"><span data-stu-id="b203b-228">In the **Submission status** field, select **Pending**.</span></span>
7. <span data-ttu-id="b203b-229">В поле **Сопоставление моделей** выберите **Формат импорта ответного сообщения — сопоставление модели из ответного сообщения**.</span><span class="sxs-lookup"><span data-stu-id="b203b-229">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
8. <span data-ttu-id="b203b-230">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b203b-230">Select **Save**.</span></span>
9. <span data-ttu-id="b203b-231">Выберите **Создать**, затем в поле **Тип ответа** выберите **ResponseData**.</span><span class="sxs-lookup"><span data-stu-id="b203b-231">Select **New**, and then, in the **Response type** field, select **ResponseData**.</span></span>
10. <span data-ttu-id="b203b-232">В поле **Статус отправки** выберите **Ожидание**.</span><span class="sxs-lookup"><span data-stu-id="b203b-232">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="b203b-233">В поле **Сопоставление моделей** выберите **Формат импорта данных ответа CFDI (подробности) — импорт данных ответов**.</span><span class="sxs-lookup"><span data-stu-id="b203b-233">In the **Model mapping** field, select **CFDI response data import format (details) – Response data import**.</span></span>
12. <span data-ttu-id="b203b-234">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b203b-234">Select **Save**.</span></span>

## <a name="process-electronic-invoices-in-finance"></a><span data-ttu-id="b203b-235">Обработка электронных накладных в Finance</span><span class="sxs-lookup"><span data-stu-id="b203b-235">Process electronic invoices in Finance</span></span> 

<span data-ttu-id="b203b-236">Во время обработки накладных CFDI в Finance с помощью модуля электронного выставления накладных можно выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="b203b-236">During the processing of CFDI invoices in Finance through Electronic invoicing, you can perform the following tasks:</span></span>

- <span data-ttu-id="b203b-237">Отправка накладных CFDI.</span><span class="sxs-lookup"><span data-stu-id="b203b-237">Submit CFDI invoices.</span></span>
- <span data-ttu-id="b203b-238">Просмотр журналов выполнения отправки.</span><span class="sxs-lookup"><span data-stu-id="b203b-238">View the submission execution logs.</span></span>
- <span data-ttu-id="b203b-239">Отправка отмены накладной CFDI.</span><span class="sxs-lookup"><span data-stu-id="b203b-239">Submit the cancellation of a CFDI invoice.</span></span>

### <a name="submit-cfdi-invoices"></a><span data-ttu-id="b203b-240">Отправка накладных CFDI</span><span class="sxs-lookup"><span data-stu-id="b203b-240">Submit CFDI invoices</span></span>

<span data-ttu-id="b203b-241">После включения функции **Настраиваемая интеграция модуля электронного выставления накладных** процесс **Экспорт/импорт электронной накладной** (**Расчеты с клиентами \> Накладные \> Электронные накладные**) больше не может использоваться для отправки накладных CFDI.</span><span class="sxs-lookup"><span data-stu-id="b203b-241">After you turn on the **Configurable Electronic invoicing integration** feature, the **Export/Import electronic invoice** process (**Accounts receivable \> Invoices \> E-invoices**) for submitting CFDI invoices can no longer be used.</span></span> <span data-ttu-id="b203b-242">Он заменяется новым процессом с именем **Отправка электронных документов**.</span><span class="sxs-lookup"><span data-stu-id="b203b-242">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="b203b-243">Перед созданием нового процесса **Отправка электронных документов** Убедитесь, что настройка, необходимая для электронных накладных для Мексики, была завершена.</span><span class="sxs-lookup"><span data-stu-id="b203b-243">Before you use the new **Submit electronic documents** process, verify that the setup that is required for Mexican e-invoices was completed.</span></span> <span data-ttu-id="b203b-244">Дополнительные сведения см. в разделе [Макет CFDI версии 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span><span class="sxs-lookup"><span data-stu-id="b203b-244">For more information, see [CFDI layout version 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span></span>

1. <span data-ttu-id="b203b-245">Перейдите в раздел **Администрирование организации \> Периодические задачи \> Электронные документы \> Отправка электронных документов**.</span><span class="sxs-lookup"><span data-stu-id="b203b-245">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="b203b-246">Для первой отправки любого документа обязательно установите для параметра **Повторно отправить документы** значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="b203b-246">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="b203b-247">Если необходимо повторно отправить документ через службу, установите для этого параметра значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="b203b-247">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="b203b-248">На экспресс-вкладке **Включаемые записи** выберите **Фильтр**, чтобы открыть диалоговое окно **Запрос**, в котором можно построить запрос для выбора повторно отправляемых документов.</span><span class="sxs-lookup"><span data-stu-id="b203b-248">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![Отправка документа CFDI](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> <span data-ttu-id="b203b-250">При первой попытке отправить документ через службу вам будет предложено подтвердить связь с модулем электронного выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="b203b-250">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with Electronic invoicing.</span></span> <span data-ttu-id="b203b-251">Выберите **Щелкните здесь для подключения к службе отправки электронных документов**.</span><span class="sxs-lookup"><span data-stu-id="b203b-251">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-submission-logs"></a><span data-ttu-id="b203b-252">Просмотр журналов отправки</span><span class="sxs-lookup"><span data-stu-id="b203b-252">View submission logs</span></span>

<span data-ttu-id="b203b-253">Можно просмотреть журналы отправки для всех отправленных документов или только для одного отправленного документа.</span><span class="sxs-lookup"><span data-stu-id="b203b-253">You can view the submission logs for all submitted documents or for just one submitted document.</span></span>

#### <a name="view-all-submission-logs"></a><span data-ttu-id="b203b-254">Просмотр всех журналов отправки</span><span class="sxs-lookup"><span data-stu-id="b203b-254">View all submission logs</span></span>

<span data-ttu-id="b203b-255">После включения функции **Настраиваемая интеграция модуля электронного выставления накладных** будет доступна новая страница, позволяющая отслеживать процесс отправки документа.</span><span class="sxs-lookup"><span data-stu-id="b203b-255">After you turn on the **Configurable Electronic invoicing integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="b203b-256">Можно использовать эту страницу, чтобы просмотреть журналы отправки для всех отправленных документов.</span><span class="sxs-lookup"><span data-stu-id="b203b-256">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="b203b-257">Перейдите в раздел **Администрирование организации \> Периодические задачи \> Электронные документы \> Журнал отправки электронных документов**.</span><span class="sxs-lookup"><span data-stu-id="b203b-257">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="b203b-258">В поле **Тип документов** выберите **Журнал накладных клиента**, чтобы отфильтровать необходимые электронные документы.</span><span class="sxs-lookup"><span data-stu-id="b203b-258">In the **Document type** field, select **Customer invoice journal** to filter for the required electronic documents.</span></span>

    ![Выбор типа документов для просмотра журналов отправки](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. <span data-ttu-id="b203b-260">В области действий выберите **Запросы \> Сведения об отправке** для просмотра сведений о журналах выполнения отправки.</span><span class="sxs-lookup"><span data-stu-id="b203b-260">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Просмотр сведений журнала отправки](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

<span data-ttu-id="b203b-262">Сведения в журналах отправки делятся между тремя экспресс-вкладками:</span><span class="sxs-lookup"><span data-stu-id="b203b-262">The information in the submission logs is divided among three FastTabs:</span></span>

- <span data-ttu-id="b203b-263">**Действия по обработке** — на этой экспресс-вкладке отображается журнал выполнения для действий, настроенных в версии функции, которая была настроена в RCS.</span><span class="sxs-lookup"><span data-stu-id="b203b-263">**Processing actions** – This FastTab shows the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="b203b-264">Столбец **Состояние** показывает, было ли действие успешно выполнено.</span><span class="sxs-lookup"><span data-stu-id="b203b-264">The **Status** column shows whether the action was successfully run.</span></span>
- <span data-ttu-id="b203b-265">**Файлы действий** — на этой экспресс-вкладке отображаются промежуточные файлы, созданные во время выполнения действий.</span><span class="sxs-lookup"><span data-stu-id="b203b-265">**Action files** – This FastTab shows the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="b203b-266">Можно выбрать **Просмотр**, чтобы загрузить и просмотреть файл.</span><span class="sxs-lookup"><span data-stu-id="b203b-266">You can select **View** to download and view the file.</span></span>
- <span data-ttu-id="b203b-267">**Журнал действий обработки** — на этой экспресс-вкладке отображаются результаты взаимодействия между модулем электронного выставления накладных и целевой веб-службой.</span><span class="sxs-lookup"><span data-stu-id="b203b-267">**Processing action log** – This FastTab shows the results of the communication between Electronic invoicing and the target web service.</span></span> <span data-ttu-id="b203b-268">Он также показывает, что было возвращено после обработки веб-службой.</span><span class="sxs-lookup"><span data-stu-id="b203b-268">It also shows what was returned by the processing from the web service.</span></span> <span data-ttu-id="b203b-269">В столбце **Код ошибки** отображается код возврата, возвращенный веб-службой авторизации.</span><span class="sxs-lookup"><span data-stu-id="b203b-269">The **Error code** column shows the return code that was returned by the authorization web service.</span></span>

<span data-ttu-id="b203b-270">Когда отправленная накладная CFDI авторизована, ее статус обновляется на **Утверждено**.</span><span class="sxs-lookup"><span data-stu-id="b203b-270">When the submitted CFDI invoice is authorized, its status is updated to **Approved**.</span></span>

#### <a name="view-submission-logs-from-cfdi-invoices"></a><span data-ttu-id="b203b-271">Просмотр журналов отправки из накладных CFDI</span><span class="sxs-lookup"><span data-stu-id="b203b-271">View submission logs from CFDI invoices</span></span>

<span data-ttu-id="b203b-272">После включения функции **Настраиваемая интеграция модуля электронного выставления накладных** можно также просмотреть журналы отправки из накладных CFDI.</span><span class="sxs-lookup"><span data-stu-id="b203b-272">After you turn on the **ConfigurableElectronic invoicing integration** feature, you can also view the submission logs from CFDI invoices.</span></span>

1. <span data-ttu-id="b203b-273">Перейдите в раздел **Расчеты с клиентами \> Запросы и отчеты \> CFDI (электронные накладные)**.</span><span class="sxs-lookup"><span data-stu-id="b203b-273">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="b203b-274">Выберите накладную CFDI, которая была отправлена после включения функции **Настраиваемая интеграция модуля электронного выставления накладных**.</span><span class="sxs-lookup"><span data-stu-id="b203b-274">Select a CFDI invoice that was submitted after the **Configurable Electronic invoicing integration** feature was turned on.</span></span>
3. <span data-ttu-id="b203b-275">На панели операций откройте вкладку **Журнал** и выберите **Журнал электронных документов**.</span><span class="sxs-lookup"><span data-stu-id="b203b-275">On the Action Pane, on the **History** tab, select **Electronic document log**.</span></span>

![Просмотр журналов отправки из накладных CFDI](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> <span data-ttu-id="b203b-277">Для накладных CFDI, которые были отправлены до включения функции **Настраиваемая интеграция модуля электронного выставления накладных**, кнопка **Журнал** доступна.</span><span class="sxs-lookup"><span data-stu-id="b203b-277">For CFDI invoices that were submitted before the **Configurable Electronic invoicing integration** feature was turned on, the **History** button is available.</span></span> <span data-ttu-id="b203b-278">Кнопка **Журнал** недоступна для накладных CFDI, которые были отправлены после включения функции **Настраиваемая интеграция модуля электронного выставления накладных**.</span><span class="sxs-lookup"><span data-stu-id="b203b-278">The **History** button isn't available for CFDI invoices that were submitted after the **Configurable Electronic invoicing integration** feature was turned on.</span></span>

### <a name="submit-cancellation-of-cfdi-invoices"></a><span data-ttu-id="b203b-279">Отправка отмены накладных CFDI</span><span class="sxs-lookup"><span data-stu-id="b203b-279">Submit cancellation of CFDI invoices</span></span>

<span data-ttu-id="b203b-280">После включения функции **Настраиваемая интеграция модуля электронного выставления накладных** нельзя будет использовать старый процесс отмены накладных CFDI.</span><span class="sxs-lookup"><span data-stu-id="b203b-280">After you turn on the **Configurable Electronic invoicing integration** feature, the old process for canceling CFDI invoices can no longer be used.</span></span> <span data-ttu-id="b203b-281">Он заменяется новым процессом отмены, который внедрен на странице **Журнал отправки электронных документов**.</span><span class="sxs-lookup"><span data-stu-id="b203b-281">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

1. <span data-ttu-id="b203b-282">Перейдите в раздел **Расчеты с клиентами \> Запросы и отчеты \> CFDI (электронные накладные)**.</span><span class="sxs-lookup"><span data-stu-id="b203b-282">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="b203b-283">Если накладная CFDI имеет статус **Утверждено**, выберите **Функции \> Отменить CFDI**.</span><span class="sxs-lookup"><span data-stu-id="b203b-283">If the CFDI invoice has a status of **Approved**, select **Functions \> Cancel CFDI**.</span></span>
3. <span data-ttu-id="b203b-284">Перейдите в раздел **Администрирование организации \> Периодические задачи \> Электронные документы \> Журнал отправки электронных документов**.</span><span class="sxs-lookup"><span data-stu-id="b203b-284">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
4. <span data-ttu-id="b203b-285">Выберите накладную CFDI, затем выберите **Функции \> Отправить связанные отправки**.</span><span class="sxs-lookup"><span data-stu-id="b203b-285">Select the CFDI invoice, and then select **Functions \> Send related submissions**.</span></span>
5. <span data-ttu-id="b203b-286">Введите описание для соответствующей отправки, затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b203b-286">Enter a description for the related submission, and then select **OK**.</span></span>

#### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="b203b-287">Просмотр журналов отправки отмены</span><span class="sxs-lookup"><span data-stu-id="b203b-287">View cancellation submission logs</span></span>

1. <span data-ttu-id="b203b-288">Перейдите в раздел **Администрирование организации \> Периодические задачи \> Электронные документы \> Журнал отправки электронных документов**.</span><span class="sxs-lookup"><span data-stu-id="b203b-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="b203b-289">В поле **Тип документов** выберите **Журнал накладных клиента**, чтобы отфильтровать только документы журнала накладных клиентов.</span><span class="sxs-lookup"><span data-stu-id="b203b-289">In the **Document type** field, select **Customer invoice journal** to filter for customer invoice journal documents only.</span></span>
3. <span data-ttu-id="b203b-290">Выберите накладную CFDI, затем в области действий выберите **Запросы \> Связанная отправка**</span><span class="sxs-lookup"><span data-stu-id="b203b-290">Select the CFDI invoice, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="b203b-291">На странице **Связанные отправки** отображаются все связанные отправки и их статус отправки для данной накладной CFDI.</span><span class="sxs-lookup"><span data-stu-id="b203b-291">The **Related submissions** page shows all related submissions, and their submission status, for a given CFDI invoice.</span></span> <span data-ttu-id="b203b-292">На следующем рисунке первая строка представляет собой отправку, которая запрашивала утверждение накладной CFDI.</span><span class="sxs-lookup"><span data-stu-id="b203b-292">In the following illustration, the first line represents the submission that requested approval of the CFDI invoice.</span></span> <span data-ttu-id="b203b-293">Вторая строка представляет собой отправку, которая отменила эту накладную CFDI.</span><span class="sxs-lookup"><span data-stu-id="b203b-293">The second line represents the submission that canceled that CFDI invoice.</span></span>

    ![Просмотр журналов отправки отмены](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. <span data-ttu-id="b203b-295">В области действий выберите **Запросы \> Сведения об отправке** для просмотра сведений о журналах выполнения отправки.</span><span class="sxs-lookup"><span data-stu-id="b203b-295">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Просмотр сведений журнала отправки отмены](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="b203b-297">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="b203b-297">Privacy notice</span></span>
<span data-ttu-id="b203b-298">Для включения функции **мексиканских электронных накладных (MX) CFDI** может потребоваться отправка ограниченных данных, которые включают код налоговой регистрации организации.</span><span class="sxs-lookup"><span data-stu-id="b203b-298">Enabling the **CFDI Mexican electronic invoice (MX)** feature may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="b203b-299">Они будут переданы сторонним агентствам, которые уполномочены налоговыми органами для целей отправки электронных накладных в этот налоговый орган в заранее определенном формате, требуемом для интеграции с веб-службой правительственного учреждения.</span><span class="sxs-lookup"><span data-stu-id="b203b-299">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="b203b-300">Администратор может включать и отключать функцию **мексиканских электронных накладных (MX) CFDI** путем перехода к разделу **Администрирование организации \> Настройка \> Параметры электронных документов**.</span><span class="sxs-lookup"><span data-stu-id="b203b-300">An administrator can enable and disable the **CFDI Mexican electronic invoice (MX)** feature by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="b203b-301">Перейдите на вкладку **Функции**, выберите строки, содержащие функции **мексиканских электронных накладных (MX) CFDI**, затем выполните соответствующие действия по выбору.</span><span class="sxs-lookup"><span data-stu-id="b203b-301">Select the **Features** tab, select the rows containing the **CFDI Mexican electronic invoice (MX)** feature, and then make the appropriate selection.</span></span> <span data-ttu-id="b203b-302">На данные, импортируемые из этих внешних систем в данную веб-службу Dynamics 365, распространяется наше [заявление о конфиденциальности](https://go.microsoft.com/fwlink/?LinkId=512132).</span><span class="sxs-lookup"><span data-stu-id="b203b-302">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="b203b-303">Дополнительные сведения см. в разделах "Уведомление о конфиденциальности" в документации по компонентам, относящимся к конкретной стране.</span><span class="sxs-lookup"><span data-stu-id="b203b-303">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b203b-304">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b203b-304">Additional resources</span></span>

- [<span data-ttu-id="b203b-305">Обзор электронного выставления накладных</span><span class="sxs-lookup"><span data-stu-id="b203b-305">Electronic invoicing overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="b203b-306">Начало работы с электронным выставлением накладных</span><span class="sxs-lookup"><span data-stu-id="b203b-306">Get started with Electronic invoicing</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="b203b-307">Настройка электронного выставления накладных</span><span class="sxs-lookup"><span data-stu-id="b203b-307">Set up Electronic invoicing</span></span>](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
