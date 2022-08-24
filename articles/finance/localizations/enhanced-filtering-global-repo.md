---
title: Улучшенная фильтрация RCS в RCS/глобальном репозитории
description: В этой статье описываются расширенные возможности фильтрации для глобального репозитория RCS, которые были усовершенствованы и теперь включают дополнительные фильтры.
author: kfend
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace
ms.openlocfilehash: e0408d0561c0cfead8781b9f49fdb84d5caf179a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274523"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>Параметры расширенной фильтрации RCS для поиска конфигураций в RCS/глобальном репозитории

[!include [banner](../includes/banner.md)]

В этой статье описываются расширенные возможности фильтрации для глобального репозитория службы Regulatory Configuration Services (RCS), которые были усовершенствованы и теперь включают возможность фильтрации по следующим критериям: 
- **Страна/регион** — на основе кодов ISO для стран  
- Типы **Теги** для:
  - Функциональная область
  - Область компонентов
  - Отрасль 
  - Бизнес-документ 

Для упрощения поиска отдельных или связанных конфигураций можно применять фильтры по отдельности или в группе. Например, чтобы найти один тип настраиваемых деловых документов, связанных с накладными поставщика, можно применить фильтр **Тип бизнес-документа** для поиска документа этого типа. 

[![Раздел фильтров для глобального репозитория.](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

Для дальнейшего уточнения поиска можно выбрать тип документа, например "накладная поставщика", и щелкнуть **Применить фильтр**. В следующем примере показаны результаты фильтрации по параметры **Тип бизнес-документов** с добавленным типом документа. 

[![Примененный фильтр и импорт для типа бизнес-документа.](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Отфильтрованные результаты могут быть импортированы в репозиторий RCS пользователей или в среду Dynamics 365 Finance по отдельности или в виде набора. Для этого выберите группу конфигураций и нажмите **Импорт**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
