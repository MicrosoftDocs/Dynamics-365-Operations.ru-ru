---
title: Настройка параметров отпусков и отсутствий
description: Определение параметров управления персоналом для отпусков и отсутствия в Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2acb8502ebcab122a0a1ff21e9f5e23931026327
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010317"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="0cc97-103">Настройка параметров отпусков и отсутствий</span><span class="sxs-lookup"><span data-stu-id="0cc97-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="0cc97-104">Прежде чем настраивать планы отпусков и отсутствия в Dynamics 365 Human Resources, рекомендуется проверить настройки для всех соответствующих параметров модуля управления персоналом, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="0cc97-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="0cc97-105">Номерная серия для запросов отпусков</span><span class="sxs-lookup"><span data-stu-id="0cc97-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="0cc97-106">Параметры Family Medical and Leave Act (FMLA)</span><span class="sxs-lookup"><span data-stu-id="0cc97-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="0cc97-107">Настройки самообслуживания сотрудников для запросов отпусков и отсутствия</span><span class="sxs-lookup"><span data-stu-id="0cc97-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="0cc97-108">Параметры отпусков и отсутствия</span><span class="sxs-lookup"><span data-stu-id="0cc97-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="0cc97-109">Просмотр и изменение параметров управления персоналом</span><span class="sxs-lookup"><span data-stu-id="0cc97-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="0cc97-110">На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="0cc97-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="0cc97-111">В **Настройка** выберите **Параметры управления персоналом**.</span><span class="sxs-lookup"><span data-stu-id="0cc97-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="0cc97-112">На вкладке **Номерные серии** проверьте **Код номерной серии** для **Код запроса отпуска** и измените его, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="0cc97-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="0cc97-113">Этот параметр определяет последовательность, используемую для автоматического назначения кодов для запросов отпуска.</span><span class="sxs-lookup"><span data-stu-id="0cc97-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="0cc97-114">На вкладке **FMLA** проверьте настройки FMLA и, если необходимо, измените их.</span><span class="sxs-lookup"><span data-stu-id="0cc97-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="0cc97-115">На вкладке **Самообслуживание сотрудников** укажите, могут ли менеджеры вводить запросы на отпуск и отсутствие от имени своих сотрудников.</span><span class="sxs-lookup"><span data-stu-id="0cc97-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

6. <span data-ttu-id="0cc97-116">На вкладке **Отпуск и отсутствие** проверьте настройки и, если необходимо, измените их.</span><span class="sxs-lookup"><span data-stu-id="0cc97-116">On the **Leave and absence** tab, verify the settings and change as necessary.</span></span>

7. <span data-ttu-id="0cc97-117">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0cc97-117">Select **Save**.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="0cc97-118">Настройка параметров календаря</span><span class="sxs-lookup"><span data-stu-id="0cc97-118">Configure calendar parameters</span></span>

<span data-ttu-id="0cc97-119">Если вы включили функцию предварительного просмотра календаря отпуска и отсутствия, вам необходимо настроить дополнительные параметры.</span><span class="sxs-lookup"><span data-stu-id="0cc97-119">If you have enabled the Leave and absence calendar preview feature, you need to configure additional parameters.</span></span> 

[!include [banner](includes/preview-feature-leave-absence.md)]

> [!NOTE]
> <span data-ttu-id="0cc97-120">Для предварительной версии 3 февраля 2020 г. включено только **Ожидающие запросы отпуска**.</span><span class="sxs-lookup"><span data-stu-id="0cc97-120">For the preview release on February 3, 2020, only **Pending leave requests** are enabled.</span></span>

1. <span data-ttu-id="0cc97-121">На странице **Отпуск и отсутствия** выберите вкладку **Ссылки**.</span><span class="sxs-lookup"><span data-stu-id="0cc97-121">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="0cc97-122">В **Настройка** выберите **Параметры управления персоналом**.</span><span class="sxs-lookup"><span data-stu-id="0cc97-122">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="0cc97-123">На вкладке **Календарь** измените настройки, если необходимо.</span><span class="sxs-lookup"><span data-stu-id="0cc97-123">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="0cc97-124">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0cc97-124">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="0cc97-125">См. также</span><span class="sxs-lookup"><span data-stu-id="0cc97-125">See also</span></span>

- [<span data-ttu-id="0cc97-126">Обзор отпусков и отсутствия на работе</span><span class="sxs-lookup"><span data-stu-id="0cc97-126">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
