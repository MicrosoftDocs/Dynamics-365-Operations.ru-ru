---
title: Порядок выполнения для первоначальной синхронизации приложений Finance and Operations и Common Data Service
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
ms.openlocfilehash: 3110cb809558d168e9d97f640701b249caf73f6c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184516"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="31eff-103">Порядок выполнения для первоначальной синхронизации приложений Finance and Operations и Common Data Service</span><span class="sxs-lookup"><span data-stu-id="31eff-103">Execution order for initial synchronization of Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="31eff-104">Перед использованием интеграции данных необходимо создать исходные данные, необходимые для клиентов, поставщиков и контактов.</span><span class="sxs-lookup"><span data-stu-id="31eff-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="31eff-105">Например, необходимо создать новый элемент **Группа поставщиков** и установить для ее параметра **Условия оплаты** значение **Net30**.</span><span class="sxs-lookup"><span data-stu-id="31eff-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="31eff-106">В этом случае, прежде чем пытаться создать элемент **Группа поставщиков**, необходимо убедиться, что **Net30** существует как в приложении, так и в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="31eff-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both the application and Common Data Service.</span></span> <span data-ttu-id="31eff-107">(В будущем Майкрософт выпустит функцию платформы двойной записи под названием "Начальная синхронизация". Эта функция будет делать одноразовую синхронизацию данных между приложением и Common Data Service в рамках настройки двойной записи.)</span><span class="sxs-lookup"><span data-stu-id="31eff-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between the application and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="31eff-108">Майкрософт выпускает карту двойной записи для всех справочных данных, включая **Условия оплаты** (условия оплаты).</span><span class="sxs-lookup"><span data-stu-id="31eff-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="31eff-109">Если у вас уже есть исходные данные в одной системе, небольшая операция обновления для записи может вызвать двойную запись для этой записи.</span><span class="sxs-lookup"><span data-stu-id="31eff-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="31eff-110">Вы должны следовать следующему порядку приоритета и убедиться, что исходные данные доступны как в приложении, так и в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="31eff-110">You must follow the following order of precedence and make sure that the initial data is available in the application and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="31eff-111">Поставщик</span><span class="sxs-lookup"><span data-stu-id="31eff-111">Vendor</span></span>

<span data-ttu-id="31eff-112">Ниже представлен порядок выполнения для объекта **Поставщик**:</span><span class="sxs-lookup"><span data-stu-id="31eff-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="31eff-113">Группа поставщиков</span><span class="sxs-lookup"><span data-stu-id="31eff-113">Vendor group</span></span>

    1. <span data-ttu-id="31eff-114">Условия оплаты</span><span class="sxs-lookup"><span data-stu-id="31eff-114">Terms of payment</span></span>

        1. <span data-ttu-id="31eff-115">Платежные дни и строки</span><span class="sxs-lookup"><span data-stu-id="31eff-115">Payment day and lines</span></span>
        2. <span data-ttu-id="31eff-116">График оплаты</span><span class="sxs-lookup"><span data-stu-id="31eff-116">Payment schedule</span></span>

2. <span data-ttu-id="31eff-117">Метод платежа поставщикам</span><span class="sxs-lookup"><span data-stu-id="31eff-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="31eff-118">Клиент (Организация)</span><span class="sxs-lookup"><span data-stu-id="31eff-118">Customer (Organization)</span></span>

<span data-ttu-id="31eff-119">Ниже представлен порядок выполнения для объекта **Клиент**:</span><span class="sxs-lookup"><span data-stu-id="31eff-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="31eff-120">Группа клиентов</span><span class="sxs-lookup"><span data-stu-id="31eff-120">Customer group</span></span>

    1. <span data-ttu-id="31eff-121">Условия оплаты</span><span class="sxs-lookup"><span data-stu-id="31eff-121">Terms of payment</span></span>

        1. <span data-ttu-id="31eff-122">Платежные дни и строки</span><span class="sxs-lookup"><span data-stu-id="31eff-122">Payment day and lines</span></span>
        2. <span data-ttu-id="31eff-123">Платеж</span><span class="sxs-lookup"><span data-stu-id="31eff-123">Payment</span></span> 

2. <span data-ttu-id="31eff-124">Способ оплаты клиента</span><span class="sxs-lookup"><span data-stu-id="31eff-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="31eff-125">Контакт (Физическое лицо)</span><span class="sxs-lookup"><span data-stu-id="31eff-125">Contact (Person)</span></span>

<span data-ttu-id="31eff-126">Ниже представлен порядок выполнения для объекта **Контакт**:</span><span class="sxs-lookup"><span data-stu-id="31eff-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="31eff-127">Заказчик</span><span class="sxs-lookup"><span data-stu-id="31eff-127">Customer</span></span>
2. <span data-ttu-id="31eff-128">Поставщик</span><span class="sxs-lookup"><span data-stu-id="31eff-128">Vendor</span></span>
