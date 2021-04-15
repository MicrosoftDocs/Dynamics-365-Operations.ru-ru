---
title: Необходимые условия для настройки каналов
description: В этом разделе представлен обзор необходимых условий настройки каналов в Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 33fcead6c0b08db17f24b638376a23b8b6024a5b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800527"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="d4bc4-103">Необходимые условия для настройки каналов</span><span class="sxs-lookup"><span data-stu-id="d4bc4-103">Channel setup prerequisites</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d4bc4-104">В этом разделе представлен обзор необходимых условий настройки каналов в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d4bc4-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d4bc4-105">Прежде чем можно будет создать канал Dynamics 365 Commerce, необходимо выполнить несколько предварительных условий.</span><span class="sxs-lookup"><span data-stu-id="d4bc4-105">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="d4bc4-106">Следующие списки необходимых условий упорядочены по типам каналов.</span><span class="sxs-lookup"><span data-stu-id="d4bc4-106">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="d4bc4-107">Документация по-прежнему записывается, и ссылки будут обновляться по мере публикации нового содержимого.</span><span class="sxs-lookup"><span data-stu-id="d4bc4-107">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="d4bc4-108">Инициализация</span><span class="sxs-lookup"><span data-stu-id="d4bc4-108">Initialization</span></span>

- [<span data-ttu-id="d4bc4-109">Инициализация начальных данных</span><span class="sxs-lookup"><span data-stu-id="d4bc4-109">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="d4bc4-110">Глобальные необходимые условия для всех типов каналов</span><span class="sxs-lookup"><span data-stu-id="d4bc4-110">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="d4bc4-111">Определение и настройка структуры юридического лица</span><span class="sxs-lookup"><span data-stu-id="d4bc4-111">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="d4bc4-112">Настройка своей организационной иерархии</span><span class="sxs-lookup"><span data-stu-id="d4bc4-112">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="d4bc4-113">Настройка склада</span><span class="sxs-lookup"><span data-stu-id="d4bc4-113">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="d4bc4-114">Настройка налога</span><span class="sxs-lookup"><span data-stu-id="d4bc4-114">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="d4bc4-115">Настройка профиля уведомлений по электронной почте</span><span class="sxs-lookup"><span data-stu-id="d4bc4-115">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="d4bc4-116">Настройка номерных серий</span><span class="sxs-lookup"><span data-stu-id="d4bc4-116">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="d4bc4-117">Настройка клиента по умолчанию и адресной книги</span><span class="sxs-lookup"><span data-stu-id="d4bc4-117">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="d4bc4-118">Необходимые условия для каналов розничной торговли</span><span class="sxs-lookup"><span data-stu-id="d4bc4-118">Retail channel prerequisites</span></span>

- [<span data-ttu-id="d4bc4-119">Инфокоды и группы инфокодов</span><span class="sxs-lookup"><span data-stu-id="d4bc4-119">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="d4bc4-120">Настройка профиля функциональности для розничной торговли</span><span class="sxs-lookup"><span data-stu-id="d4bc4-120">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="d4bc4-121">Настройка адресной книги сотрудников</span><span class="sxs-lookup"><span data-stu-id="d4bc4-121">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="d4bc4-122">Настройка макета экрана</span><span class="sxs-lookup"><span data-stu-id="d4bc4-122">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="d4bc4-123">Настройка станции оборудования</span><span class="sxs-lookup"><span data-stu-id="d4bc4-123">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="d4bc4-124">Необходимые условия для канала центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="d4bc4-124">Call Center channel prerequisites</span></span>

- <span data-ttu-id="d4bc4-125">Параметры центра обработки вызовов</span><span class="sxs-lookup"><span data-stu-id="d4bc4-125">Call center parameters</span></span>
- [<span data-ttu-id="d4bc4-126">Заказ центра обработки вызовов и способы оплаты возврата денежных средств</span><span class="sxs-lookup"><span data-stu-id="d4bc4-126">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="d4bc4-127">Режимы центра обработки вызовов для доставки и накладных расходов</span><span class="sxs-lookup"><span data-stu-id="d4bc4-127">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="d4bc4-128">Необходимые условия для каналов онлайн-торговли</span><span class="sxs-lookup"><span data-stu-id="d4bc4-128">Online channel prerequisites</span></span>

- [<span data-ttu-id="d4bc4-129">Создание профиля функциональности для онлайн-торговли</span><span class="sxs-lookup"><span data-stu-id="d4bc4-129">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="d4bc4-130">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d4bc4-130">Additional resources</span></span>

[<span data-ttu-id="d4bc4-131">Обзор каналов</span><span class="sxs-lookup"><span data-stu-id="d4bc4-131">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="d4bc4-132">Обзор организаций и организационных иерархий</span><span class="sxs-lookup"><span data-stu-id="d4bc4-132">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="d4bc4-133">Настройка организационных иерархий</span><span class="sxs-lookup"><span data-stu-id="d4bc4-133">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="d4bc4-134">Создание юридических лиц</span><span class="sxs-lookup"><span data-stu-id="d4bc4-134">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="d4bc4-135">Настройка канала розничной торговли</span><span class="sxs-lookup"><span data-stu-id="d4bc4-135">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="d4bc4-136">Настройка интернет-канала</span><span class="sxs-lookup"><span data-stu-id="d4bc4-136">Set up an online channel</span></span>](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
