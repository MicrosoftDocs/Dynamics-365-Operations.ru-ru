---
title: Интеграция для соглашений на сервисное обслуживание и проектов
description: При работе с соглашениями о сервисном обслуживании и строками соглашений о сервисном обслуживании используются данные, настроенные в областях раздела "Управление и учет по проектам".
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6bd2fb1f54a3decb77f019db6b2016cebdcaddb9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "323211"
---
# <a name="integration-for-service-agreements-and-projects"></a><span data-ttu-id="5a56f-103">Интеграция для соглашений на сервисное обслуживание и проектов</span><span class="sxs-lookup"><span data-stu-id="5a56f-103">Integration for service agreements and projects</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="5a56f-104">При работе с соглашениями о сервисном обслуживании и строками соглашений о сервисном обслуживании используются данные, настроенные в следующих областях раздела **Управление и учет по проектам**.</span><span class="sxs-lookup"><span data-stu-id="5a56f-104">When you work with service agreements and service agreement lines, you use data that is set up in the following areas in **Project management and accounting**.</span></span>

## <a name="project-prices"></a><span data-ttu-id="5a56f-105">Цены проекта</span><span class="sxs-lookup"><span data-stu-id="5a56f-105">Project prices</span></span>

<span data-ttu-id="5a56f-106">Стоимость и цена продажи для проводки соглашения о сервисном обслуживании получаются из настройки себестоимости для проекта, связанного с соглашением о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="5a56f-106">The cost and the sales price for a service agreement transaction are derived from the cost price setup that applies to the project that is attached to the service agreement.</span></span> <span data-ttu-id="5a56f-107">Стоимость и цена продажи могут быть настроены по проекту, сотруднику и категории.</span><span class="sxs-lookup"><span data-stu-id="5a56f-107">Cost and sales prices can be set up by project, employee, and category.</span></span> 

## <a name="project-validation"></a><span data-ttu-id="5a56f-108">Проверка проекта</span><span class="sxs-lookup"><span data-stu-id="5a56f-108">Project validation</span></span>

<span data-ttu-id="5a56f-109">Проекты, сотрудники и категории, доступные для выбора в строке соглашения о сервисном обслуживании, могут быть ограничены настройкой проверки в **Управление и учет по проектам**.</span><span class="sxs-lookup"><span data-stu-id="5a56f-109">The projects, employees, and categories that are available for selection on a service agreement line can be limited by the validation setup in **Project management and accounting**.</span></span> <span data-ttu-id="5a56f-110">Использование настройки проверки позволяет объединить сотрудников, проекты и категории для управления правами доступа.</span><span class="sxs-lookup"><span data-stu-id="5a56f-110">By using the validation setup, you can combine employees, projects, and categories for control access.</span></span> 

## <a name="project-line-properties"></a><span data-ttu-id="5a56f-111">Свойства строки проекта</span><span class="sxs-lookup"><span data-stu-id="5a56f-111">Project line properties</span></span>

<span data-ttu-id="5a56f-112">Свойство строки автоматически задается для строки соглашения о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="5a56f-112">A line property is entered automatically for a service agreement line.</span></span>

<span data-ttu-id="5a56f-113">Свойства строки создаются в форме **Свойства строки** в модуле **Управление и учет по проектам**.</span><span class="sxs-lookup"><span data-stu-id="5a56f-113">Line properties are created in the **Line properties** form in **Project management and accounting**.</span></span> <span data-ttu-id="5a56f-114">Свойство строки, введенное в соглашение о сервисном обслуживании, присоединяется к проекту, выбранному для соглашения о сервисном обслуживании, затем наследуется строкой соглашения о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="5a56f-114">The line property that is entered on a service agreement is attached to the project that is selected for the service agreement and inherited subsequently by the service agreement line.</span></span> 

## <a name="default-offset-accounts"></a><span data-ttu-id="5a56f-115">Корр. счета по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5a56f-115">Default offset accounts</span></span>

<span data-ttu-id="5a56f-116">При вводе проводки расходов по умолчанию для проводки автоматически устанавливается корреспондентский счет расходов.</span><span class="sxs-lookup"><span data-stu-id="5a56f-116">If you enter an expense transaction, a default expense offset account is selected automatically for the transaction.</span></span> <span data-ttu-id="5a56f-117">Счет расходов по умолчанию настраивается для проекта, прикрепленного к текущему соглашению о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="5a56f-117">The default expense account is set up for the project that is attached to the current service agreement.</span></span>

## <a name="project-categories"></a><span data-ttu-id="5a56f-118">Категории проектов</span><span class="sxs-lookup"><span data-stu-id="5a56f-118">Project categories</span></span>

<span data-ttu-id="5a56f-119">Категории, доступные для строк соглашения о сервисном обслуживании, настраиваются в форме **Категории проектов** в модуле **Управление и учет по проектам**.</span><span class="sxs-lookup"><span data-stu-id="5a56f-119">The categories that are available for service agreement lines are set up in the **Project categories** form in **Project management and accounting**.</span></span> 

> [!NOTE]
> <P><span data-ttu-id="5a56f-120">Категории, для которых установлен флажок <STRONG>Активно в журналах</STRONG> на вкладке <STRONG>Проект</STRONG> в форме <STRONG>Категории проектов</STRONG>, доступны для выбора.</span><span class="sxs-lookup"><span data-stu-id="5a56f-120">Categories that have the <STRONG>Active in journals</STRONG> check box selected on the <STRONG>Project</STRONG> tab in the <STRONG>Project categories</STRONG> form are available for selection.</span></span> <span data-ttu-id="5a56f-121">Однако, если флажок <STRONG>Неактивные категории</STRONG> установлен на вкладке <STRONG>Журналы</STRONG> в форме <STRONG>Параметры модуля "Управление и учет по проектам"</STRONG>, все категории доступны для выбора.</span><span class="sxs-lookup"><span data-stu-id="5a56f-121">However, if the <STRONG>Inactive categories</STRONG> check box is selected on the <STRONG>Journals</STRONG> tab in the <STRONG>Project management and accounting parameters</STRONG> form, all categories are available for selection.</span></span></P>

## <a name="project-parameters"></a><span data-ttu-id="5a56f-122">Параметры проекта</span><span class="sxs-lookup"><span data-stu-id="5a56f-122">Project parameters</span></span>

<span data-ttu-id="5a56f-123">Если выбрано поле **Уволенные рабочие** на вкладке **Журналы** в форме **Параметры модуля "Управление и учет по проектам"**, можно выбрать неактивных и активных сотрудников в формах **Соглашения о сервисном обслуживании** и **Заказы на сервисное обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="5a56f-123">If the **Terminated workers** field on the **Journals** tab in the **Project management and accounting parameters** form is selected, you can select inactive employees and active employees in the **Service agreements** and **Service orders** forms.</span></span>

<span data-ttu-id="5a56f-124">Также имеется возможность включить поля **Время начала** и **Время окончания** на вкладке **Проект** в форме **Заказы на обслуживание**, чтобы ввести время начала и окончания в строках заказа на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="5a56f-124">Also, you can enable the **Start time** and **End time** fields on the **Project** tab in the **Service orders** form to enter starting and ending times on service order lines.</span></span>

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a><span data-ttu-id="5a56f-125">Включение функции времени начала и окончания для заказов на сервисное обслуживание</span><span class="sxs-lookup"><span data-stu-id="5a56f-125">Enable the starting and ending time feature for service orders</span></span>

1.  <span data-ttu-id="5a56f-126">Щелкните **Управление и учет по проектам** \> **Настройка** \> **Параметры модуля "Управление и учет по проектам"**.</span><span class="sxs-lookup"><span data-stu-id="5a56f-126">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="5a56f-127">Откройте вкладку **Журналы** и установите флажок **Показать время начала/окончания**.</span><span class="sxs-lookup"><span data-stu-id="5a56f-127">Click the **Journals** tab, and then select the **Show start/end times** check box.</span></span>

3.  <span data-ttu-id="5a56f-128">Щелкните **Управление и учет по проектам** \> **Настройка** \> **Журналы** \> **Названия журналов**.</span><span class="sxs-lookup"><span data-stu-id="5a56f-128">Click **Project management and accounting** \> **Setup** \> **Journals** \> **Journal names**.</span></span>

4.  <span data-ttu-id="5a56f-129">Выберите наименование журнала, присоединенного к заказу на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="5a56f-129">Select the journal name that is attached to the service order.</span></span>

5.  <span data-ttu-id="5a56f-130">Откройте вкладку **Общие** и установите флажок **Показать время начала/окончания**.</span><span class="sxs-lookup"><span data-stu-id="5a56f-130">Click the **General** tab, and then select the **Show start/end times** check box.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5a56f-131">Выберите название журнала для заказа на сервисное обслуживание в поле <STRONG>Час</STRONG> на вкладке <STRONG>Журналы</STRONG> в форме <STRONG>Параметры управления сервисным обслуживанием</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="5a56f-131">Select the journal name for the service order in the <STRONG>Hour</STRONG> field on the <STRONG>Journals</STRONG> tab in the <STRONG>Service management parameters</STRONG> form.</span></span></P>





