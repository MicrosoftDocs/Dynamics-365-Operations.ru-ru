---
title: Создание производственных заказов
description: При создании производственного заказа инициируется запрос для начала производства номенклатуры. Производственный заказ содержит сведения о том, что будет производиться, в каком количестве, и плановую дату окончания. Он также содержит информацию о том, какие материалы будут потреблены и которому процессу следовать для произведения номенклатуры.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2957b387aac9e0218f88572fa605cde1a30c52e5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "324637"
---
# <a name="create-production-orders"></a><span data-ttu-id="e6489-105">Создание производственных заказов</span><span class="sxs-lookup"><span data-stu-id="e6489-105">Create production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6489-106">При создании производственного заказа инициируется запрос для начала производства номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="e6489-106">When a production order is created, a request is initiated to start producing an item.</span></span> <span data-ttu-id="e6489-107">Производственный заказ содержит сведения о том, что будет производиться, в каком количестве, и плановую дату окончания.</span><span class="sxs-lookup"><span data-stu-id="e6489-107">The production order contains information about what will be produced, the quantity to produce, and the planned finish date.</span></span> <span data-ttu-id="e6489-108">Он также содержит информацию о том, какие материалы будут потреблены и которому процессу следовать для произведения номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="e6489-108">It also contains information about which materials to consume and which process to follow to produce the item.</span></span>

<span data-ttu-id="e6489-109">Производственный заказ проходит через этапы жизненного цикла продукции.</span><span class="sxs-lookup"><span data-stu-id="e6489-109">A production order passes through stages of the production life cycle.</span></span> <span data-ttu-id="e6489-110">Когда заказ создается, ему назначается статус **Создано**.</span><span class="sxs-lookup"><span data-stu-id="e6489-110">When an order is created, it is assigned the status **Created**.</span></span> <span data-ttu-id="e6489-111">Когда заказ завершен, ему назначается статус **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="e6489-111">When an order is finished, it is assigned the status **Ended**.</span></span> <span data-ttu-id="e6489-112">Установка параметра на каждом этапе позволяет пользователю настроить каждый этап.</span><span class="sxs-lookup"><span data-stu-id="e6489-112">A parameter setting in each stage allows a user to configure each step.</span></span> <span data-ttu-id="e6489-113">Настройку можно сделать для отдельного пользователя или для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="e6489-113">The setting can be set up for a single user or for all users.</span></span>

<span data-ttu-id="e6489-114">Производственная спецификация и маршрут производства являются главными объектами производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="e6489-114">The production bill of material and the production route are the main entities of the production order.</span></span> <span data-ttu-id="e6489-115">Они копируются в производственный заказ на основе выбранной номенклатуры и количества, которое должно быть произведено.</span><span class="sxs-lookup"><span data-stu-id="e6489-115">They are copied to the production order based on the selected item and quantity that are going to be produced.</span></span> <span data-ttu-id="e6489-116">Прежде чем начать производственный заказ, можно редактировать производственную спецификацию и маршрут.</span><span class="sxs-lookup"><span data-stu-id="e6489-116">Before the production order is started, the production bill of material and route can be edited.</span></span>

<span data-ttu-id="e6489-117">Производственный заказ можно создать в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="e6489-117">A production order can be created in the following scenarios:</span></span>

-   <span data-ttu-id="e6489-118">Созданный сводным планированием на основе потребности в материале.</span><span class="sxs-lookup"><span data-stu-id="e6489-118">Created by master planning execution based on material demand.</span></span>
-   <span data-ttu-id="e6489-119">Созданный сразу из строки заказа на продажу или когда создается и оценивается производственный заказ более высокого уровня (фиксированное снабжение).</span><span class="sxs-lookup"><span data-stu-id="e6489-119">Created directly from a sales order line or when a higher-level production order is created and estimated (pegged supply).</span></span>
-   <span data-ttu-id="e6489-120">Созданный вручную.</span><span class="sxs-lookup"><span data-stu-id="e6489-120">Created manually.</span></span>




