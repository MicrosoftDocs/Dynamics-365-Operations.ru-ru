---
title: Устранение неполадок с соединитель платежей Dynamics 365 для Adyen
description: В этом разделе содержатся указания по устранению неполадок, которые могут помочь в обеспечении технической поддержки при возникновении проблем с соединитель платежей Microsoft Dynamics 365 для Adyen.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c779997d530d60f945bee19ee09bdabbff121fa6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801827"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="65cf4-103">Устранение неполадок с соединитель платежей Dynamics 365 для Adyen</span><span class="sxs-lookup"><span data-stu-id="65cf4-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="65cf4-104">В этом разделе содержатся указания по устранению неполадок, которые могут помочь в обеспечении технической поддержки при возникновении проблем с соединитель платежей Microsoft Dynamics 365 для Adyen.</span><span class="sxs-lookup"><span data-stu-id="65cf4-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="65cf4-105">описание</span><span class="sxs-lookup"><span data-stu-id="65cf4-105">Description</span></span>

<span data-ttu-id="65cf4-106">У вас есть вопросы с соединителем платежей Dynamics 365 для Adyen в следующих областях, и вам необходима поддержка рабочей группы Adyen:</span><span class="sxs-lookup"><span data-stu-id="65cf4-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="65cf4-107">Конфигурация POS, Modern POS (MPOS), центра обработки звонков или Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="65cf4-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="65cf4-108">Номер ссылки поставщика службы платежа Adyen (PSP) (например, если имеются вопросы о отклонениях, в том числе при ручном вводе ключа \[MKE\])</span><span class="sxs-lookup"><span data-stu-id="65cf4-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="65cf4-109">Все, что не работает в испытательной или реальной среде продавца</span><span class="sxs-lookup"><span data-stu-id="65cf4-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="65cf4-110">Приказ</span><span class="sxs-lookup"><span data-stu-id="65cf4-110">Resolution</span></span>

<span data-ttu-id="65cf4-111">Используйте следующий шаблон сообщения электронной почты для запуска процесса поддержки с помощью рабочей группы Adyen.</span><span class="sxs-lookup"><span data-stu-id="65cf4-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="65cf4-112">Для ускорения устранения неполадок убедитесь, что в сообщении электронной почты содержатся все необходимые сведения.</span><span class="sxs-lookup"><span data-stu-id="65cf4-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="65cf4-113">Поле</span><span class="sxs-lookup"><span data-stu-id="65cf4-113">Field</span></span>        | <span data-ttu-id="65cf4-114">значение</span><span class="sxs-lookup"><span data-stu-id="65cf4-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="65cf4-115">по</span><span class="sxs-lookup"><span data-stu-id="65cf4-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="65cf4-116">Копия</span><span class="sxs-lookup"><span data-stu-id="65cf4-116">Cc</span></span>           | |
| <span data-ttu-id="65cf4-117">Строка темы</span><span class="sxs-lookup"><span data-stu-id="65cf4-117">Subject line</span></span> | <span data-ttu-id="65cf4-118">Запрос на поддержку Microsoft Dynamics</span><span class="sxs-lookup"><span data-stu-id="65cf4-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="65cf4-119">Текст</span><span class="sxs-lookup"><span data-stu-id="65cf4-119">Body</span></span>         | <p><span data-ttu-id="65cf4-120">Добрый день,</span><span class="sxs-lookup"><span data-stu-id="65cf4-120">Hi Support,</span></span></p><p><span data-ttu-id="65cf4-121">Предоставьте поддержку по следующей проблеме:</span><span class="sxs-lookup"><span data-stu-id="65cf4-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="65cf4-122">Счет торговца</span><span class="sxs-lookup"><span data-stu-id="65cf4-122">Merchant account</span></span></li><li><span data-ttu-id="65cf4-123">Среда (тест/произв.)</span><span class="sxs-lookup"><span data-stu-id="65cf4-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="65cf4-124">Канал (POS/центр обработки вызовов/электронная коммерция Commerce)</span><span class="sxs-lookup"><span data-stu-id="65cf4-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="65cf4-125">Номер ссылки PSP, если проблема связана с конкретной проводкой (вы можете найти номер ссылки PSP в чеке, в области клиента Adyen или в меню проводки на POS).</span><span class="sxs-lookup"><span data-stu-id="65cf4-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="65cf4-126">Снимок экрана или фотография сообщения об ошибке, если это применимо</span><span class="sxs-lookup"><span data-stu-id="65cf4-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="65cf4-127">Журналы средства просмотра событий (в формате .txt)</span><span class="sxs-lookup"><span data-stu-id="65cf4-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="65cf4-128">Описание проблемы и шаги по устранению неполадок, которые вы пытались выполнить</span><span class="sxs-lookup"><span data-stu-id="65cf4-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="65cf4-129">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="65cf4-129">Additional resources</span></span>

[<span data-ttu-id="65cf4-130">Прием платежей с соединителем Adyen для Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="65cf4-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="65cf4-131">Соединитель платежей Dynamics 365 для Adyen</span><span class="sxs-lookup"><span data-stu-id="65cf4-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="65cf4-132">Настройка соединителя платежей Adyen для Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="65cf4-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
