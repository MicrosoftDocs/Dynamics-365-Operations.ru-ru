--- 
title: "Создание форматов электронной отчетности для подсчета и суммирования"
description: "В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для выполнения инвентаризации и суммирования на основе данных уже созданных текстовых выходных данных."
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 7261a2324b61cacfca8d69ad52762aa545b70220
ms.contentlocale: ru-ru
ms.lasthandoff: 08/09/2018

---
# <a name="create-electronic-reporting-er-formats-to-do-counting-and-summing"></a><span data-ttu-id="fb7bf-103">Создание форматов электронной отчетности (ER) для подсчета и суммирования</span><span class="sxs-lookup"><span data-stu-id="fb7bf-103">Create Electronic reporting (ER) formats to do counting and summing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fb7bf-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для выполнения инвентаризации и суммирования на основе данных уже созданных текстовых выходных данных.</span><span class="sxs-lookup"><span data-stu-id="fb7bf-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="fb7bf-105">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="fb7bf-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="fb7bf-106">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="fb7bf-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="fb7bf-107">Эта процедура предназначена для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="fb7bf-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="fb7bf-108">Получение доступа к списку конфигураций, предоставленных компанией Microsoft</span><span class="sxs-lookup"><span data-stu-id="fb7bf-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="fb7bf-109">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="fb7bf-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="fb7bf-110">Убедитесь, что поставщик Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="fb7bf-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="fb7bf-111">доступен и помечен как активный.</span><span class="sxs-lookup"><span data-stu-id="fb7bf-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="fb7bf-112">Выберите "Litware, Inc".</span><span class="sxs-lookup"><span data-stu-id="fb7bf-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="fb7bf-113">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="fb7bf-113">provider.</span></span>
3. <span data-ttu-id="fb7bf-114">Щелкните "Репозитории".</span><span class="sxs-lookup"><span data-stu-id="fb7bf-114">Click Repositories.</span></span>
    * <span data-ttu-id="fb7bf-115">Если репозиторий типа "Операционные ресурсы" уже существует, пропустите остальные шаги текущей подзадачи.</span><span class="sxs-lookup"><span data-stu-id="fb7bf-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="fb7bf-116">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="fb7bf-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="fb7bf-117">В поле "Тип репозитория конфигурации" введите "Операционные ресурсы".</span><span class="sxs-lookup"><span data-stu-id="fb7bf-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="fb7bf-118">Щелкните "Создать репозиторий".</span><span class="sxs-lookup"><span data-stu-id="fb7bf-118">Click Create repository.</span></span>
7. <span data-ttu-id="fb7bf-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="fb7bf-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="fb7bf-120">Получение конфигураций Интрастат, предоставленных компанией Microsoft</span><span class="sxs-lookup"><span data-stu-id="fb7bf-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="fb7bf-121">Щелкните Открыть.</span><span class="sxs-lookup"><span data-stu-id="fb7bf-121">Click Open.</span></span>
2. <span data-ttu-id="fb7bf-122">В дереве выберите "Модель Интрастат\Интрастат (DE)".</span><span class="sxs-lookup"><span data-stu-id="fb7bf-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="fb7bf-123">Нажмите кнопку Импорт.</span><span class="sxs-lookup"><span data-stu-id="fb7bf-123">Click Import.</span></span>
    * <span data-ttu-id="fb7bf-124">Щелкните "Импорт" для версии 1.1 выбранной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="fb7bf-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="fb7bf-125">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="fb7bf-125">Click Yes.</span></span>
5. <span data-ttu-id="fb7bf-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="fb7bf-126">Close the page.</span></span>
6. <span data-ttu-id="fb7bf-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="fb7bf-127">Close the page.</span></span>
7. <span data-ttu-id="fb7bf-128">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="fb7bf-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="fb7bf-129">В дереве разверните узел "Модель Интрастат".</span><span class="sxs-lookup"><span data-stu-id="fb7bf-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="fb7bf-130">В дереве выберите "Модель Интрастат\Интрастат (DE)".</span><span class="sxs-lookup"><span data-stu-id="fb7bf-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>


