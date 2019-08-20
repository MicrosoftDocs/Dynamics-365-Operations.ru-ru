---
title: Типы функциональных местоположений
description: В этом разделе объясняется, как создавать типы функциональных местоположений в «Управлении активами».
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb758f9ef205c06cbb9d18b498a5cd7c36012714
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783554"
---
# <a name="functional-location-types"></a><span data-ttu-id="c3eea-103">Типы функциональных местоположений</span><span class="sxs-lookup"><span data-stu-id="c3eea-103">Functional location types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="c3eea-104">В этом разделе объясняется, как создавать типы функциональных местоположений в «Управлении активами».</span><span class="sxs-lookup"><span data-stu-id="c3eea-104">This topic describes how to create functional location types in Asset Management.</span></span> <span data-ttu-id="c3eea-105">Типы функциональных местоположений используются для управления требованиями к функциональным местоположениям, включая то, как активы устанавливаются в функциональном местоположении.</span><span class="sxs-lookup"><span data-stu-id="c3eea-105">Functional location types are used to manage requirements for functional locations, including how assets are installed on a functional location.</span></span> <span data-ttu-id="c3eea-106">Можно настроить типы активов, планы обслуживания, атрибуты функционального местоположения и требования к атрибутам актива, которые будут использоваться в функциональном местоположении, использующем определенный тип функционального местоположения.</span><span class="sxs-lookup"><span data-stu-id="c3eea-106">You can set up asset types, maintenance plans, functional location attributes, and asset attribute requirements to be used on a functional location that uses the specific functional location type.</span></span> <span data-ttu-id="c3eea-107">При создании функционального местоположения тип функционального местоположения является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c3eea-107">When you create a functional location, the functional location type is mandatory.</span></span>

>[!NOTE] 
><span data-ttu-id="c3eea-108">Для работы с функциональными местоположениями необходимо создать функциональное местоположение по умолчанию, используемое только для создания новых активов.</span><span class="sxs-lookup"><span data-stu-id="c3eea-108">In order to work with functional locations, you must create a default functional location to be used only for the purpose of creating new assets.</span></span> <span data-ttu-id="c3eea-109">Для этого функционального местоположения по умолчанию следует создать тип функционального местоположения по умолчанию, который очень прост и позволяет устанавливать несколько активов в функциональном местоположении по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c3eea-109">For that default functional location, you should create a default functional location type that is really simple and allows multiple assets to be installed on the default functional location.</span></span> <span data-ttu-id="c3eea-110">Для получения дополнительной информации о том, как настроить функциональные местоположения, см. раздел [Создание функциональных местоположений](../functional-locations/create-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="c3eea-110">See [Create functional locations](../functional-locations/create-functional-locations.md) for more information on how to set up functional locations.</span></span>

## <a name="create-a-default-functional-location-type"></a><span data-ttu-id="c3eea-111">Создание типа функционального местоположения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c3eea-111">Create a default functional location type</span></span>

<span data-ttu-id="c3eea-112">Эта процедура показывает, как создать тип функционального местоположения по умолчанию, который будет использоваться для функционального местоположения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c3eea-112">This procedure shows how to create a default functional location type to be used for a default functional location.</span></span>

1. <span data-ttu-id="c3eea-113">Выберите **Управление активами** > **Настройка** > **Функциональные местоположения** > **Типы функционального местоположения**.</span><span class="sxs-lookup"><span data-stu-id="c3eea-113">Select **Asset management** > **Setup** > **Functional locations** > **Functional location types**.</span></span>
2. <span data-ttu-id="c3eea-114">Выберите **Создать**, чтобы создать тип функционального местоположения.</span><span class="sxs-lookup"><span data-stu-id="c3eea-114">Select **New** to create a functional location type.</span></span>
3. <span data-ttu-id="c3eea-115">Вставьте идентификатор типа функционального местоположения в поле **Тип функционального местоположения**, например, «По умолчанию», и имя в поле **Имя**.</span><span class="sxs-lookup"><span data-stu-id="c3eea-115">Insert a functional location type ID in the **Functional location type** field, for example, "Default", and a name in the **Name** field.</span></span>
4. <span data-ttu-id="c3eea-116">Выберите модель жизненного цикла актива в поле **Модель жизненного цикла актива функционального местоположения**.</span><span class="sxs-lookup"><span data-stu-id="c3eea-116">Select a lifecycle model in the **Functional location lifecycle model** field.</span></span>
5. <span data-ttu-id="c3eea-117">Выберите «Да» на кнопке-переключателе **Несколько активов**, чтобы с помощью этого типа можно было установить больше активов в функциональном местоположении (функциональное местоположение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="c3eea-117">Select "Yes" on the **Multiple assets** toggle button to allow more assets to be installed on a functional location (the default functional location) using this type.</span></span>

<span data-ttu-id="c3eea-118">Теперь создаетсятип функционального местоположения по умолчанию, который будет использоваться только для функционального местоположения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c3eea-118">Now, the default functional location type to be used only on a default functional location is created.</span></span> <span data-ttu-id="c3eea-119">Не следует добавлять дополнительные требования или ограничения к этому типу функционального местоположения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c3eea-119">You should not add any more requirements or restrictions to this default functional location type.</span></span>


## <a name="create-functional-location-types"></a><span data-ttu-id="c3eea-120">Создание типов функциональных местоположений</span><span class="sxs-lookup"><span data-stu-id="c3eea-120">Create Functional Location Types</span></span>

1. <span data-ttu-id="c3eea-121">Выберите **Управление активами** > **Настройка** > **Функциональные местоположения** > **Типы функционального местоположения**.</span><span class="sxs-lookup"><span data-stu-id="c3eea-121">Select **Asset Management** > **Setup** > **Functional locations** > **Functional location types**.</span></span>
2. <span data-ttu-id="c3eea-122">Выберите **Создать**, чтобы создать тип функционального местоположения.</span><span class="sxs-lookup"><span data-stu-id="c3eea-122">Select **New** to create a functional location type.</span></span>
3. <span data-ttu-id="c3eea-123">Вставьте идентификатор типа функционального местоположения в поле **Тип функционального местоположения** и имя в поле **Имя**.</span><span class="sxs-lookup"><span data-stu-id="c3eea-123">Insert a functional location type ID in the **Functional location type** field and a name in the **Name** field.</span></span>
4. <span data-ttu-id="c3eea-124">Выберите модель жизненного цикла актива в поле **Модель жизненного цикла актива функционального местоположения**.</span><span class="sxs-lookup"><span data-stu-id="c3eea-124">Select a lifecycle model in the **Functional location lifecycle model** field.</span></span> <span data-ttu-id="c3eea-125">Для получения дополнительной информации о состояниях жизненного цикла функционального местоположения и моделях жизненного цикла см. раздел [Состояния жизненного цикла функциональных местоположений](../setup-for-functional-locations/functional-location-stages.md).</span><span class="sxs-lookup"><span data-stu-id="c3eea-125">Refer to [Functional location lifecycle states](../setup-for-functional-locations/functional-location-stages.md) for more information on functional location lifecycle states and lifecycle models.</span></span>
5. <span data-ttu-id="c3eea-126">Выберите «Да» на кнопке-переключателе **Несколько активов**, если требуется возможность установить несколько активов в функциональном местоположении с помощью этого типа функционального местоположения.</span><span class="sxs-lookup"><span data-stu-id="c3eea-126">Select "Yes" on the **Multiple assets** toggle button if it should be possible to install several assets on a functional location using this functional location type.</span></span> <span data-ttu-id="c3eea-127">Если вы выберете «Нет», можно установить только *один* актив в функциональном местоположении, используя этот тип функционального местоположения.</span><span class="sxs-lookup"><span data-stu-id="c3eea-127">If you select "No", you can only install *one* asset on a functional location using this functional location type.</span></span>
6. <span data-ttu-id="c3eea-128">Выберите «Да» на кнопке-переключателе **Обновить аналитику актива**, если требуется, чтобы активы, установленные в функциональном местоположении этого типа, автоматически использовали финансовые аналитики, связанные с функциональным местоположением.</span><span class="sxs-lookup"><span data-stu-id="c3eea-128">Select "Yes" on the **Update asset dimension** toggle button if you want assets installed on a functional location of this type to automatically use the financial dimensions related to the functional location.</span></span> <span data-ttu-id="c3eea-129">Это означает, что при изменении финансовых аналитик в форме [Функциональное местоположение](../functional-locations/create-functional-locations.md), а функциональное местоположение использует тип функционального местоположения с помощью этой кнопки-переключателя, установленной на «Да», финансовые аналитики автоматически обновляются на всех активах, установленных в этом функциональном местоположении.</span><span class="sxs-lookup"><span data-stu-id="c3eea-129">This means that if you change financial dimensions in the [Functional location](../functional-locations/create-functional-locations.md) form, and the functional location uses a functional location type with this toggle button set to "Yes", financial dimensions are automatically updated on all assets installed on that functional location.</span></span>
7. <span data-ttu-id="c3eea-130">Поле **Тип актива** используется, если требуется автоматически создать *один* актив для функционального местоположения с тем же идентификатором и именем, что и функциональное местоположение, которое вы создаете.</span><span class="sxs-lookup"><span data-stu-id="c3eea-130">The **Asset type** field is used if you want to automatically create *one* asset for the functional location with the same ID and name as the functional location you are creating.</span></span> <span data-ttu-id="c3eea-131">Например, это может быть актуально, если вы создаете статическое функциональное местоположение, например здание или конвейер.</span><span class="sxs-lookup"><span data-stu-id="c3eea-131">For example, this may be relevant if you create a static functional location, such as a building or a pipeline.</span></span> <span data-ttu-id="c3eea-132">В этом случае выберите тип актива, который вы хотите использовать для автоматически созданного актива.</span><span class="sxs-lookup"><span data-stu-id="c3eea-132">In that case, select the asset type you want to use for the automatically created asset.</span></span> <span data-ttu-id="c3eea-133">Помните, что если вы делаете выбор в этом поле, кнопкапереклатель **Несколько активов** должна быть установлена на «Нет».</span><span class="sxs-lookup"><span data-stu-id="c3eea-133">Remember that if you make a selection in this field, the **Multiple assets** toggle button must be set to "No".</span></span>
8. <span data-ttu-id="c3eea-134">На экспресс-вкладке **Типы актива** выберите типы актива, которые должны быть связаны с типом функционального местоположения.</span><span class="sxs-lookup"><span data-stu-id="c3eea-134">On the **Asset types** FastTab, select the asset types to be related to the functional location type.</span></span> <span data-ttu-id="c3eea-135">Выберите **Добавить строку** и выберите типы актива.</span><span class="sxs-lookup"><span data-stu-id="c3eea-135">Select **Add line** and select the asset types.</span></span> <span data-ttu-id="c3eea-136">Если добавить типы активов здесь, только активы, использующие эти типы активов, могут быть установлены в функциональном местоположении, используя этот тип функционального местоположения.</span><span class="sxs-lookup"><span data-stu-id="c3eea-136">If you add asset types here, only assets using those asset types can be installed on a functional location using this functional location type.</span></span> <span data-ttu-id="c3eea-137">Если типы активов не выбраны на экспресс-вкладке **Типы актива**, могут быть установлены все типы активов.</span><span class="sxs-lookup"><span data-stu-id="c3eea-137">If no asset types are selected on the **Asset types** FastTab, all asset types may be installed.</span></span>
9. <span data-ttu-id="c3eea-138">На экспресс-вкладке **План обслуживания** выберите планы обслуживания, которые должны быть автоматически настроены на новых функциональных местоположениях с использованием этого типа функционального местоположения.</span><span class="sxs-lookup"><span data-stu-id="c3eea-138">On the **Maintenance plans** FastTab, select the maintenance plans that should automatically be set up on new functional locations using this functional location type.</span></span> <span data-ttu-id="c3eea-139">Выберите **Добавить строку** и выберите планы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c3eea-139">Select **Add line** and select the maintenance plans.</span></span> <span data-ttu-id="c3eea-140">Если добавить планы обслуживания здесь, только эти планы могут быть использованы на функциональном месте, используя этот функциональный тип местоположения.</span><span class="sxs-lookup"><span data-stu-id="c3eea-140">If you add maintenance plans here, only those plans can be used on a functional location using this functional location type.</span></span>
10. <span data-ttu-id="c3eea-141">На экспресс-вкладке **Требования к атрибутам актива** настройте атрибуты актива, которые должны быть автоматически настроены на новых функциональных местоположениях с использованием этого типа функционального местоположения.</span><span class="sxs-lookup"><span data-stu-id="c3eea-141">On the **Asset attribute requirements** FastTab, set up the asset attributes that should automatically be set up on new functional locations using this functional location type.</span></span> <span data-ttu-id="c3eea-142">Выберите **Добавить строку** и выберите атрибут.</span><span class="sxs-lookup"><span data-stu-id="c3eea-142">Select **Add line** and select the attribute.</span></span> <span data-ttu-id="c3eea-143">Эти требования к атрибутам функционируют как руководящие принципы.</span><span class="sxs-lookup"><span data-stu-id="c3eea-143">These attribute requirements function as guidelines.</span></span> <span data-ttu-id="c3eea-144">Они не проверяются относительно атрибутов, настроенных на активе (**Управление активами** > **Общее** > **Активы** > **Все активы** > выберите актив на странице списка > вкладка **Общее** > кнопка **Атрибуты**).</span><span class="sxs-lookup"><span data-stu-id="c3eea-144">They are not validated against attributes set up on an asset (**Asset management** > **Common** > **Assets** > **All assets** > select asset in the list page > **General** tab > **Attributes** button).</span></span> <span data-ttu-id="c3eea-145">Требования к атрибутам отображаются при установке активов в функциональные местоположения.</span><span class="sxs-lookup"><span data-stu-id="c3eea-145">The attribute requirements are shown when you install assets on functional locations.</span></span>
11. <span data-ttu-id="c3eea-146">На экспресс-вкладке **Допустимые типы** выберите типы функционального местоположения, которые должны быть действительными для вложенных типов функциональных местоположений, связанных с родительским типом функционального местоположения, который использует выбранный тип функционального местоположения.</span><span class="sxs-lookup"><span data-stu-id="c3eea-146">On the **Permitted types** FastTab, select the functional location types that should be valid for sub functional location types related to a parent functional location type, which uses the selected functional location type.</span></span>
12. <span data-ttu-id="c3eea-147">На экспресс-вкладке **Атрибуты** выберите атрибуты функционального местоположения, которые должны быть автоматически настроены на функциональных местоположениях с использованием этого типа функционального местоположения.</span><span class="sxs-lookup"><span data-stu-id="c3eea-147">On the **Attributes** FastTab, select the functional location attributes that should automatically be set up on functional locations using this functional location type.</span></span> <span data-ttu-id="c3eea-148">Выберите **Добавить строку** и выберите атрибут.</span><span class="sxs-lookup"><span data-stu-id="c3eea-148">Select **Add line** and select the attribute.</span></span>


>[!NOTE] 
><span data-ttu-id="c3eea-149">На экспресс-вкладке **Общее** можно получить обзор количества типов активов, планов обслуживания, требований к атрибутам активов, допустимых типов, атрибутов и функциональных местоположений, настроенных на тип функционального местоположения.</span><span class="sxs-lookup"><span data-stu-id="c3eea-149">On the **General** FastTab, you can get an overview of the number of asset types, maintenance plans, asset attribute requirements, permitted types, attributes, and functional locations set up on the functional location type.</span></span> <span data-ttu-id="c3eea-150">Поле **Функциональные местоположения** показывает количество функциональных местоположений, которые используют тип функционального местоположения.</span><span class="sxs-lookup"><span data-stu-id="c3eea-150">The **Functional locations** field shows the number of functional locations that use the functional location type.</span></span> <span data-ttu-id="c3eea-151">Кнопку **Копировать** можно использовать для копирования настроек из типа функционального местоположения в выбранный тип функционального местоположения.</span><span class="sxs-lookup"><span data-stu-id="c3eea-151">You can use the **Copy** button to copy settings from a functional location type to the selected functional location type.</span></span>