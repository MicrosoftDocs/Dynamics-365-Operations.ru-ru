---
title: Обзор жизненного цикла производственного заказа
description: При создании производственного заказа инициируется запрос для начала производства номенклатуры. Производственный заказ содержит сведения о том, что будет производиться, в каком количестве, и плановую дату окончания. Он также содержит информацию о том, какие материалы будут потреблены и которому процессу следовать для произведения номенклатуры.
author: johanhoffmann
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28ef1da29b38354d7ccaad56fb036f21d8c9ff15
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011180"
---
# <a name="production-order-lifecycle-overview"></a><span data-ttu-id="0adde-105">Обзор жизненного цикла производственного заказа</span><span class="sxs-lookup"><span data-stu-id="0adde-105">Production order lifecycle overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0adde-106">При создании производственного заказа инициируется запрос для начала производства номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="0adde-106">When a production order is created, a request is initiated to start producing an item.</span></span> <span data-ttu-id="0adde-107">Производственный заказ содержит сведения о том, что будет производиться, в каком количестве, и плановую дату окончания.</span><span class="sxs-lookup"><span data-stu-id="0adde-107">The production order contains information about what will be produced, the quantity to produce, and the planned finish date.</span></span> <span data-ttu-id="0adde-108">Он также содержит информацию о том, какие материалы будут потреблены и которому процессу следовать для произведения номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="0adde-108">It also contains information about which materials to consume and which process to follow to produce the item.</span></span>

<span data-ttu-id="0adde-109">Производственный заказ проходит через этапы жизненного цикла продукции.</span><span class="sxs-lookup"><span data-stu-id="0adde-109">A production order passes through stages of the production life cycle.</span></span> <span data-ttu-id="0adde-110">Когда заказ создается, ему назначается статус **Создано**.</span><span class="sxs-lookup"><span data-stu-id="0adde-110">When an order is created, it is assigned the status **Created**.</span></span> <span data-ttu-id="0adde-111">Когда заказ завершен, ему назначается статус **Завершено**.</span><span class="sxs-lookup"><span data-stu-id="0adde-111">When an order is finished, it is assigned the status **Ended**.</span></span> <span data-ttu-id="0adde-112">Установка параметра на каждом этапе позволяет пользователю настроить каждый этап.</span><span class="sxs-lookup"><span data-stu-id="0adde-112">A parameter setting in each stage allows a user to configure each step.</span></span> <span data-ttu-id="0adde-113">Настройку можно сделать для отдельного пользователя или для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="0adde-113">The setting can be set up for a single user or for all users.</span></span>

<span data-ttu-id="0adde-114">Производственная спецификация и маршрут производства являются главными объектами производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="0adde-114">The production bill of material and the production route are the main entities of the production order.</span></span> <span data-ttu-id="0adde-115">Они копируются в производственный заказ на основе выбранной номенклатуры и количества, которое должно быть произведено.</span><span class="sxs-lookup"><span data-stu-id="0adde-115">They are copied to the production order based on the selected item and quantity that are going to be produced.</span></span> <span data-ttu-id="0adde-116">Прежде чем начать производственный заказ, можно редактировать производственную спецификацию и маршрут.</span><span class="sxs-lookup"><span data-stu-id="0adde-116">Before the production order is started, the production bill of material and route can be edited.</span></span>

<span data-ttu-id="0adde-117">Производственный заказ можно создать в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="0adde-117">A production order can be created in the following scenarios:</span></span>

-   <span data-ttu-id="0adde-118">Созданный сводным планированием на основе потребности в материале.</span><span class="sxs-lookup"><span data-stu-id="0adde-118">Created by master planning execution based on material demand.</span></span>
-   <span data-ttu-id="0adde-119">Созданный сразу из строки заказа на продажу или когда создается и оценивается производственный заказ более высокого уровня (фиксированное снабжение).</span><span class="sxs-lookup"><span data-stu-id="0adde-119">Created directly from a sales order line or when a higher-level production order is created and estimated (pegged supply).</span></span>
-   <span data-ttu-id="0adde-120">Созданный вручную.</span><span class="sxs-lookup"><span data-stu-id="0adde-120">Created manually.</span></span>




