--- 
title: "Создание документов с обновлением данных приложения"
description: "Для выполнения действий в этой процедуре необходимо сначала выполнить процедуру \"Электронная отчетность — Формирование документов с обновлением данных приложения (Часть 4. Изменение формата)\"."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5001adbc1c7fae96e94e7b31a64a5a04ba886dc8
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="generate-documents-with-application-data"></a><span data-ttu-id="162df-103">Создание документов с обновлением данных приложения</span><span class="sxs-lookup"><span data-stu-id="162df-103">Generate documents with application data</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="162df-104">Для выполнения действий в этой процедуре необходимо сначала выполнить процедуру "Электронная отчетность — Формирование документов с обновлением данных приложения (Часть 4. Изменение формата)".</span><span class="sxs-lookup"><span data-stu-id="162df-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 4: Modify format)”.</span></span>



<span data-ttu-id="162df-105">В этой процедуре поясняется разработка конфигураций электронной отчетности для формирования электронного документа и обновления данных приложения.</span><span class="sxs-lookup"><span data-stu-id="162df-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="162df-106">В этой процедуре вам предстоит выполнить конфигурацию формата электронной отчетности для формирования отчета Интрастат и обновления данных приложения для архивирования сведений о процессе составления отчетности.</span><span class="sxs-lookup"><span data-stu-id="162df-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="162df-107">Эта процедура предназначена для пользователей, которым назначена роль "Системный администратор" или "Разработчик электронной отчетности".</span><span class="sxs-lookup"><span data-stu-id="162df-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="162df-108">Действия можно выполнять с использованием набора данных DEMF.</span><span class="sxs-lookup"><span data-stu-id="162df-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="162df-109">Прежде чем начать, убедитесь, что контекст страны для компании DEMF — BEL (Бельгия).</span><span class="sxs-lookup"><span data-stu-id="162df-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="162df-110">Настройка параметров внешней торговли</span><span class="sxs-lookup"><span data-stu-id="162df-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="162df-111">Перейдите в раздел "Налог" > "Настройка" > "Внешняя торговля" > "Параметры внешней торговли".</span><span class="sxs-lookup"><span data-stu-id="162df-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="162df-112">Откройте вкладку Номерные серии.</span><span class="sxs-lookup"><span data-stu-id="162df-112">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="162df-113">При архивировании сведений о процессе составления отчетности Интрастат необходимо идентифицировать записи каждого созданного нами архива.</span><span class="sxs-lookup"><span data-stu-id="162df-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="162df-114">Для этого необходимо сконфигурировать специальные номерные серии.</span><span class="sxs-lookup"><span data-stu-id="162df-114">A special number sequence must be configured for that.</span></span>  
3. <span data-ttu-id="162df-115">Выберите ссылку "Код архива Интрастат".</span><span class="sxs-lookup"><span data-stu-id="162df-115">Select the ‘Intrastat archive ID’ reference.</span></span>
4. <span data-ttu-id="162df-116">В поле "Код номерной серии" введите значение.</span><span class="sxs-lookup"><span data-stu-id="162df-116">In the Number sequence code field, type a value.</span></span>
    * <span data-ttu-id="162df-117">В поле "Код номерной серии" введите или выберите значение "Fore_2".</span><span class="sxs-lookup"><span data-stu-id="162df-117">In the ‘Number sequence code’ field, enter or select the value ‘Fore_2’.</span></span>  
5. <span data-ttu-id="162df-118">Разрешите изменения кода номерной серии.</span><span class="sxs-lookup"><span data-stu-id="162df-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="162df-119">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="162df-119">Click Save.</span></span>
7. <span data-ttu-id="162df-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="162df-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="162df-121">Запуск измененного формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="162df-121">Run modified ER format</span></span>
1. <span data-ttu-id="162df-122">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="162df-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="162df-123">В дереве разверните узел "Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="162df-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="162df-124">В дереве выберите "Intrastat (model)\Intrastat (format)".</span><span class="sxs-lookup"><span data-stu-id="162df-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="162df-125">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="162df-125">Click Run.</span></span>
5. <span data-ttu-id="162df-126">В поле "Введите имя файла" введите "intrastat2.xml".</span><span class="sxs-lookup"><span data-stu-id="162df-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
    * <span data-ttu-id="162df-127">intrastat2.xml</span><span class="sxs-lookup"><span data-stu-id="162df-127">intrastat2.xml</span></span>  
6. <span data-ttu-id="162df-128">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="162df-128">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="162df-129">Просмотр результатов выполнения формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="162df-129">Review ER format execution’s results</span></span>
    * <span data-ttu-id="162df-130">Просмотрите сформированный файл XML.</span><span class="sxs-lookup"><span data-stu-id="162df-130">Review the generated XML file.</span></span>  
1. <span data-ttu-id="162df-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="162df-131">Close the page.</span></span>
2. <span data-ttu-id="162df-132">Перейдите в раздел "Налог" > "Декларации" > "Внешняя торговля" > "Интрастат".</span><span class="sxs-lookup"><span data-stu-id="162df-132">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="162df-133">Откройте эту форму, содержащую проводки Интрастат, включенные в сформированный электронный документ.</span><span class="sxs-lookup"><span data-stu-id="162df-133">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  
3. <span data-ttu-id="162df-134">Щелкните "Архив Интрастат".</span><span class="sxs-lookup"><span data-stu-id="162df-134">Click Intrastat archive.</span></span>
    * <span data-ttu-id="162df-135">Поскольку выполненный формат электронной отчетности теперь содержит параметры для обновления данных приложения, сведения о завершенной отчетности Интрастат были архивированы.</span><span class="sxs-lookup"><span data-stu-id="162df-135">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="162df-136">В этой форме можно просмотреть запись заголовка созданного архива.</span><span class="sxs-lookup"><span data-stu-id="162df-136">In this form, you can see the header record of the created archive.</span></span>  
4. <span data-ttu-id="162df-137">Нажмите кнопку Состав.</span><span class="sxs-lookup"><span data-stu-id="162df-137">Click Details.</span></span>
    * <span data-ttu-id="162df-138">В этой форме можно просмотреть сведения о созданном архиве.</span><span class="sxs-lookup"><span data-stu-id="162df-138">In this form, you can see the details for the created archive.</span></span>  
5. <span data-ttu-id="162df-139">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="162df-139">Close the page.</span></span>
6. <span data-ttu-id="162df-140">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="162df-140">Close the page.</span></span>
7. <span data-ttu-id="162df-141">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="162df-141">Close the page.</span></span>


