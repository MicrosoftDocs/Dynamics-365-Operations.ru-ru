---
title: Создание актива
description: В этом разделе описывается, как создавать активы в управлении активами.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
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
ms.openlocfilehash: 9f15c6c5ccdcddebe7aa428cff48ca6e3b120d7f
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783545"
---
# <a name="create-an-asset"></a><span data-ttu-id="8e2f0-103">Создание актива</span><span class="sxs-lookup"><span data-stu-id="8e2f0-103">Create an asset</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="8e2f0-104">В этом разделе описывается, как создавать активы в управлении активами.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-104">This topic describes how to create an asset in Asset Management.</span></span>

1. <span data-ttu-id="8e2f0-105">Нажмите **Управление активами** > **Общее** > **активы** > **Все активы** или **Активные активы**.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-105">Click **Asset management** > **Common** > **assets** > **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="8e2f0-106">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-106">Click the **New** button.</span></span>
3. <span data-ttu-id="8e2f0-107">В диалоговом окне **Создать активы** вставьте данные, относящиеся к параметру **Актив** (идентификатор актива) и имя актива.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-107">In the **Create assets** dialog, insert data regarding **Asset** (the asset ID) and the asset name.</span></span> <span data-ttu-id="8e2f0-108">Выберите дату и время для актива в поле **Действует**.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-108">Select date and time for the asset in the **Effective** field.</span></span> <span data-ttu-id="8e2f0-109">С этой даты можно установить актив в функциональном местоположении, а также переместить и заменить актив в структуре активов.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-109">From that date, you are able to install the asset on a functional location as well as move and replace the asset in an asset structure.</span></span>
4. <span data-ttu-id="8e2f0-110">В поле **Тип актива** выберите тип актива для актива (обязательное поле).</span><span class="sxs-lookup"><span data-stu-id="8e2f0-110">In the **Asset type** field, select the asset type for the asset (mandatory field).</span></span> <span data-ttu-id="8e2f0-111">При необходимости выберите для актива значения **Производитель актива** и **Модель актива**.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-111">If required, select **Asset manufacturer** and **Asset model** for the asset.</span></span> <span data-ttu-id="8e2f0-112">Если настроен только один продукт, этот продукт автоматически выбирается в поле **Производитель активов**.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-112">If only one product has been set up, that product is automatically selected in the **Asset manufacturer** field.</span></span> <span data-ttu-id="8e2f0-113">Варианты выбора, доступные в полях **Производитель актива** и **Модель актива**, зависят от настройки в разделе [Производитель и модель актива](../setup-for-objects/product-and-model.md).</span><span class="sxs-lookup"><span data-stu-id="8e2f0-113">The selections available in the **Asset manufacturer** and **Asset model** fields depend on the setup in [Asset manufacturer and model](../setup-for-objects/product-and-model.md).</span></span>
5. <span data-ttu-id="8e2f0-114">В группе **Родительский актив** поле **Актив** является пустым по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-114">In the **Parent asset** group, the **Asset** field is blank as default.</span></span> <span data-ttu-id="8e2f0-115">При необходимости можно выбрать родительский актив, после чего все поля в группе **Родительский актив** будут автоматически заполнены.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-115">If required, you can select a parent asset, and then all fields in the **Parent asset** group will automatically be filled out.</span></span>
>[!NOTE]  
><span data-ttu-id="8e2f0-116">При выборе родительского актива доступны две или три вкладки: вкладка **Мои активы** содержит активы, связанные с функциональными местоположениями, в которые вы (как специалист по обслуживанию, выполнивший вход в систему) можете быть назначены.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-116">When you select a parent asset, two or three tabs are available: The **My assets** tab contains assets related to the functional locations to which you (the maintenance worker who is logged on the system) may be allocated.</span></span> <span data-ttu-id="8e2f0-117">Если функциональные местоположения настроены для специалиста по техническому обслуживанию в форме [Специалисты по техническому обслуживанию](../setup-for-objects/workers-and-worker-groups.md), вкладка **Мои активы** не будет видна.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-117">If no functional locations are set up on a maintenance worker in the [Maintenance workers](../setup-for-objects/workers-and-worker-groups.md) form, the **My assets** tab will not be visible.</span></span> <span data-ttu-id="8e2f0-118">Вкладка **Активные активы** содержит список всех активов с состоянием жизненного цикла актива "Активный".</span><span class="sxs-lookup"><span data-stu-id="8e2f0-118">The **Active assets** tab contains a list of all assets with asset lifecycle state "Active".</span></span> <span data-ttu-id="8e2f0-119">Вкладка **Представление актива** отображает представление дерева функциональных местоположений и ресурсов, установленных в этих местоположениях.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-119">The **Asset view** tab displays a tree view of functional locations and assets installed on those locations.</span></span>

6. <span data-ttu-id="8e2f0-120">Функциональное местоположение по умолчанию, созданное вами, предлагается для актива в группе **Актив** > поле **Функциональное местоположение**.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-120">The default functional location you have set up is suggested for the asset in the **Asset** group > **Functional location** field.</span></span> <span data-ttu-id="8e2f0-121">При необходимости выберите другое функциональное местоположение.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-121">Select another functional location, if required.</span></span>

>[!NOTE]
><span data-ttu-id="8e2f0-122">После создания актива его можно установить в другое функциональное местоположение, если требуется.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-122">After you have created an asset, you can install it on another functional location, if required.</span></span> <span data-ttu-id="8e2f0-123">Только активы верхнего уровня (активы без текущего родительского актива) могут быть установлены в функциональном местоположении.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-123">Only top-level assets (assets without a current parent asset) can be installed on a functional location.</span></span> <span data-ttu-id="8e2f0-124">Это означает, что вы устанавливаете верхний уровень, а также все дочерние активы в выбранном функциональном местоположении.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-124">This means that you install the top level as well as any child assets on the selected functional location.</span></span> <span data-ttu-id="8e2f0-125">Узнайте больше об установке активов в функциональных местоположениях в разделе [Функциональные местоположения](../functional-locations/introduction-to-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="8e2f0-125">Read more about installing assets on functional locations in [Functional locations](../functional-locations/introduction-to-functional-locations.md).</span></span>

7. <span data-ttu-id="8e2f0-126">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-126">Click **OK**.</span></span>
8. <span data-ttu-id="8e2f0-127">Выберите актив в списке **Все активы** и нажмите кнопку **Изменить**, чтобы добавить дополнительную информацию в актив.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-127">Select the asset in the **All Assets** list and click the **Edit** button to add further information to the asset.</span></span>

## <a name="general-information"></a><span data-ttu-id="8e2f0-128">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="8e2f0-128">General information</span></span>

<span data-ttu-id="8e2f0-129">Функциональное местоположение, с которым связан актив, отображается в поле **Функциональное местоположение**.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-129">The functional location to which the asset is related is shown in the **Functional location** field.</span></span> <span data-ttu-id="8e2f0-130">Если актив является родительским активом, количество связанных с ним дочерних активов отображается в поле **Дочерние**.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-130">If the asset is a parent asset, the number of children related to the asset is shown in the **Children** field.</span></span> <span data-ttu-id="8e2f0-131">Если актив является вложенным активом для существующего актива, идентификатор родительского актива отображается в поле **Родительский**.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-131">If the asset is a sub asset to an existing asset, the ID of the parent asset is shown in the **Parent** field.</span></span>

<span data-ttu-id="8e2f0-132">Вы можете изменить информацию **Производитель актива** и **Модель актива** в активе, которая используется для управления запасными частями, альтернативными запасными частями и значениями по умолчанию для типа задания.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-132">You can edit **Asset manufacturer** and **Asset model** information on the asset, which is used to manage spare parts, alternative spare parts, and job type defaults.</span></span> <span data-ttu-id="8e2f0-133">Для получения дополнительной информации см. раздел [Производитель и модель актива](../setup-for-objects/product-and-model.md).</span><span class="sxs-lookup"><span data-stu-id="8e2f0-133">Refer to [Asset manufacturer and model](../setup-for-objects/product-and-model.md) for more information.</span></span> <span data-ttu-id="8e2f0-134">Вы также можете добавить **Модельный год** и **Серийный номер**, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-134">You can also add information about **Model year** and **Serial number**, if required.</span></span>

<span data-ttu-id="8e2f0-135">**Текущее состояние жизненного цикла** используется для определения того, активен актив или нет.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-135">**Current lifecycle state** is used to define if the asset is active or inactive.</span></span> <span data-ttu-id="8e2f0-136">При создании актива этап всегда устанавливается на первый этап в группе этапов актива.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-136">When creating an asset, the stage is always set to the first stage in the asset stage group.</span></span> <span data-ttu-id="8e2f0-137">Когда вы будете готовы активировать актив, нажмите **Обновить состояние актива** и выберите состояние жизненного цикла, которое вы определили как "актив активен", и нажмите **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-137">When you are ready to activate an asset, click **Update asset state**, and select the lifecycle state that you have defined as "asset active", and click **OK**.</span></span>

<span data-ttu-id="8e2f0-138">**Примечание.** Когда актив настроен на "неактивный", больше невозможно создавать заказы на работу для актива.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-138">**Note:** When an asset is set to "inactive", it is no longer possible to create work orders for the asset.</span></span> <span data-ttu-id="8e2f0-139">Кроме того, нельзя планировать профилактические работы по техническому обслуживанию для неактивного актива.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-139">Also, you cannot schedule preventive maintenance jobs for an inactive asset.</span></span>

<span data-ttu-id="8e2f0-140">Поля **Уровень обслуживания** и **Критичность** относятся к заказам на работу, созданным для актива.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-140">The **Service level** and **Criticality** fields relate to work orders created for the asset.</span></span> <span data-ttu-id="8e2f0-141">Поля показывают числовые значения **Уровень обслуживания** и **Критичность**, рассчитанные для текущей настройки для актива.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-141">The fields show the **Service level** and **Criticality** numbers calculated for the current setup for the asset.</span></span> <span data-ttu-id="8e2f0-142">См. разделы [Уровни обслуживания активов](../setup-for-objects/object-priorities.md) и [Критичность активов](../setup-for-objects/object-criticalities.md) в отношении настройки этих значений.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-142">Refer to [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticalities](../setup-for-objects/object-criticalities.md) regarding setup of those values.</span></span>

## <a name="asset"></a><span data-ttu-id="8e2f0-143">ОС</span><span class="sxs-lookup"><span data-stu-id="8e2f0-143">Asset</span></span>

<span data-ttu-id="8e2f0-144">Можно выбрать **Ресурс** для актива.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-144">You can select a **Resource** for the asset.</span></span> <span data-ttu-id="8e2f0-145">Выбор ресурсов определяет, какой календарь используется для планирования заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-145">The resource selection determines which calendar is used for work order scheduling.</span></span> <span data-ttu-id="8e2f0-146">Выбор ресурсов часто используется для основных средств.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-146">Resource selection is often used for fixed assets.</span></span> <span data-ttu-id="8e2f0-147">В Dynamics 365 for Finance and Operations ресурсы и группы ресурсов настраиваются в разделах **Администрирование организации** > **Ресурсы** > **Группы ресурсов** или **Ресурсы**.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-147">In Dynamics 365 for Finance and Operations, resources and resource groups are set up in **Organization administration** > **Resources** > **Resource groups** or **Resources**.</span></span>

<span data-ttu-id="8e2f0-148">В поле **Номер основных средств** можно выбрать основное средство, которое будет связано с активом.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-148">In the **Fixed assets number** field, you can select a fixed asset to be related to the asset.</span></span> <span data-ttu-id="8e2f0-149">Это актуально, если ваш актив связан с инвестиционным проектом.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-149">This is relevant if your asset is related to an investment project.</span></span>

- <span data-ttu-id="8e2f0-150">Если актив связан с основным средством, можно создать тип заказа на работу, который будет использоваться для заказов на работу, связанных с инвестиционным проектом.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-150">If the asset is related to a fixed asset, you can create a work order type to be used for work orders related to an investment project.</span></span> 
- <span data-ttu-id="8e2f0-151">Информация об основных средствах для актива связана с модулем **Основные средства** в Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-151">Information about fixed assets for an asset is related to the **Fixed assets** module in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="8e2f0-152">Это означает, что в пункте **Основные средства** > **Основные средства** > **Основные средства** вы можете получить обзор проектов управления активами, которые могут быть связаны с основным средством, выбрав актив в списке и просмотрев содержимое в области **Связанные сведения** > раздел **Связанные проекты**.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-152">This means that in **Fixed assets** > **Fixed assets** > **Fixed assets**, you can get an overview of the Asset Management projects that may be related to a fixed asset by selecting the asset in the list and viewing the contents in the **Related information** pane > **Associated projects** section.</span></span>


## <a name="details"></a><span data-ttu-id="8e2f0-153">Подробно</span><span class="sxs-lookup"><span data-stu-id="8e2f0-153">Details</span></span>

<span data-ttu-id="8e2f0-154">В поле **Активен с** отображается дата, когда состояние жизненного цикла актива было обновлено до активного состояния (см. раздел [Состояния жизненного цикла активов](../setup-for-objects/object-stages.md) относительно настройки состояний жизненного цикла активов).</span><span class="sxs-lookup"><span data-stu-id="8e2f0-154">In the **Active from** field, the date on which you updated the asset lifecycle state to an active state (refer to [Asset lifecycle states](../setup-for-objects/object-stages.md) regarding setup of asset lifecycle states), is shown.</span></span> <span data-ttu-id="8e2f0-155">Если актив больше не активен и состояние жизненного цикла актива обновлено до неактивного состояния жизненного цикла, в поле **Активен по** отображается дата, с которой актив неактивен.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-155">If the asset is no longer active, and you have updated the asset lifecycle state to an inactive lifecycle state, the date from which the asset is inactive is shown in the **Active to** field.</span></span> <span data-ttu-id="8e2f0-156">Если необходимо, эти даты можно изменить вручную.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-156">If required, you can manually change those dates.</span></span>

<span data-ttu-id="8e2f0-157">При необходимости можно вставить ожидаемую дату замены актива в поле **Дата замены**.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-157">If required, you can insert an expected date for replacement of the asset in the **Replacement date** field.</span></span> <span data-ttu-id="8e2f0-158">Ориентировочная стоимость замены актива может быть вставлена в поле **Стоимость замены**.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-158">An estimated value for replacing the asset can be inserted in the **Replacement value** field.</span></span> <span data-ttu-id="8e2f0-159">Пример. Вы можете использовать информацию о замене, чтобы сравнить ее с затратами на обслуживание актива, а затем принять решение о покупке нового актива, если затраты на техническое обслуживание существующего актива быстро растут.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-159">Example: You can use replacement information to compare it with the costs of maintaining an asset, and subsequently make a decision for purchasing a new asset if maintenance costs on the existing asset increase rapidly.</span></span>

## <a name="notes"></a><span data-ttu-id="8e2f0-160">Основание</span><span class="sxs-lookup"><span data-stu-id="8e2f0-160">Notes</span></span>

<span data-ttu-id="8e2f0-161">Вы можете добавить заметки, связанные с активом, на экспресс-вкладке **Примечания**.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-161">You can add notes related to the asset on the **Notes** FastTab.</span></span> <span data-ttu-id="8e2f0-162">Перед написанием заметки нажмите кнопку **Добавить метку времени**, если хотите добавить в заметку информацию о пользователе и дату/метку времени.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-162">Click the **Add timestamp** button before you write the note, if you want to add user information and a date/timestamp to the note.</span></span>

## <a name="attributes"></a><span data-ttu-id="8e2f0-163">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="8e2f0-163">Attributes</span></span>

<span data-ttu-id="8e2f0-164">На этой экспресс-вкладке можно задать значения для атрибутов актива.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-164">On this FastTab, you can set values for asset attributes.</span></span> <span data-ttu-id="8e2f0-165">Эти атрибуты могут быть использованы для описания свойств или характеристик, относящихся к активу, например, размер, масса или конфигурация машины.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-165">These attributes can be used to describe properties or characteristics pertinent to the asset, for example, size, weight, or machine configuration.</span></span>

<span data-ttu-id="8e2f0-166">Щелкните **Добавить строку** и выберите тип атрибута.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-166">Click **Add line** and select the attribute type.</span></span> <span data-ttu-id="8e2f0-167">Затем вставьте **Значение**, связанное с типом атрибута, и сохраните запись.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-167">Next, insert the **Value** related to the attribute type and save the record.</span></span>

>[!NOTE] 
><span data-ttu-id="8e2f0-168">Можно получить обзор типов атрибутов активов и их отношения к активам в разделах **Атрибут актива** и **Обзор атрибутов активов**.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-168">You can get an overview of asset attribute types and their relation to the assets in **Asset attribute** and **Asset attribute overview**.</span></span> <span data-ttu-id="8e2f0-169">Для получения дополнительной информации обратитесь к разделу [Обзор атрибутов активов](../objects/object-specification-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8e2f0-169">Refer to [Asset attribute overview](../objects/object-specification-overview.md) for more information.</span></span>

## <a name="vendor"></a><span data-ttu-id="8e2f0-170">Поставщик</span><span class="sxs-lookup"><span data-stu-id="8e2f0-170">Vendor</span></span>

<span data-ttu-id="8e2f0-171">На экспресс-вкладке **Поставщик** выберите организацию поставщика для актива.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-171">On the **Vendor** FastTab, select a vendor account for the asset.</span></span> <span data-ttu-id="8e2f0-172">Кроме того, если гарантия поставщика была предоставлена, вы можете вставить гарантийную информацию здесь.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-172">Also, if a vendor warranty has been granted, you can insert warranty information here.</span></span>

## <a name="address"></a><span data-ttu-id="8e2f0-173">Адрес </span><span class="sxs-lookup"><span data-stu-id="8e2f0-173">Address</span></span>

<span data-ttu-id="8e2f0-174">На экспресс-вкладке **Адрес** можно вставить адрес оборудования.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-174">On the **Address** FastTab, you can insert the address of the equipment.</span></span> <span data-ttu-id="8e2f0-175">Если в актив не вставлен адрес, актив использует адрес родительского актива, если у родительского актива есть адрес.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-175">If no address is inserted on the asset, the asset uses the address of a parent asset, if the parent asset has an address.</span></span> <span data-ttu-id="8e2f0-176">Если никакой адрес не связан с активом или родительскими элементами в иерархии активов, может быть использован адрес функционального местоположения, в котором установлен актив.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-176">If no address is related to the asset or any parents in the asset hierarchy, the address of the functional location on which the asset is installed may be used.</span></span> <span data-ttu-id="8e2f0-177">Если это функциональное местоположение не имеет адреса, связанного с ним, адрес родительского функционального местоположения используется для актива.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-177">If that functional location does not have an address related to it, the address of the parent functional location is used on the asset.</span></span>

## <a name="asset-management-plans"></a><span data-ttu-id="8e2f0-178">Планы технического обслуживания активов</span><span class="sxs-lookup"><span data-stu-id="8e2f0-178">Asset management plans</span></span>

<span data-ttu-id="8e2f0-179">Планы технического обслуживания используются для планирования профилактических работ по техническому обслуживанию через регулярные промежутки времени на активе.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-179">Maintenance plans are used for scheduling preventive maintenance jobs at regular intervals on the asset.</span></span> <span data-ttu-id="8e2f0-180">На этой экспресс-вкладке можно настроить строки плана обслуживания для выбранного актива.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-180">On this FastTab, you can set up maintenance plan lines for the selected asset.</span></span> <span data-ttu-id="8e2f0-181">Циклы обслуживания могут быть настроены для различных активов, на которых необходимо выполнять аналогичную задачу через регулярные промежутки времени.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-181">Maintenance rounds can be set up for various assets, on which you need to carry out a similar task at regular intervals.</span></span> <span data-ttu-id="8e2f0-182">На вкладке **Планы обслуживания функционального местоположения** можно увидеть планы технического обслуживания, связанные с функциональным местоположением, в котором установлен актив.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-182">On the **Functional location maintenance plans** tab, you see the maintenance plans related to the functional location on which the asset is installed.</span></span>

>[!NOTE]
><span data-ttu-id="8e2f0-183">Если вы удалите строку плана обслуживания или цикл обслуживания, связанный с активом в пункте **Все активы**, вы также автоматически удалите все графики обслуживания со статусом "Созданный", которые были созданы на основе этого плана обслуживания или цикла обслуживания.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-183">If you delete a maintenance plan line or a maintenance round related to an asset in **All Asset**, you also automatically delete all maintenance schedules with status "Created" that have been created based on that maintenance plan or maintenance round.</span></span>

## <a name="functional-location-maintenance-plans"></a><span data-ttu-id="8e2f0-184">Планы обслуживания функционального местоположения</span><span class="sxs-lookup"><span data-stu-id="8e2f0-184">Functional location maintenance plans</span></span>

<span data-ttu-id="8e2f0-185">На этой экспресс-вкладке приводится обзор планов технического обслуживания, связанных с функциональным местоположением, в котором установлен актив.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-185">On this FastTab, you get an overview of the maintenance plans related to the functional location on which the asset is installed.</span></span>

## <a name="maintenance-rounds"></a><span data-ttu-id="8e2f0-186">Циклы технического обслуживания</span><span class="sxs-lookup"><span data-stu-id="8e2f0-186">Maintenance rounds</span></span>

<span data-ttu-id="8e2f0-187">На этой экспресс-вкладке можно добавить или удалить циклы обслуживания, которые связаны с активом.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-187">On this FastTab, you can add or remove maintenance rounds, which are related to the asset.</span></span>

## <a name="financial-dimensions"></a><span data-ttu-id="8e2f0-188">Финансовые аналитики</span><span class="sxs-lookup"><span data-stu-id="8e2f0-188">Financial dimensions</span></span>

<span data-ttu-id="8e2f0-189">Можно выбрать финансовые аналитики для актива.</span><span class="sxs-lookup"><span data-stu-id="8e2f0-189">You can select financial dimensions for the asset.</span></span>