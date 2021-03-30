---
title: Создание класса работ
description: В этой процедуре показано, как настроить класс работы.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49b110b93e6f0f886d180f9f2725245faad7afab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239046"
---
# <a name="create-a-work-class"></a><span data-ttu-id="05ce3-103">Создание класса работ</span><span class="sxs-lookup"><span data-stu-id="05ce3-103">Create a work class</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="05ce3-104">В этой процедуре показано, как настроить класс работы.</span><span class="sxs-lookup"><span data-stu-id="05ce3-104">This procedure shows you how to set up a work class.</span></span> <span data-ttu-id="05ce3-105">Классы работы используются для определения и/или ограничения типа строк заказа на работу, которые работник склада может обрабатывать на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="05ce3-105">Work classes are used to direct and/or limit the type of work order lines that a warehouse worker can process on a mobile device.</span></span> <span data-ttu-id="05ce3-106">Строки, которые может обрабатывать работник склада, определяются по классам работы, соответствующим пунктам меню мобильного устройства, доступ к которым имеет работник, и классу работы, указанному в строках работы.</span><span class="sxs-lookup"><span data-stu-id="05ce3-106">The lines that a worker can process are determined from the work classes on the mobile device menu items that the warehouse worker has access to and the work class that's specified on the work lines.</span></span> <span data-ttu-id="05ce3-107">Классы работы можно также использовать для проверки местонахождения размещения для строки заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="05ce3-107">Work classes can also be used to validate the put location for a work order line.</span></span> <span data-ttu-id="05ce3-108">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="05ce3-108">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="05ce3-109">Эта процедура предназначена для менеджера склада.</span><span class="sxs-lookup"><span data-stu-id="05ce3-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="05ce3-110">Перейдите в раздел "Управление складом" > "Настройка" > "Работа" > "Классы работы".</span><span class="sxs-lookup"><span data-stu-id="05ce3-110">Go to Warehouse management > Setup > Work > Work classes.</span></span>
2. <span data-ttu-id="05ce3-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="05ce3-111">Click New.</span></span>
3. <span data-ttu-id="05ce3-112">В поле "Код класса работы" введите значение.</span><span class="sxs-lookup"><span data-stu-id="05ce3-112">In the Work class ID field, type a value.</span></span>
4. <span data-ttu-id="05ce3-113">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="05ce3-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="05ce3-114">В поле "Тип заказа на выполнение работ" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="05ce3-114">In the Work order type field, select an option.</span></span>
6. <span data-ttu-id="05ce3-115">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="05ce3-115">Click New.</span></span>
7. <span data-ttu-id="05ce3-116">В поле "Тип местоположения" введите значение.</span><span class="sxs-lookup"><span data-stu-id="05ce3-116">In the Location type field, type a value.</span></span>
    * <span data-ttu-id="05ce3-117">Если выбран тип местонахождения, это устанавливает ограничение на то, где могут быть размещены номенклатуры после их комплектации.</span><span class="sxs-lookup"><span data-stu-id="05ce3-117">If you select a location type, this sets a restriction on where items can be put after they've been picked.</span></span> <span data-ttu-id="05ce3-118">Этот параметр используется, когда директива места хранения пытается разрешить местонахождение, или если работник склада вручную предоставляет местонахождение для пункта меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="05ce3-118">This setting is used when a location directive tries to resolve the location, or if a warehouse worker manually provides the location for the mobile device menu item.</span></span>  
8. <span data-ttu-id="05ce3-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="05ce3-119">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]