---
title: Мониторинг и управление аналитикой Интернета вещей
description: В этом разделе объясняется, как отслеживать и управлять аналитикой Интернета вещей.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 05aee9865dc90c97e026d5c05fa2032fc0625f7a
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597416"
---
# <a name="monitor-and-manage-iot-intelligence"></a><span data-ttu-id="b61b7-103">Мониторинг и управление аналитикой Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="b61b7-103">Monitor and manage IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b61b7-104">В этом разделе объясняется, как отслеживать и управлять аналитикой Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="b61b7-104">This topic explains how to monitor and manage IoT Intelligence.</span></span>

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a><span data-ttu-id="b61b7-105">Мониторинг сценариев в Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b61b7-105">Monitor scenarios in Microsoft Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="b61b7-106">Можно отслеживать обработку аналитики Интернета вещей в нескольких местах:</span><span class="sxs-lookup"><span data-stu-id="b61b7-106">You can monitor IoT Intelligence processing from several places:</span></span>

+ <span data-ttu-id="b61b7-107">**Модули \> Управление производством \> запросы и отчеты \> аналитика Интернета вещей \> Уведомления** — Просмотр списка необработанных уведомлений.</span><span class="sxs-lookup"><span data-stu-id="b61b7-107">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Notifications** – View the list of unresolved notifications.</span></span>
+ <span data-ttu-id="b61b7-108">**Модули \> Управление производством \> запросы и отчеты \> аналитика Интернета вещей \> Закрытые уведомления** — Просмотр списка уведомлений, которые были разрешены или отклонены.</span><span class="sxs-lookup"><span data-stu-id="b61b7-108">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Closed notifications** – View the list of notifications that have been resolved or dismissed.</span></span>
+ <span data-ttu-id="b61b7-109">**Модули \> Управление производством \> запросы и отчеты \> аналитика Интернета вещей \> ключи метрики** — Просмотр ключей метрик для диаграмм временных рядов **статуса ресурсов**.</span><span class="sxs-lookup"><span data-stu-id="b61b7-109">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys** – View the metric keys for the **Resource Status** times series charts.</span></span>
+ <span data-ttu-id="b61b7-110">**Модули \> Управление производством \> Управление производством \> Статус ресурса** — Отслеживание специфических метрик с помощью диалогового окна **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="b61b7-110">**Modules \> Production control \> Manufacturing execution \> Resource status** – Track specific metrics by using the **Configure** dialog box.</span></span> <span data-ttu-id="b61b7-111">Если сценарий определяет исключение, в уведомлении отображаются сведения об исключении.</span><span class="sxs-lookup"><span data-stu-id="b61b7-111">If a scenario detects an exception, a notification shows the details of the exception.</span></span>
+ <span data-ttu-id="b61b7-112">**Рабочие области \> Управление производственным участком \> Уведомления** — Просмотрите список необработанных уведомлений.</span><span class="sxs-lookup"><span data-stu-id="b61b7-112">**Workspaces \> Production floor management \> Notifications** – View the list of unresolved notifications.</span></span>

## <a name="modify-a-running-iot-intelligence-scenario"></a><span data-ttu-id="b61b7-113">Изменение запущенного сценария аналитики Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="b61b7-113">Modify a running IoT Intelligence scenario</span></span>

<span data-ttu-id="b61b7-114">При запуске сценария можно выполнить следующие изменения:</span><span class="sxs-lookup"><span data-stu-id="b61b7-114">When a scenario is running, you can make these changes:</span></span>

+ <span data-ttu-id="b61b7-115">Добавление новых определений схемы датчиков.</span><span class="sxs-lookup"><span data-stu-id="b61b7-115">Add new sensor schema definitions.</span></span>
+ <span data-ttu-id="b61b7-116">Выберите новые значения данных сигнала.</span><span class="sxs-lookup"><span data-stu-id="b61b7-116">Select new signal data values.</span></span>
+ <span data-ttu-id="b61b7-117">Отмена выбора существующих значений данных сигнала.</span><span class="sxs-lookup"><span data-stu-id="b61b7-117">Cancel the selection of existing signal data values.</span></span>
+ <span data-ttu-id="b61b7-118">Добавление и сопоставление новых значений данных сигнала.</span><span class="sxs-lookup"><span data-stu-id="b61b7-118">Add and map new signal data values.</span></span>
+ <span data-ttu-id="b61b7-119">Обновление пороговых значений.</span><span class="sxs-lookup"><span data-stu-id="b61b7-119">Update threshold values.</span></span>

<span data-ttu-id="b61b7-120">При запуске сценария запрещены следующие изменения:</span><span class="sxs-lookup"><span data-stu-id="b61b7-120">When a scenario is running, these changes are prohibited:</span></span>

+ <span data-ttu-id="b61b7-121">Удаление или изменение определений схемы, которые в настоящее время используются включенным сценарием.</span><span class="sxs-lookup"><span data-stu-id="b61b7-121">Delete or modify any schema definitions that are currently consumed by an enabled scenario.</span></span>
+ <span data-ttu-id="b61b7-122">Изменение выбранных путей к схемам для включенного сценария.</span><span class="sxs-lookup"><span data-stu-id="b61b7-122">Change the enabled scenario's selected schema paths.</span></span>

## <a name="simulation-options"></a><span data-ttu-id="b61b7-123">Параметры моделирования</span><span class="sxs-lookup"><span data-stu-id="b61b7-123">Simulation options</span></span>

<span data-ttu-id="b61b7-124">Можно смоделировать сигналы фабричного оборудования.</span><span class="sxs-lookup"><span data-stu-id="b61b7-124">You can simulate factory machine signals.</span></span> <span data-ttu-id="b61b7-125">Дополнительные сведения см. в этих разделах:</span><span class="sxs-lookup"><span data-stu-id="b61b7-125">For more information, see these topics:</span></span>

+ [<span data-ttu-id="b61b7-126">Подключение DevKit AZ3166 Интернета вещей к узлу Интернета вещей Azure</span><span class="sxs-lookup"><span data-stu-id="b61b7-126">Connect IoT DevKit AZ3166 to Azure IoT Hub</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [<span data-ttu-id="b61b7-127">Подключите интерактивный модулятор Raspberry Pi к узлу Интернета вещей Azure (Node.js)</span><span class="sxs-lookup"><span data-stu-id="b61b7-127">Connect Raspberry Pi online simulator to Azure IoT Hub (Node.js)</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [<span data-ttu-id="b61b7-128">Обзор ускорителя решений моделирования устройств</span><span class="sxs-lookup"><span data-stu-id="b61b7-128">Device Simulation solution accelerator overview</span></span>](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)