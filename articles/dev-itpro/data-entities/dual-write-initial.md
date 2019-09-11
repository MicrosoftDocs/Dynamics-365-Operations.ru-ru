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
ms.openlocfilehash: 1473c3bad55734d5f83ee3e4c1654921b872f3bb
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873136"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="38f8a-103">Порядок выполнения для первоначальной синхронизации Finance and Operations и Common Data Service</span><span class="sxs-lookup"><span data-stu-id="38f8a-103">Execution order for initial synchronization of Finance and Operations and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="38f8a-104">Перед использованием интеграции данных необходимо создать исходные данные, необходимые для клиентов, поставщиков и контактов.</span><span class="sxs-lookup"><span data-stu-id="38f8a-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="38f8a-105">Например, необходимо создать новый элемент **Группа поставщиков** и установить для ее параметра **Условия оплаты** значение **Net30**.</span><span class="sxs-lookup"><span data-stu-id="38f8a-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="38f8a-106">В этом случае, прежде чем пытаться создать элемент **Группа поставщиков**, необходимо убедиться, что **Net30** существует как в Microsoft Dynamics 365 for Finance and Operations, так и в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="38f8a-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both Microsoft Dynamics 365 for Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="38f8a-107">(В будущем Майкрософт выпустит функцию платформы двойной записи под названием "Начальная синхронизация". Эта функция будет делать одноразовую синхронизацию данных между Finance and Operations и Common Data Service в рамках настройки двойной записи.)</span><span class="sxs-lookup"><span data-stu-id="38f8a-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="38f8a-108">Майкрософт выпускает карту двойной записи для всех справочных данных, включая **Условия оплаты** (условия оплаты).</span><span class="sxs-lookup"><span data-stu-id="38f8a-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="38f8a-109">Если у вас уже есть исходные данные в одной системе, небольшая операция обновления для записи может вызвать двойную запись для этой записи.</span><span class="sxs-lookup"><span data-stu-id="38f8a-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="38f8a-110">Вы должны следовать следующему порядку приоритета и убедиться, что исходные данные доступны как в Finance and Operations, так и в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="38f8a-110">You must follow the following order of precedence and make sure that the initial data is available in both Finance and Operations and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="38f8a-111">Поставщик</span><span class="sxs-lookup"><span data-stu-id="38f8a-111">Vendor</span></span>

<span data-ttu-id="38f8a-112">Ниже представлен порядок выполнения для объекта **Поставщик**:</span><span class="sxs-lookup"><span data-stu-id="38f8a-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="38f8a-113">Группа поставщиков</span><span class="sxs-lookup"><span data-stu-id="38f8a-113">Vendor group</span></span>

    1. <span data-ttu-id="38f8a-114">Условия оплаты</span><span class="sxs-lookup"><span data-stu-id="38f8a-114">Terms of payment</span></span>

        1. <span data-ttu-id="38f8a-115">Платежные дни и строки</span><span class="sxs-lookup"><span data-stu-id="38f8a-115">Payment day and lines</span></span>
        2. <span data-ttu-id="38f8a-116">График оплаты</span><span class="sxs-lookup"><span data-stu-id="38f8a-116">Payment schedule</span></span>

2. <span data-ttu-id="38f8a-117">Метод платежа поставщикам</span><span class="sxs-lookup"><span data-stu-id="38f8a-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="38f8a-118">Клиент (Организация)</span><span class="sxs-lookup"><span data-stu-id="38f8a-118">Customer (Organization)</span></span>

<span data-ttu-id="38f8a-119">Ниже представлен порядок выполнения для объекта **Клиент**:</span><span class="sxs-lookup"><span data-stu-id="38f8a-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="38f8a-120">Группа клиентов</span><span class="sxs-lookup"><span data-stu-id="38f8a-120">Customer group</span></span>

    1. <span data-ttu-id="38f8a-121">Условия оплаты</span><span class="sxs-lookup"><span data-stu-id="38f8a-121">Terms of payment</span></span>

        1. <span data-ttu-id="38f8a-122">Платежные дни и строки</span><span class="sxs-lookup"><span data-stu-id="38f8a-122">Payment day and lines</span></span>
        2. <span data-ttu-id="38f8a-123">Платеж</span><span class="sxs-lookup"><span data-stu-id="38f8a-123">Payment</span></span> 

2. <span data-ttu-id="38f8a-124">Способ оплаты клиента</span><span class="sxs-lookup"><span data-stu-id="38f8a-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="38f8a-125">Контакт (Физическое лицо)</span><span class="sxs-lookup"><span data-stu-id="38f8a-125">Contact (Person)</span></span>

<span data-ttu-id="38f8a-126">Ниже представлен порядок выполнения для объекта **Контакт**:</span><span class="sxs-lookup"><span data-stu-id="38f8a-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="38f8a-127">Заказчик</span><span class="sxs-lookup"><span data-stu-id="38f8a-127">Customer</span></span>
2. <span data-ttu-id="38f8a-128">Поставщик</span><span class="sxs-lookup"><span data-stu-id="38f8a-128">Vendor</span></span>
