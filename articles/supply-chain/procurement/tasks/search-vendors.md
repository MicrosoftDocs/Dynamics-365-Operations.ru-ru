---
title: Поиск поставщиков
description: Научитесь выполнять поиск поставщиков по определенным критериям.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendSearchCriterion, VendSearchAddCategory, VendSearchAddReviewCriterionGroup, VendSearchResults, VendSearchAddReviewCriterion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bc28deb979fe8dc4e31befe6d4d5f6f91388f13e
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018060"
---
# <a name="search-for-vendors"></a><span data-ttu-id="b8565-103">Поиск поставщиков</span><span class="sxs-lookup"><span data-stu-id="b8565-103">Search for vendors</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b8565-104">Научитесь выполнять поиск поставщиков по определенным критериям.</span><span class="sxs-lookup"><span data-stu-id="b8565-104">Learn how to search for vendors based on specific criteria.</span></span> <span data-ttu-id="b8565-105">В этом примере показано, как искать поставщиков, утвержденных для определенной категории закупаемой продукции, с получением их основного адреса в конкретной стране.</span><span class="sxs-lookup"><span data-stu-id="b8565-105">This example shows you how to search for vendors that are approved for a particular procurement category and have their primary address in a specific country.</span></span> <span data-ttu-id="b8565-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="b8565-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="b8565-107">Эта задача обычно выполняется специалистом по закупкам.</span><span class="sxs-lookup"><span data-stu-id="b8565-107">This task would usually be carried out by a procurement professional.</span></span>

1. <span data-ttu-id="b8565-108">Перейдите в раздел "Закупки и источники" > "Поставщики" > "Поиск поставщика".</span><span class="sxs-lookup"><span data-stu-id="b8565-108">Go to Procurement and sourcing > Vendors > Vendor search.</span></span>
2. <span data-ttu-id="b8565-109">Щелкните значок "плюс", чтобы открыть страницу "Выбор категории закупаемой продукции".</span><span class="sxs-lookup"><span data-stu-id="b8565-109">Click on the Plus icon to open the Procurement category selection page.</span></span>  
3. <span data-ttu-id="b8565-110">В дереве выберите "CORP PROCUREMENT CATEGORIES\OFFICE MACHINES".</span><span class="sxs-lookup"><span data-stu-id="b8565-110">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE MACHINES'.</span></span>
    * <span data-ttu-id="b8565-111">Если вы выполняете эту процедуру как руководство по задаче, вам может потребоваться нажать кнопку "Разблокировать", прежде чем вы сможете выбрать правильный узел.</span><span class="sxs-lookup"><span data-stu-id="b8565-111">If you're running this procedure as a task guide, you may have to click the Unlock button before you can select the correct node.</span></span> <span data-ttu-id="b8565-112">Если вы используете не USMF, выберите одну из имеющихся у вас категорий.</span><span class="sxs-lookup"><span data-stu-id="b8565-112">If you're not using USMF, select one of the categories that you have.</span></span>  
4. <span data-ttu-id="b8565-113">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="b8565-113">Click Add.</span></span>
    * <span data-ttu-id="b8565-114">Здесь можно выбрать несколько категорий.</span><span class="sxs-lookup"><span data-stu-id="b8565-114">It's possible to select more than one category here.</span></span> <span data-ttu-id="b8565-115">При этом при поиске будут найдены все поставщики, утвержденные по крайней мере для одной из категорий.</span><span class="sxs-lookup"><span data-stu-id="b8565-115">If you do so, the search will find all the vendors that are approved for at least one of the categories.</span></span>  
5. <span data-ttu-id="b8565-116">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b8565-116">Click OK.</span></span>
6. <span data-ttu-id="b8565-117">В поле "Страна/регион" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b8565-117">In the Country/region field, type a value.</span></span>
7. <span data-ttu-id="b8565-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b8565-118">Click OK.</span></span>

