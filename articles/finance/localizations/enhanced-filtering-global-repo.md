---
title: Улучшенная фильтрация в RCS/глобальном репозитории
description: В этой теме описываются расширенные возможности фильтрации для глобального репозитория RCS, которые были усовершенствованы для включения дополнительных фильтров.
author: JaneA07
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ed5a217b8844bfc76d53370ab4c4c339f5bece36
ms.sourcegitcommit: 0dcdfedec7125562f6b33deb009a3e044a1243eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "3099875"
---
# <a name="enhanced-filtering-options-for-finding-configurations-in-the-global-repository"></a>Расширенные параметры фильтрации для поиска конфигураций в глобальном репозитории

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

В этой теме описываются расширенные возможности фильтрации для глобального репозитория службы Regulatory Configuration Service (RCS), которые были усовершенствованы для включения дополнительных фильтров. 
- **Страна/регион** — на основе кодов ISO для стран  
- **Теги** — для функциональной области/области функциональных возможностей; отрасль; тип бизнес-документа 

Можно применять фильтры по отдельности или в группах для поиска отдельных или соответствующих конфигураций. Например, для поиска всех настраиваемых деловых документов, относящихся к накладным поставщиков, можно применить фильтр **Типы бизнес-документов**. 

Можно уточнить поиск, выбрав код страны и нажав **Применить фильтр**.  

[![Раздел фильтров для глобального репозитория](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

В следующем примере показаны результаты фильтрации по параметры **Тип бизнес-документов**. 

[![Примененный фильтр и импорт для типа бизнес-документа](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Отфильтрованные результаты могут импортироваться в RCS или среду Dynamics 365 Finance пользователей, отдельно или в виде набора (путем выбора группы конфигураций), щелчком кнопки **Импорт**.






