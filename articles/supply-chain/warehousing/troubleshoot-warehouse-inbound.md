---
title: Устранение неполадок входящих операций склада
description: В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с входящими операциями склада в Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f0ea2ee208cdbb8f9fa6668bbcb6e15252a7c1b1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828234"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="26fd3-103">Устранение неполадок входящих операций склада</span><span class="sxs-lookup"><span data-stu-id="26fd3-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26fd3-104">В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с входящими операциями склада в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="26fd3-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="26fd3-105">Получено следующее сообщение об ошибке: "Создан заказ для контроля качества %1.</span><span class="sxs-lookup"><span data-stu-id="26fd3-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="26fd3-106">Не удалось найти профиль кластера. Проверьте конфигурацию."</span><span class="sxs-lookup"><span data-stu-id="26fd3-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="26fd3-107">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="26fd3-107">Issue description</span></span>

<span data-ttu-id="26fd3-108">Это сообщение об ошибке относится к процессу приемки, когда включено управление качеством (QMS).</span><span class="sxs-lookup"><span data-stu-id="26fd3-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="26fd3-109">В зависимости от конфигураций в вашей среде, для устранения проблемы могут помочь дополнительные сведения о проводке, которая создает это сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="26fd3-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="26fd3-110">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="26fd3-110">Issue resolution</span></span>

<span data-ttu-id="26fd3-111">Сначала проверьте настройку [комплектации кластера](set-up-cluster-picking.md) и убедитесь, что профили кластеров настроены правильно.</span><span class="sxs-lookup"><span data-stu-id="26fd3-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="26fd3-112">Нельзя использовать пункт меню мобильного устройства для комплектации кластера, если не настроены профили кластера.</span><span class="sxs-lookup"><span data-stu-id="26fd3-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="26fd3-113">В зависимости от среды, возможно, придется также просмотреть и другие связанные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="26fd3-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="26fd3-114">Использование смешанных грузомест не работает для любого метода обработки, за исключением кредита.</span><span class="sxs-lookup"><span data-stu-id="26fd3-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="26fd3-115">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="26fd3-115">Issue description</span></span>

<span data-ttu-id="26fd3-116">Если для поля **Действие** для кода метода обработки выбрано *Кредит* или *Отходы*, для обработки возвращенных номенклатур можно использовать только пункт меню [Получение грузоместа со смешанными номенклатурами](mixed-license-plate-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="26fd3-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="26fd3-117">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="26fd3-117">Issue resolution</span></span>

<span data-ttu-id="26fd3-118">Корпорация Майкрософт проверила эту проблему и определила, что она является ограничением функции.</span><span class="sxs-lookup"><span data-stu-id="26fd3-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="26fd3-119">В настоящее время только [коды методов обработки](../service-management/set-up-disposition-codes.md), у которых в поле **Действие** задано значение *Кредит* или *отходы*, поддерживаются для получения грузомест со смешанными номенклатурами.</span><span class="sxs-lookup"><span data-stu-id="26fd3-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="26fd3-120">При выполнении периодической задачи обновления поступлений продуктов подтверждаются неподтвержденные заказы на покупку.</span><span class="sxs-lookup"><span data-stu-id="26fd3-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="26fd3-121">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="26fd3-121">Issue description</span></span>

<span data-ttu-id="26fd3-122">После запуска периодической задачи *Обновление поступлений продуктов* система автоматически подтверждает неподтвержденные заказы на покупку, имеющие статус складской проводки *Зарегистрировано*.</span><span class="sxs-lookup"><span data-stu-id="26fd3-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="26fd3-123">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="26fd3-123">Issue resolution</span></span>

<span data-ttu-id="26fd3-124">Новая функция обработки входящей загрузки *Получение сверх количества загрузки* решает эту проблему.</span><span class="sxs-lookup"><span data-stu-id="26fd3-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="26fd3-125">Чтобы включить эту функцию, перейдите в раздел [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) и включите следующие функции (в порядке, в котором они перечислены):</span><span class="sxs-lookup"><span data-stu-id="26fd3-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="26fd3-126">Связать складские проводки по заказу на покупку с загрузкой</span><span class="sxs-lookup"><span data-stu-id="26fd3-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="26fd3-127">Получение сверх количества загрузки</span><span class="sxs-lookup"><span data-stu-id="26fd3-127">Over receipt of load quantities</span></span>

<span data-ttu-id="26fd3-128">Дополнительные сведения см. в разделе [Разноска зарегистрированных количеств товаров по заказам на покупку](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="26fd3-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a><span data-ttu-id="26fd3-129">При регистрации входящих заказов появляется следующее сообщение об ошибке: "Недопустимое количество".</span><span class="sxs-lookup"><span data-stu-id="26fd3-129">When I register inbound orders, I receive the following error message: "The quantity is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="26fd3-130">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="26fd3-130">Issue description</span></span>

<span data-ttu-id="26fd3-131">Если в поле **Политики группировки грузомест** выбрано значение *Определено пользователем* для пункта меню мобильного устройства, используемого для регистрации входящих заказов, будет выведено сообщение об ошибке ("Недопустимое количество"), и вы не сможете выполнить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="26fd3-131">If the **License plate grouping policy** field is set to *User defined* for a mobile device menu item that is used to register inbound orders, you receive an error message ("The quantity is not valid"), and you can't complete the registration.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="26fd3-132">Причина проблемы</span><span class="sxs-lookup"><span data-stu-id="26fd3-132">Issue cause</span></span>

<span data-ttu-id="26fd3-133">Когда вариант *Определено пользователем* используется в качестве политики группировки грузомест, система разделяет входящие запасы на отдельные грузоместа, как указано в группе последовательности единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="26fd3-133">When *User defined* is used as a license plate grouping policy, the system splits the incoming inventory into separate license plates, as indicated by the unit sequence group.</span></span> <span data-ttu-id="26fd3-134">Если номера партий или серийные номера используются для отслеживания принимаемой номенклатуры, количества каждой партии или серийных номеров должны быть указаны для каждого зарегистрированного грузоместа.</span><span class="sxs-lookup"><span data-stu-id="26fd3-134">If batch or serial numbers are used to track the item that is being received, the quantities of each batch or serial must be specified per license plate that is registered.</span></span> <span data-ttu-id="26fd3-135">Если количество, указанное для грузоместа, превышает количество, которое должно быть получено для текущих аналитик, выводится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="26fd3-135">If the quantity that is specified for a license plate exceeds the quantity that must still be received for the current dimensions, you receive the error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="26fd3-136">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="26fd3-136">Issue resolution</span></span>

<span data-ttu-id="26fd3-137">При регистрации номенклатуры с помощью команды меню мобильного устройства, в которой для поля **Политика группирования грузомест** установлено значение *Определено пользователем*, система может потребовать подтвердить или ввести номера грузомест, номера партий или серийные номера.</span><span class="sxs-lookup"><span data-stu-id="26fd3-137">When you register an item by using a mobile device menu item where the **License plate grouping policy** field is set to *User defined*, the system might require that you confirm or enter license plate numbers, batch numbers, or serial numbers.</span></span>

<span data-ttu-id="26fd3-138">На странице подтверждение грузоместа в системе отображается количество, выделяемое для текущего грузоместа.</span><span class="sxs-lookup"><span data-stu-id="26fd3-138">On the license plate confirmation page, the system will show the quantity that is allocated for the current license plate.</span></span> <span data-ttu-id="26fd3-139">На страницах подтверждения партии или серийных номеров система отображает количество, которое должно быть еще получено на текущем грузоместе.</span><span class="sxs-lookup"><span data-stu-id="26fd3-139">On the batch or serial confirmation pages, the system will show the quantity that must still be received on the current license plate.</span></span> <span data-ttu-id="26fd3-140">Она также включает в себя поле, в котором можно ввести количество для регистрации для этой комбинации грузоместа и номера партии или серийного номера.</span><span class="sxs-lookup"><span data-stu-id="26fd3-140">It will also include a field where you can enter the quantity to register for that combination of license plate and batch or serial number.</span></span> <span data-ttu-id="26fd3-141">В этом случае убедитесь, что количество, зарегистрированное для данного грузоместа, не превышает количество, которое должно быть еще получено.</span><span class="sxs-lookup"><span data-stu-id="26fd3-141">In this case, make sure that the quantity that is being registered for the license plate doesn't exceed the quantity that must still be received.</span></span>

<span data-ttu-id="26fd3-142">Или же, если при регистрации входящего заказа создается слишком много грузомест, значение поля **Политика группировки грузомест** может быть изменено на *Группирование грузомест*, новая группа последовательности единиц измерения может быть назначена номенклатуре или параметр **Группировка грузомест** для группы последовательности единиц измерения может быть деактивирован.</span><span class="sxs-lookup"><span data-stu-id="26fd3-142">Alternatively, if too many license plates are being generated on inbound order registration, the value of the **License plate grouping policy** field can be changed to *License plate grouping*, a new unit sequence group can be assigned to the item, or the **License plate grouping** option for the unit sequence group can be inactivated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
