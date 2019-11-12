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
ms.openlocfilehash: 9a12ab249129dce24cdca5e29d737fa9f68c0eac
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572457"
---
# <a name="organization-hierarchy-in-common-data-service"></a>Организационная иерархия в Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Поскольку Dynamics 365 Finance — это финансовая система, *организация* является основной концепцией, а настройка системы начинается с конфигурации организационной иерархии. Финансы бизнеса затем могут отслеживаться на уровне организации, а также на любом уровне в иерархии организации.

Хотя Common Data Service не имеет понятия иерархии организации, она имеет несколько отдельных концепций, таких как общий доход от продаж. В рамках интеграции Common Data Service структура данных иерархии организации добавляется в Common Data Service.

## <a name="data-flow"></a>Поток данных

Бизнес-экосистема, состоящая из приложений Finance and Operations и Common Data Service, будет по-прежнему иметь организационную иерархию. Эта иерархия организации построена на приложениях Finance and Operations, но она доступна Common Data Service для целей информации и расширения. На следующей иллюстрации показана информация об иерархии организации, которая доступна в Common Data Service в качестве одностороннего потока данных из приложений Finance and Operations в Common Data Service.

![Изображение архитектуры](media/dual-write-data-flow.png)

## <a name="templates"></a>Шаблоны

Сопоставления сущности организационной иерархии доступны для односторонней синхронизации данных из приложений Finance and Operations в Common Data Service.

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a>Цель внутренней организационной иерархии

Этот шаблон обеспечивает одностороннюю синхронизацию объекта цели организационной иерархии из Finance and Operations в другие приложения Dynamics 365.

<!-- ![architecture image](media/dual-write-purpose.png) -->

Поле источника | Тип сопоставления | Поле назначения
---|---|---
HIERARCHYTYPE | \> | msdyn\_hierarchypurposetypename
HIERARCHYTYPE | \> | msdyn\_hierarchytype.msdyn\_name
HIERARCHYPURPOSE | \>\> | msdyn\_hierarchypurpose
IMMUTABLE | \>\> | msdyn\_immutable
SETASDEFAULT | \>\> | msdyn\_setasdefault

## <a name="internal-organization-hierarchy-type"></a>Тип внутренней организационной иерархии

Этот шаблон обеспечивает одностороннюю синхронизацию объекта типа организационной иерархии из Finance and Operations в другие приложения Dynamics 365.

<!-- ![architecture image](media/dual-write-type.png) -->

Поле источника | Тип сопоставления | Поле назначения
---|---|---
НАИМЕНОВАНИЕ | \> | msdyn\_name

## <a name="internal-organization-hierarchy"></a>Внутренняя организационная иерархия

Этот шаблон обеспечивает одностороннюю синхронизацию объекта опубликованной организационной иерархии из Finance and Operations в другие приложения Dynamics 365.

<!-- ![architecture image](media/dual-write-organization.png) -->

Поле источника | Тип сопоставления | Поле назначения
---|---|---
VALIDTO | \> | msdyn\_validto
VALIDFROM | \> | msdyn\_validfrom
HIERARCHYTYPE | \> | msdyn\_hierarchytypename
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentpartyid
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childpartyid
HIERARCHYTYPE | \> | msdyn\_hierarchytypeid.msdyn\_name
CHILDORGANIZATIONPARTYNUMBER | \> | msdyn\_childid.msdyn\_partynumber
PARENTORGANIZATIONPARTYNUMBER | \> | msdyn\_parentid.msdyn\_partynumber

## <a name="internal-organization"></a>Внутренняя организация

Сведения о внутренней организации в Common Data Service поступают из двух объектов, **операционная единица** и **юридические лица**.

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a>Операционная единица

Поле источника | Тип сопоставления | Поле назначения
---|---|---
LANGUAGEID | \> | msdyn\_languageid
NAMEALIAS | \> | msdyn\_namealias
НАИМЕНОВАНИЕ | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
OPERATINGUNITTYPE | \>\> | msdyn\_type

### <a name="legal-entity"></a>Информация о компании

Поле источника | Тип сопоставления | Поле назначения
---|---|---
NAMEALIAS | \> | msdyn\_namealias
LANGUAGEID | \> | msdyn\_languageid
НАИМЕНОВАНИЕ | \> | msdyn\_name
PARTYNUMBER | \> | msdyn\_partynumber
нет | \>\> | msdyn\_type
LEGALENTITYID | \> | msdyn\_companycode

## <a name="company"></a>Организация

Обеспечивает двунаправленную синхронизацию информации о юридическом лице (компании) между Finance and Operations и другими приложениями Dynamics 365.

<!-- ![architecture image](media/dual-write-company.png) -->

Поле источника | Тип сопоставления | Поле назначения
---|---|---
НАИМЕНОВАНИЕ | = | cdm\_name
LEGALENTITYID | = | cdm\_companycode
