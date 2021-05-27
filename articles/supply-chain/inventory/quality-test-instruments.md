---
title: Инструменты проверки управления качеством
description: В этой теме описывается, как создавать инструменты проверки, чтобы можно было использовать для проверок с заказами контроля качества в Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3806ca26b8909b03768dad54ddad0084e1cea4a6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021740"
---
# <a name="quality-management-test-instruments"></a><span data-ttu-id="33375-103">Инструменты проверки управления качеством</span><span class="sxs-lookup"><span data-stu-id="33375-103">Quality management test instruments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33375-104">В этой теме описывается, как создавать инструменты проверки, чтобы можно было использовать для проверок с заказами контроля качества в Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="33375-104">This topic describes how to create test instruments that can be used for tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="33375-105">Страница **Инструменты проверки** используется для определения и просмотра сведений об устройствах, которые используются для выполнения проверок в заказах контроля качества.</span><span class="sxs-lookup"><span data-stu-id="33375-105">You use the **Test instruments** page to define and view details about the devices that are used to perform tests on quality orders.</span></span> <span data-ttu-id="33375-106">Инструменты проверки необязательны.</span><span class="sxs-lookup"><span data-stu-id="33375-106">Test instruments are optional.</span></span> <span data-ttu-id="33375-107">Однако они могут помочь работникам системы контроля качества понять, какое устройство или инструмент следует использовать для выполнения конкретной проверки.</span><span class="sxs-lookup"><span data-stu-id="33375-107">However, they can help quality workers know which device or tool they should use to perform a specific test.</span></span>

## <a name="test-instrument-example"></a><span data-ttu-id="33375-108">Пример инструмента проверки</span><span class="sxs-lookup"><span data-stu-id="33375-108">Test instrument example</span></span>

<span data-ttu-id="33375-109">Вы выполняете различные проверки электрических компонентов.</span><span class="sxs-lookup"><span data-stu-id="33375-109">You're performing various tests on electrical components.</span></span> <span data-ttu-id="33375-110">Некоторые проверки представляют собой выходное напряжение компонентов, другая — для температуры, другая — для массы.</span><span class="sxs-lookup"><span data-stu-id="33375-110">Some tests are for the voltage output of the components, one test is for their temperature, and one test is for their weight.</span></span> <span data-ttu-id="33375-111">Для выполнения каждой проверки используется несколько инструментов, устройств или приборов.</span><span class="sxs-lookup"><span data-stu-id="33375-111">Different tools, devices, or equipment is used to perform each test.</span></span> <span data-ttu-id="33375-112">Например, индикатор напряжения используется для измерения напряжения, для измерения температуры используется термометр, а для измерения веса используются весы.</span><span class="sxs-lookup"><span data-stu-id="33375-112">For example, a voltage meter is used to measure voltage, a thermometer is used to measure temperature, and a scale is used to measure weight.</span></span> <span data-ttu-id="33375-113">Каждое из этих устройств можно настроить как инструмент проверки и указать единицу измерения, в которой должны быть записаны результаты проверок.</span><span class="sxs-lookup"><span data-stu-id="33375-113">You can configure each of these devices as a test instrument and indicate the unit of measure that the test results should be recorded in.</span></span> <span data-ttu-id="33375-114">Например, результаты измерения напряжения записываются в вольтах, результаты термометра записываются в градусах по Фаренгейту или Цельсия, а результаты весов записываются в фунтах или килограммах.</span><span class="sxs-lookup"><span data-stu-id="33375-114">For example, results from the voltage meter are recorded in volts, results from the thermometer are recorded in degrees Fahrenheit or degrees Celsius, and results from the scale are recorded in pounds or kilograms.</span></span>

## <a name="create-a-test-instrument"></a><span data-ttu-id="33375-115">Создание инструмента проверки</span><span class="sxs-lookup"><span data-stu-id="33375-115">Create a test instrument</span></span>

1. <span data-ttu-id="33375-116">Перейдите **Управление запасами \> Настройка \> Контроль качества \> Инструменты проверки**.</span><span class="sxs-lookup"><span data-stu-id="33375-116">Go to **Inventory management \> Setup \> Quality control \> Test instruments**.</span></span>
1. <span data-ttu-id="33375-117">На панели операций выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="33375-117">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="33375-118">Затем задайте следующие поля для новой строки:</span><span class="sxs-lookup"><span data-stu-id="33375-118">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="33375-119">**Инструмент проверки** — введите уникальный код или название инструмента проверки.</span><span class="sxs-lookup"><span data-stu-id="33375-119">**Test instrument** – Enter a unique ID or name for the test instrument.</span></span>
    - <span data-ttu-id="33375-120">**Описание** — введите подробное описание инструмента проверки.</span><span class="sxs-lookup"><span data-stu-id="33375-120">**Description** – Enter a detailed description of the test instrument.</span></span>
    - <span data-ttu-id="33375-121">**Единица измерения** — выберите единицу измерения, в которой результаты измеряются результаты.</span><span class="sxs-lookup"><span data-stu-id="33375-121">**Unit** – Select the unit that the instrument measures results in.</span></span> <span data-ttu-id="33375-122">Поле **Точность** устанавливается автоматически в зависимости от выбранной единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="33375-122">The **Precision** field is automatically set, based on the unit that you select.</span></span>

1. <span data-ttu-id="33375-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="33375-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="33375-124">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="33375-124">Additional resources</span></span>

- [<span data-ttu-id="33375-125">Проверка управления качеством</span><span class="sxs-lookup"><span data-stu-id="33375-125">Quality management test</span></span>](quality-tests.md)
- [<span data-ttu-id="33375-126">Группы проверки контроля качества</span><span class="sxs-lookup"><span data-stu-id="33375-126">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
