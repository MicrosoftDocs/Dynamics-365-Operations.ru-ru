---
title: Что нового и что изменилось в Dynamics 365 for Talent Core HR (17 сентября 2018 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/17/2018
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
ms.search.validFrom: 2018-09-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 213324f9074f88d9fdc8efdfa46bc3ed7817d1e8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518956"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-17-2018"></a><span data-ttu-id="f6f6b-103">Что нового и что изменилось в Dynamics 365 for Talent Core HR (17 сентября 2018 г.)</span><span class="sxs-lookup"><span data-stu-id="f6f6b-103">What's new or changed in Dynamics 365 for Talent Core HR (September 17, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f6f6b-104">**Сборка 8.1.154.0**</span><span class="sxs-lookup"><span data-stu-id="f6f6b-104">**Build 8.1.154.0**</span></span>

<span data-ttu-id="f6f6b-105">В этой теме описываются новые и измененные компоненты Core HR.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="leave-and-absence--accrue-time-based-on-hours-worked"></a><span data-ttu-id="f6f6b-106">Отпуска и отсутствия — начисление времени на основе отработанных часов</span><span class="sxs-lookup"><span data-stu-id="f6f6b-106">Leave and Absence – Accrue time based on hours worked</span></span>

<span data-ttu-id="f6f6b-107">В планы отпусков добавлен новый тип начисления.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-107">A new accrual type has been added to Leave plans.</span></span> <span data-ttu-id="f6f6b-108">График начисления теперь может быть основан на отработанных месяцах или часах.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-108">The accrual schedule can now be based on months of service or hours worked.</span></span> <span data-ttu-id="f6f6b-109">Дополнительные сведения см. в разделе [Начисление времени отпуска на основе отработанных часов](leave-accrue-hours-worked.md).</span><span class="sxs-lookup"><span data-stu-id="f6f6b-109">For more information, see [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

## <a name="platform-update-18"></a><span data-ttu-id="f6f6b-110">Обновление платформы update 18</span><span class="sxs-lookup"><span data-stu-id="f6f6b-110">Platform update 18</span></span>

<span data-ttu-id="f6f6b-111">Platform update 18 теперь входит в состав выпуска Talent.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-111">Platform update 18 is now part of the Talent release.</span></span> 

-   <span data-ttu-id="f6f6b-112">Обязательные и другие поля можно скрывать посредством персонализации.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-112">Mandatory and other fields can be hidden via personalization.</span></span> <span data-ttu-id="f6f6b-113">Это позволяет пользователю создавать упрощенный интерфейс, когда обязательные поля, которые по умолчанию заполняются бизнес-логикой, не отображаются.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-113">This allows a user to create a simplified experience where mandatory fields that are defaulted by business logic are not shown.</span></span> <span data-ttu-id="f6f6b-114">Скрытые обязательные поля также временно становятся видимыми, если на момент попытки сохранения они пустые.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-114">Hidden mandatory fields are also temporarily made visible if they are empty when a save is attempted.</span></span>

-   <span data-ttu-id="f6f6b-115">В Platform update 18 визуальное оформление веб-клиента Talent теперь соответствует Microsoft Fluent Design.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-115">In Platform update 18, the Talent web client now aligns its visuals with Microsoft Fluent Design.</span></span>

    -   <span data-ttu-id="f6f6b-116">Когда поля находятся в "режиме для чтения", можно просто выбрать параметр редактирования в полях, чтобы перевести форму в режим редактирования.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-116">When fields are in “read mode”, you can simply select the edit option in the fields to switch the form to edit.</span></span>

    -   <span data-ttu-id="f6f6b-117">Изменения в отображении полей в режиме чтения.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-117">Changes in how fields display when in read mode.</span></span>

    -   <span data-ttu-id="f6f6b-118">Заголовки в рабочих областях и на страницах выделены полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-118">Headings in workspaces and pages are bold.</span></span>

-   <span data-ttu-id="f6f6b-119">Улучшено поведение поисков без замены.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-119">The behavior of non-replacing lookups has been improved.</span></span> <span data-ttu-id="f6f6b-120">Дополнительные сведения см. в разделе [Улучшенное поведение поисков без замены](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fbusiness-applications-release-notes%2FOctober18%2Fdynamics365-finance-operations%2Fnon-replacing-lookups&data=02%7C01%7C%7Ce0b3b3bee47b4424aaa208d619ce86f2%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636724772137980342&sdata=RN1qjtZSLtS010zgs0KlcwFrrB8Z7uWWGtFjdxdaamg%3D&reserved=0).</span><span class="sxs-lookup"><span data-stu-id="f6f6b-120">For more information, see [Improved behavior for non-replacing lookups](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fbusiness-applications-release-notes%2FOctober18%2Fdynamics365-finance-operations%2Fnon-replacing-lookups&data=02%7C01%7C%7Ce0b3b3bee47b4424aaa208d619ce86f2%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636724772137980342&sdata=RN1qjtZSLtS010zgs0KlcwFrrB8Z7uWWGtFjdxdaamg%3D&reserved=0).</span></span>

## <a name="bug-fixes"></a><span data-ttu-id="f6f6b-121">Исправления ошибок</span><span class="sxs-lookup"><span data-stu-id="f6f6b-121">Bug fixes</span></span>

<span data-ttu-id="f6f6b-122">Эта версия включает в себя несколько дополнительных исправлений ошибок; в частности, ссылки на ACA, ADA и I9 теперь будут включены только в компаниях, которые находятся в США.</span><span class="sxs-lookup"><span data-stu-id="f6f6b-122">This release includes several additional bug fixes, including references to ACA, ADA, and I9 now will only be enabled in US companies.</span></span>
