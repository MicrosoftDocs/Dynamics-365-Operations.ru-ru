---
title: (Электронная отчетность) Импорт конфигураций из RCS
description: В этом разделе содержатся сведения о том, как пользователь может импортировать новую версию конфигурации ER из RCS.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c458cf815837fb7e4688c4c0443b7962cac403a5
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727014"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="86413-103">(Электронная отчетность) Импорт конфигураций из RCS</span><span class="sxs-lookup"><span data-stu-id="86413-103">(ER) Import configurations from RCS</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="86413-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может импортировать новую конфигурацию электронной отчетности из Microsoft Regulatory Configuration Services (RCS).</span><span class="sxs-lookup"><span data-stu-id="86413-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="86413-105">В этом примере будет выбрана версия конфигурации ER, которая была настроена в экземпляре RCS, и импортирована в текущий экземпляр Finance and Operations для демонстрационной компании Litware, Inc. Эти шаги могут быть выполнены в любой компании, поскольку конфигурации ER используются совместно несколькими компаниями.</span><span class="sxs-lookup"><span data-stu-id="86413-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current Finance and Operations instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="86413-106">Для выполнения этих шагов необходимо сначала выполнить шаги в теме [Создание поставщика конфигурации и установка его в качестве активного](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="86413-106">To complete these steps, you must first complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="86413-107">Для выполнения этих шагов необходимо также иметь доступ к экземпляру RCS, содержащему хотя бы одну конфигурацию ER в состоянии **Завершено** или **Предоставлен общий доступ**.</span><span class="sxs-lookup"><span data-stu-id="86413-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="86413-108">Перейдите в раздел **Управление организацией** > **Рабочие области** > **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="86413-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="86413-109">Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как **Активный**.</span><span class="sxs-lookup"><span data-stu-id="86413-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="86413-110">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в разделе [Создание поставщика конфигурации и пометка его как активного](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="86413-110">If you don’t see this configuration provider, complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="86413-111">Если у вас нет среды RCS, подготовленной для вашей компании, щелкните внешнюю ссылку **Regulatory Services — конфигурация** и следуйте инструкциям по подготовке среды RCS.</span><span class="sxs-lookup"><span data-stu-id="86413-111">If you have no RCS environment provisioned to your company, click **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="86413-112">Щелкните **Параметры электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="86413-112">Click **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="86413-113">Перейдите на вкладку **RCS**.</span><span class="sxs-lookup"><span data-stu-id="86413-113">Click the **RCS** tab.</span></span> 
6. <span data-ttu-id="86413-114">Если среда RCS уже подготовлена для вашей компании, используйте представленные URL-адреса страниц для доступа к ней.</span><span class="sxs-lookup"><span data-stu-id="86413-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="86413-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="86413-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="86413-116">Зарегистрируйте новый репозиторий электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="86413-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="86413-117">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="86413-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="86413-118">Выберите поставщика Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="86413-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="86413-119">Щелкните "Репозитории".</span><span class="sxs-lookup"><span data-stu-id="86413-119">Click Repositories.</span></span> 
4. <span data-ttu-id="86413-120">Щелкните "Добавить", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="86413-120">Click Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="86413-121">В поле "Тип репозитория конфигурации" введите "RCS".</span><span class="sxs-lookup"><span data-stu-id="86413-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="86413-122">Щелкните "Создать репозиторий".</span><span class="sxs-lookup"><span data-stu-id="86413-122">Click Create repository.</span></span> 
7. <span data-ttu-id="86413-123">В поле отображаемого имени среды RCS введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="86413-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="86413-124">Выберите требуемый экземпляр RCS.</span><span class="sxs-lookup"><span data-stu-id="86413-124">Select the desired RCS instance.</span></span> <span data-ttu-id="86413-125">Обратите внимание, что у вас их может быть несколько.</span><span class="sxs-lookup"><span data-stu-id="86413-125">Note that you can have several of them.</span></span> 
9. <span data-ttu-id="86413-126">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="86413-126">Click OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="86413-127">Импорт конфигураций электронной отчетности из репозитория на основе RCS</span><span class="sxs-lookup"><span data-stu-id="86413-127">Import ER configurations from RCS based repository</span></span>
1. <span data-ttu-id="86413-128">Щелкните **Показать фильтры**.</span><span class="sxs-lookup"><span data-stu-id="86413-128">Click **Show filters**.</span></span> 
2. <span data-ttu-id="86413-129">Введите значение фильтрации "RCS" в поле **Имя** с помощью оператора фильтра **начинается с**.</span><span class="sxs-lookup"><span data-stu-id="86413-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="86413-130">Когда вы открываете выбранный репозиторий, на странице **Подключение к Regulatory Configuration Services** щелкните ссылку **Щелкните здесь, чтобы подключиться к службам Regulatory Configuration Services**.</span><span class="sxs-lookup"><span data-stu-id="86413-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, click **Click here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="86413-131">Щелкните **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="86413-131">Click **Open**.</span></span> 
5. <span data-ttu-id="86413-132">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="86413-132">Click **Close**.</span></span> 
6. <span data-ttu-id="86413-133">Выберите нужную версию конфигурации ER и щелкните **Импорт**, чтобы переместить ее в текущий экземпляр Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="86413-133">Select the desired version of ER configuration and click **Import** to bring it in the current Finance and Operations instance.</span></span>

