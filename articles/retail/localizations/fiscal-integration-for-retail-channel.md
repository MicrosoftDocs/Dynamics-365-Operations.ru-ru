---
title: "Финансовая интеграция канала розничной торговли"
description: "В этом разделе содержится обзор финансовой интеграции для Retail POS."
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: ru-ru
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a><span data-ttu-id="2ef33-103">Финансовая интеграция канала розничной торговли</span><span class="sxs-lookup"><span data-stu-id="2ef33-103">Fiscal integration for Retail channel</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ef33-104">В этом разделе приводится обзор функции финансовой интеграции, доступной в Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="2ef33-104">This topic is an overview of the fiscal integration functionality that is available in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="2ef33-105">Функция финансовой интеграции — это структура, предназначенная для поддержки местного финансового законодательства, предназначенного для исключения мошенничества в сфере розничной торговли.</span><span class="sxs-lookup"><span data-stu-id="2ef33-105">The fiscal integration functionality is a framework designed to support local fiscal laws that are aimed to prevent fraud in the Retail industry.</span></span> <span data-ttu-id="2ef33-106">Типичные сценарии, которые могут охватываться с помощью финансовой интеграции:</span><span class="sxs-lookup"><span data-stu-id="2ef33-106">Typical scenarios that could be covered by using fiscal integration include:</span></span>

- <span data-ttu-id="2ef33-107">Печать финансового отчета и предоставление его клиенту.</span><span class="sxs-lookup"><span data-stu-id="2ef33-107">Printing a fiscal receipt and giving it to the customer.</span></span>
- <span data-ttu-id="2ef33-108">Защита отправки сведений, связанных с продажами и возвратами, выполняемые в POS, во внешнюю службу, предоставляемую властями.</span><span class="sxs-lookup"><span data-stu-id="2ef33-108">Securing the submission of the information related to sales and returns performed on POS to an external service provided by the authority.</span></span>
- <span data-ttu-id="2ef33-109">Использование защиты данных с помощью цифровой подписи, авторизованной уполномоченной организацией.</span><span class="sxs-lookup"><span data-stu-id="2ef33-109">Using data protection with a digital signature authorized by the authority.</span></span>

<span data-ttu-id="2ef33-110">В этом разделе приводятся рекомендации по настройке финансовой интеграции, чтобы пользователи могли выполнять следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="2ef33-110">This topic provides guidelines for setting up fiscal integration so users can perform the following tasks.</span></span> 

- <span data-ttu-id="2ef33-111">Настройка финансовых соединителей, являющихся финансовыми устройствами или службами, используемыми для целей финансовой регистрации, таких как сохранение, цифровые подписи и защищенная отправка финансовых данных.</span><span class="sxs-lookup"><span data-stu-id="2ef33-111">Configure fiscal connectors, which are fiscal devices or services used for fiscal registration purposes like saving, digital signatures, and secured submission of fiscal data.</span></span>
- <span data-ttu-id="2ef33-112">Настройка поставщика документов, который определяет метод вывода и алгоритм создания финансового документа.</span><span class="sxs-lookup"><span data-stu-id="2ef33-112">Configure the document provider, which defines an output method and an algorithm of fiscal document generation.</span></span>
- <span data-ttu-id="2ef33-113">Настройка процесса финансовой регистрации, который определяет последовательность шагов и группы соединителей, используемые на каждом шаге.</span><span class="sxs-lookup"><span data-stu-id="2ef33-113">Configure the fiscal registration process, which is defines a sequence of steps and a group of connectors used on each step.</span></span>
- <span data-ttu-id="2ef33-114">Назначение процессов финансовой регистрации профилям функциональности POS.</span><span class="sxs-lookup"><span data-stu-id="2ef33-114">Assign fiscal registration processes to POS functionality profiles.</span></span>
- <span data-ttu-id="2ef33-115">Назначение технических профилей соединителя, либо профилям оборудования (для локальных финансовых соединителей), либо профилям функциональности POS (для других типов финансовых соединителей).</span><span class="sxs-lookup"><span data-stu-id="2ef33-115">Assign connector technical profiles, either to hardware profiles (for the local fiscal connectors) or to POS functionality profiles (for other fiscal connector types).</span></span>

## <a name="fiscal-integration-execution-flow"></a><span data-ttu-id="2ef33-116">Поток выполнения финансовой интеграции</span><span class="sxs-lookup"><span data-stu-id="2ef33-116">Fiscal integration execution flow</span></span>
<span data-ttu-id="2ef33-117">Следующий сценарий показывает общий поток выполнения финансовой интеграции.</span><span class="sxs-lookup"><span data-stu-id="2ef33-117">The following scenario shows the common fiscal integration execution flow.</span></span>

1. <span data-ttu-id="2ef33-118">Инициализация процесса финансовой регистрации.</span><span class="sxs-lookup"><span data-stu-id="2ef33-118">Initialization of the fiscal registration process.</span></span>
  
   <span data-ttu-id="2ef33-119">После выполнения некоторых действий, требующих финансовой регистрации, например после завершения проводки розничной торговли, процесс финансовой регистрации связан с текущим профилем функциональности POS.</span><span class="sxs-lookup"><span data-stu-id="2ef33-119">After performing some actions where fiscal registration is required, such as after a retail transaction has been concluded, the fiscal registration process is associated with the current POS functionality profile.</span></span>

1. <span data-ttu-id="2ef33-120">Поиск финансового соединителя.</span><span class="sxs-lookup"><span data-stu-id="2ef33-120">Search for a fiscal connector.</span></span>
   
   <span data-ttu-id="2ef33-121">Для каждого шага финансовой регистрации, включенного в процесс финансовой регистрации, система сопоставляет список финансовых соединителей.</span><span class="sxs-lookup"><span data-stu-id="2ef33-121">For each fiscal registration step included in the fiscal registration process, the system matches the list of fiscal connectors.</span></span> <span data-ttu-id="2ef33-122">Эти соединители имеют функциональной профиль, включенный в указанную группу соединителей, со списком соединителей, которые имеют технический профиль, связанный с текущим профилем оборудования (только для типа соединителя, равного **Локальный**) или с текущим профилем функциональности POS (для других типов соединителей).</span><span class="sxs-lookup"><span data-stu-id="2ef33-122">These connectors have a functional profile included in the specified connector group, with a list of connectors that have a technical profile associated with the current hardware profile (for a connector type that equals **Local** only) or with the current POS functionality profile (for other connector types).</span></span>
   
1. <span data-ttu-id="2ef33-123">Выполнение финансовой интеграции.</span><span class="sxs-lookup"><span data-stu-id="2ef33-123">Perform the fiscal integration.</span></span>

   <span data-ttu-id="2ef33-124">Система выполняет все необходимые действия, определенные сборкой, связанной с найденным соединителем.</span><span class="sxs-lookup"><span data-stu-id="2ef33-124">The system executes all necessary actions defined by an assembly linked with the found connector.</span></span> <span data-ttu-id="2ef33-125">Это выполняется в соответствии с параметрами функционального профиля и технического профиля, которые были найдены на предыдущем шаге для этого соединителя.</span><span class="sxs-lookup"><span data-stu-id="2ef33-125">This is done in accordance with the settings of the functional profile and technical profile that were found on the previous step for this connector.</span></span>

## <a name="setup-needed-before-using-fiscal-integration"></a><span data-ttu-id="2ef33-126">Настройка, необходимая перед использованием финансовой интеграции</span><span class="sxs-lookup"><span data-stu-id="2ef33-126">Setup needed before using fiscal integration</span></span>
<span data-ttu-id="2ef33-127">Прежде чем использовать функцию финансовой интеграции, следует определить следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="2ef33-127">Before using the fiscal integration functionality, you should define the following settings:</span></span>

- <span data-ttu-id="2ef33-128">Определите номерную серию на странице **Параметры Retail** для номера финансового функционального профиля.</span><span class="sxs-lookup"><span data-stu-id="2ef33-128">Define the number sequence on the **Retail parameters** page for the fiscal functional profile number.</span></span>
  
- <span data-ttu-id="2ef33-129">Определите номерные серии на странице **Общие параметры розничной торговли** для следующих ссылок:</span><span class="sxs-lookup"><span data-stu-id="2ef33-129">Define the number sequences on the **Retail shared parameters** page for the following references:</span></span>
  
  - <span data-ttu-id="2ef33-130">Номер финансового технического профиля</span><span class="sxs-lookup"><span data-stu-id="2ef33-130">Fiscal technical profile number</span></span>
  - <span data-ttu-id="2ef33-131">Номер группы финансовых соединителей</span><span class="sxs-lookup"><span data-stu-id="2ef33-131">Fiscal connector group number</span></span>
  - <span data-ttu-id="2ef33-132">Номер процесса регистрации</span><span class="sxs-lookup"><span data-stu-id="2ef33-132">Registration process number</span></span>

- <span data-ttu-id="2ef33-133">Создайте **Финансовый соединитель** в пункте **Retail > Настройка канала > Финансовая интеграция > Финансовые соединители** для каждого устройства или службы, которые планируется использовать в целях финансовой интеграции.</span><span class="sxs-lookup"><span data-stu-id="2ef33-133">Create a **Fiscal connector** in **Retail > Channel setup > Fiscal integration > Fiscal connectors** for each device or service that you plan to use for fiscal integration purposes.</span></span>

-  <span data-ttu-id="2ef33-134">Создайте **Поставщик финансовых документов** в пункте **Retail > Настройка канала > Финансовая интеграция > Поставщики финансовых документов** для всех финансовых соединителей.</span><span class="sxs-lookup"><span data-stu-id="2ef33-134">Create a **Fiscal document provider** in **Retail > Channel setup > Fiscal integration > Fiscal document providers** for all fiscal connectors.</span></span> <span data-ttu-id="2ef33-135">Сопоставление данных считается частью поставщика финансовых документов.</span><span class="sxs-lookup"><span data-stu-id="2ef33-135">Data mapping is considered a part of the fiscal document provider.</span></span> <span data-ttu-id="2ef33-136">Чтобы настроить сопоставления различных данных для одного соединителя (например, специфичных для государства правил), следует создать различных поставщиков финансовых документов.</span><span class="sxs-lookup"><span data-stu-id="2ef33-136">To set up different data mappings for the same connector (like state-specific regulations), you should create different fiscal document providers.</span></span>

- <span data-ttu-id="2ef33-137">Создайте **Функциональный профиль соединителя** в **Retail > Настройка канала > Финансовая интеграция > Функциональные профили соединителей** для каждого поставщика финансовых документов.</span><span class="sxs-lookup"><span data-stu-id="2ef33-137">Create a **Connector functional profile** in **Retail > Channel setup > Fiscal integration > Connector functional profiles** for each fiscal document provider.</span></span>
  - <span data-ttu-id="2ef33-138">Выберите название соединителя.</span><span class="sxs-lookup"><span data-stu-id="2ef33-138">Select a connector name.</span></span>
  - <span data-ttu-id="2ef33-139">Выберите поставщика документов.</span><span class="sxs-lookup"><span data-stu-id="2ef33-139">Select a document provider.</span></span>
  - <span data-ttu-id="2ef33-140">Укажите параметры ставки НДС на вкладке **Настройка службы**.</span><span class="sxs-lookup"><span data-stu-id="2ef33-140">Specify VAT rates settings on the **Service setup** tab.</span></span>
  - <span data-ttu-id="2ef33-141">Укажите коды сопоставления НДС и сопоставление типов платежных средств на вкладке **Сопоставление данных**.</span><span class="sxs-lookup"><span data-stu-id="2ef33-141">Specify VAT codes mapping and tender type mapping on the **Data mapping** tab.</span></span>

  #### <a name="examples"></a><span data-ttu-id="2ef33-142">Примеры</span><span class="sxs-lookup"><span data-stu-id="2ef33-142">Examples</span></span> 

  |  | <span data-ttu-id="2ef33-143">Форматировать</span><span class="sxs-lookup"><span data-stu-id="2ef33-143">Format</span></span> | <span data-ttu-id="2ef33-144">Пример</span><span class="sxs-lookup"><span data-stu-id="2ef33-144">Example</span></span> | 
  |--------|--------|--------|
  | <span data-ttu-id="2ef33-145">Настройки ставок НДС</span><span class="sxs-lookup"><span data-stu-id="2ef33-145">VAT rates settings</span></span> | <span data-ttu-id="2ef33-146">значение : VATrate</span><span class="sxs-lookup"><span data-stu-id="2ef33-146">value : VATrate</span></span> | <span data-ttu-id="2ef33-147">1 : 2000, 2 : 1800</span><span class="sxs-lookup"><span data-stu-id="2ef33-147">1 : 2000, 2 : 1800</span></span> |
  | <span data-ttu-id="2ef33-148">Сопоставление кодов НДС</span><span class="sxs-lookup"><span data-stu-id="2ef33-148">VAT codes mapping</span></span> | <span data-ttu-id="2ef33-149">VATcode : значение</span><span class="sxs-lookup"><span data-stu-id="2ef33-149">VATcode : value</span></span> | <span data-ttu-id="2ef33-150">vat20 : 1, vat18 : 2</span><span class="sxs-lookup"><span data-stu-id="2ef33-150">vat20 : 1, vat18 : 2</span></span> |
  | <span data-ttu-id="2ef33-151">Сопоставление типов платежных средств</span><span class="sxs-lookup"><span data-stu-id="2ef33-151">Tender types mapping</span></span> | <span data-ttu-id="2ef33-152">TenderTyp : значение</span><span class="sxs-lookup"><span data-stu-id="2ef33-152">TenderTyp : value</span></span> | <span data-ttu-id="2ef33-153">Наличные : 1, Карта : 2</span><span class="sxs-lookup"><span data-stu-id="2ef33-153">Cash : 1, Card : 2</span></span> |

- <span data-ttu-id="2ef33-154">Создайте **Группы финансовых соединителей** в **Retail > Настройка канала > Финансовая интеграция > Группа финансовых соединителей**.</span><span class="sxs-lookup"><span data-stu-id="2ef33-154">Create **Fiscal connector groups** in **Retail > Channel setup > Fiscal integration > Fiscal connector group**.</span></span> <span data-ttu-id="2ef33-155">Группа соединителей является подмножеством функциональных профилей, связанных с финансовыми соединителями, которые выполняют одинаковые функции и используются на одной стадии в процессе финансовой регистрации.</span><span class="sxs-lookup"><span data-stu-id="2ef33-155">A connector group is a subset of functional profiles linked with fiscal connectors that perform identical functions and are used at the same stage within a fiscal registration process.</span></span>

   - <span data-ttu-id="2ef33-156">Добавление функциональных профилей в группу соединителей.</span><span class="sxs-lookup"><span data-stu-id="2ef33-156">Add functional profiles to the connector group.</span></span> <span data-ttu-id="2ef33-157">Щелкните **Добавить** на странице **Функциональные профили** и выберите номер профиля.</span><span class="sxs-lookup"><span data-stu-id="2ef33-157">Click **Add** on the **Functional profiles** page and select a profile number.</span></span>
   - <span data-ttu-id="2ef33-158">Если нужно приостановить использование функционального профиля, установите для параметра **Отключить** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="2ef33-158">If you want to suspend usage of the functional profile, set **Disable** to **Yes**.</span></span> 
   
     <span data-ttu-id="2ef33-159">Это изменение затрагивает только текущую группу соединителей.</span><span class="sxs-lookup"><span data-stu-id="2ef33-159">This change affects the current connector group only.</span></span> <span data-ttu-id="2ef33-160">Можно продолжить использовать этот же функциональный профиль в других группах соединителей.</span><span class="sxs-lookup"><span data-stu-id="2ef33-160">You can continue using the same functional profile in other connector groups.</span></span>

     >[!NOTE]
     > <span data-ttu-id="2ef33-161">В группе соединителей каждый финансовый соединитель может иметь только один функциональный профиль.</span><span class="sxs-lookup"><span data-stu-id="2ef33-161">Within a connector group, each fiscal connector can only have one functional profile.</span></span>

- <span data-ttu-id="2ef33-162">Создайте **Технический профиль соединителя** в **Retail > Настройка канала > Финансовая интеграция > Технические профили соединителей** для каждого финансового соединителя.</span><span class="sxs-lookup"><span data-stu-id="2ef33-162">Create a **Connector technical profile** in **Retail > Channel setup > Fiscal integration > Connector technical profiles** for each fiscal connector.</span></span>
  - <span data-ttu-id="2ef33-163">Выберите название соединителя.</span><span class="sxs-lookup"><span data-stu-id="2ef33-163">Select a connector name.</span></span>
  - <span data-ttu-id="2ef33-164">Выберите тип соединителя:</span><span class="sxs-lookup"><span data-stu-id="2ef33-164">Select a connector type:</span></span> 
      - <span data-ttu-id="2ef33-165">**Локальный** — задавайте этот тип для физических устройств или приложений, установленных на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="2ef33-165">**Local** - Set this type for physical devices or applications installed on a local machine.</span></span>
      - <span data-ttu-id="2ef33-166">**Внутренний** — задавайте этот тип для финансовых устройств и служб, подключенных к Retail Server.</span><span class="sxs-lookup"><span data-stu-id="2ef33-166">**Internal** - Set this type for fiscal devices and services connected to Retail Server.</span></span>
      - <span data-ttu-id="2ef33-167">**Внешний** — для внешних финансовых служб, таких как веб-портал, предоставленный налоговым органом.</span><span class="sxs-lookup"><span data-stu-id="2ef33-167">**External** - For external fiscal services like a web-portal provided by a tax authority.</span></span>
    
  - <span data-ttu-id="2ef33-168">Укажите параметры на вкладке **Подключение**.</span><span class="sxs-lookup"><span data-stu-id="2ef33-168">Specify settings on the **Connection** tab.</span></span>

      
 >[!NOTE]
 > <span data-ttu-id="2ef33-169">Обновленная версия конфигурации, которая была загружена ранее, будет загружена для функциональных и технических профилей.</span><span class="sxs-lookup"><span data-stu-id="2ef33-169">An updated version of a configuration that was loaded earlier will be loaded for both functional and technical profiles.</span></span> <span data-ttu-id="2ef33-170">Если соответствующий соединитель или поставщик документов уже используется, вы будете оповещены.</span><span class="sxs-lookup"><span data-stu-id="2ef33-170">If an appropriate connector or document provider is already in use, you will be notified.</span></span> <span data-ttu-id="2ef33-171">По умолчанию все изменения, сделанные вручную в функциональных и технических профилях, будут сохранены.</span><span class="sxs-lookup"><span data-stu-id="2ef33-171">By default, all changes that have been made manually in functional and technical profiles will be stored.</span></span> <span data-ttu-id="2ef33-172">Чтобы переопределить эти профили с набором параметров по умолчанию из конфигурации, нажмите кнопку **Обновить** на странице **Функциональные профили соединителей** и **Технические профили соединителей**.</span><span class="sxs-lookup"><span data-stu-id="2ef33-172">In order to override these profiles with the default set of parameters from a configuration, click **Update** on the **Connector functional profiles** page and **Connector technical profiles** page.</span></span>
 
- <span data-ttu-id="2ef33-173">Создайте **Процесс финансовой регистрации** в пункте **Retail > Настройка канала > Финансовая интеграция > Процессы финансовой регистрации** для каждого уникального процесса финансовой интеграции.</span><span class="sxs-lookup"><span data-stu-id="2ef33-173">Create a **Fiscal registration process** in **Retail > Channel setup > Fiscal integration > Fiscal registration processes** for each unique process of the fiscal integration.</span></span> <span data-ttu-id="2ef33-174">Процесс регистрации определяется последовательностью шагов регистрации и группой соединителей, используемых на каждом шаге.</span><span class="sxs-lookup"><span data-stu-id="2ef33-174">A registration process is defined by the sequence of the registration steps and the connector group used on each step.</span></span> 
  
  - <span data-ttu-id="2ef33-175">Добавьте шаги регистрации в процесс:</span><span class="sxs-lookup"><span data-stu-id="2ef33-175">Add registration steps to the process:</span></span>
      - <span data-ttu-id="2ef33-176">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="2ef33-176">Click **Add**.</span></span>
      - <span data-ttu-id="2ef33-177">Выберите тип соединителя.</span><span class="sxs-lookup"><span data-stu-id="2ef33-177">Select a connector type.</span></span>
      
      >[!NOTE]
      > <span data-ttu-id="2ef33-178">Это поле определяет, где система будет искать технический профиль для соединителя, в аппаратных профилях для типа соединителя **Локальный** или в функциональных профилях POS для других типов финансовых соединителей.</span><span class="sxs-lookup"><span data-stu-id="2ef33-178">This field defines where the system will search in a technical profile for the connector, either in hardware profiles for connector type **Local**, or in POS functionality profiles for other fiscal connector types.</span></span>
      
   - <span data-ttu-id="2ef33-179">Выберите группу соединителей.</span><span class="sxs-lookup"><span data-stu-id="2ef33-179">Select a connector group.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="2ef33-180">Щелкните **Проверить** для проверки целостности структуры процесса регистрации.</span><span class="sxs-lookup"><span data-stu-id="2ef33-180">Click **Validate** to check the integrity of the registration process structure.</span></span> <span data-ttu-id="2ef33-181">Рекомендуется, чтобы проверки осуществлялись в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="2ef33-181">It’s recommended that validations be made in the following cases:</span></span>
       >- <span data-ttu-id="2ef33-182">Для нового процесса регистрации после всех заполненных настроек, включая привязки к профилям функциональности POS и профилям оборудования.</span><span class="sxs-lookup"><span data-stu-id="2ef33-182">For a new registration process after all the settings are completed, including binding to POS functionality profiles and hardware profiles.</span></span>
       >- <span data-ttu-id="2ef33-183">После выполнения обновления существующего процесса регистрации.</span><span class="sxs-lookup"><span data-stu-id="2ef33-183">After making updates to an existing registration process.</span></span>

-  <span data-ttu-id="2ef33-184">Свяжите процессы финансовой регистрации с профилями функциональности POS в **Retail > Настройка канала > Настройка POS > Профили POS > Профили функциональности**.</span><span class="sxs-lookup"><span data-stu-id="2ef33-184">Bind fiscal registration processes to POS functionality profiles in **Retail > Channel setup > POS setup > POS profiles > Functionality profiles**.</span></span>
   - <span data-ttu-id="2ef33-185">Щелкните **Изменить** и выберите **Номер процесса** на вкладке **Процесс финансовой регистрации**.</span><span class="sxs-lookup"><span data-stu-id="2ef33-185">Click **Edit** and select a **Process number** on the **Fiscal registration process** tab.</span></span>
- <span data-ttu-id="2ef33-186">Свяжите технические профили соединителей с профилями оборудования в пункте **Retail > Настройка канала > Настройка POS > Профили POS > Профили оборудования**.</span><span class="sxs-lookup"><span data-stu-id="2ef33-186">Bind the connector technical profiles to the hardware profiles in **Retail > Channel setup > POS setup > POS profiles > Hardware profiles**.</span></span>
   - <span data-ttu-id="2ef33-187">Щелкните **Изменить**, затем щелкните **Создать** на вкладке **Финансовый технический профиль**.</span><span class="sxs-lookup"><span data-stu-id="2ef33-187">Click **Edit**, then click **New** on the **Fiscal technical profile** tab.</span></span>
   - <span data-ttu-id="2ef33-188">Выберите технический профиль соединителя в поле **Номер профиля**.</span><span class="sxs-lookup"><span data-stu-id="2ef33-188">Select a connector technical profile in the **Profile number** field.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="2ef33-189">Можно добавить несколько технических профилей к профилю оборудования.</span><span class="sxs-lookup"><span data-stu-id="2ef33-189">You can add several technical profiles to a hardware profile.</span></span> <span data-ttu-id="2ef33-190">Однако это не поддерживается, если профиль оборудования имеет более одного пересечение с любой из групп соединителей.</span><span class="sxs-lookup"><span data-stu-id="2ef33-190">However, this is not supported if a hardware profile has more than one intersection with any connector group.</span></span> <span data-ttu-id="2ef33-191">Чтобы избежать неверных настроек, рекомендуется проверить процесс регистрации после обновления всех профилей оборудования.</span><span class="sxs-lookup"><span data-stu-id="2ef33-191">To avoid incorrect settings, it’s recommended that you validate the registration process after updating all the hardware profiles.</span></span>

