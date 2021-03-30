---
title: Оценка состояния
description: В этой теме объясняется, как создать шаблон оценки состояния и регистрацию актива в управлении активами.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectCondition, EntAssetConditionTemplate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d84520413659db32713711ad5ac980f1e8b5519
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217181"
---
# <a name="condition-assessment"></a><span data-ttu-id="6f090-103">Оценка состояния</span><span class="sxs-lookup"><span data-stu-id="6f090-103">Condition assessment</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6f090-104">В этой теме объясняется, как создать шаблон оценки состояния и регистрацию актива в управлении активами.</span><span class="sxs-lookup"><span data-stu-id="6f090-104">This topic explains how to create a condition assessment template and registration on an asset in Asset Management.</span></span> <span data-ttu-id="6f090-105">Оценка состояния проводится через регулярные промежутки времени, и основной целью является создание и поддержание данных о состоянии активов.</span><span class="sxs-lookup"><span data-stu-id="6f090-105">Condition assessment is performed at regular intervals, and the primary objective is to create and maintain condition data on assets.</span></span> <span data-ttu-id="6f090-106">С точки зрения профилактического обслуживания важно отслеживать ключевые сведения, такие как текущее состояние и продолжительность срока службы.</span><span class="sxs-lookup"><span data-stu-id="6f090-106">Seen from a preventive maintenance perspective, it is important to monitor key information such as current condition, and remaining life span.</span></span> <span data-ttu-id="6f090-107">Кроме того, если вы регулярно проводите оценку состояния, вы сможете отслеживать и сравнивать состояние оборудования на вашем заводе.</span><span class="sxs-lookup"><span data-stu-id="6f090-107">Furthermore, if you carry out condition assessment at regular intervals, you will be able to monitor and compare conditions on the machinery in your factory.</span></span>

<span data-ttu-id="6f090-108">Оценка состояния может быть использована для измерения и мониторинга многих состояний вашего оборудования.</span><span class="sxs-lookup"><span data-stu-id="6f090-108">Condition assessment can be used to measure and monitor many conditions on your equipment.</span></span> <span data-ttu-id="6f090-109">Пример. Вы можете измерить вибрации на вашем оборудовании.</span><span class="sxs-lookup"><span data-stu-id="6f090-109">Example: You could measure vibrations on your machinery.</span></span> <span data-ttu-id="6f090-110">После регистрации измерений вибрации в управлении активами на различных типах оборудования вы можете искать последние зарегистрированные оценки и просматривать измерения вибрации.</span><span class="sxs-lookup"><span data-stu-id="6f090-110">After you have registered vibration measurements in Asset Management on various types of equipment, you can search for the latest registered assessment and view vibration measurements.</span></span>

<span data-ttu-id="6f090-111">Оценка состояния создается по активам.</span><span class="sxs-lookup"><span data-stu-id="6f090-111">Condition assessment is created on assets.</span></span> <span data-ttu-id="6f090-112">Перед проведением процедуры оценки состояния вы настраиваете шаблон оценки состояния для типа актива.</span><span class="sxs-lookup"><span data-stu-id="6f090-112">You set up a condition assessment template on an asset type before you carry out the condition assessment procedure.</span></span> <span data-ttu-id="6f090-113">Причина использования шаблонов для оценки состояния заключается в том, чтобы избежать вариаций данных о состоянии для аналогичных активов.</span><span class="sxs-lookup"><span data-stu-id="6f090-113">The reason for using templates for condition assessment is to avoid variation of condition data on similar assets.</span></span> <span data-ttu-id="6f090-114">Последовательность настройки и использования оценки состояния в управлении активами: сначала вы настраиваете необходимые шаблоны оценки состояния.</span><span class="sxs-lookup"><span data-stu-id="6f090-114">The sequence for setting up and using condition assessment in Asset Management is: First you set up the required condition assessment templates.</span></span> <span data-ttu-id="6f090-115">Далее шаблоны связывают с типами активов в форме **Типы активов**.</span><span class="sxs-lookup"><span data-stu-id="6f090-115">Next, you associate templates with asset types in the **Asset types** form.</span></span> <span data-ttu-id="6f090-116">Наконец, можно создать регистрации оценки состояния для актива в форме **Актив**.</span><span class="sxs-lookup"><span data-stu-id="6f090-116">Finally, you can create condition assessment registrations on an asset in the **Asset** form.</span></span>

## <a name="create-a-condition-assessment-template"></a><span data-ttu-id="6f090-117">Создание шаблона оценки состояния</span><span class="sxs-lookup"><span data-stu-id="6f090-117">Create a condition assessment template</span></span>

1. <span data-ttu-id="6f090-118">Выберите **Управление активами** > **Настройка** > **Типы активов** > **Оценка состояния**.</span><span class="sxs-lookup"><span data-stu-id="6f090-118">Select **Asset management** > **Setup** > **Asset types** > **Condition assessment**.</span></span>
2. <span data-ttu-id="6f090-119">Выберите **Создать** для создания нового шаблона.</span><span class="sxs-lookup"><span data-stu-id="6f090-119">Select **New** to create a new template.</span></span>
3. <span data-ttu-id="6f090-120">Вставьте идентификатор для шаблона в поле **Шаблон**.</span><span class="sxs-lookup"><span data-stu-id="6f090-120">Insert and ID for the template in the **Template** field.</span></span>
4. <span data-ttu-id="6f090-121">Вставьте имя шаблона в поле **Имя**.</span><span class="sxs-lookup"><span data-stu-id="6f090-121">Insert a name for the template in the **Name** field.</span></span>
5. <span data-ttu-id="6f090-122">На экспресс-вкладке **Строки оценки состояния** добавьте строки, необходимые для оценки состояния, включая выбор соответствующего типа состояния и единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="6f090-122">On the **Condition assessment lines** FastFab, add the lines required for the condition assessment, including selection of the appropriate condition type and measurement unit.</span></span>
6. <span data-ttu-id="6f090-123">На экспресс-вкладке **Типы активов** добавьте типы активов, которые должны использовать шаблон оценки состояния.</span><span class="sxs-lookup"><span data-stu-id="6f090-123">On the **Asset types** FastTab, add the asset types that should use the condition assessment template.</span></span>
7. <span data-ttu-id="6f090-124">В полях **Строки** и **Типы активов** в группе **Детали** в верхней части экрана вы увидите количество строк оценки и типы активов, связанных с выбранным шаблоном оценки состояния.</span><span class="sxs-lookup"><span data-stu-id="6f090-124">In the **Lines** and **Asset types** fields in the **Details** group at the top of the screen, you will see the number of assessment lines and asset types related to the selected condition assessment template.</span></span>


## <a name="create-condition-assessment-registration-on-an-asset"></a><span data-ttu-id="6f090-125">Создание регистрации оценки состояния для актива</span><span class="sxs-lookup"><span data-stu-id="6f090-125">Create condition assessment registration on an asset</span></span>

1. <span data-ttu-id="6f090-126">Выберите **Управление активами** > **Общие** > **Активы** > **Все активы**.</span><span class="sxs-lookup"><span data-stu-id="6f090-126">Select **Asset management** > **Common** > **Assets** > **All Assets**.</span></span>
2. <span data-ttu-id="6f090-127">В списке выберите актив, для которого требуется создать регистрацию оценки состояния.</span><span class="sxs-lookup"><span data-stu-id="6f090-127">In the list, select the asset for which you want to create a condition assessment registration.</span></span>
3. <span data-ttu-id="6f090-128">На вкладке **Общие**, щелкните **Оценка состояния**.</span><span class="sxs-lookup"><span data-stu-id="6f090-128">On the **General** tab, click **Condition assessment**.</span></span>
4. <span data-ttu-id="6f090-129">Щелкните **Создать**, чтобы создать новую регистрацию.</span><span class="sxs-lookup"><span data-stu-id="6f090-129">Click **New** to make a new registration.</span></span>
5. <span data-ttu-id="6f090-130">Выберите дату для оценки состояния в поле **Дата**.</span><span class="sxs-lookup"><span data-stu-id="6f090-130">Select the date for the condition assessment in the **Date** field.</span></span>
6. <span data-ttu-id="6f090-131">Выберите имя работника, осуществляющего регистрацию оценки, в поле **Работник**.</span><span class="sxs-lookup"><span data-stu-id="6f090-131">Select the name of the worker who carried out the assessment registration in the **Worker** field.</span></span>
7. <span data-ttu-id="6f090-132">В поле **Строки** вы видите количество строк оценки, настроенных в оценке состояния.</span><span class="sxs-lookup"><span data-stu-id="6f090-132">In the **Lines** field, you see the number of assessment lines set up on the condition assessment.</span></span>
8. <span data-ttu-id="6f090-133">Выберите шаблон для оценки состояния в поле **Шаблон**.</span><span class="sxs-lookup"><span data-stu-id="6f090-133">Select a template for the condition assessment in the **Template** field.</span></span> <span data-ttu-id="6f090-134">Имя шаблона автоматически вставляется в поле **Имя**, а соответствующие строки регистрации вставляются на экспресс-вкладку **Строки оценки состояния**.</span><span class="sxs-lookup"><span data-stu-id="6f090-134">The name of the template is automatically inserted in the **Name** field, and the related registration lines are inserted on the **Condition assessment lines** FastTab.</span></span>
9. <span data-ttu-id="6f090-135">Вы можете вставить заметки, относящиеся к выбранной оценке состояния, на экспресс-вкладке **Примечания**.</span><span class="sxs-lookup"><span data-stu-id="6f090-135">You can insert notes relating to the selected condition assessment on the **Notes** FastTab.</span></span>
10. <span data-ttu-id="6f090-136">Для каждой строки оценки состояния вставьте данные измерений в поле **Значение**.</span><span class="sxs-lookup"><span data-stu-id="6f090-136">For each condition assessment line, insert measurement data in the **Value** field.</span></span>
11. <span data-ttu-id="6f090-137">Вы можете вставить комментарий, относящийся к выбранной строке регистрации, на экспресс-вкладке **Строки оценки состояния** > **Комментарии**.</span><span class="sxs-lookup"><span data-stu-id="6f090-137">You can insert a comment relating to the selected registration line on the **Condition assessment lines** FastTab > **Comments** field.</span></span> <span data-ttu-id="6f090-138">Если вы добавляете комментарий в строку, флажок **Комментарий** автоматически устанавливается.</span><span class="sxs-lookup"><span data-stu-id="6f090-138">If you add a comment on a line, the **Comment** check box is automatically selected.</span></span>

<span data-ttu-id="6f090-139">После выполнения регистрации оценки регистрации для актива можно распечатать отчет об оценке состояния.</span><span class="sxs-lookup"><span data-stu-id="6f090-139">After you have made a condition assessment registration on an asset, you can print a condition assessment report.</span></span>

>[!NOTE]
><span data-ttu-id="6f090-140">Вы также можете зарегистрировать оценку состояния в заказе на работу (**Управление активами** > **Общие** > **Заказы на работу** > **Все заказы на работу** > кнопка **Оценка состояния**.)</span><span class="sxs-lookup"><span data-stu-id="6f090-140">You can also register condition assessment on a work order (**Asset management** > **Common** > **Work orders** > **All Work orders** > **Condition assessment** button.)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]