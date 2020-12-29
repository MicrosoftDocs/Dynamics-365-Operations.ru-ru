---
title: Улучшенная фильтрация RCS в RCS/глобальном репозитории
description: В этой теме описываются расширенные возможности фильтрации для глобального репозитория RCS, которые были усовершенствованы для включения дополнительных фильтров.
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
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
ms.openlocfilehash: 1913b661c46af5e34da1a2939cb2a5d5b4e46411
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447077"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>Параметры расширенной фильтрации RCS для поиска конфигураций в RCS/глобальном репозитории

[!include [banner](../includes/banner.md)]

В этой теме описываются расширенные возможности фильтрации для глобального репозитория службы Regulatory Configuration Service (RCS), которые были усовершенствованы для включения возможности фильтрации по следующим критериям: 
- **Страна/регион** — на основе кодов ISO для стран  
- Типы **Теги** для:
  - Функциональная область
  - Область компонентов
  - Отрасль 
  - Бизнес-документ 

Для упрощения поиска отдельных или связанных конфигураций можно применять фильтры по отдельности или в группе. Например, чтобы найти один тип настраиваемых деловых документов, связанных с накладными поставщика, можно применить фильтр **Тип бизнес-документа** для поиска документа этого типа. 

[![Раздел фильтров для глобального репозитория](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

Для дальнейшего уточнения поиска можно выбрать тип документа, например "накладная поставщика", и щелкнуть **Применить фильтр**. В следующем примере показаны результаты фильтрации по параметры **Тип бизнес-документов** с добавленным типом документа. 

[![Примененный фильтр и импорт для типа бизнес-документа](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Отфильтрованные результаты могут импортироваться в репозиторий RCS пользователей или в среду Dynamics 365 Finance отдельно или в виде набора. Для этого выберите группу конфигураций и нажмите **Импорт**.
