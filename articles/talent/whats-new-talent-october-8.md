---
title: Что нового и что изменилось в Dynamics 365 for Talent Core HR (8 октября 2018 г.)
description: В этой теме описываются новые и измененные компоненты Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/07/2018
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
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 34216e2181915cf615e6e77fa2a10d06a4e9db85
ms.sourcegitcommit: aec1dcd44274e9b8d0770836598fde5533b7b569
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2019
ms.locfileid: "1617280"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-8-2018"></a>Что нового и что изменилось в Dynamics 365 for Talent Core HR (8 октября 2018 г.)

[!include [banner](includes/banner.md)]

**Сборка 8.1.1050.0**

В этой теме описываются новые и измененные компоненты Core HR.

## <a name="allow-other-dates-to-be-used-on-leave-tier-basis-leave-management"></a>Разрешить использовать другие даты для использования на базе уровня отпусков (управление отпусками)

При предоставлении отпуска сотрудникам база уровня вознаграждения определяет, сколько отгулов начислено сотруднику. В настоящее время эти уровни основаны на дате приема сотрудника на работу и дате трудового стажа. В некоторых сценариях организациям требуются, чтобы эти уровни были основаны на других датах, таких как дата юбилея или исходная дата приема на работу. Эти даты уже используются в плане отпусков для определения, когда происходит начисление, возможность использовать эти же даты при регистрации сотрудника в плане была добавлена для определения суммы начисления. 

## <a name="other-changes"></a>Другие изменения
Прочие исправления были включены в данный выпуск.

## <a name="known-issue"></a>Известная проблема

**Проблема:** при добавлении нового вложения в работника кнопки **Создать** и **Редактировать** неактивны. **Обход:** перед открытием страницы вложения убедитесь, что информационные панели на странице **Работник** закрыты. Если информационные панели закрыты при загрузке страницы **Работник**, кнопки вложений будут активны. (Эта проблема будет исправлена в следующем обновлении платформы.)
