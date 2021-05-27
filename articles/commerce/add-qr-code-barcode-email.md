---
title: Добавление QR-кода или штрих-кода к транзакционным письмам и сообщениям электронной почты с чеками
description: В этой теме объясняется, как вставить QR-коды и штрих-коды, представляющие коды заказов в транзакционные письма и сообщения электронной почты с чеками в Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 9eea69f9618d4387f5d6320620dfee5d74813fc0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019547"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a><span data-ttu-id="d5279-103">Добавление QR-кода или штрих-кода к транзакционным письмам и сообщениям электронной почты с чеками</span><span class="sxs-lookup"><span data-stu-id="d5279-103">Add a QR code or bar code to transactional and receipt emails</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d5279-104">В этой теме объясняется, как вставить QR-коды и штрих-коды, представляющие коды заказов в транзакционные письма и сообщения электронной почты с чеками в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d5279-104">This topic explains how to insert QR codes and bar codes that represent order IDs into transactional and receipt emails in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d5279-105">Можно легко включить QR-коды и штрих-коды в транзакционные письма, чтобы ускорить процесс поиска заказов в розничной среде.</span><span class="sxs-lookup"><span data-stu-id="d5279-105">You can easily include QR codes and bar codes in transactional emails to help speed up the order lookup process in a retail environment.</span></span> <span data-ttu-id="d5279-106">Чтобы вставить QR-коды и штрих-коды в сообщения электронной почты, используется тег HTML **\<img\>**, который запрашивает изображение с кодом QR или штрих-кодом в службе создания и визуализации.</span><span class="sxs-lookup"><span data-stu-id="d5279-106">To insert QR codes and bar codes into emails, you use an HTML **\<img\>** tag that requests a QR code or bar code image from a generation and rendering service.</span></span> <span data-ttu-id="d5279-107">Microsoft не предоставляет эту услугу.</span><span class="sxs-lookup"><span data-stu-id="d5279-107">Microsoft doesn't provide this service.</span></span> <span data-ttu-id="d5279-108">Однако имеется много бесплатных или недорогих услуг, которые могут обслуживать QR-коды или штрих-коды, которые динамически генерируются на основе значения, переданного в строке запроса.</span><span class="sxs-lookup"><span data-stu-id="d5279-108">However, there are many free or inexpensive services that can serve QR codes or bar codes that are dynamically generated based on a value that is passed in a query string.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a><span data-ttu-id="d5279-109">Добавление QR-кода или штрих-кода к транзакционное письмо</span><span class="sxs-lookup"><span data-stu-id="d5279-109">Add a QR code or bar code to a transactional email</span></span>

<span data-ttu-id="d5279-110">Для вставки QR-кода или штрих-кода в транзакционное письмо, отправляемое как часть покупки по электронной коммерции, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d5279-110">To insert a QR code or bar code into a transactional email that is sent as part of an e-commerce purchase, follow these steps.</span></span>

1. <span data-ttu-id="d5279-111">Откройте исходный HTML для шаблона транзакционного письма и добавьте тег HTML **\<img\>**, указывающий на вашу службу QR-кода или штрих-кода.</span><span class="sxs-lookup"><span data-stu-id="d5279-111">Open the source HTML for the transactional email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="d5279-112">Рассмотрим пример:</span><span class="sxs-lookup"><span data-stu-id="d5279-112">Here is an example.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    <span data-ttu-id="d5279-113">Ниже приведено объяснение предыдущего примера:</span><span class="sxs-lookup"><span data-stu-id="d5279-113">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="d5279-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** представляет домен вашей службы QR-кода или штрих-кода.</span><span class="sxs-lookup"><span data-stu-id="d5279-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="d5279-115">**данные** представляют собой параметр, используемый службой QR-кода или штрих-кода для получения содержимого, которое должно быть визуализировано как QR-код или штрих-код.</span><span class="sxs-lookup"><span data-stu-id="d5279-115">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="d5279-116">Этому параметру должно быть присвоено значение **%salesid%**.</span><span class="sxs-lookup"><span data-stu-id="d5279-116">The value **%salesid%** must be assigned to this parameter.</span></span> <span data-ttu-id="d5279-117">Обратите внимание, что в этом примере значение также используется в качестве замещающего текста для изображения.</span><span class="sxs-lookup"><span data-stu-id="d5279-117">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="d5279-118">**param1** и **param2** представляют дополнительные необязательные параметры.</span><span class="sxs-lookup"><span data-stu-id="d5279-118">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="d5279-119">Перейдите в раздел **Retail и Commerce \> Настройка Headquarters \> Параметры \> Шаблоны сообщений электронной почты организации** и загрузите обновленный HTML в соответствующий шаблон сообщения электронной почты с транзакционным письмом.</span><span class="sxs-lookup"><span data-stu-id="d5279-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the appropriate transactional email template.</span></span>

> [!NOTE]
> <span data-ttu-id="d5279-120">Параметры могут отличаться между поставщиками службы QR-кода и штрих-кода.</span><span class="sxs-lookup"><span data-stu-id="d5279-120">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="d5279-121">Поэтому обратитесь к поставщику услуг для подтверждения параметров, которые необходимо назначить значениям.</span><span class="sxs-lookup"><span data-stu-id="d5279-121">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a><span data-ttu-id="d5279-122">Добавление QR-кода или штрих-кода к сообщению электронной почты с чеками</span><span class="sxs-lookup"><span data-stu-id="d5279-122">Add a QR code or bar code to a receipt email</span></span> 

<span data-ttu-id="d5279-123">Чтобы вставить QR-код или штрих-код в сообщение электронной почты с чеками, которое может быть отправлено после покупки на POS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d5279-123">To insert a QR code or bar code into a receipt email that can be sent after a purchase is made at the point of sale (POS), follow these steps.</span></span>

1. <span data-ttu-id="d5279-124">Откройте исходный HTML для шаблона сообщения электронной почты с чеками и добавьте тег HTML **\<img\>**, указывающий на вашу службу QR-кода или штрих-кода.</span><span class="sxs-lookup"><span data-stu-id="d5279-124">Open the source HTML for the receipt email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="d5279-125">Рассмотрим пример ниже.</span><span class="sxs-lookup"><span data-stu-id="d5279-125">Here is an example below.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    <span data-ttu-id="d5279-126">Ниже приведено объяснение предыдущего примера:</span><span class="sxs-lookup"><span data-stu-id="d5279-126">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="d5279-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** представляет домен вашей службы QR-кода или штрих-кода.</span><span class="sxs-lookup"><span data-stu-id="d5279-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="d5279-128">**данные** представляют собой параметр, используемый службой QR-кода или штрих-кода для получения содержимого, которое должно быть визуализировано как QR-код или штрих-код.</span><span class="sxs-lookup"><span data-stu-id="d5279-128">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="d5279-129">Этому параметру должно быть присвоено значение **%receiptid%**.</span><span class="sxs-lookup"><span data-stu-id="d5279-129">The value **%receiptid%** must be assigned to this parameter.</span></span> <span data-ttu-id="d5279-130">Обратите внимание, что в этом примере значение также используется в качестве замещающего текста для изображения.</span><span class="sxs-lookup"><span data-stu-id="d5279-130">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="d5279-131">**param1** и **param2** представляют дополнительные необязательные параметры.</span><span class="sxs-lookup"><span data-stu-id="d5279-131">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="d5279-132">Перейдите в раздел **Retail и Commerce \> Настройка Headquarters \> Параметры \> Шаблоны сообщений электронной почты организации** и загрузите обновленный HTML в соответствующий шаблон сообщения электронной почты, имеющий код сообщения электронной почты **emailrecpt**.</span><span class="sxs-lookup"><span data-stu-id="d5279-132">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the email template that has the email ID **emailrecpt**.</span></span>

> [!NOTE]
> <span data-ttu-id="d5279-133">Параметры могут отличаться между поставщиками службы QR-кода и штрих-кода.</span><span class="sxs-lookup"><span data-stu-id="d5279-133">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="d5279-134">Поэтому обратитесь к поставщику услуг для подтверждения параметров, которые необходимо назначить значениям.</span><span class="sxs-lookup"><span data-stu-id="d5279-134">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d5279-135">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d5279-135">Additional resources</span></span>

[<span data-ttu-id="d5279-136">Отправка чеков по электронной почте из Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="d5279-136">Send email receipts from Modern POS (MPOS)</span></span>](email-receipts.md)

[<span data-ttu-id="d5279-137">Создание шаблонов сообщений электронной почты для событий проводок</span><span class="sxs-lookup"><span data-stu-id="d5279-137">Create email templates for transactional events</span></span>](email-templates-transactions.md)
