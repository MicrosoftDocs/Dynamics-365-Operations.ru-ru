---
title: Пользователь может получить доступ к Core HR, но не к приложению Onboard или Attract
description: В этом разделе объясняется, как решить проблему, когда пользователь имеет доступ к Microsoft Dynamics 365 for Talent Core HR, но не имеет доступа к приложению Attract или Onboard.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2e5d0b1bf993aec89c7d2c6d4916732f5824310d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "305984"
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

Сведения см. в разделе "Предоставление доступа к среде" в статье [Подготовка Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).

**Долгосрочное решение**

Майкрософт планирует автоматическое назначение соответствующих прав на приложения Onboard и Attract при добавлении пользователя в Core HR.
