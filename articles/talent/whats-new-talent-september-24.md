---
title: Что нового и что изменилось в Dynamics 365 Talent - Core HR (24 сентября 2018 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/21/2018
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
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6001b3c777be005dfc0b22ca0b64d5c56a56cb1e
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010069"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-september-24-2018"></a><span data-ttu-id="c20a1-103">Что нового и что изменилось в Dynamics 365 Talent: Core HR (24 сентября 2018 г.)</span><span class="sxs-lookup"><span data-stu-id="c20a1-103">What's new or changed in Dynamics 365 Talent: Core HR (September 24, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c20a1-104">**Сборка 8.1.1015.0**</span><span class="sxs-lookup"><span data-stu-id="c20a1-104">**Build 8.1.1015.0**</span></span>

<span data-ttu-id="c20a1-105">В этой теме описываются новые и измененные компоненты Core HR.</span><span class="sxs-lookup"><span data-stu-id="c20a1-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="currency-added-to-benefits"></a><span data-ttu-id="c20a1-106">В льготы добавлена валюта</span><span class="sxs-lookup"><span data-stu-id="c20a1-106">Currency added to Benefits</span></span>

<span data-ttu-id="c20a1-107">В планы льгот теперь включается валюта льготы.</span><span class="sxs-lookup"><span data-stu-id="c20a1-107">Benefit plans have been updated to include the currency of the benefit.</span></span> <span data-ttu-id="c20a1-108">Это новое поле также доступно в льготах, на которые зарегистрирован работник.</span><span class="sxs-lookup"><span data-stu-id="c20a1-108">This new field is also available on worker enrolled benefits.</span></span> <span data-ttu-id="c20a1-109">Это новое поле входит в привилегии безопасности "Ведение льгот" и "Просмотр списка льгот".</span><span class="sxs-lookup"><span data-stu-id="c20a1-109">This new field is part of the Maintain benefits and View a list of benefits security privilege.</span></span>

## <a name="update-proration-process--leave-and-absence"></a><span data-ttu-id="c20a1-110">Обновление процесса пропорционального распределения — отпуска и отсутствия</span><span class="sxs-lookup"><span data-stu-id="c20a1-110">Update proration process – Leave and Absence</span></span>

<span data-ttu-id="c20a1-111">Организации назначают отпуска по-разному в зависимости от того, когда сотрудники приходят в компанию и покидают ее.</span><span class="sxs-lookup"><span data-stu-id="c20a1-111">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="c20a1-112">Для сотрудников, которые увольняются из организации, в некоторых случаях необходимо закончить начисление в день увольнения, тогда как в других процесс начисления заканчивается в последний отработанный день.</span><span class="sxs-lookup"><span data-stu-id="c20a1-112">For employees leaving the organization, some may need to end the award on the termination date, while others rely on the last day worked to stop the accrual process.</span></span> <span data-ttu-id="c20a1-113">Эти изменения позволяют организациям выбирать, когда заканчивать регистрацию в процессе увольнения.</span><span class="sxs-lookup"><span data-stu-id="c20a1-113">These changes provide organizations the ability to choose when to end enrollment during the termination process.</span></span> <span data-ttu-id="c20a1-114">Эти новые параметры входят в привилегии "Увольнение работника" и "Уволить работника с помощью портала самообслуживания менеджера".</span><span class="sxs-lookup"><span data-stu-id="c20a1-114">These new options are part of the privileges for Terminate a worker and Terminate a worker from manager self service.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="c20a1-115">Другие изменения</span><span class="sxs-lookup"><span data-stu-id="c20a1-115">Other changes</span></span>

<span data-ttu-id="c20a1-116">Этот выпуск содержит несколько дополнительных исправлений ошибок.</span><span class="sxs-lookup"><span data-stu-id="c20a1-116">This release includes several additional bug fixes.</span></span>

## <a name="known-issue"></a><span data-ttu-id="c20a1-117">Известная проблема</span><span class="sxs-lookup"><span data-stu-id="c20a1-117">Known Issue</span></span>

-   <span data-ttu-id="c20a1-118">**Проблема:** при добавлении нового вложения в работника кнопки **Создать** и **Редактировать** неактивны. **Обход:** перед открытием страницы вложения убедитесь, что информационные панели на странице **Работник** закрыты.</span><span class="sxs-lookup"><span data-stu-id="c20a1-118">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the fact boxes on the **Worker** page are closed.</span></span> <span data-ttu-id="c20a1-119">Если информационные панели закрыты при загрузке страницы **Работник**, кнопки вложений будут активны.</span><span class="sxs-lookup"><span data-stu-id="c20a1-119">If the fact boxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="c20a1-120">(Эта проблема будет исправлена в следующем обновлении платформы.)</span><span class="sxs-lookup"><span data-stu-id="c20a1-120">(This issue will be fixed in the next platform update.)</span></span>
