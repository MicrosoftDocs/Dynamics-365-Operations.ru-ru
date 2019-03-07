---
title: Разработка конфигураций для формирования документов, имеющих данные приложений
description: Для выполнения действий в этой процедуре необходимо сначала выполнить процедуру "Электронная отчетность — Формирование документов с обновлением данных приложения (Часть 1. Импорт конфигураций)".
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8376107a33dd83e04f82fcab6847e7f073f08dbc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "316357"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="c49f0-103">Разработка конфигураций для формирования документов, имеющих данные приложений</span><span class="sxs-lookup"><span data-stu-id="c49f0-103">Design configurations to generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c49f0-104">Для выполнения действий в этой процедуре необходимо сначала выполнить процедуру "Электронная отчетность — Формирование документов с обновлением данных приложения (Часть 1. Импорт конфигураций)".</span><span class="sxs-lookup"><span data-stu-id="c49f0-104">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="c49f0-105">В этой процедуре поясняется разработка конфигураций электронной отчетности для формирования электронного документа.</span><span class="sxs-lookup"><span data-stu-id="c49f0-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="c49f0-106">В этой процедуре вам предстоит запустить импортированную конфигурацию формата электронной отчетности, созданную для демонстрационной компании Litware, Inc., для формирования электронных документов.</span><span class="sxs-lookup"><span data-stu-id="c49f0-106">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="c49f0-107">Эта процедура предназначена для пользователей, которым назначена роль "Системный администратор" или "Разработчик электронной отчетности".</span><span class="sxs-lookup"><span data-stu-id="c49f0-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="c49f0-108">Действия можно выполнять с использованием набора данных DEMF.</span><span class="sxs-lookup"><span data-stu-id="c49f0-108">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="c49f0-109">Прежде чем начать, измените контекст страны для компании DEMF с DEU (Германии) на BEL (Бельгия).</span><span class="sxs-lookup"><span data-stu-id="c49f0-109">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="c49f0-110">Выберите "Управление организацией" > "Организации" > "Юридические лица", чтобы обновить код страны в основном адресе юридического лица DEMF.</span><span class="sxs-lookup"><span data-stu-id="c49f0-110">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="c49f0-111">Перезапустите приложение.</span><span class="sxs-lookup"><span data-stu-id="c49f0-111">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="c49f0-112">Запуск импортированного формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="c49f0-112">Run imported ER format</span></span>
1. <span data-ttu-id="c49f0-113">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="c49f0-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c49f0-114">В дереве разверните узел "Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="c49f0-114">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="c49f0-115">В дереве выберите "Intrastat (model)\Intrastat (format)".</span><span class="sxs-lookup"><span data-stu-id="c49f0-115">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="c49f0-116">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="c49f0-116">Click Run.</span></span>
    * <span data-ttu-id="c49f0-117">Запустите черновую версию конфигурацию формата электронной отчетности, чтобы сформировать отчет Интрастат.</span><span class="sxs-lookup"><span data-stu-id="c49f0-117">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="c49f0-118">В поле "Введите имя файла" введите "intrastat.xml".</span><span class="sxs-lookup"><span data-stu-id="c49f0-118">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="c49f0-119">Укажите имя файла.</span><span class="sxs-lookup"><span data-stu-id="c49f0-119">Specify the name of the file.</span></span>  
6. <span data-ttu-id="c49f0-120">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="c49f0-120">Click OK.</span></span>
    * <span data-ttu-id="c49f0-121">Просмотрите сформированный файл XML.</span><span class="sxs-lookup"><span data-stu-id="c49f0-121">Review the generated XML file.</span></span>  
7. <span data-ttu-id="c49f0-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c49f0-122">Close the page.</span></span>
8. <span data-ttu-id="c49f0-123">Перейдите в раздел "Налог" > "Декларации" > "Внешняя торговля" > "Интрастат".</span><span class="sxs-lookup"><span data-stu-id="c49f0-123">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="c49f0-124">Откройте эту форму для просмотра проводок Интрастат, включенных в сформированный электронный документ.</span><span class="sxs-lookup"><span data-stu-id="c49f0-124">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="c49f0-125">Щелкните "Архив Интрастат".</span><span class="sxs-lookup"><span data-stu-id="c49f0-125">Click Intrastat archive.</span></span>
    * <span data-ttu-id="c49f0-126">Поскольку выполненный формат электронной отчетности не содержит никаких параметров для обновления данных приложения, сведения о завершенном отчете Интрастат архивированы не были.</span><span class="sxs-lookup"><span data-stu-id="c49f0-126">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="c49f0-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c49f0-127">Close the page.</span></span>
11. <span data-ttu-id="c49f0-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="c49f0-128">Close the page.</span></span>

