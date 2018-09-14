--- 
title: "Настройка рекомендаций по продуктам на основе машинного обучения"
description: "Эта процедура обновляет данные в хранилище объектов, используемые системой машинного обучения, которая обеспечивает рекомендации по продуктам, а затем обеспечивает рекомендации по продуктам в клиентах POS."
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BIMeasurementDeployManagementEntityStore, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 700af913f18e23c66db53a92033def06818af1ec
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="4d720-103">Настройка рекомендаций по продуктам на основе машинного обучения</span><span class="sxs-lookup"><span data-stu-id="4d720-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="4d720-104">Эта процедура обновляет данные в хранилище объектов, используемые системой машинного обучения, которая обеспечивает рекомендации по продуктам, а затем обеспечивает рекомендации по продуктам в клиентах POS.</span><span class="sxs-lookup"><span data-stu-id="4d720-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="4d720-105">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="4d720-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="4d720-106">Перейдите в раздел "Администрирование системы" > "Настройка" > "Хранилище объектов".</span><span class="sxs-lookup"><span data-stu-id="4d720-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="4d720-107">В списке найдите и выберите запись "RetailSales".</span><span class="sxs-lookup"><span data-stu-id="4d720-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="4d720-108">Нажмите кнопку Обновить.</span><span class="sxs-lookup"><span data-stu-id="4d720-108">Click Refresh.</span></span>
4. <span data-ttu-id="4d720-109">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="4d720-109">Click OK.</span></span>
5. <span data-ttu-id="4d720-110">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4d720-110">Close the page.</span></span>
6. <span data-ttu-id="4d720-111">Перейдите в раздел "Розничная торговля и коммерция" > "Настройка центрального офиса" > "Параметры" > "Параметры розничной торговли".</span><span class="sxs-lookup"><span data-stu-id="4d720-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="4d720-112">Выберите вкладку "Машинное обучение".</span><span class="sxs-lookup"><span data-stu-id="4d720-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="4d720-113">Выберите значение "Да" в поле "Включить рекомендации по продуктам".</span><span class="sxs-lookup"><span data-stu-id="4d720-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="4d720-114">Если получено сообщение "Не удалось извлечь модели рекомендаций", это потому, что вы недавно обновили хранилище объектов и система еще не завершила ассимиляцию новых данных.</span><span class="sxs-lookup"><span data-stu-id="4d720-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="4d720-115">Подождите 2-3 часа и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="4d720-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="4d720-116">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4d720-116">Click Save.</span></span>
10. <span data-ttu-id="4d720-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="4d720-117">Close the page.</span></span>


