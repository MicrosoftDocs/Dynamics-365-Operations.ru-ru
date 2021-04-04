---
title: (Электронная отчетность) Импорт конфигураций из RCS
description: В этом разделе содержатся сведения о том, как пользователь может импортировать новую версию конфигурации ER из RCS.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 799abeafe5f0929e6dd2f8a5f437f3c10b3b06d9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570544"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="24ee3-103">(Электронная отчетность) Импорт конфигураций из RCS</span><span class="sxs-lookup"><span data-stu-id="24ee3-103">(ER) Import configurations from RCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="24ee3-104">В следующих шагах поясняется, как пользователь с ролью "Системный администратор" или "Разработчик электронной отчетности" может импортировать новую конфигурацию электронной отчетности из Microsoft Regulatory Configuration Services (RCS).</span><span class="sxs-lookup"><span data-stu-id="24ee3-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="24ee3-105">В этом примере будет выбрана версия конфигурации ER, которая была настроена в экземпляре RCS, и импортирована в текущий экземпляр для демонстрационной компании Litware, Inc. Эти шаги могут быть выполнены в любой компании, поскольку конфигурации ER используются совместно несколькими компаниями.</span><span class="sxs-lookup"><span data-stu-id="24ee3-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="24ee3-106">Для выполнения этих шагов необходимо сначала выполнить шаги в теме [Создание поставщиков конфигурации и установка их в качестве активных](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="24ee3-106">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="24ee3-107">Для выполнения этих шагов необходимо также иметь доступ к экземпляру RCS, содержащему хотя бы одну конфигурацию ER в состоянии **Завершено** или **Предоставлен общий доступ**.</span><span class="sxs-lookup"><span data-stu-id="24ee3-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="24ee3-108">Перейдите в раздел **Управление организацией** > **Рабочие области** > **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="24ee3-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="24ee3-109">Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как **Активный**.</span><span class="sxs-lookup"><span data-stu-id="24ee3-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="24ee3-110">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в теме [Создание поставщиков конфигурации и пометка их как активных](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="24ee3-110">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="24ee3-111">Если у вас нет среды RCS, подготовленной для вашей компании, выберите внешнюю ссылку **Regulatory Services — конфигурация** и следуйте инструкциям по подготовке среды RCS.</span><span class="sxs-lookup"><span data-stu-id="24ee3-111">If you have no RCS environment provisioned to your company, select **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="24ee3-112">Выберите **Параметры электронной отчетности**.</span><span class="sxs-lookup"><span data-stu-id="24ee3-112">Select **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="24ee3-113">Выберите вкладку **RCS**.</span><span class="sxs-lookup"><span data-stu-id="24ee3-113">Select the **RCS** tab.</span></span> 
6. <span data-ttu-id="24ee3-114">Если среда RCS уже подготовлена для вашей компании, используйте представленные URL-адреса страниц для доступа к ней.</span><span class="sxs-lookup"><span data-stu-id="24ee3-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="24ee3-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="24ee3-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="24ee3-116">Зарегистрируйте новый репозиторий электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="24ee3-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="24ee3-117">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="24ee3-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="24ee3-118">Выберите поставщика Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="24ee3-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="24ee3-119">Выберите Репозитории.</span><span class="sxs-lookup"><span data-stu-id="24ee3-119">Select Repositories.</span></span> 
4. <span data-ttu-id="24ee3-120">Выберите Добавить, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="24ee3-120">Select Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="24ee3-121">В поле "Тип репозитория конфигурации" введите "RCS".</span><span class="sxs-lookup"><span data-stu-id="24ee3-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="24ee3-122">Выберите Создать репозиторий.</span><span class="sxs-lookup"><span data-stu-id="24ee3-122">Select Create repository.</span></span> 
7. <span data-ttu-id="24ee3-123">В поле отображаемого имени среды RCS введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="24ee3-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="24ee3-124">Выберите требуемый экземпляр RCS.</span><span class="sxs-lookup"><span data-stu-id="24ee3-124">Select the desired RCS instance.</span></span> <span data-ttu-id="24ee3-125">У вас их может быть несколько.</span><span class="sxs-lookup"><span data-stu-id="24ee3-125">You can have several of them.</span></span> 
9. <span data-ttu-id="24ee3-126">Нажмите ОК.</span><span class="sxs-lookup"><span data-stu-id="24ee3-126">Select OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="24ee3-127">Импорт конфигураций электронной отчетности из репозитория на основе RCS</span><span class="sxs-lookup"><span data-stu-id="24ee3-127">Import ER configurations from RCS-based repository</span></span>
1. <span data-ttu-id="24ee3-128">Выберите **Показать фильтры**.</span><span class="sxs-lookup"><span data-stu-id="24ee3-128">Select **Show filters**.</span></span> 
2. <span data-ttu-id="24ee3-129">Введите значение фильтрации "RCS" в поле **Имя** с помощью оператора фильтра **начинается с**.</span><span class="sxs-lookup"><span data-stu-id="24ee3-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="24ee3-130">Когда вы открываете выбранный репозиторий, на странице **Подключение к Regulatory Configuration Services** выберите ссылку **Выберите здесь, чтобы подключиться к службам Regulatory Configuration Services**.</span><span class="sxs-lookup"><span data-stu-id="24ee3-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, select **Select here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="24ee3-131">Выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="24ee3-131">Select **Open**.</span></span> 
5. <span data-ttu-id="24ee3-132">Выберите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="24ee3-132">Select **Close**.</span></span> 
6. <span data-ttu-id="24ee3-133">Выберите нужную версию конфигурации ER и выберите **Импорт**, чтобы переместить ее в текущий экземпляр.</span><span class="sxs-lookup"><span data-stu-id="24ee3-133">Select the desired version of ER configuration and select **Import** to bring it in the current instance.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]