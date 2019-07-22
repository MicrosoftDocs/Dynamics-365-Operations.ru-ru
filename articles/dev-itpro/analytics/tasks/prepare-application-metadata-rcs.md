---
title: Подготовка метаданных приложения для использования в RCS
description: Шаги в этом разделе описывают, как пользователь может создать новую конфигурацию электронной отчетности (ER), которая содержит метаданные приложения Finance and Operations для разработки конфигураций сопоставления модели ER в службе Regulatory Configuration Service (RCS).
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1bd2298240fa789762a350e90888201c5a7ce45
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726991"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a><span data-ttu-id="cdcef-103">Подготовка метаданных приложения для использования в RCS</span><span class="sxs-lookup"><span data-stu-id="cdcef-103">Prepare application metadata to be used in RCS</span></span>
[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cdcef-104">Следующие шаги описывают, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать новую конфигурацию электронной отчетности (ER), которая содержит метаданные приложения Microsoft Dynamics 365 for Finance and Operations для разработки конфигураций сопоставления модели ER в службе Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="cdcef-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains Microsoft Dynamics 365 for Finance and Operations application metadata for designing ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="cdcef-105">Эта конфигурация будет использоваться для разработки примера конфигурации сопоставления модели ER для доступа к проводкам внешней торговли.</span><span class="sxs-lookup"><span data-stu-id="cdcef-105">This configuration will be used for designing a sample ER model mapping configuration to access foreign trade transactions.</span></span> <span data-ttu-id="cdcef-106">В этом примере вам предстоит создать поставщика конфигурации для примера компании Litware, Inc. Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="cdcef-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company.</span></span> <span data-ttu-id="cdcef-107">Для выполнения этих шагов необходимо сначала выполнить шаги в теме [Создание поставщиков конфигурации и установка их в качестве активных](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="cdcef-107">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cdcef-108">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="cdcef-108">Prerequisites</span></span>
1.  <span data-ttu-id="cdcef-109">Перейдите в раздел **Управление организацией** > **Рабочие области** > **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-109">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2.  <span data-ttu-id="cdcef-110">Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как **Активный**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="cdcef-111">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре [Создание поставщиков конфигурации и пометка их как активных](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="cdcef-111">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3.  <span data-ttu-id="cdcef-112">Щелкните **Конфигурации метаданных**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-112">Click **Metadata configurations**.</span></span> 
4.  <span data-ttu-id="cdcef-113">Предполагается, что RCS будет использовать для создания решения ER для приложения Finance and Operations, которое будет создавать электронные документы, содержащие информацию из бизнес-домена зарубежной торговли.</span><span class="sxs-lookup"><span data-stu-id="cdcef-113">Assume that RCS will be used to design an ER solution for a Finance and Operation application that will generate electronic documents that contain information from foreign trade business domain.</span></span> <span data-ttu-id="cdcef-114">Чтобы указать сопоставление модели данных ER с источниками необходимых данных, в RCS нам необходимо иметь доступ к метаданным приложения Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cdcef-114">To specify the mapping between ER data model and sources of required data, in RCS we need to have access to metadata of the Finance and Operation application.</span></span> <span data-ttu-id="cdcef-115">Таким образом, в ходе разработки решения ER мы настроим новую конфигурацию метаданных ER, содержую все текущие необходимые метаданные для создания отчетов ER для выбранного бизнес-домена.</span><span class="sxs-lookup"><span data-stu-id="cdcef-115">Therefore, as part of designing ER solution we configure a new ER metadata configuration containing all metadata that is currently required for generation ER reports for selected business domain.</span></span> 

## <a name="add-metadata-configuration"></a><span data-ttu-id="cdcef-116">Добавление конфигурации метаданных</span><span class="sxs-lookup"><span data-stu-id="cdcef-116">Add metadata configuration</span></span> 
1.  <span data-ttu-id="cdcef-117">Щелкните **Создать конфигурацию**, чтобы открыть ниспадающее диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="cdcef-117">Click **Create configuration** to open the drop dialog.</span></span> 
2.  <span data-ttu-id="cdcef-118">В поле **Имя** введите "Метаданные внешней торговли".</span><span class="sxs-lookup"><span data-stu-id="cdcef-118">In the **Name** field, type 'Foreign trade metadata'.</span></span> 
3.  <span data-ttu-id="cdcef-119">Нажмите **Создать конфигурацию**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-119">Click **Create configuration**.</span></span> 
4.  <span data-ttu-id="cdcef-120">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-120">Click **Designer**.</span></span> 
5.  <span data-ttu-id="cdcef-121">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-121">Click **Add**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cdcef-122">Можно выбрать все метаданные для всего приложения, для выбранных моделей или выбранных модулей.</span><span class="sxs-lookup"><span data-stu-id="cdcef-122">You can select all metadata for the entire application or selected models or selected modules.</span></span> <span data-ttu-id="cdcef-123">Следует иметь в виду, что в этом случае следующие метаданные будут автоматически добавлены: таблицы записей, перечисления и расширенные типы данных.</span><span class="sxs-lookup"><span data-stu-id="cdcef-123">Be aware that in this case the following metadata will be automatically added: tables of records, enumerations, and extended data types.</span></span> <span data-ttu-id="cdcef-124">Когда требуются дополнительные типы метаданных, они должны быть добавлены вручную.</span><span class="sxs-lookup"><span data-stu-id="cdcef-124">When additional types of metadata are needed, they must be added manually.</span></span> 
 
<span data-ttu-id="cdcef-125">Мы имеем некоторые метаданные, которые относятся к проводкам внешней торговли, вручную выбрав элементы метаданных.</span><span class="sxs-lookup"><span data-stu-id="cdcef-125">We have some foreign trade transactions related metadata by selecting metadata items manually.</span></span> 
  
6.  <span data-ttu-id="cdcef-126">Щелкните **Добавить источник данных**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-126">Click **Add data source**.</span></span> 
7.  <span data-ttu-id="cdcef-127">Щелкните **Записи таблицы**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-127">Click **Table records**.</span></span> 
8.  <span data-ttu-id="cdcef-128">Используйте экспресс-фильтр для фильтрации поля **Имя** со значением "Интрастат".</span><span class="sxs-lookup"><span data-stu-id="cdcef-128">Use the Quick Filter to filter on the **Name** field with a value of 'Intrastat'.</span></span> 
9.  <span data-ttu-id="cdcef-129">Выберите запись таблицы **Интрастат**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-129">Select the **Intrastat** table record.</span></span> 
10. <span data-ttu-id="cdcef-130">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-130">Click **OK**.</span></span>
  
<span data-ttu-id="cdcef-131">Мы добавили сведения метаданных о записях таблицы Интрастат.</span><span class="sxs-lookup"><span data-stu-id="cdcef-131">We added metadata information about the Intrastat table of records.</span></span> 
  
11. <span data-ttu-id="cdcef-132">В дереве разверните **Записи таблицы Интрастат**\>**Отношения**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-132">In the tree, expand **Table records Intrastat**\>**Relations**.</span></span> 
12. <span data-ttu-id="cdcef-133">В дереве выберите **Записи таблицы Интрастат**\>**Отношения\IntrastatCommodity (записи таблицы EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-133">In the tree, select **Table records Intrastat**\>**Relations\IntrastatCommodity (Table records EcoResCategory)**.</span></span>   
13. <span data-ttu-id="cdcef-134">Щелкните **Добавить метаданные**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-134">Click **Add metadata**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cdcef-135">Метаданные о необходимых отношениях для выбранной таблицы записей необходимо добавить вручную.</span><span class="sxs-lookup"><span data-stu-id="cdcef-135">Metadata about required relations for selected table of records must be added manually.</span></span> 
  
16. <span data-ttu-id="cdcef-136">Щелкните **Добавить источник данных**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-136">Click **Add data source**.</span></span> 
17. <span data-ttu-id="cdcef-137">Щелкните **Перечисление**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-137">Click **Enumeration**.</span></span> 
18. <span data-ttu-id="cdcef-138">Используйте экспресс-фильтр для фильтрации поля **Имя** со значением "IntrastatDirection".</span><span class="sxs-lookup"><span data-stu-id="cdcef-138">Use the Quick Filter to filter on the **Name** field with a value of 'IntrastatDirection'.</span></span> 
19. <span data-ttu-id="cdcef-139">Выберите запись **Перечисление IntrastatDirection**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-139">Select the **IntrastatDirection enumeration** record.</span></span> 
20. <span data-ttu-id="cdcef-140">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-140">Click **OK**.</span></span> 
21. <span data-ttu-id="cdcef-141">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-141">Click **Save**.</span></span>  
22. <span data-ttu-id="cdcef-142">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="cdcef-142">Close the page.</span></span> 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a><span data-ttu-id="cdcef-143">Завершение черновой версии конфигурации метаданных</span><span class="sxs-lookup"><span data-stu-id="cdcef-143">Complete the draft version of metadata configuration</span></span>
1.  <span data-ttu-id="cdcef-144">Щелкните **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-144">Click **Change status**.</span></span> 
2.  <span data-ttu-id="cdcef-145">Щелкните **Завершить**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-145">Click **Complete**.</span></span> 
3.  <span data-ttu-id="cdcef-146">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-146">Click **OK**.</span></span> 
4.  <span data-ttu-id="cdcef-147">Выберите завершенную версию **1**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-147">Select the completed version **1**.</span></span> 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a><span data-ttu-id="cdcef-148">Экспорт завершенной версии конфигурации метаданных из приложения в виде файла XML</span><span class="sxs-lookup"><span data-stu-id="cdcef-148">Export the completed version of metadata configuration from application as XML file</span></span>
1.  <span data-ttu-id="cdcef-149">Щелкните **Обменять**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-149">Click **Exchange**.</span></span> 
2.  <span data-ttu-id="cdcef-150">Щелкните **Экспорт в виде XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-150">Click **Export as XML file**.</span></span> 
3.  <span data-ttu-id="cdcef-151">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="cdcef-151">Click **OK**.</span></span> 
    
<span data-ttu-id="cdcef-152">Созданная конфигурация метаданных ER была сохранена в виде файла XML, который может быть импортирован в RCS и использоваться в качестве источника сведений о метаданных для бизнес-домена внешней торговли в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cdcef-152">The created ER metadata configuration has been saved as XML file that can be imported to RCS and used as the source of information about metadata for the foreign trade business domain in Finance and Operations.</span></span> <span data-ttu-id="cdcef-153">На основе этих сведений можно указать сопоставление между метаданными приложения и моделью данных ER.</span><span class="sxs-lookup"><span data-stu-id="cdcef-153">Based on this information, we can specify the mapping between application metadata and ER data model.</span></span>
