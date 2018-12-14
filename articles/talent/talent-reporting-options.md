---
title: "Параметры отчетности в Talent"
description: "В этом разделе описан порядок решения проблемы, когда клиент хочет настроить отчеты или создать новые отчеты Microsoft Dynamics 365 for Talent."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.contentlocale: ru-ru
ms.lasthandoff: 12/04/2018

---

# <a name="reporting-options-in-talent"></a>Параметры отчетности в Talent

[!include [banner](includes/banner.md)]

**Сведения среды**

Эта проблема относится ко всем средам.

**Симптом**

Клиент хочет настроить отчеты или создать новые отчеты Microsoft Dynamics 365 for Talent.

**Расход**

Пользователь не может настраивать внедренные отчеты Microsoft Power BI.

**Решение**

- Данные Core HR, которые передаются в Common Data Service для приложений, могут передаваться через соединитель PowerApps CDS в Power BI Desktop. Обратите внимание, что Common Data Service для приложений содержит подмножество данных Core HR. Дополнительные сведения о Power BI и панелях мониторинга см. в разделе [Создание отчетов и панелей мониторинга Power BI с помощью Common Data Service PowerApps](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).
- Электронная отчетность (ER) доступна для некоторых отчетов в Talent. Настройки, управляемые клиентом, можно сделать через параметры конфигурации электронной отчетности.
- Данные можно экспортировать в Microsoft Excel или Microsoft Word с использованием различных информационных объектов, предоставляемых Talent с помощью интеграции с Microsoft Office.

**Долгосрочное решение**

Будут доступны дополнительные параметры Power BI, и дополнительные данные и объекты будут входить в Common Data Service для приложений.

