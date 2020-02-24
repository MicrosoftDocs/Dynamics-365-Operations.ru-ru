---
title: Пользователю доступно Human Resources, но недоступно Onboard или Attract
description: В этом разделе объясняется, как решить проблему, когда пользователь имеет доступ к Microsoft Dynamics 365 Talent — Human Resources, но не имеет доступа к Attract или Onboard.
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
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006318"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a>Пользователю доступно Human Resources, но недоступно Onboard или Attract

[!include [banner](includes/banner.md)]

**Сведения среды**

- Развертывание Microsoft Dynamics Lifecycle Services (LCS) было выполнено пользователем A.
- Пользователь А добавил пользователя B в качестве пользователя Microsoft Dynamics 365 Human Resources.

**Выдать**

Пользователь B имеет доступ к Human Resources, но не может получить доступ к приложению Talent: Attract или Talent: Onboard. При попытке перейти к разделу **Приложения взаимодействия** вместо этого пользователь попадает в тестовую среду.

**Решение**

Пользователю B необходимо назначить права на просмотр среды Microsoft Power Apps, которую пользователь A создал в процессе подготовки.

Сведения см. в разделе "Предоставление доступа к среде" в статье [Подготовка Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

**Долгосрочное решение**

Майкрософт планирует автоматическое назначение соответствующих прав на приложения Onboard и Attract при добавлении пользователя в Human Resources.
