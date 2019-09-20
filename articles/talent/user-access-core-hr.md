---
title: Пользователь может получить доступ к Core HR, но не к приложению Onboard или Attract
description: В этом разделе объясняется, как решить проблему, когда пользователь имеет доступ к Microsoft Dynamics 365 for Talent Core HR, но не имеет доступа к приложению Attract или Onboard.
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
ms.openlocfilehash: 6fc27a4c137fef2f8d204d90366c316389da08e6
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741734"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a>Пользователю доступно Core HR, но недоступно приложение Onboard или Attract

[!include [banner](includes/banner.md)]

**Сведения среды**

- Развертывание Microsoft Dynamics Lifecycle Services (LCS) было выполнено пользователем A.
- Пользователь А добавил пользователя B в качестве пользователя Microsoft Dynamics 365 for Talent Core HR.

**Расход**

Пользователь B имеет доступ к Core HR, но не может получить доступ к приложению Talent: Attract или Talent: Onboard. При попытке перейти к разделу **Приложения взаимодействия** вместо этого пользователь попадает в тестовую среду.

**Решение**

Пользователю B необходимо назначить права на просмотр среды Microsoft PowerApps, которую пользователь A создал в процессе подготовки.

Сведения см. в разделе "Предоставление доступа к среде" в статье [Подготовка Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

**Долгосрочное решение**

Майкрософт планирует автоматическое назначение соответствующих прав на приложения Onboard и Attract при добавлении пользователя в Core HR.
