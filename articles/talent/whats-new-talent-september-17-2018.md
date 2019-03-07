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
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6586761fc62c13c701e8a8f61e15eedc66e2f751
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "305965"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-17-2018"></a>Что нового и что изменилось в Dynamics 365 for Talent Core HR (17 сентября 2018 г.)

[!include [banner](includes/banner.md)]

**Сборка 8.1.154.0**

В этой теме описываются новые и измененные компоненты Core HR.

## <a name="leave-and-absence--accrue-time-based-on-hours-worked"></a>Отпуска и отсутствия — начисление времени на основе отработанных часов

В планы отпусков добавлен новый тип начисления. График начисления теперь может быть основан на отработанных месяцах или часах. Дополнительные сведения см. в разделе [Начисление времени отпуска на основе отработанных часов](leave-accrue-hours-worked.md).

## <a name="platform-update-18"></a>Обновление платформы update 18

Platform update 18 теперь входит в состав выпуска Talent. 

-   Обязательные и другие поля можно скрывать посредством персонализации. Это позволяет пользователю создавать упрощенный интерфейс, когда обязательные поля, которые по умолчанию заполняются бизнес-логикой, не отображаются. Скрытые обязательные поля также временно становятся видимыми, если на момент попытки сохранения они пустые.

-   В Platform update 18 визуальное оформление веб-клиента Talent теперь соответствует Microsoft Fluent Design.

    -   Когда поля находятся в "режиме для чтения", можно просто выбрать параметр редактирования в полях, чтобы перевести форму в режим редактирования.

    -   Изменения в отображении полей в режиме чтения.

    -   Заголовки в рабочих областях и на страницах выделены полужирным шрифтом.

-   Улучшено поведение поисков без замены. Дополнительные сведения см. в разделе [Улучшенное поведение поисков без замены](https://na01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fbusiness-applications-release-notes%2FOctober18%2Fdynamics365-finance-operations%2Fnon-replacing-lookups&data=02%7C01%7C%7Ce0b3b3bee47b4424aaa208d619ce86f2%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636724772137980342&sdata=RN1qjtZSLtS010zgs0KlcwFrrB8Z7uWWGtFjdxdaamg%3D&reserved=0).

## <a name="bug-fixes"></a>Исправления ошибок

Эта версия включает в себя несколько дополнительных исправлений ошибок; в частности, ссылки на ACA, ADA и I9 теперь будут включены только в компаниях, которые находятся в США.
