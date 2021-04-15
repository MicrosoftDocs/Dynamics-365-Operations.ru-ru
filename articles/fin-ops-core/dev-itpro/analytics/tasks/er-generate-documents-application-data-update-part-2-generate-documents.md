---
title: Разработка конфигураций для формирования документов, имеющих данные приложений
description: В этой теме описано, как разработать конфигурации электронной отчетности (ER) для создания электронного документа. (Часть 1 — Импорт конфигураций).
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d3f528d48f345ec4b5cc2a46d7740cb6d0a36cd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751090"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="9e877-104">Разработка конфигураций для формирования документов, имеющих данные приложений</span><span class="sxs-lookup"><span data-stu-id="9e877-104">Design configurations to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9e877-105">Для выполнения действий в этой процедуре необходимо сначала выполнить процедуру "Электронная отчетность — Формирование документов с обновлением данных приложения (Часть 1. Импорт конфигураций)".</span><span class="sxs-lookup"><span data-stu-id="9e877-105">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="9e877-106">В этой процедуре поясняется разработка конфигураций электронной отчетности для формирования электронного документа.</span><span class="sxs-lookup"><span data-stu-id="9e877-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="9e877-107">В этой процедуре вам предстоит запустить импортированную конфигурацию формата электронной отчетности, созданную для демонстрационной компании Litware, Inc., для формирования электронных документов.</span><span class="sxs-lookup"><span data-stu-id="9e877-107">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="9e877-108">Эта процедура предназначена для пользователей, которым назначена роль "Системный администратор" или "Разработчик электронной отчетности".</span><span class="sxs-lookup"><span data-stu-id="9e877-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="9e877-109">Действия можно выполнять с использованием набора данных DEMF.</span><span class="sxs-lookup"><span data-stu-id="9e877-109">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="9e877-110">Прежде чем начать, измените контекст страны для компании DEMF с DEU (Германии) на BEL (Бельгия).</span><span class="sxs-lookup"><span data-stu-id="9e877-110">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="9e877-111">Выберите "Управление организацией" > "Организации" > "Юридические лица", чтобы обновить код страны в основном адресе юридического лица DEMF.</span><span class="sxs-lookup"><span data-stu-id="9e877-111">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="9e877-112">Перезапустите приложение.</span><span class="sxs-lookup"><span data-stu-id="9e877-112">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="9e877-113">Запуск импортированного формата электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="9e877-113">Run imported ER format</span></span>
1. <span data-ttu-id="9e877-114">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="9e877-114">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="9e877-115">В дереве разверните узел "Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="9e877-115">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="9e877-116">В дереве выберите "Intrastat (model)\Intrastat (format)".</span><span class="sxs-lookup"><span data-stu-id="9e877-116">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="9e877-117">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="9e877-117">Click Run.</span></span>
    * <span data-ttu-id="9e877-118">Запустите черновую версию конфигурацию формата электронной отчетности, чтобы сформировать отчет Интрастат.</span><span class="sxs-lookup"><span data-stu-id="9e877-118">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="9e877-119">В поле "Введите имя файла" введите "intrastat.xml".</span><span class="sxs-lookup"><span data-stu-id="9e877-119">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="9e877-120">Укажите имя файла.</span><span class="sxs-lookup"><span data-stu-id="9e877-120">Specify the name of the file.</span></span>  
6. <span data-ttu-id="9e877-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="9e877-121">Click OK.</span></span>
    * <span data-ttu-id="9e877-122">Просмотрите сформированный файл XML.</span><span class="sxs-lookup"><span data-stu-id="9e877-122">Review the generated XML file.</span></span>  
7. <span data-ttu-id="9e877-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9e877-123">Close the page.</span></span>
8. <span data-ttu-id="9e877-124">Перейдите в раздел "Налог" > "Декларации" > "Внешняя торговля" > "Интрастат".</span><span class="sxs-lookup"><span data-stu-id="9e877-124">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="9e877-125">Откройте эту форму для просмотра проводок Интрастат, включенных в сформированный электронный документ.</span><span class="sxs-lookup"><span data-stu-id="9e877-125">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="9e877-126">Щелкните "Архив Интрастат".</span><span class="sxs-lookup"><span data-stu-id="9e877-126">Click Intrastat archive.</span></span>
    * <span data-ttu-id="9e877-127">Поскольку выполненный формат электронной отчетности не содержит никаких параметров для обновления данных приложения, сведения о завершенном отчете Интрастат архивированы не были.</span><span class="sxs-lookup"><span data-stu-id="9e877-127">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="9e877-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9e877-128">Close the page.</span></span>
11. <span data-ttu-id="9e877-129">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9e877-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]