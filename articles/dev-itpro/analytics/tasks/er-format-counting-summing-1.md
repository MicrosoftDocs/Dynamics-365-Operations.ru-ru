--- 
title: "Создание формата для подсчета и суммирования для электронной отчетности (ER)"
description: "В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для выполнения инвентаризации и суммирования на основе данных уже созданных текстовых выходных данных."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.openlocfilehash: efdb64fa157af0d96c2ff0e5de3db5a98190bc68
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="create-formate-for-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="b471c-103">Создание формата для подсчета и суммирования для электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="b471c-103">Create formate for counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b471c-104">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для выполнения инвентаризации и суммирования на основе данных уже созданных текстовых выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b471c-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="b471c-105">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="b471c-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="b471c-106">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="b471c-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="b471c-107">Эта процедура предназначена для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="b471c-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="b471c-108">Получение доступа к списку конфигураций, предоставленных компанией Microsoft</span><span class="sxs-lookup"><span data-stu-id="b471c-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="b471c-109">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="b471c-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="b471c-110">Убедитесь, что поставщик Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="b471c-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="b471c-111">доступен и помечен как активный.</span><span class="sxs-lookup"><span data-stu-id="b471c-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="b471c-112">Выберите "Litware, Inc".</span><span class="sxs-lookup"><span data-stu-id="b471c-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="b471c-113">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="b471c-113">provider.</span></span>
3. <span data-ttu-id="b471c-114">Щелкните "Репозитории".</span><span class="sxs-lookup"><span data-stu-id="b471c-114">Click Repositories.</span></span>
    * <span data-ttu-id="b471c-115">Если репозиторий типа "Операционные ресурсы" уже существует, пропустите остальные шаги текущей подзадачи.</span><span class="sxs-lookup"><span data-stu-id="b471c-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="b471c-116">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b471c-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="b471c-117">В поле "Тип репозитория конфигурации" введите "Операционные ресурсы".</span><span class="sxs-lookup"><span data-stu-id="b471c-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="b471c-118">Щелкните "Создать репозиторий".</span><span class="sxs-lookup"><span data-stu-id="b471c-118">Click Create repository.</span></span>
7. <span data-ttu-id="b471c-119">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b471c-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="b471c-120">Получение конфигураций Интрастат, предоставленных компанией Microsoft</span><span class="sxs-lookup"><span data-stu-id="b471c-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="b471c-121">Щелкните Открыть.</span><span class="sxs-lookup"><span data-stu-id="b471c-121">Click Open.</span></span>
2. <span data-ttu-id="b471c-122">В дереве выберите "Модель Интрастат\Интрастат (DE)".</span><span class="sxs-lookup"><span data-stu-id="b471c-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="b471c-123">Нажмите кнопку Импорт.</span><span class="sxs-lookup"><span data-stu-id="b471c-123">Click Import.</span></span>
    * <span data-ttu-id="b471c-124">Щелкните "Импорт" для версии 1.1 выбранной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b471c-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="b471c-125">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="b471c-125">Click Yes.</span></span>
5. <span data-ttu-id="b471c-126">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b471c-126">Close the page.</span></span>
6. <span data-ttu-id="b471c-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b471c-127">Close the page.</span></span>
7. <span data-ttu-id="b471c-128">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="b471c-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="b471c-129">В дереве разверните узел "Модель Интрастат".</span><span class="sxs-lookup"><span data-stu-id="b471c-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="b471c-130">В дереве выберите "Модель Интрастат\Интрастат (DE)".</span><span class="sxs-lookup"><span data-stu-id="b471c-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>


