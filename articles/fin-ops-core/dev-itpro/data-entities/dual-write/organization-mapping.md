---
title: Организационная иерархия в Dataverse
description: Эта тема описывает интеграцию организационных данных между приложениями Finance and Operations и Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 77625e6e80bfa45add6839df89d9aae27e41d456
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355306"
---
# <a name="organization-hierarchy-in-dataverse"></a>Организационная иерархия в Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Поскольку Dynamics 365 Finance — это финансовая система, *организация* является основной концепцией, а настройка системы начинается с конфигурации организационной иерархии. Финансы бизнеса затем могут отслеживаться на уровне организации, а также на любом уровне в иерархии организации.

Хотя Dataverse не имеет понятия иерархии организации, она имеет несколько отдельных концепций, таких как общий доход от продаж. В рамках интеграции Dataverse структура данных иерархии организации добавляется в Dataverse.

## <a name="data-flow"></a>Поток данных

Бизнес-экосистема, состоящая из приложений Finance and Operations и Dataverse, будет по-прежнему иметь организационную иерархию. Эта организационная иерархия построена на приложениях Finance and Operations, но она доступна в Dataverse для целей информации и расширения. На следующей иллюстрации показана информация об иерархии организации, которая доступна в Dataverse в качестве одностороннего потока данных из приложений Finance and Operations в Dataverse.

![Изображение архитектуры.](media/dual-write-data-flow.png)

Сопоставления таблицы организационной иерархии доступны для односторонней синхронизации данных из приложений Finance and Operations в Dataverse.

## <a name="templates"></a>Шаблоны

Информация о продукте содержит все сведения, имеющие отношение к продукту и его определению, такие как аналитики продукта или аналитики отслеживания и хранения. Как показано в следующей таблице, для синхронизации продуктов и связанных сведений создается коллекция сопоставлений таблиц.

Приложения Finance and Operations | Другие приложения Dynamics 365 | описание
-----------------------|--------------------------------|---
Цели организационной иерархии | msdyn_internalorganizationhierarchypurposes | Этот шаблон обеспечивает одностороннюю синхронизацию таблицы цели организационной иерархии.
Тип организационной иерархии | msdyn_internalorganizationhierarchytypes | Этот шаблон обеспечивает одностороннюю синхронизацию таблицы типа организационной иерархии.
Организационная иерархия — опубликованная версия | msdyn_internalorganizationhierarchies | Этот шаблон обеспечивает одностороннюю синхронизацию таблицы опубликованной организационной иерархии.
Операционная единица | msdyn_internalorganizations |
Юридические лица | msdyn_internalorganizations |
Юридические лица | cdm_companies | Обеспечивает двунаправленную синхронизацию информации о юридическом лице (компании).

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>Внутренняя организация

Сведения о внутренней организации в Dataverse поступают из двух таблиц, **операционная единица** и **юридические лица**.

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]