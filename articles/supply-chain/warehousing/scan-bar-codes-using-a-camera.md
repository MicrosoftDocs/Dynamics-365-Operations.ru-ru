---
title: Сканирование штрих-кодов с помощью камеры в приложении Dynamics 365 Supply Chain Management - Warehousing
description: В этом разделе объясняется, как настроить приложение Dynamics 365 Supply Chain Management - Warehousing для сканирования штрих-кодов с помощью камеры мобильного устройства.
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8062a981f792bcfed2713d3cb6a42f414394f6a4
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251477"
---
# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-supply-chain-management---warehousing-app"></a><span data-ttu-id="07415-103">Сканирование штрих-кодов с помощью камеры в приложении Dynamics 365 Supply Chain Management - Warehousing</span><span class="sxs-lookup"><span data-stu-id="07415-103">Scan bar codes using a camera in Dynamics 365 Supply Chain Management - Warehousing app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07415-104">В этом разделе объясняется, как настроить приложение Dynamics 365 Supply Chain Management - Warehousing для сканирования штрих-кодов с помощью камеры мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="07415-104">This topic explains how to set up Dynamics 365 Supply Chain Management - Warehousing app to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="07415-105">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="07415-105">Prerequisites</span></span>
<span data-ttu-id="07415-106">Для использования этой функции необходимо, чтобы была установлена версия 1.2.0.0 приложения Warehousing, а мобильное устройство должно иметь камеру.</span><span class="sxs-lookup"><span data-stu-id="07415-106">To use this feature, you need to have version 1.2.0.0 of the Warehousing app installed, and your device must have a camera.</span></span> <span data-ttu-id="07415-107">При открытии приложения после обновления будет предложено разрешить приложению использование камеры.</span><span class="sxs-lookup"><span data-stu-id="07415-107">When you open the app after updating, you will be prompted to allow the app to use the camera.</span></span> <span data-ttu-id="07415-108">Если в устройстве нет камеры, запрос не отображается, и использовать камеру как сканер будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="07415-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="07415-109">Настройка</span><span class="sxs-lookup"><span data-stu-id="07415-109">Setup</span></span>
<span data-ttu-id="07415-110">В параметрах экрана приложения Warehousing можно выбрать, следует ли использовать камеру для сканирования штрих-кодов.</span><span class="sxs-lookup"><span data-stu-id="07415-110">In the Display settings of the Warehousing application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="07415-111">Если включить пункт **Использовать камеру как сканер**, можно использовать камеру в каждом поле ввода, для которого задан предпочтительный режима ввода **Сканирование**.</span><span class="sxs-lookup"><span data-stu-id="07415-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="07415-112">Для управления возможностью сканирования для поля ввода на странице **Имена полей в приложении склада** задайте для параметра **Предпочтительный режим ввода** значение **Сканирование**.</span><span class="sxs-lookup"><span data-stu-id="07415-112">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="07415-113">Если этот параметр выбран, камеру можно использовать для сканирования в приложении Warehousing.</span><span class="sxs-lookup"><span data-stu-id="07415-113">When this option is selected, a camera can be used for scanning in the Warehousing app.</span></span> <span data-ttu-id="07415-114">Сведения о настройке имен полей приложения Warehousing см. в разделе [Настройка имен полей приложения в приложении склада](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span><span class="sxs-lookup"><span data-stu-id="07415-114">For information about how to configure app field names in Warehousing, see [Configure app field names in Warehousing app](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="07415-115">Поддерживаемые форматы штрих-кодов</span><span class="sxs-lookup"><span data-stu-id="07415-115">Supported bar code formats</span></span>
<span data-ttu-id="07415-116">Поддерживаются основные форматы штрих-кодов, включая Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, и QR-коды.</span><span class="sxs-lookup"><span data-stu-id="07415-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="07415-117">Навигация</span><span class="sxs-lookup"><span data-stu-id="07415-117">Navigation</span></span>
<span data-ttu-id="07415-118">Страница камеры будет инициирована на каждой странице, на которой поле ввода имеет предпочтительный режим ввода "Сканирование"; находясь на странице камеры, используйте следующие параметры для перемещения:</span><span class="sxs-lookup"><span data-stu-id="07415-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="07415-119">Нажмите кнопку "Назад", чтобы вернуться на страницу задачи и подробных сведений.</span><span class="sxs-lookup"><span data-stu-id="07415-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="07415-120">Щелкните значок карандаша на странице задач и сведений для перехода на страницу, на которой можно ввести данные вручную.</span><span class="sxs-lookup"><span data-stu-id="07415-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="07415-121">Щелкните значок камеры на странице задач и сведений для возврата на страницу камеры.</span><span class="sxs-lookup"><span data-stu-id="07415-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="07415-122">Страница задач и сведений</span><span class="sxs-lookup"><span data-stu-id="07415-122">Task and details page</span></span> | <span data-ttu-id="07415-123">Страница камеры</span><span class="sxs-lookup"><span data-stu-id="07415-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![пример-страницы-задач-и-сведений-для-сканирования-камерой](./media/camera-scanning-example-task-detail-page50.png)          | ![пример-страницы-камеры-для-сканирования-камерой-меньше](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="07415-126">На странице камеры при нажатии кнопки камеры она будет недоступна, пока выполняется попытка идентификации штрих-кода.</span><span class="sxs-lookup"><span data-stu-id="07415-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="07415-127">Если штрих-код не будет идентифицирован в течение 5 секунд, процесс завершится в результате истечения времени ожидания и кнопка камеры снова станет доступной.</span><span class="sxs-lookup"><span data-stu-id="07415-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="07415-128">Затем можно попытаться повторить сканирование штрих-кода.</span><span class="sxs-lookup"><span data-stu-id="07415-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="07415-129">Направляя камеру на штрих-код, следите, чтобы штрих-код был выровнен по квадратным скобкам для наилучшего результата.</span><span class="sxs-lookup"><span data-stu-id="07415-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="07415-130">После успешного сканирования штрих-кода результат будет обработан и будет произведен переход к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="07415-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="07415-131">Если следующий шаг содержит другое поле ввода с предпочтительным режимом ввода "Сканирование", страница камеры будет запущена снова.</span><span class="sxs-lookup"><span data-stu-id="07415-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="07415-132">Если следующий шаг не является полем сканирования, страница камеры не инициируется.</span><span class="sxs-lookup"><span data-stu-id="07415-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>

