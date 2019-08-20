---
title: Порядок выполнения для первоначальной синхронизации Finance and Operations и Common Data Service
description: Эта тема определяет порядок синхронизации, который необходимо соблюдать для создания исходных данных.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797306"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="525fb-103">Порядок выполнения для первоначальной синхронизации Finance and Operations и Common Data Service</span><span class="sxs-lookup"><span data-stu-id="525fb-103">Execution order for initial sychronization of Finance and Operations and Common Data Service</span></span>

<span data-ttu-id="525fb-104">Перед использованием интеграции данных необходимо создать исходные данные, необходимые для клиентов, поставщиков и контактов.</span><span class="sxs-lookup"><span data-stu-id="525fb-104">Before you use data integration, you must create the initial data required for customers, vendors and contacts.</span></span> <span data-ttu-id="525fb-105">Например, если вы хотите создать новый элемент **Группа поставщиков** и установить для него **Условия оплаты** как **Net30**, то перед попыткой создать элемент **Группа поставщиков** необходимо убедиться, что **Net30** существует как в Finance and Operations, так и в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="525fb-105">For example, if you want to create a new **Vendor group** item and set its **Terms of Payment** as **Net30**, then before you attempt to create the **Vendor group** item you need to make sure that **Net30** exists in both Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="525fb-106">(В будущем мы выпустим функцию платформы двойной записи под названием **Начальная синхронизация**. Она будет делать одноразовую синхронизацию данных между Finance and Operations и Common Data Service в рамках настройки двойной записи.)</span><span class="sxs-lookup"><span data-stu-id="525fb-106">(In the future, we will release a  dual-write platform functionality called **Initial Sync**. It will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

<span data-ttu-id="525fb-107">Советы. Мы выпускаем карту двойной записи для всех справочных данных, включая **Условия оплаты** (Условия оплаты).</span><span class="sxs-lookup"><span data-stu-id="525fb-107">Tips: We are releasing a dual-write map for all reference data including **Terms of Payment** (Payment Terms).</span></span> <span data-ttu-id="525fb-108">Если у вас уже есть исходные данные в одной системе, небольшая операция обновления для записи может вызвать двойную запись для этой записи.</span><span class="sxs-lookup"><span data-stu-id="525fb-108">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span> 

<span data-ttu-id="525fb-109">Вы должны следовать следующему порядку приоритета и убедиться, что исходные данные доступны как в Finance and Operations, так и в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="525fb-109">You must follow the following order of precedence and make sure that the initial data is available on both Finance and Operations and Common Data Service.</span></span>   

## <a name="vendor"></a><span data-ttu-id="525fb-110">Поставщик</span><span class="sxs-lookup"><span data-stu-id="525fb-110">Vendor</span></span>

<span data-ttu-id="525fb-111">Порядок выполнения для поставщика:</span><span class="sxs-lookup"><span data-stu-id="525fb-111">The order of execution for Vendor is:</span></span>

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a><span data-ttu-id="525fb-112">Клиент (Организация)</span><span class="sxs-lookup"><span data-stu-id="525fb-112">Customer (Organization)</span></span>

<span data-ttu-id="525fb-113">Порядок выполнения для клиента:</span><span class="sxs-lookup"><span data-stu-id="525fb-113">The order of execution for Customer is:</span></span>

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a><span data-ttu-id="525fb-114">Контакт (Физическое лицо)</span><span class="sxs-lookup"><span data-stu-id="525fb-114">Contact (Person)</span></span>

<span data-ttu-id="525fb-115">Порядок выполнения для контакта:</span><span class="sxs-lookup"><span data-stu-id="525fb-115">The order of execution for Contact is:</span></span>

```
Customer
Vendor               
```
