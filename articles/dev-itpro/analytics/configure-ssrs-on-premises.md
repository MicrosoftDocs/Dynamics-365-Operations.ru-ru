---
title: Настройка служб SQL Server Reporting Services для локальных развертываний
description: В этой теме представлены сведения о настройке служб SQL Server Reporting Services (SSRS) для локального развертывания.
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 166d419f16866f699b96013222ce8da147a5ec21
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548727"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a><span data-ttu-id="ec40b-103">Настройка служб SQL Server Reporting Services для локальных развертываний</span><span class="sxs-lookup"><span data-stu-id="ec40b-103">Configure SQL Server Reporting Services for on-premises deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec40b-104">Используйте шаги, приведенные ранее в этой теме, для настройки служб SQL Server Reporting Services (SSRS) для развертывания Microsoft Dynamics 365 for Finance and Operations (локальная версия).</span><span class="sxs-lookup"><span data-stu-id="ec40b-104">Use the steps in this topic to configure SQL Server Reporting Services (SSRS) for your Microsoft Dynamics 365 for Finance and Operations (on-premises) deployment.</span></span>

1. <span data-ttu-id="ec40b-105">Откройте приложение "Диспетчер конфигурации Reporting Services".</span><span class="sxs-lookup"><span data-stu-id="ec40b-105">Open the Reporting Services Configuration Manager application.</span></span>
2. <span data-ttu-id="ec40b-106">Оставьте значение по умолчанию **Имя сервера**, которое должно представлять собой имя текущего компьютера, и **Экземпляра сервера отчетов**, **MSSQLSERVER**.</span><span class="sxs-lookup"><span data-stu-id="ec40b-106">Leave the default **Server name**, which should be the name of the current machine, and the **Report Server Instance**, **MSSQLSERVER**.</span></span>
3. <span data-ttu-id="ec40b-107">Щелкните **Подключить**.</span><span class="sxs-lookup"><span data-stu-id="ec40b-107">Click **Connect**.</span></span>

    <span data-ttu-id="ec40b-108">[![Подключение конфигурации Reporting Services](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span><span class="sxs-lookup"><span data-stu-id="ec40b-108">[![Reporting services configuration connection](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span></span>

4. <span data-ttu-id="ec40b-109">Щелкните вкладку **Учетная запись службы** и убедитесь, что параметры соответствуют приведенному ниже рисунку.</span><span class="sxs-lookup"><span data-stu-id="ec40b-109">Click the **Service Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="ec40b-110">[![Вкладка "Учетная запись службы"](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span><span class="sxs-lookup"><span data-stu-id="ec40b-110">[![Service account tab](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span></span>

5. <span data-ttu-id="ec40b-111">Щелкните вкладку **URL-адрес веб-службы** и убедитесь, что параметры соответствуют приведенному ниже рисунку.</span><span class="sxs-lookup"><span data-stu-id="ec40b-111">Click the **Web Service URL** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="ec40b-112">[![Вкладка "URL-адрес веб-службы"](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span><span class="sxs-lookup"><span data-stu-id="ec40b-112">[![Web service URL tab](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span></span>

6. <span data-ttu-id="ec40b-113">Щелкните вкладку **База данных** и убедитесь, что значения **Имя базы данных** и **Параметры учетных данных** соответствуют приведенному ниже рисунку.</span><span class="sxs-lookup"><span data-stu-id="ec40b-113">Click the **Database** tab and verify that the **Database Name** and **Credential settings** match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ec40b-114">Понадобится создать новую базу данных.</span><span class="sxs-lookup"><span data-stu-id="ec40b-114">You will need to create a new database.</span></span> <span data-ttu-id="ec40b-115">Для этого щелкните **Изменить базу данных**, а затем убедитесь, что имя новой базы данных: **DynamicsAxReportServer**.</span><span class="sxs-lookup"><span data-stu-id="ec40b-115">To do this, click **Change Database**, and then verify that the new database name is: **DynamicsAxReportServer**.</span></span>

    <span data-ttu-id="ec40b-116">[![вкладка "База данных"](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span><span class="sxs-lookup"><span data-stu-id="ec40b-116">[![database tab](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span></span>

7. <span data-ttu-id="ec40b-117">Щелкните вкладку **URL-адрес веб-портала** и убедитесь, что параметры соответствуют приведенному ниже рисунку.</span><span class="sxs-lookup"><span data-stu-id="ec40b-117">Click the **Web Portal URL** tab and verify that the settings match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ec40b-118">Необходимо нажать **Применить** для создания и правильной настройки портала.</span><span class="sxs-lookup"><span data-stu-id="ec40b-118">You must click **Apply** to create and properly configure the Portal.</span></span>

    <span data-ttu-id="ec40b-119">[![вкладка "URL-адрес веб-портала"](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span><span class="sxs-lookup"><span data-stu-id="ec40b-119">[![web portal url tab](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span></span>

    <span data-ttu-id="ec40b-120">После настройки портала вкладка **Веб-портал** будет соответствовать приведенному ниже рисунку.</span><span class="sxs-lookup"><span data-stu-id="ec40b-120">After the Portal is configured, the **Web Portal** tab will match the following graphic.</span></span>

    <span data-ttu-id="ec40b-121">[![вкладка "Веб-портал"](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span><span class="sxs-lookup"><span data-stu-id="ec40b-121">[![web portal tab](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span></span>

8. <span data-ttu-id="ec40b-122">Перейдите по URL-адресу отчетов для просмотра веб-портал SQL Server Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="ec40b-122">Click the reports URL to view the SQL Server Reporting Services web portal.</span></span>
9. <span data-ttu-id="ec40b-123">Находясь на портале, создайте новую папку с именем **Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="ec40b-123">When you are in the portal, create a new folder named **Dynamics**.</span></span>

    <span data-ttu-id="ec40b-124">[![папка Dynamics](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span><span class="sxs-lookup"><span data-stu-id="ec40b-124">[![dynamics folder](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span></span>

10. <span data-ttu-id="ec40b-125">В разделе **Диспетчер конфигурации служб Reporting Services** щелкните вкладку **Параметры электронной почты** и убедитесь, что параметры соответствуют приведенному ниже рисунку.</span><span class="sxs-lookup"><span data-stu-id="ec40b-125">In the **Reporting Services Configuration Manager**, click the **E-mail Settings** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="ec40b-126">[![вкладка "Параметры электронной почты"](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span><span class="sxs-lookup"><span data-stu-id="ec40b-126">[![email settings tab](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span></span>

11. <span data-ttu-id="ec40b-127">Щелкните вкладку **Учетная запись для выполнения** и убедитесь, что параметры соответствуют приведенному ниже рисунку.</span><span class="sxs-lookup"><span data-stu-id="ec40b-127">Click the **Execution Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="ec40b-128">[![вкладка "Учетная запись для выполнения"](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span><span class="sxs-lookup"><span data-stu-id="ec40b-128">[![execution account tab](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span></span>

    <span data-ttu-id="ec40b-129">Не следует изменять параметры по умолчанию на вкладке **Ключи шифрования**.</span><span class="sxs-lookup"><span data-stu-id="ec40b-129">Don't change the default settings on the **Encryption Keys** tab.</span></span>

    <span data-ttu-id="ec40b-130">[![вкладка "Ключи шифрования"](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span><span class="sxs-lookup"><span data-stu-id="ec40b-130">[![encryption keys tab](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span></span>

12. <span data-ttu-id="ec40b-131">Щелкните вкладку **Параметры подписки** и убедитесь, что параметры соответствуют приведенному ниже рисунку.</span><span class="sxs-lookup"><span data-stu-id="ec40b-131">Click the **Subscription Settings** tab, and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="ec40b-132">[![вкладка "Параметры подписки"](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span><span class="sxs-lookup"><span data-stu-id="ec40b-132">[![subscription settings tab](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span></span>

    <span data-ttu-id="ec40b-133">Не следует изменять параметры по умолчанию на вкладке **Масштабное развертывание**.</span><span class="sxs-lookup"><span data-stu-id="ec40b-133">Don't change the default settings on the **Scale-out Deployment** tab.</span></span>

    <span data-ttu-id="ec40b-134">[![вкладка "Масштабное развертывание"](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span><span class="sxs-lookup"><span data-stu-id="ec40b-134">[![scale-out deployment tab](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span></span>

    <span data-ttu-id="ec40b-135">Не следует изменять параметры по умолчанию на вкладке **Интеграция с Power BI**.</span><span class="sxs-lookup"><span data-stu-id="ec40b-135">Don't change the default settings on the **Power BI Integration** tab.</span></span>

    <span data-ttu-id="ec40b-136">[![вкладка "Интеграция с Power BI"](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span><span class="sxs-lookup"><span data-stu-id="ec40b-136">[![power bi integration tab](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span></span>

13. <span data-ttu-id="ec40b-137">Щелкните **Выход**, чтобы закрыть **Диспетчер конфигурации Reporting Services**.</span><span class="sxs-lookup"><span data-stu-id="ec40b-137">Click **Exit** to close the **Reporting Services Configuration Manager**.</span></span>

    <span data-ttu-id="ec40b-138">[![закрытие диспетчера конфигурации служб Reporting Services](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span><span class="sxs-lookup"><span data-stu-id="ec40b-138">[![close reporting services configuration manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span></span>
