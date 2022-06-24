---
title: Варианты отчетности
description: В этой статье объясняется, как настраивать под себя отчеты Microsoft Dynamics 365 Human Resources и создавать новые отчеты.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 421883d314fb27b4592e9be0455946ab3730fb1a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856348"
---
# <a name="reporting-options"></a>Варианты отчетности


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



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
