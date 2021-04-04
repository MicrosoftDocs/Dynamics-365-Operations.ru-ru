---
title: Настройте среду разработки электронной коммерции для отладки на виртуальной машине сервера Retail уровня 1
description: В этом разделе объясняется, как настроить среду разработки электронной коммерции для отладки на виртуальной машине (VM) сервера Retail уровня 1.
author: Reza-Assadi
manager: AnnBe
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
ms.openlocfilehash: 35380a559a4f1b22bdf04ff25cb2bbfc51aff45b
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585492"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a><span data-ttu-id="801b9-103">Настройте среду разработки электронной коммерции для отладки на виртуальной машине сервера Retail уровня 1</span><span class="sxs-lookup"><span data-stu-id="801b9-103">Set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="801b9-104">В этом разделе объясняется, как настроить среду разработки электронной коммерции для отладки на виртуальной машине (VM) сервера Retail уровня 1.</span><span class="sxs-lookup"><span data-stu-id="801b9-104">This topic explains how to set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine (VM).</span></span>

## <a name="description"></a><span data-ttu-id="801b9-105">описание</span><span class="sxs-lookup"><span data-stu-id="801b9-105">Description</span></span>

<span data-ttu-id="801b9-106">Среды Microsoft Dynamics 365 Commerce уровня 1 обычно развертываются для разработки расширений для Commerce Runtime (CRT) и POS.</span><span class="sxs-lookup"><span data-stu-id="801b9-106">Microsoft Dynamics 365 Commerce Tier 1 environments are typically deployed for Commerce runtime (CRT) and point of sale (POS) extension development.</span></span> <span data-ttu-id="801b9-107">Они являются автономными средами.</span><span class="sxs-lookup"><span data-stu-id="801b9-107">They are standalone environments.</span></span> <span data-ttu-id="801b9-108">Из-за природы архитектуры программного обеспечения как услуга (SaaS) они не включают в себя компоненты электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="801b9-108">Because of the software as a service (SaaS) nature of the architecture, they don't include e-commerce components.</span></span>

<span data-ttu-id="801b9-109">В некоторых сценариях может возникнуть необходимость тестировать вызовы расширений в среде уровня 1, чтобы можно было отлаживать расширения из компонентов электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="801b9-109">In some scenarios, you might want to test calls to extensions in a Tier 1 environment, so that you can debug extensions from e-commerce components.</span></span> <span data-ttu-id="801b9-110">Общие инструкции см. в [Отладка в среде развертывания Commerce уровня 1](../e-commerce-extensibility/debug-tier-1.md).</span><span class="sxs-lookup"><span data-stu-id="801b9-110">For general instructions, see [Debug against a Tier 1 Commerce development environment](../e-commerce-extensibility/debug-tier-1.md).</span></span>

<span data-ttu-id="801b9-111">При отладке в среде уровня 1, поскольку сайт теперь выполняет вызов другого сервера Retail, вызовы между серверами могут вызывать различные ошибки, связанные с политикой безопасности содержимого.</span><span class="sxs-lookup"><span data-stu-id="801b9-111">When you debug against a Tier 1 environment, because the site is now calling a different Retail Server, cross-server calls might cause various errors that are related to the content security policy.</span></span>

<span data-ttu-id="801b9-112">На следующем рисунке показан пример ошибки, которая может возникнуть, когда выбран вариант на странице сведений о продукте.</span><span class="sxs-lookup"><span data-stu-id="801b9-112">The following illustration shows an example of an error that might occur when a variant is selected on a product details page.</span></span>

![Ошибка при выборе варианта на странице сведений о продукте](media/unhandled-rejection-error.jpg)

<span data-ttu-id="801b9-114">На следующем рисунке показан пример подобной ошибки в средствах отладчика обозревателя (Средства для разработчиков F12).</span><span class="sxs-lookup"><span data-stu-id="801b9-114">The following illustration shows an example of a similar error in a browser's debugger tools (F12 Developer Tools).</span></span> <span data-ttu-id="801b9-115">В сообщении об ошибке говорится о нарушении директивы политики безопасности содержимого.</span><span class="sxs-lookup"><span data-stu-id="801b9-115">The error message mentions violation of the content security policy directive.</span></span>

![Ошибка средств отладчика](media/debugger-tools-error.JPG)

## <a name="resolution"></a><span data-ttu-id="801b9-117">Приказ</span><span class="sxs-lookup"><span data-stu-id="801b9-117">Resolution</span></span>

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a><span data-ttu-id="801b9-118">Отключите политику безопасности содержимого для сайта в конструкторе сайтов Commerce</span><span class="sxs-lookup"><span data-stu-id="801b9-118">Disable the content security policy for the site in Commerce site builder</span></span>

1. <span data-ttu-id="801b9-119">Выберите сайт, с которым вы работаете в данный момент.</span><span class="sxs-lookup"><span data-stu-id="801b9-119">Select the site that you're working on.</span></span>
1. <span data-ttu-id="801b9-120">Выберите **Параметры**, затем выберите **Расширения**.</span><span class="sxs-lookup"><span data-stu-id="801b9-120">Select **Settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="801b9-121">На вкладке **Политика безопасности содержимого** выберите **отключить политику безопасности содержимого**.</span><span class="sxs-lookup"><span data-stu-id="801b9-121">On the **Content security policy** tab, select **Disable content security policy**.</span></span>
1. <span data-ttu-id="801b9-122">Выберите **Сохранить и опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="801b9-122">Select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="801b9-123">Вход "бизнес-потребитель" (B2C) не работает в локальной среде разработки.</span><span class="sxs-lookup"><span data-stu-id="801b9-123">Business-to-consumer (B2C) sign-in won't work in a local development environment.</span></span> <span data-ttu-id="801b9-124">Однако можно использовать гостевые оформления заказа или создать макет страницы, чтобы имитировать вход пользователя в систему по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="801b9-124">However, you can use guest checkouts or build page mocks to simulate a user sign-in as required.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="801b9-125">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="801b9-125">Additional resources</span></span>

[<span data-ttu-id="801b9-126">Начало работы с разработкой расширяемости канала продаж через Интернет для электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="801b9-126">Get started with e-commerce online extensibility development</span></span>](../e-commerce-extensibility/sdk-getting-started.md)

[<span data-ttu-id="801b9-127">Управление политикой безопасности содержимого (CSP) на сайте электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="801b9-127">Manage content security policy (CSP) on e-commerce site</span></span>](../manage-csp.md)
