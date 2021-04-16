---
title: Декларация подоходного налога для Египта
description: В этой теме объясняется, как настроить и создать декларации подоходного налога для Египта.
author: sndray
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4e3d68ac003fabaa504ffe81b8bf2f7ff8d7538d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839800"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a><span data-ttu-id="70c1f-103">Декларация подоходного налога для Египта (EG-00005)</span><span class="sxs-lookup"><span data-stu-id="70c1f-103">Withholding tax declaration for Egypt (EG-00005)</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a><span data-ttu-id="70c1f-104">Обзор</span><span class="sxs-lookup"><span data-stu-id="70c1f-104">Overview</span></span>
<span data-ttu-id="70c1f-105">В этой теме объясняется, как настроить и создать декларацию подоходного налога и формы декларации подоходного налога 41 и 11 для юридических лиц в Египте</span><span class="sxs-lookup"><span data-stu-id="70c1f-105">This topic explains how to set up and generate the withholding tax declaration and the withholding tax declaration forms 41 and 11 for legal entities in Egypt</span></span> 

<span data-ttu-id="70c1f-106">Все египетские организации должны готовить форму 41, которая суммирует все налоги, удерживаемые с местных поставщиков и поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="70c1f-106">All Egyptian entities must prepare the form  41 which summarizes all taxes that are retained from local suppliers and service providers.</span></span> <span data-ttu-id="70c1f-107">В дополнение к форме 41 необходимо создать форму 11, чтобы подробно описать удержанный налог с иностранных поставщиков.</span><span class="sxs-lookup"><span data-stu-id="70c1f-107">In addition to form 41, form 11 must be generated to detail all of the retained taxed from foreign providers.</span></span> 

<span data-ttu-id="70c1f-108">Отчет **Декларация подоходного налога** в Dynamics 365 Finance включает следующие отчеты:</span><span class="sxs-lookup"><span data-stu-id="70c1f-108">The **Withholding tax declaration** report in Dynamics 365 Finance includes the following reports:</span></span>

- <span data-ttu-id="70c1f-109">№ формы декларации</span><span class="sxs-lookup"><span data-stu-id="70c1f-109">Declaration form No.</span></span> <span data-ttu-id="70c1f-110">41</span><span class="sxs-lookup"><span data-stu-id="70c1f-110">41</span></span>
- <span data-ttu-id="70c1f-111">№ формы декларации</span><span class="sxs-lookup"><span data-stu-id="70c1f-111">Declaration form No.</span></span> <span data-ttu-id="70c1f-112">11</span><span class="sxs-lookup"><span data-stu-id="70c1f-112">11</span></span>
    
    
## <a name="prerequisites"></a><span data-ttu-id="70c1f-113">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="70c1f-113">Prerequisites</span></span>
<span data-ttu-id="70c1f-114">Основной адрес юридического лица должен быть в Египте.</span><span class="sxs-lookup"><span data-stu-id="70c1f-114">The primary address of the legal entity must be in Egypt.</span></span>
<span data-ttu-id="70c1f-115">В рабочей области **Управление функциями** следующая функция должна быть включена:</span><span class="sxs-lookup"><span data-stu-id="70c1f-115">In the **Feature management** workspace, the following feature must be enabled:</span></span>

   - <span data-ttu-id="70c1f-116">**Глобальный подоходный налог**</span><span class="sxs-lookup"><span data-stu-id="70c1f-116">**Global withholding tax**</span></span>

<span data-ttu-id="70c1f-117">Дополнительные сведения о включении этих функций см. в разделе [Обзор управления функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="70c1f-117">For more information about how to enable features, see [Feature management overview.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span></span>

1. <span data-ttu-id="70c1f-118">Перейдите в раздел **Налог** > **Настройка** > **Параметры** > **Параметры главной книги**, затем на вкладке **Подоходный налог** установите для параметра **Включить глобальный подоходный налог** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="70c1f-118">Go to **Tax** > **Setup** > **Parameters** > **General ledger parameters**, and on the **Withholding tax** tab, set **Enable global withholding tax** to **Yes**.</span></span>
2. <span data-ttu-id="70c1f-119">В рабочей области **Электронная отчетность** импортируйте из репозитория следующий форматы электронной отчетности:</span><span class="sxs-lookup"><span data-stu-id="70c1f-119">In the **Electronic reporting** workspace, import the following Electronic reporting formats from the repository:</span></span>

    - <span data-ttu-id="70c1f-120">Excel декларации подоходного налога (EG)</span><span class="sxs-lookup"><span data-stu-id="70c1f-120">WHT Declaration Excel (EG)</span></span>

    > [!NOTE]
    > <span data-ttu-id="70c1f-121">Вышеприведенный формат основан на **модели налоговой декларации** и использует **сопоставление модели налоговой декларации**.</span><span class="sxs-lookup"><span data-stu-id="70c1f-121">The format above is based on the **Tax declaration model** and uses the **Tax declaration model mapping**.</span></span> <span data-ttu-id="70c1f-122">Эта дополнительная конфигурация будет импортирована автоматически.</span><span class="sxs-lookup"><span data-stu-id="70c1f-122">This additional configuration is automatically imported.</span></span>

<span data-ttu-id="70c1f-123">Дополнительные сведения об импорте конфигураций электронной отчетности см. в разделе [Загрузка конфигураций электронной отчетности из Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="70c1f-123">For more information about how to import Electronic reporting configurations, see [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

## <a name="download-electronic-reporting-configurations"></a><span data-ttu-id="70c1f-124">Загрузка конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="70c1f-124">Download Electronic reporting configurations</span></span>

<span data-ttu-id="70c1f-125">Реализация форм декларации подоходного налога для Египта основана на конфигурациях электронной отчетности (ER).</span><span class="sxs-lookup"><span data-stu-id="70c1f-125">The implementation of the WHT declaration forms for Egypt is based on Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="70c1f-126">Дополнительные сведения о возможностях и концепциях настраиваемой отчетности см. в разделе [Электронная отчетность](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="70c1f-126">For more information about the capabilities and concepts of configurable reporting, see [Electronic reporting](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

<span data-ttu-id="70c1f-127">Для сред производства и приемочного тестирования пользователем (UAT) следуйте инструкциям в теме [Загрузка конфигураций электронной отчетности из Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="70c1f-127">For production and user acceptance testing (UAT) environments, follow the instructions in the topic, [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

<span data-ttu-id="70c1f-128">Для создания деклараций подоходного налога в египетской организации необходимо загрузить следующие конфигурации:</span><span class="sxs-lookup"><span data-stu-id="70c1f-128">To generate the Withholding declarations in an Egyptian legal entity, you need to upload the following configurations:</span></span>

- <span data-ttu-id="70c1f-129">Tax declaration model.version.82.xml или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="70c1f-129">Tax declaration model.version.82.xml or later version</span></span>
- <span data-ttu-id="70c1f-130">Tax declaration model mapping.version.82.133.xml или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="70c1f-130">Tax declaration model mapping.version.82.133.xml or a later version</span></span>
- <span data-ttu-id="70c1f-131">WHT Declaration Excel (EG).version.82.21 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="70c1f-131">WHT Declaration Excel (EG).version.82.21  or a later version</span></span>

<span data-ttu-id="70c1f-132">После окончания загрузки конфигураций электронной отчетности из Lifecycle Services (LCS) или глобального репозитория выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="70c1f-132">After you finish downloading the ER configurations from Lifecycle Services (LCS) or the global repository, complete the following steps.</span></span>

1. <span data-ttu-id="70c1f-133">Перейдите в раздел рабочей области **Электронная отчетность** и выберите плитку **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="70c1f-133">Go to the **Electronic reporting** workspace and select the **Reporting configurations** tile.</span></span>
1. <span data-ttu-id="70c1f-134">На странице **Конфигурации** на панели действий выберите **Exchange > Загрузить из XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="70c1f-134">On the **Configurations** page, on the Action Pane, select **Exchange > Load from XML file**.</span></span>
1. <span data-ttu-id="70c1f-135">Отправьте все файлы в том порядке, в котором они указаны в предыдущих пунктах.</span><span class="sxs-lookup"><span data-stu-id="70c1f-135">Upload all the files in the order in which they are listed in the previous bullets.</span></span> <span data-ttu-id="70c1f-136">После загрузки всех конфигураций дерево конфигурации должно присутствовать в Финансах.</span><span class="sxs-lookup"><span data-stu-id="70c1f-136">After all of the configurations are uploaded, the configuration tree should be present in Finance.</span></span>

## <a name="set-up-application-specific-parameters"></a><span data-ttu-id="70c1f-137">Настройка параметров конкретного приложения</span><span class="sxs-lookup"><span data-stu-id="70c1f-137">Set up application-specific parameters</span></span>

<span data-ttu-id="70c1f-138">Параметр параметров конкретного приложения, позволяет пользователям определять критерии классификации и расчета налоговых проводок в каждой строке сформированного отчета, в зависимости от конфигурации **группы номенклатур подоходного налога** или других критериев, установленных в определении поиска.</span><span class="sxs-lookup"><span data-stu-id="70c1f-138">The application-specific parameters option lets users establish the criteria of how the tax transactions will be classified and calculated in each line of a generated report depending on the configuration of **withholding tax item group** or other criteria established in the definition of lookup.</span></span>

<span data-ttu-id="70c1f-139">Форма "декларирование подоходного налога" 41 включает столбец, в котором проводка по подоходному налогу должна классифицироваться в соответствии с классификацией налогового органа с именем **Тип кода скидки**.</span><span class="sxs-lookup"><span data-stu-id="70c1f-139">Withholding declaration form 41 includes a specific column where the withholding tax transaction must be classified in accordance with the tax authority classification named **Discount code type**.</span></span> <span data-ttu-id="70c1f-140">Вместо включения этих новых классификаций в качестве новые данные при разноске проводок классификации будут определяться на основе различных уточняющих запросов, введенных в **конфигурации** > **Настройка параметров для конкретного приложения** > **Настройка** в соответствии с требованиями отчетов по подоходному налогу для Египет.</span><span class="sxs-lookup"><span data-stu-id="70c1f-140">Instead of including these new classifications as new entry data when the transactions are posted, the classifications will be determined based on the different lookups introduced in **Configurations** > **Set up application-specific parameters** > **Setup** to meet the requirements of withholding reports for Egypt.</span></span> 

<span data-ttu-id="70c1f-141">Следующая конфигурация используется для классификации проводок в отчете декларирование подоходного налога форма 41:</span><span class="sxs-lookup"><span data-stu-id="70c1f-141">The following configuration is used to classify the transactions in the Withholding declaration form 41 report:</span></span>

- <span data-ttu-id="70c1f-142">**DiscountTaxTypeLookup**-> столбец № 18</span><span class="sxs-lookup"><span data-stu-id="70c1f-142">**DiscountTaxTypeLookup**-> Column No 18</span></span> 

<span data-ttu-id="70c1f-143">Выполните следующие действия, чтобы настроить различные подстановки, используемые для создания декларации по подоходному налогу и соответствующих отчетов по книгам.</span><span class="sxs-lookup"><span data-stu-id="70c1f-143">Complete the following steps to set up the different lookups used to generate the WHT declaration and related books reports.</span></span> 

1. <span data-ttu-id="70c1f-144">В рабочей области **электронной отчетности** выберите **конфигурации** > **Настройка**, чтобы настроить правила, определяющие, как проводки классифицируются в отчете о декларации по подоходному налогу.</span><span class="sxs-lookup"><span data-stu-id="70c1f-144">In the **Electronic reporting** workspace, select **Configurations** > **Setup** to set up the rules to identify how transactions are classified in the WHT declaration report.</span></span> 
2. <span data-ttu-id="70c1f-145">Выберите текущую версию и на экспресс-вкладке **Поиск** выберите имя поиска.</span><span class="sxs-lookup"><span data-stu-id="70c1f-145">Select the current version, and on the **Lookups** FastTab, select the lookup name.</span></span> <span data-ttu-id="70c1f-146">Например, **DiscountTaxTypeLookup**.</span><span class="sxs-lookup"><span data-stu-id="70c1f-146">For example, **DiscountTaxTypeLookup**.</span></span> <span data-ttu-id="70c1f-147">Этот поиск определяет список типов скидок, необходимых для налогового органа.</span><span class="sxs-lookup"><span data-stu-id="70c1f-147">This lookup identifies the list of discount types required by the tax authority.</span></span>
3. <span data-ttu-id="70c1f-148">На экспресс-вкладке **условия** выберите **Добавить** и в новой строке столбца **результат поиска** выберите соответствующую строку, представляющую классификацию в **столбце 18**.</span><span class="sxs-lookup"><span data-stu-id="70c1f-148">On the **Conditions** FastTab, select **Add** and in the new line in the **Lookup result** column, select the related line that represents the classification in the **Column 18**.</span></span>
4. <span data-ttu-id="70c1f-149">В столбце **группы номенклатур подоходного налога** выберите связанный код, который используется для идентификации классификации.</span><span class="sxs-lookup"><span data-stu-id="70c1f-149">In the **Withholding tax item group** column, select the related code that's used to identify the classification.</span></span> <span data-ttu-id="70c1f-150">Например, **разрешенная скидка**.</span><span class="sxs-lookup"><span data-stu-id="70c1f-150">For example, **Allowed discount**.</span></span>  
5. <span data-ttu-id="70c1f-151">Повторите шаги 3 и 4 для всех доступных поисков.</span><span class="sxs-lookup"><span data-stu-id="70c1f-151">Repeat steps 3 and 4 for all available lookups.</span></span>
6. <span data-ttu-id="70c1f-152">Снова выберите **Добавить** для включения конечной строки записи, а в столбце **Результат поиска** выберите **неприменимо**.</span><span class="sxs-lookup"><span data-stu-id="70c1f-152">Select **Add** again to include the final record line, and in the **Lookup result** column, select **Not applicable**.</span></span> 
7. <span data-ttu-id="70c1f-153">В остальных столбцах выберите **не пусто**.</span><span class="sxs-lookup"><span data-stu-id="70c1f-153">In the remaining columns, select **Not blank**.</span></span> 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a><span data-ttu-id="70c1f-154">Настройте параметры главной книги</span><span class="sxs-lookup"><span data-stu-id="70c1f-154">Set up General ledger parameters</span></span>

<span data-ttu-id="70c1f-155">Чтобы создать отчет формы декларации подоходного налога в Microsoft Excel, укажите формат электронной отчетности на странице **Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="70c1f-155">To generate the WHT declaration form reports in Microsoft Excel, define an ER format on the **General ledger parameters** page.</span></span>

1. <span data-ttu-id="70c1f-156">Перейти к **Налог** > **Настройка** > **Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="70c1f-156">Go to **Tax** > **Setup** > **General ledger parameters**.</span></span>
2. <span data-ttu-id="70c1f-157">На вкладке **подоходный налог** в поле **Сопоставление формата декларации подоходного налога** выберите **Excel декларации подоходного налога (EG)**.</span><span class="sxs-lookup"><span data-stu-id="70c1f-157">On the **Withholding tax** tab, in the **WHT declaration format mapping** field, select **WHT Declaration Excel (EG)**.</span></span> <span data-ttu-id="70c1f-158">Если оставить это поле пустым, стандартный налоговый отчет будет создан в формате SSRS.</span><span class="sxs-lookup"><span data-stu-id="70c1f-158">If you leave the field blank, the standard sales tax report will be generated in SSRS format.</span></span>


![Форма декларации](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a><span data-ttu-id="70c1f-160">Создание форм декларации подоходного налога</span><span class="sxs-lookup"><span data-stu-id="70c1f-160">Generate the Withholding declaration forms</span></span>
<span data-ttu-id="70c1f-161">Процесс подготовки и отправки формы декларации подоходного налога за конкретный период основан на проводках по подоходному налогу, разнесенных в ходе задания по сопоставлению и разноске платежа.</span><span class="sxs-lookup"><span data-stu-id="70c1f-161">The process of preparing and submitting a Withholding declaration form for a specific period is based on the withholding tax transactions posted during the settle and post payment tax job.</span></span> <span data-ttu-id="70c1f-162">Дополнительные сведения о глобальном подоходном налоге см. в разделе [глобальный подоходный налог](../general-ledger/global-withholding-tax-overview.md).</span><span class="sxs-lookup"><span data-stu-id="70c1f-162">For more information about global withholding tax, see [Global withholding tax](../general-ledger/global-withholding-tax-overview.md).</span></span>

<span data-ttu-id="70c1f-163">Выполните следующие шаги для создания налоговой декларации.</span><span class="sxs-lookup"><span data-stu-id="70c1f-163">Complete the following steps to generate the tax declaration report.</span></span>

1. <span data-ttu-id="70c1f-164">Переход к **Налог** > **декларации** > **подоходный налог** > \**платеж подоходного налога*.</span><span class="sxs-lookup"><span data-stu-id="70c1f-164">Go to **Tax** > **Declarations** > **Withholding tax** > \**Withholding tax payment*.</span></span>
2. <span data-ttu-id="70c1f-165">Выберите период сопоставления, а затем выберите начальную дату для отчета.</span><span class="sxs-lookup"><span data-stu-id="70c1f-165">Select the settlement period and then select the from date for the report.</span></span> 
3. <span data-ttu-id="70c1f-166">Введите дата проводки и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="70c1f-166">Enter the transaction date and then select **OK**.</span></span>
4. <span data-ttu-id="70c1f-167">В открывшемся диалоговом окне выберите один или несколько типов форм **Форма № 41**, **Форма № 11** или **нет**.</span><span class="sxs-lookup"><span data-stu-id="70c1f-167">In the dialog box that opens, select one or more of the form types \*\*Form No 41 \*\*, **Form No 11**, or **None**.</span></span> <span data-ttu-id="70c1f-168">Если выбрано значение **нет**, создается стандартный отчет.</span><span class="sxs-lookup"><span data-stu-id="70c1f-168">If you select **None**, the standard report is generated.</span></span> 
5. <span data-ttu-id="70c1f-169">Выберите язык.</span><span class="sxs-lookup"><span data-stu-id="70c1f-169">Select the language.</span></span> <span data-ttu-id="70c1f-170">Все отчеты переводятся в **en-us** и **ar-eg**.</span><span class="sxs-lookup"><span data-stu-id="70c1f-170">All reports are translated in **en-us** and **ar-eg**.</span></span>
6. <span data-ttu-id="70c1f-171">Введите ветвь и имя банка, в котором будет оплачен налоговый платеж.</span><span class="sxs-lookup"><span data-stu-id="70c1f-171">Enter the branch and name of the bank where the tax payment will be paid.</span></span>
7. <span data-ttu-id="70c1f-172">Выберите тип бизнеса, а затем введите номера чеков и документов.</span><span class="sxs-lookup"><span data-stu-id="70c1f-172">Select the business type and then enter the check and document numbers.</span></span> 
8. <span data-ttu-id="70c1f-173">Введение типа объекта.</span><span class="sxs-lookup"><span data-stu-id="70c1f-173">Enter the entity type.</span></span> 
9. <span data-ttu-id="70c1f-174">Ввод имени лица, зарегистрированного для назначения формы, и нажмите кнопку **ОК**, чтобы подтвердить создание отчета.</span><span class="sxs-lookup"><span data-stu-id="70c1f-174">Enter the name of person registered to assign the form and select **OK** to confirm the report generation.</span></span> 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
