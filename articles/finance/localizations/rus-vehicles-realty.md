---
title: Транспортные средства и недвижимость как основные средства (Россия)
description: В этом разделе описан порядок настройки и использования транспортных средств и недвижимости в качестве основных средств для России.
author: ShylaThompson
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.search.industry: ''
ms.author: roschlom
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: d98fd4ce7e1c706f4e235263cff2fd9f2c125b13
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979624"
---
# <a name="vehicles-and-realty-as-fixed-assets-russia"></a><span data-ttu-id="a4b1c-103">Транспортные средства и недвижимость как основные средства (Россия)</span><span class="sxs-lookup"><span data-stu-id="a4b1c-103">Vehicles and realty as fixed assets (Russia)</span></span>

[!include [banner](../includes/banner.md)]

## <a name="set-up-the-depreciation-start-date-for-vehicle-and-realty-assets"></a><span data-ttu-id="a4b1c-104">Настройка даты начала амортизации для транспортных средств и объектов недвижимости</span><span class="sxs-lookup"><span data-stu-id="a4b1c-104">Set up the depreciation start date for vehicle and realty assets</span></span>

<span data-ttu-id="a4b1c-105">Используйте страницу **Амортизационные группы**, чтобы задать дату начала для амортизации основных средств типов **Недвижимость** и **Транспортное средство**.</span><span class="sxs-lookup"><span data-stu-id="a4b1c-105">Use the **Depreciation groups** page to set up the start date for depreciation of fixed assets of the **Realty** and **Vehicle** types.</span></span>

<span data-ttu-id="a4b1c-106">Можно указать, что расчет амортизации должен основываться на дате регистрации актива.</span><span class="sxs-lookup"><span data-stu-id="a4b1c-106">You can specify that the calculation of depreciation should be based on the registration date of the asset.</span></span> <span data-ttu-id="a4b1c-107">Если актив зарегистрирован после ввода в эксплуатацию, амортизация вычисляется с первого дня месяца регистрации.</span><span class="sxs-lookup"><span data-stu-id="a4b1c-107">If an asset is registered after it's put into operation, depreciation is calculated from the first day of the month of registration.</span></span> <span data-ttu-id="a4b1c-108">Если актив зарегистрирован до ввода в эксплуатацию, амортизация вычисляется с первого дня месяца после ввода актива в эксплуатацию.</span><span class="sxs-lookup"><span data-stu-id="a4b1c-108">If an asset is registered before it's put into operation, depreciation is calculated from the first day of the month after the asset is put into operation.</span></span>

1. <span data-ttu-id="a4b1c-109">Перейдите в пункт **Основные средства (Россия)** \> **Настройка** \> **Группы амортизации**.</span><span class="sxs-lookup"><span data-stu-id="a4b1c-109">Go to **Fixed assets (Russia)** \> **Setup** \> **Depreciation groups**.</span></span>
2. <span data-ttu-id="a4b1c-110">Создайте группу амортизации, затем введите требуемую информацию.</span><span class="sxs-lookup"><span data-stu-id="a4b1c-110">Create a depreciation group, and enter the required details.</span></span>
3. <span data-ttu-id="a4b1c-111">На экспресс-вкладке **Общие** в поле **Дата начала начисления амортизации** выберите **Дата регистрации**, чтобы указать, что дату регистрации ОС следует использовать в качестве даты начала амортизации.</span><span class="sxs-lookup"><span data-stu-id="a4b1c-111">On the **General** FastTab, in the **Depreciation start date** field, select **Date of the registration** to specify that the registration date of a fixed asset should be used as the depreciation start date.</span></span>

## <a name="specify-the-registration-date-for-vehicle-and-realty-assets"></a><span data-ttu-id="a4b1c-112">Указание даты регистрации транспортных средств объектов недвижимости</span><span class="sxs-lookup"><span data-stu-id="a4b1c-112">Specify the registration date for vehicle and realty assets</span></span>

1. <span data-ttu-id="a4b1c-113">Перейдите в раздел **Основные средства (Россия)** \> **Общие** \> **Основные средства**.</span><span class="sxs-lookup"><span data-stu-id="a4b1c-113">Go to **Fixed assets (Russia)** \> **Common** \> **Fixed assets**.</span></span>
2. <span data-ttu-id="a4b1c-114">Выберите **Создать**, чтобы создать группу основных средств, затем введите нужные сведения.</span><span class="sxs-lookup"><span data-stu-id="a4b1c-114">Select **New** to create a fixed asset, and enter the required details.</span></span>
3. <span data-ttu-id="a4b1c-115">На экспресс-вкладке **Общее** в поле **Тип** выберите **Недвижимость**.</span><span class="sxs-lookup"><span data-stu-id="a4b1c-115">On the **General** FastTab, in the **Type** field, select **Realty**.</span></span>
4. <span data-ttu-id="a4b1c-116">На экспресс-вкладке **Техническая информация** в поле **Дата регистрации** выберите дату регистрации основного средства.</span><span class="sxs-lookup"><span data-stu-id="a4b1c-116">On the **Technical information** FastTab, in the **Date of the registration** field, select the registration date of the fixed asset.</span></span>
5. <span data-ttu-id="a4b1c-117">В поле **Дата удаления из регистра** выберите дату, когда следует удалить актив из налогового реестра.</span><span class="sxs-lookup"><span data-stu-id="a4b1c-117">In the **Removal from the register date** field, select the date when the asset should be removed from the tax register.</span></span>

<span data-ttu-id="a4b1c-118">Дополнительные сведения об амортизации активов см. в разделе [Расчет амортизации (Россия)](rus-depreciation-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="a4b1c-118">For more information about asset depreciation, see [Calculate depreciation (Russia)](rus-depreciation-calculation.md).</span></span>
