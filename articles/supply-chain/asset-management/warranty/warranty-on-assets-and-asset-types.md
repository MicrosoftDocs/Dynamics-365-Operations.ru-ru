---
title: Гарантии на основные средства и типы основных средств
description: В этом разделе объясняется, как настроить гарантии на активы и типы активов в модуле "Управление активами".
author: josaw1
manager: tfehr
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 78ac93b1e681fca7d7eefd921f282a8496aa9d0a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245331"
---
# <a name="warranties-on-assets-and-asset-types"></a><span data-ttu-id="a8e1f-103">Гарантии на основные средства и типы основных средств</span><span class="sxs-lookup"><span data-stu-id="a8e1f-103">Warranties on assets and asset types</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="a8e1f-104">В этом разделе объясняется, как настроить гарантии на активы и типы активов в модуле "Управление активами".</span><span class="sxs-lookup"><span data-stu-id="a8e1f-104">This topic explains how to set up warranties on assets and asset types in Asset Management.</span></span>

## <a name="set-up-a-warranty-on-an-asset-type"></a><span data-ttu-id="a8e1f-105">Настройка гарантии на тип основных средств</span><span class="sxs-lookup"><span data-stu-id="a8e1f-105">Set up a warranty on an asset type</span></span>

1. <span data-ttu-id="a8e1f-106">Выберите **Управление активами** \> **Настройка** \> **Типы активов** \> **Типы активов**.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-106">Select **Asset management** \> **Setup** \> **Asset types** \> **Asset types**.</span></span>
2. <span data-ttu-id="a8e1f-107">В левой области выберите тип актива, к которому прикрепляются гарантийное соглашение поставщика, затем выберите **Значения по умолчанию для типа активов**.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-107">In the left pane, select the asset type to attach a vendor warranty agreement to, and then select **Asset type defaults**.</span></span>
3. <span data-ttu-id="a8e1f-108">На экспресс-вкладке **Общее** в поле **Гарантия поставщика** выберите соглашение.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-108">On the **General** FastTab, in the **Vendor warranty** field, select the agreement.</span></span>

## <a name="set-up-a-warranty-on-an-asset"></a><span data-ttu-id="a8e1f-109">Настройка гарантии на основное средство</span><span class="sxs-lookup"><span data-stu-id="a8e1f-109">Set up a warranty on an asset</span></span>

1. <span data-ttu-id="a8e1f-110">Выберите **Управление активами** \> **Общие** \> **Активы** \> **Все активы**.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-110">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="a8e1f-111">Выберите актив, затем выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-111">Select the asset, and then select **Edit**.</span></span>
3. <span data-ttu-id="a8e1f-112">На экспресс-вкладке **Поставщик** в разделе **Гарантия поставщика** в поле **Гарантия** выберите гарантийное соглашение.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-112">On the **Vendor** FastTab, in the **Vendor warranty** section, in the **Warranty** field, select the warranty agreement.</span></span>
4. <span data-ttu-id="a8e1f-113">В полях **Начало гарантии** и **Окончание гарантии** выберите начальную и конечную даты.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-113">In the **Warranty start** and **Warranty end** fields, select the start and end dates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="a8e1f-114">Если дата выбрана в поле **Начало гарантии** в заказе на работу, гарантия становится действительной для заказа на работу на эту дату.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-114">If a date is selected in the **Warranty start** field on a work order, the warranty becomes valid for the work order on that date.</span></span> <span data-ttu-id="a8e1f-115">При создании заказа на работу в поле **Начало гарантии** автоматически задается дата создания.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-115">When you create a work order, the **Warranty start** field is automatically set to the date of creation.</span></span> <span data-ttu-id="a8e1f-116">Однако дату можно изменить таким образом, чтобы она соответствовала, например, дате начала гарантийного соглашения.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-116">However, you can change the date so that it corresponds to, for example, the start date of a warranty agreement.</span></span>
    >
    > ![Страница заказов на работу](media/02-warranty.png)

> [!NOTE]
> <span data-ttu-id="a8e1f-118">При создании заказа на работу для актива, охватываемого гарантией поставщика, если заказ на работу имеет ожидаемую дату начала в течение гарантийного периода, вы получите уведомление о гарантийном соглашении.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-118">When you create a work order for an asset that is covered by a vendor warranty, if the work order has an expected start date during the warranty period, you receive a notification about the warranty agreement.</span></span> <span data-ttu-id="a8e1f-119">Затем можно отменить заказ на работу, если требуется.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-119">You can then cancel the work order, as you require.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]