---
title: Записи клиентов не отображаются в Commerce headquarters
description: В этом разделе содержатся указания по устранению неполадок, которые могут помочь, когда записи о клиентах не появляются сразу в Commerce Headquarters.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: b8d065dd104df616ba8f10f7813e74c900fdcf77
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018490"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a><span data-ttu-id="d4efc-103">Записи клиентов не отображаются в Commerce headquarters</span><span class="sxs-lookup"><span data-stu-id="d4efc-103">Customer records don't appear in Commerce headquarters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d4efc-104">В этом разделе содержатся указания по устранению неполадок, которые могут помочь, когда записи о клиентах не появляются сразу в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="d4efc-104">This topic provides troubleshooting guidance that can help when customer records don't immediately appear in Commerce headquarters.</span></span>

## <a name="description"></a><span data-ttu-id="d4efc-105">описание</span><span class="sxs-lookup"><span data-stu-id="d4efc-105">Description</span></span>

<span data-ttu-id="d4efc-106">При создании новой записи клиента с помощью потока регистрации в витрине электронной коммерции соответствующая запись клиента сразу же отображается в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="d4efc-106">When you create a new customer record by using the sign-up flow in the e-commerce storefront, the corresponding customer record doesn't immediately appear in Commerce headquarters.</span></span>

## <a name="resolution"></a><span data-ttu-id="d4efc-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="d4efc-107">Resolution</span></span>

### <a name="disable-customer-creation-in-async-mode"></a><span data-ttu-id="d4efc-108">Отключение создания клиентов в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="d4efc-108">Disable customer creation in async mode</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d4efc-109">Если вы отключите создание асинхронного клиента, это может повлиять на производительность системы, поскольку создание каждой записи приведет к созданию запроса в реальном времени для Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="d4efc-109">If you disable asynchronous customer creation, system performance could be affected, because creation of each record will produce a real-time request to Commerce headquarters.</span></span> <span data-ttu-id="d4efc-110">Кроме того, если Commerce headquarters не работает (например, во время потоков обслуживания), все новые потоки создания клиентов создадут ошибки.</span><span class="sxs-lookup"><span data-stu-id="d4efc-110">In addition, if Commerce headquarters is down (for example, during servicing flows), any new customer creation flows will produce errors.</span></span>

<span data-ttu-id="d4efc-111">Чтобы отключить создание клиентов в асинхронном режиме в Commerce headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d4efc-111">To disable customer creation in async mode in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d4efc-112">Перейдите в раздел **Retail и Commerce \> Настройка канала \> Настройка интернет-магазина \> Профили функциональности**.</span><span class="sxs-lookup"><span data-stu-id="d4efc-112">Go to **Retail and Commerce \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="d4efc-113">Если вы еще не используете профиль функциональности для своего интернет-канала, создайте его.</span><span class="sxs-lookup"><span data-stu-id="d4efc-113">If you aren't already using a functionality profile for your online channel, create one.</span></span>
1. <span data-ttu-id="d4efc-114">Убедитесь, что для параметра **Создание клиента в асинхронном режиме** выбрано значение **нет**.</span><span class="sxs-lookup"><span data-stu-id="d4efc-114">Make sure that the **Create customer in async mode** option is set to **No**.</span></span>
1. <span data-ttu-id="d4efc-115">Перейдите в раздел **Retail и Commerce \> Каналы \> Интернет-магазины**.</span><span class="sxs-lookup"><span data-stu-id="d4efc-115">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="d4efc-116">Выберите интернет-магазин, для которого требуется отключить создание асинхронного клиента.</span><span class="sxs-lookup"><span data-stu-id="d4efc-116">Select the online store to disable asynchronous customer creation for.</span></span>
1. <span data-ttu-id="d4efc-117">На вкладке **Общие** убедитесь, что в поле **Профиль функциональности** установлен профиль функциональности, используемый для интернет-канала.</span><span class="sxs-lookup"><span data-stu-id="d4efc-117">On the **General** tab, make sure that the **Functionality profile** field is set to the functionality profile that you're using for your online channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d4efc-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d4efc-118">Additional resources</span></span>

[<span data-ttu-id="d4efc-119">Настройка клиента B2C в Commerce</span><span class="sxs-lookup"><span data-stu-id="d4efc-119">Setup a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)
