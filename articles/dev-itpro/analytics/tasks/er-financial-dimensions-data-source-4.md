--- 
title: "Выполнение отчета, использующего финансовые аналитики как источник данных для электронной отчетности (ER)"
description: "В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: ee951d7f3f04e641f7bed767a2eebd1c180eb9f3
ms.contentlocale: ru-ru
ms.lasthandoff: 03/26/2018

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="4b527-103">Выполнение отчета, использующего финансовые аналитики как источник данных для электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="4b527-103">Run a report that uses financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4b527-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="4b527-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="4b527-105">Эти шаги можно выполнить в компании DEMF.</span><span class="sxs-lookup"><span data-stu-id="4b527-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="4b527-106">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 3. Разработка отчета)".</span><span class="sxs-lookup"><span data-stu-id="4b527-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="4b527-107">Также необходимо настроить типы документов по умолчанию на странице "Параметры электронной отчетности".</span><span class="sxs-lookup"><span data-stu-id="4b527-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="4b527-108">Типы документов по умолчанию также задаются при загрузке и импорте любой конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="4b527-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="4b527-109">Выполнение отчета</span><span class="sxs-lookup"><span data-stu-id="4b527-109">Run report</span></span>
1. <span data-ttu-id="4b527-110">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="4b527-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="4b527-111">В дереве разверните узел "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="4b527-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="4b527-112">В дереве выберите "Пример модели финансовых аналитик\Отчет журнала ГК".</span><span class="sxs-lookup"><span data-stu-id="4b527-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="4b527-113">Щелкните Выполнить.</span><span class="sxs-lookup"><span data-stu-id="4b527-113">Click Run.</span></span>
5. <span data-ttu-id="4b527-114">В поле "Имя аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="4b527-114">In the Dimension name field, In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="4b527-115">Чтобы выбрать все аналитики в текущей компании, введите следующие сведения:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="4b527-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="4b527-116">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="4b527-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="4b527-117">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="4b527-117">Click Filter.</span></span>
8. <span data-ttu-id="4b527-118">Выберите строку для таблицы "Журнал ГК" и поля "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="4b527-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="4b527-119">В поле "Критерии" введите "00057".</span><span class="sxs-lookup"><span data-stu-id="4b527-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="4b527-120">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4b527-120">Click OK.</span></span>
11. <span data-ttu-id="4b527-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4b527-121">Click OK.</span></span>
    * <span data-ttu-id="4b527-122">Просмотрите созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="4b527-122">Review the generated output.</span></span> <span data-ttu-id="4b527-123">Обратите внимание, что для каждой проводки выбранной партии представлены финансовые аналитики из соответствующих аналитик.</span><span class="sxs-lookup"><span data-stu-id="4b527-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="4b527-124">Выполните этот отчет и выберите другие аналитики, чтобы убедиться, что отчет не зависит от количества выбранных аналитик или количества аналитик, настроенных для данного экземпляра Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4b527-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations instance.</span></span>  


