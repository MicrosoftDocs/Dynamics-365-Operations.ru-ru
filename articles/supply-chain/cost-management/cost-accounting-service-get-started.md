---
title: Начало работы со службой учета затрат
description: В этом разделе приведены сведения о лицензировании и инструкции по установке для службы учета затрат.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: cbbce7eaac264973bf0b95ad5175bf70ed2b4ae9
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276956"
---
# <a name="get-started-with-the-cost-accounting-service"></a><span data-ttu-id="5e7d4-103">Начало работы со службой учета затрат</span><span class="sxs-lookup"><span data-stu-id="5e7d4-103">Get started with the cost accounting service</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="5e7d4-104">Функциональность, описанная в этой теме, доступна в рамках частного предварительного выпуска.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="5e7d4-105">Содержимое этого раздела и функции, которые в нем описываются, могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="5e7d4-106">Дополнительные сведения о предварительных выпусках см. в разделе [Вопросы и ответы по обновлениям службы с одной версией](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="5e7d4-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="5e7d4-107">Служба учета затрат позволяет выполнить несколько учетов запасов в настроенных книгах учета затрат.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="5e7d4-108">Каждая книга учета затрат связывается с *соглашением*.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="5e7d4-109">Соглашение — это совокупность следующих типов политик учета:</span><span class="sxs-lookup"><span data-stu-id="5e7d4-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="5e7d4-110">Объект затрат</span><span class="sxs-lookup"><span data-stu-id="5e7d4-110">Cost object</span></span>
- <span data-ttu-id="5e7d4-111">Базис входящих измерений</span><span class="sxs-lookup"><span data-stu-id="5e7d4-111">Input measurement basis</span></span>
- <span data-ttu-id="5e7d4-112">Предположения потока затрат</span><span class="sxs-lookup"><span data-stu-id="5e7d4-112">Cost flow assumption</span></span>
- <span data-ttu-id="5e7d4-113">Элемент затрат</span><span class="sxs-lookup"><span data-stu-id="5e7d4-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="5e7d4-114">Даже после включения службы учета затрат можно по-прежнему выполнить учет запасов в Microsoft Dynamics 365 Supply Chain Management, как обычно.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="5e7d4-115">Служба учета затрат является надстройкой.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="5e7d4-116">Чтобы сделать ее функции доступными, необходимо установить ее из Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="5e7d4-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="5e7d4-117">Таким образом, ее можно оценить в тестовой среде, прежде чем включать ее в производственной среде.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="5e7d4-118">Служба учета затрат в настоящее время не поддерживает все функции управления затратами, встроенные в Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="5e7d4-119">Таким образом, важно оценить, будет ли набор функций, доступный в данный момент, удовлетворять вашим требованиям.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="licensing"></a><span data-ttu-id="5e7d4-120">Лицензирование</span><span class="sxs-lookup"><span data-stu-id="5e7d4-120">Licensing</span></span>

<span data-ttu-id="5e7d4-121">Служба учета затрат лицензируется вместе со стандартными функциями учета запасов, которые доступны для Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-121">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="5e7d4-122">Вам не придется покупать дополнительную лицензию для использования службы учета затрат.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-122">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><span data-ttu-id="5e7d4-123">Установка надстройки</span><span class="sxs-lookup"><span data-stu-id="5e7d4-123">Install the add-in</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5e7d4-124">Для использования службы учета затрат необходима среда с поддержкой LCS с высокой доступностью (не среда OneBox), и должна использоваться Dynamics 365 Supply Chain Management версии 10.0.11 или более новая.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-124">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="5e7d4-125">Чтобы использовать службу учета затрат, установите надстройку службы учета затрат для Supply Chain Management, как описано в следующей процедуре.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-125">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="5e7d4-126">Войдите в LCS.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-126">Sign in to LCS.</span></span>

1. <span data-ttu-id="5e7d4-127">Перейдите к разделу **Управление компонентами предварительной версии**.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-127">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="5e7d4-128">Выберите знак "плюс (**+**).</span><span class="sxs-lookup"><span data-stu-id="5e7d4-128">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="5e7d4-129">В поле **Код** введите свой дополнительный ключ бета-тестера для службы учета затрат.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-129">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="5e7d4-130">(Вы должны были получить ключ по электронной почте.)</span><span class="sxs-lookup"><span data-stu-id="5e7d4-130">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="5e7d4-131">Выберите **Разблокировать**.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-131">Select **Unblock**.</span></span>

1. <span data-ttu-id="5e7d4-132">Откройте среду LCS, в которую необходимо добавить службу.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-132">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="5e7d4-133">Перейдите **Полные сведения**.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-133">Go to **Full details**.</span></span>

1. <span data-ttu-id="5e7d4-134">Перейдите на экспресс-вкладку **Надстройки среды**.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-134">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="5e7d4-135">Выберите **Установить новую надстройку**.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-135">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="5e7d4-136">Выберите **Служба учета затрат**.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-136">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="5e7d4-137">Следуйте указаниям руководства по установке и примите условия и положения.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-137">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="5e7d4-138">Выберите **Установить**.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-138">Select **Install**.</span></span>

1. <span data-ttu-id="5e7d4-139">На экспресс-вкладке **Надстройки среды** должно быть видно, что устанавливается служба учета затрат.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-139">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="5e7d4-140">Через несколько минут этот статус должен измениться с **Устанавливается** на **Установлено**.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-140">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="5e7d4-141">(Возможно, потребуется обновить страницу, чтобы увидеть это изменение.) На этом этапе служба учета затрат готова к использованию.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-141">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="5e7d4-142">Настройка интеграции</span><span class="sxs-lookup"><span data-stu-id="5e7d4-142">Set up the integration</span></span>

<span data-ttu-id="5e7d4-143">Чтобы настроить интеграцию между службой учета затрат и Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="5e7d4-143">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="5e7d4-144">Перейдите в раздел **Администрирование системы > Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-144">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="5e7d4-145">Выберите **Проверить наличие обновлений**.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-145">Select **Check for updates**.</span></span>

1. <span data-ttu-id="5e7d4-146">Откройте вкладку **Все** и выполните поиск компонента с именем *Служба учета затрат*.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-146">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="5e7d4-147">Выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-147">Select **Enable now**.</span></span>

1. <span data-ttu-id="5e7d4-148">Перейдите к разделу **управлению затратами > Служба учета затрат > Настройка > Параметры службы учета затрат > Параметры интеграции**.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-148">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="5e7d4-149">В поле **Код приложения** введите следующий код:</span><span class="sxs-lookup"><span data-stu-id="5e7d4-149">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="5e7d4-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="5e7d4-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="5e7d4-151">В поле **Конечная точка для службы данных** введите следующий URL-адрес:</span><span class="sxs-lookup"><span data-stu-id="5e7d4-151">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="5e7d4-152">В поле **Конечная точка службы учета затрат** введите следующий URL-адрес:</span><span class="sxs-lookup"><span data-stu-id="5e7d4-152">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="5e7d4-153">Теперь служба учета затрат готова к использованию.</span><span class="sxs-lookup"><span data-stu-id="5e7d4-153">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="5e7d4-154">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5e7d4-154">Related resources</span></span>

[<span data-ttu-id="5e7d4-155">Домашняя страница службы учета затрат</span><span class="sxs-lookup"><span data-stu-id="5e7d4-155">Cost accounting service home page</span></span>](cost-accounting-service-home.md)