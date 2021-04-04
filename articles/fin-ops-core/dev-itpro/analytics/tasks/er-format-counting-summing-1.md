---
title: Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 1. Создание формата)
description: В этой теме описывается, как настроить формат электронный отчетности для выполнения инвентаризации и суммирования на основе данных уже созданного текстового вывода. (Часть 1)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 64bf9f48319029e835f9e3fe2b888625100cc408
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565151"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="7399d-104">Электронная отчетность — Настройка формата для инвентаризации и суммирования (Часть 1. Создание формата)</span><span class="sxs-lookup"><span data-stu-id="7399d-104">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7399d-105">В следующих шагах поясняется, как пользователь, которому назначена роль системного администратора или разработчика электронной отчетности, может настроить формат электронной отчетности (ER) для выполнения инвентаризации и суммирования на основе данных уже созданных текстовых выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7399d-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="7399d-106">Эти шаги можно выполнить в любой компании.</span><span class="sxs-lookup"><span data-stu-id="7399d-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="7399d-107">Для выполнения этих шагов необходимо сначала выполнить шаги в процедуре "Создание поставщика конфигурации и установка его в качестве активного".</span><span class="sxs-lookup"><span data-stu-id="7399d-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="7399d-108">Эта процедура для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="7399d-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="7399d-109">Получение доступа к списку конфигураций, предоставленных компанией Microsoft</span><span class="sxs-lookup"><span data-stu-id="7399d-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="7399d-110">Перейдите в раздел "Управление организацией" > "Рабочие области" > "Электронная отчетность".</span><span class="sxs-lookup"><span data-stu-id="7399d-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="7399d-111">Убедитесь, что поставщик Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="7399d-111">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="7399d-112">доступен и помечен как активный.</span><span class="sxs-lookup"><span data-stu-id="7399d-112">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="7399d-113">Выберите "Litware, Inc".</span><span class="sxs-lookup"><span data-stu-id="7399d-113">Select the "Litware, Inc."</span></span> <span data-ttu-id="7399d-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="7399d-114">provider.</span></span>
3. <span data-ttu-id="7399d-115">Щелкните "Репозитории".</span><span class="sxs-lookup"><span data-stu-id="7399d-115">Click Repositories.</span></span>
    * <span data-ttu-id="7399d-116">Если репозиторий типа "Операционные ресурсы" уже существует, пропустите остальные шаги текущей подзадачи.</span><span class="sxs-lookup"><span data-stu-id="7399d-116">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="7399d-117">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="7399d-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="7399d-118">В поле "Тип репозитория конфигурации" введите "Операционные ресурсы".</span><span class="sxs-lookup"><span data-stu-id="7399d-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="7399d-119">Щелкните "Создать репозиторий".</span><span class="sxs-lookup"><span data-stu-id="7399d-119">Click Create repository.</span></span>
7. <span data-ttu-id="7399d-120">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="7399d-120">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="7399d-121">Получение конфигураций Интрастат, предоставленных компанией Microsoft</span><span class="sxs-lookup"><span data-stu-id="7399d-121">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="7399d-122">Щелкните Открыть.</span><span class="sxs-lookup"><span data-stu-id="7399d-122">Click Open.</span></span>
2. <span data-ttu-id="7399d-123">В дереве выберите "Модель Интрастат\Интрастат (DE)".</span><span class="sxs-lookup"><span data-stu-id="7399d-123">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="7399d-124">Нажмите кнопку Импорт.</span><span class="sxs-lookup"><span data-stu-id="7399d-124">Click Import.</span></span>
    * <span data-ttu-id="7399d-125">Щелкните "Импорт" для версии 1.1 выбранной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="7399d-125">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="7399d-126">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="7399d-126">Click Yes.</span></span>
5. <span data-ttu-id="7399d-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="7399d-127">Close the page.</span></span>
6. <span data-ttu-id="7399d-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="7399d-128">Close the page.</span></span>
7. <span data-ttu-id="7399d-129">Щелкните "Конфигурации отчетности".</span><span class="sxs-lookup"><span data-stu-id="7399d-129">Click Reporting configurations.</span></span>
8. <span data-ttu-id="7399d-130">В дереве разверните узел "Модель Интрастат".</span><span class="sxs-lookup"><span data-stu-id="7399d-130">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="7399d-131">В дереве выберите "Модель Интрастат\Интрастат (DE)".</span><span class="sxs-lookup"><span data-stu-id="7399d-131">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]