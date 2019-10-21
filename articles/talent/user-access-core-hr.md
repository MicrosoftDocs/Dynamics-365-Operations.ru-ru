---
title: Пользователю доступно Core HR, но недоступны Onboard или Attract
description: В этом разделе объясняется, как решить проблему, когда пользователь имеет доступ к Microsoft Dynamics 365 Talent - Core HR, но не имеет доступа к Attract или Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 80b1f8aeabfd033f393463f4be5a61447377f2d9
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009314"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a>Пользователю доступно Core HR, но недоступны Onboard или Attract

[!include [banner](includes/banner.md)]

**Сведения среды**

- Развертывание Microsoft Dynamics Lifecycle Services (LCS) было выполнено пользователем A.
- Пользователь А добавил пользователя B в качестве пользователя Microsoft Dynamics 365 Talent: Core HR.

**Выдать**

Пользователь B имеет доступ к Core HR, но не может получить доступ к приложению Talent: Attract или Talent: Onboard. При попытке перейти к разделу **Приложения взаимодействия** вместо этого пользователь попадает в тестовую среду.

**Решение**

Пользователю B необходимо назначить права на просмотр среды Microsoft PowerApps, которую пользователь A создал в процессе подготовки.

Сведения см. в разделе "Предоставление доступа к среде" в статье [Подготовка Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

**Долгосрочное решение**

Майкрософт планирует автоматическое назначение соответствующих прав на приложения Onboard и Attract при добавлении пользователя в Core HR.
