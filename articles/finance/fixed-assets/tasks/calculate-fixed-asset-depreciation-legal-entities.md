---
title: Расчет амортизации ОС в разных юридических лицах
description: Можно запустить амортизации основных средств для нескольких юридических лиц за один шаг.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 074a1b80584050302920a95c20fb547523a4866c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447059"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="56c6e-103">Расчет амортизации ОС в разных юридических лицах</span><span class="sxs-lookup"><span data-stu-id="56c6e-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="56c6e-104">Можно запустить амортизации основных средств для нескольких юридических лиц за один шаг.</span><span class="sxs-lookup"><span data-stu-id="56c6e-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="56c6e-105">Эта процедура показывает, как настроить и запустить процесс для нескольких юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="56c6e-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="56c6e-106">В нем используется роль бухгалтера и демонстрационные данные для юридического лица USMF.</span><span class="sxs-lookup"><span data-stu-id="56c6e-106">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="set-up-cross-company-depreciation-run-journals"></a><span data-ttu-id="56c6e-107">Настройка журналов запуска амортизации по нескольким компаниям</span><span class="sxs-lookup"><span data-stu-id="56c6e-107">Set up cross company depreciation run journals</span></span>
1. <span data-ttu-id="56c6e-108">Перейдите в раздел "Основные средства" > "Настройка" > "Параметры основных средств".</span><span class="sxs-lookup"><span data-stu-id="56c6e-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="56c6e-109">Разверните раздел "Предложения по ОС".</span><span class="sxs-lookup"><span data-stu-id="56c6e-109">Expand the Fixed asset proposals section.</span></span>
3. <span data-ttu-id="56c6e-110">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="56c6e-110">Click Add.</span></span>
4. <span data-ttu-id="56c6e-111">В поле "Слой разноски" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="56c6e-111">In the Posting layer field, enter or select a value.</span></span>
5. <span data-ttu-id="56c6e-112">В поле "Наименование журнала" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="56c6e-112">In the Journal name field, enter or select a value.</span></span>
    * <span data-ttu-id="56c6e-113">Повторите настройку журнала на странице "Параметры основных средств" в каждом юридическом лице.</span><span class="sxs-lookup"><span data-stu-id="56c6e-113">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span>  

## <a name="depreciation-run"></a><span data-ttu-id="56c6e-114">Запуск амортизации</span><span class="sxs-lookup"><span data-stu-id="56c6e-114">Depreciation run</span></span>
1. <span data-ttu-id="56c6e-115">Перейдите в раздел "Основные средства" > "Записи в журнале" > "Создать предложение по амортизации".</span><span class="sxs-lookup"><span data-stu-id="56c6e-115">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="56c6e-116">В поле "Слой разноски" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="56c6e-116">In the Posting layer field, enter or select a value.</span></span>
    * <span data-ttu-id="56c6e-117">Имя журнала по умолчанию берется из параметров основных средств.</span><span class="sxs-lookup"><span data-stu-id="56c6e-117">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="56c6e-118">Его можно изменить здесь для текущего юридического лица.</span><span class="sxs-lookup"><span data-stu-id="56c6e-118">It can be changed here for the current legal entity.</span></span>  
3. <span data-ttu-id="56c6e-119">В поле "Дата окончания" введите дату.</span><span class="sxs-lookup"><span data-stu-id="56c6e-119">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="56c6e-120">Выберите юридические лица для включения в прогон амортизации.</span><span class="sxs-lookup"><span data-stu-id="56c6e-120">Select the legal entities to be included in the depreciation run.</span></span>  
    * <span data-ttu-id="56c6e-121">В списке будут отображаться только юридические лица с журналами, настроенными для предложений ОС на странице "Параметры основных средств".</span><span class="sxs-lookup"><span data-stu-id="56c6e-121">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span>  
4. <span data-ttu-id="56c6e-122">В поле "Разнести журналы" выберите значение "Да".</span><span class="sxs-lookup"><span data-stu-id="56c6e-122">Select Yes in the Post journals field.</span></span>
    * <span data-ttu-id="56c6e-123">Поля фильтрации включают все основные средства, группы и книги для юридических лиц, выбранных для этого прогона амортизации.</span><span class="sxs-lookup"><span data-stu-id="56c6e-123">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span>  
    * <span data-ttu-id="56c6e-124">Параметр пакетной обработки по умолчанию включен.</span><span class="sxs-lookup"><span data-stu-id="56c6e-124">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="56c6e-125">Если этот параметр включен, создание и разноска журнала амортизации будут выполняться в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="56c6e-125">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span>  
5. <span data-ttu-id="56c6e-126">Щелкните "Создать журнал".</span><span class="sxs-lookup"><span data-stu-id="56c6e-126">Click Create journal.</span></span>
6. <span data-ttu-id="56c6e-127">Перейдите в раздел "Основные средства" > "Записи в журнале" > "Журнал основных средств".</span><span class="sxs-lookup"><span data-stu-id="56c6e-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

