--- 
title: "Выполнение отчета, использующего финансовые аналитики как источник данных для электронной отчетности (ER)"
description: "В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: cdecf5fb3f3047a56353ee6d4a8f94957f508e4b
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="9c9ef-103">Выполнение отчета, использующего финансовые аналитики как источник данных для электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="9c9ef-103">Run a report that uses financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9c9ef-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить модель электронной отчетности (ER) для использования финансовых аналитик как источника данных для отчетов электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="9c9ef-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="9c9ef-105">Эти шаги можно выполнить в компании DEMF.</span><span class="sxs-lookup"><span data-stu-id="9c9ef-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="9c9ef-106">Для выполнения этих действий необходимо сначала выполнить шаги в процедуре "Электронная отчетность — Использование финансовых аналитик как источника данных (Часть 3. Разработка отчета)".</span><span class="sxs-lookup"><span data-stu-id="9c9ef-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="9c9ef-107">Также необходимо настроить типы документов по умолчанию на странице "Параметры электронной отчетности".</span><span class="sxs-lookup"><span data-stu-id="9c9ef-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="9c9ef-108">Типы документов по умолчанию также задаются при загрузке и импорте любой конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="9c9ef-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="9c9ef-109">Выполнение отчета</span><span class="sxs-lookup"><span data-stu-id="9c9ef-109">Run report</span></span>
1. <span data-ttu-id="9c9ef-110">Перейдите в раздел "Управление организацией" > "Электронная отчетность" > "Конфигурации".</span><span class="sxs-lookup"><span data-stu-id="9c9ef-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="9c9ef-111">В дереве разверните узел "Пример модели финансовых аналитик".</span><span class="sxs-lookup"><span data-stu-id="9c9ef-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="9c9ef-112">В дереве выберите "Пример модели финансовых аналитик\Отчет журнала ГК".</span><span class="sxs-lookup"><span data-stu-id="9c9ef-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="9c9ef-113">Щелкните Выполнить.</span><span class="sxs-lookup"><span data-stu-id="9c9ef-113">Click Run.</span></span>
5. <span data-ttu-id="9c9ef-114">В поле "Имя аналитики" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9c9ef-114">In the Dimension name field, In the Dimension name field, enter or select a value..</span></span>
    * <span data-ttu-id="9c9ef-115">Чтобы выбрать все аналитики в текущей компании, введите следующие сведения:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="9c9ef-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="9c9ef-116">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="9c9ef-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="9c9ef-117">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="9c9ef-117">Click Filter.</span></span>
8. <span data-ttu-id="9c9ef-118">Выберите строку для таблицы "Журнал ГК" и поля "Номер партии журнала".</span><span class="sxs-lookup"><span data-stu-id="9c9ef-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="9c9ef-119">В поле "Критерии" введите "00057".</span><span class="sxs-lookup"><span data-stu-id="9c9ef-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="9c9ef-120">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="9c9ef-120">Click OK.</span></span>
11. <span data-ttu-id="9c9ef-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="9c9ef-121">Click OK.</span></span>
    * <span data-ttu-id="9c9ef-122">Просмотрите созданные выходные данные.</span><span class="sxs-lookup"><span data-stu-id="9c9ef-122">Review the generated output.</span></span> <span data-ttu-id="9c9ef-123">Обратите внимание, что для каждой проводки выбранной партии представлены финансовые аналитики из соответствующих аналитик.</span><span class="sxs-lookup"><span data-stu-id="9c9ef-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="9c9ef-124">Выполните этот отчет и выберите другие аналитики, чтобы убедиться, что отчет не зависит от количества выбранных аналитик или количества аналитик, настроенных для данного экземпляра Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="9c9ef-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  


