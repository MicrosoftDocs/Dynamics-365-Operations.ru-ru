---
title: Варианты отчетности
description: В этой статье описан порядок решения проблемы, когда клиент хочет настроить отчеты или создать новые отчеты Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5d47524033bf39a1db6b22b28ee3fcc65348829c
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431023"
---
# <a name="reporting-options"></a>Варианты отчетности

**Сведения среды**

Эта проблема относится ко всем средам.

**Симптом**

Клиент хочет настроить отчеты или создать новые отчеты Microsoft Dynamics 365 Human Resources.

**Расход**

Пользователь не может настраивать внедренные отчеты Microsoft Power BI.

**Решение**

- Данные Human Resources, которые передаются в Common Data Service, могут передаваться через соединитель Power Apps Common Data Service в Power BI Desktop. Обратите внимание, что Common Data Service содержит подмножество данных Human Resources. Дополнительные сведения о Power BI и панелях мониторинга см. в разделе [Создание отчетов и панелей мониторинга Power BI с помощью Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- Электронная отчетность (ER) доступна для некоторых отчетов в Human Resources. Настройки, управляемые клиентом, можно сделать через параметры конфигурации электронной отчетности.
- Данные можно экспортировать в Microsoft Excel или Microsoft Word с использованием различных информационных объектов, предоставляемых Human Resources с помощью интеграции с Microsoft Office.

**Долгосрочное решение**

Будут доступны дополнительные параметры Power BI, и дополнительные данные и объекты будут входить в Common Data Service.
