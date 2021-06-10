---
title: Варианты отчетности
description: В этой статье описан порядок решения проблемы, когда клиент хочет настроить отчеты или создать новые отчеты Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 64a03724d81745373d028d76a8cc64aab66efdbb
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053307"
---
# <a name="reporting-options"></a>Варианты отчетности

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Сведения среды**

Эта проблема относится ко всем средам.

**Симптом**

Клиент хочет настроить отчеты или создать новые отчеты Microsoft Dynamics 365 Human Resources.

**Расход**

Пользователь не может настраивать внедренные отчеты Microsoft Power BI.

**Решение**

- Данные Human Resources, которые передаются в Dataverse, могут передаваться через соединитель Power Apps Dataverse в Power BI Desktop. Обратите внимание, что Dataverse содержит подмножество данных Human Resources. Дополнительные сведения о Power BI и панелях мониторинга см. в разделе [Создание отчетов и панелей мониторинга Power BI с помощью Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- Электронная отчетность (ER) доступна для некоторых отчетов в Human Resources. Настройки, управляемые клиентом, можно сделать через параметры конфигурации электронной отчетности.
- Данные можно экспортировать в Microsoft Excel или Microsoft Word с использованием различных информационных объектов, предоставляемых Human Resources с помощью интеграции с Microsoft Office.

**Долгосрочное решение**

Будут доступны дополнительные параметры Power BI, и дополнительные данные и объекты будут входить в Dataverse.


[!INCLUDE[footer-include](../includes/footer-banner.md)]