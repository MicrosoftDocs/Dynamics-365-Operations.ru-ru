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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 59384d8e8d043eb14231a471c7218ced2dddf739
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172885"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="8fc38-103">Устранение неполадок, связанных с обновлениями приложений Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8fc38-103">Troubleshoot issues related to upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="8fc38-104">Эта тема предоставляет информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8fc38-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="8fc38-105">Конкретно, в этом разделе содержатся сведения об устранении неполадок, связанных с обновлениями приложений Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8fc38-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8fc38-106">Для некоторых вопросов, связанных с этим разделом, может потребоваться роль системного администратора или учетные данные администратора клиента Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="8fc38-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="8fc38-107">В разделе для каждого выпуска объясняется, требуются ли конкретная роль или учетные данные.</span><span class="sxs-lookup"><span data-stu-id="8fc38-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="8fc38-108">Ошибки синхронизации баз данных</span><span class="sxs-lookup"><span data-stu-id="8fc38-108">Database synchronization errors</span></span>

<span data-ttu-id="8fc38-109">**Роль, требуемая для исправления ошибки:** системный администратор</span><span class="sxs-lookup"><span data-stu-id="8fc38-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="8fc38-110">При попытке использовать объект **DualWriteProjectConfiguration** для обновления приложения Finance and Operations до обновления платформы Platform update 30, может появиться сообщение об ошибке, которое напоминает следующий пример.</span><span class="sxs-lookup"><span data-stu-id="8fc38-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** entity to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="8fc38-111">Чтобы устранить проблему, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8fc38-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="8fc38-112">Выполните вход в виртуальную машину для приложения Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8fc38-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="8fc38-113">Откройте Visual Studio в качестве администратора и откройте репозиторий прикладных объектов (AOT).</span><span class="sxs-lookup"><span data-stu-id="8fc38-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="8fc38-114">Выполните поиск **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="8fc38-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="8fc38-115">В AOT щелкните правой кнопкой мыши **DualWriteProjectConfiguration** и выберите **Добавить в новый проект**.</span><span class="sxs-lookup"><span data-stu-id="8fc38-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="8fc38-116">Выберите **ОК**, чтобы создать новый проект, в котором используются параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8fc38-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="8fc38-117">В обозревателе решений щелкните правой кнопкой мыши **Свойства проекта** и задайте для параметры **Синхронизация базы данных при сборке** значение **True**.</span><span class="sxs-lookup"><span data-stu-id="8fc38-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="8fc38-118">Выполните сборку проекта и проверьте, что сборка выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8fc38-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="8fc38-119">В меню **Dynamics 365** выберите **Синхронизировать базу данных**.</span><span class="sxs-lookup"><span data-stu-id="8fc38-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="8fc38-120">Выберите **Синхронизировать** для выполнения полной синхронизации базы данных.</span><span class="sxs-lookup"><span data-stu-id="8fc38-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="8fc38-121">После успешного завершения полной синхронизации базы данных перезапустите этап синхронизации базы данных в службах Microsoft Dynamics Lifecycle Services (LCS) и используйте требуемые сценарии обновления вручную, чтобы можно было продолжить обновление.</span><span class="sxs-lookup"><span data-stu-id="8fc38-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-entity-fields-issue-on-maps"></a><span data-ttu-id="8fc38-122">Проблема с отсутствующими полями объекта на картах</span><span class="sxs-lookup"><span data-stu-id="8fc38-122">Missing entity fields issue on maps</span></span>

<span data-ttu-id="8fc38-123">**Роль, требуемая для исправления ошибки:** системный администратор</span><span class="sxs-lookup"><span data-stu-id="8fc38-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="8fc38-124">На странице **Двойная запись** может быть выведено сообщение об ошибке, подобное следующему примеру:</span><span class="sxs-lookup"><span data-stu-id="8fc38-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="8fc38-125">*Отсутствует исходное поле \<имя поля\> в схеме.*</span><span class="sxs-lookup"><span data-stu-id="8fc38-125">*Missing source field \<field name\> in the schema.*</span></span>

![Пример сообщения об ошибке об отсутствующем исходном поле](media/error_missing_field.png)

<span data-ttu-id="8fc38-127">Чтобы устранить проблему, сначала необходимо выполнить следующие действия, чтобы убедиться в наличии полей в объекте.</span><span class="sxs-lookup"><span data-stu-id="8fc38-127">To fix the issue, first follow these steps to make sure that the fields are in the entity.</span></span>

1. <span data-ttu-id="8fc38-128">Выполните вход в виртуальную машину для приложения Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8fc38-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="8fc38-129">Выберите **Рабочие области \> Управление данными**, выберите плитку **Параметры структуры**, затем на вкладке **Параметры объекта** выберите **Обновить список объектов**, чтобы обновить объекты.</span><span class="sxs-lookup"><span data-stu-id="8fc38-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Entity settings** tab, select **Refresh entity list** to refresh the entities.</span></span>
3. <span data-ttu-id="8fc38-130">Выберите **Рабочие области \> Управление данными**, выберите вкладку **Объекты данных** и убедитесь, что объект указан в списке.</span><span class="sxs-lookup"><span data-stu-id="8fc38-130">Go to **Workspaces \> Data management**, select the **Data entities** tab, and make sure that the entity is listed.</span></span> <span data-ttu-id="8fc38-131">Если объект отсутствует в списке, выполните вход в виртуальную машину для приложения Finance and Operations и убедитесь, что объект доступен.</span><span class="sxs-lookup"><span data-stu-id="8fc38-131">If the entity isn't listed, sign in to the VM for the Finance and Operations app, and make sure the entity is available.</span></span>
4. <span data-ttu-id="8fc38-132">Откройте страницу **Сопоставление объектов** со страницы **Двойная запись** в приложении Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8fc38-132">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="8fc38-133">Выберите **Обновить список объектов**, чтобы автоматически заполнить поля в сопоставлениях объектов.</span><span class="sxs-lookup"><span data-stu-id="8fc38-133">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>

<span data-ttu-id="8fc38-134">Если проблема все еще не устранена, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8fc38-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8fc38-135">В этих шагах выполняется процедура удаления объекта и добавления его снова.</span><span class="sxs-lookup"><span data-stu-id="8fc38-135">These steps guide you through the process of deleting an entity and then adding it again.</span></span> <span data-ttu-id="8fc38-136">Чтобы избежать проблем, обязательно точно выполните описанные шаги.</span><span class="sxs-lookup"><span data-stu-id="8fc38-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="8fc38-137">В приложении Finance and Operations перейдите к пункту **Рабочие области \> Управление данными** и выберите плитку **Объекты данных**.</span><span class="sxs-lookup"><span data-stu-id="8fc38-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data entities** tile.</span></span>
2. <span data-ttu-id="8fc38-138">Найдите объект, в котором отсутствует поле.</span><span class="sxs-lookup"><span data-stu-id="8fc38-138">Find the entity that is missing the field.</span></span> <span data-ttu-id="8fc38-139">Запишите целевой объект, промежуточную таблицу, имя объекта и другие значения столбцов.</span><span class="sxs-lookup"><span data-stu-id="8fc38-139">Make a note of the target entity, staging table, entity name, and other column values.</span></span>
3. <span data-ttu-id="8fc38-140">Если какая-либо из групп обработки зависит от этого объекта, перед удалением объекта выполните соответствующие действия для групп обработки.</span><span class="sxs-lookup"><span data-stu-id="8fc38-140">If any of your processing groups depend on this entity, take appropriate action for the processing groups before you delete the entity.</span></span>
4. <span data-ttu-id="8fc38-141">Удалите объект, в котором отсутствует поле.</span><span class="sxs-lookup"><span data-stu-id="8fc38-141">Delete the entity that is missing the field.</span></span>
5. <span data-ttu-id="8fc38-142">Выберите **Создать** и снова добавьте объект.</span><span class="sxs-lookup"><span data-stu-id="8fc38-142">Select **New**, and add the entity back.</span></span> <span data-ttu-id="8fc38-143">Укажите значения, которые были записаны на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="8fc38-143">Specify the values that you made a note of in step 2.</span></span>
6. <span data-ttu-id="8fc38-144">Откройте страницу **Сопоставление объектов** со страницы **Двойная запись** в приложении Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8fc38-144">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
7. <span data-ttu-id="8fc38-145">Выберите **Обновить список объектов**, чтобы автоматически заполнить поля в сопоставлениях объектов.</span><span class="sxs-lookup"><span data-stu-id="8fc38-145">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>