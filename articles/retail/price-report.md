---
title: Отчеты по розничным ценам
description: В этом разделе представлен обзор функции отчета по ценам, который можно использовать для просмотра предстоящих изменений цены на продукты, включенные в ассортимент.
author: shajain
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 6db6d1c6b6eb1d69b40fe75d97eeb71564986707
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "353065"
---
# <a name="retail-price-reports"></a><span data-ttu-id="e2d96-103">Отчеты по розничным ценам</span><span class="sxs-lookup"><span data-stu-id="e2d96-103">Retail price reports</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]


<span data-ttu-id="e2d96-104">Для предоставления конкурентных цен своим клиентам предприятия розничной торговли часто изменяют цены продуктов.</span><span class="sxs-lookup"><span data-stu-id="e2d96-104">In order to provide competitive prices to their customers, retailers often change prices of products.</span></span> <span data-ttu-id="e2d96-105">Менеджерам магазина требуется возможность легкого доступа к последним или предстоящим изменениям цен, чтобы они могли планировать необходимые ресурсы для обновления ценников, отображаемых на полках магазина.</span><span class="sxs-lookup"><span data-stu-id="e2d96-105">Store managers want the ability to easily access recent or upcoming price changes so that they can plan for the required resources to update the price labels displayed on the store shelves.</span></span> <span data-ttu-id="e2d96-106">В версии 10.0 Dynamics 365 for Retail менеджер магазина может открыть отчет **Цена**, перейдя в **Все розничные магазины \> Магазин \> Отчет о цене** и просмотрев обновленные цены на продукты, связанные с магазином.</span><span class="sxs-lookup"><span data-stu-id="e2d96-106">With release 10.0 of Dynamics 365 for Retail, a store manager can open the **Price** report by navigating to **All retail stores \> Store \> Price report** and viewing the updated prices for the products associated to the store.</span></span> 

<span data-ttu-id="e2d96-107">Чтобы включить отчет о ценах, должен быть включен параметр **Включить отчет о ценах для розничного магазина**.</span><span class="sxs-lookup"><span data-stu-id="e2d96-107">To enable the price report, the **Enable price report for Retail store** parameter must be turned on.</span></span> <span data-ttu-id="e2d96-108">Этот параметр находится на вкладке **Параметры розничной торговли \> Скидки \> Разное**. При открытии страницы **Отчет о ценах** отображается диалоговое окно с различными конфигурациями.</span><span class="sxs-lookup"><span data-stu-id="e2d96-108">This parameter is located on the **Retail parameters \> Discounts \> Miscellaneous** tab. Opening the **Price report** page displays a dialog box with various configurations.</span></span> <span data-ttu-id="e2d96-109">Ниже перечислены доступные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e2d96-109">The available configurations are listed below.</span></span>

| <span data-ttu-id="e2d96-110">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="e2d96-110">Configuration</span></span> | <span data-ttu-id="e2d96-111">описание</span><span class="sxs-lookup"><span data-stu-id="e2d96-111">Description</span></span> |
|---|---|
| <span data-ttu-id="e2d96-112">Начальная дата / Конечная дата</span><span class="sxs-lookup"><span data-stu-id="e2d96-112">From date / To date</span></span>| <span data-ttu-id="e2d96-113">Диапазон дат, для которого требуется создать отчет о ценах.</span><span class="sxs-lookup"><span data-stu-id="e2d96-113">The date range for which the price report should be generated.</span></span> <span data-ttu-id="e2d96-114">Продолжительность в настоящее время ограничивается 7 днями.</span><span class="sxs-lookup"><span data-stu-id="e2d96-114">The duration is currently limited to 7 days.</span></span> |
| <span data-ttu-id="e2d96-115">Канал</span><span class="sxs-lookup"><span data-stu-id="e2d96-115">Channel</span></span>| <span data-ttu-id="e2d96-116">Розничный магазин, для которого требуется создать отчет о ценах.</span><span class="sxs-lookup"><span data-stu-id="e2d96-116">The retail store for which the price report should be generated.</span></span> |
| <span data-ttu-id="e2d96-117">Показать продукты с доступными запасами</span><span class="sxs-lookup"><span data-stu-id="e2d96-117">Display products with available inventory</span></span>| <span data-ttu-id="e2d96-118">Если установить **Да**, будут показаны цены только для тех продуктов, для которых в настоящее время в магазине имеются доступные физические складские запасы.</span><span class="sxs-lookup"><span data-stu-id="e2d96-118">Setting this to **Yes** will show the prices for only those products which currently have physical inventory available in the store.</span></span> |
| <span data-ttu-id="e2d96-119">Показать цены для вариантов</span><span class="sxs-lookup"><span data-stu-id="e2d96-119">Display prices for variants</span></span> | <span data-ttu-id="e2d96-120">Если установить **Да**, будут отображаться цены вариантов вместе с шаблонами продукта.</span><span class="sxs-lookup"><span data-stu-id="e2d96-120">Setting this to **Yes** will display the prices of the variants along with the product masters.</span></span> <span data-ttu-id="e2d96-121">Это должно быть включено **Вкл.** только при наличии разных цены за разные варианты, поскольку количество строк становится очень большим.</span><span class="sxs-lookup"><span data-stu-id="e2d96-121">This should only be turned **On** if you have variant-specific prices, because the number of rows grows very large.</span></span> <span data-ttu-id="e2d96-122">В будущих выпусках мы обеспечим цены на основе аналитик, чтобы менеджер магазина мог выбрать измерения, по которым должны отображаться цены.</span><span class="sxs-lookup"><span data-stu-id="e2d96-122">In future releases, we will enable the dimensions-based prices so that the store manager can choose the dimensions for which the prices should be displayed.</span></span> |
| <span data-ttu-id="e2d96-123">Показать продукты с изменениями цен</span><span class="sxs-lookup"><span data-stu-id="e2d96-123">Display products with price changes</span></span> | <span data-ttu-id="e2d96-124">Если установить значение **Да**, будут отображаться цены только для тех дат, в которые цены были изменены.</span><span class="sxs-lookup"><span data-stu-id="e2d96-124">Setting this to **Yes** will display the prices for only those dates on which the price has been changed.</span></span> <span data-ttu-id="e2d96-125">Цена за *один день до* выбранной даты **Начальная дата** всегда отображается, чтобы менеджер магазина мог легко выявить продукты, цены на которые не изменялись в течение всего выбранного периода, и также может просмотреть текущую цену.</span><span class="sxs-lookup"><span data-stu-id="e2d96-125">The price for *one day before* the selected **From date** will always be displayed, so that the store manager can easily identity the products which have not changed prices for the entire selected duration, and can also view the current price.</span></span> |

<span data-ttu-id="e2d96-126">После создания отчета можно загрузить файл Excel для любой дополнительной требуемой фильтрации.</span><span class="sxs-lookup"><span data-stu-id="e2d96-126">After the report is generated, the Excel file can be downloaded for any additional filtering needs.</span></span> <span data-ttu-id="e2d96-127">Отчет о ценах может также использоваться для проверки журнала цен продуктов за прошедшие даты.</span><span class="sxs-lookup"><span data-stu-id="e2d96-127">The price report can also be used to check the historical prices of products for past dates.</span></span>
