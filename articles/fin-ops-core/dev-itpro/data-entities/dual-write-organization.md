---
title: Организационная иерархия в Common Data Service
description: Эта тема описывает интеграцию организационных данных между приложениями Finance and Operations и Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9efc63c385c31a6d8848d016c1a8689460908dcc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769668"
---
# <a name="organization-hierarchy-in-common-data-service"></a>Организационная иерархия в Common Data Service

[!include [banner](../includes/banner.md)]

Поскольку Dynamics 365 Finance — это финансовая система, *организация* является основной концепцией, а настройка системы начинается с конфигурации организационной иерархии. Финансы бизнеса затем могут отслеживаться на уровне организации, а также на любом уровне в иерархии организации.

Хотя Common Data Service не имеет понятия иерархии организации, она имеет несколько отдельных концепций, таких как общий доход от продаж. В рамках интеграции Common Data Service структура данных иерархии организации добавляется в Common Data Service.

## <a name="data-flow"></a>Поток данных

Бизнес-экосистема, состоящая из приложений Finance and Operations и Common Data Service, будет по-прежнему иметь организационную иерархию. Эта иерархия организации построена на приложениях Finance and Operations, но она доступна Common Data Service для целей информации и расширения. На следующей иллюстрации показана информация об иерархии организации, которая доступна в Common Data Service в качестве одностороннего потока данных из приложений Finance and Operations в Common Data Service.

![Изображение архитектуры](media/dual-write-data-flow.png)

## <a name="templates"></a>Шаблоны

Сопоставления сущности организационной иерархии доступны для односторонней синхронизации данных из приложений Finance and Operations в Common Data Service.

## <a name="templates"></a>Шаблоны

Информация о продукте содержит все сведения, имеющие отношение к продукту и его определению, такие как аналитики продукта или аналитики отслеживания и хранения. Как показано в следующей таблице, для синхронизации продуктов и связанных сведений создается коллекция сопоставлений объектов.

Finance and Operations | Другие приложения Dynamics 365 | Описание
-----------------------|--------------------------------|---
Цели организационной иерархии | msdyn_internalorganizationhierarchypurposes | Этот шаблон обеспечивает одностороннюю синхронизацию объекта цели организационной иерархии.
Тип организационной иерархии | msdyn_internalorganizationhierarchytypes | Этот шаблон обеспечивает одностороннюю синхронизацию объекта типа организационной иерархии.
Организационная иерархия — опубликованная | msdyn_internalorganizationhierarchies | Этот шаблон обеспечивает одностороннюю синхронизацию объекта опубликованной организационной иерархии.
Операционная единица | msdyn_internalorganizations | 
Юридические лица | msdyn_internalorganizations | 
Юридические лица | cdm_companies | Обеспечивает двунаправленную синхронизацию информации о юридическом лице (компании).


[!include [banner](../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](dual-write/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](dual-write/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](dual-write/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a>Внутренняя организация

Сведения о внутренней организации в Common Data Service поступают из двух объектов, **операционная единица** и **юридические лица**.

[!include [Operating unit](dual-write/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](dual-write/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](dual-write/LegalEntities-Companies.md)]

