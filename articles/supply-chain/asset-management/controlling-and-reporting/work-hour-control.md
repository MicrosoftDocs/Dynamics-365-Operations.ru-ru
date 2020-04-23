---
title: Контроль рабочих часов
description: В этом разделе описывается контроль рабочих часов в модуле "Управление активами".
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4ba1c9548ac7ad54a459f42fd9f8f20c6936f14c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216380"
---
# <a name="work-hour-control"></a><span data-ttu-id="23199-103">Контроль рабочих часов</span><span class="sxs-lookup"><span data-stu-id="23199-103">Work hour control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="23199-104">В управлении активами можно рассчитать часы, чтобы получить обзор фактических часов по сравнению с бюджетными часами по активам, функциональным местоположениям или заказам на работу.</span><span class="sxs-lookup"><span data-stu-id="23199-104">In Asset Management, you can calculate hours to get an overview of actual hours compared to budget hours on assets, functional locations, or work orders.</span></span> <span data-ttu-id="23199-105">Фактические часы основываются на разнесенных проводках.</span><span class="sxs-lookup"><span data-stu-id="23199-105">Actual hours are based on posted transactions.</span></span>

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="23199-106">Управление рабочими часами для активов, функциональных местоположений и заказов на работу</span><span class="sxs-lookup"><span data-stu-id="23199-106">Work hour control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="23199-107">Расчеты, выполняемые для активов, функциональных местоположений и заказов на работу, практически идентичны.</span><span class="sxs-lookup"><span data-stu-id="23199-107">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="23199-108">Единственное отличие заключается в том, что для активов и функциональных местоположений можно также включить в расчет вложенные активы и вложенные функциональные местоположения.</span><span class="sxs-lookup"><span data-stu-id="23199-108">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="23199-109">Датой является дата проводки, в которую была записана регистрация.</span><span class="sxs-lookup"><span data-stu-id="23199-109">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="23199-110">Щелкните **Управление активами** > **Запросы** > **Активы** > **Управление рабочими часами по активам** или **Управление рабочими часами функционального местоположения**, или **Управление активами** > **Запросы** > **Заказы на работу** > **Управление рабочими часами по заказам на работу**.</span><span class="sxs-lookup"><span data-stu-id="23199-110">Click **Asset management** > **Inquiries** > **Assets** > **Asset hour control** or **Functional location hour control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order hour control**.</span></span>

2. <span data-ttu-id="23199-111">В диалоговом окне **Управление рабочими часами по активам**.</span><span class="sxs-lookup"><span data-stu-id="23199-111">In the **Asset hour control** dialog, .</span></span>

3. <span data-ttu-id="23199-112">В диалоговом окне **Управление рабочими часами по активам** / **Управление рабочими часами по функциональным местоположениям** / **Управление рабочими часами по заказам на работу** выберите период, который должен рассчитываться, в полях **Начальная дата** и **Конечная дата**.</span><span class="sxs-lookup"><span data-stu-id="23199-112">In the **Asset hour control** / **Functional location hour control** / **Work order hour control** dialog, select a period to be calculated in the **From date** and **To date** fields.</span></span>

4. <span data-ttu-id="23199-113">При необходимости выберите **Набор финансовых аналитик**, который необходимо включить в расчет.</span><span class="sxs-lookup"><span data-stu-id="23199-113">If required, select a **Financial dimension set** to be included in the calculation.</span></span>

5. <span data-ttu-id="23199-114">Если не требуется показывать результаты, содержащие нулевые часы, выберите "Да" для переключателя **Исключать нули**.</span><span class="sxs-lookup"><span data-stu-id="23199-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results containing zero hours.</span></span>

6. <span data-ttu-id="23199-115">Можно использовать поле **Уровень**, чтобы указать, насколько подробными должны быть строки управления часами относительно функциональных местоположений.</span><span class="sxs-lookup"><span data-stu-id="23199-115">You can use the **Level** field to indicate how detailed you want the hour control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="23199-116">Например, если вставить число "1" в это поле, и имеется иерархия функциональных местоположений с несколькими уровнями, все строки управления часами для функционального местоположения будут показаны на верхнем уровне, и поэтому часы по строке могут быть добавлены из функциональных местоположений, расположенных на более низком уровне.</span><span class="sxs-lookup"><span data-stu-id="23199-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all hour control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="23199-117">Если вставить число "0" в поле **Уровень**, будет выведен подробный результат, отображающий все строки управления часами на всех уровнях функциональных местоположений, к которым они относятся.</span><span class="sxs-lookup"><span data-stu-id="23199-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all hour control lines on all the functional location levels to which they are related.</span></span>

7. <span data-ttu-id="23199-118">Выберите "Да" для переключателя **Включить вложенные активы** для отображения затрат, относящихся к вложенным активам, в виде отдельных строк.</span><span class="sxs-lookup"><span data-stu-id="23199-118">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="23199-119">Если требуется ограничить поиск, можно выбрать отдельные активы/функциональные местоположения/заказы на работу на экспресс-вкладке **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="23199-119">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="23199-120">Нажмите **ОК**, чтобы начать расчет.</span><span class="sxs-lookup"><span data-stu-id="23199-120">Click **OK** to start the calculation.</span></span>

10. <span data-ttu-id="23199-121">На странице **Управление часами по активам** щелкните **Группировать по**, чтобы отобразить необходимый уровень детализации для расчета.</span><span class="sxs-lookup"><span data-stu-id="23199-121">On the **Asset hour control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="23199-122">Выбранные кнопки **Группировать по...** выделяются.</span><span class="sxs-lookup"><span data-stu-id="23199-122">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="23199-123">Нажимайте кнопку, чтобы активировать или деактивировать ее.</span><span class="sxs-lookup"><span data-stu-id="23199-123">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="23199-124">Пример</span><span class="sxs-lookup"><span data-stu-id="23199-124">Example</span></span>

<span data-ttu-id="23199-125">На следующем снимке экрана показан пример расчета **Управление часами по активам**.</span><span class="sxs-lookup"><span data-stu-id="23199-125">The screenshot below shows an example of an **Asset hour control** calculation.</span></span>

- <span data-ttu-id="23199-126">В поле **Исходный бюджет** отображаются бюджетные часы из прогноза заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="23199-126">The **Original budget** field shows budget hours from the work order forecast.</span></span> 
- <span data-ttu-id="23199-127">В поле **Фактические часы** отображаются разнесенные часы по заказам на работу.</span><span class="sxs-lookup"><span data-stu-id="23199-127">The **Actual hours** field shows posted hours on work orders.</span></span> 
- <span data-ttu-id="23199-128">В поле **Подтвержденные часы** отображается общая сумма часов, которые подтверждены компанией в связи с заказами на работу.</span><span class="sxs-lookup"><span data-stu-id="23199-128">The **Committed hours** field shows total amount of hours that your company is committed to in relation to work orders.</span></span>

![Пример расчета управления часами по активам](media/04-controlling-and-reporting.png)

<span data-ttu-id="23199-130">Другим способом расчета часов является выбор нескольких активов в разделе **Все активы** или **Активные активы**.</span><span class="sxs-lookup"><span data-stu-id="23199-130">Another way of making an hour calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="23199-131">Затем нажмите кнопку **Управление часами** на экспресс-вкладке **Общие**.</span><span class="sxs-lookup"><span data-stu-id="23199-131">Then you click the **Hour control** button on the **General** FastTab.</span></span> <span data-ttu-id="23199-132">Выбранные активы автоматически вставляются в поле **Актив** на экспресс-вкладке **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="23199-132">The selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="23199-133">Щелкните **ОК** в диалоговом окне **Управление рабочими часами по активам**, и отобразится расчет для выбранных активов.</span><span class="sxs-lookup"><span data-stu-id="23199-133">Click **OK** in the **Asset hour control** dialog, and the calculation for the selected assets is shown.</span></span> <span data-ttu-id="23199-134">Эта же процедура может быть выполнена для функциональных местоположений в разделе **Все функциональные местоположения** или **Активные функциональные местоположения**, а также для заказов на работу в разделе **Все заказы на работу** или **Активные заказы на работу**.</span><span class="sxs-lookup"><span data-stu-id="23199-134">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>


