---
title: Устранение неполадок входящих операций склада
description: В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с входящими операциями склада в Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 71f590ec01b757de298bd2692fdbdb0324843376
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970263"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="cd074-103">Устранение неполадок входящих операций склада</span><span class="sxs-lookup"><span data-stu-id="cd074-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd074-104">В этой теме описывается устранение распространенных проблем, которые могут встретиться при работе с входящими операциями склада в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cd074-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="cd074-105">Получено следующее сообщение об ошибке: "Создан заказ для контроля качества %1.</span><span class="sxs-lookup"><span data-stu-id="cd074-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="cd074-106">Не удалось найти профиль кластера. Проверьте конфигурацию."</span><span class="sxs-lookup"><span data-stu-id="cd074-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="cd074-107">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="cd074-107">Issue description</span></span>

<span data-ttu-id="cd074-108">Это сообщение об ошибке относится к процессу приемки, когда включено управление качеством (QMS).</span><span class="sxs-lookup"><span data-stu-id="cd074-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="cd074-109">В зависимости от конфигураций в вашей среде, для устранения проблемы могут помочь дополнительные сведения о проводке, которая создает это сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="cd074-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="cd074-110">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="cd074-110">Issue resolution</span></span>

<span data-ttu-id="cd074-111">Сначала проверьте настройку [комплектации кластера](set-up-cluster-picking.md) и убедитесь, что профили кластеров настроены правильно.</span><span class="sxs-lookup"><span data-stu-id="cd074-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="cd074-112">Нельзя использовать пункт меню мобильного устройства для комплектации кластера, если не настроены профили кластера.</span><span class="sxs-lookup"><span data-stu-id="cd074-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="cd074-113">В зависимости от среды, возможно, придется также просмотреть и другие связанные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="cd074-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="cd074-114">Использование смешанных грузомест не работает для любого метода обработки, за исключением кредита.</span><span class="sxs-lookup"><span data-stu-id="cd074-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="cd074-115">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="cd074-115">Issue description</span></span>

<span data-ttu-id="cd074-116">Если для поля **Действие** для кода метода обработки выбрано *Кредит* или *Отходы*, для обработки возвращенных номенклатур можно использовать только пункт меню [Получение грузоместа со смешанными номенклатурами](mixed-license-plate-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="cd074-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="cd074-117">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="cd074-117">Issue resolution</span></span>

<span data-ttu-id="cd074-118">Корпорация Майкрософт проверила эту проблему и определила, что она является ограничением функции.</span><span class="sxs-lookup"><span data-stu-id="cd074-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="cd074-119">В настоящее время только [коды методов обработки](../service-management/set-up-disposition-codes.md), у которых в поле **Действие** задано значение *Кредит* или *отходы*, поддерживаются для получения грузомест со смешанными номенклатурами.</span><span class="sxs-lookup"><span data-stu-id="cd074-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="cd074-120">При выполнении периодической задачи обновления поступлений продуктов подтверждаются неподтвержденные заказы на покупку.</span><span class="sxs-lookup"><span data-stu-id="cd074-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="cd074-121">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="cd074-121">Issue description</span></span>

<span data-ttu-id="cd074-122">После запуска периодической задачи *Обновление поступлений продуктов* система автоматически подтверждает неподтвержденные заказы на покупку, имеющие статус складской проводки *Зарегистрировано*.</span><span class="sxs-lookup"><span data-stu-id="cd074-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="cd074-123">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="cd074-123">Issue resolution</span></span>

<span data-ttu-id="cd074-124">Новая функция обработки входящей загрузки *Получение сверх количества загрузки* решает эту проблему.</span><span class="sxs-lookup"><span data-stu-id="cd074-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="cd074-125">Чтобы включить эту функцию, перейдите в раздел [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) и включите следующие функции (в порядке, в котором они перечислены):</span><span class="sxs-lookup"><span data-stu-id="cd074-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="cd074-126">Связать складские проводки по заказу на покупку с загрузкой</span><span class="sxs-lookup"><span data-stu-id="cd074-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="cd074-127">Получение сверх количества загрузки</span><span class="sxs-lookup"><span data-stu-id="cd074-127">Over receipt of load quantities</span></span>

<span data-ttu-id="cd074-128">Дополнительные сведения см. в разделе [Разноска зарегистрированных количеств товаров по заказам на покупку](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="cd074-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>
