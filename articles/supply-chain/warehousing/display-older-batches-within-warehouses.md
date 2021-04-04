---
title: Настройка отображения более старых партий на складе на мобильном устройстве
description: В этой теме описывается, как настроить мобильное устройство для отображения списка местонахождений с партиями старше, чем текущее местонахождение строки работы.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f5317f15a7c7aad53971812e4b22f9e4be79d5c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251848"
---
# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a><span data-ttu-id="a4821-103">Настройка отображения более старых партий на складе на мобильном устройстве</span><span class="sxs-lookup"><span data-stu-id="a4821-103">Configure Display older batches within warehouse on a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4821-104">Конфигурация **Показать более старые партии на складе** позволяет отобразить список местонахождений с партиями старше, чем текущее местонахождение строки работы.</span><span class="sxs-lookup"><span data-stu-id="a4821-104">The **Display older batches within warehouse** configuration lets you display a list of locations with batches older than the current location of the work line.</span></span> <span data-ttu-id="a4821-105">Список отображаемых местонахождений включает сведения о более старых партиях в местонахождении с указанием даты окончания срока действия и физических запасов каждой партии.</span><span class="sxs-lookup"><span data-stu-id="a4821-105">The list of locations that are displayed includes information about the older batches in the location with the expiration date and the physical inventory of each batch.</span></span> <span data-ttu-id="a4821-106">Можно выбрать комплектацию из нового местонахождения или продолжить комплектацию из текущего местонахождения.</span><span class="sxs-lookup"><span data-stu-id="a4821-106">You can choose to pick from a new location or to continue picking from the current location.</span></span> 
- <span data-ttu-id="a4821-107">Комплектация из нового местонахождения. Если выбрать новое местонахождение для комплектации, текущая строка работы будет обновлена для использования нового местонахождения, и работа будет продолжена в обычном режиме с использованием нового местонахождения.</span><span class="sxs-lookup"><span data-stu-id="a4821-107">Pick from a new location - If you select a new location to pick from, the  current work line will be updated to use the new location and work will continue as usual with the new location.</span></span> <span data-ttu-id="a4821-108">Чтобы новое местонахождение было действительным, оно должно иметь достаточное доступное количество для всей строки работы.</span><span class="sxs-lookup"><span data-stu-id="a4821-108">For the new location to be valid, it must have enough available quantity for the whole work line.</span></span> <span data-ttu-id="a4821-109">Если требуемое количество отсутствует, строка работы не будет обновлена, и отобразится список.</span><span class="sxs-lookup"><span data-stu-id="a4821-109">If the required quantity is not available, the work line will not be updated, and the list will display.</span></span> 
- <span data-ttu-id="a4821-110">Продолжить комплектацию из текущего местонахождения. Если вы продолжаете использовать текущее местонахождение строки работы, количества для строки работы будут продолжать комплектоваться из первоначального местонахождения.</span><span class="sxs-lookup"><span data-stu-id="a4821-110">Continue picking from the current location - If you continue with the current work line location, the quantities for the work line will continue to be picked from the original location.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="a4821-111">Где это применяется</span><span class="sxs-lookup"><span data-stu-id="a4821-111">Where it applies</span></span>
<span data-ttu-id="a4821-112">Отображение более старых партий на складе настраивается в меню мобильного устройства и влияет на комплектацию следующих партий номенклатур.</span><span class="sxs-lookup"><span data-stu-id="a4821-112">Display older batches within warehouse is configured on mobile device menu items and affects the pick for batch below items.</span></span>

## <a name="set-up-display-older-batches-within-warehouse"></a><span data-ttu-id="a4821-113">Настройка отображения более старых партий на складе</span><span class="sxs-lookup"><span data-stu-id="a4821-113">Set up Display older batches within warehouse</span></span>
<span data-ttu-id="a4821-114">Конфигурация **Показать более старые партии на складе** доступна в пунктах меню мобильного устройства, если для параметра **Выбрать самую старую партию** задать значение **Предупредить**.</span><span class="sxs-lookup"><span data-stu-id="a4821-114">The **Display older batches within warehouse** configuration is available on mobile device menu items when the **Pick oldest batch** option is set to **Warn**.</span></span>

- <span data-ttu-id="a4821-115">В разделе **Управление складом** > **Настройка** > **Мобильное устройство** > **Пункты меню мобильного устройства** задайте для параметра **Использовать существующую работу** значение **Да** для пункта меню и выберите **Предупредить** в поле **Выбрать самую старую партию**.</span><span class="sxs-lookup"><span data-stu-id="a4821-115">Under **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**, set **Use existing work** to **Yes** for the menu item, and select **Warn** in the **Pick oldest batch** field.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]