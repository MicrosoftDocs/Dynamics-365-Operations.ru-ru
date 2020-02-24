---
title: Что нового и что изменилось в Dynamics 365 Talent (7 января 2020 г.)
description: В этой статье описываются новые и измененные компоненты Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 615ed3e4260192ba36826e128f1afa1588e94845
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2020
ms.locfileid: "2974438"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a><span data-ttu-id="713ca-103">Что нового и что изменилось в Dynamics 365 Talent (7 января 2020 г.)</span><span class="sxs-lookup"><span data-stu-id="713ca-103">What's new or changed in Dynamics 365 Talent (January 7, 2020)</span></span>

<span data-ttu-id="713ca-104">В этой статье описываются новые и измененные компоненты в Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="713ca-104">This article describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="713ca-105">Изменения в Attract</span><span class="sxs-lookup"><span data-stu-id="713ca-105">Changes in Attract</span></span>

<span data-ttu-id="713ca-106">Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="713ca-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="713ca-107">Изменения в Onboard</span><span class="sxs-lookup"><span data-stu-id="713ca-107">Changes in Onboard</span></span>

<span data-ttu-id="713ca-108">Этот выпуск содержит исправления незначительных ошибок для Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="713ca-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="713ca-109">Изменения в Core HR</span><span class="sxs-lookup"><span data-stu-id="713ca-109">Changes in Core HR</span></span>

<span data-ttu-id="713ca-110">Изменения, описанные в этом разделе, относятся к сборке номер 8.1.2697.</span><span class="sxs-lookup"><span data-stu-id="713ca-110">Changes described in this section apply to build number 8.1.2697.</span></span> <span data-ttu-id="713ca-111">Числа в скобках в некоторых заголовках относятся к номерам поддержки в службе Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="713ca-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a><span data-ttu-id="713ca-112">Не удается удалить работников, не имеющих записей о занятости (386157)</span><span class="sxs-lookup"><span data-stu-id="713ca-112">Can't delete workers that don't have employment records - (386157)</span></span>

<span data-ttu-id="713ca-113">Это изменение добавляет параметр удаления в форме **Сотрудники без занятости**.</span><span class="sxs-lookup"><span data-stu-id="713ca-113">This change adds a delete option in the **Workers without employment** form.</span></span> <span data-ttu-id="713ca-114">Работники отображаются в этой форме, если для данного сотрудника не существует будущего, активного или исторического трудоустройства.</span><span class="sxs-lookup"><span data-stu-id="713ca-114">Workers appear in this form when no future, active, or historical employments exist for the worker.</span></span> <span data-ttu-id="713ca-115">В этом выпуске удаление разрешено только для системных администраторов.</span><span class="sxs-lookup"><span data-stu-id="713ca-115">In this release, delete is only enabled for System Administrators.</span></span> <span data-ttu-id="713ca-116">Однако в выпуске следующей недели система безопасности будет обновлена, чтобы позволить всем пользователям с ролью помощника в отделе кадров удалить сотрудников без занятости.</span><span class="sxs-lookup"><span data-stu-id="713ca-116">However, in next week's release, security will be updated to allow all users with the HR assistant role to remove employees without employments.</span></span> <span data-ttu-id="713ca-117">Эти изменения также можно выполнить вручную, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="713ca-117">You can also make these changes manually by following the following steps.</span></span>

1. <span data-ttu-id="713ca-118">Перейдите **Конфигурация безопасности**.</span><span class="sxs-lookup"><span data-stu-id="713ca-118">Go to **Security configuration**.</span></span>
2. <span data-ttu-id="713ca-119">На вкладке **Привилегии** отфильтруйте список **Привилегии** до **Ведение работников**.</span><span class="sxs-lookup"><span data-stu-id="713ca-119">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>
3. <span data-ttu-id="713ca-120">В столбце **Ссылки** выберите **Пункты меню отображения**.</span><span class="sxs-lookup"><span data-stu-id="713ca-120">In the **References** column, select **Display menu items**.</span></span>
4. <span data-ttu-id="713ca-121">В **Пункты меню отображения** выберите **HcmWOrkersWithoutEmployment**.</span><span class="sxs-lookup"><span data-stu-id="713ca-121">In **Display menu items**, select **HcmWOrkersWithoutEmployment**.</span></span>
5. <span data-ttu-id="713ca-122">Установите разрешение **Удалить** как "Разрешить".</span><span class="sxs-lookup"><span data-stu-id="713ca-122">Set the **Delete** permission to Grant.</span></span>
6. <span data-ttu-id="713ca-123">Перейдите на вкладку **Неопубликованные объекты**.</span><span class="sxs-lookup"><span data-stu-id="713ca-123">Select the **Unpublished objects** tab.</span></span>
7. <span data-ttu-id="713ca-124">Выберите **Опубликовать все**.</span><span class="sxs-lookup"><span data-stu-id="713ca-124">Select **Publish all**.</span></span>
