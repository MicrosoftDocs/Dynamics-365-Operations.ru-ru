---
title: Создание финансовых аналитик для POS-регистраторов и настройка значений аналитики для регистраторов
description: Эта процедура содержит инструкции по созданию финансовых аналитик для POS-терминалов и демонстрирует, как задать значения финансовых аналитик для терминалов.
author: jashanno
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e04af04de3d18d375ce3609ab4cd53f652c2fbc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023807"
---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="98984-103">Создание финансовых аналитик для POS-регистраторов и настройка значений аналитики для регистраторов</span><span class="sxs-lookup"><span data-stu-id="98984-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="98984-104">Эта процедура содержит инструкции по созданию финансовых аналитик для POS-терминалов и демонстрирует, как задать значения финансовых аналитик для терминалов.</span><span class="sxs-lookup"><span data-stu-id="98984-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="98984-105">Эта процедура не включает другие связанные действия, например создание наборов аналитик и структур счетов.</span><span class="sxs-lookup"><span data-stu-id="98984-105">This procedure doesn’t include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="98984-106">Эти задачи можно найти в других разделах.</span><span class="sxs-lookup"><span data-stu-id="98984-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="98984-107">В данной записи используется демонстрационная компания USRT.</span><span class="sxs-lookup"><span data-stu-id="98984-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="98984-108">Перейдите в раздел "Главная книга" > "План счетов" > "Аналитики" > "Финансовые аналитики".</span><span class="sxs-lookup"><span data-stu-id="98984-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="98984-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="98984-109">Click New.</span></span>
3. <span data-ttu-id="98984-110">В поле "Использовать значения из" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="98984-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="98984-111">В поле "Наименование аналитики" введите значение.</span><span class="sxs-lookup"><span data-stu-id="98984-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="98984-112">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="98984-112">Click Activate.</span></span>
6. <span data-ttu-id="98984-113">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="98984-113">Click Close.</span></span>
7. <span data-ttu-id="98984-114">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="98984-114">Click Activate.</span></span>
8. <span data-ttu-id="98984-115">Щелкните "Значения аналитик".</span><span class="sxs-lookup"><span data-stu-id="98984-115">Click Dimension values.</span></span>
9. <span data-ttu-id="98984-116">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="98984-116">Close the page.</span></span>
10. <span data-ttu-id="98984-117">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="98984-117">Click Save.</span></span>
11. <span data-ttu-id="98984-118">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="98984-118">Close the page.</span></span>
12. <span data-ttu-id="98984-119">Перейдите в раздел "Retail и Commerce" > "Настройка канала" > "Настройка POS" > "Кассы".</span><span class="sxs-lookup"><span data-stu-id="98984-119">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="98984-120">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="98984-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="98984-121">Переключите развертывание раздела "Финансовые аналитики".</span><span class="sxs-lookup"><span data-stu-id="98984-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="98984-122">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="98984-122">Click Edit.</span></span>
16. <span data-ttu-id="98984-123">В поле "Терминал" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="98984-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="98984-124">В списке найдите и выберите значение аналитики для обновляемого терминала.</span><span class="sxs-lookup"><span data-stu-id="98984-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="98984-125">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="98984-125">Click Save.</span></span>

