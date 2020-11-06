---
title: Устранение неполадок, связанных с обновлениями приложений Finance and Operations
description: В этом разделе содержатся сведения об устранении неполадок, связанных с обновлениями приложений Finance and Operations.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 07d6bd0bab796d7839daa2bad91f7e88c2e881b5
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997926"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="85a4e-103">Устранение неполадок, связанных с обновлениями приложений Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="85a4e-103">Troubleshoot issues related to upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="85a4e-104">Эта тема предоставляет информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="85a4e-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="85a4e-105">Конкретно, в этом разделе содержатся сведения об устранении неполадок, связанных с обновлениями приложений Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="85a4e-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85a4e-106">Для некоторых вопросов, связанных с этим разделом, может потребоваться роль системного администратора или учетные данные администратора клиента Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="85a4e-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="85a4e-107">В разделе для каждого выпуска объясняется, требуются ли конкретная роль или учетные данные.</span><span class="sxs-lookup"><span data-stu-id="85a4e-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="85a4e-108">Ошибки синхронизации баз данных</span><span class="sxs-lookup"><span data-stu-id="85a4e-108">Database synchronization errors</span></span>

<span data-ttu-id="85a4e-109">**Роль, требуемая для исправления ошибки:** системный администратор</span><span class="sxs-lookup"><span data-stu-id="85a4e-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="85a4e-110">При попытке использовать объект **DualWriteProjectConfiguration** для обновления приложения Finance and Operations до обновления платформы Platform update 30, может появиться сообщение об ошибке, которое напоминает следующий пример.</span><span class="sxs-lookup"><span data-stu-id="85a4e-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** entity to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="85a4e-111">Чтобы устранить проблему, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="85a4e-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="85a4e-112">Выполните вход в виртуальную машину для приложения Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="85a4e-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="85a4e-113">Откройте Visual Studio в качестве администратора и откройте репозиторий прикладных объектов (AOT).</span><span class="sxs-lookup"><span data-stu-id="85a4e-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="85a4e-114">Выполните поиск **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="85a4e-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="85a4e-115">В AOT щелкните правой кнопкой мыши **DualWriteProjectConfiguration** и выберите **Добавить в новый проект**.</span><span class="sxs-lookup"><span data-stu-id="85a4e-115">In the AOT, right-click **DualWriteProjectConfiguration** , and select **Add to new project**.</span></span> <span data-ttu-id="85a4e-116">Выберите **ОК** , чтобы создать новый проект, в котором используются параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="85a4e-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="85a4e-117">В обозревателе решений щелкните правой кнопкой мыши **Свойства проекта** и задайте для параметры **Синхронизация базы данных при сборке** значение **True**.</span><span class="sxs-lookup"><span data-stu-id="85a4e-117">In Solution Explorer, right-click **Project properties** , and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="85a4e-118">Выполните сборку проекта и проверьте, что сборка выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="85a4e-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="85a4e-119">В меню **Dynamics 365** выберите **Синхронизировать базу данных**.</span><span class="sxs-lookup"><span data-stu-id="85a4e-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="85a4e-120">Выберите **Синхронизировать** для выполнения полной синхронизации базы данных.</span><span class="sxs-lookup"><span data-stu-id="85a4e-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="85a4e-121">После успешного завершения полной синхронизации базы данных перезапустите этап синхронизации базы данных в службах Microsoft Dynamics Lifecycle Services (LCS) и используйте требуемые сценарии обновления вручную, чтобы можно было продолжить обновление.</span><span class="sxs-lookup"><span data-stu-id="85a4e-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-entity-fields-issue-on-maps"></a><span data-ttu-id="85a4e-122">Проблема с отсутствующими полями объекта на картах</span><span class="sxs-lookup"><span data-stu-id="85a4e-122">Missing entity fields issue on maps</span></span>

<span data-ttu-id="85a4e-123">**Роль, требуемая для исправления ошибки:** системный администратор</span><span class="sxs-lookup"><span data-stu-id="85a4e-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="85a4e-124">На странице **Двойная запись** может быть выведено сообщение об ошибке, подобное следующему примеру:</span><span class="sxs-lookup"><span data-stu-id="85a4e-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="85a4e-125">*Отсутствует исходное поле \<field name\> в схеме.*</span><span class="sxs-lookup"><span data-stu-id="85a4e-125">*Missing source field \<field name\> in the schema.*</span></span>

![Пример сообщения об ошибке об отсутствующем исходном поле](media/error_missing_field.png)

<span data-ttu-id="85a4e-127">Чтобы устранить проблему, сначала необходимо выполнить следующие действия, чтобы убедиться в наличии полей в объекте.</span><span class="sxs-lookup"><span data-stu-id="85a4e-127">To fix the issue, first follow these steps to make sure that the fields are in the entity.</span></span>

1. <span data-ttu-id="85a4e-128">Выполните вход в виртуальную машину для приложения Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="85a4e-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="85a4e-129">Выберите **Рабочие области \> Управление данными** , выберите плитку **Параметры структуры** , затем на вкладке **Параметры объекта** выберите **Обновить список объектов** , чтобы обновить объекты.</span><span class="sxs-lookup"><span data-stu-id="85a4e-129">Go to **Workspaces \> Data management** , select the **Framework parameters** tile, and then, on the **Entity settings** tab, select **Refresh entity list** to refresh the entities.</span></span>
3. <span data-ttu-id="85a4e-130">Выберите **Рабочие области \> Управление данными** , выберите вкладку **Объекты данных** и убедитесь, что объект указан в списке.</span><span class="sxs-lookup"><span data-stu-id="85a4e-130">Go to **Workspaces \> Data management** , select the **Data entities** tab, and make sure that the entity is listed.</span></span> <span data-ttu-id="85a4e-131">Если объект отсутствует в списке, выполните вход в виртуальную машину для приложения Finance and Operations и убедитесь, что объект доступен.</span><span class="sxs-lookup"><span data-stu-id="85a4e-131">If the entity isn't listed, sign in to the VM for the Finance and Operations app, and make sure the entity is available.</span></span>
4. <span data-ttu-id="85a4e-132">Откройте страницу **Сопоставление объектов** со страницы **Двойная запись** в приложении Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="85a4e-132">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="85a4e-133">Выберите **Обновить список объектов** , чтобы автоматически заполнить поля в сопоставлениях объектов.</span><span class="sxs-lookup"><span data-stu-id="85a4e-133">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>

<span data-ttu-id="85a4e-134">Если проблема все еще не устранена, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="85a4e-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85a4e-135">В этих шагах выполняется процедура удаления объекта и добавления его снова.</span><span class="sxs-lookup"><span data-stu-id="85a4e-135">These steps guide you through the process of deleting an entity and then adding it again.</span></span> <span data-ttu-id="85a4e-136">Чтобы избежать проблем, обязательно точно выполните описанные шаги.</span><span class="sxs-lookup"><span data-stu-id="85a4e-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="85a4e-137">В приложении Finance and Operations перейдите к пункту **Рабочие области \> Управление данными** и выберите плитку **Объекты данных**.</span><span class="sxs-lookup"><span data-stu-id="85a4e-137">In the Finance and Operations app, go to **Workspaces \> Data management** , and select the **Data entities** tile.</span></span>
2. <span data-ttu-id="85a4e-138">Найдите объект, в котором отсутствует атрибут.</span><span class="sxs-lookup"><span data-stu-id="85a4e-138">Find the entity that is missing the attribute.</span></span> <span data-ttu-id="85a4e-139">Нажмите **Изменить целевое сопоставление** на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="85a4e-139">Click **Modify target mapping** in the toolbar.</span></span>
3. <span data-ttu-id="85a4e-140">В области **Сопоставить промежуточные данные с целевыми** щелкните **Создать сопоставление**.</span><span class="sxs-lookup"><span data-stu-id="85a4e-140">On the **Map staging to target** pane, click **Generate mapping**.</span></span>
4. <span data-ttu-id="85a4e-141">Откройте страницу **Сопоставление объектов** со страницы **Двойная запись** в приложении Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="85a4e-141">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="85a4e-142">Если атрибут не был автоматически заполнен в сопоставлении, добавьте его вручную, нажав кнопку **Добавить атрибут** , затем щелкнув **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="85a4e-142">If the attribute is not auto-populated on the map, add it manually by clicking **Add attribute** button and then clicking **Save**.</span></span> 
6. <span data-ttu-id="85a4e-143">Выберите сопоставление и щелкните **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="85a4e-143">Select the map and click **Run**.</span></span>
