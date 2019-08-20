---
title: Уровни обслуживания активов
description: В этом разделе описываются уровни обслуживания активов в «Управлении активами».
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
ms.openlocfilehash: f079e6899a2e3949eff5945f867472c801d9e95c
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783552"
---
# <a name="asset-service-levels"></a><span data-ttu-id="aa445-103">Уровни обслуживания активов</span><span class="sxs-lookup"><span data-stu-id="aa445-103">Asset service levels</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="aa445-104">В этом разделе описываются уровни обслуживания активов в «Управлении активами».</span><span class="sxs-lookup"><span data-stu-id="aa445-104">This topic explains asset service levels in Asset Management.</span></span> <span data-ttu-id="aa445-105">Уровни обслуживания активов связаны с активами и перемещаются в запросы на обслуживание и заказы на работу.</span><span class="sxs-lookup"><span data-stu-id="aa445-105">Asset service levels are related to assets, and are transferred to maintenance requests and work orders.</span></span> <span data-ttu-id="aa445-106">Они используются для расчета приоритета заказов на работу при планировании заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="aa445-106">They are used to calculate the priority of work orders during work order scheduling.</span></span> <span data-ttu-id="aa445-107">Уровни обслуживания активов могут быть изменены, если требуются изменения.</span><span class="sxs-lookup"><span data-stu-id="aa445-107">Asset service levels can be changed, if changes are required.</span></span>

<span data-ttu-id="aa445-108">Для получения дополнительной информации о настройке, связанной с расчетом рейтинговых оценок для планирования заказа на работу, см. раздел [Параметры управления активами](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="aa445-108">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span> <span data-ttu-id="aa445-109">Необходимо настроить по крайней мере одну запись по умолчанию для уровня обслуживания активов.</span><span class="sxs-lookup"><span data-stu-id="aa445-109">You must set up at least one default record for the asset service level.</span></span> <span data-ttu-id="aa445-110">Эта запись по умолчанию используется, если во время планирования заказа на работу не найдено другого совпадения.</span><span class="sxs-lookup"><span data-stu-id="aa445-110">This default record is used if no other match is found during work order scheduling.</span></span>

<span data-ttu-id="aa445-111">**Пример 1:** Уровень обслуживания по умолчанию, используемый, если не найдено другого совпадения.</span><span class="sxs-lookup"><span data-stu-id="aa445-111">**Example 1:** The default service level that is used if no other match is found.</span></span> <span data-ttu-id="aa445-112">В этой записи вы выбираете только уровень обслуживания.</span><span class="sxs-lookup"><span data-stu-id="aa445-112">In this record, you select only a service level.</span></span>

<span data-ttu-id="aa445-113">**Пример 2:** Высокий уровень обслуживания, который используется для планирования заданий для двигателя грузовика Volvo.</span><span class="sxs-lookup"><span data-stu-id="aa445-113">**Example 2:** A high service level that is used to schedule jobs for a Volvo truck engine.</span></span> <span data-ttu-id="aa445-114">В этой записи вы выбираете соответствующий тип активов (например, **Двигатель грузовика**), производитель (**Volvo**), и уровень обслуживания.</span><span class="sxs-lookup"><span data-stu-id="aa445-114">In this record, you select a relevant asset type (such as **Truck Engine**), a manufacturer (**Volvo**), and a service level.</span></span>

## <a name="set-up-asset-service-levels"></a><span data-ttu-id="aa445-115">Настройте уровни обслуживания актива</span><span class="sxs-lookup"><span data-stu-id="aa445-115">Set up asset service levels</span></span>

1. <span data-ttu-id="aa445-116">Выберите **Управление активами** \> **Настройка** \> **Уровни обслуживания актива**.</span><span class="sxs-lookup"><span data-stu-id="aa445-116">Select **Asset management** \> **Setup** \> **Asset service levels**.</span></span>
2. <span data-ttu-id="aa445-117">Выберите **Создать**, чтобы создать запись.</span><span class="sxs-lookup"><span data-stu-id="aa445-117">Select **New** to create a record.</span></span>
3. <span data-ttu-id="aa445-118">В зависимости от уровня детализации, который требуется для уровня обслуживания активов, сделайте соответствующие выборы в полях **Функциональное местоположение**, **Тип актива**, **Производитель**, **Модель**, **Актив**, **Тип заказа на работу**, и **Уровень обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="aa445-118">Depending on the detail level that is required for the asset service level, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Work order type**, and **Service level** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="aa445-119">Когда уровень обслуживания активов используется для запросов на обслуживание и заказов на работу, «Управление активами» проходит все записи об уровне обслуживания активов, чтобы проверить на возможное совпадение.</span><span class="sxs-lookup"><span data-stu-id="aa445-119">When the asset service level is used for maintenance requests and work orders, Asset Management goes through all asset service level records to check for a possible match.</span></span> <span data-ttu-id="aa445-120">Она всегда проверяет наиболее конкретные комбинации в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="aa445-120">It always checks the most specific combination first.</span></span> <span data-ttu-id="aa445-121">Другими словами, «Управление активами» сначала проверяет соответствие для поля **Тип заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="aa445-121">In other words, Asset Management first checks for a match for the **Work order type** field.</span></span> <span data-ttu-id="aa445-122">Если совпадение не найдено, оно проверяет на совпадение поле **Актив** и т.д.</span><span class="sxs-lookup"><span data-stu-id="aa445-122">If no match is found, it checks for a match for the **Asset** field, and so on.</span></span> <span data-ttu-id="aa445-123">Как вы можете видеть в макете страницы **Уровни обслуживания актива**, это поведение означает, что, чтобы найти наиболее конкретную комбинацию, «Управление активами» проверяет каждую запись справа налево на совпадение.</span><span class="sxs-lookup"><span data-stu-id="aa445-123">As you can see in the layout of the **Asset service levels** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="aa445-124">Если совпадение не найдено, используется запись по умолчанию, которая не имеет выбора в этих полях.</span><span class="sxs-lookup"><span data-stu-id="aa445-124">If no match is found, the default record that has no selections in those fields is used.</span></span>

4. <span data-ttu-id="aa445-125">В поле **Уровень обслуживания** выберите номер, указывающий на уровень обслуживания (приоритет).</span><span class="sxs-lookup"><span data-stu-id="aa445-125">In the **Service level** field, select a number that indicates the service level (priority).</span></span>


> [!NOTE]
> <span data-ttu-id="aa445-126">Если вы измените запись уровня обслуживания актива на странице **Уровни обслуживания актива** после того, как вы уже использовали ее в заказе на работу, уровень обслуживания запросов на обслуживание и заказов на работу не обновляется соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="aa445-126">If you change an asset service level record on the **Asset service levels** page after you've already used it on a work order, the service level on maintenance requests and work orders isn't updated accordingly.</span></span>
