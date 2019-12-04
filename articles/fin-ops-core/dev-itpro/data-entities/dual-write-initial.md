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
ms.openlocfilehash: cf444ef1192fed3a6a49282da37374dd8c443356
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769645"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="c4e3e-103">Порядок выполнения для первоначальной синхронизации приложений Finance and Operations и Common Data Service</span><span class="sxs-lookup"><span data-stu-id="c4e3e-103">Execution order for initial synchronization of Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4e3e-104">Перед использованием интеграции данных необходимо создать исходные данные, необходимые для клиентов, поставщиков и контактов.</span><span class="sxs-lookup"><span data-stu-id="c4e3e-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="c4e3e-105">Например, необходимо создать новый элемент **Группа поставщиков** и установить для ее параметра **Условия оплаты** значение **Net30**.</span><span class="sxs-lookup"><span data-stu-id="c4e3e-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="c4e3e-106">В этом случае, прежде чем пытаться создать элемент **Группа поставщиков**, необходимо убедиться, что **Net30** существует как в приложении, так и в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="c4e3e-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both the application and Common Data Service.</span></span> <span data-ttu-id="c4e3e-107">(В будущем Майкрософт выпустит функцию платформы двойной записи под названием "Начальная синхронизация". Эта функция будет делать одноразовую синхронизацию данных между приложением и Common Data Service в рамках настройки двойной записи.)</span><span class="sxs-lookup"><span data-stu-id="c4e3e-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between the application and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="c4e3e-108">Майкрософт выпускает карту двойной записи для всех справочных данных, включая **Условия оплаты** (условия оплаты).</span><span class="sxs-lookup"><span data-stu-id="c4e3e-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="c4e3e-109">Если у вас уже есть исходные данные в одной системе, небольшая операция обновления для записи может вызвать двойную запись для этой записи.</span><span class="sxs-lookup"><span data-stu-id="c4e3e-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="c4e3e-110">Вы должны следовать следующему порядку приоритета и убедиться, что исходные данные доступны как в приложении, так и в Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="c4e3e-110">You must follow the following order of precedence and make sure that the initial data is available in the application and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="c4e3e-111">Поставщик</span><span class="sxs-lookup"><span data-stu-id="c4e3e-111">Vendor</span></span>

<span data-ttu-id="c4e3e-112">Ниже представлен порядок выполнения для объекта **Поставщик**:</span><span class="sxs-lookup"><span data-stu-id="c4e3e-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="c4e3e-113">Группа поставщиков</span><span class="sxs-lookup"><span data-stu-id="c4e3e-113">Vendor group</span></span>

    1. <span data-ttu-id="c4e3e-114">Условия оплаты</span><span class="sxs-lookup"><span data-stu-id="c4e3e-114">Terms of payment</span></span>

        1. <span data-ttu-id="c4e3e-115">Платежные дни и строки</span><span class="sxs-lookup"><span data-stu-id="c4e3e-115">Payment day and lines</span></span>
        2. <span data-ttu-id="c4e3e-116">График оплаты</span><span class="sxs-lookup"><span data-stu-id="c4e3e-116">Payment schedule</span></span>

2. <span data-ttu-id="c4e3e-117">Метод платежа поставщикам</span><span class="sxs-lookup"><span data-stu-id="c4e3e-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="c4e3e-118">Клиент (Организация)</span><span class="sxs-lookup"><span data-stu-id="c4e3e-118">Customer (Organization)</span></span>

<span data-ttu-id="c4e3e-119">Ниже представлен порядок выполнения для объекта **Клиент**:</span><span class="sxs-lookup"><span data-stu-id="c4e3e-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="c4e3e-120">Группа клиентов</span><span class="sxs-lookup"><span data-stu-id="c4e3e-120">Customer group</span></span>

    1. <span data-ttu-id="c4e3e-121">Условия оплаты</span><span class="sxs-lookup"><span data-stu-id="c4e3e-121">Terms of payment</span></span>

        1. <span data-ttu-id="c4e3e-122">Платежные дни и строки</span><span class="sxs-lookup"><span data-stu-id="c4e3e-122">Payment day and lines</span></span>
        2. <span data-ttu-id="c4e3e-123">Платеж</span><span class="sxs-lookup"><span data-stu-id="c4e3e-123">Payment</span></span> 

2. <span data-ttu-id="c4e3e-124">Способ оплаты клиента</span><span class="sxs-lookup"><span data-stu-id="c4e3e-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="c4e3e-125">Контакт (Физическое лицо)</span><span class="sxs-lookup"><span data-stu-id="c4e3e-125">Contact (Person)</span></span>

<span data-ttu-id="c4e3e-126">Ниже представлен порядок выполнения для объекта **Контакт**:</span><span class="sxs-lookup"><span data-stu-id="c4e3e-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="c4e3e-127">Заказчик</span><span class="sxs-lookup"><span data-stu-id="c4e3e-127">Customer</span></span>
2. <span data-ttu-id="c4e3e-128">Поставщик</span><span class="sxs-lookup"><span data-stu-id="c4e3e-128">Vendor</span></span>
