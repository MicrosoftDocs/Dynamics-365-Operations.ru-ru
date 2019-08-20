---
title: Типы запросов на обслуживание
description: В этом разделе описан порядок настройки типов запросов на обслуживание в «Управлении активами».
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19d529df6c8aab036de59502b4f14101e1a07707
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790533"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="5be33-103">Типы запросов на обслуживание</span><span class="sxs-lookup"><span data-stu-id="5be33-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="5be33-104">Типы запросов на обслуживание используются для классификации запросов на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="5be33-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="5be33-105">Например, могут быть типы запросов на обслуживание, связанные с профилактическим обслуживанием и корректирующим обслуживанием.</span><span class="sxs-lookup"><span data-stu-id="5be33-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="5be33-106">Или у вас может быть специальный тип запроса на обслуживание, который используется для управления ремонтом активов (ремонт в хранилище).</span><span class="sxs-lookup"><span data-stu-id="5be33-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="5be33-107">Тип запроса на обслуживание определяет связь с группой состояния жизненного цикла запроса на обслуживание (модель жизненного цикла обслуживания).</span><span class="sxs-lookup"><span data-stu-id="5be33-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="5be33-108">Модели жизненного цикла запроса на обслуживание определяют состояния жизненного цикла, которые могут быть установлены для запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="5be33-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="5be33-109">(Примеры состояния жизненного цикла запроса на обслуживание включают **Создано**, **Активно** и **Завершено**).</span><span class="sxs-lookup"><span data-stu-id="5be33-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="5be33-110">Выберите **Управление активами** \> **Настройка** \> **Запросы на обслуживание** \> **Типы запросов на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="5be33-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="5be33-111">Выберите **Создать** для создания типа запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="5be33-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="5be33-112">В поле **Тип запроса обслуживания** введите идентификатор для типа запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="5be33-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="5be33-113">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="5be33-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="5be33-114">На экспресс-вкладке **Общее** в поле **Модель жизненного цикла запроса на обслуживание** выберите модель жизненного цикла запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="5be33-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="5be33-115">В поле **Тип заказа на выполнение работ** выберите тип заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="5be33-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="5be33-116">При преобразовании запроса на обслуживание в заказ на работу заказ автоматически получает тип заказа на работу, связанный с типом запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="5be33-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="5be33-117">На следующем рисунке показан пример страницы **Типы запроса на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="5be33-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![Рисунок 1](media/07-setup-for-requests.png)