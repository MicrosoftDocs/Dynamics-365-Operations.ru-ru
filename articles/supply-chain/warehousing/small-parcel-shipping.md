---
title: Отгрузка небольших посылок
description: В этом разделе содержится информация о функции отгрузки небольших посылок (SPS). Эта функция позволяет Microsoft Dynamics 365 Supply Chain Management отправлять сведения о упакованном контейнере перевозчику, а затем получать этикетку отгрузки, ставку отгрузки и номер отслеживания от этого перевозчика.
author: Mirzaab
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3969ee6b46f38fe2650881fb0183c60aadce6c8a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831178"
---
# <a name="small-parcel-shipping"></a><span data-ttu-id="60b63-104">Отгрузка небольших посылок</span><span class="sxs-lookup"><span data-stu-id="60b63-104">Small parcel shipping</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="60b63-105">Функция отгрузки небольших посылок (SPS) позволяет Microsoft Dynamics 365 Supply Chain Management взаимодействовать непосредственно с перевозчиками, представляя основу для связи через API-интерфейсы перевозчиков.</span><span class="sxs-lookup"><span data-stu-id="60b63-105">The small parcel shipping (SPS) feature enables Microsoft Dynamics 365 Supply Chain Management to interact directly with shipping carriers by providing a framework for communication through carrier APIs.</span></span> <span data-ttu-id="60b63-106">Эта функция полезна при отгрузке отдельных заказов на продажу через коммерческих перевозчиков вместо использования отправки в контейнерах или отгрузки меньше грузоподъемности грузовика (LTL).</span><span class="sxs-lookup"><span data-stu-id="60b63-106">This functionality is useful when you're shipping individual sales orders via commercial shipping carriers instead of using container shipping or less-than-truckload (LTL) shipping.</span></span>

<span data-ttu-id="60b63-107">Функция SPS взаимодействует с перевозчиком, осуществляющим доставку, через выделенный *механизм ставок*.</span><span class="sxs-lookup"><span data-stu-id="60b63-107">The SPS feature interacts with your shipping carrier through a dedicated *rate engine*.</span></span> <span data-ttu-id="60b63-108">Ваша организация должна разработать этот механизм ставок совместно со службой перевозчика или центра перевозок.</span><span class="sxs-lookup"><span data-stu-id="60b63-108">Your organization must develop this rate engine in collaboration with your carrier or carrier hub service.</span></span> <span data-ttu-id="60b63-109">Механизм ставок позволяет Supply Chain Management отправлять сведения о упакованном контейнере вашему перевозчику, а затем получать этикетку отгрузки, ставку отгрузки и номер отслеживания от этого перевозчика.</span><span class="sxs-lookup"><span data-stu-id="60b63-109">The rate engine enables Supply Chain Management to submit details about a packed container to your carrier, and then receive a shipping label, shipping rate, and tracking number back from that carrier.</span></span>

<span data-ttu-id="60b63-110">Возвращаемая ставка отгрузки добавляется к соответствующему заказу на продажу в качестве накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="60b63-110">The shipping rate that is returned is added to the associated sales order as a miscellaneous charge.</span></span> <span data-ttu-id="60b63-111">Возвращаемая этикетка отгрузки может быть затем автоматически распечатана с помощью принтера, поддерживающего язык Zebra Programming Language (ZPL), и закреплена на отгрузке.</span><span class="sxs-lookup"><span data-stu-id="60b63-111">The shipping label that is returned can then automatically be printed by using a Zebra Programming Language (ZPL) printer and applied to the shipment.</span></span> <span data-ttu-id="60b63-112">Перевозчик отсканирует эту этикетку отгрузки при получении пакетов на вашем складе.</span><span class="sxs-lookup"><span data-stu-id="60b63-112">The carrier will scan this shipping label when it picks up the packages at your warehouse.</span></span>

## <a name="prepare-your-system-to-support-sps"></a><span data-ttu-id="60b63-113">Подготовка системы к поддержке SPS</span><span class="sxs-lookup"><span data-stu-id="60b63-113">Prepare your system to support SPS</span></span>

<span data-ttu-id="60b63-114">Прежде чем приступить к использованию функций SPS, необходимо включить функцию SPS в управлении функциями, добавить механизм ставок и настроить модули **Управление транспортировкой** и **Управление складом** для ее поддержки.</span><span class="sxs-lookup"><span data-stu-id="60b63-114">Before you can start to use SPS functionality, you must turn on the SPS feature in Feature management, add your rate engine, and set up the **Transportation management** and **Warehouse management** modules to support it.</span></span>

### <a name="turn-on-the-sps-feature"></a><span data-ttu-id="60b63-115">Включение функции SPS</span><span class="sxs-lookup"><span data-stu-id="60b63-115">Turn on the SPS feature</span></span>

<span data-ttu-id="60b63-116">Прежде чем использовать функцию SPS, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="60b63-116">Before you can use the SPS feature, it must be turned on in your system.</span></span> <span data-ttu-id="60b63-117">Администраторы могут использовать рабочую область [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса этой функции и ее включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="60b63-117">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="60b63-118">В этом случае функция указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="60b63-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="60b63-119">**Модуль:** *Управление транспортировкой*</span><span class="sxs-lookup"><span data-stu-id="60b63-119">**Module:** *Transportation management*</span></span>
- <span data-ttu-id="60b63-120">**Название компонента:** *Отгрузка небольших посылок*</span><span class="sxs-lookup"><span data-stu-id="60b63-120">**Feature name:** *Small parcel shipping*</span></span>

### <a name="deploy-and-set-up-rate-engines"></a><span data-ttu-id="60b63-121">Развертывание и настройка механизмов ставок</span><span class="sxs-lookup"><span data-stu-id="60b63-121">Deploy and set up rate engines</span></span>

<span data-ttu-id="60b63-122">Supply Chain Management не включает какие-либо механизмы ставок.</span><span class="sxs-lookup"><span data-stu-id="60b63-122">Supply Chain Management doesn't include any rate engines.</span></span> <span data-ttu-id="60b63-123">Необходимо получить или создать любые необходимые вам механизмы ставок, а затем добавить их в систему.</span><span class="sxs-lookup"><span data-stu-id="60b63-123">You must obtain or create any rate engines that you require, and then add them to your system.</span></span> <span data-ttu-id="60b63-124">Однако в Microsoft предусмотрен демонстрационный механизм ставок, который можно использовать для тестирования.</span><span class="sxs-lookup"><span data-stu-id="60b63-124">However, Microsoft provides a demo rate engine that you can use for testing.</span></span>

#### <a name="download-and-deploy-the-demo-rate-engine"></a><span data-ttu-id="60b63-125">Загрузка и развертывание демонстрационного механизма ставок</span><span class="sxs-lookup"><span data-stu-id="60b63-125">Download and deploy the demo rate engine</span></span>

<span data-ttu-id="60b63-126">Чтобы получить демонстрационный механизм ставок, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="60b63-126">Follow these steps to get the demo rate engine.</span></span>

1. <span data-ttu-id="60b63-127">В GitHub загрузите [библиотеку динамической компоновки (DLL) для демонстрационного механизма ставок](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span><span class="sxs-lookup"><span data-stu-id="60b63-127">On GitHub, download the [dynamic-link library (DLL) for the demo rate engine](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span></span>
1. <span data-ttu-id="60b63-128">На вашем сервере Supply Chain Management сохраните библиотеку DLL в папке **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin**.</span><span class="sxs-lookup"><span data-stu-id="60b63-128">On your Supply Chain Management server, save the DLL in the **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin** folder.</span></span>

#### <a name="create-and-deploy-functional-rate-engines"></a><span data-ttu-id="60b63-129">Создание и развертывание функциональных механизмов ставок</span><span class="sxs-lookup"><span data-stu-id="60b63-129">Create and deploy functional rate engines</span></span>

<span data-ttu-id="60b63-130">Сведения о создании и развертывании функциональных механизмов ставок для их использования в производственной или тестовой среде см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="60b63-130">For information about how to create and deploy functional rate engines so that they can be used in a production or test environment, see the following topics:</span></span>

- [<span data-ttu-id="60b63-131">Создание нового механизма управления транспортировкой</span><span class="sxs-lookup"><span data-stu-id="60b63-131">Create a new transportation management engine</span></span>](../transportation/create-new-transportation-management-engine.md)
- [<span data-ttu-id="60b63-132">Настройка механизмов управления транспортировкой</span><span class="sxs-lookup"><span data-stu-id="60b63-132">Set up transportation management engines</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

<span data-ttu-id="60b63-133">Дополнительные сведения о создании механизма ставок SPS см. в следующей записи блога: [Отгрузка небольших посылок: как использовать функцию отгрузки небольших посылок в Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span><span class="sxs-lookup"><span data-stu-id="60b63-133">For more information about how to create an SPS rate engine, see the following blog post: [Small Parcel Shipping: How to leverage small parcel shipping functionality in Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span></span>

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a><span data-ttu-id="60b63-134">Настройка механизма ставок в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="60b63-134">Set up a rate engine in Supply Chain Management</span></span>

<span data-ttu-id="60b63-135">Создав и развернут механизм ставок для SPS, выполните следующие действия, чтобы настроить его.</span><span class="sxs-lookup"><span data-stu-id="60b63-135">After you've created and deployed a rate engine for SPS, follow these steps to set it up.</span></span>

1. <span data-ttu-id="60b63-136">Перейдите в раздел **Управление транспортировкой \> Настройка \> Механизмы \> Механизм ставок**.</span><span class="sxs-lookup"><span data-stu-id="60b63-136">Go to **Transportation management \> Setup \> Engines \> Rate engine**.</span></span>
1. <span data-ttu-id="60b63-137">На панели операций выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="60b63-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="60b63-138">В новой строке установите следующие поля:</span><span class="sxs-lookup"><span data-stu-id="60b63-138">In the new row, set the following fields:</span></span>

    - <span data-ttu-id="60b63-139">**Механизм оценки** — введите уникальное имя для механизма ставок.</span><span class="sxs-lookup"><span data-stu-id="60b63-139">**Rating engine** – Enter a unique name for the rate engine.</span></span> <span data-ttu-id="60b63-140">При использовании демонстрационного механизма ставок введите *Демонстрационный механизм ставок*.</span><span class="sxs-lookup"><span data-stu-id="60b63-140">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="60b63-141">**Название** — введите краткое описание механизма ставок.</span><span class="sxs-lookup"><span data-stu-id="60b63-141">**Name** – Enter a short description of the rate engine.</span></span> <span data-ttu-id="60b63-142">При использовании демонстрационного механизма ставок введите *Демонстрационный механизм ставок*.</span><span class="sxs-lookup"><span data-stu-id="60b63-142">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="60b63-143">**ИД метаданных оценки** — выберите основу, которая должна использоваться для расчета ставки.</span><span class="sxs-lookup"><span data-stu-id="60b63-143">**Rating metadata ID** – Select the basis that should be used to calculate your rate.</span></span> <span data-ttu-id="60b63-144">Например, ставка может рассчитываться на основе расстояния.</span><span class="sxs-lookup"><span data-stu-id="60b63-144">For example, your rate might be calculated based on distance.</span></span> <span data-ttu-id="60b63-145">Если используется демонстрационный механизм ставок, это поле можно оставить пустым.</span><span class="sxs-lookup"><span data-stu-id="60b63-145">If you're using the demo rate engine, you can leave this field blank.</span></span>
    - <span data-ttu-id="60b63-146">**Сборка механизма** — введите имя файла развернутого пакета DLL.</span><span class="sxs-lookup"><span data-stu-id="60b63-146">**Engine assembly** – Enter the file name of the DLL package that you deployed.</span></span> <span data-ttu-id="60b63-147">При использовании демонстрационного механизма ставок введите *TMSSmallParcelShippingEngine.dll*.</span><span class="sxs-lookup"><span data-stu-id="60b63-147">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.dll*.</span></span>
    - <span data-ttu-id="60b63-148">**Класс механизма** — введите имя класса, установленного для механизма ставок.</span><span class="sxs-lookup"><span data-stu-id="60b63-148">**Engine class** – Enter the class name that was established for your rate engine.</span></span> <span data-ttu-id="60b63-149">При использовании демонстрационного механизма ставок введите *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span><span class="sxs-lookup"><span data-stu-id="60b63-149">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="60b63-150">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="60b63-150">Example scenario</span></span>

<span data-ttu-id="60b63-151">В этом примере показано, как настроить и использовать службы SPS после подготовки системы, как описано ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="60b63-151">This example scenario shows how to set up and use SPS after you've prepared your system as described earlier in this topic.</span></span> <span data-ttu-id="60b63-152">В этом сценарии используется ранее упомянутый демонстрационный механизм ставок.</span><span class="sxs-lookup"><span data-stu-id="60b63-152">This scenario uses the previously mentioned demo rate engine.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="60b63-153">Сделать демонстрационные данные доступными</span><span class="sxs-lookup"><span data-stu-id="60b63-153">Make demo data available</span></span>

<span data-ttu-id="60b63-154">Для работы с этим сценарием с помощью демонстрационных записей и значений, указанных здесь, необходимо использовать систему, в которой установлены стандартные [демонстрационные данные](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="60b63-154">To work through this scenario by using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="60b63-155">Дополнительно перед началом необходимо выбрать юридическое лицо **USMF**.</span><span class="sxs-lookup"><span data-stu-id="60b63-155">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="60b63-156">Настройка сценария</span><span class="sxs-lookup"><span data-stu-id="60b63-156">Set up the scenario</span></span>

<span data-ttu-id="60b63-157">В данном примере сценария у вас должен быть демонстрационный перевозчик, группа перевозчиков, политика упаковки и профиль упаковки.</span><span class="sxs-lookup"><span data-stu-id="60b63-157">For this example scenario, you must have a demo carrier, carrier group, packing policy, and packing profile.</span></span> <span data-ttu-id="60b63-158">В следующих подразделах объясняется, как подготовить записи, необходимые для сценария.</span><span class="sxs-lookup"><span data-stu-id="60b63-158">The following subsections explain how to prepare the records that are required for the scenario.</span></span> <span data-ttu-id="60b63-159">В производственном сценарии процесс настройки обычно напоминает описанный здесь процесс.</span><span class="sxs-lookup"><span data-stu-id="60b63-159">In a production scenario, the setup process typically resembles the process that is described here.</span></span> <span data-ttu-id="60b63-160">Однако у вас будут заданы другие значения.</span><span class="sxs-lookup"><span data-stu-id="60b63-160">However, you will set different values.</span></span>

#### <a name="set-up-carriers"></a><span data-ttu-id="60b63-161">Настройка перевозчиков</span><span class="sxs-lookup"><span data-stu-id="60b63-161">Set up carriers</span></span>

<span data-ttu-id="60b63-162">Чтобы настроить перевозчика, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="60b63-162">Follow these steps to set up a carrier.</span></span>

1. <span data-ttu-id="60b63-163">Перейдите в раздел **Управление транспортировкой \> Настройка \> Перевозчики \> Перевозчики, осуществляющий доставку**.</span><span class="sxs-lookup"><span data-stu-id="60b63-163">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="60b63-164">На панели операций выберите **Создать** для добавления перевозчика.</span><span class="sxs-lookup"><span data-stu-id="60b63-164">On the Action Pane, select **New** to add a carrier.</span></span>
1. <span data-ttu-id="60b63-165">В заголовке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="60b63-165">On the header, set the following values:</span></span>

    - <span data-ttu-id="60b63-166">**Перевозчик, осуществляющий доставку:** *Демонстрационный перевозчик*</span><span class="sxs-lookup"><span data-stu-id="60b63-166">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="60b63-167">**Имя:** *Демонстрационный перевозчик*</span><span class="sxs-lookup"><span data-stu-id="60b63-167">**Name:** *Demo Carrier*</span></span>
    - <span data-ttu-id="60b63-168">**Режим:** *Земля*</span><span class="sxs-lookup"><span data-stu-id="60b63-168">**Mode:** *Ground*</span></span>

1. <span data-ttu-id="60b63-169">На экспресс-вкладке **Обзор** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="60b63-169">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="60b63-170">**Активировать перевозчика:** *Да*</span><span class="sxs-lookup"><span data-stu-id="60b63-170">**Activate shipping carrier:** *Yes*</span></span>
    - <span data-ttu-id="60b63-171">**Активировать рейтинг перевозчика:** *Да*</span><span class="sxs-lookup"><span data-stu-id="60b63-171">**Activate carrier rating:** *Yes*</span></span>

1. <span data-ttu-id="60b63-172">На экспресс-вкладке **Службы** выберите **Создать**, чтобы добавить службу в сетку.</span><span class="sxs-lookup"><span data-stu-id="60b63-172">On the **Services** FastTab, select **New** to add a service to the grid.</span></span>
1. <span data-ttu-id="60b63-173">Задайте следующие значения для новой службы:</span><span class="sxs-lookup"><span data-stu-id="60b63-173">Set the following values for the new service:</span></span>

    - <span data-ttu-id="60b63-174">**Служба перевозчика:** *Демонстрационная служба перевозчика*</span><span class="sxs-lookup"><span data-stu-id="60b63-174">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="60b63-175">**Имя:** *Демонстрационная служба перевозчика*</span><span class="sxs-lookup"><span data-stu-id="60b63-175">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="60b63-176">**Способ транспортировки:** *Земля*</span><span class="sxs-lookup"><span data-stu-id="60b63-176">**Transportation method:** *Ground*</span></span>

    <span data-ttu-id="60b63-177">Введите произвольные значения для всех остальных полей по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="60b63-177">Enter arbitrary values for all the other fields, as required.</span></span> <span data-ttu-id="60b63-178">(При сохранении новой записи перевозчика отгрузки будет создан новый способ поставки, и поле **Способ поставки** будет установлено автоматически.)</span><span class="sxs-lookup"><span data-stu-id="60b63-178">(When you save the new shipping carrier record, a new mode of delivery will be created, and the **Mode of delivery** field will be set automatically.)</span></span>

1. <span data-ttu-id="60b63-179">На экспресс-вкладке **Профили оценки** выберите **Создать**, чтобы добавить профиль в сетку.</span><span class="sxs-lookup"><span data-stu-id="60b63-179">On the **Rating profiles** FastTab, select **New** to add a rating profile to the grid.</span></span>
1. <span data-ttu-id="60b63-180">Задайте следующие значения для нового профиля:</span><span class="sxs-lookup"><span data-stu-id="60b63-180">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="60b63-181">**Профиль оценки:** *Демонстрационная служба перевозчика*</span><span class="sxs-lookup"><span data-stu-id="60b63-181">**Rating profile:** *Demo carrier service*</span></span>
    - <span data-ttu-id="60b63-182">**Имя:** *Демонстрационная служба перевозчика*</span><span class="sxs-lookup"><span data-stu-id="60b63-182">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="60b63-183">**Механизм ставок:** *Демонстрационный механизм ставок*</span><span class="sxs-lookup"><span data-stu-id="60b63-183">**Rate engine:** *Demo rate engine*</span></span>

    <span data-ttu-id="60b63-184">Введите произвольные значения для всех остальных полей по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="60b63-184">Enter arbitrary values for all the other fields, as required.</span></span>

1. <span data-ttu-id="60b63-185">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="60b63-185">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="60b63-186">Дополнительные сведения о настройке перевозчиков см. в разделе [Настройка перевозчиков](../transportation/tasks/set-up-shipping-carriers.md).</span><span class="sxs-lookup"><span data-stu-id="60b63-186">For more information about how to set up carriers, see [Set up shipping carriers](../transportation/tasks/set-up-shipping-carriers.md).</span></span>

#### <a name="set-up-carrier-service-accounts"></a><span data-ttu-id="60b63-187">Настройка учетных записей перевозчиков</span><span class="sxs-lookup"><span data-stu-id="60b63-187">Set up carrier service accounts</span></span>

<span data-ttu-id="60b63-188">Выполните следующие действия, чтобы настроить учетную запись службы перевозчика.</span><span class="sxs-lookup"><span data-stu-id="60b63-188">Follow these steps to set up a carrier service account.</span></span>

1. <span data-ttu-id="60b63-189">Перейдите в раздел **Управление транспортировкой \> Настройка \> Расчет ставок \> Учетная запись службы перевозчика**.</span><span class="sxs-lookup"><span data-stu-id="60b63-189">Go to **Transportation management \> Setup \> Rating \> Carrier service account**.</span></span>
1. <span data-ttu-id="60b63-190">На панели операций выберите **Создать**, чтобы добавить учтеную запись службы перевозчика.</span><span class="sxs-lookup"><span data-stu-id="60b63-190">On the Action Pane, select **New** to add a carrier service account.</span></span>
1. <span data-ttu-id="60b63-191">Задайте следующие значения для новой учетной записи:</span><span class="sxs-lookup"><span data-stu-id="60b63-191">Set the following values for the new account:</span></span>

    - <span data-ttu-id="60b63-192">**Перевозчик, осуществляющий доставку:** *Демонстрационный перевозчик*</span><span class="sxs-lookup"><span data-stu-id="60b63-192">**Shipping Carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="60b63-193">**Служба перевозчика:** *Демонстрационная служба перевозчика*</span><span class="sxs-lookup"><span data-stu-id="60b63-193">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="60b63-194">**Номер счета клиента перевозчика:** номер счета клиента-перевозчика, используемый для проверки и аутентификации подключения к перевозчику, осуществляющему доставку.</span><span class="sxs-lookup"><span data-stu-id="60b63-194">**Carrier customer account number:** The carrier customer account number that is used to verify and authenticate the connection to the shipping carrier.</span></span> <span data-ttu-id="60b63-195">Это значение будет предоставлено вашим перевозчиком.</span><span class="sxs-lookup"><span data-stu-id="60b63-195">Your carrier will provide this value.</span></span> <span data-ttu-id="60b63-196">Если используется демонстрационная служба, можно ввести произвольное значение.</span><span class="sxs-lookup"><span data-stu-id="60b63-196">If you're using the demo service, you can enter an arbitrary value.</span></span>
    - <span data-ttu-id="60b63-197">**Сайт:** *6*</span><span class="sxs-lookup"><span data-stu-id="60b63-197">**Site:** *6*</span></span>
    - <span data-ttu-id="60b63-198">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="60b63-198">**Warehouse:** *62*</span></span>

    > [!NOTE]
    > <span data-ttu-id="60b63-199">Часто значение **Номера счета клиента-перевозчика** является единственным значением, необходимым для проверки подлинности подключения.</span><span class="sxs-lookup"><span data-stu-id="60b63-199">Often, the **Carrier customer account number** value is the only value that is required to authenticate the connection.</span></span> <span data-ttu-id="60b63-200">Однако если для перевозчика требуются дополнительные параметры проверки подлинности, ваша организация должна настроить эту страницу, чтобы добавить дополнительные поля, если необходимо.</span><span class="sxs-lookup"><span data-stu-id="60b63-200">However, if your carrier requires additional authentication parameters, your organization should customize this page to add extra fields as appropriate.</span></span>

#### <a name="set-up-a-container-packing-policy"></a><span data-ttu-id="60b63-201">Настройка политики упаковки контейнеров</span><span class="sxs-lookup"><span data-stu-id="60b63-201">Set up a container packing policy</span></span>

<span data-ttu-id="60b63-202">Выполните следующие действия, чтобы настроить политику упаковки контейнера.</span><span class="sxs-lookup"><span data-stu-id="60b63-202">Follow these steps to set up a container packing policy.</span></span>

1. <span data-ttu-id="60b63-203">Если вы еще не настроили определение принтера ZPL, настройте его с помощью приложения агента маршрутизации документов.</span><span class="sxs-lookup"><span data-stu-id="60b63-203">If you haven't already set up a ZPL printer definition, use the Document Routing Agent application to set it up.</span></span> <span data-ttu-id="60b63-204">Дополнительные сведения см. в разделе [Обзор печати документов](../../fin-ops-core/dev-itpro/analytics/print-documents.md) и связанных темах.</span><span class="sxs-lookup"><span data-stu-id="60b63-204">For more information, see [Document printing overview](../../fin-ops-core/dev-itpro/analytics/print-documents.md) and related topics.</span></span>
1. <span data-ttu-id="60b63-205">Перейдите в раздел **Управление складом \> Настройка \> Контейнеры \> Политики упаковки контейнеров**.</span><span class="sxs-lookup"><span data-stu-id="60b63-205">Go to **Warehouse Management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="60b63-206">На панели операций выберите **Создать**, чтобы добавить политику упаковки контейнеров.</span><span class="sxs-lookup"><span data-stu-id="60b63-206">On the Action Pane, select **New** to add a container packing policy.</span></span>
1. <span data-ttu-id="60b63-207">В заголовке новой политики задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="60b63-207">On the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="60b63-208">**Политика упаковки контейнеров:** *Демонстрационная политика упаковки*</span><span class="sxs-lookup"><span data-stu-id="60b63-208">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="60b63-209">**Описание:** описание политики</span><span class="sxs-lookup"><span data-stu-id="60b63-209">**Description:** A description of the policy</span></span>

1. <span data-ttu-id="60b63-210">На экспресс-вкладке **Обзор** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="60b63-210">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="60b63-211">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="60b63-211">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="60b63-212">**Местоположение по умолчанию для окончательной отгрузки:** *Дверь отсека*</span><span class="sxs-lookup"><span data-stu-id="60b63-212">**Default location for final shipment:** *Baydoor*</span></span>
    - <span data-ttu-id="60b63-213">**Единица измерения веса:** *КГ*</span><span class="sxs-lookup"><span data-stu-id="60b63-213">**Weight unit:** *KG*</span></span>
    - <span data-ttu-id="60b63-214">**Политика закрытия контейнера:** *Автоматический выпуск*</span><span class="sxs-lookup"><span data-stu-id="60b63-214">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="60b63-215">**Политика выпуска контейнеров:** *Сделать доступным в окончательном местоположении отгрузки*</span><span class="sxs-lookup"><span data-stu-id="60b63-215">**Container release policy:** *Make available at final shipping location*</span></span>

1. <span data-ttu-id="60b63-216">На экспресс-вкладке **Манифест контейнера** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="60b63-216">On the **Container manifest** FastTab, set the following values:</span></span>

    - <span data-ttu-id="60b63-217">**Автоматический манифест при закрытии контейнера:** *Да*</span><span class="sxs-lookup"><span data-stu-id="60b63-217">**Automatic manifest at container close:** *Yes*</span></span>
    - <span data-ttu-id="60b63-218">**Требования к манифесту для контейнера:** *Управление транспортировкой*</span><span class="sxs-lookup"><span data-stu-id="60b63-218">**Manifest requirements for container:** *Transportation management*</span></span>
    - <span data-ttu-id="60b63-219">**Печать содержимого контейнера:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="60b63-219">**Print container contents:** *No*</span></span>

1. <span data-ttu-id="60b63-220">На экспресс-вкладке **Печать этикетки перевозчика** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="60b63-220">On the **Carrier label printing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="60b63-221">**Печатать этикету отгрузки контейнера:** *Всегда*</span><span class="sxs-lookup"><span data-stu-id="60b63-221">**Print container shipping label:** *Always*</span></span>
    - <span data-ttu-id="60b63-222">**Имя принтера:** имя принтера ZPL, который должен печатать этикетки отгрузки</span><span class="sxs-lookup"><span data-stu-id="60b63-222">**Printer name:** The name of the ZPL printer that should print shipping labels</span></span>

#### <a name="set-up-a-packing-profile"></a><span data-ttu-id="60b63-223">Настройка профиля упаковки</span><span class="sxs-lookup"><span data-stu-id="60b63-223">Set up a packing profile</span></span>

<span data-ttu-id="60b63-224">Выполните следующие действия, чтобы настроить профиль упаковки.</span><span class="sxs-lookup"><span data-stu-id="60b63-224">Follow these steps to set up a packing profile.</span></span>

1. <span data-ttu-id="60b63-225">Перейдите в раздел **Управление складом \> Настройка \> Упаковка \> Профили упаковки**.</span><span class="sxs-lookup"><span data-stu-id="60b63-225">Go to **Warehouse Management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="60b63-226">На панели операций выберите **Создать**, чтобы добавить профиль упаковки в сетку.</span><span class="sxs-lookup"><span data-stu-id="60b63-226">On the Action Pane, select **New** to add a packing profile to the grid.</span></span>
1. <span data-ttu-id="60b63-227">Задайте следующие значения для нового профиля:</span><span class="sxs-lookup"><span data-stu-id="60b63-227">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="60b63-228">**Код профиля упаковки:** *Демонстрационный профиль упаковки*</span><span class="sxs-lookup"><span data-stu-id="60b63-228">**Packing profile ID:** *Demo packing profile*</span></span>
    - <span data-ttu-id="60b63-229">**Описание:** описание профиля</span><span class="sxs-lookup"><span data-stu-id="60b63-229">**Description:** A description of the profile</span></span>
    - <span data-ttu-id="60b63-230">**Политика упаковки контейнеров:** *Демонстрационная политика упаковки*</span><span class="sxs-lookup"><span data-stu-id="60b63-230">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="60b63-231">**Режим кода контейнера:** *Авто*</span><span class="sxs-lookup"><span data-stu-id="60b63-231">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="60b63-232">**Тип контейнера:** *SmallBox*</span><span class="sxs-lookup"><span data-stu-id="60b63-232">**Container type:** *SmallBox*</span></span>

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a><span data-ttu-id="60b63-233">Настройка клиента для использования перевозчика SPS</span><span class="sxs-lookup"><span data-stu-id="60b63-233">Set up a customer to use the SPS carrier</span></span>

<span data-ttu-id="60b63-234">Выполните следующие действия, чтобы настроить клиента так, чтобы он мог использовать созданного перевозчика.</span><span class="sxs-lookup"><span data-stu-id="60b63-234">Follow these steps to set up a customer so that it can use the carrier that you created.</span></span>

1. <span data-ttu-id="60b63-235">Перейдите в раздел **Расчеты с клиентами \> Клиенты \> Все клиенты**.</span><span class="sxs-lookup"><span data-stu-id="60b63-235">Go to **Accounts receivable \> customers \> All customers**.</span></span>
1. <span data-ttu-id="60b63-236">В сетке найдите и выберите клиента *US-027*.</span><span class="sxs-lookup"><span data-stu-id="60b63-236">In the grid, find and select customer *US-027*.</span></span>
1. <span data-ttu-id="60b63-237">В области действий на вкладке **Общие** в группе **Настройка** выберите **Учетные записи клиентов-перевозчиков**.</span><span class="sxs-lookup"><span data-stu-id="60b63-237">On the Action Pane, on the **General** tab, in the **Set up** group, select **Carrier customer accounts**.</span></span>
1. <span data-ttu-id="60b63-238">На странице **Учетные записи клиентов-перевозчиков** на панели операций выберите **Создать**, чтобы добавить учетную запись в сетку.</span><span class="sxs-lookup"><span data-stu-id="60b63-238">On the **Carrier customer accounts** page, on the Action Pane, select **New** to add an account to the grid.</span></span>
1. <span data-ttu-id="60b63-239">Задайте следующие значения для новой учетной записи:</span><span class="sxs-lookup"><span data-stu-id="60b63-239">Set the following values for the new account:</span></span>

    - <span data-ttu-id="60b63-240">**Перевозчик, осуществляющий доставку:** *Демонстрационный перевозчик*</span><span class="sxs-lookup"><span data-stu-id="60b63-240">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="60b63-241">**Номер учетной записи клиента-перевозчика:** *12345* (Для этого сценария значение не имеет значения, но на него есть ссылки в следующем разделе.)</span><span class="sxs-lookup"><span data-stu-id="60b63-241">**Carrier customer account number:** *12345* (The value isn't important for this scenario, but it will be referred to in the next section.)</span></span>

### <a name="go-through-the-example-scenario"></a><span data-ttu-id="60b63-242">Прохождение примера сценария</span><span class="sxs-lookup"><span data-stu-id="60b63-242">Go through the example scenario</span></span>

<span data-ttu-id="60b63-243">После настройки всех демонстрационных примеров, как описано в предыдущем разделе, можно приступать к прохождению примера сценария.</span><span class="sxs-lookup"><span data-stu-id="60b63-243">After you've set up all the sample data as described in the previous section, you're ready to go through the example scenario.</span></span>

#### <a name="create-a-sales-order-and-process-the-work"></a><span data-ttu-id="60b63-244">Создание заказа на продажу и обработка работы</span><span class="sxs-lookup"><span data-stu-id="60b63-244">Create a sales order and process the work</span></span>

<span data-ttu-id="60b63-245">Выполните эти действия, чтобы создать заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="60b63-245">Follow these steps to create a sales order.</span></span>

1. <span data-ttu-id="60b63-246">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="60b63-246">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="60b63-247">Выберите **Создать**, чтобы создать заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="60b63-247">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="60b63-248">В диалоговом окне **Создать заказ на продажу** задайте в поле **Счет клиента** значение *US-027*.</span><span class="sxs-lookup"><span data-stu-id="60b63-248">In the **Create sales order** dialog box, set the **Customer account** field to *US-027*.</span></span>
1. <span data-ttu-id="60b63-249">Выберите **ОК**, чтобы создать заказ на продажу и закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="60b63-249">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="60b63-250">Открывается новый заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="60b63-250">The new sales order is opened.</span></span> <span data-ttu-id="60b63-251">На экспресс-вкладке **Заголовок заказа на продажу** задайте в поле **Номер учетной записи клиента-перевозчика** значение, выбранное для этого клиента ранее (*12345*).</span><span class="sxs-lookup"><span data-stu-id="60b63-251">On the **Sales order header** FastTab, set the **Carrier customer account number** field to the value that you selected for this customer earlier (*12345*).</span></span>
1. <span data-ttu-id="60b63-252">В разделе **Строки заказа на продажу** добавьте строку заказа на продажу и установите для нее следующие значения:</span><span class="sxs-lookup"><span data-stu-id="60b63-252">In the **Sales order lines** section, add a sales line, and set the following values for it:</span></span>

    - <span data-ttu-id="60b63-253">**Код номенклатуры:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="60b63-253">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="60b63-254">**Количество:** *1*</span><span class="sxs-lookup"><span data-stu-id="60b63-254">**Quantity:** *1*</span></span>
    - <span data-ttu-id="60b63-255">**Сайт:** *6*</span><span class="sxs-lookup"><span data-stu-id="60b63-255">**Site:** *6*</span></span>
    - <span data-ttu-id="60b63-256">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="60b63-256">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="60b63-257">Перейдите к представлению **Заголовок**.</span><span class="sxs-lookup"><span data-stu-id="60b63-257">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="60b63-258">На экспресс-вкладке **Доставка** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="60b63-258">On the **Delivery** FastTab, set the following values:</span></span>

    - <span data-ttu-id="60b63-259">**Перевозчик, осуществляющий доставку:** *Демонстрационный перевозчик*</span><span class="sxs-lookup"><span data-stu-id="60b63-259">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="60b63-260">**Служба перевозчика:** *Демонстрационная служба перевозчика*</span><span class="sxs-lookup"><span data-stu-id="60b63-260">**Carrier service:** *Demo carrier service*</span></span>

1. <span data-ttu-id="60b63-261">Перейдите обратно в представление **Строки**.</span><span class="sxs-lookup"><span data-stu-id="60b63-261">Switch back to the **Lines** view.</span></span> <span data-ttu-id="60b63-262">Если будет предложено обновить способ поставки для строк продаж, выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="60b63-262">If you're prompted to update the mode of delivery for the sales lines, select **Yes**.</span></span>
1. <span data-ttu-id="60b63-263">В разделе **Строки заказа на продажу** выберите строку заказа, которую вы настроили ранее, затем выберите **Запасы \> Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="60b63-263">In the **Sales order lines** section, select the order line that you set up earlier, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="60b63-264">На странице **Резервирование** выберите **Резервирование лота**, чтобы зарезервировать полное количество по выбранной строке на складе.</span><span class="sxs-lookup"><span data-stu-id="60b63-264">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="60b63-265">Закройте страницу **Резервирование**, чтобы вернуться в заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="60b63-265">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="60b63-266">На панели операций на вкладке **Склад** выберите вариант **Выпустить на склад**.</span><span class="sxs-lookup"><span data-stu-id="60b63-266">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="60b63-267">Работа создается для перемещения номенклатур из местоположения комплектации на станцию упаковки.</span><span class="sxs-lookup"><span data-stu-id="60b63-267">Work is created to move items from the picking location to the packing station.</span></span>

1. <span data-ttu-id="60b63-268">В разделе **Строки заказа на продажу** выберите **Склад \> Сведения об отгрузке**.</span><span class="sxs-lookup"><span data-stu-id="60b63-268">In the **Sales order lines** section, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="60b63-269">На странице **Сведения о отгрузке** запишите идентификатор отгрузки.</span><span class="sxs-lookup"><span data-stu-id="60b63-269">On the **Shipment details** page, make a note of the shipment ID.</span></span> <span data-ttu-id="60b63-270">Он потребуется при упаковке отгрузки на упаковочной станции.</span><span class="sxs-lookup"><span data-stu-id="60b63-270">You will need it when you pack the pack the shipment at the packing station.</span></span>
1. <span data-ttu-id="60b63-271">Закройте страницу **Сведения об отгрузке**, чтобы вернуться в заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="60b63-271">Close the **Shipment details** page to return to the sales order.</span></span>
1. <span data-ttu-id="60b63-272">Запишите номер заказа на продажу, затем перейдите в раздел **Управление складом \> Работа \> Вся работа**.</span><span class="sxs-lookup"><span data-stu-id="60b63-272">Make a note of the sales order number, and then go to **Warehouse management \> Work \> All work**.</span></span>
1. <span data-ttu-id="60b63-273">Номер заказа на продажу используется для поиска и выбора работы, которая была создана для заказа.</span><span class="sxs-lookup"><span data-stu-id="60b63-273">Use the sales order number to find and select the work that was created for the order.</span></span>
1. <span data-ttu-id="60b63-274">На панели операций откройте вкладку **Работа** и выберите **Завершить работу**.</span><span class="sxs-lookup"><span data-stu-id="60b63-274">On the Action Pane, on the **Work** tab, select **Complete work**.</span></span>
1. <span data-ttu-id="60b63-275">На странице **Завершение работы** в поле **Код пользователя** выберите код пользователя.</span><span class="sxs-lookup"><span data-stu-id="60b63-275">On the **Work completion** page, in the **User ID** field, select a user ID.</span></span> <span data-ttu-id="60b63-276">Затем на панели операций выберите **Проверить работу**.</span><span class="sxs-lookup"><span data-stu-id="60b63-276">Then, on the Action Pane, select **Validate work**.</span></span>
1. <span data-ttu-id="60b63-277">Если работа прошла проверку, выберите **Завершить работу** в области действий.</span><span class="sxs-lookup"><span data-stu-id="60b63-277">If the work passes validation, select **Complete work** on the Action Pane.</span></span>

    <span data-ttu-id="60b63-278">Работа помечается как завершенная для моделирования перемещения номенклатур на станцию упаковки.</span><span class="sxs-lookup"><span data-stu-id="60b63-278">The work is marked as completed to simulate the movement of items to the packing station.</span></span>

#### <a name="pack-the-shipment"></a><span data-ttu-id="60b63-279">Упаковка отгрузки</span><span class="sxs-lookup"><span data-stu-id="60b63-279">Pack the shipment</span></span>

<span data-ttu-id="60b63-280">Выполните следующие действия, чтобы упаковать отгрузку.</span><span class="sxs-lookup"><span data-stu-id="60b63-280">Follow these steps to pack the shipment.</span></span>

1. <span data-ttu-id="60b63-281">Перейдите к разделу **Управление складом \> Настройка \> Работник** и убедитесь, что ваша учетная запись пользователя связана с учетной записью работника для управления складом.</span><span class="sxs-lookup"><span data-stu-id="60b63-281">Go to **Warehouse management \> Setup \> Worker**, and make sure that your user account is associated with a worker account for warehouse management.</span></span>
1. <span data-ttu-id="60b63-282">Перейдите в раздел **Управление складом \> Комплектация и контейнеризация \> Упаковка**.</span><span class="sxs-lookup"><span data-stu-id="60b63-282">Go to **Warehouse management \> Picking and containerization \> Pack**.</span></span>
1. <span data-ttu-id="60b63-283">В диалоговом окне **Выбрать станцию упаковки** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="60b63-283">In the **Select packing station** dialog box, set the following values:</span></span>

    - <span data-ttu-id="60b63-284">**Сайт:** *6*</span><span class="sxs-lookup"><span data-stu-id="60b63-284">**Site:** *6*</span></span>
    - <span data-ttu-id="60b63-285">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="60b63-285">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="60b63-286">**Местонахождение:** *Упаковка*</span><span class="sxs-lookup"><span data-stu-id="60b63-286">**Location:** *Pack*</span></span>
    - <span data-ttu-id="60b63-287">**Код профиля упаковки:** *Демонстрационный профиль упаковки*</span><span class="sxs-lookup"><span data-stu-id="60b63-287">**Packing profile ID:** *Demo packing profile*</span></span>

1. <span data-ttu-id="60b63-288">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="60b63-288">Select **OK**.</span></span>
1. <span data-ttu-id="60b63-289">Появится страница **Упаковка**.</span><span class="sxs-lookup"><span data-stu-id="60b63-289">The **Pack** page appears.</span></span> <span data-ttu-id="60b63-290">В производственном сценарии работник отсканирует грузоместо или код отгрузки.</span><span class="sxs-lookup"><span data-stu-id="60b63-290">In a production scenario, a worker will scan a license plate or shipment ID.</span></span> <span data-ttu-id="60b63-291">Однако для этого сценария откройте страницу **Все отгрузки** и найдите номер отгрузки для только что созданной отгрузки.</span><span class="sxs-lookup"><span data-stu-id="60b63-291">However, for this scenario, open the **All shipments** page, and look up the shipment number for the shipment that you just created.</span></span> <span data-ttu-id="60b63-292">Затем введите это значение в поле **Грузоместо или отгрузка** на странице **Упаковка**.</span><span class="sxs-lookup"><span data-stu-id="60b63-292">Then enter this value in the **License plate or shipment** field on the **Pack** page.</span></span> <span data-ttu-id="60b63-293">В качестве альтернативы введите код отгрузки, который вы записали ранее.</span><span class="sxs-lookup"><span data-stu-id="60b63-293">Alternatively, enter the shipment ID that you made a note of earlier.</span></span>
1. <span data-ttu-id="60b63-294">В области действий выберите **Создать контейнер**.</span><span class="sxs-lookup"><span data-stu-id="60b63-294">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="60b63-295">В появившемся диалоговом окне отображаются подробные сведения о новом контейнере.</span><span class="sxs-lookup"><span data-stu-id="60b63-295">The dialog box that appears shows details about the new container.</span></span> <span data-ttu-id="60b63-296">Оставьте значения по умолчанию, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="60b63-296">Leave the default values, and then select **OK**.</span></span>
1. <span data-ttu-id="60b63-297">На странице **Упаковка** на экспресс-вкладке **Упаковка номенклатуры** в поле **Код** выберите *A0002*, чтобы упаковать эту номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="60b63-297">On the **Pack** page, on the **Item packing** FastTab, in the **Identifier** field, select *A0002* to pack that item.</span></span> <span data-ttu-id="60b63-298">Номенклатура добавляется в контейнер.</span><span class="sxs-lookup"><span data-stu-id="60b63-298">The item is added to the container.</span></span>
1. <span data-ttu-id="60b63-299">На панели операций выберите **Контейнеры для отгрузки**.</span><span class="sxs-lookup"><span data-stu-id="60b63-299">On the Action Pane, select **Containers for shipment**.</span></span>

    <span data-ttu-id="60b63-300">На появившейся странице **Контейнеры для отгрузки** имеется строка для только что созданного контейнера.</span><span class="sxs-lookup"><span data-stu-id="60b63-300">The **Containers for shipment** page that appears has a row for the container that you just created.</span></span> <span data-ttu-id="60b63-301">Однако поле **Кода манифеста контейнера** в этой строке в настоящее время пусто, так как вы еще не получили этикетку отгрузки и номер отслеживания от перевозчика.</span><span class="sxs-lookup"><span data-stu-id="60b63-301">However, the **Container manifest ID** field in that row is currently blank, because you haven't yet received the shipping label and tracking number from the carrier.</span></span>

1. <span data-ttu-id="60b63-302">В области действий выберите **Закрыть контейнер**.</span><span class="sxs-lookup"><span data-stu-id="60b63-302">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="60b63-303">В диалоговом окне **Закрыть контейнер** установите для поля **Вес брутто** значение *1 кг*, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="60b63-303">In the **Close container** dialog box, set the **Gross weight** field to *1 kg*, and then select **OK**.</span></span>

    <span data-ttu-id="60b63-304">Этикетка отгрузки должна быть напечатана на принтере ZPL, который был выбран ранее.</span><span class="sxs-lookup"><span data-stu-id="60b63-304">The shipping label should now be printed on the ZPL printer that you selected earlier.</span></span> <span data-ttu-id="60b63-305">Она должна быть похожа на следующий пример.</span><span class="sxs-lookup"><span data-stu-id="60b63-305">It should resemble the following example.</span></span>

    <span data-ttu-id="60b63-306">![Пример этикетки отгрузки](media/sps-label-example.png "Пример этикетки отгрузки")</span><span class="sxs-lookup"><span data-stu-id="60b63-306">![Example shipping label](media/sps-label-example.png "Example shipping label")</span></span>

1. <span data-ttu-id="60b63-307">Обратите внимание, что значения **Код манифеста контейнера** и **Итоговый фрахт** были добавлены как полученные от перевозчика.</span><span class="sxs-lookup"><span data-stu-id="60b63-307">Notice that the **Container manifest ID** and **Total freight** values have been added as received from the carrier.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]