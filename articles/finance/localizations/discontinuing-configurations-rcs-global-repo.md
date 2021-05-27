---
title: Прекращение поддержки конфигураций в глобальном репозитории RCS
description: В этом разделе описывается, как прекратить поддержку конфигураций в глобальном репозитории RCS.
author: JaneA07
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 2bd22e991de376cfd93f75158f1f29716d2559e1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018741"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a><span data-ttu-id="0a1c8-103">Прекращение поддержки конфигураций в глобальном репозитории RCS</span><span class="sxs-lookup"><span data-stu-id="0a1c8-103">Discontinue configurations in the RCS Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a1c8-104">В этом разделе описывается, как прекратить поддержку конфигурации в глобальном репозитории RCS.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-104">This topic describes how to discontinue configuration in the RCS Global repository.</span></span> <span data-ttu-id="0a1c8-105">Раньше было возможно только удалить конфигурации, которые больше не требуются.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-105">Previously, it was possible only to delete configurations that were no longer required.</span></span> <span data-ttu-id="0a1c8-106">Однако теперь можно пометить выпущенную конфигурацию как **Поддержка прекращена** в глобальном репозитории RCS.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-106">However now you can mark a released configuration as **Discontinued** in the RCS Global repository.</span></span> <span data-ttu-id="0a1c8-107">С помощью этой функции также можно делать следующее:</span><span class="sxs-lookup"><span data-stu-id="0a1c8-107">With this functionality, you can also do the following:</span></span> 
 
 - <span data-ttu-id="0a1c8-108">Предоставление предварительных уведомлений, когда планируется отмена конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-108">Provide up front notifications when a configuration is planned to be discontinued.</span></span>
 - <span data-ttu-id="0a1c8-109">Включает в себя применимые сведения о конфигурации замены.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-109">Include applicable details about the replacement configuration.</span></span>
 - <span data-ttu-id="0a1c8-110">Настройка **даты окончания поддержки** для определенной конфигурации для информирования пользователя о прекращении продолжения ее работы.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-110">Set a **Supported until** date for the specific configuration to inform the user when it will be discontinued.</span></span>

<span data-ttu-id="0a1c8-111">При прекращении работы версии конфигурации можно указать следующие дополнительные сведения:</span><span class="sxs-lookup"><span data-stu-id="0a1c8-111">When you discontinue a configuration version, you can specify the following optional information:</span></span>

  - <span data-ttu-id="0a1c8-112">**Конфигурация замены**</span><span class="sxs-lookup"><span data-stu-id="0a1c8-112">**Replacement configuration**</span></span>
  - <span data-ttu-id="0a1c8-113">**Версия конфигурации замены**</span><span class="sxs-lookup"><span data-stu-id="0a1c8-113">**Replacement configuration version**</span></span>
  - <span data-ttu-id="0a1c8-114">**Примечание с произвольным текстом**: используйте это поле, чтобы предоставить ссылки на документацию или ссылки</span><span class="sxs-lookup"><span data-stu-id="0a1c8-114">**Free text note**: Use this field to provide documentation links or references</span></span>
  - <span data-ttu-id="0a1c8-115">**Поддерживается до**: в это поле входит предложенная дата, до которой будет поддерживаться текущая конфигурация/версия.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-115">**Supported until**: This field provides the proposed date up to which the current configuration/version will be supported.</span></span> <span data-ttu-id="0a1c8-116">Эта дата должна быть обновлена вручную.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-116">This date must be updated manually.</span></span>
  
<span data-ttu-id="0a1c8-117">Чтобы прекратить настройку, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-117">To discontinue the configuration, complete the following steps.</span></span> 

1. <span data-ttu-id="0a1c8-118">Укажите, необходимо ли отменить одну или все версии с одинаковыми параметрами в одной операции, задав для **всех версий** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-118">Select whether you want to discontinue a single version or all versions with the same settings in one operation by setting **All versions** to **Yes**.</span></span> 
2. <span data-ttu-id="0a1c8-119">Установите для параметра **Отменить** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-119">Set the **Discontinue** parameter to **Yes**.</span></span>
3. <span data-ttu-id="0a1c8-120">Нажмите кнопку **ОК**, чтобы прекратить настройку.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-120">Select **OK** to discontinue the configurations.</span></span> <span data-ttu-id="0a1c8-121">При сохранении изменений поле **Дата прекращения поддержки** будет заполнено.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-121">The **Discontinued date** field will be populated when you save the changes.</span></span>

![Сведения о прекращении поддержки конфигурации](media/Discontinue-details-2.png)
  
<span data-ttu-id="0a1c8-123">В любое время можно вернуть конфигурацию к **Общий** или скорректировать сведения о прекращении поддержки.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-123">You can revert configuration back to **Shared** or adjust discontinuation information at any time.</span></span> <span data-ttu-id="0a1c8-124">При совместном использовании конфигурации укажите дату **Поддерживается до** и все остальные сведения, связанные с прекращением поддержки, чтобы указать планы для будущей отмены поддержки.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-124">If you share a configuration, specify the **Supported until** date and all other information related to the discontinuation to indicate your plans for future discontinuation.</span></span>

<span data-ttu-id="0a1c8-125">Если требуется предоставить общий доступ к сведениям о спланированном отмене поддержки, перед фактическим прекращением поддержки конфигурации пользователь может предварительно заполнить все поля, связанные с заменой, но оставить для параметра **Прекратить поддержку** значение **нет**.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-125">If you want to share information about a planned discontinuation, prior to actually discontinuing the configuration, user is able to prefill all fields related to replacement but leave the **Discontinue** parameter set to **No**.</span></span>

> [!NOTE]
> <span data-ttu-id="0a1c8-126">При прекращении поддержки не ограничивается выполнение операций с конфигурациями.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-126">Discontinuation doesn't limit operations with configurations.</span></span> <span data-ttu-id="0a1c8-127">Можно продолжить импорт, выполнение или наследование конфигураций, эти поля являются информационными.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-127">You can continue to import, run, or derive the configurations, these fields are informational.</span></span>

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a><span data-ttu-id="0a1c8-128">Финансы поддерживает отображение этой информации начиная с версии 10.0.14</span><span class="sxs-lookup"><span data-stu-id="0a1c8-128">Finance supports displaying this information starting in version 10.0.14</span></span>

<span data-ttu-id="0a1c8-129">Начиная с версии 10.0.14 Dynamics 365 Finance поддерживает отображение информации о прекращении поддержки.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-129">Starting in version 10.0.14, Dynamics 365 Finance supports displaying discontinuation information.</span></span> <span data-ttu-id="0a1c8-130">На странице **глобального репозитория** можно просмотреть последние сведения, имеющие отношение к прекращению поддержки.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-130">On the **Global repository** page, you can view up to date information related to discontinuation.</span></span> <span data-ttu-id="0a1c8-131">По умолчанию, неподдерживаемые конфигурации отфильтровываются.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-131">By default, configurations that are discontinued are filtered out.</span></span>
  
<span data-ttu-id="0a1c8-132">Страница **импортированные конфигурации** (ERSolutionTable) отображает конфигурации, которые уже не поддерживаются после импорта.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-132">The **Imported configurations** (ERSolutionTable) page, shows configurations that were already discontinued when there were imported.</span></span> <span data-ttu-id="0a1c8-133">Для тех конфигураций, которые не поддерживаются после импорта, сведения о прекращении поддержки могут быть синхронизованы путем запуска задания **Импорт обновлений конфигураций**.</span><span class="sxs-lookup"><span data-stu-id="0a1c8-133">For those configurations that were discontinued after import, the discontinuation information can be synchronized by running the **Import configurations updates** job.</span></span>


