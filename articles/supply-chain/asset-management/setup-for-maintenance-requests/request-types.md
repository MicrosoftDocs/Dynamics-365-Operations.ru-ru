---
title: Типы запросов на обслуживание
description: В этом разделе описан порядок настройки типов запросов на обслуживание в «Управлении активами».
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e4f622cda62cad13a8146cbc26bc2e5f1a45222
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261197"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="4730c-103">Типы запросов на обслуживание</span><span class="sxs-lookup"><span data-stu-id="4730c-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4730c-104">Типы запросов на обслуживание используются для классификации запросов на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="4730c-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="4730c-105">Например, могут быть типы запросов на обслуживание, связанные с профилактическим обслуживанием и корректирующим обслуживанием.</span><span class="sxs-lookup"><span data-stu-id="4730c-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="4730c-106">Или у вас может быть специальный тип запроса на обслуживание, который используется для управления ремонтом активов (ремонт в хранилище).</span><span class="sxs-lookup"><span data-stu-id="4730c-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="4730c-107">Тип запроса на обслуживание определяет связь с группой состояния жизненного цикла запроса на обслуживание (модель жизненного цикла обслуживания).</span><span class="sxs-lookup"><span data-stu-id="4730c-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="4730c-108">Модели жизненного цикла запроса на обслуживание определяют состояния жизненного цикла, которые могут быть установлены для запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="4730c-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="4730c-109">(Примеры состояния жизненного цикла запроса на обслуживание включают **Создано**, **Активно** и **Завершено**).</span><span class="sxs-lookup"><span data-stu-id="4730c-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="4730c-110">Выберите **Управление активами** \> **Настройка** \> **Запросы на обслуживание** \> **Типы запросов на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="4730c-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="4730c-111">Выберите **Создать** для создания типа запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="4730c-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="4730c-112">В поле **Тип запроса обслуживания** введите идентификатор для типа запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="4730c-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="4730c-113">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="4730c-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="4730c-114">На экспресс-вкладке **Общее** в поле **Модель жизненного цикла запроса на обслуживание** выберите модель жизненного цикла запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="4730c-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="4730c-115">В поле **Тип заказа на выполнение работ** выберите тип заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="4730c-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="4730c-116">При преобразовании запроса на обслуживание в заказ на работу заказ автоматически получает тип заказа на работу, связанный с типом запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="4730c-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="4730c-117">На следующем рисунке показан пример страницы **Типы запроса на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="4730c-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![Страница типов запросов на обслуживание](media/07-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]