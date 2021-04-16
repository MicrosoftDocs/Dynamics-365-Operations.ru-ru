---
title: Сканирование штрих-кодов с помощью камеры в мобильном приложении управления складом
description: В этом разделе объясняется, как настроить мобильное приложение управления складом для сканирования штрих-кодов с помощью камеры мобильного устройства.
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f61f9c45b95b730a7f1743963658ec00abfbb56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831226"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="9c77e-103">Сканирование штрих-кодов с помощью камеры в мобильном приложении управления складом</span><span class="sxs-lookup"><span data-stu-id="9c77e-103">Scan bar codes using a camera in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c77e-104">В этом разделе объясняется, как настроить мобильное приложение управления складом для сканирования штрих-кодов с помощью камеры мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="9c77e-104">This topic explains how to set up the Warehouse Management mobile app to scan bar codes using a camera on a mobile device.</span></span>

## <a name="setup"></a><span data-ttu-id="9c77e-105">Настройка</span><span class="sxs-lookup"><span data-stu-id="9c77e-105">Setup</span></span>

<span data-ttu-id="9c77e-106">В параметрах экрана мобильного приложения управления складом можно выбрать, следует ли использовать камеру для сканирования штрих-кодов.</span><span class="sxs-lookup"><span data-stu-id="9c77e-106">In the display settings of the Warehouse Management mobile app, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="9c77e-107">Если включить пункт **Использовать камеру как сканер**, можно использовать камеру в каждом поле ввода, для которого задан предпочтительный режима ввода **Сканирование**.</span><span class="sxs-lookup"><span data-stu-id="9c77e-107">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span>

<span data-ttu-id="9c77e-108">Для управления возможностью сканирования для поля ввода на странице **Имена полей в приложении склада** задайте для параметра **Предпочтительный режим ввода** значение **Сканирование**.</span><span class="sxs-lookup"><span data-stu-id="9c77e-108">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="9c77e-109">Если этот параметр выбран, камеру можно использовать для сканирования в мобильном приложении управления складом.</span><span class="sxs-lookup"><span data-stu-id="9c77e-109">When this option is selected, a camera can be used for scanning in the Warehouse Management mobile app.</span></span> <span data-ttu-id="9c77e-110">Дополнительные сведения см. в разделе [Настройка полей мобильного приложения управления складом](configure-app-field-names-priorities-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="9c77e-110">For more information, see [Configure fields for the Warehouse Management mobile app](configure-app-field-names-priorities-warehouse.md).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="9c77e-111">Поддерживаемые форматы штрих-кодов</span><span class="sxs-lookup"><span data-stu-id="9c77e-111">Supported bar code formats</span></span>

<span data-ttu-id="9c77e-112">Поддерживаются основные форматы штрих-кодов, включая Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, и QR-коды.</span><span class="sxs-lookup"><span data-stu-id="9c77e-112">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span>

## <a name="navigation"></a><span data-ttu-id="9c77e-113">Навигация</span><span class="sxs-lookup"><span data-stu-id="9c77e-113">Navigation</span></span>

<span data-ttu-id="9c77e-114">Страница камеры будет инициирована на каждой странице, на которой в поле ввода для параметра **Предпочтительный режим ввода** установлено значение *Сканирование*; находясь на странице камеры, используйте следующие параметры для перемещения:</span><span class="sxs-lookup"><span data-stu-id="9c77e-114">The camera page will be initiated on each page where the input field has its **Preferred input mode** set to *Scanning*, when you are on the camera page use the following options to navigate:</span></span>

- <span data-ttu-id="9c77e-115">Выберите кнопку "Назад", чтобы вернуться на страницу **Задачи и сведения**.</span><span class="sxs-lookup"><span data-stu-id="9c77e-115">Select the back button to go back to the **Task and details** page.</span></span>
- <span data-ttu-id="9c77e-116">Выберите значок карандаша на странице **Задача и сведения** для перехода на страницу, на которой можно ввести данные вручную.</span><span class="sxs-lookup"><span data-stu-id="9c77e-116">Select the pencil on the **Task and details** page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="9c77e-117">Выберите значок камеры на странице **Задача и сведения** для возврата на страницу камеры.</span><span class="sxs-lookup"><span data-stu-id="9c77e-117">Select the camera on the **Task and details** page to go back to the camera page.</span></span>

<span data-ttu-id="9c77e-118">На странице камеры при выборе кнопки камеры она будет недоступна, пока выполняется попытка идентификации штрих-кода.</span><span class="sxs-lookup"><span data-stu-id="9c77e-118">On the camera page, when you select the camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="9c77e-119">Если штрих-код не будет идентифицирован в течение 5 секунд, процесс завершится в результате истечения времени ожидания и кнопка камеры снова станет доступной.</span><span class="sxs-lookup"><span data-stu-id="9c77e-119">If a bar code is not identified within 5 seconds, the process will time out and the camera button will become available again.</span></span> <span data-ttu-id="9c77e-120">Затем можно попытаться повторить сканирование штрих-кода.</span><span class="sxs-lookup"><span data-stu-id="9c77e-120">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="9c77e-121">Направляя камеру на штрих-код, следите, чтобы штрих-код был выровнен по квадратным скобкам для наилучшего результата.</span><span class="sxs-lookup"><span data-stu-id="9c77e-121">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="9c77e-122">После успешного сканирования штрих-кода результат будет обработан и будет произведен переход к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="9c77e-122">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="9c77e-123">Если следующий шаг содержит другое поле ввода с предпочтительным режимом ввода "Сканирование", страница камеры будет запущена снова.</span><span class="sxs-lookup"><span data-stu-id="9c77e-123">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="9c77e-124">Если следующий шаг не является полем сканирования, страница камеры не инициируется.</span><span class="sxs-lookup"><span data-stu-id="9c77e-124">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]