---
title: Настройка элемента меню мобильного устройства для предоставления обзора строк комплектации
description: В этой теме объясняется, как определить, когда список всех рабочих строк будет отображаться для сотрудников склада, обрабатывающих работу склада на мобильном устройстве. Эта возможность может быть полезной для работников складов, которым часто требуется обзор строк комплектации в заказе на работу, чтобы они могли оптимизировать последовательность комплектации.
author: MarkusFogelberg
manager: tfehr
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 22e724b60ec5cc8bf39a520022f43784d3a328eb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232919"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a><span data-ttu-id="e41f2-104">Настройка элемента меню мобильного устройства для предоставления обзора строк комплектации</span><span class="sxs-lookup"><span data-stu-id="e41f2-104">Set up a mobile device menu item to provide a pick line overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e41f2-105">В этой теме описывается, как настроить параметры, которые относятся к обзору строки комплектации для элементов меню мобильного устройства, которые используются для обработки работы по комплектации.</span><span class="sxs-lookup"><span data-stu-id="e41f2-105">This topic explains how to configure options that are related to the pick line overview for mobile device menu items that are used to process picking work.</span></span> <span data-ttu-id="e41f2-106">Обзор строки комплектации позволяет сотрудникам склада просматривать и выбирать из списка всех строки работ, которые связаны с их текущей задачей.</span><span class="sxs-lookup"><span data-stu-id="e41f2-106">The pick line overview lets warehouse workers view and select from a list of all the work lines that are related to their current task.</span></span> <span data-ttu-id="e41f2-107">Эта возможность может помочь работникам оптимизировать свою последовательность комплектации.</span><span class="sxs-lookup"><span data-stu-id="e41f2-107">This capability can help workers optimize their picking sequence.</span></span> <span data-ttu-id="e41f2-108">Функция предоставляет параметры, которые заменяют стандартную кнопку **Пропустить**, которая позволяет работникам циклически проходить по одной строке за раз в фиксированном порядке.</span><span class="sxs-lookup"><span data-stu-id="e41f2-108">The feature provides options that replace the standard **Skip** button that lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="e41f2-109">(Однако возможность использования этой кнопки все еще доступна.)</span><span class="sxs-lookup"><span data-stu-id="e41f2-109">(However, the option to use that button is still available.)</span></span>

<span data-ttu-id="e41f2-110">Администраторы могут настраивать каждый пункт меню по отдельности, чтобы управлять тем, как в приложении склада отображается обзор строк комплектации.</span><span class="sxs-lookup"><span data-stu-id="e41f2-110">Admins can configure each menu item individually to control how, when, and where the warehouse app presents the pick line overview.</span></span>

## <a name="turn-on-the-work-pick-line-overview-feature"></a><span data-ttu-id="e41f2-111">Включение функции обзора строк работы по комплектации</span><span class="sxs-lookup"><span data-stu-id="e41f2-111">Turn on the Work pick line overview feature</span></span>

<span data-ttu-id="e41f2-112">Прежде чем использовать эту функцию, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="e41f2-112">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="e41f2-113">Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="e41f2-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="e41f2-114">В рабочей области **Управление функциями** эта функция перечисляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="e41f2-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e41f2-115">**Модуль:** _Управление складом_</span><span class="sxs-lookup"><span data-stu-id="e41f2-115">**Module:** _Warehouse management_</span></span>
- <span data-ttu-id="e41f2-116">**Имя функции:** _Обзор строк работы по комплектации_</span><span class="sxs-lookup"><span data-stu-id="e41f2-116">**Feature name:** _Work pick line overview_</span></span>

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a><span data-ttu-id="e41f2-117">Настройка пунктов меню для отображения списка всех строк работы</span><span class="sxs-lookup"><span data-stu-id="e41f2-117">Configure menu items to show a list of all work lines</span></span>

<span data-ttu-id="e41f2-118">Чтобы настроить элемент меню мобильного устройства для предоставления обзора строк комплектации выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="e41f2-118">To set up a mobile device menu item to provide a pick line overview, follow these steps.</span></span>

1. <span data-ttu-id="e41f2-119">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="e41f2-119">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="e41f2-120">Выберите или создайте пункт меню, связанный с работой по комплектации, и установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e41f2-120">Select or create a menu item that is related to picking work, and set the following values:</span></span>

    - <span data-ttu-id="e41f2-121">**Режим:** *Работа*</span><span class="sxs-lookup"><span data-stu-id="e41f2-121">**Mode:** *Work*</span></span>
    - <span data-ttu-id="e41f2-122">**Использовать существующую работу:** *Да*</span><span class="sxs-lookup"><span data-stu-id="e41f2-122">**Use existing work:** *Yes*</span></span>
    - <span data-ttu-id="e41f2-123">**Кем управляется:** *Управляется пользователем* или *Управляется системой*</span><span class="sxs-lookup"><span data-stu-id="e41f2-123">**Directed by:** *User directed* or *System directed*</span></span>

    <span data-ttu-id="e41f2-124">Дополнительные сведения о порядке создания пунктов меню и использовании различных настроек, доступных на странице **Пункты меню мобильного устройства**, см. в разделе [Настройка мобильных устройств для работы склада](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="e41f2-124">For more information about how to create menu items and use the various settings that are available on the **Mobile device menu items** page, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

1. <span data-ttu-id="e41f2-125">На вкладке **Общие** настройте функцию, установив для поля **Показывать список строк работы** одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="e41f2-125">On the **General** FastTab, configure the feature by setting the **Show work line list** field to one of the following values:</span></span>

    - <span data-ttu-id="e41f2-126">**Показывать только по запросу** — работники могут выбрать просмотр списка строк комплектации, нажав кнопку **Пропустить до** в приложении склада.</span><span class="sxs-lookup"><span data-stu-id="e41f2-126">**Show only upon request** – Workers can choose to view the pick line list by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="e41f2-127">**Показывать в начале каждой комплектации** — работники видят список каждый раз при запуске или завершении строки комплектации.</span><span class="sxs-lookup"><span data-stu-id="e41f2-127">**Show at the start of every pick** – Workers see the list every time that they start or finish a pick line.</span></span> <span data-ttu-id="e41f2-128">Они также могут просмотреть этот список снова, нажав кнопку **Пропустить до** в приложении склада.</span><span class="sxs-lookup"><span data-stu-id="e41f2-128">They can also view the list again by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="e41f2-129">**Показывать только в начале первой комплектации** — работники видят список каждый раз, когда начинают новую комплектации, но не после каждой строки.</span><span class="sxs-lookup"><span data-stu-id="e41f2-129">**Show at the start of the first pick only** – Workers see the list every time that they start new picking work, but not after each line.</span></span> <span data-ttu-id="e41f2-130">Они также могут просмотреть этот список снова, нажав кнопку **Пропустить до** в приложении склада.</span><span class="sxs-lookup"><span data-stu-id="e41f2-130">They can also view the list again by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="e41f2-131">**Никогда не показывать** — стандартная кнопка **Пропустить** появляется в приложении склада, и отображение списка строк работы отключено.</span><span class="sxs-lookup"><span data-stu-id="e41f2-131">**Never show** – The standard **Skip** button appears in the warehouse app, and display of the work line list is turned off.</span></span> <span data-ttu-id="e41f2-132">С помощью кнопки **Пропустить** работники могут циклически переходить между строками по одной за раз в фиксированном порядке.</span><span class="sxs-lookup"><span data-stu-id="e41f2-132">The **Skip** button lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="e41f2-133">Они также могут циклически проходить через список столько раз, сколько необходимо, пока не будут обработаны все строки.</span><span class="sxs-lookup"><span data-stu-id="e41f2-133">They can also cycle through the list as many times as they require, until all lines have been processed.</span></span>

1. <span data-ttu-id="e41f2-134">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="e41f2-134">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="e41f2-135">Если в поле **Показывать список строк работы** выбрано любое значение, за исключением *Никогда не показывать*, кнопка **Список полей** в области действий становится доступной.</span><span class="sxs-lookup"><span data-stu-id="e41f2-135">If you set the **Show work line list** field to any value except *Never show*, the **Field list** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="e41f2-136">На панели операций выберите **Список полей**.</span><span class="sxs-lookup"><span data-stu-id="e41f2-136">On the Action Pane, select **Field list**.</span></span>
1. <span data-ttu-id="e41f2-137">На странице **Список полей** настройте информацию, которую приложение склада показывает для каждой строки в списке.</span><span class="sxs-lookup"><span data-stu-id="e41f2-137">On the **Field list** page, configure the information that the warehouse app shows for each line in the list.</span></span>

    - <span data-ttu-id="e41f2-138">Поле **Основной элемент управления** всегда имеет значение *LineNum*.</span><span class="sxs-lookup"><span data-stu-id="e41f2-138">The **Primary control** field is always set to *LineNum*.</span></span> <span data-ttu-id="e41f2-139">Таким образом, каждая строка списка начинается с номера строки.</span><span class="sxs-lookup"><span data-stu-id="e41f2-139">Therefore, each row in the list begins with a line number.</span></span>
    - <span data-ttu-id="e41f2-140">Используйте оставшиеся поля **Отображаемое поле** для добавления до семи дополнительных отображаемых полей, как это требуется.</span><span class="sxs-lookup"><span data-stu-id="e41f2-140">Use the remaining **Display field** fields to add up to seven additional display fields, as you require.</span></span> <span data-ttu-id="e41f2-141">В каждом поле **Отображаемое поле** выберите имя поля строки работы.</span><span class="sxs-lookup"><span data-stu-id="e41f2-141">In each **Display field** field, select the name of a work line field.</span></span> <span data-ttu-id="e41f2-142">Затем каждая строка отобразит значение для этого поля.</span><span class="sxs-lookup"><span data-stu-id="e41f2-142">Each line will then show a value for that field.</span></span> <span data-ttu-id="e41f2-143">Значения будут показаны в том порядке, в котором они выбраны здесь.</span><span class="sxs-lookup"><span data-stu-id="e41f2-143">The values will be shown in the order that you select here.</span></span> <span data-ttu-id="e41f2-144">Если не требуются все семь значений, можно оставить некоторые из полей **Отображаемое поле** пустыми.</span><span class="sxs-lookup"><span data-stu-id="e41f2-144">You can leave some of the **Display field** fields blank if you don't require all seven values.</span></span>

1. <span data-ttu-id="e41f2-145">На панели действий выберите **Сохранить**, затем закройте страницу **Список полей**.</span><span class="sxs-lookup"><span data-stu-id="e41f2-145">On the Action Pane, select **Save**, and then close the **Field list** page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]